---
title: FAQ
description: Reqable FAQ solutions.
sidebar_position: 7
---

# FAQ

### 1. Reqable cache directory{#cache}

- Windows
```
C:\Users\xxx\AppData\Roaming\Reqable
```
- MacOS
```
~/Library/Application Support/com.reqable.macosx
```
- Linux
```
~/.local/share/reqable
```

### 2. Browser or application no respond {#troubleshot-pc}

It may be caused by port conflict, just change the proxy port of Reqable.

![](arts/troubleshot-pc.png)

### 3. No traffic can be observed on mobile phone {#troubleshot-mobile}

If the computer is working normally, the mobile phone cannot get any traffic, please check the CheckList below.

- [x] Both mobile phone and PC are connected to the same LAN.
- [x] The mobile Wifi proxy has set the IP address and port number of Reqable (see the top of the Reqable window), or use SocksDroid for forwarding.
- [x] The CA certificate has been correctly installed on the phone (Only has `CONNECT` traffic).
- [x] The PC network firewall has opened the port address of Reqable.