---
title: Change Log (v7.49)
excerpt: ':calendar: Date Added: October 2022'
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

### Webcast Content Embeds

*Rev Only*

New APIs are now available for the [Webcast Engagement Embed](doc:allow-webcast-engagement-embeds) feature release.  This feature allows you to embed content or URLs from third-party sites of your choice so that they function in a Rev webcast. API support includes:

* [Embed Webcast Engagement](ref:createembeddedcontentlink) - Creates a new embedded webcast engagement for a specific webcast. 

* [Set Embedded Engagement Status](ref:setembeddedcontentlinkstatus) - Activates or deactivates an embedded engagement link for Webcast. Activating a link makes it visible to attendees. Multiple embeds can be activated but only one at a time is activated each time the API is run. Additionally, the webcast must be in-progress for an engagement to be activated.

* [Get Embedded Engagements for a Webcast](ref:getwebcastembeddedcontentlinks) - Retrieves a list of *all* embedded webcast links for a specific webcast.  Also specifies if the links are active.

* [Update Embedded Engagement for a Webcast](ref:updateembeddedcontentlink) - Updates a (previously created) Embedded Webcast Engagement for a Webcast. You must specify both the webcast and the engagement Ids.

* [Delete Embedded Engagement for a Webcast](ref:deletewebcastembeddedcontentlink) - Deletes a (previously created) Embedded Webcast Engagement for a Webcast. You must specify both the webcast and the engagement Ids.

## :wrench: **Updated/Fixed**

### Webcast API Updates

Webcast APIs were updated in v7.48 to include the ability to add **Producer** as a **videoSourceType** and the corresponding **presenterIds**.  Those fields are now active with the release of [Producer](doc:producer-event-set-up) in v7.49.

Webcast APIs have also been updated with the **embeddedContent** object in support of the new [Webcast Engagement Embed](doc:allow-webcast-engagement-embeds) feature.  

Note that you can either [add a new engagement](ref:createembeddedcontentlink) to an event or [update an engagement](ref:updateembeddedcontentlink) that has been previously created directly in the webcast itself using the same parameters found in the new **Embed APIs** above.

The following APIs are updated for both of these updates:

* [Create an Event](ref:createevent) 
* [Update Webcast](ref:editevent)
* [Patch Webcast](ref:patchwebcast)
* [Get Webcast Details](ref:getevent)
* [Get Webcasts By Time Range](ref:geteventslist)

### Viewer ID Content Restriction Updates

**Webcast** and **Video** APIs have been updated with the new **viewerIdEnabled** parameter.  The default value is false.  When set to **true**, viewer information is displayed over the video for playback on the web.  View the [Viewer ID Content Restriction](doc:viewer-id-content-restriction) topic update for more details.

Webcast APIs updated with viewerIdEnabled:

* [Create Webcast](ref:createevent)
* [Update Webcast](ref:editevent) 
* [Patch Webcast](ref:patchwebcast) 
* [Get Webcast Details](ref:getevent) 

Video APIs updated with viewerIdEnabled:

* [Upload Video](ref:uploadvideo) 
* [Update Video Details/Metadata](ref:editvideo) 
* [Patch Video Details/Metadata](ref:editvideopatch) 
* [Get Video Details/Metadata](ref:getvideosdetails) 

### Video Upload Updates

The [Upload Video](ref:uploadvideo) endpoint is now able to send large video files in chunks that can be uploaded over multiple sessions.  The **Content-Range** header specifies the start and end range chunks and includes the total size.  Video processing only begins once the final chunk is received.  Video status is also returned when the last chunk is received.
