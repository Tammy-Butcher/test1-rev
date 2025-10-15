---
title: Private Metadata Sharing
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
You can enable private video metadata sharing so that Rev video links shared on sites like Facebook, LinkedIn, and Twitter render a thumbnail, title, and friendly description of the video. When you enable this setting, Rev modifies the HTML text in the ‘Header’ element to produce the enhanced link sharing.

To enable Rev private video metadata sharing:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **Sharing and Embedding** section.
3. Select the **Allow Sharing of Metadata for Private Videos** checkbox to enable enhanced link sharing.

![](https://files.readme.io/ecb8f69-shareMetadata.png "shareMetadata.png")

4. Specify which social sites returning metadata that Rev will accept by entering a valid user agent bot in the **Recognized User Agents** form.

View the following links for details on how to formulate these:

- <https://oembed.com/>
- <https://ogp.me/>

Now when you [Share a Video](doc:share-a-video)  on external social sites like Facebook, LinkedIn, and Twitter a thumbnail, title, and friendly description of the video is displayed.