---
title: Use Vbrick Custom Widgets on ServiceNow Portal Pages
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

Once you have installed the **Vbrick Videos** app, you are able to use Vbrick custom widgets on your ServiceNow pages. Specifically, you can:

* Use the **Vbrick Video** custom widget to embed Vbrick-hosted videos . 
* Use the **Vbrick Event** custom widget to view Vbrick Rev Public events directly in your ServiceNow portal, including attendee engagements you have enabled. (Vbrick customers only)
* Use the **Vbrick Playlist** custom widget to embed Vbrick-hosted playlists.

> 📘 Note
>
> ServiceNow Portal Pages must support the use of custom widgets to use this feature.

## Requirements

* Vbrick Rev Cloud
* A Vbrick Rev user account that has an email that matches the email being used in the ServiceNow account. This integration also supports usernames or custom fields in ServiceNow to match Vbrick usernames. View the developer documentation that is packaged with the Vbrick app for details.
* The Vbrick Rev account performing the installation/configuration steps *must* be an Account Admin account on *both* the **Vbrick** and **ServiceNow** instances.
* Before you are able to proceed, make sure your Account Admin has properly [installed and configured the Vbrick Video app](doc:servicenow#vbrick-video-app-installation) for **ServiceNow**.  This step *must* be completed before you are able to access Vbrick custom widgets.

## Add a Vbrick Custom Widget to a Page

For those ServiceNow pages that can use custom widgets, [installing the Vbrick Videos App](doc:servicenow#vbrick-video-app-installation) also provides access to the **Vbrick custom widgets**.

To use the a vbrick custom widget:

1. Access the page **Designer** in the **Service Portal** as you normally would and create or edit a page.

<Image alt="Use the Designer to design your Pages and include the Vbrick Video By ID custom widget" align="center" src="https://files.readme.io/de7ca61-serviceNowDesigner.png">
  Use the Designer to design your Pages and include the vbrick custom widgets
</Image>

2. Search the term **vbrick** to display and use the custom Vbrick widget(s) available.  Each section below details what information you will need to use a specific Vbrick custom widget.

<Image alt="Search the term vbrick to view available custom widgets" align="center" src="https://files.readme.io/a7bff7d-vbrickWidget.png">
  Search on 'vbrick' to view the custom widgets available to use on your pages
</Image>

## Vbrick Video

Installing the Vbrick Videos app provides access to the **Vbrick Video** custom widget through the Service Portal Designer. This widget embeds and then plays videos the user is authorized to view directly in the ServiceNow page.

### Finding the Video ID

Before you use the **Vbrick Video** custom widget, you need to know the **video IDs** of the video(s) you plan to embed on your page.  There are two methods to do this:

1. In your **Vbrick Rev** portal, copy the ID at the end of the URL string in the video player. The ID is the string of characters that comes after `/videos/` in the address bar.
   1. For example: `0e96dd68-b1d8-4510-9582-ec6f81ca2a8f` is the ID in a URL that looks similar to `https://my.rev-portal.vbrick.com/#/videos/0e96dd68-b1d8-4510-9582-ec6f81ca2a8f`
2. In the **ServiceNow Platform UI**, search for **Vbrick Video** > **Add a Vbrick Video** and click the video you want to use. Copy the ID from the **Video ID** field.

### Using the Vbrick Video Custom Widget

To use the Vbrick Video custom widget:

1. Access the page **Designer** in the **Service Portal** as you normally would and create or edit a page.
2. Search `Vbrick` to display the custom Vbrick widget(s) available. In this case, the **Vbrick Video** widget.
3. Drag and drop the widget to your page, and click **Edit** to enter the **Video ID** for the video you want to embed on the page.  You can drag the custom widget to the same page multiple times.

<Image align="center" src="https://files.readme.io/054d8f6-videoIDConfig.png" />

4. When users view your page, their user identifier associated with their ServiceNow login is sent to their linked Vbrick portal and, if that user is allowed to view the video, it will load and play for them just like it would if they were logged into their Vbrick instance directly.  

<Image align="center" src="https://files.readme.io/6bf035e-videoByIDWidget.png" />

5. If they are *not* authorized to view a video, they will see an 'Unauthorized' message instead.

## Vbrick Event

Installing the Vbrick Videos App provides access to the **Vbrick Event** custom widget. This widget embeds and then plays a Vbrick Rev webcast the user is *authorized* to view directly in the ServiceNow page.

> 🚧 Important!
>
> The **Vbrick Event** widget is not available if you are using the **Vbrick Video On Demand** app for ServiceNow.  You must be using the **Vbrick Video Connector** app and be a Vbrick Rev customer.

### Finding the Webcast ID or Webcast URL

Before you use the **Vbrick Event** custom widget, you need to know the **Webcast ID** or **Webcast URL** of the event you plan to embed on your page.

1. In your **Vbrick Rev** portal, copy the **Webcast ID** at the end of the **Webcast URL**. The ID is the string of characters that comes after the `/events/` in the address bar.  For example:
   1. `b854903c-c34b-49e5-8116-3becb37b4184` is the ID in a Webcast URL that looks similar to `https://my.rev-portal.vbrick.com/#/events/b854903c-c34b-49e5-8116-3becb37b4184`
2. You can also enter the entire **Webcast Link** that is assigned in Vbrick Rev once you have finished event setup.

### Using the Vbrick Event Custom Widget

To use the **Vbrick Event** custom widget:

1. Access the page **Designer** in the **Service Portal** as you normally would and create or edit a page.
2. Search **Vbrick** to display the custom Vbrick widget(s) available. In this case, the **Vbrick Event** widget.
3. Drag and drop the widget to your page, and click **Edit** to enter the **Webcast ID** for the webcast you want to embed on the page.  You can drag the custom widget to the same page multiple times.

<Image align="center" src="https://files.readme.io/29a85d0-vbrickEventConfig.png" />

4. When users view your ServiceNow page with the event, they are automatically logged into private events. For public events that do not require registration, the video will play once the event begins.  Keep in mind that the Rev Event Host must start and run the event in Rev.

<Image align="center" src="https://files.readme.io/f3477f3-embeddedRevEvent.png" />

## Vbrick Playlist

Installing the Vbrick Videos App provides access to the **Vbrick Playlist** custom widget through the Service Portal Designer. This widget embeds and then plays a Vbrick playlist the user is authorized to view directly in the ServiceNow page. You can also set Rev's playlist Layout options and select it to display in filmstrip, grid, or slider format.

### Finding the Playlist ID or Playlist URL

Before you use the **Vbrick Playlist** custom widget, you need to know the **playlist ID** or **playlist URL** you plan to embed on your page. 

1. In your **Vbrick Rev** portal, copy the ID at the end of the URL string in the video player. The ID is the string of characters that comes after `/media/playlists/` in the address bar.
   1. For example: `19b83c60-9dd6-4f83-9b98-74b6b4ad1c4e` is the ID in a URL that looks similar to `https://my.rev-portal.vbrick.com/#/media/playlists/19b83c60-9dd6-4f83-9b98-74b6b4ad1c4e`
2. In the **Vbrick Rev** portal, follow the steps to [embed a playlist](doc:share-a-playlist#embed-a-playlist). In the **Sharing** flyout, copy the URL in the embed code. Using this method, you can also copy the **Layout** styling options that are set.
   1. For example, the URL `https://my.rev.portal.vbrick.com/embed?playlist=19b83c60-9dd6-4f83-9b98-74b6b4ad1c4e&layout=row` is the embed URL of the playlist using a filmstrip (row) layout from the Rev portal.

<Image align="center" src="https://files.readme.io/86525cc-embedPlaylistURL.png" />

### Using the Vbrick Playlist Custom Widget

To use the Vbrick Playlist custom widget:

1. Access the page **Designer** in the **Service Portal** as you normally would and create or edit a page.
2. Search `Vbrick` to display the custom Vbrick widget(s) available. In this case, the **Vbrick Playlist** widget.
3. Drag and drop the widget to your page, and click **Edit** to enter the **Playlist ID** or the **Playlist URL** for the playlist you want to embed on the page.  You can drag the custom widget to the same page multiple times.

<Image align="center" src="https://files.readme.io/61068fa-playlistIDConfig.png" />

4. When users view your page, their user identifier associated with their ServiceNow login is sent to their linked Vbrick portal and, if that user is allowed to view the playlist (videos), it will load and play for them just like it would if they were logged into their Vbrick instance directly.  

<Image align="center" src="https://files.readme.io/5882897-embeddedRevPlaylist.png" />

5. If they are *not* authorized to view any videos in a playlist, they will see an 'Unauthorized' message instead.  Note that the Public videos will display but not those that the user is not authorized to view.
