---
title: Change Log (v7.55)
excerpt: ':calendar: Date Added: October 2023'
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

### Get Video Summary Statistics

_For Rev and Vbrick Distribution_

The new [Get Video Summary Statistics](ref:getvideosummary) endpoint returns the summary statistics of a given video such as total views, completion rate, unique views, and so forth. You can specify an optional before and after date range or return the entire summary by leaving the before and after dates blank. You must have **edit rights** to the video or have the **VOD Analyst** role.

### Get Video Report

The new [Get Video Report](ref:postvideoreport) endpoint returns detailed viewing information for up to 50 videos per query.  It includes individual viewing sessions and also specifies if each user completed the video. If individual video Ids and date range are not specified, the response includes data for every video in your Rev account. The maximum duration for a reporting period is 31 days. Note that the current **Get Video Report** endpoint continues to work at present but has been deprecated.

## :wrench: **Updated/Fixed**

### Start Video Conference Recording

The [Start Video Conference Recording](ref:startrecording) endpoint has been updated with an **audioOnly** parameter.  This optional Boolean is _false_ by default.  When true, only the audio is recorded and an mp4 and HLS version is provided for playback.  Keep in mind this will be an audio-only recording and no other video assets are provided (such as thumbnails).