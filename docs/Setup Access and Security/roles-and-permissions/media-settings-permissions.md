---
title: Media Settings Permissions
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
Adding, editing, and deleting **Media Settings** varies by role depending on what you are attempting. The roles below have the Media Settings permissions in Rev as specified.

| Permission(s) By Role              | Account Admin | Media Admin | Category Creator | Category Manager | Category Contributor |
| :--------------------------------- | :------------ | :---------- | :--------------- | :--------------- | :------------------- |
| Add/Edit/Delete Category           | X             | X           | X ¹              | X ²              |                      |
| Add Sub-Category                   | X             | X           | X ¹              |                  |                      |
| Add Secure Category Content        | X             | X           |                  | X                | X                    |
| Add/Edit/Delete Transcode Presets  | X             | X           |                  |                  |                      |
| Edit Transcode Settings            | X             | X           |                  |                  |                      |
| Edit Media Feature Settings        | X             | X           |                  |                  |                      |
| Edit Integration Settings          | X             | X           |                  |                  |                      |
| Add/Edit/Delete Approval Processes | X             | X           |                  |                  |                      |
| Edit Recording Settings            | X             | X           |                  |                  |                      |
| Add/Edit/Delete Expiration Rules   | X             | X           |                  |                  |                      |
| Add/Edit/Delete Video Templates    | X             | X           |                  |                  |                      |
| Add/Edit/Delete Webcast Templates  | X             | X           |                  |                  |                      |

<sup>1: Category Creators may only add new categories and subcategories only for Restricted categories that they manage. They may not delete categories.</sup>

<sup>2: Category Managers may only edit and delete categories. They may not add new categories.

## Licensing and Add-On Granular Roles and Permissions

[block:parameters]
{
  "data": {
    "h-0": "Role",
    "h-1": "Permissions",
    "h-2": "Description",
    "0-0": "Rev IQ User",
    "0-1": "Access to use [Rev IQ](doc:rev-ai) features and functions (if enabled)  \n  \nNote:  Rev IQ features and functions are included in Admin roles.",
    "0-2": "If Rev IQ is enabled on the portal, only Admin users and those assigned the **Rev IQ** role have access to its features and functions; all other roles are restricted. This includes:  \n  \n- Generating and translating [Rev IQ subtitles](doc:rev-iq-transcription-and-translation#usage) for a video\n- [Tagging Users](doc:update-basic-video-settings#tag-users-in-a-video) in a video\n- Ability to enable/edit [Live Subtitles](doc:video-sources#live-event-subtitles) for an event (if enabled for the portal)\n- Use of [Generative AI](doc:generative-ai-tools) features such as auto generating metadata and transcriptions."
  },
  "cols": 3,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]