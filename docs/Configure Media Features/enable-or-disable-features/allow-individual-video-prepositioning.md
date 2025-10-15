---
title: Allow Individual Video Prepositioning
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
You may want to preposition important content immediately instead of waiting for defined timeframes on the DME to occur. If you have the **Enable Prepositioning of Individual Videos** option enabled, you enable an additional option in [Video Settings](doc:updating-video-settings) titled [Preposition](doc:update-advanced-video-settings#preposition-a-video). 

Select the **Enable Prepositioning of Individual Videos** checkbox under **Media Settings** > **Features** to enable this setting. This adds a **Preposition **tab in [Video Settings](doc:updating-video-settings). The video must be finished processing before this will occur.

When *enabled*:
* The [Preposition tab](doc:update-advanced-video-settings#preposition-a-video) is visible to Media and Account Admins (Media Contributors are exempt)
* This tab can be used to set a date and time to preposition the individual video to all DMEs that have VOD playback set to **true**.
* Even those DMEs not marked to preposition content receive the video at the date and time specified so long as VOD playback is set to **true**.
* If other uploads are in progress, the prepositioned individual video is prioritized.