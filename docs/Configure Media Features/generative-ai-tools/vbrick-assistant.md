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
[block:html]
{
  "html": "\n<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>&#128736; <a href=\"/docs/rev-ai\">Rev IQ Module</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


Featured as part of Vbrick’s **Generative AI Tools** is Vbrick’s **Video Assistant**. The Video Assistant enables you to engage with a Generative AI chat interface to gain valuable insights from a pre-recorded video. You can ask questions about video highlights and speaker information or explore in-depth content-related inquiries.

<MetadataGenerationAvailabilityNotice />

## Requirements

- You must have a **Rev AI license** and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available to use the Vbrick Assistant. 
- The video must have an [English transcript](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings) available.
- The feature must be enabled.  It is disabled by default.

## Configuration

To globally enable the **Video Assistant**:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Scroll to the **Generative AI Tools** section.

3. Select the **Ask questions about a video using an AI chatbot** checkbox next to the **Video Assistant** label. If this checkbox is not visible, **Rev AI Hours** licensing must be purchased and **Rev Credits** applied first.  Contact your Account Admin.

4. To enable analysis of images and supplemental files in addition to the video transcript when using the chatbot, click the checkbox for [Enhanced Multimedia Analysis](doc:enhanced-multimedia-analysis).

5. Click **Save Changes**.

- The **Video Assistant** icon and flyout panel is now available and functions as a Generative AI chat interface.
- When clicked, the context of the video's transcript is fed to the **Large Language Model (LLM)** service that Rev uses.
- This allows you to prompt the Video Assistant with questions about the video.

## Usage

### Video Assistant Flyout Panel Functions

The [Video Assistant](doc:rev-video-player-features#video-assistant) flyout panel allows you to engage with the Generative AI chat interface and prompt it with questions about the video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2cc6a996b22cc91da19a8dffba21dbd39bd08830223cabbd6ad8adfaed41aee1-videoAssistantFlyout.png",
        "videoBasicInfoFlyout.png",
        "Use the Vbrick Assistant if you want to gain quick insights about a video's content or context"
      ],
      "align": "center",
      "caption": "Use the Vbrick Assistant if you want to gain quick insights about a video's content or context"
    }
  ]
}
[/block]


Your chat history for the specific video is stored for 90 days unless you choose to clear it.  To clear your chat history, click the three dot menu and then **Clear Conversation**. The conversation history is also cleared if there is a change to the video's transcript.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2f32a10a9e057198eebce1d6bc747e1b6d4ef88ecd87180c8d88facd3369b77b-clearConversation.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


Use the **Copy** icon at the bottom of a response to copy it to your clipboard. Timestamps, if present, are also copied along with the text.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9fb989f245b3dea14418bebdb458b5c4bed06909174315bee626e21add9d52b4-copyIcon.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


Keep in mind that you should _always_ verify Video Assistant information through trusted sources!

> 📘 Note
> 
> Remember, if there is not an **English** transcript available for the video, the Video Assistant is not available.

### Video Assistant Timestamps and Citations

Timestamps that appear in Video Assistant responses are clickable and will help you navigate directly to that point in the video if clicked.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3762a722503798b698343b08127456538de26a4a9b56e5c54d9e41899028aa4d-timestamp.png",
        "",
        "Click a timestamp to jump to it on the video timeline"
      ],
      "align": "center",
      "caption": "Click a timestamp to jump to it on the video timeline"
    }
  ]
}
[/block]


The Video Assistant may also cite specific points in the transcript that it references to obtain the answers to your questions as appropriate. These citations appear in a new section labeled **Video Citations** below your answer if there are relevant citations to display. If there are no relevant citations, this section does not appear. Timestamps that appear in Video Citations are also clickable and will navigate you to that point in the video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5c61352c4f203cfd44690f0019328090b30e473fd495c670e00e65730cabebae-videoAssistantCitation.png",
        "",
        "Responses to specific questions are cited in a playback box that can also be clicked and access on the timeline"
      ],
      "align": "center",
      "caption": "Citations will include timestamps that can be clicked to access the timeline"
    }
  ]
}
[/block]


Finally, take note that you can also ask for timestamps about a specific subject directly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/68266914a52711f19ed7202fa283b14506c4dde80cb139ad337999b216403347-timestampRequest.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]