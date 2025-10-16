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

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Role
      </th>

      <th>
        Permissions
      </th>

      <th>
        Granular Restrictions
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Internal Event Host
      </td>

      <td>
        Add Internal [All Users Events](doc:all-users-events)
        Add [Private Events](doc:private-events)
      </td>

      <td>
        * This is a granular form of the **Event Host** role and is used to create hosts that can create/edit _internal_ **All Users** or **Private** events only.
        * Further, this role _restricts_ the ability to make [Public Events](doc:public-events).
        * The role may edit an existing event only if they are the internal event's **Host/Event Host** (or an **Event Admin**) role.
      </td>
    </tr>

    <tr>
      <td>
        Event Analyst
      </td>

      <td>
        Access to the Events tab and [Events System Analytics](doc:events-system-analytics)
      </td>

      <td>
        Only access to the **Events** tab is provided with this role; all other Admin/analytics areas are restricted.
      </td>
    </tr>
  </tbody>
</Table>

