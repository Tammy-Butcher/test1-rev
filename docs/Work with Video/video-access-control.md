---
title: Video Access Control
excerpt: >-
  How to put secure measures in place to determine who can access, view, and
  edit your videos both internally and externally.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
To update **Video Settings** in Rev:

1. Navigate to a video and hover over the **Video Settings** button in the top right corner.

2. Click **Details ** from the options that appear.  Several tabs appear that allow you to create and modify the video's metadata. Select a tab depending on which setting you want to update. 

3. The features in this topic describe **Access Control** tab features.

A video's **Access Control** puts security measures in place to determine who can view and edit the video.  There are several implementable and flexible access levels in Rev that allow multiple combinations of Rev **Users**, **Groups**, and **Channels **access in combination with a **Public **video along with assigning **Edit Access** as needed. You can also designate _specific_ external users **Trusted Access** via email address with **expiration** dates.  Each level of access is described in detail in this topic.

> 📘 Note
> 
> Some Access Controls must first be enabled under the [Public Access](doc:guest-portal-and-public-access-control) section by your Account Admin in **System Settings** > **Content Restriction** before they are visible and/or usable.

## Set Video Access to Public

When the **Public** setting is enabled, this means a video is accessible to everyone both internally and externally when the video is embedded or shared. The video must be in **Active** [status](doc:video-status).

> 👍 Tip
> 
> The **All Internal Users** Access Control is also enabled by default as a result of setting a video to **Public**.  This may not be disabled since users may also choose to use a Rev account to view a Public video as an alternative at any time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/25363e9-addPublicAccess.png",
        "publicAccessControl.png",
        575
      ],
      "align": "center",
      "caption": "Passwords on Public videos are shared. For increased security, consider an alternative Access Control, such as a Trusted Access Viewer."
    }
  ]
}
[/block]


### Set a Password on a Public Video

You also have the option to implement a shared **Password **on a Public video for additional security.

Notes about password-protected videos:

- This is a _shared_ password that cannot be changed by any one user account.
- Users need to know this password before viewing the video on the **Guest Access URL** or through any sharing or embedding options used. To remove the password, simply delete it and save the video again.
- When a user attempts to view the video using a public URL, a password prompt is displayed displaying the video **Title **and **Description**. The password you set must be entered. The user may alternatively login using a registered **Rev account** as well as previously noted.

> ❗️ Caution
> 
> If this video is added to a **Playlist**, it will _not_ play. The user receives a message stating, "The resource you have requested cannot be accessed". The user is redirected back to the login page.

## Provide External Application Access to a Video

If the **Trusted Access setting for External Applications** has been enabled, this toggle is used to provide access to this _specific_ video on _external_ business applications that have been specified by your organiation.  This setting is disabled by default and requires additional setup by your Account Admin.

## Set Video Access to Logged In Users

To make sure that viewers are logged-in **Rev Account** users, set your Video Access control to **All Internal Users**.  This means that to view the video, the user _must_ log in to your Rev portal first.  

However, this is only true if this is the _only_ Access Control set.  In other words, if you enable this setting and also enable the **Public** access control or either of the **External Viewer** controls, they _also_ function along with this control. They are _not_ mutually exclusive.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dfdf29e-addInternalAccess.png",
        "allInternalUsersAccessControl.png",
        574
      ],
      "align": "center",
      "caption": "Rev accounts that are logged in may view an All Internal Users video.  \n However, to edit the video, the Edit Access button next to the account must be toggled on."
    }
  ]
}
[/block]


> 👍 Tip
> 
> The _only_ way to permit only Rev Account users to view a video is to enable only the **All Internal Users** Access Control and _disable_ all other Access Controls. 
> 
> When _only_ the **All Internal Users** control is enabled, this means that to view the video, the account _must_ be logged in to a Rev portal.
> 
> If you do _not_ select **All Internal User** control, only the specific Access Controls selected will have access to the video.

### Add Edit Permissions to a Video

You can specify edit permissions for a video by adding the user, group, or channel to the **Internal Viewers** form. **Edit Access** permissions are **off** by default to accounts added to this control, however, you can **add** edit permissions by clicking the **Edit Access** button next to the user, group, or channel name once you add them.

- To specify edit permissions for an internal account (users, groups, channels), that account must be added to the **Access Control List** in the **Find Items** control first.  
- **Edit Access** permissions are **off** by default to all internal accounts added to this control.

## Provide an External Viewer Access to a Video

