---
title: Record a Zoom Meeting as a New Rev VOD
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

Similar to **Video Conference** recording, Rev Cloud also supports recording Zoom meetings and ingesting them into your standard media workflow with the Zoom integration enabled. The recordings capture both active speakers and any content streams (if available). Vbrick’s player displays both streams and allows the user control of the layout.

To record a Zoom meeting:

1. Click the **Live Recording** tab > **Zoom Meeting** option.

<Image alt="Click the Recording tab and then select the Zoom Meeting option" align="center" src="https://files.readme.io/d879f63-recordZoomMeeting.png">
  Click the Recording tab and then select the Zoom Meeting option
</Image>

2. Type in the **Zoom Meeting ID** or **Zoom Meeting URL**.

3. If the meeting is password protected, you must enter the **H323/SIP numeric password** for the meeting into the **Password** field.

4. Configure the [DTMF](doc:dtmf-configuration-and-usage#use-dtmf-codes-in-video-recording) codes you want to use with the recording if any. (optional)

5. Click the **Start Recording** button. If a valid Zoom Meeting is used, Rev connects and begins recording.

6. When the **Stop** button is pushed, Rev uploads the video to Rev and disconnects.  You can then modify and control the [Video Settings](doc:updating-video-settings) and metadata in Rev as you normally would.
