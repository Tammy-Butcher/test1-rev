---
title: Delete a User Account
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
> ❗️ Warning!
> 
> Users that are deleted may not be recovered so use this feature with extreme caution!

- You may not delete your own account.
- Consider suspending accounts as opposed to deleting them.
- You may delete Users imported through LDAP, however, if a sync occurs again, they are re-imported. It is better to manage the deletions through LDAP. Only suspended users that have never logged in are automatically deleted forever when synced. (View: **LDAP Server Synchronization Settings** for details on how to delete users that have never logged in to Rev and are suspended.)
- Users that are suspended manually through this drop-down are not deleted when an LDAP sync is run again if the **Delete Suspended Users** checkbox is enabled. (View: **LDAP Server Synchronization Settings** for details on how to delete users that have never logged in to Rev and are suspended.)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e61aa54-deleteUserLink.png",
        "deleteUserLink.png",
        233
      ],
      "align": "center",
      "caption": "Click the Delete link on Actions dropdown to delete a User.  This process may not be reversed!"
    }
  ]
}
[/block]