---
title: Enable JWT Authentication
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
Vbrick Rev supports authentication based on signed and encrypted **JSON Web Token (JWT)** also known as **JSON Web Encryption (JWE)**.

> 📘 Note
> 
> If you are a **Vbrick EVP Customer** or **Partner** and want to use the [Vbrick Universal eCDN SDK](ref:vbrick-universal-ecdn-sdk), you must complete the steps below and enable **JWT Authentication**.
> 
> If you are a **Vbrick Universal eCDN Customer** or **Partner**, you must _also_ setup and configure your account.  View the [How to Set Up the Vbrick Universal eCDN](doc:how-to-set-up-the-vbrick-universal-ecdn) topic for details.

To start this process, navigate to the **Admin >  System Settings > User Security** menu:

1. Scroll to the **JWT Authentication** section.
2. Click the **Enable JWT Authentication & Authorization** checkbox.
3. Click the **Add New** button to upload your signing certificate and then generate and download your new encryption certificate.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0ba20d0-enableJWT.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


For complete details and a process overview, view the [JWT Authentication](ref:jwt-authentication) topic in the **Developer's** reference section of our **API** documentation.