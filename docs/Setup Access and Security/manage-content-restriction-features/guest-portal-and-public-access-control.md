---
title: Manage External Access to Videos and Webcasts
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
Vbrick Rev provides several methods of providing access and controlling the ability for users (or APIs) to share videos to external viewers.  They are:

- Public Access
- Guest Portal Access
- Trusted Access for VOD (External Viewers)
- Trusted Access for VOD (External Applications)

Each method is explained in more detail in the sections below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2d2f533-publicAccess.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


## Enable Public Webcasts Listing Type

Rev allows the ability to create and host [Public Events](doc:public-events) once this setting is enabled.

To enable Public Webcasts:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **Public Access** section and select the **Enable Public Webcasts** checkbox.

When _enabled_:

- Event Admins and Hosts are able to set the event **Listing Type** to **Public ** (and include a password if desired).
- This means that a user need not authenticate or possess a Rev user account to view the Webcast when launched. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0949e50-publicListingType.png",
        "publicWebcast.png",
        602
      ],
      "align": "center",
      "caption": "Enabling Public Webcasts makes the Public Listing Type visible during the event set up"
    }
  ]
}
[/block]


When _disabled_:

- Event Admins and Hosts are not able to set the event **Listing Type** to **Public **. The tab is not visible during set up.
- This means that a user needs to possess a Rev user account to view a Webcast when launched. 

## Enable Public Video Access

Rev permits videos to be designated [Public](doc:video-access-control#set-video-access-to-public) and does not require viewers to log in to Rev first to view them when they are shared. Instead, users can view all Public videos on a guest portal (no log-in needed) or view an individual shared video directly via the guest portal. 

Keep in mind that this grants _all_ external users access to the **Public** video (that also have the **Guest Portal** URL or the link to the video) versus **Trusted Access** where only _specific_ external users are granted access via email address and they are not listed on the guest portal.

To enable Public Video Access:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **Public Access** section and select the **Enable Public Video Access** checkbox.

When _enabled_:

- The [Public Access Control](doc:video-access-control#set-video-access-to-public) option in **Video Settings** becomes available for use. 
- This means that sharing this video does not require a login to Rev before viewing it.  It can be viewed by navigating directly to a guest portal (if enabled) or through a shared link (which plays it on the guest portal).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/062f3db-vodPublicAccessControl.png",
        "videoAccessControl.png",
        502
      ],
      "align": "center",
      "caption": "Enabling Public Videos makes the Public Access Control visible in Video Settings"
    }
  ]
}
[/block]


> 📘 Note
> 
> If a password is set for the video, the password is required before that individual video may be viewed through any public or embedded URL.

When _disabled_:

- The **Public Access Control** is no longer visible.
- This means that a user needs to possess a Rev user account to view the video or be granted **Trusted Access**. 

## Enable Guest Portal Access

If the **Guest Portal** setting is enabled, users can be directed to the **Rev Guest Portal URL**, where they may view all **Active** videos that are also **Public**. Guest users may _not_ any access to Rev menu functions with the exception of the Search, Filters, and Sort functions.

To enable Guest Portal Access:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **Public Access** section and select the **Enable Guest Portal Access** checkbox.

The **Guest Portal URL** displays under the checkbox for access to all videos that have been specified Public.  This is the URL that may be provided to users once enabled.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/09144b2-guestPortalAccess.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


When this setting is disabled, users _cannot_  view the Guest portal videos.  Instead, they must be shared directly. This prevents anyone from accessing videos without logging in first (embedded or otherwise) and keeps videos secure.

## Enable Trusted Access for External Viewers

Rev allows you to enable access to videos to _specific external users_ via email address.  They do not need to have Rev accounts and the videos do not need to be Public for this access. You can also specify an **expiration date** on this access (in days) or make the access infinite.

> 🚧 Important!
> 
> To use this control, you must have [Media Contributor](doc:roles-and-permissions) role or above. This does not include the Internal Media Contributor role.

To enable Trusted Access for External Viewers:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **Public Access** section and select the **Enable Trusted Access (External Viewers) for VOD** checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/28939cd-enableTrustedViewer.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


The **Expiry** field under the checkbox allows you to specify how long the access to the video is granted in number of days or if the access is infinite.  The default is fourteen days.

When _enabled_:

- The [External Viewers](doc:video-access-control#provide-an-external-viewer-access-to-a-video) control in **Video Settings** becomes available for use to grant **Trusted Viewer** access.
- This means that this video becomes available to those external **Trusted Viewers** you specify via email.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22aeed1-addTrustedViewer.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


> 👍 Tip
> 
> Each email address receives a unique secure link to the video. You can revoke, refresh, or delete the access at any time.

When _disabled_:

- The **External Viewers** control is no longer available.
- To view the video it must be **Public** or the user must log in with a Rev Account and have access to it through your portal.

## Enable Trusted Access for External Applications

This settings is enabled to allow your company to provide access to videos on your portal within other business applications.  Note that this does consume [Public hours](doc:rev-license-types-and-add-ons#usage-tracking) so you should plan accordingly.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7a8861e-trustedExternalApplicationEnable.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


When _enabled_:

The [External Application Access](doc:video-access-control#provide-external-application-access-to-a-video) control is available to enable on a video.  It is disabled by default.

Disabling this (once enabled), _immediately rejects_ all access to currently deployed authorization tokens you have set up.  This also requires configuration of a [JWT Authentication](doc:enable-jwt-authentication) token for the application on the **User Security** page.