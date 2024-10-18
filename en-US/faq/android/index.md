---
title: Android
description: Android FAQs and solutions.
sidebar_position: 4
---

# Android FAQs

:::info
Please update Reqable to the latest version before troubleshooting.
:::

### 1. Certificate Issue

- [Installation](../../getting-started/installation)
- [Troubleshoot](../ssl)

### 2. Reqable log files

Open the side menu, long press the top logo, and select the log file to view.

### 3. Unable to capture application traffic

Please make sure the following actions have been processed.

- The capture button has been turned on.
- The `Record Mode` has been set to VPN instead of proxy.
- The `Enhanced Mode` has been enabled.
- All filtering and search conditions have been turned off.
- All target applications have been removed.

After Reqable starts the capture, open the mobile browser and visit www.google.com.

:::caution
The browser may prompt an unsecured connection. In this case, it is a certificate issue. Please read the following content.
- [Chrome](#chrome)
- [Firefox](#firefox)
:::

Case 1: Google cannot be accessed, and no traffic (including CONNECT requests) can be seen.

It may be that the Reqable proxy server port is broken (for example, occupied by other program processes). You can try to change the port and try again.

If your browser still cannot access Google after changing the port, please report it to us on [Github](https://github.com/reqable/reqable-app/issues).

Case 2: Google is accessible, but no traffic (including CONNECT requests) can be seen.

Check again whether the `Record Mode` is VPN. If this situation still occurs in VPN mode, please report it to us on [Github](https://github.com/reqable/reqable-app/issues).

Case 3: Google is accessible, and traffic (including CONNECT requests) can also be seen.

This indicates that the application is prohibited from working when VPN is actived. Please contact the application owner for a solution.

### 4. The mobile device cannot connect to PC

- Check if the mobile and PC are in the same LAN.
- Check if the mobile and PC are in the same LAN segment. Some LANs prohibit cross-segment communication when networking.
- Try connecting the PC to the mobile's hotspot, and then scan the QR code on the mobile to connect to the PC.
- Check if the system firewall has disabled the inbound and outbound traffic of the Reqable proxy port number.

### 5. Unable to capture application traffic in collaborative mode

You can follow the steps below to troubleshoot:

- Switch to standalone mode (Select the `Traffic` tab in the side menu), and troubleshoot according to 3 above.
- Reqable mobile app disables or enables `Enhanced mode` and try again.
- Change the port of Reqable on PC, and then scan the code to connect again.

### 6. Chrome prompts unsafe website{#chrome}

Chrome's trust policy for certificates is constantly changing. For example, the latest version of Chrome will ignore the self-signed CA certificate installed in the Android system certificate directory. If you need to capture the Chrome traffic, please note:

- If you using a higher version of Chrome, you need to install the CA certificate in the user certificate directory.
- If you using a lower version of Chrome, you need to install the CA certificate in the system certificate directory.

If you are not sure which method to choose, you can try them two.

### 7. Firefox prompts unsafe website{#firefox}

Firefox uses a built-in CA store. Regardless of whether the Reqable CA certificate is installed in the system directory or the user directory, it will not be trusted, and the user needs to perform additional actions.

- Firefox settings -> About Firefox -> Click on the top logo 5 times to enable the debug menu.
- Firefox settings -> Secret Settings -> Enable Use third party CA certificates.