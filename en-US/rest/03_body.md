# Body

Reqable supports multiple types of request bodies, including:

- [JSON](#json)
- [Text](#text)
- [XML](#xml)
- [Raw](#raw)
- [Form-data](#multipart)
- [Urlencode](#urlencode)
- [File](#binary)

Tap the `Content Type` drop-down menu to switch the request body type:

![](arts/body_01.png)

:::info
Request bodies support the use of [Environment Variables](../environment).
:::

### JSON {#json}

JSON is the most common request body type. Reqable provides an editor with syntax highlighting support.

![](arts/body_02.png)

The JSON type automatically appends `Content-Type: application/json` and `Content-Length` to [Built-in Headers](header#builtin). The `Content-Length` value is calculated automatically when the request is sent.

![](arts/body_03.png)

JSON data supports comments. Commented content will not be sent with the request.

![](arts/body_04.png)

:::caution
Formatting, minifying, and expand operations are not currently supported for JSON content that contains comments.
:::

### Text {#text}

The simplest request body type:

![](arts/body_05.png)

The Text type automatically appends `Content-Type: text/plain` and `Content-Length` to [Built-in Headers](header#builtin). The `Content-Length` value is calculated automatically when the request is sent.

![](arts/body_06.png)

### XML {#xml}

The XML request body type supports syntax highlighting.

![](arts/body_07.png)

The XML type automatically appends `Content-Type: application/xml` and `Content-Length` to [Built-in Headers](header#builtin). The `Content-Length` value is calculated automatically when the request is sent.

![](arts/body_08.png)

### Raw {#raw}

The Raw type is similar to [Text](#text), except that it does not automatically append `Content-Type` to [Built-in Headers](header#builtin), making it suitable for custom types defined by the user.

### Form-data {#multipart}

Form-data supports three part types: `Single-line Text`, `Multi-line Text`, and `File`.

![](arts/body_09.png)

Tap the more button on the right to open the part action menu, including changing type, moving position, editing headers, deleting, and more.

![](arts/body_10.png)

For multi-line text, tap to open the edit dialog for modification.

![](arts/body_11.png)

Reqable also supports editing the header information of each part.

![](arts/body_12.png)

The Multipart type automatically appends `Content-Type: multipart/form-data` and `Content-Length` to [Built-in Headers](header#builtin). The `Content-Length` value is calculated automatically when the request is sent.

![](arts/body_13.png)

:::info About Boundary

There is no need to add `Boundary` manually. Reqable automatically generates it when the request is sent.

:::

### Urlencode {#urlencode}

The Urlencode form type is a set of key-value pairs combined in the following format:

```
foo=bar&hello=reqable
```

By default, form data can be edited in table mode.

![](arts/body_14.png)

It can also be switched to text mode for editing. In text mode, `//` comments are supported for unchecking items.

![](arts/body_15.png)

The Urlencode type automatically appends `Content-Type: application/x-www-form-urlencoded` and `Content-Length` to [Built-in Headers](header#builtin). The `Content-Length` value is calculated automatically when the request is sent.

![](arts/body_16.png)

### File {#binary}

The File type supports selecting a file as the request body. You can choose a file through the system file manager, or drag it directly into the dotted area.

![](arts/body_17.png)

The File type automatically appends the corresponding `Content-Type` (guessed automatically) and `Content-Length` (calculated automatically when the request is sent) to [Built-in Headers](header#builtin).

![](arts/body_18.png)
