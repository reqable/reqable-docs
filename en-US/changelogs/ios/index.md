---
sidebar_position: 5
---

# iOS

## v3.1.0 <small><small>*2026-05-09*</small></small>
- 🚀 [New] Introduce API documentation feature.
- 🚀 [New] Redesign capture gateway, supporting network Layer4 and Layer7 configurations and other new features.
- 🚀 [New] Redesign SSE view, supporting raw view and Markdown preview.
- 🚀 [New] Redesign remote device management features.
- 🚀 [New] Add rename option in the API collection and folder settings page menu.
- 💪 [OPT] Upgrade OpenSSL version to 3.6.1.
- 💪 [OPT] Align API names in the API collection list.
- 💪 [OPT] SSE chat view now limits each text message to 4k characters.
- 💪 [OPT] SSE list may experience lag due to long text.
- 💪 [OPT] WebSocket chat view now limits each text message to 4k characters.
- 💪 [OPT] WebSocket list may experience lag due to long text.
- 💪 [OPT] Update Magisk module template.
- 🐞 [FIX] The bug where capturing failed when the server used new algorithms like X25519MLKEM768.
- 🐞 [FIX] The bug where the application crashed when the API carried a non-standard `Referer` header.
- 🐞 [FIX] The bug where `Content-Type` was displayed incorrectly in the capture overview.
- 🐞 [FIX] The bug where API collection and folder settings did not sync correctly with the cloud.
- 🐞 [FIX] The bug where API request Cookie headers were not automatically updated.
- 🐞 [FIX] The bug where the order of cURL request headers was incorrect when copying from traffic list.

## v3.0.40 <small><small>*2026-03-27*</small></small>
- 🐞 [FIX] The bug where the response data in the raw tab did not automatically update.
- 🐞 [FIX] A bug in the curl command where the `-no-buffer` option causes import failures.
- 🐞 [FIX] The bug where JSONP data with a trailing semicolon was not formatted correctly.

## v3.0.39 <small><small>*2026-03-06*</small></small>
- 💪 [OPT] Support adding multiple records from the traffic list to API collection at once.
- 💪 [OPT] Go code snippet now fully supports form requests.
- 💪 [OPT] Optimize error message when opening HAR files.
- 🐞 [FIX] The bug where SSL exceptions with Missing Authority Key Identifier might occur during capture.
- 🐞 [FIX] The bug where data in the capture overview did not update with request status.
- 🐞 [FIX] The bug where binary data in non-ASCII headers in the raw tab of the capture details was incorrect.
- 🐞 [FIX] The bug where custom encoding without specifying the encoding type in `Content-Disposition` caused file names to appear garbled when saving response content.
- 🐞 [FIX] A bug in the curl command where the `-g` option causes import failures.

## v3.0.38 <small><small>*2026-02-02*</small></small>
- 🐞 [FIX] The bug where SOCKS proxy URLs were not syntax highlighted.
- 🐞 [FIX] The bug where URL syntax highlighting for IPv6 addresses was abnormal.
- 🐞 [FIX] The bug where IPv6 address requests were interrupted under SOCKS proxy.
- 🐞 [FIX] The bug where URL was incorrect when creating IPv6 requests from the traffic list.
- 🐞 [FIX] The bug where enabling follow debug caused the application to crash with IPv6 requests.
- 🐞 [FIX] The bug where the new version changelog did not refresh after switching languages in app settings.

## v3.0.37 <small><small>*2026-01-22*</small></small>
- 🐞 [FIX] The bug where the port number for HTTP access to the local server may be incorrect.

## v3.0.36 <small><small>*2026-01-20*</small></small>
- 💪 [OPT] Update CA certificate download link.

## v3.0.35 <small><small>*2026-01-19*</small></small>
- 💪 [OPT] Support input and parsing of `foo=bar&abc=123` format in urlencode request text mode.

