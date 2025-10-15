---
title: Change Log (v7.54)
excerpt: ':calendar: Date Added: August 2023'
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

### Get Public Webcast Status

*Rev Only*

The new [Get Public Webcast Status](ref:get_api-v2-scheduled-events-eventid-is-public) endpoint checks if a webcast is **Public** and returns true if it is.  A 401 error is returned if the event is **Private** for security reasons.  No authorization is required.
