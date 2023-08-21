# Windows

## v1.1.8 <small><small>*2023-08-10*</small></small>
- 🚀【New】Support API session global settings.
- 💪【Opt】Important performance optimization.
- 💪【Opt】The storage limit of the database has been increased from 1G to 10G.
- 💪【Opt】The traffic history data is stored in compression.
- 💪【Opt】Raw body data is automatically prettified.
- 💪【Opt】Exiting the program no longer automatically closes the system proxy if Reqable proxy is unset.
- 🐞【Fix】The bug that the request header in the imported API collection is incomplete.
- 🐞【Fix】The bug that the API repeatedly adds the Cookie header.
- 🐞【Fix】The bug that auto-cookie settings is not working.
- 🐞【Fix】The bug that API session shortcut keys are not working.

## v1.1.7 <small><small>*2023-08-07*</small></small>
- 🚀【New】Support export and import Reqable api collections.
- 🚀【New】API editor added `Follow Debug` shortcut icon.
- 🚀【New】The traffic list supports `client address` search terms.
- 🚀【New】Added a button to clear the results in the URL codec tool.
- 💪【Opt】Added error message display in the URL codec tool.
- 💪【Opt】Cleaning strategy of history cache files.
- 💪【Opt】API collection naming and renaming verification.
- 💪【Opt】Some input boxes will change the border color after getting the focus.
- 🐞【Fix】The bug that the remote device sll bypass does not take effect.
- 🐞【Fix】A bug that failed to read some traffic history.
- 🐞【Fix】Failed to clean up the websocket cache file after deleting traffic history.
- 🐞【Fix】A bug where input auto-completes were lost in traffic search items.
- 💪【Opt】Configure web proxy no longer uses `powershell` to execute commands.

## v1.1.6 <small><small>*2023-08-03*</small></small>
- 🚀【New】Refactor capture multi-session UX.
- 🚀【New】Supports importing API collections of Postman, Hoppscotch, ApiPost and Apifox.
- 🚀【New】Support for merging capture records into other session tabs.
- 💪【Opt】Improve application startup speed.
- 💪【Opt】Automatically clean up expired capture cache files.
- 💪【Opt】Bookmark filtering and domain name filtering conditions are changed from `and` to `or`.
- 🐞【Fix】The bug that the SSL traffic of the remote device is not decrypted when the computer does not have a certificate installed.

## v1.1.5 <small><small>*2023-07-31*</small></small>
- 🚀【New】Support SSL bypass configuration (right-click the shield icon).
- 💪【Opt】MITM proxy is skipped if the certificate is not installed successfully.
- 💪【Opt】Remove the limit of 9999 repeats.
- 💪【Opt】Server address will also be displayed in the traffic list after the proxy connection fails.
- 💪【Opt】License window adds a display of the reason for restriction.
- 💪【Opt】Traffic list supports Home/End/PageUp/PageDown shortcut keys.
- 💪【Opt】The editor supports Home/End shortcut keys.
- 🐞【Fix】Wildcard matching algorithm may enter an infinite loop.
- 🐞【Fix】cURL format for copying Multipart requests in the traffic list is incorrect.
- 💪【Opt】The method of obtaining the unique ID of windows device.
