---
title: Bulk Transcription and AI Metadata Creation
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
Use the [Bulk Edit](doc:bulk-edit-video-settings) interface to auto generate the transcription or the metadata of several videos at once. This feature is selected by default when you click the **Bulk Edit** icon. Note that to use this feature you must have the [Rev IQ User](doc:granular-roles-and-permissions) role and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3019381dc99f9714c50ff22e6009ad313a45793b3414538cb643e78afb6f8af8-autoGenTranscriptionMetadataIcon.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


To access this feature, if not already selected, click the **Bulk Edit** icon and then click the **Auto Generate Transcription & Metadata** icon (seen above) which are visible when you access most [Media menu](doc:user-menu-options) options.

## Bulk Transcription Generation

The **Transcribe** dropdown allows you to transcribe several different videos at once into the language of your choice.

To use bulk transcription:

1. Select the videos you want to transcribe by clicking the checkbox to the left of the video.
2. Click the **Select Language** link to choose the language you want one or more additional languages transcribed from. The default language that your Account Admin has set, most often English, is selected in parentheses. This should _not_ be modified unless discussed with your admin since most Rev IQ functions depend on an English transcript.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4f545f65fe50665bdda4b32906ae530b549416bffa2420651c617317c85e4cb0-selectLanguageLink.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


3. Once you have selected the transcription language, select your **Transcribe** options.
   1. **Generate for Videos with No Matching Transcripts** - This is the default selection. Only generates a transcript if _one_ of the following is **true** for the selected video(s):
      1. No transcript in place with the selected language
      2. No transcript in place at all
      3. Transcript in place but in a different language than what is selected
   2. **Generate and Replace** - Generates a transcript and replaces exiting transcript for language(s) selected for the selected video(s).
   3. **Do not generate** - Does not generate a transcript.  Choose if you want to make sure no transcript is generated when you click the **Generate** button. You will not be able to generate additional languages in this case either if this option is selected.
   4. **Select additional language(s) for subtitles** - You can choose additional languages to generate transcripts for in addition to the default language in parentheses that has been selected by your Account Admin. For this box to be available you must have **Generate for Videos with No Matching Transcripts** or **Generate and Replace** selected as well.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44a67e5bd49b38e094b6ba1636433521e95f57c978abee0c4a6bff855eeb7db1-selectAdditionalLanguages.png",
        "",
        ""
      ],
      "align": "center",
      "caption": "Additional languages can be generated based on your default transcription language selected"
    }
  ]
}
[/block]


4. When you have made your selections, click the **Generate** button to proceed and each video you have selected will have the transcripts generated with your settings.

## Bulk AI Metadata Creation

The **Title**, **Description**, **Tags**, and **Chapters** dropdown(s) work very similar as when you [generate metadata in Video Settings](doc:video-title-description-and-tags#use-vbrick-generative-ai-for-automatic-video-metadata-generation) or when [uploading videos](doc:upload-video).  In the Bulk Edit interface, you use the corresponding dropdowns to generate metadata for several videos at once just as you do with other bulk edit features. 

To use bulk AI metadata creation:

1. Select the videos you want to generate metadata for by clicking the checkbox to the left of the video.
2. Use the various metadata dropdowns and select how you want each field generated as described below.
   1. **Do not Generate** - Does not generate the field. Default for the **Title** field.
   2. **Generate and Replace** - Generates and replaces entirely the field's content. Available for **Title** and **Chapter** metadata only.
   3. **Generate for Empty Fields** - Only generates if the field is empty (no content). Default for the **Description**, **Chapters**, and **Tags** field(s).
   4. **Generate and Append** - Generates content and appends to the current content in the field.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8da5d62dfa7f1ce88b4884479fef19e68d6bc4d63710585368ec921928a1d6a1-autoGenerateMetadata.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


3. When you have made your selections, click the **Generate** button to proceed and each video you have selected will have the metadata generated with your settings.

> 📘 Note
> 
> Metadata is only successfully generated for videos that have English transcripts. 
> 
> This means that the videos in your bulk edit selection either _must_ already have English transcripts, or you must generate English transcripts as part of your bulk edit job by selecting **English** and one of the **Generate** options in the **Transcribe** dropdown.