---
sidebar_position: 0
---

# Windows

## v3.0.38 <small><small>*2026-02-02*</small></small>
- 💪 [OPT] Add a locate icon button to the API collection title bar.
- 💪 [OPT] Optimize API collection paste functionality.
- 🐞 [FIX] The bug where SOCKS proxy URLs were not syntax highlighted.
- 🐞 [FIX] The bug where URL syntax highlighting for IPv6 addresses was abnormal.
- 🐞 [FIX] The bug where IPv6 address requests were interrupted under SOCKS proxy.
- 🐞 [FIX] The bug where URL was incorrect when creating IPv6 requests from the traffic list.
- 🐞 [FIX] The bug where enabling follow debug caused the application to crash with IPv6 requests.
- 🐞 [FIX] The bug where the new version changelog did not refresh after switching languages in app settings.
- 🐞 [FIX] The bug where API collections would not automatically locate the currently opened API in some cases.
- 🐞 [FIX] The bug where the `Delete` shortcut key for API collections did not work.
- 🐞 [FIX] The bug where right-click context menu would close when clicking on an invalid item.

## v3.0.37 <small><small>*2026-01-22*</small></small>
- 💪 [OPT] Show notification in the bottom when there are too many history records, prompting to clean up.
- 🐞 [FIX] The bug where the port number for HTTP access to the local server may be incorrect.
- 🐞 [FIX] The bug where the top of the window overflowed when maximized.

## v3.0.36 <small><small>*2026-01-20*</small></small>
- 💪 [OPT] Update CA certificate download link.
- 💪 [OPT] Support importing Insomnia Yaml collection data.
- 💪 [OPT] Automatically switch to the newly imported environment after importing collections or environments.
- 💪 [OPT] AES tool icon no longer displays the premium badge if the current account is premium.
- 🐞 [FIX] The bug where importing Reqable collections would lose WebSocket requests.
- 🐞 [FIX] The bug where fonts displayed abnormally on high-resolution monitors.

## v3.0.35 <small><small>*2026-01-19*</small></small>
- 💪 [OPT] Support input and parsing of `foo=bar&abc=123` format in urlencode request text mode.
- 💪 [OPT] Use label color for environment icon in the top right corner of the home page.
- 🐞 [FIX] The bug where script content did not load correctly when using offline data mode while logged in.

## v3.0.34 <small><small>*2026-01-16*</small></small>
- 💪 [OPT] Code snippet supports Dart-Dio.
- 💪 [OPT] JSON Tree view will remember the last search type.
- 💪 [OPT] Prefer using user-set ADB path over environment variables.
- 💪 [OPT] Compatible with ADB 36.0.0 and 36.0.1 versions where the last character of pushed files is truncated, causing Reqable one-click certificate installation to fail.
- 💪 [OPT] Display application process ID in the capture overview tab.
- 💪 [OPT] Added TCP connection information to script context.
- 💪 [OPT] JSON viewer adds open file and save as buttons.
- 🐞 [FIX] The bug where the state of the previous and next scroll buttons on the home tabs might be incorrect.
- 🐞 [FIX] The bug where the ADB path could not be unset after being set.
- 🐞 [FIX] The bug where switching environment variables during script execution caused variables to update to the wrong environment.

## v3.0.33 <small><small>*2026-01-07*</small></small>
- 💪 [OPT] Automatically format node content in JSON tree view.
- 💪 [OPT] WebSocket testing will cache the last sent message.
- 🐞 [FIX] The bug where HTTP redirects did not correctly handle current path redirects.

## v3.0.32 <small><small>*2026-01-05*</small></small>
- 💪 [OPT] In the Cookie view, copying icon now copies the concatenated cookie string instead of key-value entries.
- 💪 [OPT] JSON tree view node context menu adds copy dictionary path option.
- 💪 [OPT] Protocol version is no longer specified when copying cURL from the traffic list.
- 💪 [OPT] Code snippet for Java-HttpClient adds main method and prints body text to console.
- 💪 [OPT] Hash tool automatically loads the last configuration.
- 💪 [OPT] HMAC tool automatically loads the last configuration.
- 💪 [OPT] HMAC tool adjusts the position of the key and input payload.
- 💪 [OPT] Added HMAC tool option in the Tools menu and selection context menu.
- 💪 [OPT] Timestamp tool automatically loads the last configuration.
- 💪 [OPT] AES tool automatically removes line breaks from ciphertext during decryption.
- 💪 [OPT] AES tool automatically loads the last configuration and executes automatically.
- 💪 [OPT] Always showing ADB path setting entry.
- 🐞 [FIX] The bug where code snippet for Java-HttpClient did not correctly handle query and form encoding.
- 🐞 [FIX] The bug where code snippet for Python-http.client did not correctly handle query and form encoding.
- 🐞 [FIX] The bug where WebSocket details changed with data updates.
- 🐞 [FIX] The bug where SSE details changed with data updates.
- 🐞 [FIX] The bug where running python-requests requests in the proxy terminal caused SSL verification errors.

## v3.0.31 <small><small>*2025-12-25*</small></small>
- 🚀 [New] Code snippet supports setting indentation.
- 🚀 [New] Code snippet for Python-Requests supports whether to use dictionary parameters.
- 💪 [OPT] Added background color to third-party login icon buttons.
- 💪 [OPT] API testing can inherit common headers defined in the folder when the current is not selected.
- 💪 [OPT] API testing can inherit common parameters defined in the folder when the current is not selected.
- 💪 [OPT] Automatically fill in the `Content-Length` header when generating cURL if a request body is expected but not present.
- 🐞 [FIX] The bug where exporting cURL did not correctly handle duplicate headers.
- 🐞 [FIX] The bug where code snippet did not correctly handle duplicate headers.
- 🐞 [FIX] The bug where requests missing `Content-Length` could not execute rewrite, breakpoint, and script rules.
- 🐞 [FIX] The bug where API testing history search results were sorted incorrectly.
- 🐞 [FIX] The bug where corrupted backup files could cause the application to fail to start.

## v3.0.30 <small><small>*2025-12-08*</small></small>
- 🚀 [New] Introduce Java VM root certificate automatic installation.
- 💪 [OPT] form-data parts no longer send Content-Length headers.
- 🐞 [FIX] Fixed the bug where clicking the window close button might not enter background mode.
- 🐞 [FIX] The bug where built-in environment variables could not be used in Python scripts.
- 🐞 [FIX] The bug where APIs created by the `+` button on the home page did not apply global settings.
- 🐞 [FIX] The bug where cURL import failed due to CRLF line-break.
- 🐞 [FIX] The bug where cURL import of form-data requests lost custom part headers.
- 🐞 [FIX] The bug where the text editor did not correctly locate the next match after replacing content.

## v3.0.29 <small><small>*2025-12-04*</small></small>
- 💪 [OPT] Support batch exporting API collections.
- 💪 [OPT] Support batch exporting environment variables.
- 💪 [OPT] Support dragging files into the collection view to import data.
- 💪 [OPT] Support importing multiple collection files at once.
- 💪 [OPT] Support dragging files into the environment view to import data.
- 💪 [OPT] Support importing multiple environment variable files at once.
- 💪 [OPT] Support dragging multiple files to open on the home page.
- 💪 [OPT] Set a maximum width for home page tabs.
- 💪 [OPT] When an API script execution error occurs, the console displays output from other executed scripts.
- 💪 [OPT] Loading history may cause the application to start slowly.
- 💪 [OPT] Unified the order and wording of some popup buttons.
- 💪 [OPT] Add refresh option to HAR tab context menu.
- 🐞 [FIX] Error when using newly constructed query in Python scripts.
- 🐞 [FIX] Digest authorization did not correctly handle environment variables.

## v3.0.28 <small><small>*2025-11-18*</small></small>
- 💪 [OPT] Replace cURL command parser.
- 💪 [OPT] Importing curl no longer blocks if a file is not found.
- 💪 [OPT] form-data adds a warning for missing files.
- 💪 [OPT] Compatible with some non-standard `content-type` types.
- 💪 [OPT] Display the activated environment variable name instead of icon in the home page.
- 💪 [OPT] Right-clicking the `+` on the home tab bar can directly create an HTTP request.
- 💪 [OPT] Script support for assigning `request.contentType` and `response.contentType`.
- 💪 [OPT] Traffic list supports status code conditional search.
- 💪 [OPT] When a script interrupts a request, the console displays relevant information instead of an error.
- 🐞 [FIX] HEX view in WebSocket and SSE could not gain focus, causing shortcut keys to be not working.
- 🐞 [FIX] SSE view in traffic list did not display data due to encodings.
- 🐞 [FIX] XML prettify did not correctly handle nested `>` and `<` characters.
- 🐞 [FIX] Importing cURL did not handle single and double quotes correctly.
- 🐞 [FIX] Script editor may freeze.
- 🐞 [FIX] Script editor `Editing` and `Saved` status may display incorrectly.
- 🐞 [FIX] API script did not clean up files after execution.
- 🐞 [FIX] The dialog title of environment variable creation was incorrect.
- 🐞 [FIX] Running node or commands dependent on node in the proxy terminal caused errors.

## v3.0.27 <small><small>*2025-11-18*</small></small>
- 💪 [OPT] Display all new version logs during version updates.
- 💪 [OPT] Display VPN addresses in the IP list.
- 💪 [OPT] Automatically clean up outdated log files.
- 💪 [OPT] Support opening the new Charles .chlz format files.
- 💪 [OPT] Move the Zen mode option forward in the settings.
- 💪 [OPT] Add a quick create HTTP option in settings to control whether the `+` button on the tab bar directly creates an HTTP request.
- 🐞 [FIX] Remove trailing `;` when importing cURL headers with empty values.
- 🐞 [FIX] Application does not automatically open files when launched from file association.
- 🐞 [FIX] API request tab save prompt status not displaying correctly in some cases.
- 🐞 [FIX] Failed to correctly identify request body type when importing Postman collections.

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
- 🐞 [FIX] Importing Reqable V2 version API collections lost folder configuration bug.

## v3.0.22 <small><small>*2025-11-05*</small></small>
- 💪 [OPT] Improve login and registration process.
- 💪 [OPT] Add compatibility check for `curl_close` in generated PHP code.
- 💪 [OPT] A built-in license migration notification will now automatically pop up.
- 💪 [OPT] Use `Shift + Tab` to switch to the previous input box in table mode editing.
- 🐞 [FIX] `{{` and `}}` in JSON would be incorrectly replaced with `<<` and `>>` when importing collection data.
- 🐞 [FIX] Opening the log window after the log file is deleted would result in a gray window.

