---
title: Change Log (v7.44)
excerpt: ':calendar: Date Added: December 2021'
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

### Delete Video Supplemental Files

Rev v7.44 adds the ability to [Delete Video Supplemental Files](ref:deletevideosupplementalfiles). You can specify an individual supplemental file to delete or delete all supplemental files associated with the video.

## :wrench: **Updated/Fixed**

### Get Webcast Comments Log

The [Get Webcast Comments Log](ref:geteventcomments) endpoint response now supports pagination.  Two query parameters have been added to facilitate this; **scrollId** and and an optional **size** (count) to specify the number of results returned.
  * Example: If **totalComments** > **Count/Size**, then provide the **scrollId** returned from the first request to get the next set of comments (e.g. scrollId=n)

### Granular Role API Updates

Rev v7.44 introduces the concept of [Granular Roles and Permissions](doc:roles-and-permissions#granular-roles-and-permissions). Rev Granular roles are used to grant specific permissions to an account while restricting other functions that are normally packaged with the role. This has implications for Vbrick's API as well. 

#### Internal Event Host / Internal Media Contributor Roles

Internal roles are restricted from setting ACL controls to **Public** with regard to video or webcasts.  Unauthorized exceptions are returned if this is attempted.  
[block:parameters]
{
  "data": {
    "h-0": "Endpoint",
    "h-1": "Role / Restriction",
    "0-0": "<ul>\n<li>[Create Webcast](ref:createevent) \n<li>[Update Webcast](ref:editevent) \n<li>[Patch Webcast](ref:patchwebcast)\n</ul>",
    "0-1": "The **Internal Event Host** role (that does not also have the Event Host, Event Admin, or Account Admin roles in addition to this role) may *not* set the event to **Public**. \n\nThe role may edit an existing event *only* if they are the Internal Event's Host/Event Host (or an Event Admin).\n\nAn unauthorized error is returned if this is attempted.",
    "1-0": "<ul>\n<li>[Upload Video](ref:uploadvideo) \n<li>[Update Video Details/Metadata](ref:editvideo) \n<li>[Update Video Access Control](ref:editvideoaccesscontrol) \n<li>[Patch Video Details/Metadata](ref:editvideopatch)\n</ul>",
    "1-1": "The **Internal Media Contributor** role (that does not also have the Media Contributor, Event Host, Event Admin, Media Admin, or Account Admin in addition to this role) may *not* set a video to **Public**. \n\nThat means, this role *restricts* the ability to make videos and recordings **Public** even when granted edit permissions by another user account.\n\nThis role may edit a Public video in this case but it may *not* change a Private video to Public.\n\nAn unauthorized error is returned if this is attempted."
  },
  "cols": 2,
  "rows": 2
}
[/block]
#### Rev IQ Role

All [Rev IQ](doc:rev-ai) features and functions are now restricted to accounts that have this role.
[block:callout]
{
  "type": "success",
  "title": "Tip",
  "body": "All Admin accounts include the **Rev IQ** functions."
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Endpoint",
    "h-1": "Role / Restriction",
    "0-0": "<ul>\n<li>[Create Webcast](ref:createevent) \n<li>[Update Webcast](ref:editevent) \n<li>[Patch Webcast](ref:patchwebcast)\n</ul>",
    "0-1": "Only the Rev IQ role may **Set Live Subtitles to True** when using the webcast endpoints going forward.\n\nAn unauthorized error is returned if this is attempted and the Rev IQ role is not in place.",
    "1-0": "[Transcribe Video](ref:transcribevideo)",
    "1-1": "Only the Rev IQ role can use this endpoint as of v7.44.  This only applies if serviceType = Vbrick.\n\nAn unauthorized error is returned if this is attempted and the Rev IQ role is not in place.",
    "2-0": "[Translate Video](ref:translatevideo)",
    "2-1": "Only the Rev IQ role can use this endpoint as of v7.44. \n\nAn unauthorized error is returned if this is attempted and the Rev IQ role is not in place.",
    "3-0": "[Tag Users in Video](ref:tagusersinvideo)",
    "3-1": "Only the Rev IQ role can use this endpoint as of v7.44. \n\nAn unauthorized error is returned if this is attempted and the Rev IQ role is not in place."
  },
  "cols": 2,
  "rows": 4
}
[/block]
## :+1: Partner Account Updates

### End Webcast API Enhancements

Partner accounts can now delay the true ending of a webcast through the use of a new **gracefulEnd** parameter. 

This parameter is available on the [End Webcast](ref:endevent) and [Stop Broadcasting Webcast](ref:pausebroadcastevent) endpoints. It is used to ensure that attendees do not receive the end command before the end of their segment/buffer is reached.  

For now, **gracefulEnd** is only available to Partner accounts.