## v3.0.34 <small><small>*2026-01-16*</small></small>
- 💪 [OPT] Code snippet supports Dart-Dio.
- 💪 [OPT] JSON Tree view will remember the last search type.

## v3.0.33 <small><small>*2026-01-07*</small></small>
- 💪 [OPT] Automatically format node content in JSON tree view.
- 💪 [OPT] WebSocket testing will cache the last sent message.
- 🐞 [FIX] The bug where HTTP redirects did not correctly handle current path redirects.

## v3.0.32 <small><small>*2026-01-05*</small></small>
- 💪 [OPT] In the Cookie view, copying icon now copies the concatenated cookie string instead of key-value entries.
- 💪 [OPT] JSON tree view node context menu adds copy dictionary path option.
- 💪 [OPT] Protocol version is no longer specified when copying cURL from the traffic list.
- 💪 [OPT] Code snippet for Java-HttpClient adds main method and prints body text to console.
- 🐞 [FIX] The bug where code snippet for Java-HttpClient did not correctly handle query and form encoding.
- 🐞 [FIX] The bug where code snippet for Python-http.client did not correctly handle query and form encoding.
- 🐞 [FIX] The bug where WebSocket details changed with data updates.
- 🐞 [FIX] The bug where SSE details changed with data updates.

## v3.0.31 <small><small>*2025-12-25*</small></small>
- 🚀 [New] Code snippet supports setting indentation.
- 🚀 [New] Code snippet for Python-Requests supports whether to use dictionary parameters.
- 💪 [OPT] Added background color to third-party login icon buttons.
- 💪 [OPT] API testing can inherit common headers defined in the folder when the current is not selected.
- 💪 [OPT] API testing can inherit common parameters defined in the folder when the current is not selected.
- 💪 [OPT] Automatically fill in the `Content-Length` header when generating cURL if a request body is expected but not present.
- 🐞 [FIX] The bug where exporting cURL did not correctly handle duplicate headers.
- 🐞 [FIX] The bug where code snippet did not correctly handle duplicate headers.

## v3.0.30 <small><small>*2025-12-08*</small></small>
- 💪 [OPT] form-data parts no longer send Content-Length headers.
- 🐞 [FIX] The bug where cURL import failed due to CRLF line-break.
- 🐞 [FIX] The bug where cURL import of form-data requests lost custom part headers.
- 🐞 [FIX] The bug where the text editor did not correctly locate the next match after replacing content.

## v3.0.29 <small><small>*2025-12-04*</small></small>
- 💪 [OPT] Add refresh option to HAR tab context menu.
- 🐞 [FIX] Digest authorization did not correctly handle environment variables.

## v3.0.28 <small><small>*2025-11-18*</small></small>
- 💪 [OPT] Replace cURL command parser.
- 💪 [OPT] Importing curl no longer blocks if a file is not found.
- 💪 [OPT] form-data adds a warning for missing files.
- 💪 [OPT] Compatible with some non-standard `content-type` types.
- 🐞 [FIX] HEX view in WebSocket and SSE could not gain focus, causing shortcut keys to be not working.
- 🐞 [FIX] SSE view in traffic list did not display data due to encodings.
- 🐞 [FIX] XML prettify did not correctly handle nested `>` and `<` characters.
- 🐞 [FIX] Importing cURL did not handle single and double quotes correctly.

## v3.0.27 <small><small>*2025-11-18*</small></small>
- 💪 [OPT] Display all new version logs during version updates.
- 💪 [OPT] Display VPN addresses in the IP list.
- 💪 [OPT] Automatically clean up outdated log files.
- 🐞 [FIX] Remove trailing `;` when importing cURL headers with empty values.
- 🐞 [FIX] Application does not automatically open files when launched from file association.
- 🐞 [FIX] API request tab save prompt status not displaying correctly in some cases.
- 🐞 [FIX] Tabs did not restore the previously selected remote device after app restart.