## v3.0.21 <small><small>*2025-11-05*</small></small>
- 🚀 [NEW] Changed premium authorization from license to account.
- 🚀 [NEW] Support for cloud data storage.
- 🚀 [NEW] Support for multi-device synchronization and collaboration.
- 🚀 [NEW] A new tab for environment variable editing.
- 🚀 [NEW] Now can preview SVG images.
- 💪 [OPT] Support for closing tabs to the right.
- 💪 [OPT] Rewrite redirect URLs will now omit the root path `/` when displayed.
- 💪 [OPT] Viewing request history no longer prompts you to "restore" data.
- 💪 [OPT] Support for importing OpenAPI yaml collections.
- 💪 [OPT] Request and response panels now display close and collapse icon buttons.
- 💪 [OPT] Changed the URL auto-completion scheme from https to http.
- 💪 [OPT] cURL import will automatically handle JSON escape characters.
- 💪 [OPT] Improved error message for environment variable name.
- 💪 [OPT] In code snippet, using dynamic import for Node fetch in code snippet.
- 💪 [OPT] In code snippet, axios outputs the response body instead of the entire response object.
- 🐞 [FIX] Rewriting redirects could cause other interceptors to fail.
- 🐞 [FIX] `{{` and `}}` in JSON would be incorrectly replaced with `<<` and `>>` when importing collection data.
- 🐞 [FIX] HAR format was not correctly processing HTTP2 headers when importing collection data.
- 🐞 [FIX] Components section was incorrectly imported when importing OpenAPI collections.
- 🐞 [FIX] Searching for rules might display the previous search results.
- 🐞 [FIX] Value in the environment variable hover tooltip might not be updated.
- 🐞 [FIX] Response rewrite interceptor did not show in history and sub windows.
- 🐞 [FIX] A window with disabled resizing could be maximized.
- 🐞 [FIX] The window position and size could not be restored to the previous state after the application was restarted.
- 🐞 [FIX] Proxy terminal could not intercept requests sent by Nodejs fetch.
- 🐞 [FIX] HTTPS request sent by axios in proxy terminal has no response.
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

## v2.33.12 <small><small>*2025-04-23*</small></small>
- 💪 [OPT] Reduce memory usage and lag in some scenarios.
- 💪 [OPT] Large data is displayed as `<...>` in the raw tab to avoid performance issues.
- 💪 [OPT] Python-Requests code snippet will use full url instead of param dict.
- 💪 [OPT] The `=` in the parameter value of URL is no longer automatically transcoded to `%3D`.
- 🐞 [FIX] The bug that the parameter name and parameter value of the URL will be lost when both are empty.

## v2.33.11 <small><small>*2025-04-22*</small></small>
- 💪 [OPT] SSE list supports switching between positive and reverse order.
- 💪 [OPT] WebSocket list supports switching between forward and reverse order.
- 💪 [OPT] A tooltip will display when the mouse hovers over the home page tab.
- 🐞 [FIX] The bug that the WebSocket frame read status is incorrect after search and filtering.
- 🐞 [FIX] The bug that the HTTP method of the new location is not changed to GET during 301, 302 and 303 redirection.
- 🐞 [FIX] The bug that the icon button may not trigger the click event when clicked continuously.
- 🐞 [FIX] The bug that the rewrite redirect path `*` replacement may fail.
- 🐞 [FIX] The bug that the log file location cannot be opened in the debug tool window.

## v2.33.10 <small><small>*2025-04-21*</small></small>
- 💪 [OPT] When MIME is non-text type, the data will not be detected for character encoding.
- 💪 [OPT] API testing turns off `Follow Debug` will switch to `Unset` instead of `Follow System`.
- 💪 [OPT] Python scripts support using `[]` to operate binary and multipart type data.
- 💪 [OPT] Delete the shortcut key prompt of the `Export` menu.
- 💪 [OPT] The URL scheme for importing Swagger API uses http instead of https.
- 🐞 [FIX] The bug that data saved under the `Hex` may not be the displayed data.

## v2.33.9 <small><small>*2025-04-15*</small></small>
- 💪 [OPT] Copy as JSON will automatically remove the built-in empty value header.
- 🐞 [FIX] The bug that the exported Postman file does not indicate scheme.
- 🐞 [FIX] The bug that the top-level API collection directory can be dragged and moved to other subfolders.
- 🐞 [FIX] The bug that copy content of the script editor console is incorrect.

## v2.33.8 <small><small>*2025-04-02*</small></small>
- 💪 [OPT] WebSocket and SSE JSON payload will prettified automatically.
- 💪 [OPT] Table view supports using `Tab` key to move focus to the next cell.
- 💪 [OPT] Code snippet copy no longer automatically closes the pop-up dialog.
- 🐞 [FIX] The bug that the `Content-Type` header is not automatically deleted when creating form-data API from traffic list.
- 🐞 [FIX] The bug that generated MITM certificates are not cleared after importing CA certificate.
- 🐞 [FIX] The bug that some requests have been completed but the status is displayed as processing or abort.
- 🐞 [FIX] The bug that cURL export does not correctly handle JSON comments.
- 🐞 [FIX] The bug that closing the main window in multi-window state may cause the program to crash.

## v2.33.7 <small><small>*2025-03-27*</small></small>
- 🐞 [FIX] The bug that the boundary in `Content-Type` was missing in form-data requests.

## v2.33.6 <small><small>*2025-03-27*</small></small>
- 💪 [OPT] Set the built-in headers `Content-Type` and `Content-Length` of API to be unchecked.
- 💪 [OPT] Some icons of the API text input box are no longer displayed as available when there is no content.
- 💪 [OPT] When cURL imports urlencode, it will automatically decode the key-value.
- 💪 [OPT] When cURL exports urlencode, if the value is empty, the equal sign will be omitted.
- 💪 [OPT] The traffic list search supports comments and console content.
- 💪 [OPT] Rewrite and breakpoint support more HTTP status codes.
- 🐞 [FIX] The bug that the built-in header `Content-Length` of API may lost.
- 🐞 [FIX] The bug that the diff tool does not sort by value when the header names are the same.
- 🐞 [FIX] The bug that the content of the diff tool is displayed incorrectly when the chunk is folded.
- 🐞 [FIX] The bug that the line number is displayed incorrectly when only one is selected in the diff tool.

## v2.33.5 <small><small>*2025-03-20*</small></small>
- 💪 [OPT] JSON syntax highlighting uses loop mode.
- 💪 [OPT] JSON Streaming data is automatically combined into an array when displayed.
- 💪 [OPT] Set-Cookie parsing no longer verifies data.
- 💪 [OPT] Add `Collapse All` and `Expand All` options to the context menu of the API collection folder.
- 💪 [OPT] Adjust the margins of some tool windows.
- 🐞 [FIX] The bug that `+` in URL parameters is automatically encoded as `%2B`.
- 🐞 [FIX] The bug that the new location URL has an encoding error in redirection.
- 🐞 [FIX] The bug that the `entry-viewer` page cannot be found in the subwindow.

## v2.33.4 <small><small>*2025-03-17*</small></small>
- 💪 [OPT] API testing supports using shortcut `Control + N` to open a new window to view the response data.
- 💪 [OPT] API testing supports using shortcut `Shift + Control + Y` to add the session to the diff pool list.
- 💪 [OPT] Script environment setup has been added to the `Tools` menu.
- 💪 [OPT] Changelogs has been added to the `Help` menu.
- 💪 [OPT] The currently selected tab will be maintained when opening the request or response in a new window.
- 💪 [OPT] The image viewer supports using `Control + V` to directly load base64 image data from the clipboard.
- 💪 [OPT] When detecting the Python environment, prioritize `python.exe` instead of `python3.exe`.
- 💪 [OPT] When background mode is enabled, `Alt + F4` will enter the background instead of exiting the program.
- 🐞 [FIX] A bug that API converts `%20` to `+`.
- 🐞 [FIX] A bug that duplicate `Transfer-Encoding` and `Content-Encoding` will cause repeated decoding.
- 🐞 [FIX] The error `no module named 'reqable'` will throw when using Python Embeddable Package.

## v2.33.3 <small><small>*2025-03-12*</small></small>
- 💪 [OPT] Greatly improve the performance of JSON syntax highlighting.
- 💪 [OPT] Improve the implementation of HTTP2 protocol.
- 💪 [OPT] Proxy terminal supports opening PWSH.
- 🐞 [FIX] The bug of abnormal syntax highlighting when the HTTP header contains a name starting with a number.
- 🐞 [FIX] The bug of abnormal syntax highlighting when the HTTP header contains a dot symbol.

## v2.33.2 <small><small>*2025-03-07*</small></small>
- 💪 [OPT] Support disabling URL input autocomplate in API request settings.
- 💪 [OPT] Now can open a new API tab from request traces.
- 💪 [OPT] Capture interceptor view will display the original URL of the rewrite-redirect.
- 🐞 [FIX] SSE cannot be displayed when response header Content-Type contains charset.
- 🐞 [FIX] Traffic list search condition save icon can still be interactive when it is not displayed.
- 🐞 [FIX] Traffic tab icon displays abnormally when switching Zen mode.
- 🐞 [FIX] The bug that malformed request or response execution breakpoint, rewrite, script will cause a failure.
- 🐞 [FIX] The bug that malformed request or response body cannot be displayed in diff view.
- 🐞 [FIX] The bug that the system proxy indicator is not updated in time when automatic capture is enabled.

## v2.33.1 <small><small>*2025-03-04*</small></small>
- 🐞 [FIX] The bug that an error throws when creating the form-data body.

## v2.33.0 <small><small>*2025-03-04*</small></small>
- 🚀 [NEW] Request traces feature in REST explorer panel.
- 🚀 [NEW] Add a diff tool for REST.
- 💪 [OPT] Automatically restore the response data of API testing after the application is restarted.
- 💪 [OPT] Turn off automatic query parameter decoding when inputting URL in API testing.
- 💪 [OPT] API testing provides query parameter decoding option.
- 💪 [OPT] The default setting of REST proxy option is changed to `No Proxy`.
- 💪 [OPT] API collection will check and fix duplicate IDs.
- 💪 [OPT] Unify the size and color value of borders and dividers.
- 💪 [OPT] Automatically refresh cookies when redirecting.
- 💪 [OPT] Fixed traffic tab to the left when scrolling.
- 💪 [OPT] Base64 tool supports loop decoding mode.
- 💪 [OPT] Base64 tool supports fast transfer of output to input.
- 💪 [OPT] Traffic bookmark filters support right-clicking folders to select all or unselect all.
- 💪 [OPT] Traffic list provides more copy options.
- 💪 [OPT] Traffic list provides the `Connection Reuse` selection option.
- 💪 [OPT] The default name of API from HAR will use the host rather than untitled.
- 💪 [OPT] Adjust the order of shortcut keys `Ctrl` and `Shift` prompts.
- 🐞 [FIX] The bug that redirect data is displayed in disorder.
- 🐞 [FIX] The bug that the prompt in traffic details is incorrect when the root certificate is not installed.
- 🐞 [FIX] The bug that the duplicate folder items were not saved to database.
- 🐞 [FIX] The bug that the help doc urls of rewriting are not correct.
- 🐞 [FIX] The bug that an error throws when creating the form-data body.

## v2.32.6 <small><small>*2025-02-27*</small></small>
- 🐞 [FIX] The bug that scripting is not working.

## v2.32.5 <small><small>*2025-02-26*</small></small>
- 💪 [OPT] Disable charset detection for JSON data, and use utf-8 by default.

## v2.32.4 <small><small>*2025-02-26*</small></small>
- 💪 [OPT] Improve charset detection mechanism.
- 🐞 [FIX] A bug in which garbled characters may be displayed after modifying data using rewrite, breakpoints, and scripts.

## v2.32.3 <small><small>*2025-02-25*</small></small>
- 💪 [OPT] Automatic inference will be attempted when charset is not specified in the `Content-Type` header.
- 💪 [OPT] The export curl window will no longer be automatically closed after copying.
- 💪 [OPT] The limit of database capacity is increased from 10G to 64G.
- 💪 [OPT] API collection supports duplicating folders.
- 💪 [OPT] Adjust the position and style of the icon button at the bottom of the script log console.
- 💪 [OPT] The traffic list ID is displayed in the prefix of the script log in script editor console.
- 💪 [OPT] A close button will be displayed in the upper right corner of the blank traffic details.
- 💪 [OPT] The UUID tool supports setting without hyphens.
- 🐞 [FIX] A bug that REST API may fail to merge cookies.
- 🐞 [FIX] A bug that may show a gray screen when opening the favorited WebSocket.
- 🐞 [FIX] A bug that causes the redirect title display to overlap.
- 🐞 [FIX] A bug that causes incorrect response body processing when the response header does not contain `Content-Length` and `Transfer-Encoding`.
- 🐞 [FIX] The bug that the websocket based on aiohttp cannot be connected in the proxy terminal.
- 🐞 [FIX] The bug that python scripts in the proxy terminal environment may report an error.
- 🐞 [FIX] The bug that OpenAPI(Swagger) file importing throws an error.

