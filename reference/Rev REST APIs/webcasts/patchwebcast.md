---
title: Patch Webcast
excerpt: >-
  Partially edits the details of a webcast. You do not need to provide the
  fields that you are not changing.<p>Webcast <strong>status</strong> determines
  which fields are modifiable and when. <p>If the webcast pre-production or main
  event is <strong>in progress</strong>, only fields available for inline
  editing may be patched/edited.</p><p>If the webcast main event has been run
  once, only fields available <strong>after</strong> the webcast has ended are
  available for editing. That includes <em>all</em> fields with the
  <em>exception</em> of start/end dates, lobbyTimeMinutes, preProduction,
  duration, userIds, and groupIds.</p><p>If the webcast <strong>end
  time</strong> has passed and is <strong>Completed</strong>, only edits to
  linkedVideoId and redirectVod are allowed.</p><p>Event Admins can be removed
  using their email addresses as path pointer for the fields 'EventAdminEmails'
  and 'EventAdmins', provided that all of the Event Admins associated with the
  webcast have email addresses. This is also applicable for the field
  'Moderators'.</p><p>Keep in mind that Access Controls are strictly dictated by
  <a href=/docs/roles-and-permissions>Roles and Permissions.</a></p><p>Please
  refer to http://jsonpatch.com/ for the format of the request
  body.</p><strong>Examples:</strong><p>using EventAdmins: [{ 'op': 'remove',
  'path': '/EventAdmins/Email', 'value': 'x1@test.com' }]</p><p>using
  EventAdminEmails: [{ 'op': 'remove', 'path': '/EventAdminEmails', 'value':
  'x2@test.com' }]</p><p>using Moderators: [{ 'op': 'remove', 'path':
  '/Moderators/Email', 'value': 'x3@test.com' }]</p>
api:
  file: rev-rest-apis.json
  operationId: patchWebcast
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---