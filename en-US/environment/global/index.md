---
title: Global Environment
description: Familiar with the concept and basic usage of global environment variables.
sidebar_position: 0
---

# Global Environment

In Reqable, a global environment variable is a special type of environment variable whose value is available throughout the Reqable application. Global environment variables are often used to store data values that need to be shared across multiple requests or environments.

Using global environment variables helps users share data across different requests, collections, or environments without having to define the same values repeatedly. This increases productivity and ensures data consistency and accuracy.

To use global environment variables in Reqable, you first need to define these variables. By default, Reqable has created a global environment for everyone. You can click the `Global` environment in the `Environment` panel to define and edit global environment variables. Once variables are defined, they can be used in any request, script, or elsewhere without having to repeatedly enter values.

When using global environment variables in a request, just use double angle brackets (such as `<<variable_name>>`) where you need to reference the variable. Reqable will automatically replace these references with the variable value when sending the request.

:::caution
Global environment variables have a lower priority than other environment variables. If a variable with the same name exists in other environments, the variable specified in the other environment will be used first.
:::

Global variables are divided into two types, one is [Custom Variable](#custom), and the other is [Built-in Variable](#dynamic)。

## Custom Variable {#custom}

Custom variables are defined by users. You can click the `Global` item in the environment panel to add, modify, delete and activate theme.

:::info
If you do not want the variable value to be displayed in plain text, you can click the eye icon (which automatically appears when the mouse is hovering at the end of the input box) to hide it.
:::

## Built-in Variable {#dynamic}

In Reqable, in addition to user custom variables, there are also some built-in variables, which start with a dollar symbol ($). There are currently a total of the following built-in variables.

- `$date` Current date and time (yyyy-MM-dd) in the local time zone.
- `$datetime` Current date and time (yyyy-MM-dd HH:mm:ss) in the local time zone.
- `$guid` A v4 style guid.
- `$randomBoolean` A random boolean value (true/false).
- `$randomColor` A random color name.
- `$randomCurrencyCode` A random 3-letter currency code (ISO-4217).
- `$randomCurrencyName` A random currency name.
- `$randomEmail` A random email address.
- `$randomHttpUrl` A random HTTP URL.
- `$randomHttpsUrl` A random HTTP URL.
- `$randomImageUrl` A random image URL.
- `$randomInt1` A random integer between 0 and 10.
- `$randomInt2` A random integer between 0 and 100.
- `$randomInt3` A random integer between 0 and 1000.
- `$randomInt4` A random integer between 0 and 10000.
- `$randomIPv4` A random IPv4 address.
- `$randomIPv6` A random IPv6 address.
- `$randomJustTime` A random time (HH:mm).
- `$randomLetterLower` A random lower case letter.
- `$randomLetterUpper` A random upper case letter.
- `$randomLatitude` A random latitude coordinate.
- `$randomLongitude` A random longitude coordinate.
- `$randomMACAddress` A random MAC address.
- `$randomMonth` A random month.
- `$randomPassword` A random 12-character password.
- `$randomPhoneNumberCN` A random 11-digit chinese mainland phone number.
- `$randomPhoneNumberUS` A random 10-digit us phone number.
- `$randomUsername` A random username.
- `$randomWeekday` A random weekday.
- `$timestamp` The current timestamp in milliseconds.
- `$timestampInSeconds` The current timestamp in seconds.
- `$timestampISO` The current ISO timestamp at zero UTC.

These built-in variables can dynamically generate data in requests, and users can directly reference these built-in variables in Reqable without prior definition or setting.