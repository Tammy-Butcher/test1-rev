---
title: Setup Expiration Rules
excerpt: >-
  How to configure your own expiry rules so that videos automatically Inactivate
  or Delete
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
The **Expiration Management** option under the **Media Settings** menu displays expiration rules for video uploads and allows you to define new expiration parameters as needed. Expiration rules are based on days and views. A default rule may be set for all video uploads.
[block:callout]
{
  "type": "danger",
  "title": "Warning",
  "body": "[Expiration rules](doc:allow-expiration-rules) must be enabled globally under **Media Settings** > **Features **before you may use this functionality.\n\nOnce saved, expiration rules may *not *be modified with the exception of **Name**, **Default **rule status, and **Delete **status. \n\nIf you need to modify a rule *setting*, you must re-create the rule and add the videos again (through bulk editing if you have added several videos) and then delete the old rule."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1ed871-expirationManagement.png",
        "expirationManagement.png",
        1053,
        374,
        "#f0f3f5"
      ],
      "caption": "View all rules on the Expiration Management form"
    }
  ]
}
[/block]
## Create an Expiration Rule

Expiry Rules are created so that videos may be set to **Inactive **or are **Deleted ** from the portal if they meet the following conditions:
* No views after X amount of days
* Set to expire in X days
[block:callout]
{
  "type": "success",
  "title": "Use Case Example",
  "body": "Expiry Rules can be created to set a video to **Inactive **status if it has not been viewed in 365 days. \n\nExpiry Rules can be created to make sure all Human Resource videos are set to **Delete **after 5 days."
}
[/block]
Click the **Add Expiry Rule** button to create a new rule.  Configuration options appear under existing rules at the bottom of the form.
[block:parameters]
{
  "data": {
    "h-0": "Option",
    "h-1": "Description",
    "0-0": "Default",
    "0-1": "Sets the default expiration rule. Only one default rule may be set at a time. You may also deselect all rules so that no default is set. \n\nIf a default rule is set, new uploads are automatically set to expire based on this rule.",
    "1-0": "Name",
    "1-1": "The Expiration Management rule name. Click to edit the name.",
    "2-0": "Rule Type / Days",
    "2-1": "The types of rule you may create.\n\n- **Number of Days Before Expiry**: Must be greater than zero. The video is visible for the number of days in the **Days **column and then expires and is set to either **Inactive **or **Deleted**.\n\n- **Number of Days without Views**: Must be greater than zero. The number of days in the **Days **column the video may go *without *being viewed (or partially viewed) before it expires and is set to either **Inactive **or **Deleted**.\n\n- The **Video Owner** is emailed 7 days prior to video expiration and again upon the actual expiration no matter which rule is created.",
    "3-0": "Delete Upon Expiry",
    "3-1": "If selected, videos are **Deleted **upon expiration.\n\nIf *not *selected, videos are set to **Inactive **status instead.",
    "4-0": "Delete (x)",
    "4-1": "Deletes the Expiry rule. If you delete a rule, videos that are set to expire under that rule will no longer expire."
  },
  "cols": 2,
  "rows": 5
}
[/block]