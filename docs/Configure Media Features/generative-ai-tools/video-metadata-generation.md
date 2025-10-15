---
title: Video Metadata Generation
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
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
  <li>&#128736; <a href="/docs/rev-ai">Rev IQ Module</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

Featured as part of Vbrick’s **Generative AI Tools** is Vbrick’s **Video Metadata Generation** tool. This tool enables you to automatically generate the following metadata if you also have an English transcript applied:

* Title
* Description
* Tags
* Chapters

 When you have rich metadata for your video, it enhances its searchability and context. This significantly improves content accessibility and relevance to your users. Videos become valuable resources that are easily understood and searchable and can be purposefully utilized across your various platforms and audiences.

<MetadataGenerationAvailabilityNotice />

## Requirements

* You must have a **Rev AI license** and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available to use the **Video Metadata Generation** tool. 
* The video must have an [English transcript](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings) available.
* The feature must be enabled.  It is disabled by default.

## Configuration

To globally enable the **Video Metadata Generation** tool:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Scroll to the **Generative AI Tools** section.

3. Select the **Allow automated Descriptions, Tags, Titles, and Chapters from video transcripts** checkbox next to the **Video Metadata Generation** label. 

4. If this checkbox is not visible, **Rev AI Hours** licensing must be purchased and **Rev Credits** applied first.  Contact your Account Admin.

5. Click **Save Changes**.
   1. A **Generate** icon is now available in **Basic Settings** next to the Title, Description, Tags, and Chapters fields. You can also choose to click the **Generate All Metadata**  button to generate all settings at once.
   2. if you click any **Generate** option, the context of the video's transcript is fed to the **Large Language Model (LLM)** service that Rev uses.
   3. This generates each setting as requested based on the transcript.

## Usage

### Use the Generate Link in Video Basic Settings

A **Generate** link is available for each of the metadata fields described above once you enable this setting.  Each field is then generated based on the video transcript if [Generate](doc:video-title-description-and-tags#use-vbrick-generative-ai-for-automatic-video-metadata-generation) is clicked.  

You can also click the [Generate All Metadata](doc:video-title-description-and-tags#use-vbrick-generative-ai-for-automatic-video-metadata-generation) link to generate all fields at once.

<Image title="videoBasicInfoFlyout.png" alt="Use generate links to generate all of the video metadata" align="center" src="https://files.readme.io/40fb013-generateAllMetadata.png">
  Use the Generate All Metadata link if you want to quickly generate a video's metadata
</Image>

> 📘 Note
>
> Remember, if there is not an **English** transcript available for the video, you will not be able to use this feature even if it has been enabled!
