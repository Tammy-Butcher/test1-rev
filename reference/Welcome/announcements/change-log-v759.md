---
title: Change Log (v7.59)
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

### Rev Video Editor API Support

Vbrick is revamping the [Rev Video Editor](doc:edit-a-video-clip) this release and introducing new features to make editing videos easier and more efficient.  As part of this, the following API changes have been made:

* A new [Edit Video](ref:editvideo) endpoint is available. This endpoint allows you to edit a video based on a list of supplied clips you intend to keep.  After the edit API is complete, you can then use the additional APIs to update the chapters, subtitles, transcriptions, translations, or user tags in videos as needed.
* The [Trim Video](ref:trimvideo) endpoint is deprecated as a result of the new edit video endpoint above.

## :wrench: **Updated/Fixed**

### Generate Video Metadata

The [Generate Video Metadata](ref:generatevideometadata) endpoint that was added last release now also includes the ability to auto generate **chapters** for a video. It continues to function the same in that you must specify the video Id and the field type you want to generate (title/tag/description/chapters/all metadata). If you specify **all**, all fields are generated and not the individual types.

### Zone API Updates

A new **fallbackToSource** parameter has been added to the specific Zone endpoints noted below. This parameter is a Boolean that, when true, allows viewers to fallback to Source (if available) for unicast playback if [distribution modalities](doc:vbrick-distribution-modalities) fail.

* [Add Zone](ref:createzone) 
* [Update Zone](ref:editzone) 
* [Get Zones](ref:getzones) 

### Get Rev IQ Credit

The [Get Rev IQ Credits](ref:getaccountiqcreditsusage)  response now includes **MetadataGeneration** as a possible transaction type for **Usage** if applicable.

* The description for the endpoint has been updated to clarify how it functions.  This is a documentation change only.
