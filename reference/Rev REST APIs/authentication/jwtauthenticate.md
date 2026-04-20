---
title: JWT Authentication
excerpt: >-
  This authentication API endpoint is used to authenticate individual user using
  a JWT token. Use the token that is returned in the response as the
  Authorization to run other public APIs. Once a session is established using
  this endpoint, subsequent API calls that uses the token returned from this
  endpoint will be limited according to the role and privileges of this
  particular user. Using this method, the user via API will have the same
  privileges and roles that user has when they login to Vbrick UI. This
  authentication mechanism can be used to automate Vbrick workflows using role
  and privileges of a given user.</br></br>Account Admins can generate user’s
  API Key and Secret combination. Secret is only visible at the time of
  generation. API Key and Secret combination can be regenerated and deleted. The
  key will not work for suspended users. Also authenticating a user using this
  method will consume a user license if the user is unlicensed
api:
  file: rev-rest-apis.json
  operationId: jwtauthenticate
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---