---
sidebar_position: 3
---

# Linux

## v2.9.0 <small><small>*2024-03-22*</small></small>
- 🚀 [NEW] Introduce environment variables.
- 💪 [OPT] Generate Python-Requests code using query parameters instead of long url.
- 🐞 [FIX] The bug that API can not use Python script to process form data.
- 🐞 [FIX] The bug that API space will encodes to `%20` rather than `+`.
- 🐞 [FIX] The bug that it will prompt to save when closing the API test tab.
- 🐞 [FIX] The bug that correctly to handle `--data-raw` when importing a cURL.
- 🐞 [FIX] The bug that the python environment cannot take effect.
- 💪 [OPT] API testing supports pressing the Enter key to send directly.
- 💪 [OPT] The QR code of the certificate link is changed from click display to mouse pointer hover display.
- 🐞 [FIX] The bug that app menu group position is incorrect after the window is zoomed.

## v2.8.2 <small><small>*2024-03-06*</small></small>
- 🐞 [FIX] The bug of importing ApiFox collection failed in some cases.
- 🐞 [FIX] The bug where the response raw message is incorrect.
- 🐞 [FIX] Incorrect highlighting of query parameters and cookies.
- 🐞 [FIX] The bug where `startedDateTime` of the exported HAR format is incorrect.
- 💪 [OPT] Coloring request methods.
- 💪 [OPT] File drag and drop will be disabled when a dialog is showing.
- 🐞 [FIX] The bug that the request path is incorrect in python scripts.
- 🐞 [FIX] XDE desktop cannot automatically configure the proxy.

## v2.8.1 <small><small>*2024-03-04*</small></small>
- 🐞 [FIX] App will crash with glibc 2.39.

## v2.8.0 <small><small>*2024-02-29*</small></small>
- 🚀 [NEW] Available API tabs of community version are increased from 2 to 4.
- 🚀 [NEW] Adds three new tabs, Cookies, Set-Cookies and Comment.
- 🚀 [NEW] Now you can comment a traffic record.
- 🚀 [NEW] Custom request and response tabs.
- 🐞 [FIX] The cookie automatic update mechanism causes a bug that requires saving when closing a API Tab.
- 🐞 [FIX] The bug of incorrect parsing of the '--data-urlencode' parameter when importing a cURL.
- 🐞 [FIX] The bug in which the content displayed in the Tab title is truncated.
- 🐞 [FIX] The bug where `wss` in HAR file is recognized as `ws`.
- 💪 [OPT] Supports recovery of the damaged `SharedPreferences` file.

## v2.7.1 <small><small>*2024-02-22*</small></small>
- 🐞 [FIX] The bug of incorrect encoding and decoding of URL query parameters.
- 🐞 [FIX] The bug in parsing HAR files does not correctly handle the MIME type.
- 🐞 [FIX] The bug of secondary proxy account authentication not works.
- 💪 [OPT] HEX will be displayed first when the image data decoding fails.
- 🐞 [FIX] The bug that data displayed after modifying `Content-Type` through script does not take effect.

## v2.7.0 <small><small>*2024-02-20*</small></small>
- 🐞 [FIX] The bug that the unmodified API will prompt to save when closing.
- 🐞 [FIX] The bug that closing other tabs will close all tabs.
- 🐞 [FIX] The bug of incorrect encoding of `space` and `=` in request query parameters.
- 🚀 [NEW] Supports to adjust app display scaling.
- 🚀 [NEW] Will restore the previous window position and size when restarting.
- 🚀 [NEW] Supports deleting API request history URLs.
- 💪 [OPT] No longer automatically checked the rewrite-replace checkbox.
- 🐞 [FIX] The bug that the original response data may not be brought in when creating a rewrite-replacement response rule.
- 🐞 [FIX] The bug that URL rules may not match in rewrite, breakpoint and scripting rules.

