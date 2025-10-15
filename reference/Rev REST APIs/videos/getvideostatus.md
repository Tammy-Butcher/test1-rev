---
title: Get Video Status
excerpt: >-
  This endpoint retrieves the current status of a specific video during upload
  and when upload is complete. To know whether a video is fully processed,
  including transcoding, use the field <b>isProcessing</b> along with with
  <b>status</b> state that is returned in the response. <p>For example, if the
  value of <b>isProcessing</b> is FALSE and the status is <b>Ready</b>, then the
  video has been fully processed. If the value of <b>isProcessing</b> is TRUE
  and status is <b>Ready</b>, then it means the video is available for playback
  but the transcoding process is still in progress.</p><p>The progress of the
  overall processing of the video can be tracked using the field
  <b>overallProgress</b> whose value ranges from 0.0 to 1.0 where 1.0 means that
  the processing is 100% completed.</p><p>Possible status states during upload:
  [NotUploaded, Uploading, UploadingFinished, Ingesting,
  Processing]</p><p>Possible final status states once upload is complete:
  [Canceled, UploadFailed, ProcessingFailed, Ready,
  ReadyButProcessingFailed]</p>
api:
  file: rev-rest-apis.json
  operationId: getVideoStatus
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---