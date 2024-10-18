# Proxy

Reqable uses the MITM proxy server to intercept traffic. How to use and configure the proxy correctly is very important. By default, Reqable will automatically configure the system network proxy, without the need for users to manually open the system settings.

![](arts/proxy_01.png)

The status of the system proxy will be displayed on the [QuickBar](quickbar). If the system  proxy is properly configured, the icon will show a green active state; otherwise, it will show a yellow warning state. Clicking the icon in the green state will disable the system network proxy; clicking the icon in the yellow state will enable the system network proxy.

:::caution

When you need to perform traffic analysis on native applications (such as browsers, etc.), please keep the system network proxy in the green active state! Some proxy applications such as Clash may cause conflicts. It is recommended to close other proxy applications when using Reqable.

:::

Under normal circumstances, a client application (such as a browser) will actively connect to Reqable proxy server according to the system network proxy configuration. However, some applications do not use the system network proxy configuration. In this case, users need to manually configure it in the settings of the client application. If an application neither uses the system network proxy configuration nor provides a way to manually set a proxy, Reqable will not be able to analyze its traffic. Of course, under the premise of obtaining the authorization of the target application, you can consider using tools such as `Proxifier` to forcibly forward its traffic to Reqable proxy server.

For localhost traffic, it may not go through the Reqable proxy server, even if we have properly configured the system network proxy. About the workaround, please read [localhost](localhost).

In addition, on Windows, some clients do not support default proxy rule. Please read the following [Proxy Rules](#rule) for more details.

### Proxy Protocol

Reqable supports five proxy protocols including HTTP, HTTPS, Socks4, Socks4a, and Socks5. Reqable proxy server listens to the same port (port 9000 by default), and automatically determines the protocol based on the client's message content. Reqable cannot specify which proxy protocol the target application adopts, it can only be configured in the proxy settings of the system, which is determined by the client program itself. Regarding proxy settings, different computer systems provide different methods. Please read the following according to the operation system you are using.

#### Windows

Windows can only configure Web proxy or Socks proxy, choose one of the two. By default, Reqable will automatically configure the web proxy. If there is a need to use the Socks proxy, you can switch it in the right-click menu of the proxy icon.

#### MacOS

The Mac OSX system supports the configuration of HTTP, HTTPS and SOCKS protocols at the same time. Users can configure all three or only one in Reqable. In general, it is recommended to check all three protocols.

![](arts/proxy_mac.png)

#### Linux

The Linux system is the same as the Mac OSX system, supports the configuration of HTTP, HTTPS and SOCKS protocols at the same time. Users can configure all three or only one in Reqable. In general, it is recommended to check all three protocols.

### Secondary Proxy {#secondary}

For accessing some restricted websites, such as accessing Google in mainland China, you need to use some proxy software. However, only one proxy can be configured in the system settings. When Reqable is used as the system proxy, these websites will not be accessible. In this case, Reqable's secondary proxy needs to be used. The principle of Reqable's secondary proxy: When Reqable receives the client's proxy request, it will forward it to the secondary proxy server, and the secondary proxy server will carry out the actual communication. You can create a secondary proxy configuration via **Proxy** -> **Secondary Proxy** -> **New Secondary Proxy**.

![](arts/secondary_proxy_02.png)

Enter the name, IP address, and port number of the secondary proxy server and save. The secondary proxy provides two modes: Include Mode and Exclude Mode.

Include Mode: only allow traffic with specified domain name rules to goto the secondary proxy. Exclude Mode: traffic with specified domain name rules bypasses the secondary proxy.

Users can configure multiple domain name rules, support wildcards `*` and `?`, one domain name per line. If only one `*` symbol is configured, it means matching all traffic.

:::info
The secondary proxy currently only supports the HTTP proxy protocol. After enabling the secondary proxy, the top indicator icon will change from a network to an airplane.
:::

If you have multiple proxy servers, you can create multiple configurations and manage them in the secondary proxy list.

![](arts/secondary_proxy_01.png)

:::caution
If the secondary proxy is configured and enabled, but the secondary proxy server is not started, requests to the secondary proxy will fail.
:::

### Proxy Rule {#rule}

On the Windows system, the web proxy supports the following formats.

① `{ip}:{http_port}`

② `http=http://{ip}:{http_port};https=http://{ip}:{http_port}`

③ `http={ip}:{http_port};https={ip}:{http_port}`

The first of these is a common format and is the default format chosen by Reqable. But some clients can't recognize this format (see this [issue](https://github.com/MatsuriDayo/nekoray/issues/104)), so Reqable provides an option to switch the format. When the web proxy type is selected, the proxy rules can be switched.

### Record Mode

:::caution Attention

If you are not familiar with this function, please keep the **VPN** mode.

:::

On the Android side of Reqable, we provide two`record modes`to capture network traffic:  **Proxy Mode** and **VPN Mode**。

![](arts/proxy_05.png)

- **Proxy Mode**
 Configure the IP and port of Reqable's MITM server into the system's network proxy settings. If the application supports it, it will read the system's network proxy settings for network requests, allowing Reqable to capture the traffic. On the PC side, Reqable only supports this mode and can automatically configure the system proxy settings with one click. On the mobile side, you need to manually configure the system proxy, and if the application does not support proxy settings, it may not be able to capture the traffic.

- **VPN Mode**
 Also known as TUN mode, it forces the application's network traffic into the VPN virtual network card, which is undetectable by the application itself. The virtual network card automatically forwards the traffic to Reqable's MITM server for traffic analysis. Mechanically speaking, the VPN mode can automatically intercept traffic, similar to a transparent proxy, with the application itself being unaware, offering stronger operability. Currently, only the mobile side of Reqable supports VPN mode.
