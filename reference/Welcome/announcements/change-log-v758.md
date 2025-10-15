---
title: Change Log (v7.58)
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

### Generate Video Metadata

Included as part of Vbrick’s new **Generative AI** [Video Metadata Generation](doc:video-metadata-generation) tool this release are two new endpoints have been added to our API that allow you to programmatically generate tags, titles, and descriptions (or all metadata at once) for a video just as you can in Rev's UI. 

[Generate Video Metadata](ref:generatevideometadata) - You must specify the video Id and the field type you want to generate (title/tag/description/all metadata). If you specify **all**, all fields are generated and not the individual types.

The following requirements must be met:

- Metadata generation feature must be enabled for the account (Metadata Generation is not enabled for this account returned)
- Sufficient Rev IQ credits in place (Insufficient Rev IQ credits returned if not met) 
- The user must have Rev IQ user rights (Insufficient rights if not met)
- The user must have edit access rights to the video. (Unauthorized error if not met)
- An English transcript is required (<language> transcript required returned if not met)

[Get Video Metadata Generation Status](ref:getmetadatagenerationstatus) - This endpoint allows you to see whether a video/language combination metadata generation has been processed. It returns timestamp(s) of when the request was submitted and completed.  The status returns can be: NotStarted, InProgress, Success, and Failed.

## :wrench: **Updated/Fixed**

### Transcribe Video

You can now use the [Transcribe Video](ref:transcribevideo) endpoint on a video with multiple audio tracks. There is a new (optional) **audioTrack** field that will transcribe the specified audio track.  If the audioTrack parameter is not specified (left null), the video is transcribed in the **default track** instead. If there is no audio track that matches the one specified in audioTrack, an error is returned.

### Audio Track Management in Video Details Endpoints

You can now manage multiple audio tracks in video details endpoints:

[Get Video Details/Metadata](ref:getvideosdetails)  - This endpoint now returns the array of audio tracks and includes the track, language, whether it is the default or not, and its audio track status.

[Update Video Details/Metadata](ref:editvideo)  - You can now update the video language in this endpoint by audio track. If the language passed is supported by our player language mapping, the language will display in the player.

[Patch Video Details/Metadata](ref:editvideopatch) - Now accepts multiple audio tracks using "track" and "languageId".

Note that you cannot change the order of tracks nor the default audio track.

Errors are returned for the following:

- An invalid language code is passed
- The language set is undetermined
- An invalid id or the wrong number of audio languages (for update) is set