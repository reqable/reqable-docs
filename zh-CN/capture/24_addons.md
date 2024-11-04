# 脚本API

:::info 源码

https://github.com/reqable/python-scripting-api

:::

脚本框架中涉及的python类的API文档说明。

:::tip

- 从v2.28.0版本开始，所有类名移除了`Capture`前缀。
- 变量名斜体表示只读，粗体表示可覆写。

:::

## Context {#api-context}

|   变量  |  类型 |  说明  |
|  ----  | ----  | ----  |
|*url*|str|请求url，只读。|
|*scheme*|str|请求标志符，值为http或https，只读。|
|*host*|str|域名，只读。|
|*port*|int|端口号，只读。|
|*cid*|int|TCP连接ID，只读。|
|*ctime*|int|TCP连接开始时间戳，单位毫秒，只读。|
|*sid*|int|HTTP会话ID，只读。|
|*stime*|int|HTTP会话开始时间戳，单位毫秒，只读。|
|*uid*|str|HTTP会话的唯一标志，由 `ctime` + `cid` + `sid` 组成。|
|**env**|dict|全局环境和当前已激活的自定义环境的变量合集。|
|*app*|[App](#api-app)|应用（进程）信息，未获取到为None。|
|highlight|[Highlight](#api-highlight)|设置调试列表高亮属性，v2.28.0版本新增。|
|**shared**|-|用于 `onRequest` 和 `onResponse` 之间共享数据的特殊变量，可以是str、int、list和dict等可自动序列化的变量。|

代码示例：
```python
def onRequest(context, request):
  # 打印url，例如：https://reqable.com/
  print(context.url)
  # 打印schema，例如：https
  print(context.scheme)
  # 打印host，例如：reqable.com
  print(context.host)
  # 打印port，例如：443
  print(context.port)
  # 打印TCP连接ID，例如：1
  print(context.cid)
  # 打印TCP连接开始时间，例如：1686711219444
  print(context.ctime)
  # 打印HTTP的会话ID，例如：1
  print(context.sid)
  # 打印HTTP的会话开始时间，例如：1686711224132
  print(context.stime)

  # 获取环境变量
  print(context.env['foo'])
  print(context.env['$timestamp'])

  # 写入环境变量（优先写入当前激活的自定义环境，没有激活环境则写入全局环境）
  context.env['foo'] = 'bar'

  # 设置请求红色高亮
  context.highlight = Highlight.red

  # 设置共享参数
  context.shared = 'Hello'

  # Done
  return request

def onResponse(context, response):
  #  打印共享参数，输出：Hello
  print(context.shared)
  return response
```

## HttpRequest {#api-request}

|   变量  |  类型 |  说明  |
|  ----  | ----  | ----  |
|**method**|str|请求方法。|
|**path**|str|请求路径，注意不包含query部分。|
|*protocol*|str|请求的HTTP协议版本，只读。|
|**queries**|[HttpQueries](#api-queries)|请求参数列表。|
|**headers**|[HttpHeaders](#api-headers)|请求头列表。|
|**body**|[HttpBody](#api-body)|请求体。|
|**trailers**|[HttpHeaders](#api-headers)|请求尾部列表，参见HTTP1的chunked trailers或者HTTP2的trailers。注意此功能待验证，暂时请勿使用。|
|*contentType*|str或None|请求类型（即headers中的Content-Type的值），只读。|
|*mime*|str或None|请求MIME类型，例如application/json，只读。|

代码示例：
```python
def onRequest(context, request):
  # 打印请求方法，例如：POST
  print(request.method)
  # 打印请求路径，例如：/foo
  print(request.path)
  # 打印请求参数列表，例如：[('foo', 'bar'), ('hello', 'world')]
  print(request.queries)
  # 打印请求头列表，例如：['host: reqable.com', 'content-length: 6', 'content-type: text/plain']
  print(request.headers)
  # 打印请求体，例如 {"foo":"bar"}
  print(request.body)

  # 修改请求方法
  request.method = 'GET'
  # 修改请求路径
  request.path = '/bar'

  # 修改请求参数，更多API请参考下文`HttpQueries`
  request.queries['foo'] = 'bar'
  # 直接赋值请求参数
  request.queries = 'foo=bar&hello=world&abc=123'
  request.queries = {
    'foo': 'bar',
    'hello': 'world',
    'abc': '123'
  }
  # 删除指定请求参数
  request.queries.remove('foo')

  # 修改请求头，更多API请参考下文`HttpHeaders`
  request.headers['content-type'] = 'application/json'
  # 直接赋值请求头
  request.headers = [
    'content-type: application/json',
    'foo: bar'
  ]
  # 删除指定请求头
  request.headers.remove('foo')

  # 将文本设置给Body
  request.body = 'Hello World'
  # 将字典设置给Body，会自动转成JSON
  request.body = {
    'foo': 'bar',
    'abc': 123
  }
  # 将二进制数据设置给Body
  request.body = b'\x01\x02\x03\x04'
  # 将本地文件设置给Body
  request.body.file('/User/Reqable/Desktop/test.png')

  # JSON类型的Body转成字典
  request.body.jsonify()
  # 然后操作字典来修改Body
  request.body['foo'] = 'bar'
  request.body['error'] = {
    'code': 1000,
    'message': 'Runtime Error'
  }

  # Done
  return request
```

## HttpResponse {#api-response}

|   变量  |  类型 |  说明  |
|  ----  | ----  | ----  |
|*request*|[HttpRequest](#api-request)|响应的请求信息，只读。|
|**code**|int|响应状态码。|
|*message*|str|响应状态信息，只读。注意：HTTP2协议中，值为空；此值在状态码修改后会自动更新。|
|*protocol*|str|响应的HTTP协议版本，只读。|
|**headers**|[HttpHeaders](#api-headers)|响应头列表。|
|**body**|[HttpBody](#api-body)|响应体。|
|**trailers**|[HttpHeaders](#api-headers)|响应尾部列表，参见HTTP1的chunked trailers或者HTTP2的trailers。注意此功能待验证，暂时请勿使用。|
|*contentType*|str或None|响应类型（即headers中的Content-Type的值），只读。|
|*mime*|str或None|响应MIME类型，例如application/json，只读。|

代码示例：
```python
def onResponse(context, response):
  # 打印请求信息，更多API请参考上文`HttpRequest`
  print(response.request)
  # 打印响应状态码，例如：200
  print(response.code)
  # 打印响应消息
  print(response.message)
  # 打印响应头列表，例如：['server: Netlify', 'content-length: 6', 'content-type: text/plain']
  print(response.headers)
  # 打印响应体，例如 {"foo":"bar"}
  print(response.body)

  # 修改响应状态码
  response.code = 400

  # 更多的示例参考上面的`onRequest`，完全一样。

  # Done
  return response
```

## HttpQueries {#api-queries}

|   函数  |  参数 |  返回 |  说明  |
|  ----  | ---- | ----  | ----  |
|len||int|返回query参数的个数。|
|iter|||支持迭代遍历全部的query参数。|
|add|str, str||新增一个query，参数为name和value。|
|remove|str||删除指定name的query。注意：如果有多个同名的，全部会移除。|
|clear|||清空所有query。|
|concat|bool|str|返回拼接好的完整query字符串。|
|index|str|int|查询指定name的query参数在列表中的索引，只返回第一个匹配name的索引。|
|indexes|str|list|查询指定name的query参数在列表中的索引，返回全部匹配name的索引列表。|
|getitem|str|str|获取指定name的query值。注意：如果有多个同名的，会返回第一个；如果不存在，则返回None。|
|getitem|int|tuple|按照索引获取query的名称和值。|
|setitem|str, str||更新或新增query。如果存在指定name的query，则更新它的值，否则添加一个新的query参数。|

代码示例：
```python
def onRequest(context, request):
  # 打印query参数个数
  print(len(request.queries))
  # 遍历query参数
  for query in request.queries:
    print(query)

  # 新增query参数
  request.queries.add('foo', 'bar')
  # 移除query参数
  request.queries.remove('foo')
  # 清空全部query参数
  request.queries.clear()
  # 更新query参数，如果不存在则自动新增
  request.queries['foo'] = 'bar'

  # 打印指定query参数值，例如bar
  print(request.queries['foo'])
  # 打印指定索引位置的query名称和值，例如(foo, bar)
  print(request.queries[0])
  # 打印拼接好的完整Query字符串，例如foo=bar&hello=world
  print(request.queries.concat())
  # 打印拼接好的完整Query字符串（urlencode参数值）
  print(request.queries.concat(encode=True))

  # Done
  return request
```

## HttpHeaders {#api-headers}

|   函数  |  参数 |  返回 |  说明  |
|  ----  | ---- | ----  | ----  |
|len||int|返回header的个数。|
|iter|||支持迭代遍历全部的header。|
|add|str, str||新增一个header，参数为name和value。|
|remove|str||删除指定name的header。注意：如果有多个同名的，全部会移除。|
|clear|||清空所有header。|
|index|str|int|查询指定name的header参数在列表中的索引，只返回第一个匹配name的索引。|
|indexes|str|list|查询指定name的header参数在列表中的索引，返回全部匹配name的索引列表。|
|getitem|str|str|获取指定name的header值。注意：如果有多个同名的，会返回第一个；如果不存在，则返回None。|
|getitem|int|str|按照索引获取header的名称和值。|
|setitem|str, str||更新或新增header。如果存在指定name的header，则更新它的值，否则添加一个新的header。|

代码示例：
```python
def onRequest(context, request):
  # 打印headers参数个数
  print(len(request.headers))
  # 遍历header
  for header in request.headers:
    print(header)
  # 新增header
  request.headers.add('foo', 'bar')
  # 移除header
  request.headers.remove('foo')
  # 清空全部header
  request.headers.clear()
  # 更新header，如果不存在则自动新增
  request.headers['foo'] = 'bar'
  # 打印指定header值，例如bar
  print(request.headers['foo'])
  # 打印指定索引位置的header名称和值，例如`foo: bar`
  print(request.headers[0])
  # Done
  return request
```

## HttpBody {#api-body}

|   变量  |  类型 |  说明  |
|  ----  | ----  | ----  |
|*isNone*|bool|判断是否是空Body。此类型时，payload为None。|
|*isText*|bool|判断是否是字符串Body。此类型时，payload为str。|
|*isBinary*|bool|判断是否是二进制Body。此类型时，payload为bytes。|
|*isMultipart*|bool|判断是否是Form Body。此类型时，payload为[HttpMultipartBody](#api-multipart-body)的列表。|
|*type*|int|返回Body的类型。0表示空，1表示字符串，2表示二进制，3表示Form。|
|*payload*|多态类型，参照上方说明。|Body的数据。|

```python
def onRequest(context, request):
  # 判断body类型
  print(request.body.type)
  if request.body.isNone:
    print('Http body is none')
  elif request.body.isText:
    print('Http body is text')
  elif request.body.isBinary:
    print('Http body is binary')
  elif request.body.isMultipart:
    print('Http body is multipart')

  # 打印Body的类型
  print(request.body.type)
  # 打印Body的数据
  print(request.body.payload)
```

|   函数  |  参数 |  返回 |  说明  |
|  ----  | ---- | ----  | ----  |
|none|||设置为空Body。|
|text|str||设置为字符串Body，内容为参数值。|
|textFromFile|str||设置为字符串Body，并从指定文件路径中读取字符串数据。|
|binary|str或bytes||设置为字节Body，参数为str时表示从指定文件路径中读取数据。|
|file|str||设置为字节Body，表示从指定文件路径中读取数据，功能同上面的binary函数。|
|multiparts|list||设置为Multipart Body，参数为[HttpMultipartBody](#api-multipart-body)的列表。|
|writeFile|str||将Body数据写入文件。注意：不支持Multipart类型Body。|

代码示例：
```python
def onRequest(context, request):
  # 修改body为空
  request.body.none()
  # 修改body为字符串
  request.body.text('foobar')
  # 修改body为字符串，内容从文件读取
  request.body.textFromFile('/User/Reqable/Desktop/body.json')
  # 修改body为字节序列，直接指定
  request.body.binary(b'\x01\x02\x03\x04')
  # 修改body为字节序列，内容从文件读取
  request.body.binary('~/Desktop/body.json')
  # 修改body为multipart类型
  request.body.multiparts([
    HttpMultipartBody.text('Hi World'),
    HttpMultipartBody.file('data/body_binary.bin')
  ])

  # 将body数据写入文件
  request.body.writeFile('/User/Reqable/Desktop/body.json')

  # Done
  return request
```

#### HttpMultipartBody {#api-multipart-body}

HttpMultipartBody继承于[HttpBody](#api-body)，额外多出一个headers属性。

|   变量  |  类型 |  说明  |
|  ----  | ----  | ----  |
|**headers**|[HttpHeaders](#api-headers)|分部头部。|
|**name**|str|分部名称。|
|**filename**|str|分部文件名。|

代码示例：
```python
def onRequest(context, request):
  # 遍历parts
  for part in request.body:
    print(f'name {part.name}')
    print(f'filename {part.filename}')
    print(f'value {part}')

  # 修改parts
  request.body[0] = HttpMultipartBody.text('Hi World')
  request.body[0] = HttpMultipartBody.text('Hi World', name='reqable')
  request.body[0] = HttpMultipartBody.file('data/body_binary.bin')
  request.body[0] = HttpMultipartBody.file('data/body_binary.bin', name='reqable', filename='test.png')

  # Done
  return request
```

:::caution

如果将非multipart类型修改成multipart类型，必须同时修改headers设置boundary！

:::

## App {#api-app}

|   变量  |  类型 |  说明  |
|  ----  | ----  | ----  |
|*name*|str|应用（进程）名称。|
|*id*|str|应用ID，未获取到为None。例如Android上是`packageName`，Mac上是`bundleId`。|
|*path*|str|应用执行文件路径，未获取到为None。|

代码示例：
```python
def onRequest(context, response):
  # 打印应用信息
  print(context.app.name)
  print(context.app.id)
  print(context.app.path)
  # Done
  return request
```

## Highlight {#api-highlight}

|   枚举  |  说明  |
|  ----  | ----  |
|*none*| 不高亮。|
|*red*| 红色高亮。|
|*yellow*| 黄色高亮。|
|*green*| 绿色高亮。|
|*blue*| 蓝色高亮。|
|*teal*| 靛青色高亮。|
|*strikethrough*| 中划线。|

代码示例：
```python
def onRequest(context, response):
  # 设置请求红色高亮
  context.highlight = Highlight.red
  # Done
  return request
```

## 示例1

下面是一个修改JSON响应数据的示例。

假设响应数据是下面的格式：
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
我们需要将`version`的值修改为`2.0.0`。

```python
from reqable import *

def onRequest(context, request):
  # Done
  return request

def onResponse(context, response):
  # 将响应体字典化
  response.body.jsonify()
  # 修改字典中的version值
  response.body['content']['version'] = '2.0.0'
  # Done
  return response
```

## 示例2

下面是一个自动给请求参数进行MD5签名的示例。

```python
from reqable import *
import hashlib

def onRequest(context, request):
  # 对query列表进行排序
  request.queries = sorted(request.queries)
  # 拼接query数据
  text = request.queries.concat()
  # 选用md5算法进行签名
  algorithm = hashlib.md5()
  # 计算字符串的签名
  algorithm.update(text.encode(encoding='UTF-8'))
  signature = algorithm.hexdigest()
  # 签名加到请求头中
  request.headers['signature'] = signature
  # Done
  return request

def onResponse(context, response):
  # Done
  return response
```

## 示例3

下面是一个自动保存图片的脚本示例。

```python
from reqable import *
from mimetypes import guess_extension
import datetime
import os

def onRequest(context, request):
  return request

def onResponse(context, response):
  # 检查Mime类型，非图片类型则跳过不处理
  mime = response.mime
  if mime == None:
    return response

  maintype, subtype = mime.split('/')
  if not maintype == 'image':
    return response

  # 保存图片到指定目录，文件名为时间戳，后缀根据Mime类型推导
  dir = '/Users/megatronking/Downloads/reqable/'
  os.makedirs(dir, exist_ok=True)
  name = datetime.datetime.now().strftime("%H%M%S%f")
  ext = guess_extension(mime)
  image = os.path.join(dir, name + ext)

  # 响应体写入文件
  print(f'Saving image {image}')
  response.body.writeFile(image)

  # Done
  return response
```