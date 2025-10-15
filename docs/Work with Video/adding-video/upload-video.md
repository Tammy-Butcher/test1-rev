---
title: Upload Video
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
To upload a video from your local hard drive:

1. Click the [Upload](doc:adding-video) icon > **Upload Files** tab and then click the **Select Files** button. (You can also click and drag your video into the box)

2. If you are uploading a 360-degree video, toggle the **360 Video** switch. This option must be [enabled](doc:allow-360-videos) by your Account Admin first before it is visible.

<Image alt="Click the Upload Files tab and then Add Files" align="center" src="https://files.readme.io/4aecec8f73007ee752921b7eccb06968051803f32bc18b007277dcd89c3a6acc-uploadVideoFromHarddrive.png">
  Click the Upload Files tab and then Select Files button
</Image>

3. Toggle the [Transcribe](doc:rev-iq-transcription-and-translation) switch to on and select one or more languages to auto-generate transcripts for the videos you want to upload. 
4. Note that this switch may be locked to an **on** state with a language pre-selected if an [Automatic Transcription](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings) language for uploads has been assigned by an Admin in **Media Settings**. However, additional languages for subtitles may be selected in the drop-down control.

<Image alt="Subtitles in additional languages may be generated if selected in the Transcribe drop-down" align="center" src="https://files.readme.io/b265abb90bccaa5c7d958116a84215ba1247e5983c46d1bc7957aff979ff463a-uploadVideoAddSubtitles.png">
  Subtitles in additional languages may be generated if selected in the Transcribe drop-down
</Image>

5. Toggle the [Generate All Metadata](doc:video-title-description-and-tags#use-vbrick-generative-ai-for-automatic-video-metadata-generation) switch to on to auto-generate video metadata for your upload. You may also continue to generate or re-generate metadata for individual videos in [Video Settings](doc:video-title-description-and-tags#use-vbrick-generative-ai-for-automatic-video-metadata-generation) after it uploads if it has an English transcript. The **Generate All Metadata** switch is locked in an off state if the **Transcribe** switch is off or is set to any language other than English.
6. If you do not want *all* of the metadata generated, use the carrot dropdown to choose which specific fields to auto-generate for you.
7. Video files that are selected or dragged and dropped into the upload tray for uploading are subject to the upload configurations displayed at the time the files are placed into the upload tray. 
8. If you want to upload additional videos with a different combination of settings, you can adjust individual switches and new videos dropped into the tray after these adjustments are made are subject to those new settings. Adjusting switches during an in progress upload will not effect those in progress uploads.

<Image alt="Use the dropdown to choose which metadata to generate if desired" align="center" src="https://files.readme.io/1acc5b81fefdc594beaf62411be05df363c83debe1cd50a31122f404d770f7cd-uploadVideoAIGenerate.png">
  Use the dropdown to choose which specific metadata to generate, otherwise all options are generated
</Image>

> 📘 Note
>
> Because an English transcript is required for metadata generation, you should not toggle transcription off if you wish to use any of the metadata generation toggles.
>
> You must have a Rev AI license and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available to use the metadata generation feature.

<PreferredRevSetting />

## Upload an MP3 File

**MP3** files are the only audio files supported in Rev. MP3 files that are uploaded are treated the same as video files in that they play in Rev’s video player and you also need to modify video settings once uploaded. 

To upload an MP3 file from your local hard drive:

1. Click the **Upload Files** tab and then click the **Select Files** button just as if you were uploading a video from your hard drive.

2. You may select multiple MP3 files at once to upload. The MP3 file(s) are uploaded as a video file in Rev with a MP3 file icon thumbnail background. As a result, you may manipulate it as a Rev video including modifying video settings, using an approval process, subtitles, and so forth.

## Upload from a Webex Meeting

This feature is only visible if the **Webex Integration** feature is enabled. This function makes the 100 most recent meeting videos (within the last 28 days) of a Webex user’s account available for import into Rev.

View how to [Manually Import Video from a Webex Meeting](doc:webex-meetings#manually-import-video-from-a-webex-meeting) for more details.