You can use the **External Viewers** toggle to enable access to one or more _specific_  external viewers via email.  A Rev account is not required and you do not have to make the video **Public** to everyone. This setting must be [globally enabled by your Account Admin](doc:docs/guest-portal-and-public-access-control#enable-trusted-access-for-external-viewers) first and is disabled by default on your videos.

When you _enable_ **External Viewer** access:

1. The **Specify External Viewers** form appears for **Media Contributors** and above with **Edit Access** (Internal Media Contributors are not included). 
2. Click the **Add New** button to add one or more email addresses that you want to grant access to the video to.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0be3d93-enableExternalViewers.png",
        "",
        "Use the External Viewers control to grant an external viewer access without making the video Public to everyone"
      ],
      "align": "center",
      "caption": "Use the External Viewers control to grant an external viewer access without making the video Public to everyone"
    }
  ]
}
[/block]


3. The **Add External Viewers** form appears.  Enter the viewer's email address for access to the video.  If you are entering more than one, seperate the list by a comma (with no spaces).  You can enter a message to the recipients as well.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/325466d-addExternalViewers.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


4. Click the **Send** button when you are ready to provide access to the email accounts you have listed.
5. Each email address listed receives its own, secure link to the video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b94d6a-emailSecureLinksGranted.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


6. Once the video processes the external link, the **Specify External Viewers** form is updated the email addresses you provided.

> ❗️ Warning!
> 
> You must use the **Save** button and save the video after you add an email to the **Specify External Viewers** form.  Once you add an email, it is automatically sent to the user. If you neglect to save after this, the user receives a no access error.

When you _disable_ **External Viewer** access:

- Access you have previously granted is immediately revoked.
- The viewer emails remain in place (not deleted).

### Manage External Viewer Video Access

Your Account Admin has specified how long external viewers have access to the videos in your system.  For example, your Admin may have set an expiration period of 14 days or no expiration period.  If there is a question on how long an external user has access to the videos you are granting access to, contact your Account Admin.

That said, you also have the ability to manage the access you have granted through the **Actions** drop-down control next to each email address on the **Specify External Viewers** form.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/881e8fc-externalViewersActions.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


| Action    | Description                                                                                                                                                                                                                                                   |
| :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Copy Link | Generates a new link that you can send to the specific external viewer. You cannot use this in the **Bulk Action** dropdown since each link is a unique link to that email address.                                                                           |
| Renew     | Immediately revokes the current access and generates a new access link along with a new date (if an expiration date is in effect).  It then emails the user with the new link.  Note that any status can be renewed: **Active**, **Expired**, or **Revoked**. |
| Revoke    | Only displays if access is not already remoked or exired.  Immediately revokes access to the external viewer email but leaves details in place in the **Specify External Viewers** table.                                                                     |
| Delete    | Revokes access and also removes all details from the **Specify External Viewers** table                                                                                                                                                                       |

Each of these actions are available to use through the **Bulk Action** drop-down as well if you need to perform them on several users at once with the exception of **Copy Link**.  This action cannot be performed since each user receives a unique  link to the video.

Finally, if you have granted access to several email accounts, use the **Search** control to find that account quickly.

## Private Videos

There is no physical **Private **setting for a video.  However, the default setting of a video when first uploaded/added to Rev along with **Inactive **[status](doc:video-status) is to have both all **Access Control** settings toggled to the **OFF** position. This implicitly makes the video **Private ** because, at this point, only the video owner and Account/Media Admins are able view it.  

To more widely share access, you must _explicitly_ specify the accounts that are able to _view_ it and then toggle on the appropriate control.

> 📘 Notes
> 
> Keep in mind that when adding Access Controls, you may _only_ add combinations of users, groups, and channels that you have rights/permissions to.

## Video Access Level Versus Roles and Permissions

Keep in mind that, depending on your role and/or permissions in Rev, you may not be able to modify a video's access level or add users and groups to its **Access Control**.

For example, **Media Viewers** in Rev do not possess upload abilities.  This means that, even if a Media Viewer has been specified as a [Video Owner](doc:video-owner) or has been assigned Edit rights to a video, they are _not_ able to modify the **Video Access Control** to specify a [Public](doc:video-access-control#public-videos), [All Users](doc:video-access-control#all-internal-users-videos), or [Private](doc:video-access-control#private-videos) video access level.  Further, a Media Viewer is not able to add additional **Users** or **Groups**to a video.  These controls are dimmed out or do not function.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02df17b-mediaViewersNoAccess.png",
        "accessControlMediaViewer.png",
        596
      ],
      "align": "center",
      "caption": "Media Viewers cannot modify a video's Access Control even if they are the Video Owner"
    }
  ]
}
[/block]


The exception to this concerns channels: If the **Media Viewer** is _also_ a [Channel Contributor](doc:roles-and-permissions#channel-roles-and-permissions), that specific channel can be added to the Access Control List by the Media Viewer.

> 👍 Tip
> 
> While items cannot be added _to_ the **Access Control List** (with the exception of Channel Contributor channels), items _can_ be **removed **.