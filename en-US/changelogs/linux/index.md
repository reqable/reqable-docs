# Linux

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
