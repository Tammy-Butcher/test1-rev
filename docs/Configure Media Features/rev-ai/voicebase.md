---
title: VoiceBase
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
If you have a **VoiceBase** account, you may send a video for transcription and have a **SubRip (.srt)** file created directly in Rev. Once your video is transcribed and the .srt file returned to Rev, your videos are deleted from VoiceBase, ensuring your account’s security.

> 🚧 Caution
> 
> As this time, **English **is the only supported language in VoiceBase.

## Requirements

You must have a [VoiceBase account](https://www.voicebase.com) created at before you begin this process.

## Configuration

To enable the VoiceBase Integration:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Select the **VoiceBase Integration** checkbox in the **AI & Machine Learning** section.

3. Enter the **VoiceBase Bearer Token** obtained from your VoiceBase account. 
   - To obtain a token, log in to <https://apis.voicebase.com/developer-portal>.
   - Navigate to and click the **Bearer Token Management** widget.
   - Click the **New Key** button in the upper right corner to generate a new token.
   - Copy the generated token into the **VoiceBase Bearer Token** field in Rev.

4. Configure [Automatic and Default Transcription and Translation Settings](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings) as needed.

> 📘 Note
> 
> While **Automatic Transcription **may be configured, VoiceBase may not be used for **Automatic Translation** services at this time.

5. Click **Save Changes**.

## Usage

When a video is uploaded, you can view languages and transcription options you have selected on the [Languages](doc:video-languages) tab.

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > [Languages](doc:video-languages) tab option.

2. Use this tab to view the **Default Transcription Language** on the top row and to view the translation languages you selected. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/79bbe69-languagesTab.png",
        "revIQTranscription.png",
        370
      ],
      "align": "center",
      "caption": "The Languages tab displays default transcription and translation languages"
    }
  ]
}
[/block]


3. Use this tab to [edit, delete, and dowload video subtitles](doc:video-languages) as needed.
4. You can also [autogenerate a VoiceBase .srt file](doc:video-languages#auto-generate-a-new-subtitle-file) by clicking the **Add Lanaguage** button.
5. Once you select your **Source Language**, you will be able to select VoiceBase to generate it.