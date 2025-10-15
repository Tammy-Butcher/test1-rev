---
title: Add a Background Image to a Webcast
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

You are able to add a background image to your webcast so that you can use branded imagery from your organization if desired.

<Image title="backgroundImage.png" alt={700} align="center" src="https://files.readme.io/172b2dd-backgroundImage.png">
  Select an image to display in the background of your event
</Image>

To add a background image to your event:

1. Navigate to the event and scroll to the **Attendee Engagements** section.

2. Select the image you want to upload under **Background Image**.
   * A [supported file type](doc:supported-file-types)  must be used
   * For best results, use an image that is at least 1600 pixels by 1200 pixels.

3. Choose a **Background Size**:
   * **Fit to Space**: Image is sized to fit available space and filler gray space will be displayed if image is not sized exactly to fit the space.
   * **Fill Space**: Image is expanded to fill available area and may be trimmed.

> 👍 Tip
>
> Images are automatically scaled to a smaller size for mobile devices viewing the webcast.

4. The background image appears in the following locations:
   1. **Guest** user log-in form (internal log-in page unaffected)
   2. Live webcasts behind the video and slides (during the broadcast)
   3. Full screen slide mode
5. Use the **Delete Image** button to delete a background image.

<Image title="guestLogin.png" alt={700} align="center" src="https://files.readme.io/349eb43-guestLogin.png">
  Guest Login with a background image uploaded
</Image>

> 👍 Tip
>
> Background images are not used as thumbnail images on Home page carousels.  You should [upload a custom thumbnail image](doc:add-a-thumbnail-image-to-an-event) instead.
