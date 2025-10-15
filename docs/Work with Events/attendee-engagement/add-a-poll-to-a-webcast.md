---
title: Add a Poll to a Webcast
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

A **Poll** is frequently used to keep attendees engaged in the webcast presentation as well as a means to solicit feedback and collect information.

One or more polls are often added during event set up (and before broadcasting) so that they do not have to be created on the fly. Both Event Admins and Event Moderators may create and manage polls once the event begins if needed however.

To enable and add a poll to an event:

<Image title="enablePolls.png" alt={805} src="https://files.readme.io/67f56e6-enablePolls.png">
  Polls are disabled by default when you add an event
</Image>

1. Click the **Enabled** tab next to **Enable Polls**.  This is disabled by default.

2. Choose how to log and report poll responses.
   * **Anonymous user responses** - User responses are not logged and poll responses are reported as anonymous on the [Download Poll Results](doc:webcast-reports#download-poll-results) report and in APIs
   * **Log all user responses** - All user responses to polls are collected, including the date and time, and are reported in the [Download Poll Results](doc:webcast-reports#download-poll-results) report as well as APIs

3. Click the **Add Poll** button to add a new poll to the event.

4. Use the **Question** field to enter the poll question and up to 15 answers in the **Answers** fields. At least one answer is required. These fields may be edited if no responses have been received.

<Image title="pollQuestion.png" alt={683} src="https://files.readme.io/a8e2149-pollQuestion.png">
  Answers may be edited if no responses have been received
</Image>

5. Select the **Yes** button next to **Allow Multiple Answers** if you want attendees to be able to choose more than one answer when taking the poll.

6. Click the **Delete Poll** button to remove the poll entirely from the event.

7. You may add more than one poll to the event by clicking the **Add Poll** button again to add additional polls. **Event Moderators** are able to choose when to launch each poll (and in which order) during the Webcast.

8. Polls are also added to webcast templates.
