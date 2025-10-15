---
title: Change Log (v7.53)
excerpt: ':calendar: Date Added: June 2023'
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## :wrench: **Updated/Fixed**

### Playlist API Updates

The [Get Playlists](ref:getplaylists) API now returns the playlist owner and profile image in the response.  This is included when returning a standard playlist and the featured playlist.  The new fields returned are:

- **ownerFullName**
- **ownerProfileImageUri**

The [Update Playlist](ref:editplaylist) and [Update Featured Playlist](ref:editfeaturedplaylist) body parameters were being incorrectly documented resulting in a 500 exception. This has been corrected and the **videoId** and **action** fields are now correctly added in a **playlistVideoDetails** object.

### User Avatar Updates

The following APIs now return a **profileImageURI** field so that an avatar can be displayed alongside the entities returned.

- [Get User By Username](ref:getuserbyusername)
- [Get User By Email](ref:getuserbyemailaddress)
- [Get User By ID](ref:getuser)
- [Search Users, Groups, and Channels](ref:searchaccessentity) Note: When **type** is equal to **user**.

### Role API Updates

There is a new key added to the [Get Roles](ref:getroles) API response called **roleType**. The associated value is the enum role type. This is to provide a definitive indicator of the role type referenced in the list.  Available values are those [roles currently allowed](doc:roles-and-permissions) in Rev.

### Zone API Updates

The [Get Zones](ref:getzones) API return was returning an empty successful response.  This has been corrected and the response now returns correctly.