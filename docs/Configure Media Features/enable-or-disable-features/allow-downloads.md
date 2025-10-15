---
title: Allow Downloads
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
When [downloads](doc:video-features) are globally enabled, an **Enable Downloads** checkbox displays so that individual videos may be enabled for download to a PC to anyone viewing the video using the **Download** button on the [Video Basic Information](doc:rev-video-player-features#video-basic-information) flyout. 

To globally enable downloads for videos, select the **Allow download option on all media** checkbox under **Media Settings** > **Features** > **Video Settings**.

> 🚧 Important!
>
> Account Admins (including Media Admins) are *always* able to download videos even if this setting has been disabled.

When downloads are globally *enabled*:

* There is an **Enable Download**s checkbox on all individual video's [video settings](doc:updating-video-settings) form.
* There is a **Download** button on the [Video Basic Information](doc:rev-video-player-features#video-basic-information) flyout if the **Enable Downloads** checkbox is selected AND if the user accesses the page from a PC. This checkbox is disabled by default.
* There is a **Downloads** dropdown on the [Bulk Edit](doc:bulk-edit-video-settings#enable-downloads) interface.
* When a user selects to download an enabled video, it is downloaded from the DME that they have been directed to for watching the video.
* If there is an .mp4 file available, the user is provided the .mp4 file.
* If no .mp4 file is available, the user is provided the first non-HLS/HDS file available.
* The user is never be able to download an HLS or HDS file.
* If the video is a Webcast recording with PowerPoint slides, only the video is provided.

When downloads are globally *disabled*:

* There is no **Enable Downloads** checkbox on any [video settings](doc:updating-video-settings) form.
* This means that there is no **Download** button on any [Video Basic Information](doc:rev-video-player-features#video-basic-information) flyout.
* There is no **Downloads** dropdown on the [Bulk Edit](doc:bulk-edit-video-settings#enable-downloads) interface.
* When users are editing video, no video backups of the original may be made first (which is generally advised). You may enable this ability separately however.
* If downloads are globally disabled after they have already been previously enabled, the **Download** button is removed and the video is no longer available for download. If globally enabled again in the future, the video is once again available for download so long as the **Enable Downloads** checkbox on the individual video has not been modified/deselected.

### Allow Downloads for Video Backup

This setting is mainly used in concert with the **Allow Downloads on All Media** checkbox so that backups are still allowed when [editing video](doc:edit-a-video-clip) if downloads are disabled globally for individual videos. 

<Image title="allowDownloadVideoBackup.png" alt={897} align="center" src="https://files.readme.io/06c507b-allowDownloadVideoBackup.png">
  This setting means you can allow downloads for video editing backups while disabling all other video downloads
</Image>

> ❗️ Caution
>
> It is always recommended that an original copy of a video be downloaded before editing

For those organizations with security compliance policies in place that prevent downloads, this setting is used to allow the ability to download videos for backup *before* editing while all other downloads are still prevented.  Select the **Allow download from the video editor for backup** checkbox to enable this setting.

> 🚧 Important!
>
> Account Admins (including Media Admins) are *always* able to download videos even if this setting has been disabled.

When video backup downloads are globally *enabled*:

* *All* accounts with **edit permissions** are able to download a backup of an *original* video before editing.

When video backup downloads are globally *disabled*:

* There is no **Enable Downloads** checkbox on any [video settings](doc:updating-video-settings) page.
* There is no **Download** button on the [Video Basic Information](doc:rev-video-player-features#video-basic-information) flyout.
* There is no **Downloads** dropdown on the [Bulk Edit](doc:bulk-edit-video-settings#enable-downloads) interface.
* Video backups may *not* be made when editing videos.
* *Exceptions* to this are Account and Media Admins who will still receive the message that they may make a download backup of an original video when editing. (And only Admins)
