# Windows

## v1.6.0 <small><small>*2023-09-27*</small></small>
- 🚀 [New] Supports detaching a new window to view traffic data details.
- 🚀 [New] The middle mouse button can close the Tab.
- 🚀 [New] The middle mouse button can close the sub-window.
- 💪 [Opt] Better performance and memory usage.
- 🐞 [Fix] The bug that the script editor cannot open `Visual Studio Code`.

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
- 🐞 [Fix] Fixed the bug that the system network proxy cannot be automatically disabled after restarting the system and shutting down.
- 🐞 [Fix] The bug that some devices cannot close the window to enter the background.

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
- 🐞 [Fix] The bug that the main window initial opening position is incorrect.
- 🐞 [Fix] A bug causing abnormal size when the window moves between screens with different scales.
- 🐞 [Fix] A bug where some application information cannot be dumped.

## v1.4.1 <small><small>*2023-09-18*</small></small>
- 💪 [Opt] Traffic list supports drag selection.
- 💪 [Opt] Traffic list requests and responses are saved with default file names.
- 🐞 [Fix] The bug that some JavaScript content searches have no results.
- 🐞 [Fix] The bug that sending a request when the URL contains `WIDTH NO-BREAK SPACE` characters will cause the application to crash.
- 🐞 [Fix] The bug that cURL export cannot parse commands containing `WIDTH NO-BREAK SPACE` characters.
- 🐞 [Fix] The bug that the HTTP raw data copy content does not correctly handle the CRLF.
- 🐞 [Fix] The bug of copying from a rewrite modification rule.
- 🐞 [Fix] The bug that localhost requests are unresponsive when enabled `Loopback`.
- 🐞 [Fix] There is a bug that some devices cannot obtain the system proxy configuration.

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
- 💪 [Opt] The way to obtain the system network proxy status is changed from Shell command to API.
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

## v1.2.0 <small><small>*2023-08-24*</small></small>
- 🚀 [New] Apps are signed with EV certificates.
- 💪 [Opt] Change version upgrade pop-up window.
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
- 💪 [Opt] Configure web proxy no longer uses `powershell` to execute commands.

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
- 💪 [Opt] The method of obtaining the unique ID of windows device.
