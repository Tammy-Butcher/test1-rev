---
title: Change Log (v7.50)
excerpt: ':calendar: Date Added: December 2022'
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

### Webcast Attendee Engagement / Push Links

*Rev Only*

This release includes a new webcast attendee engagement feature that allows hosts to push link (URLs) to their attendees during a live event.  New API support for the [Add Links to a Webcast](doc:add-links-to-a-webcast) feature include:

* [Add Push Links to a Webcast](ref:createpushcontentlink) - This endpoint allows you to add push content links. These can be shown in a Rev webcast player at end of webcast or during webcast is in progress by specifying the type and if a manual link isEnabled.

* [Update Push Links for a Webcast](ref:updatepushcontentlink) - Updates previously created push links for a Webcast. You must specify both the webcast and the link Ids.

* [Activate a Push Link](ref:setpushcontentlinkstatus) - Activates or deactivates a push content link for webcast. Only Manual type links can be activated/deactivated. Activating a link makes it visible to attendees.

* [Get Push Links for a Webcast](ref:getwebcastpushcontentlinks) - Retrieves a list of all push content links for a specific webcast.

* [Delete a Push Link for a Webcast](ref:deletewebcastpushcontentlink) - Deletes previously created push links for a Webcast. You must specify both the webcast and the link Ids.

### Webcast Video Source / Producer Event Addition

*Rev Only* 

The [Resend Email to External Presenter](ref:resendexternalpresenteremail) endpoint will trigger email notifications for an individual [Guest presenter](doc:producer-settings) as needed for the new Guest presenter feature in Producer events. 

### Trim Video

A new [Trim a Video](ref:trimvideo) endpoint is now available that allows you to enter timestamp segments in a video clip to trim it via API.  Use the start and end time values to trim video in timespan format (e.g. 00:00:00). Minutes and seconds should be from 0-59.  Two values are equal to min/second while three values = hour/min/second.  Note that you may not trim live videos or videos that are in process.

## :wrench: **Updated/Fixed**

### Webcast API Updates

Webcast APIs were updated in v7.50 to allow for the [Add Links to a Webcast](doc:add-links-to-a-webcast) feature to be added and managed.  Events can also be configured via API to allow for [Guest presenters](doc:producer-settings) in Producer events that were introduced in the last release of Rev Cloud.  

The following webcast APIs include the [Push Link](doc:add-links-to-a-webcast) updates:

* [Create Webcast](ref:createevent) 
* [Update Webcast](ref:editevent) 
* [Get Webcast Details](ref:getevent) 

All three Get webcast APIs return the [Guest Presenter](doc:producer-settings) functionality for Producer events:

* [Get Webcast Details](ref:getevent) 
* [Get Webcasts By Time Range](ref:geteventslist) 
* [Search Webcasts By Custom Field or Date Range](ref:searchwebcasts) 

### Zone API Updates

Zone APIs have been updated for the new [Rendition Selection](doc:automatic-multicast-and-reflection) feature with this release.   Note that at least one rendition must be selected.  APIs that reflect this change include:

* [Add Zone](ref:createzone) 
* [Update Zone](ref:editzone) 
* [Get Zone Devices](ref:getzonedevices) 
* [Get Zones](ref:getzones) 
* [Delete Zone](ref:deletezone)
