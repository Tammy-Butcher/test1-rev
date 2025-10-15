---
title: Patch Group
excerpt: >-
  Partially edits the details of a group. You do not need to provide the fields
  that you are not changing. For <strong>LDAP groups</strong>, only roles can be
  updated. For Rev system groups, <em>both</em> users and roles can be
  updated.<p>Please refer to http://jsonpatch.com/ for the format of the request
  body.</p><p><strong>Examples:</strong></p><p>To add users: [{ 'op': 'add',
  'path': '/UserIds/-', 'value': '13443c6c-e2cc-49e2-b4b2-ec3ebad97fb1'
  }]</p><p>To add roles: [{ 'op': 'add', 'path': '/RoleIds/-', 'value':
  'b14f6a56-254d-43ee-950b-145811ebfc8c' }]</p><p>To remove users: [{ 'op':
  'remove', 'path': '/UserIds', 'value': 'b14f6a56-254d-43ee-950b-145811ebfc8c'
  }]</p><p>To remove roles: [{ 'op': 'remove', 'path': '/RoleIds', 'value':
  'b14f6a56-254d-43ee-950b-145811ebfc8c' }]</p>
api:
  file: rev-rest-apis.json
  operationId: patchGroup
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---