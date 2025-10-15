---
title: Get Webcast Attendees Report
excerpt: >-
  Get attendees for a completed webcast. You may specify Pre-Production versus
  Main Event.
api:
  file: rev-rest-apis.json
  operationId: getPostEventSessions
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
[block:callout]
{
  "type": "danger",
  "title": "Warning!",
  "body": "If [Hide User Level Analytics](doc:hide-user-level-analytics) under the **Content Restriction** menu is enabled, this endpoint returns a 401 error. Totals are returned but the session array is not."
}
[/block]