---
title: Create a User Account API Key
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
Once the new user account is created and saved, you are able to generate a **user-level API key** and secret for authentication and authorization for use with Rev's [User Login API](ref:authenticateuser). When this key is used, the system respects the roles and permissions of the _user_ that the key belongs to when responding to the API calls.   

A Rev license count is consumed when this key is used _only_ if the User account is _both_ in **Unlicensed **and **Active **status.  Also, if the User is suspended, the key does not work.

> 🚧 Important!
> 
> The user-level API key created here is different than Rev's [system-level API keys](doc:create-an-api-key) that are used by Vbrick devices (DME, Encoders, AppleTV, and so forth).

To generate a user account API key:

1. Navigate to the user account and edit the account.

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