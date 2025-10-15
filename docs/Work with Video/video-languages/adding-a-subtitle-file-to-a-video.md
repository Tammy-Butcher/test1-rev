---
title: Add a Subtitle File to a Video
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
If your Account Admin has enabled [Rev IQ Transcription and Translation](doc:rev-iq-transcription-and-translation) services, you may generate a **SubRip (SRT)** file directly in Rev rather than uploading a file.  

Additionally, **Rev IQ Transcription and Translation** services allow you to translate your file into additional supported languages at the same time and define a [custom dictionary](doc:rev-iq-transcription-and-translation#create-a-custom-dictionary) to assist with company brands and speakers.

If you do not have Rev IQ enabled, you also have the option of manually uploading a Subtitle file to your videos.

> 📘 Note
>
> To add voice **Audio Tracks** in various languages, a Subtitle file in that language must be added first.

## Auto-Generate a New Subtitle File

If you want additional subtitles and languages added to your video once it has uploaded you may do so using the **Add Language** button.  You can then choose to auto-generate the subtitle file or manually upload the require .srt file.  Keep in mind, you must have a completed transcription file as a source file in place. 

> 🚧 Important!
>
> Be aware that translation services cost a portion of **Rev’s AI licensing services** in the form of **Rev IQ** credits and you should always check with your Account Admin before using.

To translate your transcription file into additional languages:

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > **Languages** tab option.
2. Click the **Add Language** button.
3. Select one of the [Supported Languages](doc:supported-languages) from the dropdown that appears.  It will be added to the **Languages** table.

<Image alt="Add more languages you want to create subtitles for to by clicking the Add Language button first. They are added to the Languages table." align="center" src="https://files.readme.io/8f9e3daf0bd25b30f4052fc79ef8a43eaef9d7c93818b624e6fdd29cfc1272d1-addAdditionalLanguages.png">
  Add more languages you want to create subtitles for to by clicking the Add Language button first. They are added to the Languages table.
</Image>

4. Click the **Add**  button next to the language you are translating.  You are prompted to choose a **Source Language** as the basis for the translation.  Once you identify the source, click the **Auto Generate** button to have a subtitle file created in the language you have specified.

<Image alt="Choose your Source Language and Auto Generate your new Subtitle File" align="center" src="https://files.readme.io/f7a12e47ae7649558aeefc9efe1b860a1cdb7e0f2aa5986b4992485e15b95f17-subtitleOptions.png">
  Choose your Source Language and Auto Generate your new Subtitle File
</Image>

5. Once started, you do not need to wait for a video to finish the transcription process before exiting Video Settings. You may download or delete the generated file just as if you had uploaded the file yourself by using the **Download** and **Delete** action links.

Please note:

* If there is no audio file, an audio-only mp3 from the original video is transcribed and saved with the video.
* During playback, an audio-only option is not displayed.
* If the video is edited, replaced, or deleted, so is the audio file.

To edit the generated file and add additional formatting, you need to **Delete** the current file that is attached to the video (after you **Download** it first to edit it) before you use the **Upload Subtitles** tab to reattach the edited file.

> 👍 Tip
>
> All video files that can be [uploaded and transcoded](doc:supported-video-and-audio-formats) in Rev are also supported by Rev IQ transcription and translation.

> ❗️ Warning!
>
> If you have previously generated a transcription file, this file is overwritten if you choose the same language to generate again.

## Upload and Attach a Subtitle File

**Subtitles** can also be manually added to video uploads by attaching various **SubRip (SRT)** files to the video in any of Rev's [Supported Languages](doc:supported-languages). You may upload a .srt file with formatted or non-formatted text in Rev; both are accepted.  You may also use formatted and non-formatted text in the *same* .srt file if desired.

> 👍 Tip
>
> Subtitle (srt) files are *not* the same as enabling **closed captions (cc)** for a video. A subtitle file can be created in the language of your choice and you also have a great deal of control over formatting options. Subtitles are normally concerned with *only* the *spoken* words in a video.
>
> **Closed captions** are encrypted within the video file itself and you have less control over formatting. Further, closed captions normally also convey additional items other than the human voice such as sound effects occurring during the video (breaking glass, music playing, and so forth).

To upload and attach a subtitle (srt) file to a video:

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > **Languages** tab option.
2. Follow **steps 1 - 3** in the [Auto-Generate a Subtitle File](doc:video-languages#auto-generate-a-new-subtitle-file) section above.
3. After clicking the **Add** button next to the language, click the **Upload Subtitles** option.

<Image title="uploadSubtitle.png" alt={527} align="center" src="https://files.readme.io/860968f-addManualSubtitle.png">
  Click the Upload Subtitles option to upload a .srt file
</Image>

> 📘 Note
>
> The following text formats are supported:
>
> * Bold
> * Italic
> * Underlined
> * Line Breaks

6. Once saved, the new subtitle language appears within the language icon on the [video player](https://revdocs.vbrick.com/docs/rev-video-player-features) so that users can select subtitles in languages that you have added or auto-generated.
