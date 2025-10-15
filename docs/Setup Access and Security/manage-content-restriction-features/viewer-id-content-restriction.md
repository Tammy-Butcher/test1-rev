---
title: Viewer ID Watermarking
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
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
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

With a focus on improved security and preventing data leakage, the **Viewer ID Watermarking** setting overlays the viewer metadata you choose on a video or webcast to deter recording or sharing content externally without proper controls in place.  

> 📘 Note
>
> Overlays added by this feature display during playback in Rev but are not displayed if the video is downloaded.

To implement Viewer ID Watermarking:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **Viewer ID Watermarking** section and decide to **Allow**, **Disable**, or **Require** watermarking on your Rev portal videos and webcasts as described below.

There are three Viewer ID settings:  **Allow**, **Disable**, and **Require**.

<Image alt="Prevent sharing of confidential information by enabling the Viewer ID watermarking feature" align="center" src="https://files.readme.io/251394d-viewerIDWatermarking.png">
  Prevent sharing of confidential information by enabling the Viewer ID watermarking feature
</Image>

* When **Allowed**:  A checkbox to enable the **Viewer ID Watermark** enabled features on *individual* [videos](doc:update-basic-video-settings#enable-viewer-id-watermark-on-a-video) and [webcasts](doc:attendees#enable-viewer-id-watermark-for-an-event) is visible and can be toggled on and off.  This means specific videos and webcast recordings can feature the Viewer ID-enabled settings while others may not if desired. Keep in mind that the **Default Text** entered here *can be changed* on individual videos with this setting. If you want specific text to display without editing, choose **Required** instead.

* When **Required**: The **Viewer ID Watermark** features that are enabled are *automatically* displayed on both videos and webcasts and may *not* be toggled on or off or changed in any way.  The checkbox to do so is *not* displayed.  This means that your **Default Text** may not be modified in any way if you choose this setting.

* When **Disabled**: All **Viewer ID Watermark** features are disabled.  The checkbox to enable the **Viewer ID Watermark** is *not* displayed.

You can choose to overlay the following information about a viewer:

* Full Name

Unique identifiers (depending upon login status):

* Username
* Email Address
* IP Address

You are also able to add a custom message string of your choice to display.

> 👍 Tip
>
> The **Viewer ID Watermarking** settings displays the user information in the Rev Player window for videos and webcasts, embeds, Featured Video, and playlists, if authenticated. Email address is displayed for guest users and the IP Address is displayed for anonymous users.

> 🚧 Important!
>
> Users that view a Live event on their **mobile device** browser are *not* able to view in **full screen** because mobile browsers use native players when in full screen mode which results in the Viewer ID Watermarking feature being removed. As a result, we have removed the full screen button from the player to ensure security.
