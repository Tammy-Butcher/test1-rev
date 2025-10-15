---
title: Record and Stream Microsoft Teams Meetings
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

To use Microsoft Teams video conferencing as a video source in Rev Webcasts you need to enable and configure Microsoft Teams Video Conferencing integration option in **Media Settings > Integrations**.

<Image alt="Enable the Microsoft Teams Video Conferencing integration to record and stream your Teams meetings" align="center" src="https://files.readme.io/ecec8d1-msTeamsVC.png">
  Enable the Microsoft Teams Video Conferencing integration to record and stream your Teams meetings
</Image>

When this option is enabled, you are able to:

* Schedule and record a Microsoft Teams Meeting in Rev (using Teams as the video source)
* Stream a Microsoft Teams Live Webcast Event in Rev (Meetings and Live Events)

## Requirements

* Rev Cloud
* Rev Account Admin / Microsoft Teams Admin access (for installation only)

## Installation

Rev is able to **record** and **stream** your Microsoft Teams meetings and live events from Webcast events when **Microsoft Teams Video Conferencing** is enabled.

To enable Microsoft Teams Video Conferencing:

1. Navigate to **Admin > Media Settings > Integrations**.

2. Scroll to the **Microsoft** section.

3. Select the **Microsoft Teams Integration** checkbox.

4. Your Microsoft Teams Admin must click and login to the **registration URL** that appears to authorize Rev to connect with Microsoft Teams. This automatically registers Rev with your Microsoft Teams account and allows it to be used as a streaming source.

<Image title="enableVideoConference.png" alt={1111} align="center" src="https://files.readme.io/cbf00f8-enableVideoConference.png">
  Once you enable the checkbox for video conferencing, login to your Microsoft Teams admin account to complete your registration.  You are now able to record and stream MS Team meetings.
</Image>

You can now use Microsoft Teams to source a Rev Webcast event. Microsoft Teams provides two different event types: a Microsoft Teams **Meeting** and a Microsoft Teams **Live Event**. These two approaches to using Microsoft Teams for collaboration are different in their presentation and reach.

* **Microsoft Teams Meetings** are similar to traditional video conferencing with many-to-many discussions and free content sharing between participants.
* **Microsoft Teams Live Events** are a few-to-many collaboration that are a more curated/controlled presentation with a producer, presenters, and attendees.

## Schedule a MS Teams Meeting Webcast

You can use a Microsoft Teams Meeting as a **video source** for your Webcast event with both Microsoft Teams integration settings enabled. You are prompted to enter a **Microsoft Teams Meeting URL**. This means you can save the recording once it is finished and use Rev’s video settings and metadata features.

To use this functionality:

* The **Microsoft Teams Integration** and **Microsoft Teams Video Conferencing** integrations must *both* be enabled.
* You *must* have the correct **Microsoft Teams Meeting URL** entered in the **Video Source** during Webcast Event set up.

To start and broadcast a Microsoft Teams Meeting in a Webcast Event:

1. Schedule an event as you normally would.

2. Select **Microsoft Teams** as the video source in the **Video Source** section. If you do not see this tab, you do not have the Microsoft Teams Integration(s) enabled or configured correctly.

3. Click the **Microsoft Teams Meeting URL** field and paste the meeting URL for your meeting. This is a *required* field and can be quite long.

**Sample URL:**

`[https://teams.microsoft.com/l/meetup-join/19%3ameeting_MTI4NWFiN2MtMmI5Mi00OTc2LWE4ODQtZjgzZTY2M2UxNTFh%40thread.v2/0?context=%7b%22Tid%22%3a%2224ed0676-67e2-4293-a8d4-28937fd33247%22%2c%32Oid%23%3a%22a3fbdcb9-04e8-4c17-9303-859cc56c0d5g%22%7d]`

<Image title="msTeamsMeetingUrl.png" alt={1157} align="center" src="https://files.readme.io/782a6d3-msTeamsMeetingUrl.png">
  Make sure you enter the full Microsoft Teams Meeting URL
</Image>

4. Finish setting up the event and, when you are ready to begin, start *both* the **Rev event** and the **MS Teams meeting**.