## v2.32.2 <small><small>*2025-02-21*</small></small>
- 💪 [OPT] Report server supports uploading a user defined tag.
- 💪 [OPT] Android network request stacktrace supports syntax highlighting.
- 💪 [OPT] Adjust the home page tab interaction logic.
- 💪 [OPT] Adjust the right-click menu options of the API collection.
- 💪 [OPT] Add some shortcuts for API collection.
- 🐞 [FIX] The bug that a gray screen will shown when exporting curl of basic auth API.
- 🐞 [FIX] The bug that basic authorized curl becomes digest authorized after import.

## v2.32.1 <small><small>*2025-02-19*</small></small>
- 💪 [OPT] JSON Tree context menu adds node search item.
- 🐞 [FIX] The bug where the API collection subfolder name may become untitled after upgraded from an old version.
- 🐞 [FIX] A bug where the window maximize icon may display incorrectly.

## v2.32.0 <small><small>*2025-02-17*</small></small>
- ❗ [IMP] Data structure upgrade, please do not downgrade to the old version after upgrading.
- 🚀 [NEW] API collection supports folder-level configuration like authorization and scripting.
- 🚀 [NEW] The traffic list supports exporting data according to the file structure.
- 🚀 [NEW] `Gateway`, `Rewrite`, `Breakpoint` and `Script` matching rules support specifying the HTTP method.
- 🚀 [NEW] Applications and domain names in explorer support copying.
- 💪 [OPT] Redesign the UI/UX of HTTP custom method management.
- 💪 [OPT] JSON tree view supports node single-click.
- 💪 [OPT] File naming rules for traffic list data export.
- 💪 [OPT] The API collection distinguishes between root directories and subdirectories, and cannot be changed by dragging and dropping.
- 💪 [OPT] The variable value can be copied in the environment variable mouse hover prompt view.
- 💪 [OPT] The environment variable name supports the `-` symbol.
- 💪 [OPT] Fully support user custom HTTP methods.
- 💪 [OPT] Adjust the display order of `Mirror` and `Gateway`.
- 💪 [OPT] The `Breakpoint` executor window can directly open the hit breakpoint rule window.
- 🐞 [FIX] A bug that the API tab fails to be automatically closed when deleting an API from the collection.
- 🐞 [FIX] A bug that the API header name uses environment variables to prompt an illegal name.
- 🐞 [FIX] A bug that the Android network stack information is not saved in the history.
- 🐞 [FIX] The API collection data may be imported with an error.
- 🐞 [FIX] The bug that the global environment variable data is written to the user environment after the script is executed.
- 🐞 [FIX] A bug that the tab does not have a modification mark when editing an API script.
- 🐞 [FIX] A bug that the environment variables are not parsed when copying URLs and cURL in the collection list.
- 🐞 [FIX] A bug that ADB may not be able to discover Android devices.

## v2.31.3 <small><small>*2025-01-21*</small></small>
- 💪 [OPT] Automatically remember the sidebar status and restore it after restarting the app.
- 💪 [OPT] Traffic records related to applications and hosts can be deleted with one click in the traffic list explorer.
- 💪 [OPT] JSON/XML/HEX tools support file dragging and file selector.
- 💪 [OPT] JSON escape tool supports JSON formatting and compression.
- 💪 [OPT] JSON escape tool no longer escapes line breaks.
- 🐞 [FIX] The bug that the exported raw data has no separator between request and response.
- 🐞 [FIX] in API testing, the sent request body is not updated after replacing the content.
- 🐞 [FIX] The bug that ADB cannot discover Android devices in some cases.
- 🐞 [FIX] A bug that the display position of the environment variable drop-down menu may be seriously offset.
- 🐞 [FIX] The conflict between the search and replace `Enter` shortcut key and the IME input `Enter` key.

## v2.31.2 <small><small>*2025-01-15*</small></small>
- 💪 [OPT] Double-clicking an API in collection and history list will enter the edit mode instead of the reading mode.
- 🐞 [FIX] The bug that API testing Bearer Token authorization cannot be used.
- 🐞 [FIX] The bug that some text is overflow or clipped.
- 🐞 [FIX] The bug that the text displayed in the API tab title is truncated prematurely.
- 🐞 [FIX] The bug that SSE content contains non-ASCII data will cause a parsing error.

## v2.31.1 <small><small>*2025-01-14*</small></small>
- ❗ [IMP] Data structure upgrade, please do not downgrade to the old version after upgrading.
- 🚀 [NEW] API collection supports exporting Postman v2.1 collection files.
- 🚀 [NEW] Home page tab UI/UX adjustment, supports temporary reading mode (title italicized).
- 💪 [OPT] API testing supports JSON single-line comments.
- 💪 [OPT] User-Agent is no longer filled in by default, but the request sent will still use the Reqable flag.
- 💪 [OPT] After disabling Reqable Id in the API settings, this item will no longer be displayed in the header list.
- 💪 [OPT] Form-data body supports entering JSON key-value pairs in text mode.
- 💪 [OPT] In API testing, comments in text editing mode will be highlighted.
- 💪 [OPT] The duplicated API will be inserted after the original API instead of being added to the end of the list.
- 💪 [OPT] The collection path is displayed in the API collection search result list.
- 💪 [OPT] The activated environment will be displayed with the first letter instead of the icon.
- 💪 [OPT] Automatically expand and mark the position of the API of the current tab in the collection.
- 💪 [OPT] Automatically mark the position of the current tab in the traffic history list.
- 🐞 [FIX] The bug that the data of unchecked parameters in API testing is wrong after reloading.
- 🐞 [FIX] The bug that digest authorization may fail.
- 🐞 [FIX] The bug that the cURL imported with cmd format did not correctly handle some `^` escape characters.
- 🐞 [FIX] The bug that some JSONP could not be automatically parsed into JSON.
- 🐞 [FIX] The bug that the environment variables were not displayed properly in ellipsis mode in the table view.
- 🐞 [FIX] The bug that may report an error when starting after upgrading the version.
- 🐞 [FIX] The bug that the pop-up window cannot be opened correctly when exporting cURL for illegal URLs.
- 🐞 [FIX] The bug that the rewrite, breakpoint and scripting may cause some HTTP2 requests to fail.
- 🐞 [FIX] The conflict shortcut keys between editor line break and sending API request.
- 🐞 [FIX] The bug of not supporting non-ASCII headers in some scenarios.
- 🐞 [FIX] The bug that JSON Tree in the new window may display abnormally.
- 🐞 [FIX] The bug that collaborative QR code may display abnormally.
- 🐞 [FIX] The bug that the right-click script creation from the traffic list does not take effect.
- 🐞 [FIX] A bug where app configuration may lost and can not be restored.

## v2.30.4 <small><small>*2025-01-10*</small></small>
- ❗ [BETA] v2.31.0 beta testing.

## v2.30.3 <small><small>*2024-12-05*</small></small>
- 💪 [OPT] Import collection and environment files are more robust.
- 🐞 [FIX] The bug that failed to import cURL in cmd format.
- 🐞 [FIX] The bug that text search has results but cannot be automatically located.
- 🐞 [FIX] The bug that text rendering issue in search mode.
- 🐞 [FIX] The bug that failed to import some Postman collection files.

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
- 💪 [OPT] Improve the API collection and environment variable import guidelines.
- 💪 [OPT] SSE message list supports right-click context menu.
- 💪 [OPT] WebSocket frame list supports right-click context menu.
- 💪 [OPT] Rewrite rules explicitly prompt whether regular expressions are enabled.
- 💪 [OPT] The traffic list will display rewrite redirected URL instead of the original URL.
- 🐞 [FIX] A bug that caused the application to crash when inputting an non-ascii domain name.
- 🐞 [FIX] A bug that failed to import the API through cURL in some cases.
- 🐞 [FIX] A bug that `basePath` is lost when importing Swagger 2.0 API.
- 🐞 [FIX] A bug that the Postman environment variables cannot be imported.
- 🐞 [FIX] Win7 startup error of GetSystemMetricsForDpi.

## v2.30.1 <small><small>*2024-11-26*</small></small>
- 🚀 [NEW] Fully support SSE real-time streaming.
- 🚀 [NEW] API testing supports digest-auth authorization.
- 🚀 [NEW] Add JSON tree viewer.
- 🚀 [NEW] Python scripting can add the comment for a request.
- 🚀 [NEW] The toolbox adds the UUID generator tool.
- 🚀 [NEW] The toolbox adds the JSON escape tool.
- 💪 [OPT] Minor adjustments to the background colors of light and dark themes.
- 💪 [OPT] MITM proxy server requests will display in the traffic list.
- 💪 [OPT] The request body and response body will automatically save the state when switching between different views.
- 💪 [OPT] The URL generated by the basic authorization request uses the `--basic` parameter instead of the `Authorization` request header.
- 💪 [OPT] Payload with encoding errors will display the original data instead of the FormatException error.
- 💪 [OPT] Create a folder according to the tag when importing OpenAPI file.
- 💪 [OPT] Use `operationId` as the API alternative name when importing OpenAPI file.
- 💪 [OPT] Automatically add `=` padding at the end of the input during Base64 decoding.
- 💪 [OPT] Correct the label and the order of right-click menu options for selected text.
- 💪 [OPT] Some search input boxes support using shortcut keys ⬆️ and ⬇️ to switch historical search records.
- 💪 [OPT] Adjust other UI details.
- 🐞 [FIX] The bug of infinite loop when sending requests to MITM server with LAN IP.
- 🐞 [FIX] The bug that the initial position of the subwindow is not displayed correctly under multiple screens.
- 🐞 [FIX] The bug that shortcut keys will conflict between API request script editor and API save.
- 🐞 [FIX] The bug that Postman API collections exported by third-party cannot be imported into Reqable.
- 🐞 [FIX] The bug that JSON viewer option in right-click menu is unavailable.
- 🐞 [FIX] The bug that some tips related to shortcut keys in the bottom bar are incomplete.
- 🐞 [FIX] The bug that some text has an incorrect font display.

## v2.29.2 <small><small>*2024-11-14*</small></small>
- 🐞 [FIX] The bug that name of attachment file is incorrect.
- 🐞 [FIX] The bug that some HTTP traffic may not be displayed correctly.

## v2.29.1 <small><small>*2024-11-14*</small></small>
- 💪 [OPT] Use `Control + ⬆️/⬇️` shortcut keys to navigate viewed traffic item.
- 💪 [OPT] If the system has VPN turned on, a prompt will be given when override system proxy.
- 💪 [OPT] Remove the green dot flashing animation of the debugging status.
- 💪 [OPT] Message digest and HMAC calculation support empty string input.
- 🐞 [FIX] The bug that base64 data with the prefix `data:` cannot pop up context menu.
- 🐞 [FIX] The bug that API save status is incorrect in some cases.
- 🐞 [FIX] The bug that the `-u` authorization is lost after importing cUrl.
- 🐞 [FIX] The bug that some HTTP traffic may not be displayed.
- 🐞 [FIX] The bug that the Win10 and Win11 clipboard history cannot be used.

