---
title: Duplicate a Webcast
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
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
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

The duplication feature copies an event so that you can quickly set up features and technical settings needed without having to create them again.  If you need to use the same event several times, you can also [Create a Webcast Template](doc:create-a-webcast-template) instead. Either choice means you do not have to create a webcast from scratch every time.

Admins and Hosts can edit the event settings and use the **Duplicate Webcast** button to use this feature.

<Image title="duplicateWebcastButton.png" alt={1202} src="https://files.readme.io/492a6d3-duplicateWebcastButton.png">
  The Duplicate Webcast button on the Webcast Landing page copies an event
</Image>

When you copy an event:

* The **Title** is prepended with "Copy of".
* The **Start Date** and **Time** are pre-populated with the next hour of the current date/time.
* The **Duration** of the event is the same as the original.

The following features from each section are copied:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Section
      </th>

      <th>
        Duplicated Features
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Basic Settings
      </td>

      <td>
        a. Title\
        b. Description\
        c. Lobby Time\
        d. Timezone\
        e. Categories\
        f. Tags
      </td>
    </tr>

    <tr>
      <td>
        Video Source
      </td>

      <td>
        a. Video Source\
        b. Closed Captions\
        c. Automated Webcast
      </td>
    </tr>

    <tr>
      <td>
        Hosts And Moderators
      </td>

      <td>
        a. Event Hosts\
        b. Event Moderators
      </td>
    </tr>

    <tr>
      <td>
        Attendees
      </td>

      <td>
        a. Listing Type\
        b. Unlist this Webcast
      </td>
    </tr>

    <tr>
      <td>
        Attendee Engagement
      </td>

      <td>
        a. Polls\
        b. Chat\
        c. Q\&A\
        d. Presentation File/Download Setting\
        e. Background Image
      </td>
    </tr>
  </tbody>
</Table>

> 🚧 Important!
>
> Event templates and duplicated events do *not* carry over the **Estimated Attendees** field (users should enter the new estimate so a more accurate number is obtained).
