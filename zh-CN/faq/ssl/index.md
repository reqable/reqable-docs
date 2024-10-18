---
title: SSL
description: SSL常见问题和解决方案。
sidebar_position: 6
---

# SSL常见问题

SSL问题大多都是证书信任问题，不同的系统、应用程序都有不同的SSL验证策略，许多问题都需要具体问题具体分析，没有统一的解决方案。这里列出了一些常见的SSL问题和解决方案供大家参考。

首先是[CA证书安装](../../getting-started/installation)，请认真阅读。先确保证书正确安装了，然后再来看其他问题。

### 1. 手机流量在电脑上出现SSL错误

如果手机端`独立模式`正常解析SSL流量，但是在`协同模式`下电脑无法解析SSL流量，说明电脑端Reqable的CA证书未安装到手机设备上。

### 2. 内置CA Store

有些应用程序为了安全性会内置CA Store而不是使用系统的CA Store，证书安装到系统的CA Store对这些应用程序无效表现为这些应用程序的请求SSL握手失败。最常见的就是Firefox浏览器，只不过Firefox为我们提供了导入CA证书的方案，有的应用程序则不会。这种情况没有办法处理，需要应用程序开发商提供解决方案。

### 3. 固定证书

固定证书（SSL Pinning）是指应用程序客户端指定服务器的SSL证书，Reqable中间人签发的SSL证书无法通过验证。如果您拥有服务器的SSL证书（公钥证书 + 私钥），可以配置到Reqable的SSL证书（服务端）中，细节请参考[SSL证书](../../capture/ssl-certificates)。

### 4. 双向验证

双向验证是指应用程序客户端需要上传SSL证书给服务器，默认情况下Reqable中间人不会上传SSL证书给服务器，因此服务器会拒绝客户端的连接。如果您拥有客户端的SSL证书（私钥可选），可以配置到Reqable的SSL证书（客户端）中，细节请参考[SSL证书](../../capture/ssl-certificates)。

### 5. Python

使用Python requests等网络库发送请求，可能会出现无法验证证书的情况，请使用可以尝试在[代理终端](../../capture/proxy-terminal)中执行Python脚本。

### 6. NodeJS

使用NodeJS下的网络库发送请求，可能会出现无法验证证书的情况，请使用可以尝试在[代理终端](../../capture/proxy-terminal)中运行Node程序。