## v2.29.0 <small><small>*2024-11-10*</small></small>
- 🚀 [NEW] Now can import Insomnia API collections.
- 🚀 [NEW] Now can import Swagger (OpenAPI) APIs.
- 🚀 [NEW] The toolbox adds SHA1, SHA256, SHA512 and other message digest.
- 🚀 [NEW] The toolbox adds HMAC tool.
- 🚀 [NEW] The toolbox adds AES encryption and decryption tool.
- 🚀 [NEW] Redesign the UI and UX of the toolbox.
- 🚀 [NEW] Add the `Crypto` option to the right-click menu after selecting text.
- 🚀 [NEW] Add the `Extract Copy` option to the right-click menu after selecting text.
- 🚀 [NEW] Some lists provide sorting options.
- 💪 [OPT] `Duration` in the traffic list is accurate to milliseconds.
- 💪 [OPT] The toolbox merges the two categories of `Encoding` and `Decoding`.
- 💪 [OPT] Environments will be automatically imported when importing API collections of third-party apps.
- 💪 [OPT] The available status of JSON and XML in the right-click view menu will be more reasonable.
- 💪 [OPT] The image viewer supports base64 format with the prefix `data:`.
- 💪 [OPT] The API `Omit Equal Sign` option is moved to the request settings.
- 💪 [OPT] Python-Requests code generation template.
- 🐞 [FIX] The bug that the requests interrupted by interceptors cannot be edited.
- 🐞 [FIX] The bug that the requests interrupted by interceptors lose the request body.
- 🐞 [FIX] The bug that the traffic list search box was unable to input chinese.
- 🐞 [FIX] The bug that the right-click menu may not disappear in some input fields.
- 🐞 [FIX] The bug that the right-click menu may not popup in some tables.
- 🐞 [FIX] The bug that the Apipost collection import failed.
- 🐞 [FIX] The file name for uploading is no longer URL-encoded.
- 🐞 [FIX] The bug that multipart header names are converted to lowercase when parsing.

## v2.28.0 <small><small>*2024-11-04*</small></small>
- 🚀 [NEW] Community edition no longer limits the number of API tabs.
- 🚀 [NEW] Introduce interceptor tab to track running processes.
- 🚀 [NEW] Support saving traffic list search options.
- 🚀 [NEW] Support setting highlights from Python scripts.
- 🚀 [NEW] Interceptor filtering and highlighting support gateway rules.
- 🚀 [NEW] The `Raw` tab will display the decoded body by default.
- 💪 [OPT] Remove the `Capture` prefix from the Python script class name.
- 💪 [OPT] Automatically prompt historical keywords for traffic list search.
- 💪 [OPT] Requests blocked and suspended by the gateway will display their content in the traffic list.
- 💪 [OPT] Add zen mode switch in the app settings.
- 💪 [OPT] Now can move rules to specified folders in right-click context menus.
- 💪 [OPT] Opening the rewrite replacement rule will automatically switch to the enabled tab.
- 🐞 [FIX] The bug that the move up and move down states of the rule item in right-click menu are not correct.
- 🐞 [FIX] The bug that the search box state is not closed after clicking the clear icon in the rule list.
- 🐞 [FIX]Some bugs in rewriting redirection.

## v2.27.2 <small><small>*2024-10-29*</small></small>
- 💪 [OPT] Adjust UI of some dialogs.
- 💪 [OPT] Keep the selected display type of body when switching.
- 🐞 [FIX] The bug that adding or modifying the comment of favorites will not be saved.
- 🐞 [FIX] The bug that non-ASCII file names cause multipart data to not display properly.
- 🐞 [FIX] The bug that some settings do not take effect when importing cURL or HTTP raw for API.
- 🐞 [FIX] The bug that HTTP2 rewrite redirection may cause the connection broken.
- 🐞 [FIX] The bug that non-ASCII file names in multiparts will cause breakpoints not working.

## v2.27.1 <small><small>*2024-10-22*</small></small>
- 🚀 [NEW] Support more accent colors and user-defined accent colors.
- 🚀 [NEW] Show application information in request overview.
- 🚀 [NEW] Support creating API from HTTP raw request message.
- 🚀 [NEW] Introduce in app notification feature.
- 🚀 [NEW] Traffic list supports exporting CSV format files.
- 🚀 [NEW] Add `Request & Response` layout option in settings.
- 🚀 [NEW] Add color viewer in toolbox.
- 💪 [OPT] Request overview will remember the expanded and closed states of each group.
- 💪 [OPT] History will remember the last selected type.
- 💪 [OPT] Generated cURL command will include protocol version.
- 💪 [OPT] Enhance cURL command import.
- 💪 [OPT] Detached windows will use current layout direction.
- 💪 [OPT] In Zen mode, the traffic tab only displays an icon when not selected.
- 💪 [OPT] The request that is aborted by breakpoints, rewrites, scripts will be displayed in the traffic list.
- 💪 [OPT] When a request is aborted by breakpoints, rewrites, and scripts, the reason will be displayed in the details.
- 💪 [OPT] The copywriting of some tools in the toolbox.
- 💪 [OPT] Base64 encoding and decoding supports more charsets.
- 💪 [OPT] Support manual configuration of ADB path.
- 💪 [OPT] Support shrinking and adjusting the subwindow size.
- 🐞 [FIX] The bug that the `Buy` button cannot be redirected.
- 🐞 [FIX] A crash bug cuased by rewrite redirect.

## v2.26.1 <small><small>*2024-10-14*</small></small>
- 🚀 [NEW] Introduce `Proxy Terminal` feature.
- 🚀 [NEW] A new CA certificate setup guide.
- 🚀 [NEW] Android root devices support one-click installation of CA certificate via ADB.
- 🚀 [NEW] A Deep search option for traffic list searching.
- 💪 [OPT] Uri tool supports three input modes.
- 💪 [OPT] Middle ellipsis for long context menu text.
- 🐞 [FIX] A bug that WebSocket will broken due to incorrect frame codec.
- 🐞 [FIX] A Bug that environment variable writing may not take effect in scripts.

## v2.25.1 <small><small>*2024-10-07*</small></small>
- 💪 [OPT] WebSocket message timestamp is accurate to milliseconds.
- 💪 [OPT] Android certificate installation guide.
- 💪 [OPT] Adjust the size of the image view window.

## v2.25.0 <small><small>*2024-09-30*</small></small>
- 🚀 [NEW] Introduce favorite request list.
- 🚀 [NEW] Support deleting items in traffic history list.
- 🚀 [NEW] Support opening images in a new window.
- 🚀 [NEW] Support opening binary in a new window.
- 🚀 [NEW] Support opening API response in a new window.
- 🚀 [NEW] Support using the shortcut `Control + Shift + I` to quickly import cURL from the clipboard.
- 🚀 [NEW] support using the shortcut key `Control + Shift + E` to generate cURL and write it to the clipboard.
- 💪 [OPT] Backup the database instead of deleting it when the database is downgraded and cannot be opened.
- 💪 [OPT] The shortcut key for automatically saving history in API testing is changed from `Control + Shift + H` to `Alt + H`.
- 💪 [OPT] The shortcut key for auto-cookie in API testing is changed from `Control + Shift + C` to `Alt + C`.
- 💪 [OPT] The shortcut key for Reqable ID in API testing is changed from `Control + Shift + I` to `Alt + I`.
- 💪 [OPT] Dialog positive button can be triggered by the `Enter` shortcut key.
- 🐞 [FIX] The bug that AVIF images cannot be displayed normally on some platforms.
- 🐞 [FIX] The bug that Android certificate hash name may lack prefix 0.
- 🐞 [FIX] The bug of failing to restore a damaged SharedPreferences file from backups.

## v2.24.0 <small><small>*2024-09-23*</small></small>
- 🚀 [NEW] Introduce image viewer in toolbox.
- 🚀 [NEW] The Base64 string of image can be previewed through the image viewer.
- 🚀 [NEW] You can repeat requests in the breakpoint window.
- 🚀 [NEW] Add social media entrances to the bottom bar.
- 💪 [OPT] Support previewing of image in AVI, AVIF and APNG formats.
- 💪 [OPT] Repeat provides a reuse connection option, and the connection is no longer reused by default.
- 💪 [OPT] Rewrite redirection no longer sends requests to the original server.
- 💪 [OPT] Breakpoint supports shortcut keys such as `Execute` and `Break`.
- 💪 [OPT] Adjust tray menu options.
- 💪 [OPT] The tray tooltip will show the recording status.
- 🐞 [FIX] The bug that animated image only display the first frame.
- 🐞 [FIX] The bug that the tray tooltip does not display.

## v2.23.1 <small><small>*2024-09-12*</small></small>
- 💪 [OPT] Deflate encoding supports decoding with and without headers.
- 💪 [OPT] Update the UI style of some multi-line input boxes.

## v2.23.0 <small><small>*2024-09-05*</small></small>
- 🚀 [NEW] Support network condition simulation.
- 🚀 [NEW] Support viewing of HAR content in clipboard.
- 🚀 [NEW] Support Internationalized Domain Name (IDN) API.
- 💪 [OPT] Import and export API collections will include built-in headers.
- 💪 [OPT] Search condition in traffic list increased from 3 to 5.
- 💪 [OPT] Now can send and download data directly in API testing.
- 💪 [OPT] Proxy recovery logic when exiting the application.
- 💪 [OPT] Use the decoded file name when saving the request and response.
- 🐞 [FIX] The bug that importing reqable collections will lose unnamed APIs.
- 🐞 [FIX] The bug that some requests in HAR file cannot be edited and repeated.
- 🐞 [FIX] The bug that importing some cURLs will lose the body payload.

## v2.22.2 <small><small>*2024-08-28*</small></small>
- 💪 [OPT] Backup SharedPreferences and some other config files.
- 💪 [OPT] WebSocket supports clearing message list.
- 💪 [OPT] WebSocket read messages are displayed in gray.
- 💪 [OPT] WebSocket message details display frame number.
- 💪 [OPT] A new overview URL display view.
- 💪 [OPT] A more reasonable list selection mechanism.
- 🐞 [FIX] The Bug that the gateway cannot edit behavior options.

## v2.22.1 <small><small>*2024-08-27*</small></small>
- 💪 [OPT] HAR files support WebSocket message frames.
- 💪 [OPT] A new URL redirection UI and UX.
- 💪 [OPT] Reduce editor transparency when API testing script is not enabled.
- 💪 [OPT] Unify the size of some pop-up windows.
- 💪 [OPT] More friendly wildcard prompts.
- 🐞 [FIX] A bug that the API testing environment variables may cause the request to fail.
- 🐞 [FIX] A bug that the API testing history may lose the response body.

## v2.22.0 <small><small>*2024-08-19*</small></small>
- 🚀 [NEW] Introduce new rewrite UI and UX.
- 💪 [OPT] Improve configuration file storage performance.
- 💪 [OPT] Support holding down the `Alt` key to force close the tab.
- 💪 [OPT] The console supports text prettify and syntax highlighting.
- 💪 [OPT] More shortcut keys for HexViewer.
- 💪 [OPT] HexViewer supports copying selected data as Base64.
- 💪 [OPT] HexViewer tool displays the total number of bytes.
- 💪 [OPT] The character limit of the QR code tool is increased from 256 to 512.
- 💪 [OPT] The editor context menu supports generating QR codes.
- 🐞 [FIX] Form form multiple decoding causes `+` to become a space bug.
- 🐞 [FIX] The bug that HexViewer selection may be lost in WebSocket viewing.
- 🐞 [FIX] The bug that deflate is not correctly encoded and decoded.
- 🐞 [FIX] The bug that environment variable in `Basic Auth` is not working.
- 🐞 [FIX] The bug that clicking the scroll bar in HexViewer will cancel the current selection.
- 🐞 [FIX] The bug that the drag view position is incorrect after zoom the view.
- 🐞 [FIX] The bug that fork the script template from repository may fail.
- 🐞 [FIX] The bug that the script template repository fails to delete the newly created script.

