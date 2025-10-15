---
title: Manage Transcoding Settings
excerpt: >-
  Understanding transcoding in Rev and how to edit the default settings to
  create your own profiles
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
The **Transcoding **menu displays the recommended transcoding presets included out-of-the-box with Rev and their status.  You can use this form to add new presets, duplicate a preset, or delete a preset.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6b0541c-transcodingMenu.png",
        "transcodingMenu.png",
        805
      ],
      "align": "center",
      "caption": "Transcoding options are accessed through the Media Settings > Transcoding menu"
    }
  ]
}
[/block]

## Transcoding Preset Default Settings

By default, six transcoding presets are configured when your portal is installed. These six presets have been carefully tested and authenticated and are the recommended settings to use to transcode a stored file from one video encoding format to another. They are seen in **Table 1** below.

For example, when adding a stored MP4 video, the file can automatically be transcoded to H.264 or HLS format. The presets defined below are used to configure the bitrate, frame rate, aspect ratio, and so forth of the transcoded output.

Admins can also specify which user actions or “rules” prompt transcoding to occur such as when users add or record a video. If set, when a user performs the action specified, a list of the transcoding presets selected appear for the user to select.

**Table 1: Transcoding Preset Descriptions and Encoding Output Types** 

| Preset Name                      | Description                                                                                                                            | Encoding Output |
| :------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- | :-------------- |
| Standard Definition              | Distribution Method: Supports a broad range of Internet connections. Target Displays: Works best for embedding on Web pages.           | H.264           |
| High Definition 720p             | Distribution Method: Best for higher Internet Speeds or Corporate Intranet. Target Displays: Tablets, TVs, and full screen PC viewing. | H.264           |
| High Definition 1080p            | Distribution Method: Corporate Intranet. Also useful for local archival and playback. Target Displays: TV, full screen PCs.            | H.264           |
| 360 Video 1080p                  | Distribution method: WiFi, 4G+ and Intranet. Delivery: Windows 7 IE11 and other browsers that cannot play HLS                          | H.264           |
| Adaptive Streaming               | Distribution Method: WiFi or 4G+ Delivery Method: iOS and Android smartphones and tablets.                                             | HLS             |
| Adaptive Streaming for 360 Video | Distribution method: WiFi, 4G+ and Intranet. Target Displays: full screen PCs                                                          | HLS             |

Each preset has additional attributes such as an average bit rate versus a peak bitrate setting defined for video and audio.

**Table 2: Transcoding Preset Attributes**

[block:html]
{
  "html": "<table style=\"border-collapse:collapse;border-color:#ccc;border-spacing:0\" class=\"tg\"><thead><tr><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\" colspan=\"2\">Preset Name</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Video Bitrate</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Avg. Bitrate</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Peak Bitrate</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Frame Width</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Frame Height</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Audio Codec</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Audio Bitrate</th><th style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">Audio Sample Rate</th></tr></thead><tbody><tr><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal\" colspan=\"2\">Standard Definition</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">800</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">1100</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">640</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">AAC-LC</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">96</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">48</td></tr><tr><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal\" colspan=\"2\">High Definition 720p</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">2100</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">3000</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">1280</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">AAC-LC</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">128</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">48</td></tr><tr><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal\" colspan=\"2\">High Definition 1080p</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">4000</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">5400</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">1920</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">AAC-LC</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">160</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">48</td></tr><tr><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal\" colspan=\"2\">360 Video 1080p</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">2000</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">2200</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">1080</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">AAC-LC</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">160</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">48</td></tr><tr><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal\">Adaptive Streaming</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">1.<br>2.</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">2962<br>1296</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">1280<br>640</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">AAC-LC</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">128</td><td style=\"background-color:#fff;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">44.1</td></tr><tr><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal\">Adaptive Streaming for 360 Video</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">1.<br>2.<br>3.<br>4.</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">8000<br>5000<br>2000<br>1200</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">2160<br>1440<br>1080<br>720</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\"></td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">AAC-LC</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">160</td><td style=\"background-color:#f6f8fa;border-color:inherit;border-style:solid;border-width:1px;color:#333;font-family:Arial, Helvetica, sans-serif !important;;font-size:14px;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal\">48</td></tr></tbody></table>"
}
[/block]



Each transcoded instance of the video is viewable in **Video Settings** and also presented to the viewer of the video in the video player. 

