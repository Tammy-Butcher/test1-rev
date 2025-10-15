---
title: Attendees
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

The **Attendees** section determines who has access to attend and view the event.  You can also specify content restrictions on the webcast recording by unlisting it and enabling Viewer ID.

<Image title="attendeesSection.png" alt={1147} align="center" src="https://files.readme.io/1902e13-attendeesSection.png">
  The Listing Type determines what settings are available.  All types can be unlisted and estimate number of attendees.
</Image>

## Set the Listing Type

**Listing Type** determines who has access to view the webcast and is normally the first determination you make when you schedule an event.  The Listing Type is set to either [Public](doc:public-events) (anyone can attend), [Private](doc:private-events) (you must be specifically invited), or the [All Users](doc:all-users-events)  (for licensed Rev accounts only) setting.  

Which type you choose also determines what additional settings appear for event configuration.  View the [Create an Event](doc:create-event) guide for complete details on how to set up the different types of events and the additional fields that are available based on List Type.

## Estimate Event Attendees

Use the **Estimated Number of Attendees** field to estimate the number of people that will attend your event so technical resources can be adjusted as necessary. The actual number of attendees can then be compared once the webcast concludes so that plans can be adjusted accordingly for the next webcast as needed. Estimated attendees is included on the [Webcast Event Report](doc:view-webcast-analytics). 

## Unlist a Webcast

When you choose to **Unlist this Webcast**, it prevents its display from all Media Contributors, Media Viewers, and Event Hosts that did not create it and hides it from view, similar to when you [unlist a video](doc:delete-replace-or-deactivate-videos#unlist-a-video).

> 👍 Tip
>
> An Unlisted webcast may still be manipulated through Rev APIs.

## Enable Viewer ID Watermark for an Event

You may want to make sure that your webcast is not shared or leaked outside of your company portal. To discourage this, you can select the **Enable Viewer ID Watermark** checkbox for your event.

<Image alt="If you enable Viewer ID Watermark for the event, the viewer's information is displayed during the playback of the recorded event" align="center" src="https://files.readme.io/8fb7d73-videoWatermarked.png">
  If you enable Viewer ID Watermark for the event, the viewer's information is displayed during the playback of the recorded event
</Image>

This floats the viewer's information over the recorded event during playback to discourage recording and sharing in other places on the Web. If the viewer is anonymous, the IP Address displays instead. You can also enter any custom text you want to display as well.

> 📘 Note
>
> Overlays added by this feature display during playback in Rev but are not displayed if the video is downloaded.

Your Account Admin must [enable this feature](doc:viewer-id-content-restriction) before you are able to use it on your webcast.  You may also use it on your [videos](doc:update-basic-video-settings#enable-viewer-id-watermark-on-a-video).
