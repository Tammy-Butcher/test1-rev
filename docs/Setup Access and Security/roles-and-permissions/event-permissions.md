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

[block:parameters]
{
  "data": {
    "h-0": "Role",
    "h-1": "Permissions",
    "h-2": "Granular Restrictions",
    "0-0": "Internal Event Host",
    "0-1": "Add internal [All Users Events](doc:all-users-events)  \nAdd [Private Events](doc:private-events)",
    "0-2": "This is a granular form of the **Event Host** role and is used to create hosts that can create/edit _internal_ **All Users** or **Private** events _only_.  \n  \nFurther, this role _restricts_ the ability to make [Public](doc:public-events) events.  \n  \nThe role may edit an existing event _only_ if they are the **Internal Event's Host/Event Host** (or an Event Admin).",
    "1-0": "Event Analyst",
    "1-1": "Access to the **Events** tab and [Events System Analytics](doc:events-system-analytics) on the **Account Admin Dashboard**",
    "1-2": "Only access to the **Events** tab is provided with this role; all other Admin/analytics areas are restricted."
  },
  "cols": 3,
  "rows": 2,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]