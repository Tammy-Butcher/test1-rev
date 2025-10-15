---
title: Link and Redirect a Webcast Recording to a Completed Event
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
Linking and redirecting webcast recordings offers attendees the ability to seamlessly transition from viewing a live webcast to its recording once the event is complete. Event Hosts also control _when_ it is redirected so that it may be edited before it is viewed if desired.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b8433004ed7790d7ee6afc43be62d76ae837a7375d73e54a9670b8dbe8cd8e2f-enableWebcastLinkRedirects.png",
        "linkRedirect.png",
        "These two settings specify to link the webcast recording to the completed event and then to redirect attendees to the linked recording once you are done editing it"
      ],
      "align": "center",
      "caption": "These two settings specify to link the webcast recording to the completed event and then to redirect attendees to the linked recording once you are done editing it"
    }
  ]
}
[/block]


**Link ** a webcast recording to a completed event by enabling the **Associate and link webcast recording with the completed event** tab in the **Webcast Recording** section. You can enable it once the webcast has started or during set up.

When a webcast recording is **linked ** to a completed event:

- The event recording is automatically associated to the completed event for both manual and automated webcasts.
- In the event that multiple recordings took place during the webcast, the _last_ recording is associated upon event completion.

**Redirect ** attendees to a linked webcast recording by enabling the **Redirect attendees to linked webcast recording for the completed event** tab in the **Webcast Recording** section.

When attendees are redirected to a linked Webcast recording:

- Attendees visiting the event link after the webcast has completed (and event linking has been enabled) are redirected to the recorded video.
- If this setting is disabled, attendees visiting the event link after the Webcast has completed are redirected the **Webcast Landing Page** instead.
- Redirect settings also apply to embedded webcasts after the event ends.
- Keep in mind that the video must be also viewable by the attendee. That is, **Active**, not in a **Legal Hold**, part of an **Approval Process**, and so forth.

Account and Event Admins may use the **Edit **icon from the **Webcast Landing Page** to edit either setting link/redirect at any time. 

For example, you may decide to edit the event recording to a more professional version (or to remove sensitive information) and disable redirecting while doing so.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1d54f2-landingPageLinkRedirect.png",
        "landingPageLinkRedirect.png",
        722
      ],
      "align": "center",
      "caption": "You can disable redirecting from the Webcast Landing Page if needed to make necessary adjustments"
    }
  ]
}
[/block]


> 👍 Tip
> 
> If you are using **RTMP redundancy** and the **Backup Stream** feature enabled of an RTMP/S event, the Webcast link points to the last stream used once the event has concluded.