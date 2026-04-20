---
title: Update Video Access Control
excerpt: >-
  This endpoint edits the Access Control permissions on a specific
  video.<p>Allows Access Control entities to be set for all four types. Note
  that if set to <b>Public</b>, the Public setting must first be enabled on the
  Vbrick account and a password may then be set if desired. If set to
  <b>Channels</b>, there should be one valid Channel in the account, otherwise
  the request is rejected. The default setting is <b>Private</b>.</p>
api:
  file: rev_v2_openapi.json
  operationId: editVideoAccessControl
hidden: false
---