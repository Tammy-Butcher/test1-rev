---
title: Vbrick Universal eCDN System Settings
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
The Vbrick Universal eCDN **System Settings** menu is limited to eCDN features only and allows you to create API keys, and manage Universal eCDN and user security features.

## Create an API Key for the Vbrick Universal eCDN

1. To create an **API Key** for the Vbrick Universal eCDN, navigate to **Admin > System Settings > API Key**.
2. Click the **Add Key** button.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cbc5d1d-apiKey.png",
        null,
        "Click the Add Key button to add a new API Key"
      ],
      "align": "center",
      "caption": "Click the Add Key button to add a new API Key"
    }
  ]
}
[/block]


Creating a key here works exactly like creating a [Vbrick Rev API Key](doc:create-an-api-key) with no differences.

## Vbrick Universal eCDN Settings

The **eCDN Settings** menu option under **System Settings** allows you to enable specific features for your Vbrick Universal eCDN account that are explained below.

### Enable Local DME Accounts for Vbrick Universal eCDN

Enable this setting to allow local Universal eCDN accounts access to DME Vbadmin pages on all DMEs that are connnected to the Vbrick Universal eCDN.

1. To enable local DME account access, navigate to **Admin > System Settings > eCDN Settings**.
2. In the DME Accounts section, enable the **Allow Local DME Accounts** checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/669eb18-allowLocalDME.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


For complete details on how this functionality works, view the [Allow Local DME Accounts](doc:dme-accounts) topic.

### Set the User Location Service URLs for the Vbrick Universal eCDN

Zone logic in Rev depends on routing users to the correct zone and closest DME to ensure optimal video distribution. Additionally, the Vbrick Peer-to-Peer feature can optionally (based on Administrator preference) utilize the user location to facilitate routing and peer sharing across subnets.  Make sure you understand the [User Location Service (ULS)](doc:user-location-service-uls) completely before you enable and configure this in the Vbrick Universal eCDN.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b74dcb0-userLocationRamp.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


### Vbrick Multicast Settings for the Vbrick Universal eCDN

The **Enable Vbrick Multicast Encryption** feature, when enabled, will force all Vbrick Multicast data payloads to be encrypted. While not required, this setting is highly recommended. There are specific requirements for this feature so you should read and understand the [DME and Vbrick Multicast Security](doc:dme-and-vbrick-multicast-security) topic in full before proceeding.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2228f93-enableVbrickMulticast.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


## User Security for the Vbrick Universal eCDN

The [JWT Authentication](doc:how-to-set-up-the-vbrick-universal-ecdn) section in **User Security** is where you set up your encryption and signing certificates for the Vbrick Universal eCDN during set up.

The remaining sections in this menu option function exactly the same as their Rev counterparts and take care of log-ins, password security, system messages and so forth.  For more details:

- [Single Sign On](doc:configure-single-sign-on-sso)
- [Set Password Rules](doc:set-portal-password-rules)
- [Rev Mobile](doc:enable-vbrick-mobile-access)
- [Suspended Users](doc:manage-system-login-and-email-messages)
- [System Login Messages](doc:create-a-login-message)