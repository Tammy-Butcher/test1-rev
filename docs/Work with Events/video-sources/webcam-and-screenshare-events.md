---
title: Webcam and Screenshare Event Set Up
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

A **Webcam and Screenshare** source is an event that allows you to quickly start and stream a webcast  *without* the need for any additional 3rd party hardware or software set up. Instead, utilizing [WebRTC](https://en.wikipedia.org/wiki/WebRTC) technologies, a **Presenter** is able to use their own internal or USB webcam, microphone, and browser or screenshare with audio to broadcast an event.  

You can schedule a webcam and screenshare event as you normally would by selecting **Webcam and Screenshare** as a **Video Source** when you are configuring your event.

<Image title="selfProducedSource.png" alt={1805} align="center" src="https://files.readme.io/4f8e65d-selfProducedSource.png">
  Choose Webcam and Screenshare as your Video Source if you want to self produce your event
</Image>

When scheduling a **Webcam and Screenshare** event, you must designate a **Presenter**.  This is the person who will share their webcam and screenshare.  This is done in the **Host and Moderators** section (now termed the **Hosts, Presenter, And Moderators** section for this event source type.)  

The **Presenter** is defaulted to the person creating the webcast but may be edited to any other user. There may be only one **Presenter** for the event.  A **Presenter** can also be a Host (Called a **Presenter-Host**) who has all the capabilities of a **Presenter** as well as a **Host** (i.e., they can start/stop the event as well as present.)  Alternatively, as with other event types, there may be multiple, additional **Hosts** who are not **Presenters**.

<Image title="hostPresenterModerator.png" alt={1151} align="center" src="https://files.readme.io/d1a36c2-hostPresenterModerator.png">
  The Presenter defaults to the person who creates the event
</Image>

## Configuration Settings

The following settings display and are configured as follows:

* [Pre-Production](doc:prepare-a-dry-run) settings are available and perform the same as for [Presentation Profile](doc:video-sources#presentation-profile-events) events. Disabled by default.
* The [Autoplay](doc:video-sources#autoplay-a-webcast) setting is enabled by default.
* [Live Event Subtitles](doc:video-sources#live-event-subtitles) may be used and is disabled by default.
* [Polls, chat, and Q\&A](doc:attendee-engagement) functions are available in the **Attendee Engagement** section with their default settings.

**Webcast and Screenshare** events The following settings are *disabled* and/or hidden with webcam and screenshare events:

* [Automated Webcast](doc:video-sources#automated-webcasts)
* [Closed Captions](doc:video-sources#closed-captions)
* [Presentation Files](doc:attendee-engagement#add-a-presentation-to-an-event)  This source does not allow for Presentation Files (ppts).  Considering sharing the screen with your ppt display.

> 📘 Note
>
> This feature must be globally enabled by an Account Admin under [Additional Video Sources](doc:additional-video-sources) in **Integrations** before it is visible.

## Hosting and Presenting

[Presenting a Webcam and Screenshare Event](doc:host-a-self-produced-webcast), either scheduled or Live, is very similar to hosting a regularly scheduled Production event with a few small differences.  Make sure you familiarize yourself with these before hosting your first event.

You also have the option of using the **Go Live** button at the top of the Rev interface to start an event quickly.  Clicking this button automatically sets up a new **Webcam and Screenshare** event to start now with you as the **Presenter** and **Host**.  Just fill in a few pieces of information (including any necessary custom fields), and then click **Next** to start the event.
