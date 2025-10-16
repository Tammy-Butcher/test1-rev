---
title: Producer Event Set Up
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
Rev's **Producer** capability is a collaborative way to create live events within Rev using just a webcam, screenshare, and mic with up to nine producers and presenters – even if they are all remote. Producer events are similar to [Webcam and Screenshare Events](doc:video-sources#webcam-and-screenshare-events) except that those assigned roles of **Producer** and **Presenter** are grouped in a private “backstage” interface together and control exactly what attendees see and experience. They can choose what is displayed, including the webcams and screenshares of presenters, layouts, backgrounds, and banners with speakers’ names.

> 📘 Note
>
> This feature must be globally enabled under [Additional Video Sources](doc:additional-video-sources#allow-producer) before it appears in the Video Source drop-down.

<Image align="center" alt={1152} border={false} caption="Select Producer as a Video Source to create a Producer event" title="producerVideoSource.png" src="https://files.readme.io/5a34432-producerVideoSource.png" />

When scheduling a **Producer** event, you must designate at least one **Event Producer**.  These **Event Producers** are actually Hosts with additional capabilities and responsibilities around controlling the event -- including selecting layouts, presenters, and ultimately will "producing" the event.  This is done in the **Event Producers** section.  Additionaly, the person creating the webcast will automatically be included as a **Producer**, but this may be edited to any other user.

It is important to note that currently you can only have a total of 9 users in the backstage (for all Producers and Presenters, with the additional rule that there must be at least one Producer.)

<Image align="center" alt={1272} border={false} caption="At least one Producer must be designated.  These Producers are Hosts with additional capabilities and responsibilities with controlling a Producer event." title="eventHosts.png" src="https://files.readme.io/a89f552-eventHosts.png" />

**Presenters** for a Producer event can be either Internal or External. Presenters are only able to control their own webcam and screenshare, and cannot modify the Preview or OnStage views within a Producer event.  Presenters are moved to live view by the Producers of the event so that Attendees can see them .

**Internal Event Presenters** are Presenters that have a Rev account, and as such, are required to log in to attend a Producer event.

<Image align="center" alt={1147} border={false} caption="Internal Event Presenters are Rev Account holders and must be logged in to attend the event" title="eventPresentersInternal.png" src="https://files.readme.io/5f8fb80-eventPresentersInternal.png" />

**External Event Presenters** (also called Guest Presenters) are treated just like **Internal Presenters** within the event.  However, **Guest** presenters do not have Rev accounts and do not need to be logged for the event.  They are required, however, to have a valid email since Rev will issue/email them a specific (per presenter) URL used to gain entry into the event.  The email will be sent when the event is created, and updates will be sent if the event changes.  To add **External Event Presenters**, click the **Add** button.  You will be asked to provide a **Name**, **Title**, and valid **E-mail** address.

> 📘 Note
>
> External presenters must be enabled in [Producer Settings](doc:producer-settings) by an Account Admin before it is visible.

<Image align="center" alt={1112} border={false} caption="External Event Presenters are Guest presenters and are only required to have a valid email address for invite purposes." title="externalEventPresenter.png" src="https://files.readme.io/d8b54d0-externalEventPresenter.png" />

As a reminder, when a webcast is a Producer event:

* **Producer** is selected as a video source during event setup.
* The **Host And Moderators** section is renamed to **Event Producers (Internal Only)**.
* **Event Producers** have Host controls.
* **Presenters** (Internal or External) can _only_ control their _own_ webcam and screen share (unlike Producers).
* Unlike other video sources, Producers (acting as Hosts) view the Live stream directly so at least one **Moderator** is recommended to observe what Attendees are viewing.
* If there are multiple Producers within the event, it is recommended that you select a primary Producer.
* If your Producer is going to be OnStage, it is recommended that you have at least one other Producer manage the Backstage during that period.

> 🚧 Important!
>
> A total of up to nine unique Producers and Presenters (no matter the type) can be selected for the event.

## Producer-Specific Settings

A Producer event contains a **Producer Settings** section where only settings related to this type of webcast are configured.  For example, you can upload a custom background image for your Producer event in this section.  Click the **Add New** button to upload a jpeg/png image (gifs and animated gifs are not supported).  The images are scaled to fit within the presentation. Vbrick recommends an image with a 16:9 aspect ratio (which matches the output) -- with the ideal size being a 1920 x 1080 image.  Background images can be applied to the **Preview** and promoted to the **Onstage** streams for increased customization.

<Image align="center" alt={1144} border={false} caption="Add a custom background image for your event in Producer Settings" title="addBackgroundImage.png" src="https://files.readme.io/d5cc50b-addBackgroundImage.png" />

If you want to change or remove your image, hover over the existing image and click the **X** in the upper right corner to delete it and add a new image again.  Make sure you **Save** your event again to save the newly added image.

> 📘 Note
>
> Backgrounds (static images or live streams) add production value to your event. However, backgrounds also increase the encoding complexity of the overall stream.  The more detailed the background is in terms of objects, lines, and colors, the more complex it is. It takes more bits/bandwidth to provide a high-quality output when encoding a video with increased complexity.  Producer currently uses the same settings as our VCI solutions, so it has upper limits for bitrate and resolution.
>
> Please test all your backgrounds (with foreground streams) for output encoding quality and, if necessary, consider reducing encoding complexity for better quality.

## Additional Configuration Settings

The following event settings display and are configured as you would for a "normal" Rev event:

* [Pre-Production](doc:prepare-a-dry-run) settings are available and perform the same as for [Presentation Profile](doc:video-sources#presentation-profile-events) events. Disabled by default.
* The [Autoplay](doc:video-sources#autoplay-a-webcast) setting is enabled by default.
* [Live Event Subtitles](doc:video-sources#live-event-subtitles) may be used and are disabled by default.
* [Polls, chat, and Q&A](doc:attendee-engagement) functions are available in the **Attendee Engagement** section with their default settings.

The following settings are _disabled_ and/or hidden with **Producer** events:

* [Automated Webcast](doc:video-sources#automated-webcasts)
* [Closed Captions](doc:video-sources#closed-captions)
* [Presentation Files](doc:attendee-engagement#add-a-presentation-to-an-event)  This source does not allow for Presentation Files (ppts).  Considering sharing the screen with your ppt display instead.

## Producing the Event

[Producing an Event](doc:produce-an-event) is similar to hosting a regularly scheduled **Production** event with some differences in Host duties and capabilities in their Producer roles.  Make sure you familiarize yourself with these before you produce your first webcast in Rev.
