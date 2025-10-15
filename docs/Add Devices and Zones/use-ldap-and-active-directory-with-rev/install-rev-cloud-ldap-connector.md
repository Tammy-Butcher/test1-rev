---
title: Download and Install the Rev Cloud LDAP Connector
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Before you may import LDAP groups, you must first download and install the **Rev Cloud LDAP Connector**. Vbrick recommends that Rev Cloud customers upgrade to the latest version of the LDAP Connector to maintain integrity with the latest release of Rev Cloud. Vbrick supports the current release and two prior versions of the LDAP Connector.

> 📘 Note
> 
> You do _not_ need to download this application if you are using **On-Prem Rev**. Proceed to [Add an LDAP Connector Device](doc:add-ldap-connector-device).
> 
> If you are performing a **fresh install** of the LDAP Connector (rather than an upgrade), follows the same steps outlined here and begin at step three by uninstalling your current LDAP Connector. 
> 
> Be aware that you may not copy the config file to a new install. If you are upgrading, please follow the steps as outlined in this document.

The latest LDAP Connector version is found on the Vbrick Customer Portal [Downloads ](https://portal.vbrick.com/downloads/)site under the **Applications **tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e03ea3bd0581807dc2fd5ccf65a08cd5c3d0788a6b2fa1f8cd4e312f48ce8de-LDAPDownloads.png",
        "ldapConnectorDownload.png",
        "The latest LDAP Connector for Rev Cloud should be installed on your local environment"
      ],
      "align": "center",
      "caption": "The latest LDAP Connector for Rev Cloud should be installed on your local environment"
    }
  ]
}
[/block]


## Requirements

Before you begin your installation or upgrade, make sure you have the following:

- URL to your Rev portal
- The API Key you created to use with your LDAP Connector
- Make sure you [collect this information first](doc:getting-started-with-rev-devices) from your Rev portal before you begin.
- The following Operating Systems are supported for the LDAP Connector (v8.0+):
  - Windows Server 2019
  - Windows Server 2022
  - Windows Server 2025

## Installation/Upgrade Steps

To upgrade or install the LDAP Connector, complete the following steps:

1. In the **Windows Task Manager** > **Services** tab, stop the **VBrick Rev LDAP Connector** service. (Right-click > Stop)
2. Move the current LDAP log file to another directory such as "temp" or "oldlogs". The log file location is `C:\\Logs` and is titled, `LDAPConnectorlog.txt`.
3. Uninstall the current LDAP Connector by using Windows **System Settings** > **Add or Remove Programs**.

> 📘 Note
> 
> The first three steps (1-3) only need to be performed if you already have the connector installed.

4. As noted above, download the latest version of the LDAP Connector from the [Customer Portal Download](doc:https://portal.vbrick.com/downloads/) site.
5. Right-click and run the downloaded Rev LDAP Connector program as an Admin.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d544a723498da96b2f31a03a193e3e239d7fba9d7c6a0d9347b87abe9a0fa88-001_Welcome.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


6. Click **Next** to begin the installation set-up once it starts.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e35859ef442b36216dade40197b78a5d71f4a902ec8c447e560054e7fa86c6f-002_Installing_ASP.NET_Core.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


7. Your .NET version needs to be v8.0.16 or later. If you are upgrading to Rev v8.0 or installing the connector for the first time, you will be notified that this version is installing. If you already have this version or later, this step is skipped.

> ❗️ Caution!
> 
> Note that if you click **Cancel** here and do _not_ have v8.0.16 or later installed, your connector will not work!

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f8d278aa75952629c9f6eb93099af52ba9987452e3b3cf02b2235425d8dc3482-003_Destination_Path.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


8. Verify the installation directory for the connector.  Click the **Change** button to change the installation directory.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6cd46c2bc85a570c2a15b4c1f5fb32ec6492b01254cb25029bfee83c6ad28bcc-004_Customer_Information.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


9. Enter your **Rev URL** and **Rev API Key**. As noted, this should be [created and/or retrieved](doc:getting-started-with-rev-devices) before you begin the installation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1e48fff0868a2d7d5b7f6b98361357b6f33d28180390f3d1eda335569cd12d74-005_Ready_to_Install_.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


10. Click the **Install** button to begin the LDAP Connector installation or upgrade once all set-up is complete.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50ba6df911effbcf0c18764e9041f886909f4bdc1056f45c783dddd673463e71-006_installing.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


11. A **Status** bar will keep you informed of the installation or upgrade's progress.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29d325360358c355bd21d113b807d5cdd52e1eb12d3b98599b7f07915bf0b199-009_Finish.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


12. Click the **Finish** button to complete the installation/upgrade.
13. Once the connector is installed, verify that the **Vbrick Rev LDAP Connector** service is running again in the **Windows Task Manager**.

## Proxy Server Settings

If you are using the connector with a Proxy server, the following settings can be added to the **VBrickPlatform.LdapConnector.Runtime.dll.config** file:

```Text VBrickPlatform.LdapConnector.Runtime.dll.config
<add key="ProxyServerUrl" value=""></add>
<add key="ProxyServerUsername" value=""></add>
<add key="ProxyServerPassword" value=""></add>
```

> 📘 Note
> 
> The LDAP Connector must be on **v8.0** or greater to use a Proxy server.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22aa0adc984bddd0304f905adb73c86cafe3afadd13f5633a71a42f9381092cc-LDAPConnectorv8.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


## Verifying Your LDAP Connector Installation or Upgrade

To verify your installation or upgrade, complete the following steps:

1. Check the new **LDAP log** and ensure it is connecting to Rev with no errors. These are normally preceded by [ERROR], [WARN], or [FATAL] if there are connection errors.
2. In Rev, navigate to **Admin** > All Devices. Ensure that your LDAP Connector status is **Active** with a green checkmark displayed.
3. Open the LDAP Connector, scroll to the bottom, and click the [Reset Connector Sync](doc:reset-ldap-connector-sync) button; then select **Update**.
4. Allow a few minutes (or longer for large imports) for the connector to sync completely. Confirm you are able to search for LDAP groups and the users are able to log in.

## Security Scanning Software

Certain security scanning software (such as **virus/malware protection software** or **Windows Firewall**) might interfere with proper functioning of the LDAP connector. Please make sure to configure all security scanning software and firewall(s) to allow LDAP Connector to run properly or disable them on the Windows Server.