---
title: Change Log (v7.57)
excerpt: ''
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

### Get Playlist with Video Details

The new [Get Playlist with Video Details](ref:getplaylistdetails) returns a specified playlist and includes all the videos that are part of the playlist.  It also returns the **playlist type** (static or dynamic), the **video count**, **playback URL**, and details of the search query if it is a dynamic playlist. You must have access to view the playlist or an error is returned.

### Convert Dual Streams to Switched (Single) Streams

Account Admins can now manage and reduce storage needs by deleting dual stream version videos and forcing switched streams to be the default version through the [Convert Dual Stream to Switched Stream](ref:convertdualstreamtoswitchedstream) endpoint. Note that this API only works for dual stream videos.  When you run this API:

* The **MP4 switched stream** version is marked as the original
* The **HLS switched stream** version remains
* The **HLS dual stream** version is deleted
* Two new parameters are updated:
  * The **hasDualStreams** parameter is updated to False
  * The **isConvertedToSwitched** parameter is updated to True
  * These flags are updated accordingly in the [Get Video Details/Metadata](ref:getvideosdetails) and [Search Videos](ref:searchvideo) endpoints.
  * They have also been added to the [Video Inventory](doc:view-video-reports#download-video-inventory-report) report download.

### Get Video Unique Sessions Report

The [Get Video Unique Sessions Report](ref:uniquevideosessionsreport) API returns detailed viewing information for a video.  It is limited to one session per user within a given time range.  It reports the **individual viewing session with the maximum viewing time** for each user who watched the video, and whether or not each user **completed** the video. Up to 500 responses can be generated with supported scrolling. Guest user sessions are only reported for authenticated guests.

### Search Assignable Users, Groups, and Channels

The [Search Assignable Users, Groups, and Channels](ref:searchaccessentityassignable) API searches and returns a list of specified access entities (user/group/channel) that the user has access to assign. The list is filtered by type and is returned alphabetically by first name, group name or channel name. You can specify a type (or leave blank to return all types) and use a query string (or leave it blank to perform a blank search).

## :wrench: **Updated/Fixed**

### Dynamic Playlist Support

[Dynamic Playlists](doc:playlists#dynamic-playlists) are available as of v7.57 with current playlist functionality remaining the same and renamed to **Static Playlists**. API support for Dynamic Playlists includes the following updates:

* A new parameter **type** that can = **static** or **dynamic**. The default is static and all existing playlists are static.
* When type = **dynamic**, a new field is used to define the dynamic playlist criteria called: **playlistDetails**. 
* The [Add Playlist](ref:createplaylist), [Update Playlist](ref:editplaylist), and [Get Playlists](ref:getplaylists) endpoints have been updated to reflect these updates.
