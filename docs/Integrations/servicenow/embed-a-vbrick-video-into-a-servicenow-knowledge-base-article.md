---
title: Embed a Vbrick Video into a ServiceNow Knowledge Base Article
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
Vbrick Videos can be embedded and viewed with seamless authorization directly into your Knowledge Base once you install the Vbrick Video app.

> 📘 Note
> 
> Vbrick videos must be Public to be embedded without the need for additional authorization (SSO). Otherwise, users will need to sign-in to view them.

## Requirements

- Vbrick Rev Cloud
- A Vbrick Rev user account that has an email that matches the email being used in the ServiceNow account. This integration also supports usernames or custom fields in ServiceNow to match Vbrick usernames.
- The Vbrick Rev account performing the installation/configuration steps _must_ be an Account Admin account on _both_ the **Vbrick** and **ServiceNow** instances.
- Before you are able to proceed, make sure your Account Admin has properly [installed and configured the Vbrick Video app](doc:servicenow#vbrick-video-app-installation) for **ServiceNow**.

## Usage

To embed in Vbrick video into a Knowledge Base article:

1. Navigate to the **Add a Vbrick Video** page in our ServiceNow App and search for the video you want to embed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/da18069-addVbrickVideo.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


2. Click on the **Copy Embed Code** button for the selected video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e3b6197-copyEmbedCode.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


3. Edit a **Knowledge Base** article and click **Insert Media** and select the **Embed** option.
4. Paste in the copied embed code and publish.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4adc302-insertMedia.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


4. The video then displays in your Knowledge Base article.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23206a7-embedVideoKA.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


## Troubleshooting

If the video source disappears after pasting the embed code and saving the Knowledge Article, your ServiceNow Admin may need to modify the global Script Include **HtmlSanitizerConfig** to include iframe in the **HTML_WHITELIST** object.

For complete details on how to do this, view "Section 3.3.4 Global Script Html Sanitizer Config" in the Scoped Application Installation and Configuration Guide that is included with the Vbrick Video App download.

> 🚧 Important
> 
> This is an optional step and should _only_ be used if needed. 
> 
> ServiceNow does not recommend using iframe in general and any change to the script include will count as a “customization”. Further updates to the script include from ServiceNow won’t be auto-applied.