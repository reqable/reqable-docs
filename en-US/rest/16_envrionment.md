# Environment

You can use angle brackets (such as `<<variable_name>>`) to reference the corresponding environment variables in the request. Reqable will automatically replace these references with the actual variable values when sending the request. Users can use environment variables in the URL, Query Parameters, Headers, Body, and Authorization.

After entering a angle bracket `<` in the input box, the variable prompt will automatically appear, and the user can view the currently matching environment variables. When the mouse pointer hovers over a variable, the variable information will be automatically prompted.

![](arts/envrionment_01.png)

Reqable will automatically replace these references with actual variable values when sending the request.

![](arts/envrionment_02.png)

For more information, please read the document: [Environment](../environment)