## v2.21.4 <small><small>*2024-08-08*</small></small>
- 💪 [OPT] Duration time format of history.
- 💪 [OPT] HexViewer supports viewing the total count of bytes.
- 💪 [OPT] Improve the interactive experience of ImageViewer.
- 💪 [OPT] Improve the WebSocket UI.
- 💪 [OPT] Bearer Token input box is changed from single line to multiple lines.
- 💪 [OPT] HTTP request method and response status code can go to MDN documentation.
- 💪 [OPT] Add an documentation link for request and response tab management.
- 💪 [OPT] A batch of `206 Partial Content` records can be selected at once.
- 💪 [OPT] `206 Partial Content` records can be exported into one file.
- 🐞 [FIX] A bug that HTTP raw message syntax may not be highlighted.
- 🐞 [FIX] A bug that the proxy port number may be displayed incorrectly.
- 🐞 [FIX] A bug that can not move down the bookmark.

## v2.21.2 <small><small>*2024-08-02*</small></small>
- 💪 [OPT] Supports HTTP `103 Early Hints`.
- 💪 [OPT] Supports HTTP2 `Trailers`.
- 💪 [OPT] Supports `Windows-31J`, `Shift-31J` and `EUC-JP` character encodings.
- 💪 [OPT] Upgrade Flutter to v3.19.6，fix multi-window crash issue.
- 🐞 [FIX] The bug where `Early Hints` causes the response header and body to not display correctly.
- 🐞 [FIX] MITM does not handle `100 Continue` requests correctly.
- 🐞 [FIX] The bug that python scripts lose URL params.
- 🐞 [FIX] The bug that reverse proxy automatically adds non-original request headers.

## v2.21.1 <small><small>*2024-07-29*</small></small>
- 💪 [OPT] Automatically decode URL parameters when importing cURL.
- 💪 [OPT] The traffic list header column management.
- 🐞 [FIX] A bug that may lose the request body when importing form-data cRUL requests.
- 🐞 [FIX] A bug that the generated code Python-requests may lose the form-data request body.
- 🐞 [FIX] A bug that two identical applications may appear in the traffic list sidebar.

## v2.21.0 <small><small>*2024-07-23*</small></small>
- 🚀 [NEW] Support editing HAR files.
- 🚀 [NEW] Support access control.
- 🚀 [NEW] Support text editing mode for form-data.
- 🚀 [NEW] Copy query parameters, headers, etc. as JSON.
- 🚀 [NEW] Support importing collection data from HAR files.
- 🚀 [NEW] Condition matching for traffic list search.
- 🚀 [NEW] Support filtering applications and domains in explorer.
- 🚀 [NEW] A new `Select` menu is added to the right-click of the traffic list.
- 🚀 [NEW] License supports configuring network proxies.
- 🚀 [NEW] Various useful tips in the bottom bar.
- 💪 [OPT] Tab title style and indicator style.
- 💪 [OPT] HAR export request and response body do not use base64 encoding first.
- 💪 [OPT] Compatible with some non-standard IPv6 proxy requests.
- 💪 [OPT] Adjust the position of the collection search input field.
- 💪 [OPT] Adjust the position of the history search input field.
- 💪 [OPT] The traffic list URL will display mirroring host rather than the proxy host.
- 💪 [OPT] The shortcut key for adding API to the collection from the traffic list is changed from `Control` + `S` to `Control` + `I`.
- 💪 [OPT] Drag with `Control` for continuous list item selection.
- 🐞 [FIX] The bug that that may fail to open HAR file.
- 🐞 [FIX] Secondary proxy authentication issue.
- 🐞 [FIX] The bug that SSL proxy cannot hit some HTTPS requests.
- 🐞 [FIX] A bug that the API request data may not be updated when using shortcut keys to send the request.

## v2.20.2 <small><small>*2024-07-16*</small></small>
- 💪 [OPT] Key-value pair type data supports copying as JSON.
- 💪 [OPT] Traffic list search supports `or` logical relationship.
- 💪 [OPT] Enables loopback proxy by default.
- 💪 [OPT] Only bypass localhost in non-loopback proxy mode.
- 🐞 [FIX] The bug that may fail to open HAR file.
- 🐞 [FIX] The bug that some URL input cannot expand multiple lines.

## v2.20.1 <small><small>*2024-07-12*</small></small>
- 💪 [OPT] Support HEX viewer for raw message.
- 💪 [OPT] Delete duplicate java.net.http code snippet.
- 💪 [OPT] API testing supports sending request with empty request header value.
- 💪 [OPT] Traffic list supports compose and repeat shortcut keys when there is no focus.
- 🐞 [FIX] A bug where importing raw multipart curl loses the last Part.
- 🐞 [FIX] Incorrect implementations for websocket extensions.
- 🐞 [FIX] Open a HAR file will lost the highlighting.

## v2.20.0 <small><small>*2024-07-08*</small></small>
- 🚀 [NEW] Introduce report server feature.
- 🚀 [NEW] Supports `Zstandard` encoding and decoding.
- 🚀 [NEW] Supports C# HttpClient and RestSharp code snippet.
- 🚀 [NEW] Supports Java Apache HttpClient code snippet.
- 🚀 [NEW] Supports raw multipart data from curl.
- 🚀 [NEW] Right-click to add traffics to a new capture session.
- 💪 [OPT] SSL proxy rules support configuring port numbers.
- 💪 [OPT] Improve API request cURL import and export input box.
- 💪 [OPT] Improve multipart table mode UI/UX.
- 🐞 [FIX] The bug of syntax highlighting rendering.
- 🐞 [FIX] The bug that request parameters may be lost when reading HAR files.

## v2.19.1 <small><small>*2024-07-02*</small></small>
- 💪 [OPT] API requests give priority to using custom Host as SNI.
- 💪 [OPT] API request parameters, headers, and form editing automatically convert JSON key-value pairs.
- 💪 [OPT] curl import and export support `--insecure` option.
- 💪 [OPT] Right-click of traffic item can open url in browser.
- 💪 [OPT] Limit the number of tabs opened at one time to a maximum of 32.
- 💪 [OPT] Traffic search supports filtering unhighlighted data.
- 🐞 [FIX] Fix the bug where reverse proxy access exception.

## v2.19.0 <small><small>*2024-06-26*</small></small>
- 🚀 [NEW] The home page `+` right click can automatically create API from cURL/URL on pasteboard.
- 💪 [OPT] The traffic export provides more options.
- 💪 [OPT] The image preview displays information such as format, size and size.
- 💪 [OPT] The pasteboard url will display on the top of the url drop-down list.
- 💪 [OPT] The API collection import dialog displays cURL icon.
- 💪 [OPT] The request and response tabs will auto-collapsed when the space is not enougth.
- 💪 [OPT] When only one comparison item is selected in diff tool, its content will also be displayed.
- 💪 [OPT] Logic of restoring system network proxy settings.
- 🐞 [FIX] When more than 2 requests are selected to add to diff pool, only 2 are successfully added.

## v2.18.1 <small><small>*2024-06-17*</small></small>
- 💪 [OPT] Cookie view allows cookies to be displayed in a merged or split.
- 💪 [OPT] Traffic list allows cURLs for multiple requests to be copied at once.
- 💪 [OPT] Traffic list allows multiple API requests to be created at once.
- 🐞 [FIX] A bug that ALPN is displayed incorrectly.
- 🐞 [FIX] A bug that some empty tips are displayed incorrectly.
- 🐞 [FIX] A bug that using IP by SOCKS proxy are automatically bypassed by SSL proxying.
- 🐞 [FIX] A bug that restarting MITM proxy server may fail.

## v2.18.0 <small><small>*2024-06-11*</small></small>
- 🚀 [NEW] WebSocket frames support search and filtering.
- 🚀 [NEW] SSL proxy and secondary proxy lists support search and sorting.
- 🚀 [NEW] Added three options to right-click menu of tab, `Force Close`, `Force Close Others`, and `Force Close All`.
- 🚀 [NEW] SSL certificates support dragging and dropping files for import.
- 💪 [OPT] Improve the prompt text for errors of certificate import and export.
- 💪 [OPT] The `=` in the API request URL is no longer automatically encoded.
- 💪 [OPT] Improve the Android certificate installation guide.
- 💪 [OPT] Logic of the `Close Others` option in the right-click menu of the tab.
- 🐞 [FIX] The bug that single quotes are not escaped when importing and exporting cURL.
- 🐞 [FIX] The bug that the SSL certificate enable/disable status cannot be saved.
- 🐞 [FIX] The bug that the SSL certificate domain name modification cannot be saved.
- 🐞 [FIX] A bug that mobile HTTP requests are unable to match scripting, rewrite and breakpoint rules.
- 🐞 [FIX] A bug that the selected item may change after reordering the SSL proxying and secondary proxy lists.
- 🐞 [FIX] A bug that the `Close` option in the right-click menu of the home page tab is not available.
- 🐞 [FIX] A bug that the URL request query parameter encoding and decoding behavior changes due to the mounting script.
- 🐞 [FIX] A bug that the p12 file path has monospaced character encoding, which prompts that the password is incorrect.

## v2.17.0 <small><small>*2024-06-05*</small></small>
- 🚀 [NEW] Support `SSL Proxying`.
- 🚀 [NEW] Add a search icon in `Raw` tab.
- 🚀 [NEW] Folder level management for `Gateway`, `Mirror`, `Rewrite`, `Breakpoint`, `Script` and `Reverse Proxy`.
- 🚀 [NEW] Drag and drop file to import config files.
- 🚀 [NEW] Search feature for `Gateway`, `Mirror`, `Rewrite`, `Breakpoint`, `Script` and `Reverse Proxy`.
- 💪 [OPT] Remove `SSL Bypass` and merge it into the `SSL Proxying`.
- 💪 [OPT] Provide more export solutions for capture traffic.
- 💪 [OPT] Automatically remember word wrap status.
- 💪 [OPT] A new `Tools` app menu group.
- 💪 [OPT] A new UI style of the secondary proxy list.
- 💪 [OPT] The prompt style when dragging and dropping files on the home page.
- 💪 [OPT] The diff view will display a prompt text when no item is selected.
- 🐞 [FIX] A bug that the API request Cookie path is forcibly converted to lowercase.
- 🐞 [FIX] A bug that the SOCKS proxy does not display the host if hits SSL bypass.
- 🐞 [FIX] The bug that the application in the explorer is not displayed on top after being pinned.
- 🐞 [FIX] The bug that failed to open some multiple windows.

## v2.16.1 <small><small>*2024-05-20*</small></small>
- 💪 [OPT] HTTP2 disables server push by default.

