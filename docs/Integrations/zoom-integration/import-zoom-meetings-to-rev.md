---
title: Import Zoom Meetings to Rev
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
[block:html]
{
  "html": "\n<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


You can choose to have your Zoom meetings imported automatically or you can choose to import them manually.  Both options are described here.

## Automatically Import Zoom Meetings

You can choose to make Rev your repository for all of your recorded Zoom meetings by having Rev ingest any new recordings from your Zoom meeting site automatically.

To automatically import a Zoom meeting:

1. Navigate to **Admin** > **Media Settings** > **Integrations** > **Zoom**.
2. Make sure the **Automatically import Zoom meeting recordings** checkbox is selected.  Once it is selected, more options become visible. Each setting is described in the table below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fada0e7-zoomAutoImport.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


| Setting                                   | Description                                                                                                                                                                                                                        |
| :---------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Import Past Recordings                    | Enter a number from 1 to 90.  Skips importing meetings older than the number (of days) entered.                                                                                                                                    |
| Default Uploader                          | Required.  Must be a user account and not a group.  This is the [default uploader](doc:video-owner) that will be assigned as the uploader to any newly imported Zoom meeting.                                                      |
| Import Recordings for the Following Users | All Users is the default selection.  You can specify specific users and groups if desired.                                                                                                                                         |
| Access Control                            | Required. The [Access Control ](doc:video-access-control)to set for newly imported recordings. The default is Private. You can only specify a Team here if you are a contributor for that Team.                                    |
| Subtitles                                 | This setting is enabled by default and will import [subtitle files](doc:/video-languages) if they are available for the recording.                                                                                                 |
| Deletion                                  | This setting is disabled by default.  It will delete the recording in Zoom after it is imported to Rev.  **_Enable this setting with Caution!_**                                                                                   |
| Status                                    | Required. This setting is Inactive by default.  [Sets the status](doc:video-status) of the newly imported recording to Active or Inactive. Note that any defined Approval Workflows will always take precedence over this control. |
| Expiration                                | This setting is off by default.  Allows you to set an [Expiration Date or Rule](doc:video-publish-and-expiration-dates) for the newly imported recording.                                                                          |
| Categories                                | Apply one ore more [categories](doc:video-categories) to the imported recordings.                                                                                                                                                  |
| Tags                                      | Apply one or more [tags](doc:video-title-description-and-tags) to the imported recordings.                                                                                                                                         |

## Manually Import a Zoom Meeting

You can quickly and easily manually import one or more of your Zoom Meeting recordings into your Vbrick portal.

To manually import a Zoom meeting:

1. Click the **Upload Tray** > **Import Meetings** tab > **Zoom Meetings** icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e79710d-importZoomMeetings.png",
        null,
        "Click the Import Meetings tab and then select the Zoom Meetings icon"
      ],
      "align": "center",
      "caption": "Click the Import Meetings tab and then select the Zoom Meetings icon"
    }
  ]
}
[/block]


2. A list of recorded meetings associated with your Zoom account appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/073da98-zoomVideosAvailable.png",
        null,
        "Select the videos you want to import by clicking the checkbox next to it"
      ],
      "align": "center",
      "caption": "Select the videos you want to import by clicking the checkbox next to it"
    }
  ]
}
[/block]


3. Select one or more videos to import by clicking the checkbox next to the video.
4. If a transcript is associated with the video, a dropdown appears allowing you to select the language of the transcript file.
5. Once all videos are selected, click the **Import** button to begin your import.  You will be notified via the **Notifications** tray and email once it has concluded.

> 👍 Tip
> 
> If you do not see the **Zoom Meetings** icon in the **Import Meetings** tab on the Upload tray, make sure you have updated your _Vbrick Rev_ Zoom App to the [latest version](doc:zoom-integration#update-the-zoom-integration).