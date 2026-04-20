---
title: Convert Dual Stream to Switched (Single) Stream
excerpt: >-
  Converts a dual-stream video to a switched-stream (single) video. This
  endpoint only works for dual stream videos. <p>When you run this API, the MP4
  switched-stream version is marked as the original and the HLS switched-stream
  version remains.</p><p>The HLS dual-stream version is deleted.</p><p>The
  <strong>hasDualStreams</strong> and <strong>isConvertedToSwitched</strong>
  parameters are updated accordingly in the [Get Video
  Details/Metadata](/reference/getvideosdetails) and [Search
  Video](/reference/searchvideo) endpoints.</p>
api:
  file: rev-rest-apis.json
  operationId: convertDualStreamToSwitchedStream
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---