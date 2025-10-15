---
title: Vbrick Assistant
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

Featured as part of Vbrick’s **Generative AI Tools** is Vbrick’s **Video Assistant**. The Video Assistant enables you to engage with a Generative AI chat interface to gain valuable insights from a pre-recorded video. You can ask questions about video highlights and speaker information or explore in-depth content-related inquiries.

<MetadataGenerationAvailabilityNotice />

## Requirements

* You must have a **Rev AI license** and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available to use the Vbrick Assistant. 
* The video must have an [English transcript](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings) available.
* The feature must be enabled.  It is disabled by default.

## Configuration

To globally enable the **Video Assistant**:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Scroll to the **Generative AI Tools** section.

3. Select the **Ask questions about a video using an AI chatbot** checkbox next to the **Video Assistant** label. If this checkbox is not visible, **Rev AI Hours** licensing must be purchased and **Rev Credits** applied first.  Contact your Account Admin.

4. Click **Save Changes**.

* The **Video Assistant** icon and flyout panel is now available and functions as a Generative AI chat interface.
* When clicked, the context of the video's transcript is fed to the **Large Language Model (LLM)** service that Rev uses.
* This allows you to prompt the Video Assistant with questions about the video.

## Usage

### Video Assistant Flyout Panel Functions

The [Video Assistant](doc:rev-video-player-features#video-assistant) flyout panel allows you to engage with the Generative AI chat interface and prompt it with questions about the video.

<Image title="videoBasicInfoFlyout.png" alt={322} align="center" src="https://files.readme.io/b75cb31-videoAssistantPrompt.png">
  Use the Vbrick Assistant if you want to gain quick insights about a video's content or context
</Image>

Keep in mind that you should always verify this information through trusted sources!

> 📘 Note
>
> Remember, if there is not an **English** transcript available for the video, this icon and flyout panel is not visible.
