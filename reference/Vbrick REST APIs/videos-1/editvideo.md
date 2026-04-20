---
title: Edit a Video
excerpt: >-
  This endpoint allows you to edit and replace a specified video based on a list
  of supplied clips. Each clip is defined by the start and end parameters and
  applied to the videoId you specify. Multiple clips can be defined.<br><br>Be
  aware that this is a destructive process and you may wish to create a copy of
  the original video <em>before</em> applying changes with this endpoint.
  Meaning, the end result is a <em>new</em> video with the same videoId combined
  from all the concatenated video clips from the original video. Any video not
  acessible is ignored in the concatenation process.<br><br>Note that if you
  edit a video that has transcripts, those trascripts may be out of sync with
  the video and will need to be regenerated.<br><br>This endpoint replaces the
  [Trim Video](/reference/trimvideo) API which is now deprecated as a
  result.</br>
api:
  file: rev_v2_openapi.json
  operationId: editVideo
hidden: false
---