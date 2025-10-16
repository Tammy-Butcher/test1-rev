---
title: Rebroadcast an Existing Video
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
When you rebroadcast an [existing video](doc:video-sources#existing-video-sourced-events) as a "Live" webcast, many of the same controls you use when you [Host a Production Webcast](doc:host-a-production-webcast) for managing attendees and invites are still used.

In addition, hosting the event itself is also similar.  Hosts should be aware of the following settings for rebroadcasting:

* [Pre-Production](doc:prepare-a-dry-run) settings are available should you want to host a dry run
* The [Automated Webcast](doc:video-sources#automated-webcasts) setting is disabled by default. If this were to be enabled, you must manually begin the webcast.
* The [Autoplay](doc:video-sources#autoplay-a-webcast) setting is also enabled by default.

When the automated webcast setting is enabled, it means that both Hosts and Attendees are presented the [Lobby Time](doc:event-basic-settings#lobby-time) screen (if configured) prior to the start of the event with a message that the broadcast is starting soon.

Hosts are able to see the details of the VOD asset that has been selected as the source, and view a 15-second preview of it if desired.

<Image align="center" alt={1861} border={false} caption="Event Hosts are able to preview the VOD source before the event begins" title="rebroadcastPreview.png" src="https://files.readme.io/6cc80b0-rebroadcastPreview.png" />

When automated webcast is enabled, just above the preview window a countdown appears when the event is about to begin.

<Image align="center" alt={426} border={false} caption="A countdown appears when the broadcast is about to begin" title="vodCountdown.png" src="https://files.readme.io/6c4edd9-vodCountdown.png" />

Once the webcast begins, there is a status bar that indicates to Hosts that attendees can now see the event and that a VOD is being broadcasted.

<Image align="center" alt=" " border={false} src="https://files.readme.io/8d3442b-vodEventStatus.png" title="vodEventStatus.png" />

[Polls, chat, and Q&A](doc:controlling-attendee-engagement) functions are available (if configured during set up).

<Image align="center" alt=" " border={false} src="https://files.readme.io/1027131-vodAttendeeEngage.png" title="vodAttendeeEngage.png" />

You are also able to see the **Event Details** and Host controls (with an option to switch to **Manual Control** if needed which allows you to End the event).

<Image align="center" alt=" " border={false} src="https://files.readme.io/13aabb2-hostManualControl.png" title="hostManualControl.png" />

Keep in mind that if you switch automated control off by clicking the **Manual Control** button, you will either have to manually start the broadcast or have the option to end it depending on if the event has started.

For example:

If the Broadcast has **not** started, the **Broadcast** button is shown and the status banner displays: "Attendees cannot see the event.  When you are ready, click "Broadcast" to start the video on demand playing and to enable attendees to view the event".  You are also able to click the **End Event** button when you are ready to end the event.

If the Broadcast has _started_, the **Pause Broadcast** button is shown instead and the status banner displays: "Attendees can see the event. You are broadcasting the video on demand file to your audience". You are also able to click the **End Event** button when you are ready.

When rebroadcasting an existing video:

* The **Recording** button is not available
* The **Slides** button is disabled as slides are not supported
* Starting a webcast starts the event just as if it were a "Live" webcast
* Beginning a broadcast begins the VOD source to start playing for all attendees
* The video cannot be fast forwarded or rewound
* Once the webcast is ended, it cannot be restarted
* There is no outward indication to an attendee that they are watching a pre-recorded video.  From their perspective it is a "Live" event.
