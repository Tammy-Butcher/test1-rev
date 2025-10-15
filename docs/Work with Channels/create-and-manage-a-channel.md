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
  robots: index
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

1. Navigate to the **Users **> **Channels** menu in the [Admin Menu Options](doc:admin-menu-options).  (You may also use the **Media **> **Channels** > **Add New** dropdown option from the [User Menu Options](doc:user-menu-options)).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/96474c1c334849782ac41b22d5b9746a54bd3f213af61a728a6b802161abea49-channelsMenu.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


2. Click the **Create Channel** button to display the **New Channel** form and create your channel by completing the fields.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22857fb5b0cfffe7136044e52220861b1b76371a77b6dc536a2ac590019d4a7f-createChannel.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Channel Name",
    "0-1": "Create or edit the name as needed. _Must be unique._ ",
    "1-0": "Channel Description",
    "1-1": "Create or edit text on the purpose of the channel.",
    "2-0": "Default Sort Order",
    "2-1": "Set the default order of how videos are shown for specific channels. Choose from **Upload Date** (default), **Recommended**, **Title**, and **Views**.",
    "3-0": "Channel Logo Image",
    "3-1": "Upload a logo for the channel. Use a size of **480 x 360** for best results.  \n  \nIf no image is uploaded, there will be a default icon used to show the channel.",
    "4-0": "Channel Banner Image",
    "4-1": "Upload the banner image for the channel. For best results, use a size of **1650 x 300** for best results.",
    "5-0": "Assign Users and Groups",
    "5-1": "Add **Users **and **Groups **to the channel.  \n  \nAssign a **Channel Admin** in charge of managing the Channel _immediately_."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]