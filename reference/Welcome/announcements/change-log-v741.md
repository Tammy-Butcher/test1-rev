---
title: Change Log (v7.41)
excerpt: ':calendar: Date Added: June 2021'
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

** Channels & Groups Patch Endpoints Added **

* Similar to existing patch endpoints in place, the [Patch Channel](ref:patchchannel) and [Patch Group](ref:patchgroup) endpoints allow you to partially update the details of a channel and/or group in Rev without the need to update details that are not changing.
   *  Similar to LDAP Users, there are some limitations with patching if the group is an **LDAP Group**.  Namely, only the roles in the group may be updated.  Whereas, Rev system groups may have both roles and users updated with the Patch endpoint.

** Get Groups **

The new [Get Groups](ref:getgroups) endpoint returns a list of all groups matching the entered query.  The response parameters returned include group Id, group name, and role Ids in the groups.  Pagination is supported.

** Get Group Details By ID **

The new [Get Group Details By ID](ref:getgroup) endpoint returns a group name, roles assigned, and the role Ids for a specified group Id.

## :wrench: **Updated/Fixed**

A video **source type** and relevant **source details** are now returned in the [Get Webcasts By Time Range](ref:geteventslist) endpoint. 

Video Source type returns when getting webcast details may include:
* Presentation Profile and ID
* Zoom and Zoom Meeting ID
* Webex and Webex Meeting ID
* RTMP/RTMPS
* SipAddress
* Microsoft Teams

**Uploader **information returned for a video has been expanded. The [Get Video Metadata](ref:getvideosdetails) endpoint now includes an **Uploader **section that contains:
  * First Name
  * Last Name
  * User ID
  * Username

The incorrect path for [Get Zone Devices](ref:getzonedevices)  has been fixed and now correctly displays **/api/v2/zonedevices**.