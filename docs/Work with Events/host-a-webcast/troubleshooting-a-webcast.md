---
title: Troubleshooting a Webcast
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
There are times when you may need to troubleshoot a Webcast after it has started.  This topic addresses methods to help you figure out what may go wrong during a Webcast and what you can do to find an issue and address it quickly to make sure it continues to run smoothly.

First, you should understand that most Webcast settings can be edited after it has started.  The means that if you have made a mistake during set up, it can be corrected.

## Edit a Webcast's Settings After it Starts

All Webcast settings may be edited once an event has started with the **_exception _**of the following which you may _not_ edit once an event has started:

- Closed Captions
- Listing Type
- Custom (Event-Friendly) URLs
- Lobby Time
- Video Source (you may [restart the source](doc:troubleshooting-a-webcast#restart-a-webcasts-video-source), in some cases, but not edit it)
- Start/End Date and Time
- Timezone

Make sure you understand what settings you need to have set up before your webcast starts and what you may edit “on-the-fly” during the event.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1fff501-editEventDetailsDuringEvent.png",
        "editWebcastDuringEvent.png",
        "Note you may need to expand the section you want to edit"
      ],
      "align": "center",
      "caption": "Note you may need to expand the section you want to edit"
    }
  ]
}
[/block]


- Click the **Edit Settings** button on the [Event Details](doc:host-a-production-webcast#view-details-for-the-webcast) form.
- [Webcast settings](doc:event-basic-settings) that are available for editing appear here.  You will need to expand the section you want to edit as needed.
- The new settings are available immediately to all attendees once you click **Save**.

## Restart a Webcast's Video Source

In the case of technical difficulties, Event Admins and Hosts have the ability to review the **Video Source** for the event in the **Event Details** (this requires clicking the **Edit Settings** button) [during an ongoing webcast](doc:troubleshooting-a-webcast#edit-a-webcasts-settings-after-it-starts).  The following video sources are currently supported for this feature:

- Video Address
- Microsoft Teams
- RTMP/RTMPS

Further, depending on the type of **Video Source** , you also have the ability to restart (or reconnect) to the video source such as displayed in the image below where the source is is a  **Microsoft Teams** URL.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ee6fe93-restartVideoSource.png",
        "",
        "Expand the Video Source section and click the Restart Video Source button to restart the webcast"
      ],
      "align": "center",
      "caption": "Expand the Video Source section and click the Restart Video Source button to restart the webcast"
    }
  ]
}
[/block]


Clicking the **Restart Video Source** button will restart the source without ending the event. You are also able to send a message to Attendees of the event that it is being restarted so there is no confusion as to what is occurring on their end.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5adef71224bb0bbaa0e84eb9979aff904da152c3fb91165f1098569947d1eaf-rtmpRestartVidSource.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


> 👍 Tip
> 
> Attendees of the event only see the **Message to Audience** that you enter.

Once the event has restarted, you must click the **Broadcast** button to begin broadcasting it again.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e24ca96-broadcastEventButton.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


> 📘 Note
> 
> Additional video sources will be added in the future as this feature continues to develop.

## Switch to a Backup RTMP Stream

If you have enabled RTMP redundancy and have a Backup Stream streaming, it is displayed in the** Video Source** section during a Webcast along with the **Primary Push URL** and **Stream Key**. If an issue occurs with the Primary Stream during the event, you can click the **Switch to Backup (Streaming)** button to seamlessly toggle to your backup stream (and then back again) easily.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/da45d83e59c11776bf08c6b8695d7e6d167fed7f57e6214db77a7946035f65bc-rtmpPrimaryStreaming.png",
        "",
        "When a Backup Stream is enabled for RTMP/S events, each stream is displayed as well as the ability to toggle between streams in the Video Source section"
      ],
      "align": "center",
      "caption": "When a Backup Stream is enabled for RTMP/S events, each stream is displayed as well as the ability to toggle between streams in the Video Source section"
    }
  ]
}
[/block]


> 🚧 Important!
> 
> When switching streams, audio settings for both the Host/Admin players and the Attendee's players revert to default audio settings. For example, this means that if a player is muted, it will unmute each time a stream is switched.

## Troubleshooting Webcast Failures

There are times when a Webcast fails to start during initial start. For example:

- At the beginning of the RTMP/S sourced event, if issues occur within the infrastructure, for whatever reason, you will shortly return to the Webcast details page.  You can then select the **Restart Webcast** button at that time.