---
title: Video Languages
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
To update **Video Settings** in Rev:

1. Navigate to a video and hover over the **Video Settings** button in the top right corner.

2. Click **Details ** from the options that appear.  Several tabs appear that allow you to create and modify the video's metadata. Select a tab depending on which setting you want to update. 

3. This feature is a **Languages Setting**.

When a video is uploaded, you can view global language and transcription options that were set by the Account Admin for your portal videos.

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > **Languages** tab option.

2. Use this tab to view the **Default Transcription Language** on the top row and to view the **Default Translation Languages** that the video audio was automatically translated to (if any). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8655919-languagesTab.png",
        "revIQTranscription.png",
        370
      ],
      "align": "center",
      "caption": "The Languages tab displays default transcription and translation languages that are set for video uploads"
    }
  ]
}
[/block]


3. The **Default Translation Languages** (in this example, French and Spanish) are listed in alphabetical order under the **Default Transcription Language** (English) on the top row. 
4. Note that your Account Admin must configure [automatic and default transcription/translation](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings) options for these to be present.

## View or Set a Video's Audio Track

When a video is uploaded, Rev attempts to detect the language of its audio track where it is then merged with its default transcription language in the top row of the Languages tab when they match.  In this case, the first row appears similar to the image below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d71463-mergedAudioSubtitleTrack.png",
        "",
        "Rev attempts to automatically detect the audio track in an uploaded video"
      ],
      "align": "center",
      "caption": "Rev attempts to automatically detect the audio track in an uploaded video"
    }
  ]
}
[/block]


There are certain [supported video types](doc:supported-file-types) that do not have a language code in their file which is what Rev needs to detect the audio track.  When this occurs, the top row of the **Languages** table returns **Unknown**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d46770c-unknownAudioTrack.png",
        "",
        "Unknown is returned if the video language cannot be detected by Rev"
      ],
      "align": "center",
      "caption": "Unknown is returned if the video language cannot be detected by Rev"
    }
  ]
}
[/block]


This issue can be corrected by clicking the **Select** button, selecting the language used in the video which is most often the **Default Transcription Language**, and then clicking the **Save** button.  The audio track is then merged with the transcription file on the top row as expected.

> 📘 Note
> 
> The video format types that do _not_ have a language code specified in the file (along with legacy/historical videos and those created by Rev via webcast recording) include the following:
> 
> - avi
> - flv
> - mp3
> - mpg (mpeg-1)
> - mp4

## Edit, Download, or Delete Subtitles

The **Default Transcription Language** and **Audio Track** is the top row on the **Languages** tab.  You can edit this language by using the **Actions** kebab menu next to the row.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/43c0e5d-languageActionsMenu.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


To edit, download, or delete a subtitle file:

1. Click the **Actions** kebab next to the row on the **Languages** tab.  
2. Click **Edit Language** if you want to modify the default language file.  You may only update the original transcription file and not the subtitles files that were default translations.  To do this, you need to add a new language.
3. Click the **Select** button to choose the new language.
4. Click the **Save** button.  One the video finishes processing, the new subtitle file is available.
5. You can also use this menu to **Download** or **Delete** subtitle files.  Please note that if you delete a subtitle file, this action is not saved until you click the **Save** button.

## Auto-Generate a New Subtitle File

If you want additional subtitles and languages added to your video once it has uploaded you may do so using the **Add Language** button.  You can then choose to auto generate the subtitle file or manually upload the require .srt file.  Keep in mind, you must have a completed transcription file as a source file in place.  It can be one that you manually identify or one that Rev has auto-detected as described in the section above.

> 🚧 Important!
> 
> Be aware that translation services cost a portion of **Rev’s AI licensing services** in the form of **Rev IQ** credits and you should always check with your Account Admin before using.

To translate your transcription file into additional languages:

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > **Languages** tab option.
2. Click the **Add Language** button.
3. Select one of the [Supported Languages](doc:supported-languages) from the dropdown that appears.  It will be added to the **Languages** table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb5c1c2-addAdditionalLanguages.png",
        "",
        "Add more languages you want to create subtitles for to by clicking the Add Language button first. They are added to the Languages table."
      ],
      "align": "center",
      "caption": "Add more languages you want to create subtitles for to by clicking the Add Language button first. They are added to the Languages table."
    }
  ]
}
[/block]


