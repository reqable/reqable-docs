---
title: Android
description: Android下常见问题和解决方案。
sidebar_position: 4
---

# Android常见问题

:::info
请更新Reqable到最新版本，然后再进行问题排错。
:::

### 1. 证书问题

- [证书安装](../../getting-started/installation)
- [问题排错](../ssl)

### 2. 查看日志

打开侧边栏，长按顶部Logo，可以选择日志文件进行查看。

### 3. 获取不到应用程序的流量

请先确保下面的操作已经处理。

- 已经开启了调试开关。
- 已经设置`记录模式`为VPN而不是代理。
- 已经启用`增强模式`。
- 已关闭全部筛选和搜索条件。
- 已移除全部指定应用程序。

Reqable启动调试开关后，打开手机浏览器，访问百度首页。

:::caution
浏览器可能会提示不安全连接，这种情况是证书问题，请阅读下面的内容。
- [Chrome](#chrome)
- [Firefox](#firefox)
:::

情况一：百度首页无法访问，并且Reqable调试列表中看不到任何流量（包括CONNECT请求）。

可能是Reqable代理服务器端口异常（例如被其他程序进程占用），可以尝试更换下端口重试。

如果更换端口后浏览器仍然无法访问百度首页，请在[Github](https://github.com/reqable/reqable-app/issues)或者微信反馈给我们。

情况二：百度首页可以访问，但是Reqable调试列表中看不到任何流量（包括CONNECT请求）。

再次检查`记录模式`是否是VPN模式，如果VPN模式下依然是这种情况，请在[Github](https://github.com/reqable/reqable-app/issues)或者微信反馈给我们。

情况三：百度首页可以访问，Reqable调试列表中也能看到浏览器的访问流量（包括CONNECT请求）。

浏览器正常说明应用程序禁止在VPN模式下工作，请联系应用程序开发商获取解决方案。

### 4. 无法连接电脑

- 检查手机和电脑是否在同一个局域网下。
- 检查手机和电脑是否在同一个局域网段，有些局域网组网时会禁止跨段通信。
- 尝试电脑连接手机热点，然后手机再扫码连接电脑。
- 检查电脑防火墙是否禁用了Reqable代理端口号流量出入。

### 5. 协同模式下获取不到应用程序的流量

您可以按照下面的步骤进行排查：

- 切换到独立模式（即侧边栏选择`调试`Tab），按照上面3进行排查。
- 手机端Reqable关闭或者启用`增强模式`再次尝试。
- 更换电脑端Reqable的端口，然后重新扫码连接。

### 6. Chrome访问提示不安全的网站{#chrome}

Chrome浏览器对证书的信任策略一直在变化，比如最新版本的Chrome浏览器会忽略安装到Android系统证书目录的自签CA证书，如果需要对Chrome浏览器进行抓包，请按照下面的方式进行处理：

- 如果是高版本Chrome浏览器，需要将CA证书安装到用户证书目录；
- 如果是低版本的Chrome浏览器，需要将CA证书安装到系统证书目录。

如果不确定选用那种方式，可以分别尝试下。

### 7. Firefox访问提示不安全的网站{#firefox}

Firefox浏览器使用内置的CA Store，系统安装的CA证书无法生效，需要在Firefox调试菜单中启用信任。

- Firefox设置 -> 关于Firefox -> 点击顶部Logo 5下启用调试菜单。
- Firefox设置 -> Secret Settings -> 启用 Use third party CA certificates。

### 8. 无法访问境外受限网站

Reqable本身不具备访问受限网站的能力，您可以在取得境外访问许可的前提下按照下面的步骤操作。

- 电脑端安装并启动科学上网工具。
- 电脑端Reqable配置[二级代理](../../capture/proxy#secondary)到上一步的工具。
- 手机端Reqable扫码连接电脑（协同模式）。