## v2.16.0 <small><small>*2024-05-17*</small></small>
- 🚀 [NEW] WebSocket supports list display mode.
- 🚀 [NEW] Request parameter supports whether to omit `=` for empty value.
- 💪 [OPT] Creating API requests from the traffic list no longer checks non-ASCII characters.
- 💪 [OPT] The default display of WebSocket is changed from chat mode to list mode.
- 💪 [OPT] WebSocket chat mode performance.
- 💪 [OPT] Reset md5 result when input was changed.
- 🐞 [FIX] The bug where WebSocket filtering does not reset type and code filters.
- 🐞 [FIX] The bug that tooltip does not disappear automatically.
- 🐞 [FIX] The bug that some column widths will be automatically restored after some operations.

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
- 💪 [OPT] Rework script template context menu options.
- 🐞 [FIX] A bug where `Content-Type` may be lost when copying cURL from traffic list.
- 🐞 [FIX] The bug that the content of the client certificate in the overview is incorrect.

## v2.14.1 <small><small>*2024-04-30*</small></small>
- 🚀 [NEW] Add app info APIs in python scripting framework.
- 💪 [OPT] Traffic analysis supports abnormal requests with `Content-Length`.
- 💪 [OPT] The file name of request and response body.
- 💪 [OPT] API testing no longer verifies the validity of response headers.
- 💪 [OPT] A new icon will use after the secondary proxy is enabled.
- 🐞 [FIX] The bug that the secondary proxy connection may fail.
- 🐞 [FIX] The bug of API testing settings being reset after restarting the application.
- 🐞 [FIX] A bug where some files were not cleaned after deleting the API testing history.
- 🐞 [FIX] The bug that parsing API testing query input incorrectly.
- 🐞 [FIX] The bug that traffic history search not works.
- 🐞 [FIX] The bug that REST script will lost when importing Reqable's API collection.

## v2.14.0 <small><small>*2024-04-29*</small></small>
- 🚀 [NEW] Add app info APIs in python scripting framework.
- 💪 [OPT] Traffic analysis supports abnormal requests with `Content-Length`.
- 💪 [OPT] The file name of request and response body.
- 💪 [OPT] API testing no longer verifies the validity of response headers.
- 💪 [OPT] A new icon will use after the secondary proxy is enabled.
- 🐞 [FIX] The bug that the secondary proxy connection may fail.
- 🐞 [FIX] The bug of API testing settings being reset after restarting the application.
- 🐞 [FIX] A bug where some files were not cleaned after deleting the API testing history.
- 🐞 [FIX] The bug that traffic history search not works.
- 🐞 [FIX] The bug that REST script will lost when importing Reqable's API collection.

## v2.13.0 <small><small>*2024-04-24*</small></small>
- 🚀 [NEW] API testing supports setting whether to verify SSL certificate.
- 🚀 [NEW] API testing response displays redirect URLs.
- 🚀 [NEW] You can drag to sort environments.
- 🚀 [NEW] Add a quick icon to open the log directory.
- 💪 [OPT] Clear cache in settings will only clear temporary data and not include user data.
- 💪 [OPT] API testing history will save script console outputs.
- 💪 [OPT] The editor still maintains focus after pressing the save shortcut key.
- 💪 [OPT] Enlarge the click effective area of the sidebar Tab.
- 🐞 [FIX] The bug that the redirected request will fail due to incorrect `Host` header value.
- 🐞 [FIX] The bug that `OPTIONS` request status is incorrect.
- 🐞 [FIX] The bug that the secondary proxy can not be copied to create a new one.
- 🐞 [FIX] Incorrect logic of `Close Other Tabs`.
- 🐞 [FIX] The bug where the selected text will lost after right-clicking in the script editor.
- 🐞 [FIX] The bug that the editor cannot automatically get focus when dragging to select content for the first time.
- 🐞 [FIX] The bug of new prompt words (such as finally) appearing again after selecting a prompt word (such as final) in the scripting editor.
- 🐞 [FIX] The bug in which the collection folder automatically collapsed or fails to automatically expand after the API is saved to the collection.

## v2.12.1 <small><small>*2024-04-19*</small></small>
- 💪 [OPT] The focus of the input field is still maintained after selecting auto-complete content in table mode.
- 🐞 [FIX] The bug of API request global setting not taking effect in some cases.
- 🐞 [FIX] The bug that the API request domain name cannot be associated with cookies when using environment variables.
- 🐞 [FIX] The bug that `=` and `&` in API request query entry are not automatically encoded.
- 🐞 [FIX] A bug that some exceptions caused by automatic decoding of API query when created from the traffic list.
- 🐞 [FIX] The bug that the table mode input autocomplte list will be display incomplete near the bottom of the application.
- 🐞 [FIX] A bug that may cause crash when importing p12 certificate.
- 🐞 [FIX] The bug that dragging selection in the editor cannot automatically request focus.
- 🐞 [FIX] A bug where directly importing cURL into the API request input box would cause the app to freeze.
- 🐞 [FIX] Fix the bug where the app information cannot be dumped in some cases.
- 🐞 [FIX] Fix the bug where some chinese fonts are displayed abnormally.

## v2.12.0 <small><small>*2024-04-13*</small></small>
- 🚀 [NEW] Automatic generate a magisk module to install CA certificate.
- 🚀 [NEW] API collection supports importing from cURL.
- 🚀 [NEW] The number of community rewrites limitation is adjusted from 2 to 3.
- 🚀 [NEW] The number of community breakppints limitation is adjusted from 2 to 3.
- 🚀 [NEW] The number of community scripts limitation is adjusted from 2 to 3.
- 🚀 [NEW] The number of community mirrors limitation is adjusted from 2 to 3.
- 🚀 [NEW] The number of community reverse proxy limitation is adjusted from 2 to 3.
- 💪 [OPT] Prompt whether to clear license information when unregistering license.
- 💪 [OPT] Automatically delete configuration backup files older than 14 days.
- 💪 [OPT] Refactor the Android certificate installation guide.
- 🐞 [FIX] Fix the bug where some limitation of the community do not take effect.
- 🐞 [FIX] The bug of window size calculation not considering the taskbar size.

## v2.11.1 <small><small>*2024-04-09*</small></small>
- 🚀 [NEW] Remove the restriction of API collections for Community Edition.
- 🚀 [NEW] Drag and drop for API collections.
- 💪 [OPT] Remove the restriction that the depth of API collections is up to 4.
- 💪 [OPT] Display text first if `application/octet-stream` is a text.
- 🐞 [FIX] The bug that the window size and content rendering area are incorrect under multiple monitors.
- 🐞 [FIX] The bug that double-clicking the application icon or opening a HAR file will reset the maximized state of the window.

## v2.10.2 <small><small>*2024-04-02*</small></small>
- 🐞 [FIX] The bug that the editor and text display empty.

## v2.10.1 <small><small>*2024-04-02*</small></small>
- 💪 [OPT] Query parameter parsing automatically identifies gbk encoding.
- 💪 [OPT] Disable the custom tab settings in detected window.
- 🐞 [FIX] The bug that the environment variable `<<url>>` is not highlighted.
- 🐞 [FIX] The bug of abnormal `chunked` decoding in some cases.
- 🐞 [FIX] The bug that exporting HAR throws the format error.

## v2.10.0 <small><small>*2024-03-29*</small></small>
- 🚀 [NEW] Support writing environment variables from Python scripts.
- 🚀 [NEW] Environment variables can be created from the context menu after selecting text.
- 🚀 [NEW] Support opening all APIs in the collection at one time.
- 🚀 [NEW] Increase the available number of API collections for Community Edition users from 2 to 3.
- 🚀 [NEW] Increase the available number of Environments for Community Edition users from 2 to 3.
- 💪 [OPT] Improved page effects for new users when opening the app for the first time.
- 💪 [OPT] The focus is still maintained after pressing the Enter key to send an API request.
- 💪 [OPT] Some context menu options will be displayed as unavailable when the selected data is invalid.
- 💪 [OPT] Some input fields support the Enter key to complete input.
- 🐞 [FIX] A bug where duplicate encoding of request parameters in code generation.
- 🐞 [FIX] Corrected the logic for saving form requests in API testing.
- 🐞 [FIX] A bug where there was an exception in parsing text for API request parameters.
- 🐞 [FIX] A bug where parameters and headers starting with `_` were not highlighted.
- 🐞 [FIX] A bug where environment name is empty.
- 🐞 [FIX] A bug where illegal values in Set-Cookie were not displayed correctly.
- 🐞 [FIX] The bug of incorrect HEX export data.
- 🐞 [FIX] A bug where input content was lost in certain scenarios in the text editor.

## v2.9.0 <small><small>*2024-03-22*</small></small>
- 🚀 [NEW] Introduce environment variables.
- 🚀 [NEW] Now can rename the API request.
- 💪 [OPT] Generate Python-Requests code using query parameters instead of long url.
- 💪 [OPT] API testing supports pressing the Enter key to send directly.
- 💪 [OPT] The QR code of the certificate link is changed from click display to mouse pointer hover display.
- 🐞 [FIX] The bug that API can not use Python script to process form data.
- 🐞 [FIX] The bug that API space will encodes to `%20` rather than `+`.
- 🐞 [FIX] The bug that it will prompt to save when closing the API test tab.
- 🐞 [FIX] The bug that correctly to handle `--data-raw` when importing a cURL.
- 🐞 [FIX] The bug that the python environment cannot take effect.
- 🐞 [FIX] The bug that app menu group position is incorrect after the window is zoomed.

## v2.8.2 <small><small>*2024-03-06*</small></small>
- 💪 [OPT] Coloring request methods.
- 💪 [OPT] File drag and drop will be disabled when a dialog is showing.
- 🐞 [FIX] The bug of importing ApiFox collection failed in some cases.
- 🐞 [FIX] The bug where the response raw message is incorrect.
- 🐞 [FIX] Incorrect highlighting of query parameters and cookies.
- 🐞 [FIX] The bug where `startedDateTime` of the exported HAR format is incorrect.
- 🐞 [FIX] The bug that the request path is incorrect in python scripts.
- 🐞 [FIX] The bug that `Active Code Page` will cause the python environment detection to fail.

## v2.8.0 <small><small>*2024-02-29*</small></small>
- 🚀 [NEW] Available API tabs of community version are increased from 2 to 4.
- 🚀 [NEW] Adds three new tabs, Cookies, Set-Cookies and Comment.
- 🚀 [NEW] Now you can comment a traffic record.
- 🚀 [NEW] Custom request and response tabs.
- 💪 [OPT] Supports recovery of the damaged `SharedPreferences` file.
- 🐞 [FIX] The cookie automatic update mechanism causes a bug that requires saving when closing a API Tab.
- 🐞 [FIX] The bug of incorrect parsing of the '--data-urlencode' parameter when importing a cURL.
- 🐞 [FIX] The bug in which the content displayed in the Tab title is truncated.
- 🐞 [FIX] The bug where `wss` in HAR file is recognized as `ws`.
- 🐞 [FIX] The bug that the application cannot exit normally when right-clicking on the taskbar to close the window.
- 🐞 [FIX] A bug where an error dialog appears when the os is shutdown and the system network proxy cannot be automatically reset.

## v2.7.1 <small><small>*2024-02-22*</small></small>
- 💪 [OPT] HEX will be displayed first when the image data decoding fails.
- 🐞 [FIX] The bug of incorrect encoding and decoding of URL query parameters.
- 🐞 [FIX] The bug in parsing HAR files does not correctly handle the MIME type.
- 🐞 [FIX] The bug of secondary proxy account authentication not works.
- 🐞 [FIX] The bug that data displayed after modifying `Content-Type` through script does not take effect.
- 🐞 [FIX] A bug where the white window flashes obviously when the app starts.
- 🐞 [FIX] The bug that the sub window may be reset to the default size when maximized.

