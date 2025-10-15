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
  <table>
    <thead>
      <tr>
        <th>Role</th>
        <th>Permissions</th>
        <th>Granular Restrictions</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Internal Event Host</td>
        <td>Add internal [All Users Events](doc:all-users-events)<br>Add [Private Events](doc:private-events)</td>
        <td>This is a granular form of the <strong>Event Host</strong> role and is used to create hosts that can create/edit <em>internal</em> <strong>All Users</strong> or <strong>Private</strong> events <em>only</em>.<br><br>Further, this role <em>restricts</em> the ability to make [Public](doc:public-events) events.<br><br>The role may edit an existing event <em>only</em> if they are the <strong>Internal Event's Host/Event Host</strong> (or an Event Admin).</td>
      </tr>
      <tr>
        <td>Event Analyst</td>
        <td>Access to the <strong>Events</strong> tab and [Events System Analytics](doc:events-system-analytics) on the <strong>Account Admin Dashboard</strong></td>
        <td>Only access to the <strong>Events</strong> tab is provided with this role; all other Admin/analytics areas are restricted.</td>
      </tr>
    </tbody>
  </table>
</div>