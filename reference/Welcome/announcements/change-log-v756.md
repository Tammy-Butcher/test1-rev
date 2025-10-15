---
title: Change Log (v7.56)
excerpt: ':calendar: Date Added: December 2023'
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## :star2: **New**

### Trusted VOD Access API Support

As part of the new [Trusted External User Video Access](doc:guest-portal-and-public-access-control#enable-trusted-access-for-external-viewers) feature this release, five new endpoints are available to manage the new functions programmatically.  They are:

- [Add Video External Access](ref:addvideoexternalaccess)
- [Delete Video External Access](ref:deletevideoexternalaccess)
- [Get Video External Access](ref:getvideoexternalaccess)
- [Renew Video External Access](ref:renewvideoexternalaccess)
- [Revoke Video External Access](ref:revokevideoexternalaccess)

Please note that you can use the endpoints to use this feature and in Rev at the same time. It must be enabled first.  View the topic [Manage External Access to Videos and Webcasts](doc:guest-portal-and-public-access-control) for complete details on trusted access.

In addition to new endpoints, the **enableExternalApplicationAccess** and **enableExternalViewersAccess** Boolean parameters have been added to the following existing endpoints in support this feature:

- [Upload Video](ref:uploadvideo-1)
- [Update Video Details/Metadata](ref:editvideo)
- [Patch Video Details/Metadata](ref:editvideopatch)
- [Get Video Details/Metadata](ref:getvideosdetails)

## :wrench: **Updated/Fixed**

### Get Rev IQ Credits

The [Get Rev IQ Credits Usage](ref:getaccountiqcreditsusage) API has been updated to now account for the credit used in the [summarization](doc:video-title-and-description#use-vbrick-generative-ai-to-add-a-video-description) and [video assistant](doc:vbrick-assistant) [Generative AI](doc:generative-ai-tools) tools.

### Download Video Update

To support the new video cloud storage optimization updates this release, the [Download Video](ref:downloadvideo) endpoint has been updated to immediately return 405 or 409 if a zip is necessary for download and one does not exist.  The zip is then created (following aging rules).  An email is sent when the download is ready with the URL. View the [December Release Notes](changelog:release-notes-v756-december-2023) for more details.

### Get User Status

You can now manage a user's status via our API.  You are able to view the user's **type** (SCIM, LDAP, etc.) and **status** (suspended, active, etc.) in the following endpoints:

- [Get User By ID](ref:getuser)
- [Get User by Username](ref:getuserbyusername)
- [Get User by Email](ref:getuserbyemailaddress)

### Set User Suspended Status

You are now able to manage a user's suspended status (or remove it) via the [Patch User](ref:edituserdetails) API.  This is done by passing the status of **Active** or **Suspended**.  Any other value returns an error.