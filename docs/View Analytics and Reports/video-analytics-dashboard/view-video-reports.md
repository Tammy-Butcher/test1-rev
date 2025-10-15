---
title: Video Report Downloads
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
## Download Video Views Report

To download the complete **Video Views** report, click the **CSV** tab next to the **Date** control. 

<Image title="downloadVideoViewsReport.png" alt={905} align="center" src="https://files.readme.io/e5198cd-downloadVideoViewsReport.png">
  The CSV tab next to the Date Control downloads the Video Views report from the Video Analytics Dashboard
</Image>

A \<video\_name>.csv file is downloaded to your **Downloads** folder with the following viewing data statistics about the video:

* Date \[each video] is viewed - For continued sessions that take place on different days, the Date Viewed cell will be the most recent date that the video was resumed; not the first day that the video was started/viewed.
* Username of person who viewed the video
* First name of person who viewed the video
* Last name of person who viewed the video
* Email address of person who viewed the video
* IP Address of the person who viewed the video
* Whether or not the video was completed - A video completion occurs when a user’s viewing time is greater than or equal to 90% of the duration of the video.
* Zone the video was viewed from
* Device that was used to view the video - PC or Mobile
* Playback URL
* The type of browser the person used - Chrome, Edge, Firefox, etc.
* Viewing Time - The amount of time that a user has spent viewing a video. Note that you could see multiple entries for a user for one video in VOD analytics during different play-through of the video. This is because Viewing Time resets once a viewer has completed watching the video.
* Drop-Off Time (if applicable) - The maximum point a viewer watched in a video as reported by a heartbeat in a player every 30 seconds or whenever a user presses Play, Pause, or Seeks to another point in the video.
* Platform Version - Specific Operating System (Windows 10, macOS 10.14 Mojave, Android 9.0, etc.).
* Platform - Generic Operating System (Windows, macOS, Android, iOS, etc.).

## Download Video Inventory Report

The **Video Inventory Report** is accessible by Account and Media Admins from the Search/Filters toolbar.

<Image title="downloadVideoInventoryReport.png" alt={352} align="center" src="https://files.readme.io/21ff674-downloadVideoInventoryReport.png">
  If you click the CSV icon without filtering it, the report downloads all the videos, all the uploads, all of the category, and so forth
</Image>

Inventory reports are based on the content that you have access to and on the search results and filters you set. For example, if you run a search on the keyword “Training”, you can retrieve an inventory report on the search results returned. 

Another use case is a report on the results returned from **Media** > **My Videos**. Note: Unlisted videos are included in inventory reports.

Specifically, you can retrieve a report from the following areas in Rev:

* Search Results (tile, list, bulk edit)
* All Videos
* My Videos
* Category video listing
* Channel video listing
* Expirations
* Pending Approvals

The **VideoInventory.csv** is placed in your **Downloads** folder.

> 👍 Tip
>
> The **Video Inventory** report is generated asynchronously and you are notified when your download is complete to better support larger video libraries.
