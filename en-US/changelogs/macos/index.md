# Macos

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
- 🐞[Fix] The bug that the `Webkit Networking` related request icon displays incorrectly.

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
- 🐞 [Fix] A bug in which application information cannot be obtained under certain circumstances.

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
