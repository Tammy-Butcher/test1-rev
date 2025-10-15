---
title: Change Log (v7.63)
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

### Get Video Thumbnail Sheet

The [Get Video Thumbnail Sheet](ref:downloadthumbnailsheet) is a new endpoint that is now returned by the [Get Video Thumbnail Configuration](ref:getvideothumbnailconfig) endpoint.  It replaces the non-API URL that was returned previously.

## :wrench: **Updated/Fixed**

### Featured Event API Support

There is a new **isFeatured** Boolean parameter that allows Event Admins to mark a webcast as a [Featured Event](doc:create-a-featured-event). The default value is false. When marked true, the event displays in [Featured Content](doc:customize-the-featured-video-playlist#choosing-featured-content) areas if enabled in **Branding**.  The endpoints affected include:

The following endpoints support this feature:

- [Create Webcast](ref:createevent)
- [Update Webcast](ref:editevent)
- [Patch Webcast](ref:patchwebcast)
- [Get Webcast Details](ref:getevent)
- [Get Webcasts By Time Range](ref:geteventslist)
- [Search Webcasts By Custom Field or Date Range](ref:searchwebcasts)

### Audio Track Generation Support

You can [generate audio tracks using Rev IQ](doc:manage-audio-tracks-for-a-video) if you have the appropriate permissions using the new **audioTracks** object.  

For example, setting the **status** field in this object to `adding` will generate a new audio track for the specified video while setting it to `updating` will update the previously added track. Setting the field to `deleting` will delete a previously associated audio track. For existing tracks or when using a **Get** endpoint, the field returns status information such as `ready`, `pending`, `processing`, etc.

You also have the option to specify if the track is the default audio using **isDefault** and supported languages using **languageID**.  The following endpoints are able to use these values and objects:

- [Update Video Details/Metadata](ref:updatevideo)
- [Patch Video Details/Metadata](ref:editvideopatch)
- [Get Video Details/Metadata](ref:getvideosdetails)

The [Get Rev IQ Credits Usage](ref:getaccountiqcreditsusage) endpoint has been updated so that Account Admins can now track audio translation updates and the credits used for them as we do with other Rev IQ usage parameters.  A **Usage** type equal to **AudioGeneration** is returned for audio translation tracking actions.