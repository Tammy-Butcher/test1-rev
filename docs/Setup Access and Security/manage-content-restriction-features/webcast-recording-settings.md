---
title: Webcast Recording Settings
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
The **Webcast Recording** section determines how webcast and meeting recordings are handled and displayed in the portal. You can specify if it is allowed, required, or disabled entirely. Depending on the setting selected, Rev’s UI is modified in both events setup and in the upload tray **Recording **tab when recording video conferences.

For example, if webcast recording is set to required, the Event Host no longer needs to remember to click the **Record **button when broadcasting begins because Rev automatically records all webcasts. The **Webcast Recording** section in the event setup is no longer visible as a result.  How each setting affects the recording function and UI display is described in the table below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7f31f80-enableWebcastRecording.png",
        "enableWebcastRecording.png",
        502
      ],
      "align": "center",
      "caption": "The Webcast Recording setting determines how webcast and meeting recordings are handled in Rev; the default setting is to allow recording."
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Allow",
    "h-1": "Disable",
    "h-2": "Require",
    "0-0": "Use this option to give Hosts a choice to record.",
    "0-1": "Use this option to disable recording entirely.",
    "0-2": "Use this option to have all webcasts begin recording automatically when Hosts begin broadcasting.",
    "1-0": "The [Recording](doc:stream-and-record-video) tab in the video upload tray is visible.",
    "1-1": "The [Recording](doc:stream-and-record-video) tab in the video upload tray is _not_ visible.",
    "1-2": "The [Recording](doc:stream-and-record-video) tab in the video upload tray is visible.",
    "2-0": "Webcast recording is optional. The [Webcast Recording](doc:webcast-recordings) section in an event setup is visible.",
    "2-1": "All webcasts are created with recording disabled. The [Webcast Recording](doc:webcast-recordings) section in an event setup is _not_ visible.",
    "2-2": "All webcasts are created with recording required and automatic. The [Webcast Recording](doc:webcast-recordings) section in an event setup is _not_ visible.",
    "3-0": "The **Automatic Recording** tab is visible during event setup.  \n  \n  - If disabled, the Event Host is able to manually start and stop recording the webcast.  \n  \n  - If the automatic recording tab is enabled, the webcast automatically begins recording when the Event Host begins broadcasting. The Host can choose to stop and start recording at any time.  \n  \n- Automatic recording is enabled by default, but can also be set via a [template](doc:create-a-webcast-template).",
    "3-1": "The [Record](doc:host-a-production-webcast#recording-the-webcast) button is _not_ visible during a webcast.  \n  \n- If a [template](doc:create-a-webcast-template) is applied with recording options set, it is overridden with recording options disabled.  \n  \n- If an API user attempts to enable recording or start recording during a webcast, an error is generated.",
    "3-2": "- As soon as the Event Host begins **Broadcasting**,  the webcast records automatically.  \n  \n- If a [template](doc:create-a-webcast-template) is applied with recording options set, it is overridden with recording options required.  \n  \n- If an API user attempts to disable recording during setup or stop recording during a webcast, an error is generated."
  },
  "cols": 3,
  "rows": 4,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]

> 🚧 Important!
> 
> Some webcast video sources will disable and/or hide the **Webcast Recording** section of an event even if it is enabled in the **Webcast Recording Settings** described in this topic.  This includes using an [existing video](doc:video-sources#existing-video-sourced-events) as a video source.