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
Rev also has Channel roles and permissions that are separate from Rev roles though they are similar in function. Channel roles and permissions relate *only* to the management of a Rev channel. Further, Rev roles do *not* have permissions within the scope or context of a Channel, and this includes a Rev Account Admin. Instead, Admins need to access the Channel through the Users menu if needed.

> 🚧 Important!
>
> You should always make sure that your Channels have *at least one* **Channel Admin** assigned when you create a Channel so that you have someone in charge of managing the Channel settings and members.

Because Channel roles are separate from Rev roles, this means that you may designate a non-admin account in Rev as a Channel Admin for a Channel if you so choose.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Role
      </th>

      <th>
        Permissions
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Channel Admin
      </td>

      <td>
        Access to all Channel features  

        Manage all Channel content  

        Manage all Channel users and groups  

        Ability to edit all Channel content
      </td>

      <td>
        Similar to the Rev **Account Admin** role only Channel specific only.  

        This role has all the abilities of the **Channel Member** and **Channel Contributor** roles in addition to being able to edit new Channel Members and Channel settings (of the specific Channels they administer *only*).  

        Channel Admins may *not* edit the settings of Channels where they do *not* have the Channel Admin role assigned even if they are an Account Admin role in Rev.  

        As previously stated, within the context of a Channel, the *Channel* role governs, not the Rev role.
      </td>
    </tr>

    <tr>
      <td>
        Channel Contributor
      </td>

      <td>
        All permissions granted to Channel Members, plus:  

        Upload video assets including recording Live streams  

        View/edit content based on permissions
      </td>

      <td>
        Similar to the **Media Contributor** role in Rev. This role has view and upload permissions to the Channel along with sort and filter abilities.  

        However, Channel Contributors have *no* ability to edit Channel settings and members. Only Channel Admins may do this.
      </td>
    </tr>

    <tr>
      <td>
        Channel Member
      </td>

      <td>
        View, sort, and filter Channel video assets  

        Attend events that the Channel has been granted access to  

        This user *cannot* add content to the Channel
      </td>

      <td>
        The default role that is assigned when a User or Group is first added to a Channel.  

        Similar to a **Media Viewer** role in Rev, the Channel Member role only has view, sort, and filter access. It may *not* upload or edit Channel video assets.
      </td>
    </tr>
  </tbody>
</Table>

## Channel Granular Roles and Permissions

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Role
      </th>

      <th>
        Permissions
      </th>

      <th>
        Granular Restrictions
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Channel Uploader
      </td>

      <td>
        Attend events that the Channel has been granted access to.  

        View, sort, and filter Channel video assets.  

        Upload content to the Channel.
      </td>

      <td>
        This is a granular form of the **Channel Contributor** role with the main difference being this role has *no* access to the **Live Recording** tab on **Upload** for channels.
      </td>
    </tr>
  </tbody>
</Table>