## v3.0.26 <small><small>*2025-11-14*</small></small>
- 💪 [OPT] Improve the logic for creating APIs from raw HTTP messages.
- 💪 [OPT] cURL import input box automatically gains focus.
- 💪 [OPT] cURL import automatically filters leading and trailing spaces and line breaks.
- 💪 [OPT] API request form supports selecting multiple files at once.
- 💪 [OPT] API request body formdata will show more action icon by default.
- 💪 [OPT] API request body formdata switches to file type automatically open file selector.
- 💪 [OPT] API request body formdata switches to multiline text type automatically open text editor and focus.
- 🐞 [FIX] Data is not displayed initially in non-table mode.
- 🐞 [FIX] API request apikey authorization value was used incorrectly.
- 🐞 [FIX] Email addresses containing `+` were not passing validation.

## v3.0.24 <small><small>*2025-11-12*</small></small>
- 🐞 [FIX] Data loss of secondary folders when upgrading from versions before v2.32.0 to the new version.

## v3.0.23 <small><small>*2025-11-11*</small></small>
- 💪 [OPT] Check if the current version is a downgrade and display a warning.
- 🐞 [FIX] API authorization referencing environment variables not taking effect.
- 🐞 [FIX] API authorization type switching not taking effect.
- 🐞 [FIX] WebSocket request header case sensitivity issue.
- 🐞 [FIX] Custom theme color settings are not working.
- 🐞 [FIX] Rewrite query parameters are double encoded.
- 🐞 [FIX] Unable to open HAR files.
- 🐞 [FIX] Opening history and favorites did not correctly display loading and error messages.

## v3.0.22 <small><small>*2025-11-05*</small></small>
- 💪 [OPT] Improve login and registration process.
- 💪 [OPT] Add compatibility check for `curl_close` in generated PHP code.
- 🐞 [FIX] `{{` and `}}` in JSON would be incorrectly replaced with `<<` and `>>` when importing collection data.
- 🐞 [FIX] WebSocket requests created from the sidebar `+` menu were incorrectly created as HTTP requests.

## v3.0.21 <small><small>*2025-11-05*</small></small>
- ❗ [IMP] The minimum supported version is upgraded from 12.0 to 13.0.
- 🚀 [NEW] Changed premium authorization from license to account.
- 🚀 [NEW] Support for cloud data storage.
- 🚀 [NEW] Support for multi-device synchronization and collaboration.
- 🚀 [NEW] A new tab for environment variable editing.
- 🚀 [NEW] Now can preview SVG images.
- 💪 [OPT] Changed the URL auto-completion scheme from https to http.
- 💪 [OPT] cURL import will automatically handle JSON escape characters.
- 💪 [OPT] Improved error message for environment variable name.
- 💪 [OPT] In code snippet, using dynamic import for Node fetch in code snippet.
- 💪 [OPT] In code snippet, axios outputs the response body instead of the entire response object.
- 💪 [OPT] Entries are now displayed in text mode instead of table mode by default.
- 💪 [OPT] Ignore traffic records larger than 16MB when searching to prevent OOM.
- 🐞 [FIX] Rewrite help document path redirected incorrectly.
- 🐞 [FIX] Closing a newly created, unedited API would prompt a save request.
- 🐞 [FIX] Urlencode encoding was incorrect.
- 🐞 [FIX] Custom proxy settings for API testing were not saved correctly.
- 🐞 [FIX] The tab modification status was not updated in time when the API request body was modified.
- 🐞 [FIX] API redirection failed to handle the location starting with `//`.
- 🐞 [FIX] API request global settings did not take effect in certain scenarios.
- 🐞 [FIX] API request inherited basic auth environment variables were not resolved.
- 🐞 [FIX] API request basic auth environment variables were not effective after switching the current environment.
- 🐞 [FIX] Hoppscotch environment variables were lost after import.
- 🐞 [FIX] Malformed cookies could cause the app to freeze.
- 🐞 [FIX] Cookie creation and editing did not take effect.
- 🐞 [FIX] Some HAR files could not be parsed correctly.
- 🐞 [FIX] Search results in the text editor could be obscured.
- 🐞 [FIX] HTTP2 requests could fail in certain situations.
- 🐞 [FIX] Selecting items in the traffic list and adding it to a new session would clear the list.
- 🐞 [FIX] Input an invalid regex in HexViewer search would cause always no result.
- 🐞 [FIX] Long press options on the tab and Tooltip conflicted.
- 🐞 [FIX] Paste multi-line text from the IME's clipboard will make text editor display abnormally.
- 🐞 [FIX] Tab index in history page is incorrect.
- 🐞 [FIX] Version update prompt was obscured by the bottom navigation bar.

