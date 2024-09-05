# 上报服务器

Reqable支持将捕获的HTTP请求和响应自动上传到指定的服务器，适用于数据自动采集等场景。

:::info
使用此功能需要更新Reqable到v2.20.0及以上版本。
:::

### 原理

用户需要自行部署一个服务端，用于接收Reqable上报的数据。Reqable与服务端使用HTTP协议进行通信，请求方法为`POST`，请求路径用户可以自行定义。每当Reqable检测到一个请求会话完成，会将数据以HAR的组织格式（JSON）发送给服务端。服务端接收到数据后，按照HAR的格式进行数据解析并进行自定义的后续操作。Reqable支持传输数据压缩，用户可以选择Gzip、Brotli和Zstandard三种压缩算法。

### 使用方式

从`工具`菜单中打开`报告服务器`，然后添加一个配置。用户需要指定一个配置名称，一个需要采集的数据的URL匹配规则（支持`*`和`?`通配符），一个服务端数据接收的接口路径。此外，还可以选择Reqable和服务端的数据传输的压缩算法（前提是服务端支持），为了提高上传效率，建议配置压缩算法。

![](arts/server-report_01.png)

举个例子，如果希望采集`dev.reqable.com`域名下的所有接口，可以配置规则为`https://dev.reqable.com/*`。

:::info
手机版本可以从`⋮` -> `更多`中打开`上报服务器`功能。
:::

Reqable除了会向服务器发送请求和响应数据，还会在请求头中携带下面这些数据：
- x-reqable-platform：Reqable运行的平台名称，例如windows，macos，linux，android，ios等。
- x-reqable-reporter-host：当前会话的域名，例如`dev.reqable.com`。
- x-reqable-reporter-rule：命中的规则。

:::caution
每一个HTTP会话Reqable只会发送1次，且发送失败不会重试。
:::

我们提供了一个Python服务器的代码示例以供参考：

https://github.com/reqable/report-server-example/blob/main/server.py