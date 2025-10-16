---
title: Share a Video
excerpt: How to share a Rev video with other services
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
Rev offers multiple options to share a video with other users from the video player on the [Sharing](doc:rev-video-player-features#video-sharing) flyout panel.

<Image align="center" alt="Click the Sharing icon to access the flyout panel" border={false} caption="Click the Sharing icon to access the flyout panel" src="https://files.readme.io/e523ff5-shareIcon.png" />

When you share a video:

* It must be in **Active**[status](doc:update-basic-video-settings#video-status)
* If set to an **All Users** or **Private**[Access Level](doc:update-basic-video-settings#video-access-control), users must log in to view it. When sharing **Private** videos, make sure that viewers have permission to view the video. Otherwise, viewers are notified that they are not authorized.
* This feature is not available for [Live videos](doc:link-to-video-urls)
* For Links shared on sites like Facebook, LinkedIn, and Twitter to render a thumbnail, title, and friendly description of the video, your Account Admin must enable [private metadata sharing](doc:private-metadata-sharing).

To share a video:

1. Navigate to the video you want to share and access the [Sharing](doc:rev-video-player-features#video-sharing) flyout panel.

2. Click the **Link** tab for sharing options.  The [Embed](doc:embed-a-video)  tab is used for generating the embed code needed for use on 3rd-party Websites.

3. The URL for the video link is displayed.  Modify the sharing settings below the URL as needed.

<Image align="center" alt={392} border={false} caption="The Link tab provides sharing options for a video when the Sharing flyout panel is accessed" title="shareVideo.png" src="https://files.readme.io/ce16698-shareVideo.png" />

* **Copy** - Click the copy text to copy the video link and start time to the clipboard. Note that not all browsers support this function. The text will not be present if your browser does not support clipboard copy.
* **Share to Webex Teams** - This icon is active only if you have the **Webex Teams integration** activated in Rev. It allows you to share the video to a previously defined [Webex Teams](doc:webex-teams#share-a-video-to-a-webex-team-space) space.
* **Email** - Generate an e-mail that links to the video. It begins playing the video URL at the designated start time when clicked. The video title and description will also be included in the e-mail body.
* **Start At** - If you want the video to play from the beginning, leave the **Start at:** field _unchanged_. Otherwise, specify where on the timeline you want to start sharing the video. To select a different time, select a different time on the timeline or manually enter the new time.
* **Show video only** - This toggle selects how you want to link to the video.  It is off by default.
  * **Off**:  Links to a complete video page including the header and navigation options
  * **On**: Links to the video only and no page structure is displayed (similar to embedding)
* **Autoplay** - Select if you want the video to autoplay when accessed. Autoplay videos start muted.
* Click the **Password** checkbox to include the password needed to view a Public video (if applicable) in the link.
