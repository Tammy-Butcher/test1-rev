---
title: Change Log (v7.45)
excerpt: ':calendar: Date Added: March 2022'
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

### Delete Video Transcription Files

You now have the ability to [Delete Video Transcription Files](ref:deletetranscriptionfiles). You can specify an individual transcription file associated with a video by its specific language Id (locale) or delete all transcription files associated with the video.

### Reboot a DME

This new endpoint allows you to [Reboot a DME](ref:rebootdmedevice).  It functions exactly as the reboot command performs in Rev's UI and allows you to specify an individual DME to reboot.

## :wrench: **Updated/Fixed**

### Get Video oEmbed

The [Get Video oEmbed](ref:oembed) endpoint has been updated to accept the formatting of Rev's **Shared URL** as input to the **url** query parameter.

### Get Webcast Attendee Reports

Webcast reports have been updated so that you can view the aggregated real-time health metrics of your events. For example, if errors or buffering on a given event climb above a certain threshold, you are able to automate certain actions. 

The [Get Webcast Attendees Report](ref:getposteventsessions) and [Get Webcast Attendees Realtime](ref:getrealtimeattendeessearchrequest) have been updated to include the following aggregated, single value, event metrics:

* Experienced Rebuffering (%)
* Average Experienced Rebuffer Duration 
* Experienced Errors / Attendees 
* Multicast Errors (average, same as in UI)

> 📘 Note
>
> These are event-level metrics and do not change based on Search criteria.  For example, a search on users with just "Kyle" returns stats for the event, not just "Kyle".

The [Get Webcast Attendees Report](ref:getposteventsessions) response now includes the following responses at the top of the response body:

* hostCount
* moderatorCount
* attendeeCount
* Additionally, the existing totalsessions object has also been moved to the top of the response

### Get Webcast Poll Report

The [Get Webcast Poll Report](ref:geteventpolls) now includes the date and time that a poll was created in the **whenPollCreated** parameter.
