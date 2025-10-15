---
title: Video Languages
excerpt: >-
  Manage Rev's various transcription, translation, and audio track abilities
  that may be added and generated for a video.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
To update **Video Settings** in Rev:

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > **Languages** tab option.

2. Click **Details ** from the options that appear.  Several tabs appear that allow you to create and modify the video's metadata. Select a tab depending on which setting you want to update. 

3. This feature is a **Languages Setting**.

When a video is uploaded, you can view global transcription and translation options that have been set by the Account Admin for your portal videos. Once enabled, you also have the ability to generate up to ten audio tracks for the languages that are supported if they have a transcription file.

> 📘 Note
> 
> [Audio Track Generation](doc:rev-iq-transcription-and-translation#allow-ai-generated-voices-for-audio-tracks) must be enabled by your Admin before you can use this feature. View a list of [Supported Languages](doc:supported-languages) for both [transcription and translation](doc:supported-languages#vod-transcription-and-translation-subtitles-for-rev-iq) options and [audio/voice language](doc:supported-languages#vod-audio-and-voice-language-support-for-rev-iq) support.

The **Languages** tab is used to view the **Automatic Transcription Language** and voice **Audio Track** on the top row and becomes the video's default row.  Your Account Admin can specify that the automatic transcription language is also automatically translated into additional languages when a video is uploaded. 

If this is the case, the **Automatic Translation Languages** and subtitles that the video is translated to when uploaded are displayed in subsequent rows beneath the top default language row. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/78406b409153e5efd8ad01b2edba071b5c64499f62a695e75ffb47e077d9efe4-languagesTab.png",
        "revIQTranscription.png",
        "The Languages tab displays default transcription and translation languages that are set for video uploads"
      ],
      "align": "center",
      "caption": "The Languages tab displays default transcription and translation languages that are set for video uploads"
    }
  ]
}
[/block]


In the image above, when the video is uploaded, the **Automatic Transcription Language** and voice **Audio Track** (English) are displayed on the top row and become the default. The Account Admin also configured automatic translation to occur in French and Spanish and, as a result, the **Automatic Translation Languages** rows are listed in alphabetical order _under_  the English file default row.  You can specify that a [voice Audio Track be generated](doc:adding-alternative-audio-tracks-to-a-video) for those rows as well.

As mentioned,  your Account Admin must configure [automatic transcription and translation](doc:rev-iq-transcription-and-translation#automatic-transcription-settings) options for these options to be present.