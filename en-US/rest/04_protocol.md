# Protocol

Reqable supports three HTTP protocols: [HTTP1.1](https://www.ietf.org/rfc/rfc2616.txt), [HTTP2](https://www.ietf.org/rfc/rfc7540.txt) And [HTTP3](https://www.ietf.org/rfc/rfc9114.txt), we can specify the protocol version in the request settings.

![](arts/protocol_01.png)

:::info Server Support

All protocol versions need to be supported by the server. If the server does not support a higher version, it will be downgraded to HTTP1.1 version.

:::

### HTTTP1.1

HTTP1.1 is currently the most popular version of the HTTP protocol, with well-known features such as maintaining connections and chunk transmission. Currently, almost all HTTP frameworks support this version. We can check the protocol version used on the response label.

![](arts/protocol_02.png)

### HTTTP2

HTTP2 is currently a very commonly used HTTP protocol version. Compared with HTTP/1.1, its features such as multiplexing and header compression have very obvious performance advantages, but not all HTTP frameworks support this version. If the server does not support the HTTP2 protocol version, it will be downgraded to the HTTP1.1 protocol version, and we can check the specific protocol version used on the response label.

![](arts/protocol_03.png)

### HTTTP3

HTTP3 is developed from [QUIC](https://www.ietf.org/rfc/rfc9000.txt). Compared with HTTP2, its performance and security have been further improved, but unfortunately, most HTTP services None of the frameworks support this version. As a new protocol in the future, Reqable still gives enough support. If the server does not support the HTTP3 protocol version, it will be downgraded to the HTTP/1.1 protocol version, and we can check the specific protocol version used on the response label.

![](arts/protocol_04.png)