---
title: 付费会员
description: 有关Reqable需要付费的功能介绍。
sidebar_position: 9
---

Reqable的会员分为两种，普通会员和高级会员。通过邮箱注册账号后即是普通会员，付费后可以成为高级会员。Reqable绝大多数功能免费，且不要求注册会员，但为了项目的可持续发展，我们提供付费功能，付费的高级会员享有比普通会员更多的权益，Reqable的部分功能也仅对高级会员开放。

这篇文档简要介绍了Reqable的付费功能，不同的Reqable版本可能略有差异，请以最新版本实际情况为准。

:::info
随着版本迭代，我们可能会做适当调整，例如将部分付费功能改成全员免费。
:::

### 云服务存储空间

Reqable支持将数据同步到云端，普通会员的最大存储空间为 `100M`，高级会员的最大存储空间为 `1G`。

![](./arts/storage.png)

:::info
无论是普通会员还是高级会员，注销账号后云端数据均会被删除，无法恢复。
:::

### 多设备同步

普通会员仅支持同时在一台设备上登录，登录其他设备后，之前登录的设备会自动退出登录。高级会员最多支持同时登录6台设备（不限平台），超出这个数量，最先登录的一台设备会自动退出登录。

如果启用了云端数据模式，存储的数据可以在登录后的设备上实时同步。

![](./arts/device.png)

用户可以在个人中心管理已登录的设备，移除设备后，该设备需要重新登录。

### MCP操作 {#mcp}

普通会员的MCP仅支持读操作，例如从调试列表读取抓包数据，从API集合中读取API接口信息。高级会员支持写操作，例如向API集合中写入数据、更新API文档，创建调试脚本等。

### HTTP3测试 {#http3_testing}

Reqable支持发送 `HTTP/1.1`、`HTTP2` 以及 `HTTP3(QUIC)` 请求，其中 `HTTP3(QUIC)` 仅对高级会员开放。

![](../rest/arts/protocol_04.png)

:::info
如果服务端不支持 `HTTP3(QUIC)` 协议版本，则会被降级到 `HTTP/1.1`，可以在响应标签上查看实际使用的协议版本。
:::

### 自定义主题 {#custom_accent_color}

Reqable内置了十六种强调色，高级会员可以设置自定义强调色。

![](./arts/accent.png)

### 无限制SSL代理 {#unlimited_ssl_proxying_rules}

