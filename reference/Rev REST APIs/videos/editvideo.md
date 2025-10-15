---
title: Edit a Video
excerpt: >-
  This endpoint allows you to edit and replace a video based on a list of
  supplied clips.  Each clip (an object within clips) defines start and end
  times within the video. The end result is a new video concatenating the clips
  (from the original video). This endpoint replaces the <a
  href=/reference/trimvideo>trim video</a> API which is now deprecated as a
  result.</br>
api:
  file: rev-rest-apis.json
  operationId: editVideo
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 📘 Note
>
> Once this endpoint is complete, you can then use additional APIs to update the video clips as needed. For example:
>
> * [Update](ref:uploadvideochaptersupdate) or [delete](ref:deletevideochapters) video chapters
> * [Upload](ref:uploadtranscriptionfiles-1) , [transcribe](ref:transcribevideo) , or [translate](ref:translatevideo) video
> * Apply user tags with [tag users in a video](ref:tagusersinvideo)
