---
title: Change Log (v7.62)
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

### Webcast Comments APIs

With this release is the ability to [moderate a Live webcast chat](doc:chat-module-management).  You can choose to hide a specific comment or mute a specific attendee and reverse both actions if you choose.  The comments log has been updated in support of this feature to include a new Hidden parameter which denotes if a comment has been hidden during the event.

- [Hide Webcast Comment](ref:hidewebcastcomment) and [Unhide Webcast Comment](ref:unhidewebcastcomment)
- [Mute Webcast Attendee](ref:mutewebcastattendee) and [Unmute Webcast Attendee](ref:unmutewebcastattendee)
- [Get Webcast Comments Log](ref:geteventcomments)

### Get Video Thumbnail Configuration

You can use the new [Get Video Thumbnail Configuration](ref:getvideothumbnailconfig) to return the video thumbnail sheet in grid view. Each thumbnail is indexed from left to right, then top to bottom. You are able to calculate the index, scaling value, and background style using the formulas provided with the endpoint.

### Get Deleted Videos

The new [Get Deleted Videos](ref:getdeletedvideos) endpoint returns a list of videos that have been deleted, made inactive, or made otherwise inaccessible to all users in the last 30 days.

### Channel Logos

You are now able to use the [Upload Channel Logo Image](ref:uploadchannellogofile) endpoint to upload an image file for a channel. Keep in mind, it must be an [accepted image type](doc:supported-file-types) or it will not be accepted and you must have permissions to upload to the channel.

## :wrench: **Updated/Fixed**

### Live Webcast Emoji Reactions Support

This release features the ability for Event Hosts to allow attendees to express how they feel about the content through the [use of emojis reactions in a Live Webcast](doc:add-live-emoji-reactions-to-a-webcast). 

We are also updating each of our event APIs to support this feature with the addition of a **reactionsSetting** object.  This object first allows you to enable the setting (it is defaulted to off) so that when it is true, you can set the list of emojis that will be available for the event through the **character** and name **parameters**.

The following endpoints support this feature:

- [Create Webcast](ref:createevent)
- [Update Webcast](ref:editevent)
- [Patch Webcast](ref:patchwebcast)
- [Get Webcast Details](ref:getevent)

There is a new [Get Webcast User Reactions Summary Report](ref:geteventreactions) that will detail the reactions used (and how many times) once an event has concluded.