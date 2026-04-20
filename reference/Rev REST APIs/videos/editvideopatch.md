---
title: Patch Video Details/Metadata
excerpt: >-
  Partially edits the metadata details of a video. You do not need to provide
  the fields that are not changing.<p>Operations supported:
  add,remove,copy,replace,test,move.</p><p>Keep in mind that Access Controls are
  strictly dictated by [Roles and
  Permissions](/docs/roles-and-permissions).</p><p>Please refer to
  http://jsonpatch.com/ for the format of the request
  body.</p><strong>Examples:</strong><p>using categories: [{'op': 'add', 'path':
  '/Categories/0', 'value': '03846100-96ac-4628-bbe3-b23a0df1081d'
  }]</p><p>using accessControlEntities: [{ 'op': 'replace', 'path':
  '/accessControlEntities/0/CanEdit', 'value': 'false' }]</p><p>Non-Editable
  fields [Id,ApprovalStatus,UploadedBy,WhenUploaded,LastViewed] are
  ignored.</p></p>
api:
  file: rev-rest-apis.json
  operationId: editVideoPatch
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---