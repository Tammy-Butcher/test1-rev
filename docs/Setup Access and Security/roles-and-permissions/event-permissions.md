---
title: Event Permissions
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
What you can do with events in Rev is defined by the role you are assigned. The roles below have permissions in Rev as specified.

| Permission(s) By Role | Account Admin | Media Admin | Media Contributor | Media Viewer | Channel Creator | Event Admin | Event Host |
| :-------------------- | :------------ | :---------- | :---------------- | :----------- | :-------------- | :---------- | :--------- |
| Add Event             | X             | X           |                   |              |                 | X           | X          |
| Add Public Event      | X             | X           |                   |              |                 | X           | X          |
| Edit Event            | X             | X           |                   |              |                 | X           | X ¹        |
| View Event            | X             | X           | X                 | X            | X               | X           | X          |
| Delete Event          | X             | X           |                   |              |                 | X           | X ¹        |

<sup>1: Event Hosts may only perform these functions on events they create or are assigned to.</sup>

## Event Granular Roles and Permissions

<div>
  <strong>Role</strong>: Internal Event Host
  <br/>
  <strong>Permissions</strong>: Add internal <a href="doc:all-users-events">All Users Events</a>  <br/>
  Add <a href="doc:private-events">Private Events</a>
  <br/>
  <strong>Granular Restrictions</strong>: This is a granular form of the <strong>Event Host</strong> role and is used to create hosts that can create/edit <em>internal</em> <strong>All Users</strong> or <strong>Private</strong> events <em>only</em>.  <br/>
  Further, this role <em>restricts</em> the ability to make <a href="doc:public-events">Public</a> events.  <br/>
  The role may edit an existing event <em>only</em> if they are the <strong>Internal Event's Host/Event Host</strong> (or an Event Admin).
</div>
<div>
  <strong>Role</strong>: Event Analyst
  <br/>
  <strong>Permissions</strong>: Access to the <strong>Events</strong> tab and <a href="doc:events-system-analytics">Events System Analytics</a> on the <strong>Account Admin Dashboard</strong>
  <br/>
  <strong>Granular Restrictions</strong>: Only access to the <strong>Events</strong> tab is provided with this role; all other Admin/analytics areas are restricted.
</div>