## v2.33.12 <small><small>*2025-04-23*</small></small>
- 💪 [OPT] Reduce memory usage and lag in some scenarios.
- 💪 [OPT] Large data is displayed as `<...>` in the raw tab to avoid performance issues.
- 💪 [OPT] Python-Requests code snippet will use full url instead of param dict.
- 💪 [OPT] The `=` in the parameter value of URL is no longer automatically transcoded to `%3D`.
- 💪 [OPT] Collaborative QR code IP address list will remove the VPN virtual address.
- 🐞 [FIX] The bug that the parameter name and parameter value of the URL will be lost when both are empty.
- 🐞 [FIX] A bug that caused a traffic loop when accessing the device remotely after switching networks.

## v2.33.11 <small><small>*2025-04-22*</small></small>
- 💪 [OPT] SSE list supports switching between positive and reverse order.
- 💪 [OPT] WebSocket list supports switching between forward and reverse order.
- 🐞 [FIX] The bug that the WebSocket frame read status is incorrect after search and filtering.
- 🐞 [FIX] The bug that the HTTP method of the new location is not changed to GET during 301, 302 and 303 redirection.
- 🐞 [FIX] The bug that the icon button may not trigger the click event when clicked continuously.

## v2.33.10 <small><small>*2025-04-21*</small></small>
- 💪 [OPT] When MIME is non-text type, the data will not be detected for character encoding.
- 💪 [OPT] API testing turns off `Follow Debug` will switch to `Unset` instead of `Follow System`.
- 🐞 [FIX] The bug that data saved under the `Hex` may not be the displayed data.

## v2.33.9 <small><small>*2025-04-15*</small></small>
- 💪 [OPT] Copy as JSON will automatically remove the built-in empty value header.

## v2.33.8 <small><small>*2025-04-02*</small></small>
- 💪 [OPT] WebSocket and SSE JSON payload will prettified automatically.
- 🐞 [FIX] The bug that the `Content-Type` header is not automatically deleted when creating form-data API from traffic list.
- 🐞 [FIX] The bug that generated MITM certificates are not cleared after importing CA certificate.
- 🐞 [FIX] The bug that some requests have been completed but the status is displayed as processing or abort.
- 🐞 [FIX] The bug that cURL export does not correctly handle JSON comments.

## v2.33.7 <small><small>*2025-03-27*</small></small>
- 🐞 [FIX] The bug that the boundary in `Content-Type` was missing in form-data requests.

## v2.33.6 <small><small>*2025-03-27*</small></small>
- 💪 [OPT] Set the built-in headers `Content-Type` and `Content-Length` of API to be unchecked.
- 💪 [OPT] Some icons of the API text input box are no longer displayed as available when there is no content.
- 💪 [OPT] When cURL imports urlencode, it will automatically decode the key-value.
- 💪 [OPT] When cURL exports urlencode, if the value is empty, the equal sign will be omitted.
- 🐞 [FIX] The bug that the built-in header `Content-Length` of API may lost.

## v2.33.5 <small><small>*2025-03-20*</small></small>
- 💪 [OPT] JSON syntax highlighting uses loop mode.
- 💪 [OPT] JSON Streaming data is automatically combined into an array when displayed.
- 💪 [OPT] Set-Cookie parsing no longer verifies data.
- 🐞 [FIX] The bug that `+` in URL parameters is automatically encoded as `%2B`.
- 🐞 [FIX] The bug that the new location URL has an encoding error in redirection.

