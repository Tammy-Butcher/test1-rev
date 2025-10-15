---
title: Enable Legal Hold
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
The **Legal Hold** functionality allows Account Admins to place a legal hold on any VOD video in Rev. 

To enable the Legal Hold functionality:

1. Navigate to **Admin > System Settings > Content Restrictions**.
2. Scroll to the **Legal Hold** section and enable the **Legal Hold** checkbox.

<Image alt="Enabling the Legal Hold checkbox makes this function available on the Rev portal" align="center" src="https://files.readme.io/a4bc19e-enableLegalHold.png">
  Enabling the Legal Hold checkbox makes this function available on the Rev portal
</Image>

When this checkbox is enabled, the **Apply Legal Hold** option is visible to Account Admins under **Video Settings** for a video.

<Image title="videoSettingsLegalHold.png" alt={139} align="center" src="https://files.readme.io/d9058e0-videoSettingsLegalHold.png">
  Videos in Legal Hold are not viewable anywhere except to Account Admins
</Image>

When selected, a video is placed on legal hold and is no longer viewable or accessible to other users of Rev. This function is *not* visible to any role except Account Admins.

A message and **Legal Hold Lock** icon is displayed in the upper left-corner of the video confirming that it is now in a state of **Legal Hold**. This status is also displayed in tile view.

<Image title="legalHoldVid.png" align="center" src="https://files.readme.io/522ff20-legalHoldVid.png" />

When Legal Hold status is applied:

* The video is set to **Inactive** status
* The **Delete** option is removed for all users, including Account/Media Admins
* Video Settings may not be edited either through Rev or Rev’s API
* The video may not be **Replaced**
* All **Video Approval** processes are stopped
* Account Admins are emailed with notice that it has been placed in **Legal Hold** status

When Legal Hold status is disabled (Video Settings > Remove Legal Hold):

* The video remains **Inactive**.  You must manually update the status.
* The **Delete** option is restored
* Video Settings and the ability to **Edit** the video is restored
* The video may be Replaced again by eligible users
* If the video was in an **Approval Process** prior to being placed on Legal Hold, the Approval Process will start over again from the beginning with the user requiring approval needing to request approval again
* Account Admins will be sent emails with updated details regarding the Legal Hold and the removal

> 👍 Tip
>
> The **Legal Hold** setting is also available under [Bulk Edit](doc:bulk-edit-video-settings#legal-hold-status) settings and can be used on several videos at once.
