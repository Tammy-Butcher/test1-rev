---
title: Existing Video Event Set Up
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

You can use a previously recorded video as a source for a Rev event. This is also known as a "simulated-live event" or a [rebroadcast](doc:rebroadcast-an-existing-video). This provides Hosts with many benefits including the ability to:

* Easily repurpose existing recorded content in a simulated "Live" event
* Rebroadcast a recorded event to new audiences
* Accommodate multiple time zones
* Record and edit high-profile webcasts in advance
* Remove the stress of speaking to a Live audience
* Access new search and select capabilities with video preview

Select **Existing Video** in the **Video Source** dropdown to rebroadcast a previously recorded video as a Live webcast. All videos that you have edit rights to appear under the **Select Video** tab.

<Image title="preRecordedVideo.png" alt={1809} src="https://files.readme.io/433dfa3-preRecordedVideo.png">
  Select Existing Video in the Video Source dropdown to rebroadcast a previously recorded video
</Image>

Enter search terms to search through your video library and use the **My Videos** and **All Videos** tab(s) to filter the pre-recorded video assets.  A selection is required if you have the Video Source for the event set to Existing Video.

The following event settings are configured as follows:

* [Pre-Production](doc:prepare-a-dry-run) settings are available and perform the same as for [Presentation Profile](doc:video-sources#presentation-profile-events) events.
* The [Automated Webcast](doc:video-sources#automated-webcasts) setting is available and is disabled by default.  When enabled, your webcast will start automatically at start time.
* The [Autoplay](doc:video-sources#autoplay-a-webcast) setting is enabled by default.
* [Polls, chat, and Q\&A](doc:attendee-engagement) functions are enabled in the **Attendee Engagement** section with their default settings.

The following event settings are *disabled* and hidden and may not be used when using an Existing Video as the webcast video source:

* [Closed Captions](doc:video-sources#closed-captions)
* [Live Event Subtitles](doc:video-sources#live-event-subtitles)
* [Webcast Recordings](doc:webcast-recordings)
* [Presentation Files](doc:attendee-engagement#add-a-presentation-to-an-event)

Once the selection is made, if you want to change to a different video, note that you must **Delete (X)** the selection and start over by selecting a new video before the webcast begins.

<Image title="deletePreRecordedVideo.png" alt={1495} src="https://files.readme.io/0b4bf8d-deletePreRecordedVideo.png">
  To choose a different Existing Video, delete the previously selected VOD first to replace it
</Image>

> ❗️ Caution!
>
> It is important to note the time of your video! If the scheduled event end time is less than the duration of the video source file, the webcast will potentially end early and cut off the video too soon.  You are given a warning about this but are still able to save the video.  
>
> This is to allow you to place "filler" material at the end of the video if needed such as music and a thank you for attending message.

<Image title="videoTimeError.png" alt={1499} src="https://files.readme.io/be744ae-videoTimeError.png">
  Be aware of your video length versus your event duration!
</Image>

[Rebroadcasting an Existing Video](doc:rebroadcast-an-existing-video) is very similar to hosting a Live event with small differences when switching from automated to manual control.  Make sure you familiarize yourself with these before hosting your first event.  This feature must be globally enabled by an Account Admin under [Additional Video Sources](doc:additional-video-sources) in **Integrations** before it is visible.
