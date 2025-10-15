---
title: Set a Slide Delay
excerpt: Add a manual slide delay for live events
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The **Slide Delay** feature is used to further sync presentation slide transitions to ensure that Live Webcast video presentations are seamless. **This feature \_only \_applies to HLS video streaming Live on Webcasts and is an account level setting in that it affects \_all \_Webcasts.** You may override this setting at the zone level by specifying a different delay however.

To set a Slide Delay for presentation slides:

- Select the **Manual **option for **Slide Delay for HLS Live Video**
- Enter the **Delay in Seconds**. The **default **is 24 seconds. This is the number of seconds that will occur between _each_ slide transition.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/672441e-slideDelay.png",
        "slideDelay.png",
        ""
      ],
      "align": "center",
      "caption": "Enter the delay you want to occur between each slide transition. The default is 24 seconds."
    }
  ]
}
[/block]


Keep in mind:

- This feature is disabled by default which means the slides transition in real-time
- If the video is stopped, slides also transition in real-time
- If a user has control, slides transition in real-time
- If an HLS failover occurs, the automated delay in seconds occurs
- This is a global portal setting. You may override this setting for a specific zone in **Zone Settings**. **View**: [Add a New Zone](doc:add-a-zone#add-a-new-zone) > [Slide Delay for HLS Video](doc:add-a-zone#slide-delay-for-hls-live-video)