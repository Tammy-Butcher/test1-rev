---
title: User Account Management
excerpt: This topic describes how to create and manage Users in Rev
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
You must have the **Account Admin** role to manage user accounts in Rev. This includes adding, editing, and managing passwords. Users are also imported and managed with LDAP and Okta groups. Finally, you may also add users (and groups) through a CSV upload process.

> 👍 Tip
> 
> A new user is considered an **Unlicensed **account and must be **activated **or **confirmed **so that the account status becomes **Active**.

Once the user is **Active**, you may assign the user a **Role **that has certain permissions defined such as the ability to view, edit, and upload content. You may also add the user to a **Group**. 

To access the Users module:

1. Navigate to **Admin** > **Users **> **Users** menu in the [Admin Menu Options](doc:admin-menu-options). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/568e6a112fd2adec23eb850778def0051ee2f9c8d3dfbd6a82c333f7e00ef0ac-usersMenu.png",
        null,
        "The Users Menu is accessible to Account Admins under the Users Header Navigation Menu"
      ],
      "align": "center",
      "caption": "The Users Menu is accessible to Account Admins under the Users Header Navigation Menu"
    }
  ]
}
[/block]


2. The **Users **module is displayed. Use it to add, edit, upload, and manage the user accounts in your portal.

## Create a User API Key

Once the new User account is created and saved, you are able to generate a **User-level API key** and secret for authentication and authorization for use with Rev's [User Login API](ref:authenticateuser). When this key is used, the system respects the role/permission of the user that the key belongs to when responding to the API calls.   

A Rev license count is consumed when this key is used _only_ if the User account is _both_ in **Unlicensed **and **Active **status.  Also, if the User is suspended, the key does not work.

> 🚧 Important!
> 
> The user-level API key created here is different than Rev's [system-level API keys](doc:create-an-api-key) that are used by Vbrick devices (DME, Encoders, AppleTV, and so forth).

To generate a User API key:

1. Navigate to the User account and edit the account.

2. Scroll to the **API Key** section and click the **Generate API Key** button.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc713a2-generateKey.png",
        "generateKey.png",
        402
      ],
      "align": "center",
      "caption": "Click the Generate API Key button to create an API Key and Secret for a User Account"
    }
  ]
}
[/block]


3. Be aware that the first time the API Key is generated is also the _only_ time the Secret is visible.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8c3ab8e-keyGenerated.png",
        "keyGenerated.png",
        502
      ],
      "align": "center",
      "caption": "The Secret can be viewed and copied only after the first time it is generated.  It must be regenerated if you need to view it again later."
    }
  ]
}
[/block]


4. You can copy the API Key, delete it, or regenerate it.  You may _not _ view the Secret again once you have saved the User.  You must regenerate the API Key to retrieve the Secret again.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1ec3e2-keyFinalized.png",
        "keyFinalized.png",
        502
      ],
      "align": "center",
      "caption": "Click the Copy button next to the API Key to copy it"
    }
  ]
}
[/block]