4. Click the **Add**  button next to the language you are translating.  You are prompted to choose a **Source Language** as the basis for the translation.  Once you identify the source, click the **Auto Generate** button to have a subtitle file created in the language you have specified.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/751e427-subtitleOptions.png",
        "",
        "Choose your Source Language and Auto Generate your new Subtitle File"
      ],
      "align": "center",
      "caption": "Choose your Source Language and Auto Generate your new Subtitle File"
    }
  ]
}
[/block]


4. If you are using the [VoiceBase](doc:voicebase) integration for transcription, you can choose this service to auto-generate your file in this step.

> ❗️ Caution!
> 
> If you have both **Rev IQ** and **VoiceBase** transcription services enabled, you may only use Rev IQ in this step.  VoiceBase will _not_ be available to add and translate additional subtitle files.

5. Once started, you do not need to wait for a video to finish the transcription process before exiting Video Settings. You may download or delete the generated file just as if you had uploaded the file yourself by using the **Download **and **Delete ** action links.

Please note:

- If there is no audio file, an audio-only mp3 from the original video is transcribed and saved with the video.
- During playback, an audio-only option is not displayed.
- If the video is edited, replaced, or deleted, so is the audio file.

To edit the generated file and add additional formatting, you need to **Delete **the current file that is attached to the video (after you **Download **it first to edit it) before you use the **Upload Subtitles** tab to reattach the edited file.

> 👍 Tip
> 
> All video files that can be [uploaded and transcoded](doc:supported-video-and-audio-formats) in Rev are also supported by Rev IQ transcription and translation.

> ❗️ Warning!
> 
> If you have previously generated a transcription file, this file is overwritten if you choose the same language to generate again.

## Upload and Attach a Subtitle File

**Subtitles ** can also be manually added to video uploads by attaching various **SubRip (SRT)** files to the video in any of Rev's [Supported Languages](doc:supported-languages). You may upload a .srt file with formatted or non-formatted text in Rev; both are accepted.  You may also use formatted and non-formatted text in the _same _.srt file if desired.

> 👍 Tip
> 
> Subtitle (srt) files are _not_ the same as enabling **closed captions (cc)** for a video. A subtitle file can be created in the language of your choice and you also have a great deal of control over formatting options. Subtitles are normally concerned with _only_ the _spoken_ words in a video.
> 
> **Closed captions** are encrypted within the video file itself and you have less control over formatting. Further, closed captions normally also convey additional items other than the human voice such as sound effects occurring during the video (breaking glass, music playing, and so forth).

To upload and attach a subtitle (srt) file to a video:

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > **Languages** tab option.
2. Follow **steps 1 - 3** in the [Auto-Generate a Subtitle File](doc:video-languages#auto-generate-a-new-subtitle-file) section above.
3. After clicking the **Add** button next to the language, click the **Upload Subtitles** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/860968f-addManualSubtitle.png",
        "uploadSubtitle.png",
        527
      ],
      "align": "center",
      "caption": "Click the Upload Subtitles option to upload a .srt file"
    }
  ]
}
[/block]


> 📘 Note
> 
> The following text formats are supported:
> 
> - Bold
> - Italic
> - Underlined
> - Line Breaks

6. Once saved, the new subtitle language appears within the language icon on the [video player](https://revdocs.vbrick.com/docs/rev-video-player-features) so that users can select subtitles in languages that you have added or auto-generated.

## Generate Subtitles with Rev IQ or VoiceBase

If your Account Admin has enabled [Rev IQ Transcription and Translation](doc:rev-iq-transcription-and-translation) services or the [VoiceBase](doc:voicebase) integration, you may generate a SubRip (SRT) file directly in Rev rather than uploading a file.  

Additionally, **Rev IQ Transcription and Translation** services allow you to translate your file into additional supported languages at the same time and define a [custom dictionary](doc:rev-iq-transcription-and-translation#create-a-custom-dictionary) to assist with company brands and speakers.