## v2.33.4 <small><small>*2025-03-17*</small></small>
- 🐞 [FIX] A bug that API converts `%20` to `+`.
- 🐞 [FIX] A bug that duplicate `Transfer-Encoding` and `Content-Encoding` will cause repeated decoding.

## v2.33.3 <small><small>*2025-03-12*</small></small>
- 💪 [OPT] Greatly improve the performance of JSON syntax highlighting.
- 💪 [OPT] Improve the implementation of HTTP2 protocol.
- 🐞 [FIX] The bug of abnormal syntax highlighting when the HTTP header contains a name starting with a number.
- 🐞 [FIX] The bug of abnormal syntax highlighting when the HTTP header contains a dot symbol.

## v2.33.2 <small><small>*2025-03-07*</small></small>
- 💪 [OPT] Support disabling URL input autocomplate in API request settings.
- 🐞 [FIX] SSE cannot be displayed when response header Content-Type contains charset.

## v2.33.0 <small><small>*2025-03-04*</small></small>
- 💪 [OPT] Automatically restore the response data of API testing after the application is restarted.
- 💪 [OPT] Turn off automatic query parameter decoding when inputting URL in API testing.
- 💪 [OPT] API testing provides query parameter decoding option.
- 💪 [OPT] The default setting of REST proxy option is changed to `No Proxy`.
- 💪 [OPT] API collection will check and fix duplicate IDs.
- 💪 [OPT] Unify the size and color value of borders and dividers.
- 💪 [OPT] Automatically refresh cookies when redirecting.
- 🐞 [FIX] The bug that redirect data is displayed in disorder.
- 🐞 [FIX] The bug that the prompt in traffic details is incorrect when the root certificate is not installed.

## v2.32.5 <small><small>*2025-02-26*</small></small>
- 💪 [OPT] Disable charset detection for JSON data, and use utf-8 by default.

## v2.32.4 <small><small>*2025-02-26*</small></small>
- 💪 [OPT] Improve charset detection mechanism.
- 🐞 [FIX] A bug in which garbled characters may be displayed after modifying data using rewrite, breakpoints, and scripts.

## v2.32.3 <small><small>*2025-02-25*</small></small>
- 💪 [OPT] Automatic inference will be attempted when charset is not specified in the `Content-Type` header.
- 💪 [OPT] The export curl window will no longer be automatically closed after copying.
- 💪 [OPT] The limit of database capacity is increased from 10G to 64G.
- 💪 [OPT] The API collection setting page supports left and right sliding tabs.
- 🐞 [FIX] A bug that REST API may fail to merge cookies.
- 🐞 [FIX] A bug that may show a gray screen when opening the favorited WebSocket.
- 🐞 [FIX] A bug that causes the redirect title display to overlap.
- 🐞 [FIX] A bug that causes incorrect response body processing when the response header does not contain `Content-Length` and `Transfer-Encoding`.
- 🐞 [FIX] The bug that the API collection list is not updated after the API is updated.
- 🐞 [FIX] The bug that the environment variable displays the data import entry.

## v2.32.2 <small><small>*2025-02-21*</small></small>
- 💪 [OPT] JSON tree key-value width adjustment is more sensitive.
- 🐞 [FIX] The bug that a gray screen will shown when exporting curl of basic auth API.
- 🐞 [FIX] The bug that basic authorized curl becomes digest authorized after import.

## v2.32.1 <small><small>*2025-02-19*</small></small>
- 🐞 [FIX] The bug where the API collection subfolder name may become untitled after upgraded from an old version.

