---
title: Enable Vbrick Mobile Access
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
To provide **Vbrick Mobile** app access to your portal users, you must make sure it is enabled.

To enable Vbrick Mobile access:

1.  Navigate to **Admin > System Settings > User Security**.
2. Scroll to the **Rev Mobile App Settings** section and click the **Mobile App Access** checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a4b00a1-enableMobileApp.png",
        null,
        "Users must have an active account and email address before they will be able to use the mobile app"
      ],
      "align": "center",
      "caption": "Users must have an active account and email address before they will be able to use the mobile app"
    }
  ]
}
[/block]

Settings for the app can be adjusted based on your security and compliance requirements by adjusting the **Mobile Inactivity Timeout** setting to the number of days (up to 365) that a user may be inactive before they are logged out automatically.

The **Vbrick Mobile** app is designed for on-demand playback and provides the ability to search for videos, browse channels and categories, and upload videos from Android or iOS devices. All custom settings, including branding, logo, and accent colors, are displayed in the app.

Once you enable access, users may [Download Vbrick Mobile](doc:download-vbrick-mobile) from both **Google Play** and the **Apple Store** for their mobile devices.

> 🚧 Important!
> 
> Vbrick mobile is available to all Vbrick cloud customers. Users must have an active account and email address in their company's cloud-hosted Vbrick portal to use the app.

## Microsoft Intune MAM Support

The Vbrick Mobile app is integrated with the **Microsoft Intune SDK** and can be managed by Intune if you enable it in Rev.  

### Rev Configuration

To enable **Mobile Application Management (MAM) **in Rev:

1. In the **Rev Mobile App Settings** section, check the **Microsoft Intune** checkbox.

> ❗️ Warning!
> 
> This setting is disabled by default and should _not_ be enabled until Intune is configured first. Enabling this before Intune is configured can cause unexpected results or crashes.

### Microsoft Intune Configuration

1. Navigate to the [Microsoft Intune Admin Center](https://intune.microsoft.com/#home).
2. [Add the Vbrick Mobile apps](https://learn.microsoft.com/en-us/mem/intune/apps/apps-add) - both Android and iOS.  Note that the types should be "Apps from the store (store apps)".
3. Once the app is published, [create and assign app protection policies](https://learn.microsoft.com/en-us/mem/intune/apps/app-protection-policies).

### Grant App Permissions

The Vbrick Mobile app can be [granted permissions](https://learn.microsoft.com/en-us/azure/active-directory/manage-apps/manage-application-permissions?pivots=portal) to your organization and its data by three methods: 

1. An admin consents to the application for all users.
2. A user grants consent to the application.
3. An admin integrates an application and enables self-service access or assigns users directly to the application.

An admin can consent to the application for all users by performing the following steps:

1. Login into <https://portal.azure.com> as admin.
2. Click **Enterprise applications** from the left side menu.
3. Click **Vbrick Mobile** from the app list.  If you do not see this option, try **install the app** and then login from the app first.
4. Click **Permissions** from the left side menu.
5. Click the **Grant admin consent for Vbrick Systems** blue button.

### Troubleshooting

If you see an error when you try to **Upload** a video in the Android app, check your **Intune app protection policy** for the Android app.  By default, the Intune policy sets **receive data from other apps** to **policy managed apps**.  You need to add the app that provides the video to the managed apps list or set **receive data from other app** to **All apps**.