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
**Channels** are an additional means in Rev to bundle users and groups together that may need to share specific content or video access rights for that content.

The Channels module is used to set up expanded permission structures for organizations since [Channel Roles (and permissions)](doc:roles-and-permissions#section-channel-role-definitions-and-permissions) are entirely separate from Rev's standard [Roles and Permissions](doc:roles-and-permissions).

For example, a User may be granted permission to upload videos to a Channel while outside of the Channel scope, the same User may only view videos in the general Rev portal.  This is because Roles and permissions are different within the scope of a Rev Channel.

It is important to remember that there are only two Rev roles that are able to *create* a new channel; **Account Admins** and **Media Admins**.  Other than these two roles, only the **Channel Creator** role can create a new channel.

> 👍 Tip
>
> A **Channel Admin** should be designated *immediately* after the Channel is created.  This role is in charge of editing the Channel's settings and members.
>
> It is important to note that the *Channel* role governs what you can and cannot do within the structure of a Channel and its content rather than the *Rev* role. This means that even Rev Account Admins are somewhat limited in actions and view options if they are not *also* a member of the Channel in question.

To add a new Channel:

1. Navigate to the **Users** > **Channels** menu in the [Admin Menu Options](doc:admin-menu-options).  (You may also use the **Media** > **My Channels** > **Create New Channel** dropdown option from the [User Menu Options](doc:user-menu-options)).

<Image align="center" src="https://files.readme.io/97e7488-channelsMenu.png" />

2. Click the **Create Channel** button to display the **New Channel** form and create your channel by completing the required fields.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Channel Name
      </td>

      <td>
        Create or edit the name as needed. *Must be unique.* 
      </td>
    </tr>

    <tr>
      <td>
        Channel Description
      </td>

      <td>
        Create or edit text on the purpose of the channel.
      </td>
    </tr>

    <tr>
      <td>
        Channel Logo Image
      </td>

      <td>
        Upload a logo for the channel. Use a size of **480x360** for best results.  

        If no image is uploaded, the background color only is used for the Channel tile and Header.
      </td>
    </tr>

    <tr>
      <td>
        Colors
      </td>

      <td>
        Assign a background color for the Channel tile and Header.  

        Click on the current color to use the color wheel or enter a hexadecimal color value in the **Header Background** field. **Reset Default** resets the color to template default in use.  

        Select either a **Light**or **Dark**font for the **Header Font Color** based on the background color you select.
      </td>
    </tr>

    <tr>
      <td>
        Assign Users and Groups
      </td>

      <td>
        Add **Users**and **Groups**to the channel.  

        Assign a **Channel Admin** in charge of managing the Channel immediately.
      </td>
    </tr>
  </tbody>
</Table>
