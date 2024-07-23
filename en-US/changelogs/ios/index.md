---
sidebar_position: 5
---

# iOS

## v2.21.0 <small><small>*2024-07-23*</small></small>
- 🚀 [NEW] Support editing HAR files.
- 🚀 [NEW] Support access control.
- 🚀 [NEW] Support text editing mode for form-data.
- 🚀 [NEW] Copy query parameters, headers, etc. as JSON.
- 🚀 [NEW] Add `Settings` in the side menu.
- 🚀 [NEW] Add `Feedback` in the side menu.
- 🚀 [NEW] Add `Review App` in the side menu.
- 💪 [OPT] Tab title style and indicator style.
- 💪 [OPT] HAR export request and response body do not use base64 encoding first.
- 💪 [OPT] Compatible with some non-standard IPv6 proxy requests.
- 🐞 [FIX] The bug that that may fail to open HAR file.
- 🐞 [FIX] Secondary proxy authentication issue.
- 🐞 [FIX] The bug that SSL proxy cannot hit some HTTPS requests.
- 🐞 [FIX] A bug that highlighted information is lost when opening sub-list from the grouped host.

## v2.20.2 <small><small>*2024-07-16*</small></small>
- 💪 [OPT] Key-value pair type data supports copying as JSON.
- 🐞 [FIX] The bug that may fail to open HAR file.

## v2.20.1 <small><small>*2024-07-12*</small></small>
- 💪 [OPT] Support HEX viewer for raw message.
- 💪 [OPT] Delete duplicate java.net.http code snippet.
- 💪 [OPT] API testing supports sending request with empty request header value.
- 🐞 [FIX] A bug where importing raw multipart curl loses the last Part.
- 🐞 [FIX] Incorrect implementations for websocket extensions.
- 🐞 [FIX] Open a HAR file will lost the highlighting.

## v2.20.0 <small><small>*2024-07-08*</small></small>
- 🚀 [NEW] Introduce report server feature.
- 🚀 [NEW] Supports `Zstandard` encoding and decoding.
- 🚀 [NEW] Supports C# HttpClient and RestSharp code snippet.
- 🚀 [NEW] Supports Java Apache HttpClient code snippet.
- 🚀 [NEW] Supports raw multipart data from curl.
- 💪 [OPT] SSL proxy rules support configuring port numbers.
- 💪 [OPT] Improve API request cURL import and export input box.
- 💪 [OPT] Improve multipart table mode UI/UX.
- 💪 [OPT] After initializing with collaborative mode, will automatically switch to the remote device page.
- 🐞 [FIX] The bug of syntax highlighting rendering.
- 🐞 [FIX] The bug that request parameters may be lost when reading HAR files.
- 🐞 [FIX] A bug where the host grouping page displays irrelevant domain name data.

## v2.19.1 <small><small>*2024-07-02*</small></small>
- 💪 [OPT] API requests give priority to using custom Host as SNI.
- 💪 [OPT] API request parameters, headers, and form editing automatically convert JSON key-value pairs.
- 💪 [OPT] curl import and export support `--insecure` option.
- 🐞 [FIX] The bug of the top safe area height being too large.

## v2.19.0 <small><small>*2024-06-26*</small></small>
- 🚀 [NEW] Support enhanced mode and non-enhanced capture mode.
- 💪 [OPT] The traffic export provides more options.
- 💪 [OPT] The image preview displays information such as format, size and size.
- 🐞 [FIX] The bug that the remote device details page do not exit after deleting the device.

## v2.18.1 <small><small>*2024-06-17*</small></small>
- 💪 [OPT] Cookie view allows cookies to be displayed in a merged or split.
- 💪 [OPT] Traffic list allows cURLs for multiple requests to be copied at once.
- 💪 [OPT] Traffic list allows multiple API requests to be created at once.
- 💪 [OPT] More options are provided for sharing and exporting traffic item.
- 💪 [OPT] Long press menu of collaborative device in sidebar supports deleting device.
- 💪 [OPT] Title action menu of collaborative device supports viewing device info.
- 💪 [OPT] Click the warning icon in the collaborative device title bar can synchronize the certificate directly instead of jumping to the device detail page.
- 🐞 [FIX] A bug that ALPN is displayed incorrectly.
- 🐞 [FIX] A bug that some empty tips are displayed incorrectly.
- 🐞 [FIX] A bug that using IP by SOCKS proxy are automatically bypassed by SSL proxying.
- 🐞 [FIX] A bug that restarting MITM proxy server may fail.
- 🐞 [FIX] The bug that the collaborative device synchronization data will reset the device name.
- 🐞 [FIX] The bug that the status of the warning icon in the collaborative device title bar is not updated in time.

