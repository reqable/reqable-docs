---
title: SSL
description: SSL FAQs and solutions.
sidebar_position: 6
---

# SSL FAQs

Most SSL issues are certificate trust issues. Different systems and applications have different SSL verification strategies. Many issues require specific analysis and there is no unified solution. Here are some FAQs and solutions for your reference.

First is [CA Certificate Installation](../getting-started/installation), please read it carefully. Make sure the CA certificate is installed correctly in your device, then look at other issues.

### 1. SSL error on PC for mobile traffic

If the mobile phone can capture SSL traffic in `Standalone Mode`, but PC cannot capture SSL traffic in `Collaborative Mode`, it means that the CA certificate of PC is not installed on the mobile device.

### 2. Built-in CA Store

Some applications have built-in CA Stores instead of using the system CA Store for security reasons. Certificates installed in the system CA Store are invalid for these applications, which means that the SSL handshake requests of these applications fail. The most see one is the Firefox browser, but Firefox provides us with a solution for importing CA certificates, while some applications do not. There is no way to deal with this issue, need to ask the app owner for a solution.

### 3. Certificate Pinning

SSL Pinning refers to the SSL certificate of the server specified by the application client. The SSL certificate issued by the Reqable MITM cannot be verified. If you have the server's SSL certificate (certificate + private key), you can configure it to Reqable's SSL certificate (server). For details, please refer to [SSL Certificate](../capture/ssl#ssl-certificates).

### 4. Two-way authentication

Two-way authentication means that the application client needs to upload the SSL certificate to the server. By default, the Reqable MITM will not upload the SSL certificate to the server, so the server will reject the client's connection. If you have the client's SSL certificate (private key is optional), you can configure it in Reqable's SSL certificate (client). For details, please refer to [SSL Certificate](../capture/ssl#ssl-certificates).

### 5. Python

When sending requests using a network library such as Python requests, the certificate may not be verified. Try running the Python script in the [Proxy Terminal](../capture/proxy-terminal).

### 6. NodeJS

When using the network library under NodeJS to send a request, the certificate may not be verified. In this case, you can try running the Node program in the [Proxy Terminal](../capture/proxy-terminal).