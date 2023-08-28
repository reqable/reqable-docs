# SSL

Reqable支持分析SSL加密流量，如果已经成功安装了CA根证书，Reqable默认会自动分析所有SSL流量，反之Reqable则会绕过SSL解密逻辑。未解密的SSL流量图标会显示一个🔒的标记，如下：

![](arts/ssl_01.png)

在默认情况下，Reqable自动解析SSL加密流量，可能会带来一些问题。例如客户端固定证书、双向验证等，导致请求失败。这种情况下，我们需要配置旁路规则（SSL Bypass）来让Reqable绕过这些SSL流量。右键点击盾牌图标，在菜单中点击**SSL旁路**，可以打开配置界面。

![](arts/ssl_02.png)

在配置页面可以按照**行**来配置域名，支持Wildcard通配符 `*` 和 `?`。

![](arts/ssl_03.png)

举个例子，假如配置了 `*.apple.com` 这个规则，那么下面的请求都将跳过SSL解密过程。
```
https://www.apple.com/
https://api.apple.com/
```

匹配上SSL旁路规则的流量仍然会在列表中显示，可以通过🔒的图标分辨出来。如果希望不在列表中显示，可以勾选上`静默模式`。

:::info
- 配置SSL Bypass有利于过滤掉一些无关的流量，对于提高响应性能有帮助。
- 在MacOS系统上，Reqable默认配置了苹果公司要求Bypass的域名，因为这些域名都进行了证书固定。
:::