## v2.18.0 <small><small>*2024-06-11*</small></small>
- 🚀 [NEW] WebSocket frames support search and filtering.
- 💪 [OPT] Improve the prompt text for errors of certificate import and export.
- 💪 [OPT] The `=` in the API request URL is no longer automatically encoded.
- 🐞 [FIX] The bug that single quotes are not escaped when importing and exporting cURL.
- 🐞 [FIX] The bug that the SSL certificate enable/disable status cannot be saved.
- 🐞 [FIX] The bug that the SSL certificate domain name modification cannot be saved.

## v2.17.0 <small><small>*2024-06-05*</small></small>
- 🚀 [NEW] Support `SSL Proxying`.
- 🚀 [NEW] Add a search icon in `Raw` tab.
- 💪 [OPT] Remove `SSL Bypass` and merge it into the `SSL Proxying`.
- 💪 [OPT] Provide more export solutions for capture traffic.
- 💪 [OPT] Automatically remember word wrap status.
- 🐞 [FIX] A bug that the API request Cookie path is forcibly converted to lowercase.
- 🐞 [FIX] A bug that the SOCKS proxy does not display the host if hits SSL bypass.

## v2.16.1 <small><small>*2024-05-20*</small></small>
- 🚀 [NEW] Support starting app from HAR file.
- 💪 [OPT] HTTP2 disables server push by default.
- 💪 [OPT] Traffic list in host view will receive updates.
- 🐞 [FIX] The bug of gray screen when opening from host traffic list.

## v2.16.0 <small><small>*2024-05-17*</small></small>
- 🚀 [NEW] WebSocket supports list display mode.
- 🚀 [NEW] Request parameter supports whether to omit `=` for empty value.
- 💪 [OPT] Creating API requests from the traffic list no longer checks non-ASCII characters.
- 💪 [OPT] The default display of WebSocket is changed from chat mode to list mode.
- 💪 [OPT] WebSocket chat mode performance.
- 🐞 [FIX] The bug where WebSocket filtering does not reset type and code filters.

## v2.15.1 <small><small>*2024-05-13*</small></small>
- 💪 [OPT] Prompted to turn off SSL certificate verification when a certificate error occurs.
- 💪 [OPT] The count of sub-files is displayed after the API collection name.
- 💪 [OPT] API collection supports expanding/collapsing all subfolders.
- 🐞 [FIX] The bug of HTTP proxy request failure in some cases.
- 🐞 [FIX] The bug of losing request headers when importing Reqable collection.

## v2.15.0 <small><small>*2024-05-09*</small></small>
- 🚀 [NEW] Supports configuring custom SSL certificates.
- 🚀 [NEW] Supports previewing SSL certificate details in capture overview.
- 🚀 [NEW] Supports creating REST API from redirected URLs.
- 💪 [OPT] Certificate info will display more details.
- 💪 [OPT] Adjust the UI details of redirect Tab.
- 💪 [OPT] The copy button of `Cookie View` will copy the full cookie string instead of the key-value pair.
- 🐞 [FIX] A bug where `Content-Type` may be lost when copying cURL from traffic list.
- 🐞 [FIX] The bug that the content of the client certificate in the overview is incorrect.

## v2.14.1 <small><small>*2024-04-30*</small></small>
- 💪 [OPT] Traffic analysis supports abnormal requests with `Content-Length`.
- 💪 [OPT] The file name of request and response body.
- 💪 [OPT] API testing no longer verifies the validity of response headers.
- 🐞 [FIX] The bug that the secondary proxy connection may fail.
- 🐞 [FIX] The bug of API testing settings being reset after restarting the application.
- 🐞 [FIX] A bug where some files were not cleaned after deleting the API testing history.
- 🐞 [FIX] The bug that parsing API testing query input incorrectly.
- 🐞 [FIX] The bug that root certificate cannot be downloaded in collaboration mode.

## v2.14.0 <small><small>*2024-04-29*</small></small>
- 💪 [OPT] Traffic analysis supports abnormal requests with `Content-Length`.
- 💪 [OPT] The file name of request and response body.
- 💪 [OPT] API testing no longer verifies the validity of response headers.
- 🐞 [FIX] The bug that the secondary proxy connection may fail.
- 🐞 [FIX] The bug of API testing settings being reset after restarting the application.
- 🐞 [FIX] A bug where some files were not cleaned after deleting the API testing history.
- 🐞 [FIX] The bug that root certificate cannot be downloaded in collaboration mode.

