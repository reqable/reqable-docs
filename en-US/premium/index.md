---
title: Premium
description: An overview of Reqable's paid features.
sidebar_position: 9
---

Reqable offers two membership tiers: Basic and Premium. Registering an account with your email address gives you Basic membership, and you can upgrade to Premium by paying for membership. Most Reqable features are free and do not require an account. However, to support the project's continued development, we offer paid features. Premium members enjoy more benefits than Basic members, and some Reqable features are available exclusively to Premium members.

This document provides a brief overview of Reqable's paid features. Features may vary slightly between versions; refer to the latest version for the most up-to-date information.

:::info
As Reqable evolves, we may make adjustments, such as making certain paid features free for everyone.
:::

### Cloud Storage

Reqable supports syncing data to the cloud. Basic members receive up to `100M` of storage, while Premium members receive up to `1G`.

![](./arts/storage.png)

:::info
For both Basic and Premium members, deleting your account permanently deletes all associated cloud data. This data cannot be recovered.
:::

### Multi-Device Sync

Basic members can be signed in on only one device at a time. Signing in on another device automatically signs out the previously signed-in device. Premium members can be signed in on up to six devices simultaneously, across any platforms. If this limit is exceeded, the device that was signed in first is automatically signed out.

When cloud data mode is enabled, stored data syncs in real time across devices signed in to your account.

![](./arts/device.png)

You can manage your signed-in devices in the account center. After you remove a device, you will need to sign in again on that device.

### MCP Operations {#mcp}

For Basic members, MCP supports read-only operations, such as reading captured traffic from the capture list and retrieving API information from API collections. Premium members also have access to write operations, such as adding data to API collections, updating API documentation, and creating debugging scripts.

### HTTP3 Testing {#http3_testing}

Reqable supports sending `HTTP/1.1`, `HTTP2`, and `HTTP3(QUIC)` requests. `HTTP3(QUIC)` is available exclusively to Premium members.

![](../rest/arts/protocol_04.png)

:::info
If the server does not support `HTTP3(QUIC)`, the request falls back to `HTTP/1.1`. You can check the protocol version actually used in the response tab.
:::

### Capture Preview Mode {#capture_grid_view}

In addition to the default list view, Reqable also provides a preview mode for captured traffic, making it easier to quickly locate images and other media resources.

![](./arts/grid.png)

### Custom Themes {#custom_accent_color}

Reqable includes sixteen built-in accent colors. Premium members can set a custom accent color.

![](./arts/accent.png)

### Unlimited SSL Proxying Rules {#unlimited_ssl_proxying_rules}

