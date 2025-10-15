---
title: Pexip
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

Rev integrates with **Pexip** so that you are able to use a **Pexip Meeting** conference call as the **video source** for a Rev Webcast Event. You can also record a Pexip Meeting as a new Rev VOD which means you can then apply all of Rev's associated metadata settings once it has concluded.

## Requirements

* Rev Cloud
* [Video Conference (VC) Integrations](doc:video-conference-vc-integrations) enabled
* A Pexip account that has access to the Pexip video conference meeting you want to stream and/or record

## Configuration

To enable Pexip in Rev:

1. Navigate to **Media Settings** > **Integrations**.  Scroll to the **Video Address Conference Integration** section.

2. Select the **Enable Video Address Conference Integration** checkbox to enable it if it is not already enabled.

3. Enter any [DTMF codes](doc:dtmf-configuration-and-usage) you want to use (optional).

4. This will make Pexip Meetings available in the **Recording** menu of the **Upload** tray and as a **Video Source** for Rev events.

## Usage

### Stream a Pexip Meeting to a Scheduled Rev Webcast Event

You can use a Pexip meeting as a video source for your Webcast event once you have enabled the Video Conference meeting Integration.

This means you can take advantage of Rev’s Webcast functionality to distribute the Pexip meeting. Afterward, you can then save the recording and use Rev’s video settings and metadata features.

To stream a Pexip Meeting to a Rev Webcast event:

1. Schedule the Rev event as you normally would. **View**: [Scheduled Webcasts](doc:webcast-listing-types-and-video-sources#scheduled-webcasts)

2. Select **Pexip** as the source in the [Video Sources](doc:video-sources)  section.

3. Enter a **Pexip** email address that is associated with the Pexip meeting room you want to join.  Pexip also allows you to [join the Pexip Meeting as a Guest](https://help.pexip.com/service/join-as-guest.htm#guest_android_join).

<Image title="pexipVidSource.png" alt={1141} align="center" src="https://files.readme.io/009d793-pexipVidSource.png">
  Select Pexip as the video source to stream a Pexip meeting
</Image>

4. Enter the Pin / Password for the meeting if one was set up.

5. Configure the [DTMF](doc:dtmf-configuration-and-usage#use-dtmf-codes-in-events) codes you want to use with the event if any. (optional)

6. Start the Rev event and the Pexip meeting when ready.  Starting the Rev event also starts the Pexip meeting although ideally the end point (Pexip meeting) should be started first before beginning your Rev meeting.

7. An “Initializing” message appears in the Webcast window while Rev and Pexip connect. Note that initialization may take up to a minute for video from Pexip to display in Rev.

8. Once your Pexip conference video appears, you may begin **Broadcasting** your event as you would any other Rev webcast.

9. You may end the event in either Rev or Pexip. The video appears in Rev with the Pexip Meeting Name if you choose to save the recording. You may modify its metadata and Video Settings as you would any other video.

### Record a Pexip Meeting as a New Rev VOD

Similar to **Video Conference** recording, Rev Cloud also supports recording Pexip meetings and ingesting them into your standard media workflow. The recordings capture both active speakers and any content streams (if available). Vbrick’s player displays both streams and allows the user control of the layout.

To record a Pexip meeting:

1. Click the **Recording** tab > **Pexip** option.

<Image alt="Click the Recording tab and then select the Pexip option" align="center" src="https://files.readme.io/1e25d1e-pexipRecording.png">
  Click the Recording tab and then select the Pexip option
</Image>

2. Enter a **Pexip** email address that is associated with the Pexip meeting room you want to join. 

3. Enter the Pin / Password required for the meeting (if set up).

4. Configure the [DTMF](doc:dtmf-configuration-and-usage#use-dtmf-codes-in-video-recording) codes you want to use with the recording if any. (optional)

5. Click the **Start Recording** button. If a valid Pexip meeting is used, Rev connects and begins recording.

6. When the **Stop** button is pushed, Rev uploads the video to Rev and disconnects.  You can then modify and control the [Video Settings](doc:updating-video-settings) and metadata in Rev as you normally would.
