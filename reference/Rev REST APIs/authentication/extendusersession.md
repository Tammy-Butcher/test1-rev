---
title: Extend Login Session for All Authentication Methods
excerpt: >-
  Extends the current user login session regardless of the authentication method
  used. This includes preventing user API key sessions and JWT authentication
  sessions from timing out. Successful completion returns a new expiration date
  and time which then expires the session at that new date and time.
api:
  file: rev-rest-apis.json
  operationId: extendUserSession
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---