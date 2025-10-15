---
title: Link to Video URLs
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
When you link to a URL, you are also able to specify if the video is a **Live **stream or a **VOD ** and its **encoding type**.

> 📘 Note
> 
> URL-linked videos do not have an actual file saved to Rev. Instead, the file plays from the _source_ of the URL that is provided. The linked videos do have the same features of videos that are uploaded to the system such as comments, ratings, and so forth.

To add a video through a URL link:

1. Click the [Upload](doc:adding-video) icon > **Add URLs** tab and then specify **Direct URL** in the **Create Using** dropdown.

2. Enter the **Link to URL** address in the **Web Address** field. _Only RTP/RTSP unicast/multicast (H.264 encoding) streams may be used for videos to be streamed to STBs._

3. Select **Live **or **VOD **as the **Video Type**.

4. Select the **Encoding Type**.

5. Click the **Add **button to save the link.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa81014f11eb1052633ab68dbb6034ca9438fc91b3e4afd53b8e11987a33ad03-linkDirectURL.png",
        null,
        "Click the Add URLs tab and then choose Direct URL in the Create Using dropdown"
      ],
      "align": "center",
      "caption": "Click the Add URLs tab and then choose Direct URL in the Create Using dropdown"
    }
  ]
}
[/block]


> 👍 Tip
> 
> Videos with a **Video Type** of **Live ** appear in the **Live Video** slider on [The Home Page](doc:the-rev-home-page).

## Create Using a Presentation Profile

Similar to adding through a URL, you are also able to specify if the video is a **Live **stream or a **VOD **as well as the **encoding type** when using a **Presentation Profile** to add a video.  

Note that you must have the [Presentation Profile](doc:add-a-presentation-profile) set up first  and that the streams specified in the profile may be controlled by Rev’s zone logic as far as who may view the video.

To add a video through a Presentation Profile:

1. Click the [Upload](doc:adding-video) icon > **Add URLs** tab and then specify  **Presentation Profile** in the **Create Using** dropdown.

2. Select the [Presentation Profile](doc:add-a-presentation-profile) you want to use and then click **Add**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b9c548eceafad414141dd5ba53e61fcb4eeda2ef1cf6b87806c544e64b94d791-linkPresentationProfile.png",
        null,
        "Click the Add URLs tab and then choose Presentation Profile in the Create Using dropdown"
      ],
      "align": "center",
      "caption": "Click the Add URLs tab and then choose Presentation Profile in the Create Using dropdown"
    }
  ]
}
[/block]