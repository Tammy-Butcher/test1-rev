---
title: Video Permissions
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
What you can do with video in Rev is defined by the role you are assigned. The roles below have permissions in Rev as specified.

| Permission(s) By Role  | Account Admin | Media Admin | Media Contributor | Event Admin | Event Host |
| :--------------------- | :------------ | :---------- | :---------------- | :---------- | :--------- |
| Upload Video           | X             | X           | X                 |             |            |
| Upload Public Video ¹  | X             | X           | X                 | X           | X ²        |
| Record Video           | X             | X           | X ³               |             |            |
| Manage Featured Videos | X             | X           |                   |             |            |
| Manage All Videos      | X             | X           |                   |             |            |
| Approve Videos         | X             | X           |                   |             |            |

<sup>1: Public videos must be enabled on the Rev portal first.</sup>

<sup>2: The Event Host role must be combined with another role that has public video upload permissions to be able to upload Public videos.

<sup>3: An Internal Media Contributor may not record video.

## Media and Video Granular Roles and Permissions

| Role                       | Permissions                                                                                                                | Granular Restrictions                                                                                                                                             |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Internal Media Contributor | Allows a user to upload, manage, and record content using the **Upload** menu.                                             | This is a granular form of the **Media Contributor** role with the main difference being this role is _not_ allowed to set a video to **Public**.                 |
| Media Uploader             | Allows a user to upload and manage content using the **Upload** menu.                                                      | This is a granular form of the **Media Contributor** role with the main difference being this role is _not_ allowed to **record** using the **Upload** menu.      |
| Internal Media Uploader    | Allows a user to upload and manage content using the **Upload** menu.                                                      | This is a granular form of the **Media Contributor** role with the main difference being this role is _not_ allowed to **record** _or_ set a video to **Public**. |
| VOD Analyst                | Access to the **Videos** tab and [Videos System Analytics](doc:videos-system-analytics) on the **Account Admin Dashboard** | Only access to the **Videos** tab is provided with this role; all other admin/analytics areas are _restricted_.                                                   |