- [View Transcoded Video Instances](doc:update-advanced-video-settings#view-transcoded-video-instances)
- [Rev Video Player Features](doc:rev-video-player-features#playback-bar-functions)

Note the following about playback options when more than one transcoded instance of the video is available:

- Auto where auto = HLS or the lowest quality stream available.
- Each available video quality where the transcoding output type = H.264.

> ❗️ Warning!
> 
> Safari browsers do \_not \_play MP4 videos from Rev when the 1080p original transcoding option is selected. To use this playback option, the user should clear browser cache and then make sure that the **Always Allow** option is selected for **Cookies and Website** data under **Privacy **data.

## Modify a Default Transcoding Rule

Transcoding occurs, with one or more transcoding presets selected, when a user performs the following actions:

- Adds a Video
- Adds a 360 Video
- Records a Video

By default, transcoding rules select the **High Definition 720p** preset for each action and ingests the original file after transcoding.

[block:parameters]
{
  "data": {
    "h-0": "Action",
    "h-1": "Transcoding Preset",
    "h-2": "Ingest Original File",
    "0-0": "User Adds a Video",
    "0-1": "High Definition 720p",
    "0-2": "Yes",
    "1-0": "User Adds a 360 Video",
    "1-1": "- Adaptive Streaming for 360 Video  \n- 360 Video 1080p",
    "1-2": "Yes",
    "2-0": "User Records a Video",
    "2-1": "High Definition 720p",
    "2-2": "Yes"
  },
  "cols": 3,
  "rows": 3,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]

Account Admins and Media Admins may view and edit transcoding rules.

Keep in mind:

- Admins may select additional transcoding presets used for an action; or change the current transcoding preset used.
- Admins can specify that no transcoding should occur for a given action
- Admins can specify whether the original file should be transferred to DMEs
- Ingesting the original file is different from “keeping” an original file in Rev. Rev always keeps an original file even if ingest is unchecked. However, some distinctions apply and should be noted:
  - If the **Ingest Original** (file) checkbox is enabled, Rev also ingests the file to DMEs. This is a subtle but important distinction.
  - If the **Ingest Original** checkbox is enabled along with the [Enable Playback During Transcoding](doc:allow-playback-during-transcoding) setting, then users are allowed to watch the video via the _original instance_ during the transcoding process of the video.
  - If the **Ingest Original** checkbox is enabled then the video playback options (in the player playback selection) include original video playback.

To edit a default transcoding rule setting:

1. Navigate to **Media Settings > Transcoding**.
2. Click the **Settings** button and click **Edit **next to the action you want to modify.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d942a6-editDefaultTranscodingAction.png",
        "editDefaultTranscodingAction.png",
        805
      ],
      "align": "center",
      "caption": "Click the Edit link next to a Default setting to modify what occurs when an action is taken"
    }
  ]
}
[/block]

3. Click on a format in the **All **column to add it to the **Assigned Preset** column.
4. To remove a format, click on it in the **Assigned Presets** column and the format is removed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6dea74b-transcodingAssignedPresets.png",
        "transcodingAssignedPresets.png",
        521
      ],
      "align": "center",
      "caption": "Add and remove settings to the Assigned Presets column to modify a setting"
    }
  ]
}
[/block]

5. Click **Save Changes**.
6. The action (when performed) now transcodes video into the new settings and the modified preset is selected.

> 📘 Note
> 
> To transfer the original video to DMEs after transcoding, click the **Ingest Original** checkbox. You may not have transcoding disabled for a rule (no preset selected) and have **Ingest Original** deselected for the same setting.

## Add a New Transcoding Rule

By default, four transcoding presets are configured when your portal is installed. These four presets have been carefully tested and authenticated and are the recommended settings to use for most of your transcoding needs. Should you decide you need additional transcoding presets, you may easily define them. It is recommended that you work with Vbrick Professional Services to define your own settings.

> 👍 Tip
> 
> You do not have to add a preset from scratch if a default preset has most of the settings you need. Use the **Duplicate Preset** icon in the **Actions **column to copy the preset and then edit the parameters you need. More importantly, the format of the original preset is preserved.

To add a new transcoding preset:

1. Navigate to **Media Settings > Transcoding**.

2. Click the **Add Preset** button and complete each section of the form.

### Preset Name and Description

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1ff5088-transcodingNameDescription.png",
        "transcodingNameDescription.png",
        802
      ],
      "align": "center",
      "caption": "Enter a name and description for your new Preset"
    }
  ]
}
[/block]

- **Preset Name** - Choose a descriptive name for the preset.
- **Description **- A meaningful description of what the preset is intended to do.
- **Status **- Status of the preset. Active is the default.

### Video Settings

- **Transcoding Output Type** - The type of output that is produced. For suggestions on best practices, see [Transcoding Preset Default Settings](doc:manage-transcoding-settings#transcoding-preset-default-settings)
- **Transcoding Profile** - Profiles control which encoding techniques are used to produce the encoded output. The **Baseline **profile should be selected to produce a file that plays on devices with minimal CPU power and memory whereas the **High **profile may be used to produce output that plays using more powerful platforms (most computers built in the last five years play output produced using the **High **profile). Note that **Baseline**, **Main**, and **High **profiles are only applicable to H.264 outputs.
- **Codec **- This value is automatically set based on the **Transcoding Output Type** selected.
- **Prevent Upscale** - If _enabled_, Rev only transcodes using the preset if the input file’s resolution is greater than or equal to the resolution specified for H.264 and WM outputs. For HLS, Rev transcodes to all resolutions in the preset that are less than or equal to the resolution of the input file. If _disabled_, Rev transcodes to the preset regardless of the input file’s resolution for H.264 and WM. For HLS, Rev transcodes to all resolutions specified in the preset. If the input video’s resolution is less than that indicated by the preset, the video is scaled up to meet the dimensions specified. The recommended best practice is to disable this attribute for the lowest resolution preset. This ensures that all files are transcoded to at least one preset with higher resolution files being generated as well if the input file is a higher quality file.
- **Key Frame Interval** - Specifies the number of seconds between key frames.
- **Frame Rate (FPS)** - Specifies the number of frames per second for the transcoded video. This may be explicitly set or it can be left as the same as the incoming video by selecting “source”.
- **Aspect Ratio** - Specifies the aspect ratio of the output frame (proportional relationship between the width and height of the output video and typically expressed in 4:3 and 16:9 in video); choose **Source **to match the aspect ratio and pixel aspect ratio of the source file being transcoded.
- **Bitrate Type** - **Constant **versus **Variable**. Refers to amount of output data that is consumed per time segment.
- **Dimensions and Quality** -Select the target **width**, **height**, and **bitrate**.

### Audio Settings

- **Codec **- This value is automatically set based on the Transcoding Output Type that is selected.
- **Bitrate **- Specifies the bitrate (kilobits per second) of the audio. The higher the bitrate, the more space it will take.
- **Sample Rate (kHz)** - Specifies the sample rate of the audio. Current professional/consumer standards for recording and playback are 128 and 48 kHz.