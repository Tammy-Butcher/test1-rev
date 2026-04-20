---
title: Get Video Report
excerpt: >-
  This endpoint returns detailed viewing information for one or more videos. The
  report includes individual video viewing sessions, along with information on
  whether each user completed the video.<p>If video Ids are not specified in the
  call, the response includes data for every video in your Vbrick account.
  Maximum duration for a reporting period is 31 days.
api:
  file: rev-rest-apis.json
  operationId: postVideoReport
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> ❗️ Warning!
>
> If [Hide User Level Analytics](doc:hide-user-level-analytics) under the **Content Restriction** menu is enabled, this endpoint returns a 401 error.