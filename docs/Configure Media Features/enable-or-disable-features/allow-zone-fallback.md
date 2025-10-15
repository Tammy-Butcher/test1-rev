---
title: Allow Zone Fallback
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
If you have the **Allow zone fallback for VOD** streams option checked, zone logic fallback and hierarchies are enabled in Rev. 

Select the **Allow zone fallback for VOD streams** checkbox under **Media Settings** > **Features** > **Video Settings** to enable. This option is enabled by default. 

When _enabled_:

- This adds failover and zone hierarchy logic to Rev for VOD streaming video.

When _disabled_:

- Zone logic only returns the playback URL of the DMEs in the user’s matched zone.
- Default zone is also ignored. So if you have DMEs only in the default zone, then no Playback URLs are returned and a "Playback of this video is not currently supported in this browser” message is displayed.
- Zone logic does not return a playback URL from Rev as noted.
- Downloads - Depend on different factors:
  - **No **playback URLs (**no **zones match) there are **no **download URLs.
  - Playback URLs (zone **matches **but the video is **not **yet available on the DME) the video downloads from REV until it is ready on the DME. Then it downloads from DME.

> ❗️ Warning!
> 
> If this option is disabled, zone logic only returns the playback URL of the DMEs in the user’s matched zone and zone logic does not return a playback URL from Rev.
> 
> Further, if there is **no **matching URL, then the viewer is displayed the following message: **“Playback of this video is not available at this time. Please try again later.”**