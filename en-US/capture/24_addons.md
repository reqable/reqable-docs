# Addons API

:::info Source Code

https://github.com/reqable/python-scripting-api

:::

API documentation for the Reqable scripting.

:::tip

- Starting from v2.28.0, the `Capture` prefix is ​​removed from all class names.
- Variable names in italics are read-only, and in bold they can be overwritten.

:::

## Context {#api-context}

|   Variable  |  Type |  Description  |
|  ----  | ----  | ----  |
|*url*|str|Request url, read-only.|
|*scheme*|str|URL scheme, http or https, read-only.|
|*host*|str|Host, read-only.|
|*port*|int|Port number, read-only.|
|*cid*|int|Connection ID, read-only.|
|*ctime*|int|TCP connection establishment timestamp, in milliseconds, read-only.|
|*sid*|int|HTTP session ID, read-only.|
|*stime*|int|HTTP session start timestamp, in milliseconds, read-only.|
|*uid*|str|The unique identifier of an HTTP session, consisting of `ctime` + `cid` + `sid`.|
|*app*|[App](#api-app)|App/Process information.|
|highlight|[Highlight](#api-highlight)|Set request highlighting in traffic list, added on v2.28.0.|
|**env**|dict|A collection of variables for the global environment and currently actived custom environment.|
|**shared**|-|A special variable used to share data between `onRequest` and `onResponse`, which can be auto-serializable variables such as str, int, list and dict.|

Code example:
```python
def onRequest(context, request):
  # Print url, for example: https://reqable.com/
  print(context.url)
  # Print scheme, for example: https
  print(context.scheme)
  # Print host, for example: reqable.com
  print(context.host)
  # Print port number, for example: 443
  print(context.port)
  # Print connection ID, for example: 1
  print(context.cid)
  # Print TCP connection timestamp, for example: 1686711219444
  print(context.ctime)
  # Print HTTP session ID, for example: 1
  print(context.sid)
  # Print HTTP session start timestamp, for example: 1686711224132
  print(context.stime)

  # Get an environment variable
  print(context.env['foo'])
  print(context.env['$timestamp'])

  # Write an environment variable
  # The currently activated custom environment is written first, and if there is no activated environment, the global environment is written.
  context.env['foo'] = 'bar'

  # Set shared value
  context.shared = 'Hello'

  # Done
  return request

def onResponse(context, response):
  #  Print shared value, output: Hello
  print(context.shared)
  return response
```

## HttpRequest {#api-request}

|   Variable  |  Type |  Description  |
|  ----  | ----  | ----  |
|**method**|str|HTTP request method.|
|**path**|str|HTTP request path. Note that the query part is not included.|
|*protocol*|str|HTTP protocol version of the request, read-only.|
|**queries**|[HttpQueries](#api-queries)|List of request query parameters.|
|**headers**|[HttpHeaders](#api-headers)|List of request headers.|
|**body**|[HttpBody](#api-body)|Request body.|
|**trailers**|[HttpHeaders](#api-headers)|List of request trailers, see chunked trailers of HTTP1 or trailers of HTTP2.|
|*contentType*|str or None|Request type (that is, the value of Content-Type in headers), read-only.|
|*mime*|str or None|Request MIME type, such as application/json, read-only.|

Code example:
```python
def onRequest(context, request):
  # Print method, for example: POST
  print(request.method)
  # Print path, for example: /foo
  print(request.path)
  # Print query parameters, for example: [('foo', 'bar'), ('hello', 'world')]
  print(request.queries)
  # Print headers, for example: ['host: reqable.com', 'content-length: 6', 'content-type: text/plain']
  print(request.headers)
  # Print body payload, for example: {"foo":"bar"}
  print(request.body)

  # Update request method
  request.method = 'GET'
  # Update request path
  request.path = '/bar'

  # Update request parameters, more APIs please refer to `HttpQueries` below.
  request.queries['foo'] = 'bar'
  # Assign request parameters
  request.queries = 'foo=bar&hello=world&abc=123'
  request.queries = {
    'foo': 'bar',
    'hello': 'world',
    'abc': '123'
  }
  # Delete specified request parameters
  request.queries.remove('foo')

  # Update request headers, more APIs please refer to `HttpHeaders` below.
  request.headers['content-type'] = 'application/json'
  # Assign request headers
  request.headers = [
    'content-type: application/json',
    'foo: bar'
  ]
  # Delete specified request headers
  request.headers.remove('foo')

  # Set a text to body
  request.body = 'Hello World'
  # Set a dictionary to body, it will be automatically converted to JSON
  request.body = {
    'foo': 'bar',
    'abc': 123
  }
  # Set a binary data to body
  request.body = b'\x01\x02\x03\x04'
  # Set a file path to body
  request.body.file('/User/Reqable/Desktop/test.png')

  # JSON body is converted into a dictionary
  request.body.jsonify()
  # Then manipulate the dictionary to modify the Body
  request.body['foo'] = 'bar'
  request.body['error'] = {
    'code': 1000,
    'message': 'Runtime Error'
  }

  # Done
  return request
```

## HttpResponse {#api-response}

|   Variable  |  Type |  Description  |
|  ----  | ----  | ----  |
|*request*|[HttpRequest](#api-request)|The request of response, read-only.|
|**code**|int|Response status code.|
|*message*|str|Response status message, read-only. Note: In the HTTP2 protocol, the value is empty; this value will be automatically updated after the status code is changed.|
|*protocol*|str|The HTTP protocol version of the response, read-only.|
|**headers**|[HttpHeaders](#api-headers)|List of response headers.|
|**body**|[HttpBody](#api-body)|Response body.|
|**trailers**|[HttpHeaders](#api-headers)|List of response trailers, see chunked trailers for HTTP1 or trailers for HTTP2.|
|*contentType*|str or None|Response type (that is, the value of Content-Type in headers), read-only.|
|*mime*|str or None|Response MIME type, such as application/json, read-only.|

Code example:
```python
def onResponse(context, response):
  # Print request information, for more APIs, please refer to `HttpRequest` above
  print(response.request)
  # Print response status code, for example: 200
  print(response.code)
  # Print response status message, for example: OK
  print(response.message)
  # Print response headers, for example: ['server: Netlify', 'content-length: 6', 'content-type: text/plain']
  print(response.headers)
  # Print response body payload, for example: {"foo":"bar"}
  print(response.body)

  # Update status code
  response.code = 400

  # More examples refer to `onRequest` above, exactly the same.

  # Done
  return response
```

## HttpQueries {#api-queries}

|   Function  |  Parameters |  Return |  Description  |
|  ----  | ---- | ----  | ----  |
|len||int|Returns the count of query parameters.|
|iter|||Iterate the query parameters.|
|add|str, str||Add a new query, the parameters are `name` and `value`.|
|remove|str||Delete the query with the specified name. Note: If there are more than one with the same name, all will be removed.|
|clear|||Delete all queries.|
|concat|bool|str|Returns the concatenated complete query string.|
|index|str|int|Query the index of the query parameter of the specified name in the list, and only return the first index that matches the name.|
|indexes|str|list|Query the index of the query parameter of the specified name in the list, and return a list of all indexes matching the name.|
|__getitem__|str|str|Get the query value of the specified name. Note: If there are more than one with the same name, it will return the first one; if it does not exist, it will return `None`.|
|__getitem__|int|tuple|Get query by index.|
|__setitem__|str, str||Update or add a query. If there is a query with the specified name, update its value, otherwise add a new query parameter.|

Code example:
```python
def onRequest(context, request):
  # Print the count of query parameters
  print(len(request.queries))
  # Iterate the query parameters
  for query in request.queries:
    print(query)

  # Add a new query
  request.queries.add('foo', 'bar')
  # Remove the query named `foo`
  request.queries.remove('foo')
  # Remove all query parameters
  request.queries.clear()
  # Update the query parameter, if it does not exist, it will be added automatically.
  request.queries['foo'] = 'bar'

  # Print the query value, for example: bar
  print(request.queries['foo'])
  # Print the query name and value at the specified index position, for example: (foo, bar)
  print(request.queries[0])
  # Print the concatenated query string, such as: foo=bar&hello=world
  print(request.queries.concat())
  # Print the concatenated query string(URL encoded).
  print(request.queries.concat(encode=True))

  # Done
  return request
```

## HttpHeaders {#api-headers}

|   Function  |  Parameters |  Return |  Description  |
|  ----  | ---- | ----  | ----  |
|len||int|Returns the count of headers.|
|iter|||Iterate the headers.|
|add|str, str||Add a new header, the parameters are `name` and `value`.|
|remove|str||Delete the header with the specified name. Note: If there are more than one with the same name, all will be removed.|
|clear|||Delete all headers.|
|index|str|int|Query the index of the header of the specified name in the list, and only return the first index that matches the name.|
|indexes|str|list|Query the index of the header of the specified name in the list, and return a list of all indexes matching the name.|
|__getitem__|str|str|Get the header value of the specified name. Note: If there are more than one with the same name, it will return the first one; if it does not exist, it will return `None`.|
|__getitem__|int|str|Get header by index.|
|__setitem__|str, str||Update or add a header. If there is a header with the specified name, update its value, otherwise add a new header.|

Code example:
```python
def onRequest(context, request):
  # Print the count of headers
  print(len(request.headers))
  # Iterate the header list
  for header in request.headers:
    print(header)
  # Add a new header
  request.headers.add('foo', 'bar')
  # Remove the header named `foo`
  request.headers.remove('foo')
  # Remove all headers
  request.headers.clear()
  # Update the header, if it does not exist, it will be added automatically.
  request.headers['foo'] = 'bar'
  # Print the header value, for example: bar
  print(request.headers['foo'])
  # Print the header at the specified index position, for example: `foo: bar`
  print(request.headers[0])
  # Done
  return request
```

## HttpBody {#api-body}

|   Variable  |  Type |  Description  |
|  ----  | ----  | ----  |
|*isNone*|bool|Determine whether it is an empty Body. For this type, payload is `None`.|
|*isText*|bool|Determine whether it is a string Body. For this type, the payload is `str`.|
|*isBinary*|bool|Determine whether it is a binary Body. For this type, the payload is `bytes`.|
|*isMultipart*|bool|Determine whether it is a form Body. For this type, the payload is a list of [HttpMultipartBody](#api-multipart-body).|
|*type*|int|Returns the type of Body. 0 means none, 1 means text, 2 means binary, 3 means form.|
|*payload*|Polymorphic types, refer to the description above.|Body payload.|

```python
def onRequest(context, request):
  # Judging body type
  print(request.body.type)
  if request.body.isNone:
    print('Http body is none')
  elif request.body.isText:
    print('Http body is text')
  elif request.body.isBinary:
    print('Http body is binary')
  elif request.body.isMultipart:
    print('Http body is multipart')

  # Print body type value
  print(request.body.type)
  # Print body payload
  print(request.body.payload)
```

|   Function  |  Parameters |  Return  |  Description  |
|  ----  | ---- | ----  | ----  |
|none|||Set `None` to body.|
|text|str||Set a text value to body.|
|textFromFile|str||Set a file content(text) to body.|
|binary|str or bytes||Set binary data to body.|
|file|str||Set the file content(binary) to body.|
|multiparts|list||Set to forms, the parameter is a list of [HttpMultipartBody](#api-multipart-body).|
|writeFile|str||Write body payload to a file. Note: form body is not supported.|

Code example:
```python
def onRequest(context, request):
  # Set `None` to body.
  request.body.none()
  # Set `foobar`` to body.
  request.body.text('foobar')
  # Set the file content to body, body type is text.
  request.body.textFromFile('/User/Reqable/Desktop/body.json')
  # Set bytes to body
  request.body.binary(b'\x01\x02\x03\x04')
  # Set the file content to body, body type is binary.
  request.body.binary('~/Desktop/body.json')
  # Set the forms to body.
  request.body.multiparts([
    HttpMultipartBody.text('Hi World'),
    HttpMultipartBody.file('data/body_binary.bin')
  ])

  # Write body payload to the file.
  request.body.writeFile('/User/Reqable/Desktop/body.json')

  # Done
  return request
```

#### HttpMultipartBody {#api-multipart-body}

HttpMultipartBody inherits from [HttpBody](#api-body), with an additional headers field.

|   Variable  |  Type |  Description  |
|  ----  | ----  | ----  |
|**headers**|[HttpHeaders](#api-headers)|List of headers in the part.|
|**name**|str|Part name.|
|**filename**|str|Part file name.|

Code example:
```python
def onRequest(context, request):
  # Iterate parts
  for part in request.body:
    print(f'name {part.name}')
    print(f'filename {part.filename}')
    print(f'value {part}')

  # Update parts
  request.body[0] = HttpMultipartBody.text('Hi World')
  request.body[0] = HttpMultipartBody.text('Hi World', name='reqable')
  request.body[0] = HttpMultipartBody.file('data/body_binary.bin')
  request.body[0] = HttpMultipartBody.file('data/body_binary.bin', name='reqable', filename='test.png')

  # Done
  return request
```

:::caution

If you change the non-form type to form type, you must modify the headers and set boundary at the same time!

:::

## App {#api-app}

|   Variable  |  Type |  Description  |
|  ----  | ----  | ----  |
|*name*|str|Name of the app/process.|
|*id*|str|App unique id, such as `bundleId` for mac app, `packageName` for android app. Return None if not detected.|
|*path*|str|The app installed path.|

Code example:
```python
def onRequest(context, response):
  # Print app information
  print(context.app.name)
  print(context.app.id)
  print(context.app.path)
  # Done
  return request
```

## Highlight {#api-highlight}

|   Enum  |  Description  |
|  ----  | ----  |
|*none*| No highlight |
|*red*| Red highlight |
|*yellow*| Yellow highlight |
|*green*| Green highlight |
|*blue*| Blue highlight |
|*teal*| Teal highlight |
|*strikethrough*| Strike-through highlight |

Code example:
```python
def onRequest(context, response):
  # Set request read highlight
  context.highlight = Highlight.red
  # Done
  return request
```

## Example 1

Below is an example of modifying JSON response data.

Suppose the response data is in the following format:
```json
{
  "code": 10000,
  "message": "ok",
  "content": {
    "version": "1.0.0",
    "platform": "windows"
  }
}
```
We need to change the value of `version` to `2.0.0`.

```python
from reqable import *

def onRequest(context, request):
  # Done
  return request

def onResponse(context, response):
  # Jsonify the response body
  response.body.jsonify()
  # Modify the version value in the dictionary
  response.body['content']['version'] = '2.0.0'
  # Done
  return response
```

## Example 2

The following is an example of automatically signing request parameters with MD5.

```python
from reqable import *
import hashlib

def onRequest(context, request):
  # Sort the query list
  queries = sorted(request.queries)
  # Concat the query parameters
  text = queries.concat()
  # Sign using the md5 algorithm
  algorithm = hashlib.md5()
  algorithm.update(text.encode(encoding='UTF-8'))
  signature = algorithm.hexdigest()
  # The signature is added to the request header
  request.headers['signature'] = signature
  # Done
  return request

def onResponse(context, response):
  # Done
  return response
```

## Example 3

Below is an example script that automatically saves images.

```python
from reqable import *
from mimetypes import guess_extension
import datetime
import os

def onRequest(context, request):
  return request

def onResponse(context, response):
  # Check the Mime type, if it is not an image type, it will be skipped and not processed
  mime = response.mime
  if mime == None:
    return response

  maintype, subtype = mime.split('/')
  if not maintype == 'image':
    return response

  # Save the image to the directory, the file name is timestamp, and the suffix is derived according to the mime type
  dir = '/Users/megatronking/Downloads/reqable/'
  os.makedirs(dir, exist_ok=True)
  name = datetime.datetime.now().strftime("%H%M%S%f")
  ext = guess_extension(mime)
  image = os.path.join(dir, name + ext)

  # Write body payload to file
  print(f'Saving image {image}')
  response.body.writeFile(image)

  # Done
  return response
```