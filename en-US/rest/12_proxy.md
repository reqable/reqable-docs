# Proxy

Proxy is one of the essential settings when testing APIs. We can configure proxy in the request settings.

![](arts/proxy_01.png)

Reqable supports 4 proxy settings:
- **Follow System** Use the proxy configured by the system.
- **Follow Debug** Use the MITM proxy and work with capture features.
- **Manual** To use a custom web proxy, just specify the proxy IP and port number.
- **Unset** Disable any proxy.

### Follow Debug

**Follow Debug** is an important feature of Reqable. You can use [Script](../capture/script) and other capture features with the request. Requests are also displayed in the traffic list without enabling capture separately.

![](arts/proxy_02.png)

### Manual Proxy

Reqable currently only supports setting a custom web proxy. You need to specify the proxy IP and port number. The configuration method is as follows:

![](arts/proxy_03.png)

:::info Proxy Protocol

If there is a need for proxy protocols such as Socks, you can configure it in the system and select **Follow System** in settings.

:::