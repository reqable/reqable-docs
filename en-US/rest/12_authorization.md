# Authorization

Reqable provides a simple authorization and supports 3 modes: [Basic Auth](#basic-auth), [Bearer Token](#bearer-token) and [Api Key](#api-key).

![](arts/authorization_01.png)

### Basic Auth {#basic-auth}

For details and specifications of Basic Auth, please refer to the [RFC document](https://datatracker.ietf.org/doc/html/rfc7617), without much explanation. The usage is very simple, just select **Basic Auth** in the authorization and fill in the username and password.

![](arts/authorization_02.png)

Reqable will automatically generate Authorization in the built-in request header.

![](arts/authorization_03.png)

### Bearer Token {#bearer-token}

For details and specifications of Bearer Token, please refer to the [RFC document](https://datatracker.ietf.org/doc/html/rfc6750), without much explanation. The usage is very simple, just select **Bearer Token** in the authorization and fill in the token.

![](arts/authorization_04.png)

Reqable will automatically generate Authorization in the built-in request header.

![](arts/authorization_05.png)

### Api Key {#api-key}

Api Key supports passing in request headers and query parameters.

![](arts/authorization_06.png)

Passed in request headers:

![](arts/authorization_07.png)

passed in rquery parameters:

![](arts/authorization_08.png)