## v2.7.0 <small><small>*2024-02-20*</small></small>
- 🚀 [NEW] Supports to adjust app display scaling.
- 🚀 [NEW] Will restore the previous window position and size when restarting.
- 🚀 [NEW] Supports deleting API request history URLs.
- 💪 [OPT] No longer automatically checked the rewrite-replace checkbox.
- 🐞 [FIX] The bug that the unmodified API will prompt to save when closing.
- 🐞 [FIX] The bug that closing other tabs will close all tabs.
- 🐞 [FIX] The bug of incorrect encoding of `space` and `=` in request query parameters.
- 🐞 [FIX] The bug that the original response data may not be brought in when creating a rewrite-replacement response rule.
- 🐞 [FIX] The bug that URL rules may not match in rewrite, breakpoint and scripting rules.
- 🐞 [FIX] The bug that the encoding of API scripting console is not utf-8.

## v2.6.3 <small><small>*2024-02-07*</small></small>
- 💪 [OPT] Runtime error of API testing scripts will output to the console.
- 💪 [OPT] The auto-complete list of text input field supports up and down key selection.
- 🐞 [FIX] Some prompts of Python scripting api are incorrect.
- 🐞 [FIX] The bug that response body is not automatically decoded when scripting is enabled.

## v2.6.2 <small><small>*2024-02-04*</small></small>
- 🐞 [FIX] A bug where some webSocket requests are not recognized.
- 🐞 [FIX] A bug in the API request script caused the request path to be incorrectly encoded.

## v2.6.1 <small><small>*2024-01-31*</small></small>
- 🚀 [NEW] Code editor supports code auto-completion.
- 🚀 [NEW] Console tab for traffic details.
- 🚀 [NEW] Console tab for API testing response.
- 🚀 [NEW] Supports win7 OS.
- 🐞 [FIX] The bug that text syntax highlighting may be incorrect.
- 🐞 [FIX] The bug that missing `/` at the end of URL.
- 🐞 [FIX] The bug that `HexViewer` will get focus by default.
- 🐞 [FIX] The bug that IP was displayed rather than host.

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
- 💪 [OPT] Remove the application ID option from the default column of the traffic list.
- 💪 [OPT] Tabs on the home page can be directly dragged and sorted without long pressing.
- 🐞 [FIX] The bug of duplicate cookie values in the code snippet.
- 🐞 [FIX] The bug that unable to decode deflate data.
- 🐞 [FIX] A bug that may trigger content selection when scrolling the editor.
- 🐞 [FIX] The bug that unable to copy cURL of the WebSocket request.
- 🐞 [FIX] The bug of failing to handle WebSocket compression extension correctly.
- 🐞 [FIX] The bug that cannot create form request or copy cURL from traffic list.
- 🐞 [FIX] A bug where the tab title on the home page may be displayed incompletely.
- 🐞 [FIX] The bug that cannot resize traffic list column width.
- 🐞 [FIX] The bug that the application window cannot be restored by tapping the tray icon.

## v2.4.0 <small><small>*2024-01-12*</small></small>
- 🚀 [NEW] Introduce a new secondary proxy feature.
- 🚀 [NEW] Supports drag sorting of working tabs.
- 🚀 [NEW] You can select or unselect a search condition for traffic list.
- 💪 [OPT] The time threshold for triggering drag is reduced from 500ms to 150ms.
- 💪 [OPT] Supports mouse wheel to control horizontal layout scrolling.
- 🐞 [FIX] The bug that the generated cURL does not merge cookies.
- 🐞 [FIX] The bug that the `Referer` header cannot be sent in API requests.
- 🐞 [FIX] The bug of missing `application/x-www-form-urlencoded` header in code snippet.
- 🐞 [FIX] A bug that may crash when exporting P12 format certificate.
- 🐞 [FIX] A bug that may jump abnormally when selecting a debug list.

## v2.3.2 <small><small>*2024-01-08*</small></small>
- 💪 [OPT] Adjustment of some UI details.
- 🐞 [FIX] The bug that the raw message in the traffic details cannot be code highlighted.
- 🐞 [FIX] The bug that JSON array type throws an error int code snippet.
- 🐞 [FIX] The bug that the root certificate installed to the current user cannot be recognized.

## v2.3.0 <small><small>*2024-01-05*</small></small>
- 🚀 [NEW] Upgrade the Flutter framework to the latest version 3.16.5.
- 🚀 [NEW] Use Material Design 3 styles.
- 🚀 [NEW] 15 code syntax highlighting color options.
- 🚀 [NEW] Add the application ID column for traffic list.
- 🚀 [NEW] Context menu for traffic overview URL.
- 🚀 [NEW] Introduce secondary proxy for SOCKS and VPN modes.
- 🚀 [NEW] Remote app can control the recording status of the host app.
- 🚀 [NEW] Allow auto-dismiss the QR code pop-up dialog when the remote device connected.
- 💪 [OPT] Adjust the proxy port detection logic and automatically change the port number when a conflict is detected.
- 💪 [OPT] URL syntax highlighting supports universal schemes.
- 💪 [OPT] Apply URL syntax highlighting for QR code input text.
- 💪 [OPT] The traffic record in collaborative mode will display domain name instead of IP address.
- 🐞 [FIX] The bug that the urlencode request body may be lost when parsing HAR files.
- 🐞 [FIX] A failure with non-standard HAR connection fields.
- 🐞 [FIX] The bug that the uppercase encoding value such as GZIP cannot be recognized.

## v2.2.1 <small><small>*2023-12-29*</small></small>
- 🐞 [FIX] The bug that the status of system proxy indicator icon is not correct.

## v2.2.0 <small><small>*2023-12-28*</small></small>
- 🚀 [NEW] API testing supports splitting merged cookies into multiple ones.
- 🚀 [NEW] API testing supports opening additional editors to edit cookies.
- 🚀 [NEW] Remember and restore previous system proxy configuration when exiting the app.
- 🐞 [FIX] The bug where some items in the traffic list were sorted incorrectly.
- 🐞 [FIX] The bug that the application cannot start in some cases.

## v2.1.1 <small><small>*2023-12-25*</small></small>
- 🚀 [NEW] Allow root certificate regeneration.
- 🚀 [NEW] You can pin application filter and domain filter now.
- 🚀 [NEW] You can configure interceptors such as rewriting in auto-highlighting.
- 🚀 [NEW] A shortcut key `Alt + Control + ↑/↓` for traffic list, switch browsing history before and after.
- 🚀 [NEW] A shortcut key `Shift + Control + I` for all list, invert the current selection.
- 💪 [OPT] API testing `reqableId` supports displaying in two lines.
- 💪 [OPT] API testing will automatically fill key-value entries when switching from text.
- 💪 [OPT] The domain filter list is expanded by default.
- 💪 [OPT] Slightly increase the size of the diff tool window.
- 💪 [OPT] The application uses MiSans font by default.
- 🐞 [FIX] The bug that it is unable to install root certificate.
- 🐞 [FIX] The bug of abnormal display of collaborative QR code when there is no local IP.
- 🐞 [FIX] A bug that the mirror icon will display incorrectly in some cases.
- 🐞 [FIX] A debug that interceptor icon color is not highlighted.
- 🐞 [FIX] The bug where the system shows that the application is tracking the location.

## v2.0.0 <small><small>*2023-12-15*</small></small>
- 🚀 [NEW] Supports collaboration with Reqable mobile apps.
- 🚀 [NEW] Supports importing and exporting pkcs12 root certificate file.
- 🚀 [NEW] Supports viewing the currently used root certificate file.
- 🚀 [NEW] Diff tool supports header name lowercase comparation.
- 🚀 [NEW] Adds a search icon for Code Editor and Hex Viewer.
- 💪 [OPT] Supports some non-standard proxy protocol messages.
- 💪 [OPT] Redo traffic overview UI/UX.
- 💪 [OPT] Redo Websocket UI/UX.
- 💪 [OPT] Redo styling of settings window option switches.
- 💪 [OPT] More `Certificate` menu bar options.
- 💪 [OPT] Code Editor removes unnecessary padding areas.
- 💪 [OPT] Reduces drag and scroll speed of Code Editor and HexViewer.
- 💪 [OPT] Code editor will not lose the currently selection when dragging to expand the selection area.
- 💪 [OPT] Android certificate setup adds network security configuration guides.
- 💪 [OPT] Android certificate setup adds certificate file permission tips.
- 💪 [OPT] Diff tool enables sorting headers by default.
- 💪 [OPT] New sub windows no longer flicker on startup.
- 💪 [OPT] Copying API cURL will close the pop-up window automatically.
- 💪 [OPT] Tips will be displayed in the bottom bar if the current API testing has a proxy setting.
- 💪 [OPT] Max redirection button will automatically wrap when there is insufficient display space.
- 💪 [OPT] You can click the cookie list item to edit it.
- 💪 [OPT] In table mode, long press the cell will copy the key or value.
- 💪 [OPT] License registration automatically fills in the last email address and license code.
- 💪 [OPT] Try using SSL SNI as the host of the URL instead of the IP.
- 💪 [OPT] Adds some prompts in SSL bypass editor.
- 💪 [OPT] Double-clicking outside the traffic list will automatically close the details panel.
- 💪 [OPT] Supports `Control + L` shortcut key to quickly locate the currently selected traffic item.
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
- 💪 [OPT] Reduce the number of traffic capture cache files.
- 🐞 [Fix] The issue of flashing when opening a new window.
- 🐞 [Fix] The bug of missing query parameters in rewrite redirection.

## v1.6.1 <small><small>*2023-10-09*</small></small>
- 💪 [OPT] Traffic list application filtering option displays remote device IP.
- 💪 [OPT] The API editor URL input box will display the historical URL and you can choose to enter it.
- 💪 [OPT] URL rule wildcard matching.
- 💪 [OPT] When a lower version application opens a higher version database, it will reset the database instead of reporting an error.
- 💪 [OPT] The raw message displays the body encoding type.
- 🐞 [Fix] The API testing tab that is no save prompt after the application is restarted.
- 🐞 [Fix] The bug that API testing may prompt saving again when a saved API is closed.
- 🐞 [Fix] The bug that requests in socks proxy mode cannot trigger interceptors such as rewriting, breakpoints, and scripts.
- 🐞 [Fix] A bug where quotes were not escaped during code generation..
- 🐞 [Fix] A bug where some cache files failed to be automatically cleared in incognito mode.

## v1.6.0 <small><small>*2023-09-27*</small></small>
- 🚀 [NEW] Supports detaching a new window to view traffic data details.
- 🚀 [NEW] The middle mouse button can close the Tab.
- 🚀 [NEW] The middle mouse button can close the sub-window.
- 💪 [OPT] Better performance and memory usage.
- 🐞 [Fix] The bug that the script editor cannot open `Visual Studio Code`.

## v1.5.1 <small><small>*2023-09-25*</small></small>
- 💪 [OPT] The count of free tabs for history and file viewing has been increased from 1 to 2.
- 💪 [OPT] The pop-up dialog supports the `Enter` shortcut key to trigger positive button.
- 💪 [OPT] When saving API collection, the last save path will be used by default.
- 💪 [OPT] When saving API collection, the host will be used as the name by default.
- 💪 [OPT] Automatically change the port when MITM proxy port conflict is detected.
- 💪 [OPT] Python scripts can be directly opened with `Visual Studio Code` for editing.
- 💪 [OPT] Automatically merge the Cookie value of the request header when generating code snippet.
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
- 🐞 [Fix] Fixed the bug that the system network proxy cannot be automatically disabled after restarting the system and shutting down.
- 🐞 [Fix] The bug that some devices cannot close the window to enter the background.