Basic members can create up to two [SSL proxying](../capture/ssl#ssl-proxying) rules. Premium members can create an unlimited number of rules.

![](./arts/ssl-proxying.png)

### Unlimited Mirror Rules {#unlimited_mirror_rules}

Basic members can create up to three [mirror](../capture/mirror) rules. Premium members can create an unlimited number of rules.

![](./arts/mirror.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Gateway Rules {#unlimited_gateway_rules}

Basic members can create up to three [gateway](../capture/gateway) rules. Premium members can create an unlimited number of rules.

![](./arts/gateway.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Rewrite Rules {#unlimited_rewrite_rules}

Basic members can create up to three [rewrite](../capture/rewrite) rules. Premium members can create an unlimited number of rules.

![](./arts/rewrite.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Breakpoint Rules {#unlimited_breakpoint_rules}

Basic members can create up to three [breakpoint](../capture/breakpoint) rules. Premium members can create an unlimited number of rules.

![](./arts/breakpoint.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Script Rules {#unlimited_script_rules}

Basic members can create up to three [script](../capture/script) rules. Premium members can create an unlimited number of rules.

![](./arts/script.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Script Templates {#unlimited_script_templates}

Basic members can create up to two script templates. Premium members can create an unlimited number of templates.

![](./arts/script-template.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Access Control Rules {#unlimited_access_control_rules}

Basic members can create one [access control](../capture/access-control) rule. Premium members can create an unlimited number of rules.

![](./arts/access-control.png)

### Unlimited Network Throttling Rules {#unlimited_network_throttling_rules}

Basic members can create one [network throttling](../capture/network-condition) rule. Premium members can create an unlimited number of rules.

![](./arts/network-condition.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Reverse Proxy Rules {#unlimited_reverse_proxy_rules}

Basic members can create up to three [reverse proxy](../capture/reverse-proxy) rules. Premium members can create an unlimited number of rules.

![](./arts/reverse-proxy.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Secondary Proxy Rules {#unlimited_secondary_proxy_profiles}

Basic members can create one [secondary proxy](../capture/proxy#secondary) rule. Premium members can create an unlimited number of rules.

![](./arts/secondary-proxy.png)

### Unlimited Report Server Rules {#unlimited_report_server_profiles}

Basic members can create one [report server](../capture/report-server) rule. Premium members can create an unlimited number of rules.

![](./arts/report-server.png)

### Unlimited gRPC Definition Rules {#unlimited_grpc_definition_rules}

Basic members can create up to three `gRPC definition` rules. Premium members can create an unlimited number of rules.

![](./arts/grpc-definition.png)

### Unlimited Protobuf Definition Rules {#unlimited_protobuf_definition_rules}

Basic members can create up to three `Protobuf definition` rules. Premium members can create an unlimited number of rules.

![](./arts/protobuf-definition.png)

### Unlimited Favorite Folders {#unlimited_favorite_folder}

Basic members cannot create custom favorite folders. Premium members can create as many favorite folders as they need.

![](./arts/favorite-folder.png)

:::info
- Creating custom favorite folders is not yet supported on mobile devices.
:::

### Unlimited Favorite Requests {#unlimited_favorite_save_items}

Basic members can save up to ten requests to favorites. Premium members can save an unlimited number of requests.

:::info
- Favorites cannot yet be synced to the cloud.
:::

### Unlimited Bookmark Folders {#unlimited_bookmark_folder}

Basic members cannot create custom bookmark folders. Premium members can create as many bookmark folders as they need.

![](./arts/bookmark-folder.png)

:::info
This feature is not yet available on mobile devices.
:::

### Unlimited Bookmarks {#unlimited_bookmark_save_items}

Basic members can create up to ten bookmarks. Premium members can create an unlimited number of bookmarks.

:::info
- Bookmarks cannot yet be synced to the cloud.
- This feature is not yet available on mobile devices.
:::

### Unlimited Capture History Access {#unlimited_history_review}

Basic members can view capture history from the past 30 days. Premium members are not subject to this limit.

### Multi-Condition Search {#unlimited_search_conditions}

Basic members can search captured traffic using only one condition. Premium members can combine up to five conditions in a search.

![](./arts/filter-search.png)

### Unlimited Saved Search Filters {#unlimited_save_filters}

Basic members can save one search filter. Premium members can save an unlimited number of filters.

![](./arts/filter-save.png)

### Unlimited Capture Sessions {#unlimited_capture_sessions}

Basic members can use one capture session. Premium members can use an unlimited number of sessions.

![](./arts/sessions.png)

### Unlimited Highlight Conditions {#unlimited_capture_highlight_conditions}

When configuring automatic highlighting for captured traffic, Basic members can use only one condition. Premium members can use an unlimited number of conditions.

![](./arts/highlight.png)

### Unlimited Request and Response Comparisons {#unlimited_capture_diff_items}

When comparing captured traffic, Basic members can add only two request items. Premium members can add an unlimited number of items.

![](./arts/diff.png)

### Unlimited Detached Windows {#unlimited_capture_session_window}

Basic members can open one detached window to view captured traffic details. Premium members can open an unlimited number of detached windows.

![](./arts/session-window.png)

:::info
This feature is not yet available on mobile devices.
:::

### IP Lookup {#ip_query}

The Reqable toolbox includes an IP geolocation lookup tool. This feature is available exclusively to Premium members.

![](./arts/ip.png)

:::info
This feature is not yet available on mobile devices.
:::

### Multi-Device Capture Collaboration {#unlimited_collaborations}

When adding collaboration devices on mobile, Basic members can add only one device. Premium members can add an unlimited number of devices.

![](./arts/collaboration.png)

### Multi-App Capture {#unlimited_target_apps}

When selecting apps to capture traffic from on mobile, Basic members can select only one app. Premium members can select an unlimited number of apps.

![](./arts/target-app.png)

:::info
This feature is not yet available on desktop.
:::

### Enhanced Capture Mode {#capture_enhanced_mode}

Premium members can enable enhanced capture mode on mobile devices. Enhanced mode offers the following benefits:

- Intercept all system traffic without missing any traffic.
- Identify the source app for traffic on Android.

![](./arts/enhanced-mode.png)

:::info
Enhanced mode is not yet available on desktop, but support is planned.
:::

### AES Encryption and Decryption {#crypto_aes}

The Reqable toolbox includes an AES encryption and decryption tool that supports `CBC`, `CFB`, `CTR`, `ECB`, `OFB`, `SIC`, and `GCM` modes. This feature is available exclusively to Premium members.

![](./arts/aes.png)

:::info
This feature is not yet available on mobile devices.
:::
