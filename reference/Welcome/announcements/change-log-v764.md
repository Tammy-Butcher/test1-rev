---
title: Change Log (v7.64)
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
> 🚧 Important!
> 
> Per our [Rev v7.40 deprecation announcement](https://revdocs.vbrick.com/v7.40/reference/announcements), the Rev v1 API is being decommissioned and will no longer function as of the **Rev June 2025 Release**. If you have not already done so, please begin using the Rev v2 API _immediately_.

## :star2: **New**

### Channel Header Image Endpoints

There are two new endpoints for Channels that support the new Header image feature for channels.

The [Upload Channel Header Image](ref:uploadchannelheaderfile) endpoint allows you to upload an **ImageFile** for a specific **channelId** and the [Get Channel Header Image](ref:downloadheaderimage) endpoint allows you to specify a **headerKey** to download a previously uploaded Channel header. 

Both the **headerKey** and **headerURI** are new properties that are returned in the [Get Channels For User](ref:getuserchannels) and [Get Channels](ref:getchannels) endpoint(s) as of this release.

## :wrench: **Updated/Fixed**

### Channel Default Sort Order Updates

In addition to the new Header endpoints above for new Channel features, existing Channel endpoints have also been updated this release with the ability to specify a default sort order for videos in the channel using the **defaultSortOrder** parameter that is now available.

The following endpoints support this parameter:

- [Create Channel](ref:createchannel)
- [Update Channel](ref:editchannel)
- [Patch Channel](ref:patchchannel)
- [Get Channels](ref:getchannels)
- [Get Channels For User](ref:getuserchannels)

### Webcast Bumper and Trailer Setting Updates

Webcast endpoints have been updated in support of the new bumper (**preRollVideoId**) and trailer (**postRollVideoId**) settings that can now be [used with events during setup](doc:add-a-bumper-and-trailer-to-the-webcast-recording).

The following endpoints support these two parameters:

- [Create Webcast](ref:createevent)
- [Update Webcast](ref:editevent)
- [Patch Webcast](ref:patchwebcast)
- [Get Webcast Details](ref:getevent)

### Video Endpoint Updates

The **accessControlEntities** object in the [Get Video Details/Metadata](ref:getvideosdetails) response has been updated so that, if the user calling the endpoint is a **Channel Member**, the response returns _all_ the channels that the video is a part of. Previously, the response only displayed the video's channels when the user was a **Channel Contributor**.