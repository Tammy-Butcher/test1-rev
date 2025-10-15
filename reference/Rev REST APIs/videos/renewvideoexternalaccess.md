---
title: Renew Video External Access
excerpt: >-
  This endpoint immediately revokes the current access and generates a new
  access link and expiration date (if one is in effect). It then emails the
  user(s) with the new link.
api:
  file: rev-rest-apis.json
  operationId: renewVideoExternalAccess
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
> The default expiration date for **Trusted External Access** is 14 days.  You can change this amount in Rev. Any status can be renewed: **Active**, **Expired**, or **Revoked**.
>
> View: [Manage External Access to Videos and Webcasts](doc:guest-portal-and-public-access-control) for more details.
