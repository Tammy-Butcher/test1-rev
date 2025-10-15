---
title: Closed Captions Set Up
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
If your stream includes embedded 608/708 closed captions, you may enable the player to display them by clicking the **Enabled **button under **Closed Captions** in the **Video Source** section. Closed captions are actually embedded in video stream. These are not to be confused with [Vbrick Rev IQ Subtitles](doc:update-advanced-video-settings#generate-subtitles-with-rev-iq-or-voicebase), which are provided for the stream separately.

Requirements:

* A **Presentation Profile** video source must be used
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/24aed7e-closedCaptionsWebcasts.png",
        "closedCaptionsWebcasts.png",
        706,
        70,
        "#eff2f4"
      ]
    }
  ]
}
[/block]
When **Closed Captions **are enabled:

* A closed caption (CC) toggle is visible on the webcast video player just as it is on the VOD video player
* This setting requires that you have closed captions embedded in your stream
* Closed captions are only available for RTMP and HLS for HTML5 players
* If closed captions are enabled, they are displayed only if available for the video