---
title: Change Log (v7.38)
excerpt: ':calendar: Date Added: December 2020'
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

* **Post/Put/Get** endpoints for video [Chapters](https://rev.readme.io/reference#uploadvideochapters) have been added.  Multiple chapters may be added to a video and this includes the ability to add images to a chapter.

* Introduction of [Secure Category](https://rev.readme.io/docs/add-categories#create-a-secure-category) API endpoint support which includes updates to the [Category](https://rev.readme.io/reference#createcategory) APIs and the ability to add and edit restricted categories.
   * The **Post/Put/Patch** endpoints for Video and Webcast have also been updated to note that an error is generated if you attempt to add or edit restricted categories on these endpoints without contribute rights.

## :wrench: **Updated/Fixed**

* **Webcast **endpoints updated with a new [Get Webcast Attendees Realtime](https://rev.readme.io/reference#getrealtimeattendeessearchrequest) endpoint to retrieve a real-time attendees list (user-session) and analytics for a running Webcast.