---
title: Change Log (v7.60)
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

### Live Webcast Banners API Support

Vbrick is revamping the attendee engagement push link functionality for v7.60 and introducing the new [Live Webcast Banner](doc:add-links-to-a-webcast) feature. This allows longer messages to be sent to attendees in addition to URL links.  Accordingly, the **Get Push Links** for a Webcast endpoints are now deprecated and new endpoints are being introduced.

The following endpoints are new for this release:

- [Get Banners for a Webcast](ref:getwebcastbanners)
- [Add Banners to a Webcast](ref:createbanner)
- [Set Banner Status](ref:setbannerstatus)
- [Update Banner for a Webcast](ref:updatebanner)
- [Delete a Banner for a Webcast](ref:deletewebcastbanner)

As a result, the following endpoints are now **deprecated**.  _Please update as soon as possible_.

- [Get Push Links for a Webcast](ref:getwebcastpushcontentlinks)
- [Add Push Links to a Webcast](ref:createpushcontentlink)
- [Set Push Link Status](ref:setpushcontentlinkstatus)
- [Update Push Links for a Webcast](ref:updatepushcontentlink)
- [Delete a Push Link for a Webcast](ref:deletewebcastpushcontentlink-1)

## :wrench: **Updated/Fixed**

### Generate Video Metadata During Video Upload

The [Upload Video](ref:uploadvideo-1) endpoint now includes the ability to auto generate metadata for a video with the postUploadActions object.  You must specifiy the auto generate actions to take after the upload is complete in the **metadataGenerationFields** array (title/tag/description/chapters/all metadata). 

The video must also have an English transcription or be transcribed after the upload is complete by using the **transcribeLanguageId** field.

### Enable Chapter Images By Default

A new boolean parameter is now present that specifies if chapter images for a video are shown or hidden by default (when chapter images exist). The **enableAutoShowChapterImages** parameter is now present in the following endpoints:

- [Patch Video Details/Metadata](ref:editvideopatch)
- [Update Video Details/Metadata](ref:updatevideo)
- [Get Video Details/Metadata](ref:getvideosdetails)

### Video Feature Parameter Default Updates

Three video boolean feature default settings were updated for the [Update Video Details/Metadata](ref:updatevideo) endpoint.  The three features below have now been updated and set to **false** by default.

- enableRatings
- enableDownloads
- enableComments