## v2.32.0 <small><small>*2025-02-17*</small></small>
- ❗ [IMP] Data structure upgrade, please do not downgrade to the old version after upgrading.
- 🚀 [NEW] API collection supports folder-level configuration like authorization and scripting.
- 💪 [OPT] Redesign the UI/UX of HTTP custom method management.
- 💪 [OPT] JSON tree view supports node single-click.
- 💪 [OPT] File naming rules for traffic list data export.
- 🐞 [FIX] A bug that the API tab fails to be automatically closed when deleting an API from the collection.
- 🐞 [FIX] A bug that the API header name uses environment variables to prompt an illegal name.
- 🐞 [FIX] A bug that the collaborative QR code displays no valid IP address.

## v2.31.3 <small><small>*2025-01-21*</small></small>
- 🐞 [FIX] The bug that the exported raw data has no separator between request and response.
- 🐞 [FIX] in API testing, the sent request body is not updated after replacing the content.

## v2.31.2 <small><small>*2025-01-15*</small></small>
- 🐞 [FIX] The bug that API testing Bearer Token authorization cannot be used.
- 🐞 [FIX] The bug that some text is overflow or clipped.

## v2.31.1 <small><small>*2025-01-14*</small></small>
- ❗ [IMP] Data structure upgrade, please do not downgrade to the old version after upgrading.
- 💪 [OPT] API testing supports JSON single-line comments.
- 💪 [OPT] User-Agent is no longer filled in by default, but the request sent will still use the Reqable flag.
- 💪 [OPT] After disabling Reqable Id in the API settings, this item will no longer be displayed in the header list.
- 💪 [OPT] Form-data body supports entering JSON key-value pairs in text mode.
- 💪 [OPT] In API testing, comments in text editing mode will be highlighted.
- 🐞 [FIX] The bug that the data of unchecked parameters in API testing is wrong after reloading.
- 🐞 [FIX] The bug that digest authorization may fail.
- 🐞 [FIX] The bug that the cURL imported with cmd format did not correctly handle some `^` escape characters.
- 🐞 [FIX] The bug that some JSONP could not be automatically parsed into JSON.
- 🐞 [FIX] The bug that the environment variables were not displayed properly in ellipsis mode in the table view.
- 🐞 [FIX] The bug that may report an error when starting after upgrading the version.
- 🐞 [FIX] The bug that the pop-up window cannot be opened correctly when exporting cURL for illegal URLs.
- 🐞 [FIX] The bug that the rewrite, breakpoint and scripting may cause some HTTP2 requests to fail.

## v2.30.4 <small><small>*2025-01-10*</small></small>
- ❗ [BETA] v2.31.0 beta testing.

## v2.30.3 <small><small>*2024-12-05*</small></small>
- 🐞 [FIX] The bug that failed to import cURL in cmd format.
- 🐞 [FIX] The bug that text search has results but cannot be automatically located.
- 🐞 [FIX] The bug that text rendering issue in search mode.

## v2.30.2 <small><small>*2024-11-29*</small></small>
- 💪 [OPT] Some large texts cause the application to freeze.
- 💪 [OPT] SSE supports displaying non-standard formatted messages.
- 💪 [OPT] SSE search is not case-sensitive now.
- 💪 [OPT] SSE message list supports the shortcut key `Control + F` to open the search input.
- 💪 [OPT] SSE message list displays raw data instead of prettified data.
- 💪 [OPT] WebSocket frame list supports the shortcut key `Control + F` to open the search input.
- 💪 [OPT] WebSocket frame list displays raw data instead of prettified data.
- 💪 [OPT] JSON Tree supports copying the path of a node.
- 💪 [OPT] JSON Tree supports expanding and collapsing all child nodes.
- 💪 [OPT] JSON type detection is more accurate.
- 💪 [OPT] JSONP is automatically parsed as JSON format.
- 💪 [OPT] SSE message list supports long-press context menu.
- 💪 [OPT] WebSocket frame list supports long-press context menu.
- 🐞 [FIX] A bug that caused the application to crash when inputting an non-ascii domain name.
- 🐞 [FIX] A bug that failed to import the API through cURL in some cases.

