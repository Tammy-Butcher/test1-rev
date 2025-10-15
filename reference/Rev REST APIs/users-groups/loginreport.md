---
title: Get Users By Login Date
excerpt: >-
  Get a list of users and their last login date. Users who have never logged in
  are not be returned.
api:
  file: rev-rest-apis.json
  operationId: loginReport
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
  "body": "If [Hide User Level Analytics](doc:hide-user-level-analytics) under the **Content Restriction** menu is enabled, this endpoint returns a 401 error."
}
[/block]