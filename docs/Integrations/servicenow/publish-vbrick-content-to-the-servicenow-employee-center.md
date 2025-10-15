---
title: Publish Vbrick Content to the ServiceNow Employee Center
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
Vbrick features a ServiceNow integration for natively publishing Rich Content and News Articles to the **Employee Center** via Content Publishing.  Vbrick Videos and Events can be published to Employee Center and viewed with seamless authorization.

> 📘 Note
>
> Vbrick Videos must be Public to be embedded without the need for additional authorization (SSO).  Otherwise, users will need to sign-in to view them.

<Image align="center" src="https://files.readme.io/c9193cf-employeeCenterContentPublish.PNG" />

> 🚧 Important!
>
> The **Employee Center** integration *requires* **Content Publishing v31.0.3** or greater. View the installation documentation packaged with your zip file for prerequisite and configuration details.

## Requirements

* Vbrick Rev Cloud
* ServiceNow's **Content Publishing** app v31.0.3 or greater with system table permissions
* The **Vbrick Video Employee Center Pro** integration from the ServiceNow Store
* A Vbrick Rev user account that has an email that matches the email being used in the ServiceNow account. This integration also supports usernames or custom fields in ServiceNow to match Vbrick usernames. View the developer documentation that is packaged with the Vbrick app for details.
* The Vbrick Rev account performing the installation/configuration steps must be an Account Admin account on *both* the **Vbrick** and **ServiceNow** instances.

## Vbrick Video App Installation

Before you are able to proceed, make sure your Account Admin has properly [installed and configured the Vbrick Video app](doc:servicenow#installation) for ServiceNow in addition to the **Vbrick Video Employee Center Pro** integration from the ServiceNow Store.  This step *must* be completed before you are able to publish Vbrick content to Employee Center.

## Access the Vbrick Video Library

After your Account Admin configures the **Vbrick Employee Center Integration**, you can publish Vbrick videos directly from your Vbrick portal to your Employee Center Rich Content and News Articles components.

To access the Vbrick Video Library:

1. In the **Employee Center**, select **Vbrick Video** as the **Provider**.
2. You can also enter the Vbrick Rev portal in the **URL Source**.

<Image alt="The Rich Content Editor configured for Vbrick Videos" align="center" src="https://files.readme.io/ae6ad85-openVideoLibrary.png">
  The Rich Content Editor configured for Vbrick Videos
</Image>

3. Click the **Open Video Library** button. The videos that are available to you are displayed along with the ability to search (if necessary) for videos by specific titles.
4. Select a video and click the **Apply** button to embed it into the **Employee Center** where you can add a **Publish Plan** for it that includes additional data such as **Location**, **Page**, **Widget**, and so forth.

<Image alt="The videos displayed are based on the current user (access) and the (configured) Vbrick Portal" align="center" src="https://files.readme.io/653ba77-employeeCenterPublishPlan.PNG">
  Specify Publish attributes for the video such as location, page, and widget
</Image>

5. Finally, you can click the **Preview on portal** button to preview your video before you publish the Vbrick video to the Employee Center.

## Advanced Embedding Options

The workflow steps above allow you to embed videos in **Employee Center** using the Rich Content Editor. There are additional use cases where you might want to use a **custom URL Source** to embed a live event, playlist, or video with additional options.

This can be accomplished by configuring [embedded content](doc:embed-a-video) in the **Vbrick Rev Portal**. Within the embed code, you will see a URL. Pasting that URL into the **URL Source field** of a video object in **ServiceNow** with the provider set to **Vbrick** allows you to embed virtually *any* content from Vbrick into Employee Center. 

Use the advanced option to build video galleries, town hall landing pages, and more.
