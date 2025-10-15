---
title: Change Log (v7.40)
excerpt: ':calendar: Date Added: April 2021'
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

**Webcast Branding Support**

* [Upload Webcast Branding](ref:uploadwebcastbranding) New multi-part API for customizing the look and feel of an individual webcast with branding parameters. When the webcast is loaded by a user, the branding parameters are applied.

* The parameters are also returned by the [Get Webcast Details](ref:getevent) endpoint.

**External PATCH support** for editing a webcast per JSON patch specification added in the new [Partially Update a Webcast](ref:patchwebcast) endpoint.

## :wrench: **Updated/Fixed**

**Live Subtitle for Encoder-Sourced Events Support**

* The [Create Webcast](ref:createevent) , [Update Webcast](ref:editevent) , and [Start Webcast](ref:startevent) event endpoints now support live subtitles for encoder-sourced webcasts that use [Rev IQ-enabled presentation profile](doc:add-a-presentation-profile#rev-iq-enabled-presentation-profiles) video sources.

* To enable live subtitles on an encoder-sourced event via API, **transcription and translation** must be enabled, **Rev IQ credits** must be available, and the event must be using a Rev IQ enabled presentation profile.

**RTMP(S) Sourced Webcast Support**

* The [Create Webcast](ref:createevent) , [Update Webcast](ref:editevent) , and [Get Webcast Details](ref:getevent) endpoints now support **RTMP(S) sourced webcasts** including the ability to regenerate the RTMP URL and key needed when using the PUT method.
