---
title: Change Log (v7.42)
excerpt: ':calendar: Date Added: August 2021'
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## :wrench: **Updated/Fixed**

Video endpoints have been updated to reflect the flexible [Video Access Control](doc:update-basic-video-settings#video-access-controls) model released with build v7.42.  This means that multiple **Users**, **Groups**, and **Channels **may now be specified in addition to the AllUsers and Public access types.  Updated APIs include:

  * [Upload Video](ref:uploadvideo) 
  * [Add Video Link](ref:createvideolink) 
  * [Update Video Details/Metadata](ref:editvideo) 
  * [Update Video Access Control](ref:editvideoaccesscontrol) 
  * [Patch Video Details/Metadata](ref:editvideopatch)

The [Get Video Details/Metadata](ref:getvideosdetails) endpoint has been updated significantly.  It now returns additional parameter details to include:

  * duration
  * whenModified
  * expiration (expiration object details if an expiration date/rule applied)
  * hasAudioOnly
  * source
  * videoConference > sipAddress
  * chapters
  * commentCount
  * ratingsCount
  * avgRating
  * instances (video instance details if applicable)
  * transcodeFailed
  * closedCaptionsEnabled
  * approval (approval object details if part of an approval process)