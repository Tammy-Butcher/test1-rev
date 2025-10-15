---
title: Change Log (v8.1)
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## :wrench: **Updated/Fixed**

### RTMP Stream Redundancy Support

Webcast endpoints that include RTMP event information now support [RTMP stream redundancy](doc:rtmprtmps-event-set-up) and the creation of a **Backup Stream** with the Boolean parameter **secondarySourceEnabled**. This parameter can be set to true when the **videoSourceType** is set to RTMP.

When enabled, the **secondaryRTMP url** and **key** are displayed but toggling between the two streams is *not* available through the API and can only be done through Rev's UI. 

The endpoints updated are:

* [Create Webcast](ref:createevent)
* [Update Webcast](ref:editevent)
* [Patch Webcast](ref:patchwebcast)
* [Get Webcast Details](ref:getevent)
* [Get Webcasts By Time Range](ref:geteventslist)