## v2.30.1 <small><small>*2024-11-26*</small></small>
- 🚀 [NEW] Fully support SSE real-time streaming.
- 🚀 [NEW] API testing supports digest-auth authorization.
- 🚀 [NEW] Add JSON tree viewer.
- 💪 [OPT] Minor adjustments to the background colors of light and dark themes.
- 💪 [OPT] MITM proxy server requests will display in the traffic list.
- 💪 [OPT] The request body and response body will automatically save the state when switching between different views.
- 💪 [OPT] The URL generated by the basic authorization request uses the `--basic` parameter instead of the `Authorization` request header.
- 💪 [OPT] Payload with encoding errors will display the original data instead of the FormatException error.
- 🐞 [FIX] The bug of infinite loop when sending requests to MITM server with LAN IP.

## v2.29.2 <small><small>*2024-11-14*</small></small>
- 🐞 [FIX] The bug that name of attachment file is incorrect.
- 🐞 [FIX] The bug that some HTTP traffic may not be displayed correctly.

## v2.29.1 <small><small>*2024-11-14*</small></small>
- 🐞 [FIX] The bug that the `-u` authorization is lost after importing cUrl.
- 🐞 [FIX] The bug that some HTTP traffic may not be displayed.

## v2.29.0 <small><small>*2024-11-10*</small></small>
- 🚀 [NEW] Some lists provide sorting options.
- 💪 [OPT] The API `Omit Equal Sign` option is moved to the request settings.
- 💪 [OPT] Python-Requests code generation template.
- 🐞 [FIX] The file name for uploading is no longer URL-encoded.
- 🐞 [FIX] The bug that multipart header names are converted to lowercase when parsing.

## v2.28.0 <small><small>*2024-11-04*</small></small>
- 🚀 [NEW] The `Raw` tab will display the decoded body by default.

## v2.27.2 <small><small>*2024-10-29*</small></small>
- 💪 [OPT] Adjust UI of some dialogs.
- 💪 [OPT] Keep the selected display type of body when switching.
- 💪 [OPT] Remember the `Group by Host` option.
- 🐞 [FIX] The bug that adding or modifying the comment of favorites will not be saved.
- 🐞 [FIX] The bug that non-ASCII file names cause multipart data to not display properly.
- 🐞 [FIX] The bug that some settings do not take effect when importing cURL or HTTP raw for API.

## v2.27.1 <small><small>*2024-10-22*</small></small>
- 🚀 [NEW] Support more accent colors and user-defined accent colors.
- 🚀 [NEW] Show application information in request overview.
- 🚀 [NEW] Support creating API from HTTP raw request message.
- 💪 [OPT] Request overview will remember the expanded and closed states of each group.
- 💪 [OPT] History will remember the last selected type.
- 💪 [OPT] Generated cURL command will include protocol version.
- 💪 [OPT] Enhance cURL command import.
- 🐞 [FIX] The bug that no traffic will be captured in enhanced mode.

## v2.26.1 <small><small>*2024-10-14*</small></small>
- 🐞 [FIX] A bug that WebSocket will broken due to incorrect frame codec.

## v2.25.1 <small><small>*2024-10-07*</small></small>
- 💪 [OPT] WebSocket message timestamp is accurate to milliseconds.
- 🐞 [FIX] A bug that data will be lost after canceling a favorite and then adding it again.
- 🐞 [FIX] A bug that may cause network error in enhanced mode.

## v2.25.0 <small><small>*2024-09-30*</small></small>
- 🚀 [NEW] Introduce favorite request list.
- 🚀 [NEW] Support deleting items in traffic history list.
- 🚀 [NEW] Add `Social and Community` to the sidebar.
- 💪 [OPT] Backup the database instead of deleting it when the database is downgraded and cannot be opened.
- 💪 [OPT] Hide script tab in API testing editor.
- 🐞 [FIX] The bug that AVIF images cannot be displayed normally on some platforms.
- 🐞 [FIX] A bug where creating API request from the traffic list could not automatically back to home.