## v2.13.0 <small><small>*2024-04-24*</small></small>
- 🚀 [NEW] API testing supports setting whether to verify SSL certificate.
- 🚀 [NEW] API testing response displays redirect URLs.
- 💪 [OPT] Clear cache in settings will only clear temporary data and not include user data.
- 💪 [OPT] Reduce the size of the toolbar menu that pops up after selection in the editor.
- 💪 [OPT] UI details of license pricing page.
- 🐞 [FIX] The bug that the redirected request will fail due to incorrect `Host` header value.
- 🐞 [FIX] The bug that `OPTIONS` request status is incorrect.
- 🐞 [FIX] The bug of clearing cache and resetting app in settings does not take effect.

## v2.12.1 <small><small>*2024-04-19*</small></small>
- 🐞 [FIX] The bug of API request global setting not taking effect in some cases.
- 🐞 [FIX] The bug that the API request domain name cannot be associated with cookies when using environment variables.
- 🐞 [FIX] The bug that `=` and `&` in API request query entry are not automatically encoded.
- 🐞 [FIX] A bug that some exceptions caused by automatic decoding of API query when created from the traffic list.
- 🐞 [FIX] The bug that the table mode input autocomplte list will be display incomplete near the bottom of the application.
- 🐞 [FIX] A bug that may cause crash when importing p12 certificate.

## v2.12.0 <small><small>*2024-04-13*</small></small>
- 🚀 [NEW] Supports purchasing lifetime professional license.
- 💪 [OPT] Prompt whether to clear license information when unregistering license.
- 💪 [OPT] Automatically delete configuration backup files older than 14 days.

## v2.11.1 <small><small>*2024-04-09*</small></small>
- 🚀 [NEW] Remove the restriction of API collections for Community Edition.
- 💪 [OPT] Remove the restriction that the depth of API collections is up to 4.
- 💪 [OPT] Display text first if `application/octet-stream` is a text.
- 💪 [OPT] Adjust the UI margin of the traffic list.
- 💪 [OPT] Adjust the URL display color in the traffic list.
- 🐞 [FIX] The bug of incorrect toolbar position of the code editor.
- 🐞 [FIX] The bug that the selector handles are not displayed after the code editor is long pressed.

## v2.10.1 <small><small>*2024-04-02*</small></small>
- 💪 [OPT] Query parameter parsing automatically identifies gbk encoding.
- 💪 [OPT] Open a new page instead of a dialog to view url.
- 🐞 [FIX] The bug that the environment variable `<<url>>` is not highlighted.
- 🐞 [FIX] The bug of abnormal `chunked` decoding in some cases.
- 🐞 [FIX] The bug that exporting HAR throws the format error.

## v2.10.0 <small><small>*2024-03-29*</small></small>
- 🚀 [NEW] Support opening all APIs in the collection at one time.
- 🚀 [NEW] Increase the available number of API collections for Community Edition users from 2 to 3.
- 🚀 [NEW] Increase the available number of Environments for Community Edition users from 2 to 3.
- 🐞 [FIX] A bug where duplicate encoding of request parameters in code generation.
- 🐞 [FIX] Corrected the logic for saving form requests in API testing.
- 🐞 [FIX] A bug where there was an exception in parsing text for API request parameters.
- 🐞 [FIX] A bug where parameters and headers starting with `_` were not highlighted.
- 🐞 [FIX] A bug where environment name is empty.
- 🐞 [FIX] A bug where illegal values in Set-Cookie were not displayed correctly.
- 🐞 [FIX] The bug of incorrect HEX export data.
- 🐞 [FIX] A bug where input content was lost in certain scenarios in the text editor.

## v2.9.0 <small><small>*2024-03-22*</small></small>
- ❗ [IMP] The minimum supported version is upgraded from 11.0 to 12.0.
- 🚀 [NEW] Introduce environment variables.
- 🚀 [NEW] Now can rename the API request.
- 💪 [OPT] Generate Python-Requests code using query parameters instead of long url.
- 🐞 [FIX] The bug that API can not use Python script to process form data.
- 🐞 [FIX] The bug that API space will encodes to `%20` rather than `+`.
- 🐞 [FIX] The bug that it will prompt to save when closing the API test tab.
- 🐞 [FIX] The bug that correctly to handle `--data-raw` when importing a cURL.

