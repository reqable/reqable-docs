---
title: 常见问题
description: Reqable使用的遇到常见问题解决方案。
sidebar_position: 7
---

# 常见问题

### 1. Reqable日志文件目录{#log}

- Windows
```
C:\Users\xxx\AppData\Roaming\Reqable\log
```
- MacOS
```
~/Library/Caches/Reqable/log
```
- Linux
```
~/.local/share/reqable
```

### 2. 无法访问境外受限网站 {#restrict}

Reqable本身不具备访问受限网站的能力，需要借助其他代理软件并在Reqable中配置[二级代理](../capture/proxy#secondary)。

### 3. Android代理无效问题 {#socksdroid}

部分网络框架不支持使用系统代理配置，我们可以通过VPN转发流量到Reqable的方式进行调试。

在模拟器上安装`socksdroid`（开源工具，也可自行编译），打开下面的地址下载apk文件。

```
https://github.com/bndeff/socksdroid/releases/download/1.0.3/socksdroid-1.0.3.apk
```

将下载好的`socksdroid`直接拖到模拟器窗口中进行安装，也可以使用`adb`进行安装。
```bash
adb install socksdroid-1.0.3.apk
```
安装完成后打开`socksdroid`，配置电脑的IP地址和Reqable代理端口，并启动右上角的开关。

![](arts/socksdroid.png)