---
title: Getting Started - Devices
excerpt: >-
  This topic describes how to access Device set up in Rev and the initial steps
  you need to take before you begin to configure any device in Rev
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
To add and configure devices in Rev, use the **Devices **menu under the [Admin Menu Options](doc:admin-menu-options).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/138932e-devices.png",
        null,
        "The Devices Menu is accessible to Account Admins under the Admin Header Navigation Menu"
      ],
      "align": "center",
      "caption": "The Devices Menu is accessible to Account Admins under the Admin Header Navigation Menu"
    }
  ]
}
[/block]


There are some initial steps that are performed first before you are ready to add a device in Rev.

1. Each device _must _ have an API Key associated with it.  You may add a key for _each _ device or one that is used for _all _ devices. The exception is the **LDAP connector key** which must be a _separate_ key from system device keys. **View**: [Create an API Key](doc:create-an-api-key).  Make note of this key so you can add it to the device you eventually create.

2. Add the **Host URL** of your Rev installation to _each_ device you are configuring. Each device has a Rev section and field to place this information.
   - Example 1: To configure and link a DME, enter your **Rev Host URL** in the **System Configuration** > **Rev Interface** section of the DME.
   - Example 2: To configure and link an Encoder, enter your **Rev Host URL** in the **API Key** and **Host **fields under the **System Configuration** > **General **section of the Encoder.

> 👍 Tip
> 
> See the individual device's online Help (keyword search: Rev) for details on setting up **Rev Host URLs** if needed.  Or, contact [Vbrick Support](https://portal.vbrick.com/open-a-case/).

3. The Rev Host URL is obtained from the **Account Host Name** field on the **Contact **module or from your browser bar URL on the **Log in** screen minus the “**#/login**” text. **View**: [View and Edit Account Details](doc:view-and-edit-account-details) for instructions on finding the Host URL.

4. Once you have created and made note of **API Keys** for each device and entered the **Rev Host URL** for each, you are ready to add your individual devices to Rev.