## v2.6.3 <small><small>*2024-02-07*</small></small>
- 💪 [OPT] Runtime error of API testing scripts will output to the console.
- 💪 [OPT] The auto-complete list of text input field supports up and down key selection.
- 🐞 [FIX] Some prompts of Python scripting api are incorrect.
- 🐞 [FIX] The bug that response body is not automatically decoded when scripting is enabled.
- 💪 [OPT] The application ID is changed from `reqable` to `com.reqable.linux`.

## v2.6.2 <small><small>*2024-02-04*</small></small>
- 🐞 [FIX] A bug where some webSocket requests are not recognized.
- 🐞 [FIX] A bug in the API request script caused the request path to be incorrectly encoded.

## v2.6.1 <small><small>*2024-01-31*</small></small>
- 🚀 [NEW] Code editor supports code auto-completion.
- 🐞 [FIX] The bug that text syntax highlighting may be incorrect.
- 🐞 [FIX] The bug that missing `\` at the end of URL.
- 🐞 [FIX] The bug that `HexViewer` will get focus by default.
- 🐞 [FIX] The bug that IP was displayed rather than host.
- 🚀 [NEW] Console tab for traffic details.
- 🚀 [NEW] Console tab for API testing response.

## v2.5.0 <small><small>*2024-01-25*</small></small>
- 🚀 [NEW] Introduce scripting for API testing.
- 🚀 [NEW] Introduce script templates.
- 🚀 [NEW] Fork templates from public script repositories.
- 🚀 [NEW] Introduce zen mode.
- 💪 [OPT] New console for script editor.
- 💪 [OPT] Remember highlight and application informations when saving HAR files.
- 🐞 [FIX] The secondary proxy may cause an infinite loop of requests.
- 🐞 [FIX] The bug that unable to capture HTTP2 plaintext traffic.
- 🐞 [FIX] The bug that handling HTTP trailer incorrectly.
- 🐞 [FIX] The bug of failing to handle WebSocket compression extension correctly.
- 🐞 [FIX] The bug that text selection is incorrect after double-clicking a word.
- 🐞 [FIX] The bug that the editor composing menu does not follow the input position.

## v2.4.1 <small><small>*2024-01-16*</small></small>
- 💪 [OPT] Use form body when creating API requests from the form request cURL.
- 🐞 [FIX] The bug of duplicate cookie values in the code snippet.
- 🐞 [FIX] The bug that unable to decode deflate data.
- 🐞 [FIX] A bug that may trigger content selection when scrolling the editor.
- 🐞 [FIX] The bug that unable to copy cURL of the WebSocket request.
- 🐞 [FIX] The bug of failing to handle WebSocket compression extension correctly.
- 🐞 [FIX] The bug that cannot create form request or copy cURL from traffic list.
- 💪 [OPT] Remove the application ID option from the default column of the traffic list.
- 💪 [OPT] Tabs on the home page can be directly dragged and sorted without long pressing.
- 🐞 [FIX] A bug where the tab title on the home page may be displayed incompletely.
- 🐞 [FIX] The bug that cannot resize traffic list column width.
- 🐞 [FIX] The bug that `VS Code` cannot be launched in the script editor.

## v2.4.0 <small><small>*2024-01-12*</small></small>
- 🚀 [New] Introduce a new secondary proxy feature.
- 🐞 [FIX] The bug that the generated cURL does not merge cookies.
- 🐞 [FIX] The bug that the `Referer` header cannot be sent in API requests.
- 🐞 [FIX] The bug of missing `application/x-www-form-urlencoded` header in code snippet.
- 🐞 [FIX] A bug that may crash when exporting P12 format certificate.
- 🚀 [New] Supports drag sorting of working tabs.
- 🚀 [New] You can select or unselect a search condition for traffic list.
- 💪 [OPT] The time threshold for triggering drag is reduced from 500ms to 150ms.
- 🐞 [FIX] A bug that may jump abnormally when selecting a debug list.
- 💪 [OPT] Supports mouse wheel to control horizontal layout scrolling.
- 🐞 [FIX] A bug that may have some exceptions when the certificate is not installed.

## v2.3.2 <small><small>*2024-01-08*</small></small>
- 💪 [OPT] Adjustment of some UI details.
- 🐞 [FIX] The bug that the raw message in the traffic details cannot be code highlighted.
- 🐞 [FIX] The bug that JSON array type throws an error int code snippet.

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
- 🐞 [FIX] The bug that the urlencode request body may be lost when parsing HAR files.
- 🐞 [FIX] A failure with non-standard HAR connection fields.
- 🐞 [FIX] The bug that the uppercase encoding value such as GZIP cannot be recognized.
- 🚀 [NEW] Allow auto-dismiss the QR code pop-up dialog when the remote device connected.

## v2.2.0 <small><small>*2023-12-28*</small></small>
- 🚀 [NEW] API testing supports splitting merged cookies into multiple ones.
- 🚀 [NEW] API testing supports opening additional editors to edit cookies.
- 🐞 [FIX] The bug where some items in the traffic list were sorted incorrectly.
- 🐞 [FIX] The bug that the application cannot start in some cases.

## v2.1.1 <small><small>*2023-12-25*</small></small>
- 🚀 [NEW] Allow root certificate regeneration.
- 💪 [OPT] API testing `reqableId` supports displaying in two lines.
- 💪 [OPT] API testing will automatically fill key-value entries when switching from text.
- 🐞 [FIX] The bug that it is unable to install root certificate.
- 🐞 [FIX] The bug of abnormal display of collaborative QR code when there is no local IP.
- 🐞 [FIX] A bug that the mirror icon will display incorrectly in some cases.
- 🚀 [NEW] You can pin application filter and domain filter now.
- 🚀 [NEW] You can configure interceptors such as rewriting in auto-highlighting.
- 🚀 [NEW] A shortcut key `Alt + Ctrl + ↑/↓` for traffic list, switch browsing history before and after.
- 🚀 [NEW] A shortcut key `Shift + Contrl + I` for all list, invert the current selection.
- 💪 [OPT] The domain filter list is expanded by default.
- 💪 [OPT] Slightly increase the size of the diff tool window.
- 🐞 [FIX] A debug that interceptor icon color is not highlighted.

## v2.0.0 <small><small>*2023-12-15*</small></small>
- 🚀 [New] Supports collaboration with Reqable mobile apps.
- 🚀 [New] Supports importing and exporting pkcs12 root certificate file.
- 🚀 [New] Supports viewing the currently used root certificate file.
- 🚀 [New] Diff tool supports header name lowercase comparation.
- 🚀 [New] Adds a search icon for Code Editor and Hex Viewer.
- 💪 [Opt] Supports some non-standard proxy protocol messages.
- 💪 [Opt] Redo traffic overview UI/UX.
- 💪 [Opt] Redo Websocket UI/UX.
- 💪 [Opt] Redo styling of settings window option switches.
- 💪 [Opt] More `Certificate` menu bar options.
- 💪 [Opt] Code Editor removes unnecessary padding areas.
- 💪 [Opt] Reduces drag and scroll speed of Code Editor and HexViewer.
- 💪 [Opt] Code editor will not lose the currently selection when dragging to expand the selection area.
- 💪 [Opt] Android certificate setup adds network security configuration guides.
- 💪 [Opt] Android certificate setup adds certificate file permission tips.
- 💪 [Opt] Diff tool enables sorting headers by default.
- 💪 [Opt] New sub windows no longer flicker on startup.
- 💪 [Opt] Copying API cURL will close the pop-up window automatically.
- 💪 [Opt] Tips will be displayed in the bottom bar if the current API testing has a proxy setting.
- 💪 [Opt] Max redirection button will automatically wrap when there is insufficient display space.
- 💪 [Opt] You can click the cookie list item to edit it.
- 💪 [Opt] In table mode, long press the cell will copy the key or value.
- 💪 [Opt] License registration automatically fills in the last email address and license code.
- 💪 [Opt] Try using SSL SNI as the host of the URL instead of the IP.
- 💪 [Opt] Adds some prompts in SSL bypass editor.
- 💪 [Opt] Double-clicking outside the traffic list will automatically close the details panel.
- 💪 [Opt] Supports `Control + L` shortcut key to quickly locate the currently selected traffic item.
- 🐞 [Fix] A bug that unverified license will cause the page to remain in the loading state forever.
- 🐞 [Fix] A bug that code syntax highlighting may cause content display to be lost.
- 🐞 [Fix] A bug where URL port number displayed in the traffic list was incorrectly in some cases.
- 🐞 [Fix] A bug where clicking outside the traffic list may cancel the selected item.
- 🐞 [Fix] A bug where response body replacement cannot automatically fill the original payload.
- 🐞 [Fix] A bug that failed to import Postman collection if containing multi-file values.
- 🐞 [Fix] A bug that failed to open some HAR files.
- 🐞 [Fix] An infinite loop bug occurs when directly requesting the proxy port.
- 🐞 [Fix] A bug where the close frame of Websocket was displayed incorrectly.
- 🐞 [Fix] App may crash when failed to send a POST request.
- 🐞 [Fix] A bug where the response content may not be updated after sending a request.
- 🐞 [Fix] The bug of URL display overflow in API testing explorer.
- 🐞 [Fix] A bug that the file content is empty when VS Code opens a new script.
- 🐞 [Fix] A bug that the reset application in settings does not take effect.

## v1.6.2 <small><small>*2023-10-12*</small></small>
- 💪 [Opt] Reduce the number of traffic capture cache files.
- 🐞 [Fix] The issue of flashing when opening a new window.
- 🐞 [Fix] The bug of missing query parameters in rewrite redirection.

## v1.6.1 <small><small>*2023-10-09*</small></small>
- 💪 [Opt] Traffic list application filtering option displays remote device IP.
- 💪 [Opt] The API editor URL input box will display the historical URL and you can choose to enter it.
- 💪 [Opt] URL rule wildcard matching.
- 💪 [Opt] When a lower version application opens a higher version database, it will reset the database instead of reporting an error.
- 💪 [Opt] The raw message displays the body encoding type.
- 🐞 [Fix] The API testing tab that is no save prompt after the application is restarted.
- 🐞 [Fix] The bug that API testing may prompt saving again when a saved API is closed.
- 🐞 [Fix] The bug that requests in socks proxy mode cannot trigger interceptors such as rewriting, breakpoints, and scripts.
- 🐞 [Fix] A bug where quotes were not escaped during code generation..
- 🐞 [Fix] A bug where some cache files failed to be automatically cleared in incognito mode.
- 🐞 [Fix] The bug that the app will get stuck when exiting from the menu or tray.

## v1.6.0 <small><small>*2023-09-27*</small></small>
- 🚀 [New] Supports detaching a new window to view traffic data details.
- 🚀 [New] The middle mouse button can close the Tab.
- 🚀 [New] The middle mouse button can close the sub-window.
- 💪 [Opt] Better performance and memory usage.

## v1.5.1 <small><small>*2023-09-25*</small></small>
- 💪 [Opt] The count of free tabs for history and file viewing has been increased from 1 to 2.
- 💪 [Opt] The pop-up dialog supports the `Enter` shortcut key to trigger positive button.
- 💪 [Opt] When saving API collection, the last save path will be used by default.
- 💪 [Opt] When saving API collection, the host will be used as the name by default.
- 💪 [Opt] Automatically change the port when MITM proxy port conflict is detected.
- 💪 [Opt] Python scripts can be directly opened with `Visual Studio Code` for editing.
- 💪 [Opt] Automatically merge the Cookie value of the request header when generating code snippet.
- 🐞 [Fix] The bug that API testing request body `compress` and `prettify` did not take effect when actually sent.
- 🐞 [Fix] The bug that API testing traffic will not appear in the traffic list when following the redirection in debug mode.
- 🐞 [Fix] The bug that API testing traffic with mirroring is not displayed in the traffic list in debug mode.
- 🐞 [Fix] The bug that rewriting redirected requests will automatically perform redirection based on the response.
- 🐞 [Fix] The bug that `Reset App` in settings is not working.
- 🐞 [Fix] A bug that caused abnormal composing input in some text fields.
- 🐞 [Fix] The bug that the application info cannot be displayed for requests that have established a TCP connection before capture is enabled.
- 🐞 [Fix] A Bug where `Host` header is missing in the raw message.
- 🐞 [Fix] A bug that causes crash when exiting the app under certain circumstances.
- 🐞 [Fix] A Bug where proxy protocol cannot be correctly identified in some cases.

## v1.5.0 <small><small>*2023-09-21*</small></small>
- 🚀 [New] Add HTTP request and response diff tool.
- 🚀 [New] Add `JWT` decoder in the toolbox.
- 🚀 [New] API JSON data editing supports one-click compression.
- 💪 [Opt] Supports `Control + W` shortcut key to close sub windows.
- 💪 [Opt] Use name instead of timestamp when exporting traffic history.
- 💪 [Opt] Raw packet syntax supports JSON and XML highlighting.
- 🐞 [Fix] In the API testing, the cURL import dialog will not automatically pop up if the command containing `WIDTH NO-BREAK SPACE`.
- 🐞 [Fix] The bug of uploading crash and statistic configuration not taking effect.
- 🐞 [Fix] `Space` and `*` in the `urlencode` of the Python script may cause some servers to fail to correctly obtain the request path.

## v1.4.1 <small><small>*2023-09-18*</small></small>
- 💪 [Opt] Traffic list supports drag selection.
- 💪 [Opt] Traffic list requests and responses are saved with default file names.
- 🐞 [Fix] The bug that some JavaScript content searches have no results.
- 🐞 [Fix] The bug that sending a request when the URL contains `WIDTH NO-BREAK SPACE` characters will cause the application to crash.
- 🐞 [Fix] The bug that cURL export cannot parse commands containing `WIDTH NO-BREAK SPACE` characters.
- 🐞 [Fix] The bug that the HTTP raw data copy content does not correctly handle the CRLF.
- 🐞 [Fix] The bug of copying from a rewrite modification rule.

## v1.4.0 <small><small>*2023-09-14*</small></small>
- 🚀 [New] `Code Snippet` supports cURL and Guzzle for PHP language.
- 🚀 [New] Add `Certificate` application menu bar.
- 🚀 [New] Add `Raw` display for request details.
- 🚀 [New] Add `Automatic Debugging` switch in app settings.
- 🚀 [New] Support reviewing Charles Session files.
- 💪 [Opt] A prompt pop-up dialog will be displayed when Reqable exits.
- 💪 [Opt] A prompt will be displayed after dragging unsupported files to the Reqable main window and releasing them.
- 💪 [Opt] The session content area displays information about file or history opening failure.
- 💪 [Opt] Opening HAR files no longer filters out `CONNECT` requests.
- 🐞 [Fix] Reverse proxy certificate trust issue.
- 🐞 [Fix] A bug where SSL handshake failure are not displayed.
- 🐞 [Fix] A bug in which operations such as deleting, clearing, and editing bookmarks lead to incorrect bookmark selection status.
- 🐞 [Fix] A bug in importing cURL that causes the URL parsing to fail due to the `--location` parameter.
- 🐞 [Fix] The bug that the request cannot be sent due to malformed `Content-Type`.
- 🐞 [Fix] The bug of incorrect application window position and size on certain resolution devices.
- 🐞 [Fix] SOCKS proxy causing MySql database to be unable to connect.

## v1.3.1 <small><small>*2023-09-11*</small></small>
- 🚀 [New] Support `Reverse Proxy` now.
- 🚀 [New] Add `Proxy` application menu group bar.
- 🚀 [New] When you paste the cURL into the API testing URL input field, the import cURL dialog will automatically pop up.
- 💪 [Opt] Cancel the certificate status detection polling mechanism.
- 💪 [Opt] API query parameters created from the traffic list are automatically URL decoded.
- 💪 [Opt] The URL displayed in the traffic list removes the display of the default root path `/`.
- 💪 [Opt] A new `Help` button is added to the secondary proxy configuration page.
- 🐞 [Fix] A bug where expanding the sidebar may cause the gateway, mirror, script, rewrite, and breakpoint to not work.
- 🐞 [Fix] A bug where clicking the start button might cause the content layout size to jump back to its previous size.
- 🐞 [Fix] The bug that may cause the CONNECT proxy request status to be displayed as interrupted after the gateway successfully silences the request.
- 🐞 [Fix] The bug of incorrect Toast style used in some error prompts.
- 🐞 [Fix] The bug of incomplete display of changelogs in the version update window.

## v1.3.0 <small><small>*2023-09-05*</small></small>
- 🚀 [New] Display the application where the traffic from.
- 🚀 [New] Support filtering traffic according to application in the explorer.
- 💪 [Opt] When the traffic list is at the bottom, it will automatically scroll if new data appears.
- 💪 [Opt] The read items in the structure tree are grayed out.
- 💪 [Opt] Added type icon display in the structure tree.
- 💪 [Opt] Importing cURL will automatically recognize the JSON/XML type.
- 💪 [Opt] Explorer UI details adjustment.

## v1.2.5 <small><small>*2023-09-01*</small></small>
- 🐞 [Fix] Fixed the bug that scripting broken the connection.

## v1.2.4 <small><small>*2023-09-01*</small></small>
- 🐞 [Fix] Fixed the bug that an error was reported when opening the app after updating to version 1.2.3.
- 🐞 [Fix] Fixed the bug that the name of the opened tab could not be updated synchronously after modifying the name of the capture history.

## v1.2.3 <small><small>*2023-08-31*</small></small>
- 🚀 [New] The traffic list read items are grayed out.
- 🚀 [New] The traffic history supports configuring the cache duration, which is 7 days by default.
- 🚀 [New] Traffic history supports renaming.
- 🚀 [New] Traffic history supports adding/removing stars.
- 🚀 [New] Query parameter list viewing supports text mode.
- 💪 [Opt] The traffic list removes gray highlighting and adds teal highlighting.
- 💪 [Opt] Use the resident daemon process to get the CA root certificate installation status.

## v1.2.1 <small><small>*2023-08-28*</small></small>
- 🚀 [New] SSL bypass supports switch and silent mode.
- 🚀 [New] Supports adding SSL bypass from traffic list.
- 💪 [Opt] Automatically changing context menu text color when hovering.
- 💪 [Opt] The right click of the traffic list supports batch copying of URLs.
- 🐞 [Fix] An exception occurs when generating python code when the root node of JSON is a list.
- 🐞 [Fix] The bug that localhost requests will not be displayed when the API test is followed by debugging.
- 🐞 [Fix] The bug that the SSL Bypass requests will not be displayed when the API test is followed by debugging.
- 🐞 [Fix] The bug that the `Proxy-Connection` header was not removed when sending to remote server.
- 🐞 [Fix] The bug that some Linux systems cannot open the application and prompt `GLIBCXX_3.4.26 not found`.
- 🐞 [Fix] Fix the bug that the title bar height of some Linux systems is abnormal.

## v1.2.0 <small><small>*2023-08-24*</small></small>
- 💪 [Opt] The UX of expanding the app menu bar.
- 🚀 [New] Added code snippet for API and traffic.
- 🚀 [New] Added `Clear Cache` and `Reset App` in settings.
- 🚀 [New] Urlencode supports text editing mode.
- 🚀 [New] Urlencode supports importing and copying concatenated strings.
- 💪 [Opt] Adding quotes to URL values in generated cURL commands.
- 🐞 [Fix] The bug that the number of checks displayed in the domain filter of the traffic list is wrong.
- 🐞 [Fix] The bug that the request or response cannot continue to execute after the breakpoint window is closed.
- 🐞 [Fix] Possible duplicate `Content-Type` header bug in API created from traffic list.
- 🐞 [Fix] The bug that the text display error in the API query parameter text editing mode.

## v1.1.8 <small><small>*2023-08-10*</small></small>
- 🚀 [New] Support API session global settings.
- 💪 [Opt] Important performance optimization.
- 💪 [Opt] The storage limit of the database has been increased from 1G to 10G.
- 💪 [Opt] The traffic history data is stored in compression.
- 💪 [Opt] Raw body data is automatically prettified.
- 💪 [Opt] Exiting the program no longer automatically closes the system proxy if Reqable proxy is unset.
- 🐞 [Fix] The bug that the request header in the imported API collection is incomplete.
- 🐞 [Fix] The bug that the API repeatedly adds the Cookie header.
- 🐞 [Fix] The bug that auto-cookie settings is not working.
- 🐞 [Fix] The bug that API session shortcut keys are not working.

## v1.1.7 <small><small>*2023-08-07*</small></small>
- 🚀 [New] Support export and import Reqable api collections.
- 🚀 [New] API editor added `Follow Debug` shortcut icon.
- 🚀 [New] The traffic list supports `client address` search terms.
- 🚀 [New] Added a button to clear the results in the URL codec tool.
- 💪 [Opt] Added error message display in the URL codec tool.
- 💪 [Opt] Cleaning strategy of history cache files.
- 💪 [Opt] API collection naming and renaming verification.
- 💪 [Opt] Some input boxes will change the border color after getting the focus.
- 🐞 [Fix] The bug that the remote device sll bypass does not take effect.
- 🐞 [Fix] A bug that failed to read some traffic history.
- 🐞 [Fix] Failed to clean up the websocket cache file after deleting traffic history.
- 🐞 [Fix] A bug where input auto-completes were lost in traffic search items.

## v1.1.6 <small><small>*2023-08-03*</small></small>
- 🚀 [New] Refactor capture multi-session UX.
- 🚀 [New] Supports importing API collections of Postman, Hoppscotch, ApiPost and Apifox.
- 🚀 [New] Support for merging capture records into other session tabs.
- 💪 [Opt] Improve application startup speed.
- 💪 [Opt] Automatically clean up expired capture cache files.
- 💪 [Opt] Bookmark filtering and domain name filtering conditions are changed from `and` to `or`.
- 🐞 [Fix] The bug that the SSL traffic of the remote device is not decrypted when the computer does not have a certificate installed.

## v1.1.5 <small><small>*2023-07-31*</small></small>
- 🚀 [New] Support SSL bypass configuration (right-click the shield icon).
- 💪 [Opt] MITM proxy is skipped if the certificate is not installed successfully.
- 💪 [Opt] Remove the limit of 9999 repeats.
- 💪 [Opt] Server address will also be displayed in the traffic list after the proxy connection fails.
- 💪 [Opt] License window adds a display of the reason for restriction.
- 💪 [Opt] Traffic list supports Home/End/PageUp/PageDown shortcut keys.
- 💪 [Opt] The editor supports Home/End shortcut keys.
- 🐞 [Fix] Wildcard matching algorithm may enter an infinite loop.
- 🐞 [Fix] cURL format for copying Multipart requests in the traffic list is incorrect.
