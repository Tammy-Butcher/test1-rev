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

<sup>2: Category Managers may only edit and delete categories. They may not add new categories.</sup>

## Licensing and Add-On Granular Roles and Permissions

<div>
  <table>
    <thead>
      <tr>
        <th>Role</th>
        <th>Permissions</th>
        <th>Description</th>
      </tr>
    </thead>

    <tbody>
      <tr>
        <td>Rev IQ User</td>
        <td>Access to use <a href="doc:rev-ai">Rev IQ</a> features and functions (if enabled)</td>

        <td>
          If Rev IQ is enabled on the portal, only Admin users and those assigned the <strong>Rev IQ</strong> role have access to its features and functions; all other roles are restricted. This includes:

          <ul>
            <li>Generating and translating <a href="doc:rev-iq-transcription-and-translation#usage">Rev IQ subtitles</a> for a video</li>
            <li><a href="doc:update-basic-video-settings#tag-users-in-a-video">Tagging Users</a> in a video</li>
            <li>Ability to enable/edit <a href="doc:video-sources#live-event-subtitles">Live Subtitles</a> for an event (if enabled for the portal)</li>
            <li>Use of <a href="doc:generative-ai-tools">Generative AI</a> features such as auto generating metadata and transcriptions.</li>
          </ul>
        </td>
      </tr>
    </tbody>
  </table>
</div>
