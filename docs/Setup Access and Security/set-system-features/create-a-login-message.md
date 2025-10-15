---
title: Create a Login Message
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
**Login Messages** are used to create text messages or notifications that appear to users when they log in to Rev so that messages such as Terms of Service may be created and updated as needed. When a system login message is created, the user _must_ accept that they have seen the message the first session they log in _after_ the message is created (or updated) by an Account Admin. 

Each successive session after that, the message is no longer viewed _unless_ the Account Admin updates and resets the message _or_ sets the message to display each time a user logs in (disabled by default).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8db1854-loginMessageReset.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]

To create a login message:

1. Navigae to **Admin > System Settings > User Security**.
2. Scroll to the **Login Messages** section.
3. Enter the text to display in the supported language form.
4. If you want the message to display _every_ time the user logs in, click the **Show login message on every login** checkbox.
5. As noted above, you can click the **Reset** button to display all messages again to users and force acceptance (such as updating a Terms of Service Agreement). This means the message will display again on the next login even if the **Show login message on every login** checkbox is not enabled.
6. Click the **Save** button once you have made your selections and have created your login message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fd5c8ad-loginMessage.png",
        null,
        "Login Messages display to users the first time they log in after it is created."
      ],
      "align": "center",
      "caption": "Login Messages display to users the first time they log in after it is created."
    }
  ]
}
[/block]