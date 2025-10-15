---
title: Channel Roles and Permissions
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
Rev also has Channel roles and permissions that are separate from Rev roles though they are similar in function. Channel roles and permissions relate _only_ to the management of a Rev channel. Further, Rev roles do _not_ have permissions within the scope or context of a Channel, and this includes a Rev Account Admin. Instead, Admins need to access the Channel through the Users menu if needed.

> 🚧 Important!
> 
> You should always make sure that your Channels have _at least one_ **Channel Admin** assigned when you create a Channel so that you have someone in charge of managing the Channel settings and members.

Because Channel roles are separate from Rev roles, this means that you may designate a non-admin account in Rev as a Channel Admin for a Channel if you so choose.

[block:parameters]
{
  "data": {
    "h-0": "Role",
    "h-1": "Permissions",
    "h-2": "Description",
    "0-0": "Channel Admin",
    "0-1": "Access to all Channel features  \n  \nManage all Channel content  \n  \nManage all Channel users and groups  \n  \nAbility to edit all Channel content",
    "0-2": "Similar to the Rev **Account Admin** role only Channel specific only.  \n  \nThis role has all the abilities of the **Channel Member** and **Channel Contributor** roles in addition to being able to edit new Channel Members and Channel settings (of the specific Channels they administer _only_).  \n  \nChannel Admins may _not_ edit the settings of Channels where they do _not_ have the Channel Admin role assigned even if they are an Account Admin role in Rev.  \n  \nAs previously stated, within the context of a Channel, the _Channel_ role governs, not the Rev role.",
    "1-0": "Channel Contributor",
    "1-1": "All permissions granted to Channel Members, plus:  \n  \nUpload video assets including recording Live streams  \n  \nView/edit content based on permissions",
    "1-2": "Similar to the **Media Contributor** role in Rev. This role has view and upload permissions to the Channel along with sort and filter abilities.  \n  \nHowever, Channel Contributors have _no_ ability to edit Channel settings and members. Only Channel Admins may do this.",
    "2-0": "Channel Member",
    "2-1": "View, sort, and filter Channel video assets  \n  \nAttend events that the Channel has been granted access to  \n  \nThis user _cannot_ add content to the Channel",
    "2-2": "The default role that is assigned when a User or Group is first added to a Channel.  \n  \nSimilar to a **Media Viewer** role in Rev, the Channel Member role only has view, sort, and filter access. It may _not_ upload or edit Channel video assets."
  },
  "cols": 3,
  "rows": 3,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


## Channel Granular Roles and Permissions

[block:parameters]
{
  "data": {
    "h-0": "Role",
    "h-1": "Permissions",
    "h-2": "Granular Restrictions",
    "0-0": "Channel Uploader",
    "0-1": "Attend events that the Channel has been granted access to.  \n  \nView, sort, and filter Channel video assets.  \n  \nUpload content to the Channel.",
    "0-2": "This is a granular form of the **Channel Contributor** role with the main difference being this role has _no_ access to the **Live Recording** tab on **Upload** for channels."
  },
  "cols": 3,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]