## v2.8.2 <small><small>*2024-03-06*</small></small>
- 💪 [OPT] Coloring request methods.
- 💪 [OPT] Correct some tips.
- 🐞 [FIX] The bug of importing ApiFox collection failed in some cases.
- 🐞 [FIX] The bug where the response raw message is incorrect.
- 🐞 [FIX] Incorrect highlighting of query parameters and cookies.
- 🐞 [FIX] The bug where `startedDateTime` of the exported HAR format is incorrect.

## v2.8.0 <small><small>*2024-02-29*</small></small>
- 🚀 [NEW] Available API tabs of community version are increased from 2 to 4.
- 🚀 [NEW] Adds three new tabs, Cookies, Set-Cookies and Comment.
- 🚀 [NEW] Now you can comment a traffic record.
- 🚀 [NEW] Custom request and response tabs.
- 💪 [OPT] Adjust the margins of the dialogs.
- 🐞 [FIX] The cookie automatic update mechanism causes a bug that requires saving when closing a API Tab.
- 🐞 [FIX] The bug of incorrect parsing of the '--data-urlencode' parameter when importing a cURL.
- 🐞 [FIX] The bug in which the content displayed in the Tab title is truncated.
- 🐞 [FIX] The bug where `wss` in HAR file is recognized as `ws`.
- 🐞 [FIX] The bug where the content at the bottom of some dialogs is incompletely displayed.
- 🐞 [FIX] The bug that the editor toolbar display and disappear are incorrectly handled.

## v2.7.1 <small><small>*2024-02-22*</small></small>
- 💪 [OPT] HEX will be displayed first when the image data decoding fails.
- 🐞 [FIX] The bug of incorrect encoding and decoding of URL query parameters.
- 🐞 [FIX] The bug in parsing HAR files does not correctly handle the MIME type.
- 🐞 [FIX] The bug of secondary proxy account authentication not works.
- 🐞 [FIX] The bug that the file selection not works.

## v2.7.0 <small><small>*2024-02-20*</small></small>
- 🐞 [FIX] The bug that the unmodified API will prompt to save when closing.
- 🐞 [FIX] The bug that closing other tabs will close all tabs.
- 🐞 [FIX] The bug of incorrect encoding of `space` and `=` in request query parameters.

## v2.6.3 <small><small>*2024-02-07*</small></small>
- 💪 [OPT] Remote device will wait for 5 seconds to reconnect.

## v2.6.2 <small><small>*2024-02-04*</small></small>
- 🐞 [FIX] A bug where some webSocket requests are not recognized.

## v2.6.1 <small><small>*2024-01-31*</small></small>
- 🚀 [NEW] Code editor supports code auto-completion.
- 🚀 [NEW] Supports manual input the remote device address in collaboration mode initialization.
- 🐞 [FIX] The bug that text syntax highlighting may be incorrect.
- 🐞 [FIX] The bug that missing `/` at the end of URL.
- 🐞 [FIX] The bug that `HexViewer` will get focus by default.
- 🐞 [FIX] The bug that IP was displayed rather than host.
- 🐞 [FIX] The bug that the rescanned device address displays incorrectly after the remote device address changes.
- 🐞 [FIX] The bug that the collaboration mode does not work after the app moves to background for a period of time.

## v2.5.0 <small><small>*2024-01-25*</small></small>
- 🚀 [NEW] Introduce scripting for API testing.
- 🚀 [NEW] Introduce script templates.
- 🚀 [NEW] Fork templates from public script repositories.
- 🚀 [NEW] Introduce zen mode.
- 💪 [OPT] New console for script editor.
- 💪 [OPT] Remember highlight and application informations when saving HAR files.
- 💪 [OPT] Try to reconnect after the remote device is disconnected.
- 🐞 [FIX] The secondary proxy may cause an infinite loop of requests.
- 🐞 [FIX] The bug that unable to capture HTTP2 plaintext traffic.
- 🐞 [FIX] The bug that handling HTTP trailer incorrectly.
- 🐞 [FIX] The bug of failing to handle WebSocket compression extension correctly.
- 🐞 [FIX] The bug that text selection is incorrect after double-clicking a word.
- 🐞 [FIX] The bug that the editor composing menu does not follow the input position.
- 🐞 [FIX] The bug that the remote device connection status displays incorrectly.

