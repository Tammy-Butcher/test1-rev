---
title: Change Log (v7.46)
excerpt: ':calendar: Date Added: April 2022'
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## :star2: **New**

### OAuth2 with PKCE Support

Rev APIs now support [OAuth2 Authorization](ref:authorize) with fully compliant PKCE support.  As a result, previous [OAuth Authorization](ref:authorization) and [OAuth Access Token](ref:token) endpoints are now deprecated.

### Search Suggestions for Videos

The new [Search Suggestions for Videos](ref:searchsuggestedvideos) API allows you to enter a string of 2-15 characters to return video search suggestions (up to 10) based on that string.  The suggestions returned all begin with the string entered and results directly mimic using the **Rev UI** search bar.

### Get User Pending Completion Videos

The [Get User Pending Completion Videos](ref:getcontinuewatchingvideos) endpoint allows you to provide the ability to resume watching a video(s) for a user by retrieving the user's pending completion videos.  This endpoint retrieves a list of video details (up to an array of 18) that the user paused while watching.  To retrieve the status of a specific video for a user, use [Get User Pending Completion Status By ID](ref:getcontinuewatchingvideo) instead.

### Get User Pending Completion Status By ID

The [Get User Pending Completion Status By ID](ref:getcontinuewatchingvideo) retrieves the Pending Completion status of a specific video for a user and is used along with [Get User Pending Completion Videos](ref:getcontinuewatchingvideos) to provide **Continue Watching** suggestions.  A **timestamp** and a **session Id** are returned.

### Get Video Playback URLs

The [Get Video Playback URLs](ref:getvideoplaybackurls) returns a list of **playback URLs** for a given video Id that account for **Zone** logic.  Note that this endpoint is different than the previously named Get Video Playback URL which is used for *embedding* purposes only.  

To avoid confusion between the two, the embedding API has now been renamed to: [Get Video Embed Playback URL](ref:getvideoplaybackurl).

### Get Video Thumbnail By ID

[Get Video Thumbnail By ID](ref:downloadthumbnailfile) is similar to the [Download Video Thumbnail](ref:downloadvideothumbnailfile) API in that it returns a **thumbnail image** for a video.  The difference is that for **Get Video Thumbnail** you need to specify the Video Id.  You do *not* need to retrieve and use a thumbnail **key**.

Note that if **Allow Sharing of Metadata for Private Videos** is disabled in **System Settings**, or if the user does not have view access, a default image is returned.

### Get Video Feature Settings

[Get Video Feature Settings](ref:getvideofeatures) returns all the account-level video settings and features that are available and/or enabled for videos in your Rev portal, including any custom settings.  If you specify a video Id, it returns the features and settings that are applied for just that video.  You must have edit rights to return a specific video's features, otherwise you must have Media Admin rights or above to use this endpoint.

### Get Channel Logo

[Get Channel Logo](ref:downloadthumbnail) allows you to download a Channel's logo.  

It requires a channel's **logoKey** from the [Get Channels](ref:getchannel) and/or [Get Channels For User](ref:getuserchannels) API.

## :wrench: **Updated/Fixed**

### Search Videos

The [Search Videos](ref:searchvideo) API now allows you to enter an optional **Channel Id** parameter to filter returns based on specific channels.  You must have permissions to that channel to search returns by channel.

### Get Video Embed Playback URL

[Get Video Embed Playback URL](ref:getvideoplaybackurl) was previously named **Get Video Playback URL**.  It has been renamed to better identify its embedding purpose and to avoid confusion with the new zone playback URL endpoint mentioned above.

### Get Webcast Playback URLs

The [Get Webcast Playback URLs](ref:getplaybackurl) response has been updated to include a **jwtToken** that can be used when sending analytics events. It is valid for 24 hours.

### Get Category By ID

The [Get Category By ID](ref:getcategory) response has updated to include a count of **activeVideos**, **inActiveVideos**, and **totalVideos** for that category.

### Get Channels

The [Get Channels](ref:getchannel) and [Get Channels For User](ref:getuserchannels) endpoints have been updated to include the channel **logoKey**, **logoUri**, **headerBackGroundColor**, and **headerFontColor** in the response returned.
