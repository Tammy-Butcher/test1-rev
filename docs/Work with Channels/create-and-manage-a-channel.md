---
title: Adding a Channel
excerpt: >-
  How to set up new Channels and Channel Roles and best practices for managing
  them
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
**Channels **are an additional means in Rev to bundle users and groups together that may need to share specific content or video access rights for that content.

The Channels module is used to set up expanded permission structures for organizations since [Channel Roles (and permissions)](doc:roles-and-permissions#section-channel-role-definitions-and-permissions) are entirely separate from Rev's standard [Roles and Permissions](doc:roles-and-permissions).

For example, a User may be granted permission to upload videos to a Channel while outside of the Channel scope, the same User may only view videos in the general Rev portal.  This is because Roles and permissions are different within the scope of a Rev Channel.

It is important to remember that there are only two Rev roles that are able to _create_ a new channel; **Account Admins** and **Media Admins**.  Other than these two roles, only the **Channel Creator** role can create a new channel.

> 👍 Tip
> 
> A **Channel Admin** should be designated _immediately_ after the Channel is created.  This role is in charge of editing the Channel's settings and members.
> 
> It is important to note that the _Channel_ role governs what you can and cannot do within the structure of a Channel and its content rather than the _Rev_ role. This means that even Rev Account Admins are somewhat limited in actions and view options if they are not _also_ a member of the Channel in question.

To add a new Channel:

1. Navigate to the **Users **> **Channels** menu in the [Admin Menu Options](doc:admin-menu-options).  (You may also use the **Media **> **My Channels** > **Create New Channel** dropdown option from the [User Menu Options](doc:user-menu-options)).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/97e7488-channelsMenu.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]



2. Click the **Create Channel** button to display the **New Channel** form and create your channel by completing the required fields.

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Channel Name",
    "0-1": "Create or edit the name as needed. _Must be unique._ ",
    "1-0": "Channel Description",
    "1-1": "Create or edit text on the purpose of the channel.",
    "2-0": "Channel Logo Image",
    "2-1": "Upload a logo for the channel. Use a size of **480x360** for best results.  \n  \nIf no image is uploaded, the background color only is used for the Channel tile and Header.",
    "3-0": "Colors",
    "3-1": "Assign a background color for the Channel tile and Header.  \n  \nClick on the current color to use the color wheel or enter a hexadecimal color value in the **Header Background** field. **Reset Default** resets the color to template default in use.  \n  \nSelect either a **Light **or **Dark **font for the **Header Font Color** based on the background color you select.",
    "4-0": "Assign Users and Groups",
    "4-1": "Add **Users **and **Groups **to the channel.  \n  \nAssign a **Channel Admin** in charge of managing the Channel immediately."
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]