5. Rev utilizes the Microsoft Teams meeting URL to stream through Rev via the Webcast settings you selected.

6. You may end the event in either Rev or MS Teams when you are finished. The video appears in Rev with the **Meeting Name** if you choose to save the recording. You may modify its metadata and Video Settings as you would any other video.

## Schedule a Microsoft Teams Live Event Webcast

Using an MS Teams Live Event and distributing it through a Rev webcast requires a specific workflow for optimum success. The MS Teams Live Event is configured with the Rev webcast already joined – before any attendees see it.

To schedule and run a Microsoft Teams Live Event Webcast:

* Create your **MS Teams Live Event** as you normally would.
* Communicate details to **Producers**, **Presenters**, and any **Attendees** that will view via MS Teams.
* Complete the Rev event set up needed to distribute the MS Teams Live Event (using the MS Teams **Live Event URL** in the **Video Source** field in Rev described above).
* Communicate the Rev webcast details to Rev Attendees.

> ❗️ Caution!
>
> It is important that the steps below happen in the order they are presented.  Otherwise, your Live Event may have unexpected results or may not stream.

### Time of Event Tasks

**Configure MS Teams Live Event and Rev Event as you normally would.** 

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Role
      </th>

      <th>
        Action
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Producer** 
      </td>

      <td>
        * \*1. Joins (but does not start) the MS Teams Live Event\*\*.  

        **2. Configures the event.**  

        Producer has complete control to specify and/or test the stream, move display items, pre-queue view to Live Event queue view, and ultimately, to the Live Event view (via **Send Live** button).
      </td>
    </tr>

    <tr>
      <td>
        **Presenters** 
      </td>

      <td>
        **3. Join the MS Teams Live Event.**  

        Presenters may *only* join by invitation.
      </td>
    </tr>

    <tr>
      <td>
        **Rev Event Host** 
      </td>

      <td>
        * \*4. Starts (but does not Broadcast) the associated Rev Webcast.\*\* This can happen while the Producer is configuring the Live Event.  

        Once Rev connects, it is listed as a Presenter in the MS Teams Live Event (Note that Rev *cannot* be added to the MS Teams Live Event view.)
      </td>
    </tr>
  </tbody>
</Table>

At this point, the MS Teams Live Event production environment is enabled and displayed to the MS Teams Live Event Producer and Presenters. The MS Teams Live Event stream is also available to the Rev Event Host (on the Event Page). 

MS Teams Live Event Attendees and Rev Attendees do *not* see the stream yet. This is an ideal opportunity to verify the stream and settings on both the MS Teams Live Event production page, as well as, within the Rev Event Host.

### Event Start Time Tasks

**Start the MS Teams Live Event and Broadcast the Rev webcast.**

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Role
      </th>

      <th>
        Action
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Producer** 
      </td>

      <td>
        * \*5. Initiates the MS Teams Live Event using the Start button.\*\* This begins the stream for all MS Teams Live Event attendees.  

        MS Teams Live Events *cannot* be stopped and restarted (like Rev Webcasts), so please make sure you are ready to begin.  

        When using any external virtual Production system like MS Teams Live Events, please be aware that Rev webcasts and recordings have a **10-hour maximum**.
      </td>
    </tr>

    <tr>
      <td>
        Rev Event Host
      </td>

      <td>
        * \*6. Broadcasts the Rev Webcast\*\*.  

        The MS Teams Live Event stream is now available to Rev attendees.  

        * Note: Once Broadcast from Rev after it’s Live from MS Teams, the same URL for MS Teams cannot be used again if it is stopped\_.  

        The stream is a single stream controlled by the MS Teams Live Event Producer and not a dual (speaker and content) stream.  

        It is recommended that you *not* start/stop the Rev Webcast, but control the experience through the **MS Teams Live Event** interface.
      </td>
    </tr>
  </tbody>
</Table>

### Event Completion Tasks

* The Event Host ends the **Rev Webcast** first. 
* The Producer can then use the **Leave** button in the **MS Live Event** to end the Live Event.
