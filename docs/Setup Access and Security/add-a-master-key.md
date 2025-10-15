---
title: Add a Master Key
excerpt: >-
  Use Rev's Master Key system to manage and control your assets independently of
  Vbrick
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
The **Key Management** module provides the ability to activate a new **Master Key** and also maintains a **History of Master Key Rotations**.

Adding a Master Key transfers complete ownership of encryption keys to you allowing you to own, manage, and control access to all of your assets independently of Vbrick through Rev’s use of the Amazon Web Service (AWS) S3 Key Management Service. 

You have the assurance of knowing that you retain complete control of your video assets, even when they are in the cloud. Further, Rev keeps track of Master Key rotations so that you are fully aware of past key history and usage.

<Image title="keyManagementModule.png" alt={655} align="center" src="https://files.readme.io/94b7fbb-keyManagementModule.png">
  Manage Master Keys under the System Settings menu option
</Image>

> ❗️ Warning!
>
> A waiver must be on file with Vbrick to use this feature.

The Key Management module displays:

* **Key** — The current **Master Key** and all previous keys used. Note: The actual **Master Encryption Key** is *not* stored in Rev.
* **Key Added** — The date each key is added and the user name that added the key.
* **Key Activated** — The date each key is activated and the user name that activated the key.
* **Key Disabled** — The date each key is disabled and the user name that disabled the key.
* **Status** — They key’s status. The number of files that failed encryption is noted here.

## Activate a New Master Key

To activate a new Master Key:

1. Navigate to **Admin > System Settings** > **Key Management**.

2. Enter a new key in the **Master Key** field.

3. **Validate** and **Activate** the new key.

<Image title="activateMasterKey.png" alt={655} align="center" src="https://files.readme.io/0ea90ae-activateMasterKey.png">
  Previous Master Keys are tracked below the Current Key in use
</Image>

> ❗️ Warning!
>
> If you are replacing a Master Key, be sure to retain access to your previous Master Key until the key rotation process is complete.