## v2.4.1 <small><small>*2024-01-16*</small></small>
- 💪 [OPT] Use form body when creating API requests from the form request cURL.
- 💪 [OPT] Coloring response status line.
- 🐞 [FIX] The bug of duplicate cookie values in the code snippet.
- 🐞 [FIX] The bug that unable to decode deflate data.
- 🐞 [FIX] A bug that may trigger content selection when scrolling the editor.
- 🐞 [FIX] The bug that unable to copy cURL of the WebSocket request.
- 🐞 [FIX] The bug of failing to handle WebSocket compression extension correctly.
- 🐞 [FIX] The bug that cannot create form request or copy cURL from traffic list.
- 🐞 [FIX] The bug that auto-highlighting configuration cannot be saved.
- 🐞 [FIX] The bug that search does not work.

## v2.4.0 <small><small>*2024-01-12*</small></small>
- 🚀 [New] Introduce a new secondary proxy feature.
- 🚀 [New] Supports double-clicking the title to open the search bar.
- 🚀 [New] Supports opening the browser to download the CA certificate description file.
- 🐞 [FIX] The bug that the generated cURL does not merge cookies.
- 🐞 [FIX] The bug that the `Referer` header cannot be sent in API requests.
- 🐞 [FIX] The bug of missing `application/x-www-form-urlencoded` header in code snippet.
- 🐞 [FIX] A bug that may crash when exporting P12 format certificate.
- 🐞 [FIX] The bug where the proxy port number display is inconsistent with the actual one.
- 🐞 [FIX] The bug that the remote device may not be able to coordinate after the address is changed.
- 🐞 [FIX] The bug that the network will get stuck when entering the background.

## v2.3.2 <small><small>*2024-01-08*</small></small>
- 💪 [OPT] Adjustment of some UI details.
- 🐞 [FIX] The bug that the raw message in the traffic details cannot be code highlighted.
- 🐞 [FIX] The bug that JSON array type throws an error int code snippet.
- 🐞 [FIX] The selection handles render incorrectly after long pressing to select.
- 🐞 [FIX] The bug that CONNECT requests can be repeated.

## v2.3.0 <small><small>*2024-01-05*</small></small>
- 🚀 [NEW] Upgrade the Flutter framework to the latest version 3.16.5.
- 🚀 [NEW] Use Material Design 3 styles.
- 🚀 [NEW] 15 code syntax highlighting color options.
- 🚀 [NEW] Add the application ID column for traffic list.
- 🚀 [NEW] Context menu for traffic overview URL.
- 🚀 [NEW] Introduce secondary proxy for SOCKS and VPN modes.
- 🚀 [NEW] Remote app can control the recording status of the host app.
- 💪 [OPT] Adjust the proxy port detection logic and automatically change the port number when a conflict is detected.
- 💪 [OPT] URL syntax highlighting supports universal schemes.
- 💪 [OPT] Apply URL syntax highlighting for QR code input text.
- 💪 [OPT] The traffic record in collaborative mode will display domain name instead of IP address.
- 💪 [OPT] Enable horizontal scroll gesture to switch tabs.
- 🐞 [FIX] The bug that the urlencode request body may be lost when parsing HAR files.
- 🐞 [FIX] A failure with non-standard HAR connection fields.
- 🐞 [FIX] The bug that the uppercase encoding value such as GZIP cannot be recognized.
- 🐞 [FIX] The bug that the keyboard will pop up when scrolling code editor content.

## v2.2.0 <small><small>*2023-12-28*</small></small>
- 🚀 [NEW] API testing supports splitting merged cookies into multiple ones.
- 🚀 [NEW] API testing supports opening additional editors to edit cookies.
- 💪 [OPT] Prevent URL from wrapping automatically in traffic list.
- 💪 [OPT] Remove the custom transition animation effect of entering details from the traffic list.
- 🐞 [FIX] The bug where some items in the traffic list were sorted incorrectly.
- 🐞 [FIX] The bug that the application cannot start in some cases.

## v2.1.1 <small><small>*2023-12-25*</small></small>
- 🚀 [NEW] Allow root certificate regeneration.
- 🚀 [NEW] You can share the app from side drawer.
- 🚀 [NEW] You can add a traffic item to API collections and ssl-bypass rules.
- 💪 [OPT] API testing `reqableId` supports displaying in two lines.
- 💪 [OPT] API testing will automatically fill key-value entries when switching from text.
- 💪 [OPT] Use an external browser to open links instead of within the app.
- 🐞 [FIX] The bug that it is unable to install root certificate.
- 🐞 [FIX] The bug of abnormal display of collaborative QR code when there is no local IP.
- 🐞 [FIX] A bug that the mirror icon will display incorrectly in some cases.
- 🐞 [FIX] A bug where the traffic list application name was too long.

## v2.0.0 <small><small>*2023-12-15*</small></small>
- 🚀 [NEW] First version!
