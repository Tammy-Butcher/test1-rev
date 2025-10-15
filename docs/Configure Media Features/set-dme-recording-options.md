---
title: Set DME Recording Options
excerpt: >-
  Instructions on setting a preferred recording order for a Primary and
  Secondary DME
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
Use the **Recording** menu to designate the DME order that Rev uses to record content. You are able to designate a primary and secondary DME device.

> 📘 Note
>
> To record content and event Webcasts, you \_must \_add a DME device. Once added, use **Monitor > Recording Status** in the DME Admin menu to verify ongoing status updates of DME recordings.

## Set a Primary and Secondary DME

To set a preferred recording order:

1. Navigate to **Media Settings > Recording**.

2. Use the **Primary DME** and **Secondary DME** dropdown options to set the recording order.

<Image title="recordingDME.png" alt={760} align="center" src="https://files.readme.io/95e85df-recordingDME.png">
  Navigate to Media Settings > Recording to set your Primary and Secondary recording options.  You must set up your DME devices first.
</Image>

> 📘 Note
>
> An RTSP unicast stream is required for recording Live Webcasts in Rev. Make sure that your stream has a keyframe interval between 2 to 5 seconds and do \_not \_use B-frames. See your individual encoder (stream source) documentation for setting information.

Keep in mind:

* Only \_Active \_DMEs may be selected and used
* The **Secondary DME** is used in the event the **Primary DME** becomes unavailable or reaches maximum storage capacity
* To avoid maximum capacity issues, the Account Admin is displayed this information upon DME selection. (**Total Disk Space / Free Disk Space**)
* After you have set a DME, in the DME Admin Menu, navigate to **Monitor > Recording Status** to obtain real-time status updates on any ongoing recordings on this DME. Specifically, you may:
  * Verify the existence of an ongoing recording
  * Verify status of the ongoing recording
  * Get a copy of source URL
