---
title: Patch Channel
excerpt: >-
  Partially edits the members and details of a channel. You do not need to
  provide the fields that you are not changing.<p>Please refer to
  http://jsonpatch.com/ for the format of the request
  body.</p><strong>Examples:</strong><p>To add members: [{'op': 'add',  'path':
  '/Members/-', 'value': {'id': '0e2a1bfc-0a36-4ee1e-ac1e-3647b256537d','type':
  'Group','roleTypes': ['Member','Contributor']}} ]</p><p>To remove members : [{
  'op': 'remove',  'path': '/Members',  'value':
  '63a76eb9-fa62-46e0-bdb5-c8ad34aec086' }]</p><p>To update channel name : [{
  'op': 'replace', 'path': '/Name', 'value': 'New Name' }]</p>
api:
  file: rev-rest-apis.json
  operationId: patchChannel
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---