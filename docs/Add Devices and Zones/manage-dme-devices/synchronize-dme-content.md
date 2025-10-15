---
title: Synchronize DME Content
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
Once the DME is saved, you may initiate a content sync to a DME so that users obtain content immediately from that DME. This is useful if the DME is added later to the video ecosystem so that it may obtain all current content in Rev.  

* A sync may \_only \_be scheduled in the future.
* If a pending sync is already scheduled, it is noted in the **Status** column on the **DME Management** module.
* A scheduled sync can be canceled at any time by unchecking the **Schedule Sync** checkbox and saving your changes. If the scheduled sync has already started, you can cancel the sync by clicking the **Cancel** button.

<Image title="scheduleSync.png" alt={1154} align="center" src="https://files.readme.io/e5aca6c-scheduleSync.png">
  The Sync Now button performs an immediate content sync on demand
</Image>

The **Sync Now** button is only available if the DME is in **Active** status and the **VOD Playback Device** checkbox is enabled.

When a content sync is initiated the DME downloads all **Active** videos in batches of ten. The \_oldest \_content downloads first (ascending by upload date/time)

During the sync, playback URLs are updated based on:

* If playback URLs already exist, they are overwritten.
* If playback URLs do \_not \_exist, they are added.
* The DME \_always \_sends back playback URLs, even if it already has the content, to indicate to Rev that the video is synced.

The following sync rules are also observed:

* If your DMEs support the **MESH** caching feature, the DME attempts to get the videos from a meshed DME first before it attempts to retrieve files from Rev.
* The DME only downloads files that it does \_not \_have.
* The content sync may be canceled at any time by clicking the **Cancel** button. All videos that have been sent to the DME for download will continue. All videos that have \_not \_yet been sent to the DME (queued) are canceled.
* You may also sync the device from the **Actions** dropdown on the **DME Management** module.

## Bulk Schedule DME Content

<Image title="dmeScheduledDownload.png" alt={202} align="center" src="https://files.readme.io/3d25d8f-dmeScheduledDownload.png">
  Use the Bulk Action dropdown to create a common maintenance schedule for all of your DMEs
</Image>

The **DME Management Bulk Action** dropdown menu allows you to create a schedule for several DMEs at once. This means you can synchronize their content on the same day and time so that Rev creates and performs a maintenance schedule of your choosing and you are easily able to manage it under one intuitive interface.

To create a bulk schedule content sync:

1. Navigate to **Devices** > **DME Management**.

2. Select checkboxes to the left of the DMEs you want to add to the schedule.

3. Click the **Bulk Action** > **Scheduled Download** dropdown.

<Image title="bulkScheduleDmeDownload.png" alt={1202} align="center" src="https://files.readme.io/76ac729-bulkScheduleDmeDownload.png">
  Easily create a maintenance sync for your DMEs with the Scheduled Download option under Bulk Actions
</Image>

* Just as with individual content syncs, bulk syncs may only be scheduled in the future.
* If a pending sync is already scheduled, it is noted in the **Status** column of the device on the **DME Management** page.
* A scheduled sync can be canceled at any time by editing the \_individual \_DME’s schedule.

> 📘 Note
>
> All selected DMEs are set to preposition content as part of scheduling their download windows.
