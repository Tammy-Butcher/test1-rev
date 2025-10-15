---
title: ServiceNow
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

Vbrick integrates with **ServiceNow** via our **Vbrick Video** app that is available in the [ServiceNow App Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/2a3d530f87b4e1100af91f873cbb35a0/2.0.14). Once installed, you can:

* Publish a Vbrick-hosted video using both the **Content Publishing** workflow in ServiceNow as well as by using the **Vbrick Video** custom widget to embed Vbrick-hosted videos on those Service Portal Pages that support the use of custom widgets. 
* Embed a Vbrick-hosted playlist with the **Vbrick Playlist** custom widget using either the Playlist ID or URL while applying seamless access controls for your end users.
* Use the **Vbrick Event** custom widget to view Vbrick Rev Public events directly in your ServiceNow portal, including attendee engagements you have enabled.
* Publish Vbrick content with automatic authentication to the **Employee Center** for video components in **Rich Content** and **News Articles**.  Note: Private videos will still require a log-in if not already authenticated.

> 🚧 Important!
>
> If you previously installed the **Vbrick Video** (or **Vbrick Video Connector**) app **v1.4** or earlier, it is important that you **uninstall** it first before installing the latest version.

## Requirements

* Vbrick Rev Cloud
* A Vbrick Rev user account that has an email that matches the email being used in the ServiceNow account. This integration also supports usernames or custom fields in ServiceNow to match Vbrick usernames as of Rev v7.56. View the developer documentation that is packaged with the Vbrick app for details.
* The Vbrick Rev account performing the installation/configuration steps must be an Account Admin account on *both* the **Vbrick** and **ServiceNow** instances.

## Installation

To enable and install the **Vbrick Video** app on the **ServiceNow Platform UI**:

1. Navigate to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/2a3d530f87b4e1100af91f873cbb35a0/2.0.14) and search for **Vbrick Video**.

2. Download and install the **Vbrick Video** app. Complete installation instructions are included in the zip file downloaded with the app.

<Image align="center" src="https://files.readme.io/b09e78b-serviceNowStore.png" />

<br />

> 🚧 Important!
>
> An Account Admin must perform the installation steps.

3. Once the app is installed, you can search on **Vbrick** in your **ServiceNow** platform UI filter box in the left navigation menu. This displays the Vbrick options available to you where you can favorite them for easy access in the future.

<Image alt="Vbrick navigation options become available in ServiceNow once the Vbrick Video app is installed" align="center" src="https://files.readme.io/10f5ab3-vbrickNavOptions.png">
  Vbrick navigation options become available in ServiceNow once the Vbrick Video app is installed
</Image>

4. You are now ready to use the app features which are described below and in the topic sections below this one.

<Image align="center" src="https://files.readme.io/59019d7-contentLinks.png" />

## Vbrick Rev AI-Powered Videos in ServiceNow Workflows

Vbrick brings enhanced and [generative AI capabilities](doc:generative-ai-tools) into your ServiceNow workflows. Vbrick's [Smart Search](doc:search-and-filter-functions#ai-powered-smart-search), [Summarization](doc:video-title-and-description#use-vbrick-generative-ai-to-add-a-video-description), and [Video Assistant](doc:vbrick-assistant) capabilities are embedded into your contextual search screens and videos to streamline knowledge sharing, improve self-service options, and speed up your issue resolutions.

<Image align="center" src="https://files.readme.io/82a35ea-incidentForm.png" />

You can use custom fields in ServiceNow forms that will use Vbrick's **Smart Search** to generate results.

<Image align="center" src="https://files.readme.io/cd7fa7b-vidAssistantforSN.png" />

Vbrick videos will use our Generative AI features such as the **Video Assistant** to summarize what the video is about if it meets the requirements needed.

For details on how to use this feature in details, view the developer documentation included with the Vbrick app.

## Vbrick Rev Reporting and Analytics with ServiceNow Views

Videos that are viewed in ServiceNow are tracked in Rev by returning a **Viewing Context** of "Service Now".

You can enable **Viewing Context** on the **Views** tab in [Videos System Analytics](doc:videos-system-analytics) and also on the **Reports** flyout panel when viewing [Video Analytics](doc:video-analytics-dashboard)  for an individual video. Viewing Context can also be seen for Webcasts and, specifically, on the **Attendees** tab for [Real-Time Webcast Analytics](doc:attendees-in-real-time) and the post-event [Webcast Analytic Report](doc:view-webcast-analytics) on the **Users** tab.
