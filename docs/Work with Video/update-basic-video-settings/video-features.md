---
title: Video Features
excerpt: >-
  How to enable additional video features such as commenting on a video,
  ratings, and the ability to download a video.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
To update **Video Settings** in Rev:

1. Navigate to a video and hover over the **Video Settings** button in the top right corner.

2. Click **Details** from the options that appear.  Several tabs appear that allow you to create and modify the video's metadata. Select a tab depending on which setting you want to update. 

3. This feature is a **Basic Setting**.

## Enable Comments, Ratings, and Downloading

Toggling the comments, ratings, and downloads features enables and make these settings available for use on individual videos.

<Image title="enableVidFeatures.png" alt="Individual video features must be enabled to use them" align="center" src="https://files.readme.io/cfd2260-enableVideoFeatures.png">
  Individual video features must be enabled to use them
</Image>

* If comments are enabled, owners are notified by email when a user leaves a comment on their video. The email includes the user’s name, date, and time the comment was left, and the comment itself along with a link to the video in Rev. This includes nested comments.
* Ratings allow the video to be rated on a scale of 1 to 5 stars.
* Enabling downloads means that the video may be downloaded to the viewer's PC (mobile not available).

> 📘 Note
>
> These features must be [globally activated](doc:allow-comments) first by your Account Admin. If they have not been activated, you will not have them available to be enabled on individual videos.

## Enable Viewer ID Watermark on a Video

You may want to make sure that your video is not shared or leaked outside of your company portal.  To discourage this, you can select the **Enable Viewer ID Watermark** checkbox for your video uploads in the **Features** section.  

<Image align="center" src="https://files.readme.io/f98595b-enableViewerIDWatermarking.png" />

This tiles and floats the viewer's information over the video during playback to discourage recording and sharing in other places on the Web. If the viewer is anonymous, the IP Address displays instead.

<Image alt="Floating viewer information displays during playback if Viewer ID is enabled to discourage recording and sharing with outside sources" align="center" src="https://files.readme.io/fb29a18-videoWatermarked.png">
  Floating viewer information displays during playback if Viewer ID Watermark is enabled to discourage recording and sharing with outside sources
</Image>

> 📘 Note
>
> Overlays added by this feature display during playback in Rev but are not displayed if the video is downloaded.

Your Account Admin must [enable this feature](doc:viewer-id-content-restriction) before you are able to use it on your videos.  You may also use it on your [webcasts](doc:attendees#enable-viewer-id-watermark-for-an-event).

## Show Chapter Images By Default

If chapter images are present in your video, you can choose to have them display by default when the video is accessed by toggling the **Show Chapter Images By Default** switch.

<Image alt="Toggle the Show Chapter Images By Default switch if you want chapter images to display every time a video is accessed" align="center" src="https://files.readme.io/4f7046c-showChapterImagesEnabled.png">
  Toggle the Show Chapter Images By Default switch if you want chapter images to display every time a video is accessed
</Image>

This switch is *only* visible if [chapters are added to the video](doc:add-chapters-to-a-video) and at least one chapter contains an image. The toggle switch will *not* be visible if there are no chapters or no images for the video.

Viewers can always hide the images (if this is enabled) by toggling the **Show Chapter Images** icon in the [video player](doc:rev-video-player-features#playback-bar-functions).

<Image align="center" src="https://files.readme.io/8123be7-hideChapterImages.png" />
