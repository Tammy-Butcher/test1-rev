---
title: Publish Vbrick Videos Using Search and Content Links
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

Once you have installed the **Vbrick Videos** app, you are able to seamlessly incorporate videos from the Vbrick Rev cloud platform by using **Vbrick video search** and **Content Links**.

## Requirements

* Vbrick Rev Cloud
* ServiceNow's **Content Publishing** app with system table permissions
* The **Vbrick Video Employee Center Pro** integration from the ServiceNow Store
* A Vbrick Rev user account that has an email that matches the email being used in the ServiceNow account. This integration also supports usernames or custom fields in ServiceNow to match Vbrick usernames. View the developer documentation that is packaged with the Vbrick app for details.
* The Vbrick Rev account performing the installation/configuration steps must be an Account Admin account on *both* the **Vbrick** and **ServiceNow** instances.

## Vbrick Video App Installation

Before you are able to proceed, make sure your Account Admin has properly [installed and configured the Vbrick Video app](doc:servicenow#installation) for ServiceNow in addition to the **Vbrick Video Employee Center Pro** integration from the ServiceNow Store. This step *must* be completed before you are able to update the Content Publishing links.

## Add a Vbrick Video URL to the Content Publishing - Link Content Table

You can add a Vbrick video URL to a Content Publishing page as you normally would add other types of Link content, by first adding your **Vbrick Video URL** to the **Content Publishing - Link Content** table.  This does not require the use of a custom widget.

To add a Vbrick video to the Content Publishing - Link Content table:

1. Navigate to **Vbrick Video** > **Add a Vbrick Video**.

2. Use the **Search** box to search for the video(s) you want to add.

<Image alt="Add the videos you want to use by searching on them first through Add a Vbrick Video" align="center" src="https://files.readme.io/8ebc71e-addVbrickVideo.png">
  Add the videos you want to use by searching on them first through Add a Vbrick Video
</Image>

> 🚧 Important!
>
> Only those videos you have access to in your Vbrick instance appear here.

3. Click the video you want to add and then click **Select**.  Additional details about the video appear, including the **Playback URL** and **Video ID**.

<Image alt="The Video ID seen here can also be used in the Vbrick Video By ID widget" align="center" src="https://files.readme.io/5e198a2-videoDetails.png">
  The Video ID seen here can also be used in the Vbrick Video custom widget
</Image>

3. Make note of the **Video ID** if you want to use it in the **Vbrick Video** custom widget. Click the **Submit** button.

4. You have now added the Vbrick video to the **Content Publishing - Content Link** table and it is available for inclusion on your **Content Publishing** pages in the **Video URL** dropdown.

<Image align="center" src="https://files.readme.io/59019d7-contentLinks.png" />