## v1.5.0 <small><small>*2023-09-21*</small></small>
- 🚀 [NEW] Add HTTP request and response diff tool.
- 🚀 [NEW] Add `JWT` decoder in the toolbox.
- 🚀 [NEW] API JSON data editing supports one-click compression.
- 💪 [OPT] Supports `Control + W` shortcut key to close sub windows.
- 💪 [OPT] Use name instead of timestamp when exporting traffic history.
- 💪 [OPT] Raw packet syntax supports JSON and XML highlighting.
- 🐞 [Fix] In the API testing, the cURL import dialog will not automatically pop up if the command containing `WIDTH NO-BREAK SPACE`.
- 🐞 [Fix] The bug of uploading crash and statistic configuration not taking effect.
- 🐞 [Fix] `Space` and `*` in the `urlencode` of the Python script may cause some servers to fail to correctly obtain the request path.
- 🐞 [Fix] The bug that the main window initial opening position is incorrect.
- 🐞 [Fix] A bug causing abnormal size when the window moves between screens with different scales.
- 🐞 [Fix] A bug where some application information cannot be dumped.

## v1.4.1 <small><small>*2023-09-18*</small></small>
- 💪 [OPT] Traffic list supports drag selection.
- 💪 [OPT] Traffic list requests and responses are saved with default file names.
- 🐞 [Fix] The bug that some JavaScript content searches have no results.
- 🐞 [Fix] The bug that sending a request when the URL contains `WIDTH NO-BREAK SPACE` characters will cause the application to crash.
- 🐞 [Fix] The bug that cURL export cannot parse commands containing `WIDTH NO-BREAK SPACE` characters.
- 🐞 [Fix] The bug that the HTTP raw data copy content does not correctly handle the CRLF.
- 🐞 [Fix] The bug of copying from a rewrite modification rule.
- 🐞 [Fix] The bug that localhost requests are unresponsive when enabled `Loopback`.
- 🐞 [Fix] There is a bug that some devices cannot obtain the system proxy configuration.

## v1.4.0 <small><small>*2023-09-14*</small></small>
- 🚀 [NEW] `Code Snippet` supports cURL and Guzzle for PHP language.
- 🚀 [NEW] Add `Certificate` application menu bar.
- 🚀 [NEW] Add `Raw` display for request details.
- 🚀 [NEW] Add `Automatic Debugging` switch in app settings.
- 🚀 [NEW] Support reviewing Charles Session files.
- 💪 [OPT] A prompt pop-up dialog will be displayed when Reqable exits.
- 💪 [OPT] A prompt will be displayed after dragging unsupported files to the Reqable main window and releasing them.
- 💪 [OPT] The session content area displays information about file or history opening failure.
- 💪 [OPT] Opening HAR files no longer filters out `CONNECT` requests.
- 🐞 [Fix] Reverse proxy certificate trust issue.
- 🐞 [Fix] A bug where SSL handshake failure are not displayed.
- 🐞 [Fix] A bug in which operations such as deleting, clearing, and editing bookmarks lead to incorrect bookmark selection status.
- 🐞 [Fix] A bug in importing cURL that causes the URL parsing to fail due to the `--location` parameter.
- 🐞 [Fix] The bug that the request cannot be sent due to malformed `Content-Type`.
- 🐞 [Fix] The bug of incorrect application window position and size on certain resolution devices.
- 🐞 [Fix] SOCKS proxy causing MySql database to be unable to connect.

## v1.3.1 <small><small>*2023-09-11*</small></small>
- 🚀 [NEW] Support `Reverse Proxy` now.
- 🚀 [NEW] Add `Proxy` application menu group bar.
- 🚀 [NEW] When you paste the cURL into the API testing URL input field, the import cURL dialog will automatically pop up.
- 💪 [OPT] Cancel the certificate status detection polling mechanism.
- 💪 [OPT] API query parameters created from the traffic list are automatically URL decoded.
- 💪 [OPT] The URL displayed in the traffic list removes the display of the default root path `/`.
- 💪 [OPT] A new `Help` button is added to the secondary proxy configuration page.
- 🐞 [Fix] A bug where expanding the sidebar may cause the gateway, mirror, script, rewrite, and breakpoint to not work.
- 🐞 [Fix] A bug where clicking the start button might cause the content layout size to jump back to its previous size.
- 🐞 [Fix] The bug that may cause the CONNECT proxy request status to be displayed as interrupted after the gateway successfully silences the request.
- 🐞 [Fix] The bug of incorrect Toast style used in some error prompts.
- 🐞 [Fix] The bug of incomplete display of changelogs in the version update window.

## v1.3.0 <small><small>*2023-09-05*</small></small>
- 🚀 [NEW] Display the application where the traffic from.
- 🚀 [NEW] Support filtering traffic according to application in the explorer.
- 💪 [OPT] When the traffic list is at the bottom, it will automatically scroll if new data appears.
- 💪 [OPT] The read items in the structure tree are grayed out.
- 💪 [OPT] Added type icon display in the structure tree.
- 💪 [OPT] Importing cURL will automatically recognize the JSON/XML type.
- 💪 [OPT] Explorer UI details adjustment.
- 🐞 [Fix] The bug that the sub-window icon in the taskbar does not display the logo.
- 🐞 [Fix] The bug that import cURL does not support the --insecure option.
- 🐞 [Fix] The bug that import cURL escape character is lost.
- 🐞 [Fix] the bug that cURL syntax highlighting causes the content to be incompletely displayed.

## v1.2.5 <small><small>*2023-09-01*</small></small>
- 🐞 [Fix] Fixed the bug that scripting broken the connection.

## v1.2.4 <small><small>*2023-09-01*</small></small>
- 🐞 [Fix] Fixed the bug that an error was reported when opening the app after updating to version 1.2.3.
- 🐞 [Fix] Fixed the bug that the name of the opened tab could not be updated synchronously after modifying the name of the capture history.

## v1.2.3 <small><small>*2023-08-31*</small></small>
- 🚀 [NEW] The traffic list read items are grayed out.
- 🚀 [NEW] The traffic history supports configuring the cache duration, which is 7 days by default.
- 🚀 [NEW] Traffic history supports renaming.
- 🚀 [NEW] Traffic history supports adding/removing stars.
- 🚀 [NEW] Query parameter list viewing supports text mode.
- 💪 [OPT] The way to obtain the system network proxy status is changed from Shell command to API.
- 💪 [OPT] The traffic list removes gray highlighting and adds teal highlighting.
- 💪 [OPT] Use the resident daemon process to get the CA root certificate installation status.

## v1.2.1 <small><small>*2023-08-28*</small></small>
- 🚀 [NEW] SSL bypass supports switch and silent mode.
- 🚀 [NEW] Supports adding SSL bypass from traffic list.
- 💪 [OPT] Automatically changing context menu text color when hovering.
- 💪 [OPT] The right click of the traffic list supports batch copying of URLs.
- 🐞 [Fix] An exception occurs when generating python code when the root node of JSON is a list.
- 🐞 [Fix] The bug that localhost requests will not be displayed when the API test is followed by debugging.
- 🐞 [Fix] The bug that the SSL Bypass requests will not be displayed when the API test is followed by debugging.
- 🐞 [Fix] The bug that the `Proxy-Connection` header was not removed when sending to remote server.

## v1.2.0 <small><small>*2023-08-24*</small></small>
- 🚀 [NEW] Apps are signed with EV certificates.
- 🚀 [NEW] Added code snippet for API and traffic.
- 🚀 [NEW] Added `Clear Cache` and `Reset App` in settings.
- 🚀 [NEW] Urlencode supports text editing mode.
- 🚀 [NEW] Urlencode supports importing and copying concatenated strings.
- 💪 [OPT] Change version upgrade pop-up window.
- 💪 [OPT] The UX of expanding the app menu bar.
- 💪 [OPT] Adding quotes to URL values in generated cURL commands.
- 🐞 [Fix] The bug that the number of checks displayed in the domain filter of the traffic list is wrong.
- 🐞 [Fix] The bug that the request or response cannot continue to execute after the breakpoint window is closed.
- 🐞 [Fix] Possible duplicate `Content-Type` header bug in API created from traffic list.
- 🐞 [Fix] The bug that the text display error in the API query parameter text editing mode.

## v1.1.8 <small><small>*2023-08-10*</small></small>
- 🚀 [NEW] Support API session global settings.
- 💪 [OPT] Important performance optimization.
- 💪 [OPT] The storage limit of the database has been increased from 1G to 10G.
- 💪 [OPT] The traffic history data is stored in compression.
- 💪 [OPT] Raw body data is automatically prettified.
- 💪 [OPT] Exiting the program no longer automatically closes the system proxy if Reqable proxy is unset.
- 🐞 [Fix] The bug that the request header in the imported API collection is incomplete.
- 🐞 [Fix] The bug that the API repeatedly adds the Cookie header.
- 🐞 [Fix] The bug that auto-cookie settings is not working.
- 🐞 [Fix] The bug that API session shortcut keys are not working.

## v1.1.7 <small><small>*2023-08-07*</small></small>
- 🚀 [NEW] Support export and import Reqable api collections.
- 🚀 [NEW] API editor added `Follow Debug` shortcut icon.
- 🚀 [NEW] The traffic list supports `client address` search terms.
- 🚀 [NEW] Added a button to clear the results in the URL codec tool.
- 💪 [OPT] Added error message display in the URL codec tool.
- 💪 [OPT] Cleaning strategy of history cache files.
- 💪 [OPT] API collection naming and renaming verification.
- 💪 [OPT] Some input boxes will change the border color after getting the focus.
- 💪 [OPT] Configure web proxy no longer uses `powershell` to execute commands.
- 🐞 [Fix] The bug that the remote device sll bypass does not take effect.
- 🐞 [Fix] A bug that failed to read some traffic history.
- 🐞 [Fix] Failed to clean up the websocket cache file after deleting traffic history.
- 🐞 [Fix] A bug where input auto-completes were lost in traffic search items.

## v1.1.6 <small><small>*2023-08-03*</small></small>
- 🚀 [NEW] Refactor capture multi-session UX.
- 🚀 [NEW] Supports importing API collections of Postman, Hoppscotch, ApiPost and Apifox.
- 🚀 [NEW] Support for merging capture records into other session tabs.
- 💪 [OPT] Improve application startup speed.
- 💪 [OPT] Automatically clean up expired capture cache files.
- 💪 [OPT] Bookmark filtering and domain name filtering conditions are changed from `and` to `or`.
- 🐞 [Fix] The bug that the SSL traffic of the remote device is not decrypted when the computer does not have a certificate installed.

## v1.1.5 <small><small>*2023-07-31*</small></small>
- 🚀 [NEW] Support SSL bypass configuration (right-click the shield icon).
- 💪 [OPT] MITM proxy is skipped if the certificate is not installed successfully.
- 💪 [OPT] Remove the limit of 9999 repeats.
- 💪 [OPT] Server address will also be displayed in the traffic list after the proxy connection fails.
- 💪 [OPT] License window adds a display of the reason for restriction.
- 💪 [OPT] Traffic list supports Home/End/PageUp/PageDown shortcut keys.
- 💪 [OPT] The editor supports Home/End shortcut keys.
- 💪 [OPT] The method of obtaining the unique ID of windows device.
- 🐞 [Fix] Wildcard matching algorithm may enter an infinite loop.
- 🐞 [Fix] cURL format for copying Multipart requests in the traffic list is incorrect.