## v2.24.0 <small><small>*2024-09-23*</small></small>
- 💪 [OPT] Support previewing of image in AVI, AVIF and APNG formats.
- 💪 [OPT] Repeat provides a reuse connection option, and the connection is no longer reused by default.
- 🐞 [FIX] The bug that animated image only display the first frame.

## v2.23.1 <small><small>*2024-09-12*</small></small>
- 💪 [OPT] Deflate encoding supports decoding with and without headers.
- 💪 [OPT] Update the UI style of some multi-line input boxes.

## v2.23.0 <small><small>*2024-09-05*</small></small>
- 🚀 [NEW] Support Internationalized Domain Name (IDN) API.
- 💪 [OPT] Use the decoded file name when saving the request and response.
- 🐞 [FIX] The bug that some requests in HAR file cannot be edited and repeated.
- 🐞 [FIX] The bug that importing some cURLs will lose the body payload.

## v2.22.2 <small><small>*2024-08-28*</small></small>
- 💪 [OPT] Backup SharedPreferences and some other config files.
- 💪 [OPT] WebSocket supports clearing message list.
- 💪 [OPT] WebSocket read messages are displayed in gray.
- 💪 [OPT] WebSocket message details display frame number.
- 💪 [OPT] A new overview URL display view.

## v2.22.1 <small><small>*2024-08-27*</small></small>
- 💪 [OPT] HAR files support WebSocket message frames.
- 💪 [OPT] A new URL redirection UI and UX.
- 💪 [OPT] The title bar more menu is no longer folded twice.
- 🐞 [FIX] A bug that the API testing environment variables may cause the request to fail.
- 🐞 [FIX] A bug that the API testing history may lose the response body.

## v2.22.0 <small><small>*2024-08-19*</small></small>
- 💪 [OPT] Improve configuration file storage performance.
- 🐞 [FIX] Form form multiple decoding causes `+` to become a space bug.
- 🐞 [FIX] The bug that HexViewer selection may be lost in WebSocket viewing.
- 🐞 [FIX] The bug that deflate is not correctly encoded and decoded.
- 🐞 [FIX] The bug that environment variable in `Basic Auth` is not working.

## v2.21.4 <small><small>*2024-08-08*</small></small>
- 💪 [OPT] Duration time format of history.
- 💪 [OPT] HexViewer supports viewing the total count of bytes.
- 💪 [OPT] Improve the interactive experience of ImageViewer.
- 💪 [OPT] Improve the WebSocket UI.
- 💪 [OPT] Bearer Token input box is changed from single line to multiple lines.
- 💪 [OPT] HTTP request method and response status code can go to MDN documentation.
- 💪 [OPT] Editor search no longer displays the result count.
- 🐞 [FIX] A bug that HTTP raw message syntax may not be highlighted.

## v2.21.2 <small><small>*2024-08-02*</small></small>
- 💪 [OPT] Supports HTTP `103 Early Hints`.
- 💪 [OPT] Supports HTTP2 `Trailers`.
- 💪 [OPT] Supports `Windows-31J`, `Shift-31J` and `EUC-JP` character encodings.
- 💪 [OPT] Adjust the HexViewer space to better adapt to mobile devices.
- 🐞 [FIX] The bug where `Early Hints` causes the response header and body to not display correctly.
- 🐞 [FIX] MITM does not handle `100 Continue` requests correctly.

## v2.21.1 <small><small>*2024-07-29*</small></small>
- 💪 [OPT] Automatically decode URL parameters when importing cURL.
- 🐞 [FIX] A bug that may lose the request body when importing form-data cRUL requests.
- 🐞 [FIX] A bug that the generated code Python-requests may lose the form-data request body.

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
- 🚀 [NEW] Introduce a new secondary proxy feature.
- 🚀 [NEW] Supports double-clicking the title to open the search bar.
- 🚀 [NEW] Supports opening the browser to download the CA certificate description file.
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
