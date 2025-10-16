---
title: Produce an Event
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
<iframe  width="640" height="360" src="https://vision.rev.vbrick.com/embed?id=34cff193-d29e-4acd-9cda-36c069b40350" allowfullscreen style="" frameborder=""></iframe>
`}</HTMLBlock>

Producer events are a uniquely collaborative way to create live events within Rev using just a webcam, screen share, and mic for up to nine producers and presenters – even if they are all remote. Within the event, special users are assigned roles of **Producer** and **Presenter**.  When they join the event, they are grouped in a private “backstage” where they can talk and collaborate.  Ultimately, they control exactly what attendees see and experience.  Meaning, **Producers** backstage can choose what is displayed (sent Onstage), selecting from the webcams and screen shares of presenters, layouts, backgrounds, and banners with speakers’ names.

This feature uses [WebRTC](https://en.wikipedia.org/wiki/WebRTC) within the producers’ and presenters’ browsers, so there are no downloads or other necessary hardware or software. Broadcasts created with Producer utilize Rev’s built-in eCDN, Rev IQ, and analytics. Producer is available to Rev customers without any additional licensing or fees.

## Host a Producer Event

When you [schedule a Producer event](doc:producer-event-set-up), the event Producers have the same controls as Hosts (see [Host a Production Webcast](doc:host-a-production-webcast)).  This means that many of the standard [configuration settings](doc:producer-event-set-up#configuration-settings) are available for Producers -- who should be aware of them.  Presenters do not have access to these Host features.

Like all Rev events, a [Producer event](doc:producer-event-set-up) must be created. In addition to all other event settings, **Producers** and **Presenters** are also specified. Both Producers and Presenters receive emails outlining the date/time and description of the event. (They also receive update emails if changes occur.)

Once it is time for the event, any user designated **Producer** in the event may click the **Start Webcast** button from the [Webcast Settings Dashboard](doc:webcast-settings-dashboard) to launch the event at the appropriate Start time.  (Note: Other users may have system-defined roles that allow them to start the event, but they will not receive the Producer interface or capabilities -- they must be defined as a Producer within the Event.)

<Image align="center" alt="Any Producer may click the Start Webcast button" border={false} caption="Any Producer may click the Start Webcast button" title="startProducerWebcast.png" src="https://files.readme.io/aa0e94d-startProducerWebcast.png" />

When a Producer starts the event, as each designated Producer and Presenter enters the event, they are prompted to configure their webcam, mic, and any screenshare _before_ they enter **Backstage**.  (Don't worry, they can always change it backstage as well.)  The Webcam and Mic may be configured to use any existing using appropriate USB or virtual device.  The ability for screen share is controlled by WebRTC (please see [Rev Sharing Control Options](doc:rev-sharing-control-options) for more details.)

Don't forget to click **Go Backstage** once all configuration is done! This is where you begin collaborating with other Producers and Presenters to "produce" the Live event for attendees.

<Image align="center" alt="Use the controls under the image to select your screen, your camera or your audio, and then select **Go Backstage**" border={false} caption="Use the controls under the image to select your screen, your camera or your audio, and then select **Go Backstage**" src="https://files.readme.io/716da77-goBackstage.png" />

> 👍 Tip
>
> Similar to a "normal" webcast, the event is not broadcasting or recording at this point.  The **Backstage** area is for **Producers** and **Presenters** only to collaborate on the look and feel of the production _before_ any scenes are pushed to live for attendees.
>
> The **Broadcast** button will not be enabled until shortly after your first scene is pushed to **Onstage** (described below).

Keep in mind that you can use the **Event Details** flyout panel at any time to modify your Producer **Event Settings** by clicking the **Edit Settings** button.

<Image align="center" alt={459} border={false} caption="Click the Event Details icon to access the Edit Settings button to modify the Producer event settings during the event" title="accessEventDetails.png" src="https://files.readme.io/910f8c4-accessEventDetails.png" />

After you click the **Edit Settings** button, click on the section you want to modify for your event.  Make sure you click the **Save** button to save your edit afterward.  You can also click the **Cancel** button if you change your mind.

<Image align="center" alt={499} border={false} caption="Expand the section you want to edit by clicking the + icon.  Make sure you Save your edit." title="editEventDetails.png" src="https://files.readme.io/6a93bb9-editEventDetails.png" />

## Producer Interface Overview

Once the event is started and the **Go Backstage** button is clicked by each Producer and Presenter, Rev "sets the stage" and each Producer and Presenter is placed together in the **Backstage**.  Everyone **Backstage** can hear and collaborate with each other.

The **Backstage** is just one part of the **Producer Environment**.  The easiest way to visualize the Producer environment is to think of it as a grid with three rows and two columns. It also has a flyout menu (only for Producers) that contains **Production Design** tools.

<Image align="center" alt={1165} border={false} caption="The **Producer Environment** includes the Staging, Scenes, and Backstage rows.  The flyout, with Design controls, is available only to **Producers**." title="uiOverview.png" src="https://files.readme.io/1d3fbef-uiOverview.png" />

### Staging (Preview and On Stage)

<Image align="center" alt="Stage your scene in the Preview window and then &#x22;push&#x22; it to the Onstage window to present it to attendees" border={false} caption="Stage your scene in the Preview window and then &#x22;push&#x22; it to the Onstage window to present it to attendees" src="https://files.readme.io/178023d-stagingRow.png" />

**Staging** is the top section where Producers design the scenes within the **Preview** and then push them **Onstage** for attendees of the webcast to see.  Presenters can also see the **Staging** section, but cannot change it.  Generally, the flow is: A layout is selected, speakers are then dragged from the **Backstage** to the **Preview** and, when ready, the **Send Live** button is clicked.

<Image align="center" alt="The double arrow is the &#x22;Send Live&#x22; button. It will move your Preview configuration to Onstage." border={false} caption="The double arrow is the &#x22;Send Live&#x22; button. It will move your Preview configuration to Onstage." title="pushToLive.png" src="https://files.readme.io/fe8e878-pushToLive.png" />

When **Send Live** is clicked, everything (and everyone) in the **Preview** window is "pushed" live to the **Onstage** window.  If you are broadcasting, this means that attendees can now hear and see the speakers.

### Audio Controls

You should familiarize yourself with Producer's various audio controls and where they are.

* Everyone **Onstage** can _only_ hear everyone else **Onstage**.
* Everyone **Onstage** can _not_ hear anyone who is only **Backstage**.
* Everyone **Backstage** can hear _all_ **Backstage** AND _all_ **Onstage** participants.

> 👍 Tip
>
> Keeping in contact with both **Backstage** and **Onstage** producers and presenters does take some practice!

Everyone has the ability to control what they hear Onstage and Backstage by using the audio controls when the **Speaker** icon is clicked.  Producers can also speak directly to _everyone_ Onstage by holding the **Speak To Stage** button.

<Image align="center" alt="Click the Speaker icon to use Onstage and Backstage audio controls" border={false} caption="Click the Speaker icon to use Onstage and Backstage audio controls" src="https://files.readme.io/e5deb22-personalAudioControls.png" />

The slider(s) control volume control for both Onstage and Backstage while clicking the speaker next to each will **mute** both areas entirely if needed.

Please note:

* Everyone can mute/unmute themselves (using their own A/V controls)
* Everyone can mute/unmute **Onstage** only for **themselves**
* Everyone can mute/unmute **Backstage** only for themselves
* Everyone can mute/unmute other individuals, but only for themselves -- not for the event.
* To speak to _all_ **Onstage** participants **Producers** can click and hold the **Speak To Stage** button.
* While Producer provides a great deal of mute/unmute capabilities, we recommend judicious use.

### Using Push to Talk During an Event

Producer features "push-to-talk" audio controls so Backstage Producers and Presenters can hold the push-to-talk control to speak to any other individual that is also **Backstage** and _only_ that target individual will hear what is said.  As noted above, **Producers** (only) can also hold the push-to-talk control to speak to any individual who is **Onstage** or to _all_ participants that are Onstage.

This feature is frequently used by Producers to work out production issues such as a Speaker being muted or to change a slide and so forth when the entire stage does not need to hear what is being said but only a specific participant.

<Image align="center" alt="Click the three-dot control for specific audio options for that specific person" border={false} caption="A Producer (only) can click and hold the push-to-talk control for a specific participant Onstage to speak directly to them" src="https://files.readme.io/726598a-pushToTalkControl.png" />

When a **Backstage Producer** clicks the push-to-talk control, the system performs the following steps:

* That Producer's audio is reduced slightly by 20% so that an audio cue to begin speaking can be heard.
* The Producer can then begin speaking to an _individual_ **Onstage** (seen above) or to _all_ Onstage participants depending on which control is being held.
* The targeted participants hear an audio cue (beep) to alert them there is an incoming message, the Producer's spoken message, and then another audio cue (beep) to alert them the message is over.  The audio cues are not added to the final video audio or Onstage audio.
* For **muted** Onstage presenters, only the Producers message audio is heard.

> 👍 Tip
>
> When using the push-to-talk feature, it is _highly_ recommended that ear pieces are used.
>
> Producers and Presenters that are **Onstage** _cannot_ use push-to-talk.  Only Backstage roles can use this feature to speak to Onstage participants.

### Scenes

<Image align="center" alt={1864} border={false} caption="Need to return to a particular scene?  Click on the scene in this row and back you go." title="scenesRow.png" src="https://files.readme.io/d8fc95d-scenesRow.png" />

There are times during an event when you need to quickly return to a preview you have already specified and used -- including the configuration of speakers, content shares, and backgrounds. These saved configurations are called "Scenes".

**Scenes** provide one-click access to your previous configurations and keeps them in order of use. Any configuration that is sent **Onstage** is immediately saved as a scene and placed in this row. This means you can immediately bring a scene back to the **Preview** window with a simple mouse click.

### Backstage

<Image align="center" alt="All collaborators in the webcast are in this row where they are dragged to the Preview window by Producers to create Scenes" border={false} caption="All collaborators in the webcast are in this row where they are dragged to the Preview window by Producers to create Scenes" src="https://files.readme.io/ce19842-backstageRow.png" />

The **Backstage** displays all collaborators in the production. The left side features your logged-in account and controls for your screenshare and/or webcam. You can modify your settings at any time during the event by using the sharing control buttons.

The right side of **Backstage** includes all other participants in the event.  All participants, according to mute/unmute settings, can communicate within the backstage (refer back to **Audio Notes** above.)  It is from the backstage that **Producers** click and drag participant's screenshare or webcam into the **Preview** window in **Staging** to create **Scenes** before pushing them to **Onstage** for attendees to view while broadcasting the event.

### Production Design Flyout

<Image align="center" alt={65} border={false} caption="Toggle layout and branding options" title="productionDesignIcon.png" src="https://files.readme.io/89eb4ea-productionDesignIcon.png" />

The **Production Design** flyout window, viewable only by **Producers**, can be toggled on and off and is used to build your **Preview** window which is eventually "pushed" **Onstage** to the attendees that are viewing your webcast.  You should think of this flyout as a toolset for customizing each Scene that you produce in your event.

Within the **Production Design** flyout, you will find several areas -- each controlling a different aspect of the scene you are creating.

<Image align="center" alt=" " border={false} src="https://files.readme.io/79f329a-layoutOptions.png" title="layoutOptions.png" />

#### Layout

Use the **Layout** options within the **Production Design** flyout to choose how you want to structurally present speakers and content within the frame of the scene.  Producers have several different options available and can click the **Show More** button to expand the area to view more, and a convenient way to quickly toggle and select 1, 2,3 ... up views.

**Layout Types and Behavior**

* Each **Layout** has numbered areas that represents where participant webcams or screen shares can be dragged and dropped into. Layouts are named based on number of "video areas" within each.  For example, a **1-Up** layout indicates there is one area for video while a **2-Up** means there are two areas for video that are side-by-side and so forth.
* Clicking on a Layout in the **Production Design** flyout will change the existing layout in the Preview Window -- the system will try to maintain any already selected streams.
* Clicking a specific Layout numbered area in the Preview window will remove any existing participant stream in that area

> 👍 Tip
>
> Non-specified areas in a Layout that are pushed Onstage will be transparent and the selected Background will display instead.

#### Background

<Image align="center" alt={461} border={false} caption="Select a pre-existing background or upload a custom background" title="backgroundOptions.png" src="https://files.readme.io/fdd5618-backgroundOptions.png" />

For your background color, Producer provides a few pre-existing colors that are applied behind the **Layout** window.  During set up or even during the event, a Producer may upload a custom background image as well.  The recommended image size is 1920 x 1080 (16:9 aspect ratio). Custom images appear behind the Layout, just as a background color appears.

<Image align="center" alt=" " border={false} src="https://files.readme.io/40c9027-brandingOptions.png" title="brandingOptions.png" />

#### Setting a Stream as a Background

Along with images, Producer also allows you to set either a Producer's or Presenter's stream as a background. Using streams as a background provides a more active and engaging presentation. To set a stream as background:

1. The Producer selects either a webcam or screen share of a Producer or Presenter. (Producers can even select from their own streams.)

2. In the example below, an HD ocean video streaming on YouTube is selected.  Producers can click on the "..." menu to access their background options.

<Image align="center" alt="Click Add Screen as Background on a streaming video to set it as the Producer Onstage background" border={false} caption="Click Add Screen as Background on a streaming video to set it as the Producer Onstage background" src="https://files.readme.io/7262661-addStreamBackground.png" />

3. Click **Add Screen as Background** to set the stream as the background in the **Preview** window.  This adds both the background audio as well as the microphone audio (for the stream owner).  The stream will be presented as the background within the **Preview** window and can be sent to **Onstage** from there when you are ready.

<Image align="center" alt=" " border={false} src="https://files.readme.io/5bbf910-streamingBackground.png" title="streamingBackground.png" />

When using streams as backgrounds, it is important to pay attention to the audio.  As mentioned above, both the microphone _and_ the streaming audio are added into the background.  If you are sharing a video stream -- you may want to mute the speaker audio.  Notice in the example above, the Speaker audio is muted.  This allows for a silent, but active, background stream to be added.  Of course, enabling the speaker microphone will allow for voiceovers.

When using backgrounds, streams, or images, you can also generate PIP (picture-in-picture) outputs.  As an example, you can set a stream or image background, select the 9-up "Brady Bunch" layout -- but only put one speaker into the 9th layout area.  Sending this live will leave all other (non-specified) layout areas transparent.  This is a very powerful capability for your Producer presentations.

> 📘 Note
>
> Backgrounds (static images or live streams) add production value to your event. However, backgrounds also increase the encoding complexity of the overall stream. The more detailed the background is in terms of objects, lines, and colors, the more complex it is. It takes more bits/bandwidth to provide a high-quality output when encoding a video with increased complexity. Producer currently uses the same settings as our VCI solutions, so it has upper limits for bitrate and resolution.
>
> Please test all your backgrounds (with foreground streams) for output encoding quality and, if necessary, consider reducing encoding complexity for better quality.

#### Banners

The **Banners** section is where you can specify if you want participant Names overlapped within their webcam video.  **Banners**, **Theme**, and **Accent Color** sections work together to apply light branding to your layouts and, more specifically, the speakers.

**Banners** can be toggled on and off and are, as mentioned, name tags for your speakers.  The **Theme** is the type of visual banner that is applied while the **Accent Color** is applied to it.

<Image align="center" alt={1449} border={false} caption="Branding options applied on a Townhall layout - Attendee's view" title="townhallAttendeeView.png" src="https://files.readme.io/1db1dce-townhallAttendeeView.png" />

## Designing a Scene

The single most _important_ aspect of Producer events is _designing Scenes_ for your event.  Simply put, the steps are:

1. Pick a **Layout** for the **Preview** window.
2. Add some participant streams (speakers or content)
3. Send it **Onstage**.
4. Repeat the process as many times as needed.

Most events will have several different **Scenes** that will be designed and toggled through during the event.

There are several different [Layout types](doc:produce-an-event#layout) (1-UP, 2-UPs, 3-UPs, etc.) that you can select for a **Scene**.

Click your desired **Layout** in the **Production Design** flyout to place it in the **Preview** window in **Staging**. It is ready to be filled by the **Backstage**.

<Image align="center" alt={491} border={false} caption="Selecting a layout option places it in the Preview window on the Staging Row" title="panelLayoutSelected.png" src="https://files.readme.io/31ee4b6-panelLayoutSelected.png" />

> 👍 Tip
>
> Click the **Show More** button to make sure you see all layout options available to you.

Once a Producer selects a layout, its blank form is placed in **Preview** and is ready to be filled with participants in the **Backstage** row.

<Image align="center" alt={1356} border={false} caption="The selected layout is blank until it is filled with Backstage members" title="panelLayoutPreview.png" src="https://files.readme.io/6d8eb5a-panelLayoutPreview.png" />

Producers click participants' (either **Presenters** or other **Producers**) webcam or even their shared screens and drag them to one of the numbered areas within the Preview Layout.

<Image align="center" alt={800} border={false} caption="Complete the Preview window by clicking and dragging options from the Backstage Row" title="panelLayoutPreviewComplete.png" src="https://files.readme.io/cc85bb9-panelLayoutPreviewComplete.png" />

Once the Preview window is complete, click the **Send Live** button to broadcast your **Scene** to attendees of the webcast.  Attendees view exactly what you have put together in Preview!

<Image align="center" alt={1386} border={false} caption="The Attendee view of a Panel layout" title="panelAttendeeView.png" src="https://files.readme.io/4889c40-panelAttendeeView.png" />

## Tips When Working Backstage

When working Backstage and collaborating with your fellow Producers and Presenters, here are some tips to keep your Production running smoothly and to make your experience running the event more intuitive and easier to use.

You can expand or collapse any of the Producer's rows at any time by using the arrows next to the row.  This gives you more "real estate" to work with if you need it.  The same is true with the **Production Design** flyout.  If you do not need a specific UI piece, you can close it.

The **Backstage Row** keeps track of all designated participants in the production so you do not start the event without a scheduled speaker being present.

<Image align="center" alt="Easily track who is supposed to be present before you begin Broadcasting" border={false} caption="Easily track who is supposed to be present before you begin Broadcasting" src="https://files.readme.io/c41b228-backstageCount.png" />

When you are designing layouts, you can choose what options to add for a Speaker such as audio only, audio and video, and so forth.

<Image align="center" alt={800} border={false} caption="You are able to see at a glance what Speakers are going to be Live next" title="speakerIcons.png" src="https://files.readme.io/2e25392-speakerIcons.png" />

Each **Speaker** card on the **Backstage Row** features a three-dot menu.  Roll over a card and use this menu to decide on options you want to add in the **Preview** window.  You can also just click and drag the Speaker to add them all.

<Image align="center" alt={222} border={false} caption="You can add different Speaker options to the Preview window" title="speakerDotMenu.png" src="https://files.readme.io/c78810b-speakerDotMenu.png" />

Muting a Speaker is visibly displayed in both **Preview** and **Onstage** windows by a red circle.

<Image align="center" alt=" " border={false} src="https://files.readme.io/fffb787-mutedSpeaker.png" title="mutedSpeaker.png" />

Keep in mind that, similar to all Rev events, Producer events keep you informed when you are Broadcasting.  You are also informed if the **Onstage** window is broadcasting in addition to the webcast itself.

<Image align="center" alt={1448} border={false} caption="You are told if the Onstage window is broadcasting" title="onstageBroadcasting.png" src="https://files.readme.io/52a8c7e-onstageBroadcasting.png" />

For Speakers in the **Preview** window, Producer also lets you know if you are queued to present next.  You are never caught unawares.

<Image align="center" alt=" " border={false} src="https://files.readme.io/196c6e1-speakerQue.png" title="speakerQue.png" />

Finally, all Producers and Presenters should review [Rev Screen Share and Webcam Best Practices](doc:rev-screen-share-and-webcam-best-practices) before getting started.