普通会员最多创建2条 [SSL代理](../capture/ssl#ssl-proxying) 规则，高级会员可以不受任何数量限制。

![](./arts/ssl-proxying.png)

### 无限制镜像规则 {#unlimited_mirror_rules}

普通会员最多创建3条 [镜像](../capture/mirror) 规则，高级会员可以不受任何数量限制。

![](./arts/mirror.png)

:::info
此功能尚不支持移动端。
:::

### 无限制网关规则 {#unlimited_gateway_rules}

普通会员最多创建3条 [网关](../capture/gateway) 规则，高级会员可以不受任何数量限制。

![](./arts/gateway.png)

:::info
此功能尚不支持移动端。
:::

### 无限制重写规则 {#unlimited_rewrite_rules}

普通会员最多创建3条 [重写](../capture/rewrite) 规则，高级会员可以不受任何数量限制。

![](./arts/rewrite.png)

:::info
此功能尚不支持移动端。
:::

### 无限制断点规则 {#unlimited_breakpoint_rules}

普通会员最多创建3条 [断点](../capture/breakpoint) 规则，高级会员可以不受任何数量限制。

![](./arts/breakpoint.png)

:::info
此功能尚不支持移动端。
:::

### 无限制脚本规则 {#unlimited_script_rules}

普通会员最多创建3条 [脚本](../capture/script) 规则，高级会员可以不受任何数量限制。

![](./arts/script.png)

:::info
此功能尚不支持移动端。
:::

### 无限制脚本模板 {#unlimited_script_templates}

普通会员最多创建2个脚本模板，高级会员可以不受任何数量限制。

![](./arts/script-template.png)

:::info
此功能尚不支持移动端。
:::

### 无限制访问控制规则 {#unlimited_access_control_rules}

普通会员最多创建1条 [访问控制](../capture/access-control) 规则，高级会员可以不受任何数量限制。

![](./arts/access-control.png)

### 无限制网络模拟规则 {#unlimited_network_throttling_rules}

普通会员最多创建1条 [网络模拟](../capture/network-condition) 规则，高级会员可以不受任何数量限制。

![](./arts/network-condition.png)

:::info
此功能尚不支持移动端。
:::

### 无限制反向代理规则 {#unlimited_reverse_proxy_rules}

普通会员最多创建3条 [反向代理](../capture/reverse-proxy) 规则，高级会员可以不受任何数量限制。

![](./arts/reverse-proxy.png)

:::info
此功能尚不支持移动端。
:::

### 无限制二级代理规则 {#unlimited_secondary_proxy_profiles}

普通会员最多创建1条 [二级代理](../capture/proxy#secondary) 规则，高级会员可以不受任何数量限制。

![](./arts/secondary-proxy.png)

### 无限制上报服务器规则 {#unlimited_report_server_profiles}

普通会员最多创建1条 [上报服务器](../capture/report-server) 规则，高级会员可以不受任何数量限制。

![](./arts/report-server.png)

### 无限制gRPC定义规则 {#unlimited_grpc_definition_rules}

普通会员最多创建3条 `gRPC定义` 规则，高级会员可以不受任何数量限制。

![](./arts/grpc-definition.png)

### 无限制Protobuf定义规则 {#unlimited_protobuf_definition_rules}

普通会员最多创建3条 `Protobuf定义` 规则，高级会员可以不受任何数量限制。

![](./arts/protobuf-definition.png)

### 无限制收藏文件夹 {#unlimited_favorite_folder}

普通会员无法创建自定义收藏文件夹，高级会员可以自由创建收藏文件夹。

![](./arts/favorite-folder.png)

:::info
- 移动端目前尚不支持自定义创建收藏文件夹。
:::

### 无限制收藏请求 {#unlimited_favorite_save_items}

普通会员最多收藏10条请求，高级会员可以不受任何数量限制。

:::info
- 收藏数据目前尚不支持同步到云端。
:::

### 无限制书签文件夹 {#unlimited_bookmark_folder}

普通会员无法创建自定义书签文件夹，高级会员可以自由创建书签文件夹。

![](./arts/bookmark-folder.png)

:::info
此功能尚不支持移动端。
:::

### 无限制添加书签 {#unlimited_bookmark_save_items}

普通会员最多创建10个书签，高级会员可以不受任何数量限制。

:::info
- 书签数据目前尚不支持同步到云端。
- 此功能尚不支持移动端。
:::

### 无限制查看历史记录 {#unlimited_history_review}

普通会员可以查看30天内的抓包历史记录，高级会员可以不受此限制。

### 多条件搜索 {#unlimited_search_conditions}

普通会员仅可以单条件搜索抓包记录，高级会员可以使用多条件（上限5个）搜索。

![](./arts/filter-search.png)

### 无限制保存搜索条件 {#unlimited_save_filters}

普通会员仅可以保存一个搜索条件，高级会员可以不受任何数量限制。

![](./arts/filter-save.png)

### 无限制抓包会话 {#unlimited_capture_sessions}

普通会员仅可以使用一个抓包会话，高级会员可以不受任何数量限制。

![](./arts/sessions.png)

### 无限制高亮条件 {#unlimited_capture_highlight_conditions}

在设置调试数据自动高亮时，普通会员仅可以使用一个条件，高级会员可以不受任何数量限制。

![](./arts/highlight.png)

### 无限制对比请求响应 {#unlimited_capture_diff_items}

在对比调试数据时，普通会员仅可以添加两个请求项，高级会员可以不受任何数量限制。

![](./arts/diff.png)

### 无限制分离窗口 {#unlimited_capture_session_window}

普通会员可以分离一个窗口查看调试数据详情，高级会员可以不受任何数量限制。

![](./arts/session-window.png)

:::info
此功能尚不支持移动端。
:::

### 多设备抓包协同 {#unlimited_collaborations}

在移动端添加协同设备时，普通会员最多可以添加一台设备，高级会员不受数量限制。

![](./arts/collaboration.png)

### 多应用抓包 {#unlimited_target_apps}

在移动端指定抓包应用时，普通会员最多可以指定一个应用程序，高级会员不受数量限制。

![](./arts/target-app.png)

:::info
此功能尚不支持桌面端。
:::

### 增强模式抓包 {#capture_enhanced_mode}

高级会员支持在移动端开启增强模式抓包，增强模式具备如下优势：

- 可以拦截系统全部流量，不会漏包。
- Android平台可以获取流量来源应用信息。

![](./arts/enhanced-mode.png)

:::info
桌面端尚不支持增强模式，目前已经在规划中。
:::

### AES加解密 {#crypto_aes}

Reqable工具箱提供AES加解密工具，支持 `CBC`，`CFB`，`CTR`，`ECB`，`OFB`，`SIC` 和 `GCM` 算法，此功能仅对高级会员开放。

![](./arts/aes.png)

:::info
此功能尚不支持移动端。
:::

### IP查询 {#ip_query}

Reqable工具箱提供IP归属地查询能力，此功能仅对高级会员开放。

![](./arts/ip.png)

:::info
此功能尚不支持移动端。
:::