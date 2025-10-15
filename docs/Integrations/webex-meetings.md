---
title: Webex Meetings
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


Users may upload their Webex meeting recordings (**My Webex** > **My Files** > **My Recordings**) directly from Vbrick Rev if a **Webex Meetings** site is added and configured. Only Account Admins and Media Admins are able to add and configure a meeting site in Rev.

If your organization supports multiple Webex Meetings sites, Rev allows you to configure as many as needed with supporting functionality to edit, delete, and duplicate sites.

> ❗️ Warning!
> 
> This integration requires that **AllowDownloadRecordingWithoutPwd** is enabled for your Webex site as described in, "F9847 A New Download URL is able to Download Recording Directly”.
> 
> Submit a ticket to the **Webex Provisioning Team** to enable this feature flag before proceeding.

## Requirements

- Webex Meetings v29+
- Webex Meetings Admin access
- **AllowDownloadRecordingWithoutPwd** must be enabled for your Webex site. Submit a ticket to your Webex Provisioning Team to enable this feature flag before proceeding if you are not sure this is enabled.
- [Webex Developer Site](https://developer.webex.com/docs/integrations) log in with a **Webex Meeting app** created and [scoped](doc:webex-meetings#webex-meeting-app-setup) correctly.
- Live Streaming support configuration requires **Rev Cloud** and **Webex Meetings vWBS39.10+**

> 🚧 Important!
> 
> You must make sure you have updated your Webex Meeting App to make sure it is compatible with new APIs and contains the new [scopes](doc:webex-meetings#webex-meeting-app-setup) detailed below or it will _not_ function correctly!

## Configuration

### Webex Meeting App Setup

Before you can setup the integration in Rev, you need to create an App on the [Webex Developers](https://developer.webex.com/docs/integrations#scopes) site and make sure it has the correct scopes applied. Enter the following Rev-specific information and scopes below during the creation of the Webex Meeting app.

> 📘 Note
> 
> You must be a Webex Admin to complete this step.

| Webex Meeting App | Rev Configuration                | Example                                                                     |
| :---------------- | :------------------------------- | :-------------------------------------------------------------------------- |
| Redirect URI(s)   | `<RevURL>/webex-oauth/cb`        | `YourOrgsRev.com/webex-oauth/cb`                                            |
| Scopes            | `meeting:admin_recordings_read`  | Retrieve recordings of all WebEx users of your organization                 |
|                   | `meeting:admin_recordings_write` | Manage or delete recordings of all WebEx users of your organization         |
|                   | `meeting:admin_transcripts_read` | Retrieve Webex meetings transcripts of all WebEx users of your organization |

Click the **Add Integration** button to save the Webex Meeting App and make note of the **Client ID** and **Client Secret** under the **OAuth Settings** section.

### Rev Integration Setup

There are different configurations for a **Webex Meetings** site in Rev including the ability to specify auto versus manual Meeting imports, and Live streaming options. Make sure you have created and scoped your **Webex Meeting app** on the Developer's site as described above before you begin.

To add a Webex Meetings site:

1. Navigate to **Media Settings** > **Integrations** and scroll to the **Webex Meetings** section.

2. A table of Webex Meetings sites already created displays with the following information:
   - **Name**: User-provided name of the site when configured.
   - **Auto Import**: Specifies if the site is available or used for Live streaming.
   - **Manual Import**: Specifies if the site is available for manual import.
   - **Live Streaming**: Specifies if the site is enabled for Live streaming.
   - **Status**: Specifies site status - Linked, Unlinked, or not applicable (blank).
   - **Actions**: Edit, Delete, or Duplicate an existing site. Note that if you delete a site that any pending scheduled auto-imports are also removed. This does _not_ interrupt an in-progress import however.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6d93a90-webexMeetingsModule.png",
        null,
        "The Webex Meetings table provides an overview of all created sites.  Use the Actions dropdown to edit, delete, or duplicate existing sites."
      ],
      "align": "center",
      "caption": "The Webex Meetings table provides an overview of all created sites.  Use the Actions dropdown to edit, delete, or duplicate existing sites."
    }
  ]
}
[/block]


3. Click the **Add Webex Meeting Site** button to add a new site.  Or use the **Actions ** dropdown to duplicate an existing site to keep its settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/39350c5-basicWebexMeetingSiteFields.png",
        null,
        "These settings need to be completed first to save a basic Webex Meetings site in Rev"
      ],
      "align": "center",
      "caption": "These settings need to be completed first to save a basic Webex Meetings site in Rev"
    }
  ]
}
[/block]


4. To add a basic Webex Meetings site, complete and **Save** the following options as needed:

- **Webex Meeting Site Name**: A descriptive name for the site. This is a required field.
- **Description**:  A description for the Webex Meeting site you are creating.
- **Hosted Website (Webex Meeting Site Url)**: The **Site Brand Name** field found in the **Site Administration** section when logged in Webex Meetings as an Admin.  This is a required field.

> 🚧 Important!
> 
> Pay particular attention to the **Hosted Website** field. _You must include https\:// here_.

- **Support for Webex Meeting Live Streaming**: Enables [Live streaming](doc:webex-meetings#support-for-webex-meetings-live-streaming) from Webex Meetings. This is an optional checkbox. Configuration is described below.
- **Support for Import Recordings**: Opens manual and auto [import configuration options](doc:webex-meetings#configure-import-settings) for Webex Meetings recordings. This is an optional checkbox.  Configuration is described below.

<h4>Enable Support for Webex Meeting Live Streaming</h4>

When **Support for Webex Meeting Live Streaming** is enabled, you are able to access the following functions directly _from_ your Webex Meetings client:

- [Stream a Webex Meeting to a New Rev Webcast Event](doc:webex-meetings#stream-to-a-new-rev-event). Start and broadcast your Webex Meetings, including the ability to save your meeting as a (VOD) video once completed, to a _new_ Rev Webcast event. Some Rev Webcast event features are limited until after the event starts (such as polls and Q&A) at which point you may edit them inline.
- [Stream a Webex Meeting to an Existing (Scheduled) Rev Webcast Event](doc:webex-meetings#stream-to-a-rev-scheduled-event). Start and broadcast your previously _scheduled_ Rev Webcast event directly from your Webex Meeting, including the ability to save your meeting as a (VOD) video once completed.
- [Stream a Webex Meeting as a new VOD Recording](doc:webex-meetings#record-a-webex-meeting-as-a-new-rev-vod). This records your Webex Meeting as a new (VOD) video in Rev. Once complete, update the Video Settings in Rev as you normally would.

<h4>Enable Support for Import Recordings</h4>

When you enable the checkbox for **Support for Import Recordings**, you will be able to choose to **manually** import Webex Meeting Recordings or have them automatically imported instead.

> 📘 Note
> 
> To import Webex meeting recordings, you must create a **Webex Meeting App** to grant Rev permissions to Webex Meetings. This is done through the [Cisco Developer](https://developer.webex.com/docs/integrations#scopes) site by creating a **New Integration** as described in the [Webex Meeting App setup](doc:webex-meetings#webex-meeting-app-setup) section above. This provides you a **Client ID** and **Client Secret** that can then be assigned in the required fields below.

To configure your Webex Meetings Import Settings:

1. Select the **Support for Import Recordings** checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3cfa76d-commonIdentitySiteFields.png",
        null,
        "The Common Identity Site fields are visible once you enable Support for Import Recording.  You will need values from the Webex Meeting App created on the Cisco Developer Site to complete them."
      ],
      "align": "center",
      "caption": "The Import options are visible once you enable the Support for Import Recordings checkbox.  You will need your Client ID and Client Secret from your Webex App to configure importing."
    }
  ]
}
[/block]


2. **Site Name**: This is normally provided by Webex. By default, it is the sub-domain on the webex.com URL. For example, for `acme.webex.com`, the site name is `acme`.
3. **Client ID**: Provided by the Webex Meeting App.
4. **Client Secret**: Provided by the Webex Meeting App.
5. **Link to Webex Site** button: This launches authentication to Webex to obtain an access token. Status is displayed directly on the button once it is linked.

- **Green checkmark: Linked** - authentication is established and access token was received and is valid (last known).
- **Red X: Not currently authenticated** or the access token is now no longer valid or in a current state of authentication.

> 👍 Tip
> 
> You will need to **Save** your site first before the ability to **Link** it becomes available.  You will also need to click the button again each time you update your Webex app.  Most customers link their site to import Webex meetings.  If this is the case, it is recommended you also choose an import option as well.

6. Finally, when you add a **Webex Meetings** site, you need to decide how you will import your saved video as part of that site configuration. You may choose to **manually** import or to **auto **import each time a meeting is saved as a video.  Both import types and how to set them up are described in the sections below.

> 🚧 Important!
> 
> Rev only allows a maximum of 100 hours of ingested recordings per day and/or 10 hours of ingested recordings per recurrence to prevent overwhelming the system at any one time. 
> 
> A recording will not be re-imported if it has previously been ingested even if it has since been removed or deleted from Rev.

<h4> Manual Import </h4>

Click the **Manual Import of Webex Meetings Recordings** checkbox to enable manual imports.

What this does:

- This site now appears in the meeting dropdown when you click the **Upload Tray** > **Import Meetings** > **Webex Meetings** icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fc11adc-importZoomMeetings.png",
        null,
        "Enabling Manual Import makes this Webex Meeting Site available in the Webex Meetings dropdown under Import Meetings"
      ],
      "align": "center",
      "caption": "Enabling Manual Import makes this Webex Meeting Site available in the Webex Meetings dropdown under Import Meetings"
    }
  ]
}
[/block]


- If you choose the site, the **Import **tab lists the 100 most recent video files (within the last 180 days only) that are available in MP4 format. (Note: Legacy Webex accounts with .arf files are not supported in this integration)
- Only the newest video files are listed first with the following attributes:
  - Recording name
  - Create date and time
  - File size (MB)
  - If the file has already been imported to Rev (if previously uploaded and deleted, it will not be marked as imported)
  - Multiple files may be selected and imported
- If the videos are not listed when selecting webex meetings please ensure your user details for your Rev account include your email address.

<h4> Auto Import </h4>

You can choose to automatically import your saved meeting videos. This allows you to leverage Rev as the repository for all recorded Webex Meetings and also have Rev automatically ingest any new recordings from your Organizational site. Click the **Automatically Import Webex Meeting Recordings** checkbox.

There are a number of options that are available when you choose to configure auto-import. They include:

- Automatically delete recorded Webex Meetings from the Webex Site once they are imported into Rev
- View how many Site meeting recordings remain to be imported into Rev
- Stop an import process if needed

<h5> View Total Imports and Remaining Imports</h5>

Rev automatically keeps track of the number of imports that have occurred (every 30-60 minutes) and the number of Webex Meetings videos left to import based on the settings you configure. This is viewed directly under the **Auto Import** checkbox.

Also displayed:

- Date and time of the last (most recent) import
- Number of meeting recordings imported on the last run of the import
- Number of meeting recordings remaining to import (if any). **Note**: If import in progress, a **Postpone **button is visible next to this detail to postpone the import.
- Date and time of next scheduled import (if applicable)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec56a17-autoImportsRemaining.png",
        "autoImportsRemaining.png",
        722
      ],
      "align": "center",
      "caption": "When auto imports are enabled, the number of videos imported along with how many are remaining is displayed"
    }
  ]
}
[/block]


Click the **View Log** button for more details on specific dates of the imports. You are also able to view this log from the **Actions **dropdown menu next to the Webex Site. You are able to observe:

- Date and time of the import run
- Number of meetings imported on that run
- Number of meetings not imported (individual videos are disabled from importing)
- Number of meetings postponed
- Status (Success, Partial, Error)
- Details
  - Partial (Exceeded maximum videos allowed per day)
  - Errors/Warnings
- Admin must re-authenticate with Webex
- Exceeding available storage
- Other system errors

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/61f2e25-autoImportLog.png",
        "autoImportLog.png",
        722
      ],
      "align": "center",
      "caption": "The View Log button provides more details on the video imports"
    }
  ]
}
[/block]


<h5> Set Age of Import and Default Uploader</h5>

You have the option to specify how many days back Rev should go when auto importing video from a site. For example, you can specify that Rev should _only_ import meetings that were recorded within the past 10 days. You can also configure a default **Uploader **and email address to assign to the import.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/96c1d8a-meetingAgeUploader.png",
        "meetingAgeUploader.png",
        671
      ],
      "align": "center",
      "caption": "Set the age of the imported meeting and the default Uploader and email address if needed"
    }
  ]
}
[/block]


This is accomplished through the following:

- **Skip importing meetings older than (# of days)** - In the image above, videos older than 50 days are not auto imported.
- **Select Default Uploader** - You may enter a default user account that is assigned as the video uploader in this field. Otherwise, you may use autouploader here. **Note**: The user account _must_ be a Media Contributor or higher and cannot be a group.
- **Use Email Address to Match Uploader** - If this checkbox is enabled, then the video uploader is set as the Rev user account that matches the Webex Host’s email address. If no matching email address is found, then the **Default Uploader** field is used instead.

<h5> Import Recordings for Specific Users </h5>

You can specify to import recordings for specific users by adding them to the **Import recordings for the following users** selection box.  This designates that _only_ those specific users, Groups, or Team recordings are imported instead of all meeting recordings. **Note:** If a Team is set and the effective Uploader does _not_ have **Team Contributor** or higher permissions for the selected Team, then the video is not assigned to that Team.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/53b2c78-importRecordingsforUser.png",
        null,
        "Specify to import specific users, groups, or team recordings by adding them here"
      ],
      "align": "center",
      "caption": "Specify to import only specific users, groups, or team recordings by adding them here"
    }
  ]
}
[/block]


<h5> Delete Recordings </h5>

Use the **Delete Recordings** checkbox if you want to remove the videos from your Webex Meetings site once they have been ingested into Rev.

> ❗️ Warning!
> 
> Be aware that if you use this setting, your videos are _permanently_ deleted from your Webex Meeting and you are _not_ able to retrieve them. Use with caution!

<h5>Configure Video Settings </h5>

Finally, you may configure several **Video Settings** with the auto import setting just as you normally would when uploading a video. They are:

- Access Control
- Status
- Expiration Rules
- Categories
- Tags

For more details, view the corresponding [Video Settings](doc:updating-video-settings) help topic.

## Usage

### Manually Import Video from a Webex Meeting

Use the **Webex Meetings** icon in the **Import Meetings** tray to import videos from a Webex Meetings site that you have configured for [manual import](doc:webex-meetings#section-manual-import). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4f2e4ff-importWebexMeetings.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


You must also have **video upload permissions**. The 100 most recent meeting videos (within the last 180 days) of the (logged-in) Webex user’s account are available for upload into Rev when you use this feature.

To import a video from a Webex Meeting:

1. Click **Add Content** icon on the menu bar.
2. Click the **Import Meetings **tab > **Webex Meetings** icon.
3. You are prompted to log in with your Webex user account if you are not logged in. 
4. You will need to select a **Webex Meetings** site you want to import from if multiple sites have been configured for use.
5. Use the **Select Videos** window to choose which videos from Webex to import.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/706dc35-importWebexMeetingsVideos.png",
        null,
        "Use the Webex Meetings Select Videos window to decide which meeting videos to import to Rev"
      ],
      "align": "center",
      "caption": "Use the Webex Meetings Select Videos window to decide which meeting videos to import to Rev"
    }
  ]
}
[/block]


6. Click the **Name **checkbox to select and import all videos.

7. Only **MP4** videos are displayed and supported for Webex import. (.ARF files are _not_ imported.) Note that you should be on **v29** or higher of Webex and you may need to ensure that **MP4 **recording files are available if you have issues with your import.

8. Once your video(s) are finished uploading and transcoding, you receive an email with a link to the video. This means you do not have to keep manually checking your videos to see if they have finished processing.

9. Similar to a Rev video upload, Webex uploads are automatically set to **Inactive **status by default unless your Admin has specified otherwise. Your Webex upload appears under the **My Videos** menu option with its Webex title. Rev **Video Settings** should be assigned such as categories, tags, and so forth before setting it to **Active** status.

### Record a Webex Meeting as a New Rev VOD

You can use Webex Meetings as a source for a new video recording if you have enabled [Support for Webex Meetings Live Streaming](doc:webex-meetings#support-for-webex-meetings-live-streaming).

> 📘 Note
> 
> This is a **Rev Cloud** only feature that requires **Webex Meetings WBS39.10** or later.

When support for Webex Meeting Live streaming is enabled for VOD recording:

- The Webex Meetings **Vbrick Rev Streaming** interface presents an option to **Record Video**. Only those Rev user accounts with **Media Contributor** permissions or higher are able to use this function.
- The maximum recording duration is **10 hours**.
- The recording ends if the meeting stream stops for more than 5 minutes. An email is sent to the Webex Meeting **Host **with a URL to the video recording so that **Video Settings** in Rev may be configured and finalized.
- This functionality supports conversion to **MP4 **for download.

To stream a Webex Meeting as a new Rev VOD recording:

1. Login to your Webex Meetings account when you are ready to stream to a new VOD recording. 

2. Start a meeting.

3. In the Header navigation menu, click **Meeting** > **Start Live Streaming**. It is also available in the 3 dot menu featured at the bottom of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7fbbbab-startWebexLiveStreamingMenu.png",
        "startWebexLiveStreamingMenu.png",
        295
      ],
      "align": "center",
      "caption": "After you start your Webex Meeting, click the Start live streaming option to initiate the Rev menu functions"
    }
  ]
}
[/block]


4. You are prompted to login to Rev. You _must_ login to an account that is listed as a **Media Contributor** or above or you will not be able to record the Live stream from the Webex Meeting.

5. Select the Rev function you want to initiate from the Webex Meeting; in this case **Record Video**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0480bf3-revWebexMenuFunctions.png",
        "revWebexMenuFunctions.png",
        445
      ],
      "align": "center",
      "caption": "After you log in to Rev, tell Webex what you want to do with the Live Stream.  In this case, you will Record Video."
    }
  ]
}
[/block]


6. The **Name **of the final video is created from the name you give when you schedule a Webex Meeting (or the name of your personal room). Click the **Start Recording** button to start Rev’s recording interface.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f08b26c-webexMeetingVODName.png",
        "webexMeetingVODName.png",
        498
      ],
      "align": "center",
      "caption": "Webex Meeting to Rev recording naming conventions are taken from what you name your scheduled meeting in Webex"
    }
  ]
}
[/block]


7. Click the **Start Streaming** button to begin the Live stream of your Webex Meeting window to Rev.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e7ceaac-webexStartLiveStream.png",
        "webexStartLiveStream.png",
        442
      ],
      "align": "center",
      "caption": "After Rev's recording interface is started, click the Start Streaming to send the Live stream to it"
    }
  ]
}
[/block]


8. The Webex Meetings interface notes that you are **Live** and **Connected **in the upper right corner of your meeting window.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9176214-webexMeetingStatusBox.png",
        "webexMeetingStatusBox.png",
        320
      ],
      "align": "center",
      "caption": "Check the Webex Meeting connection status in the upper right corner"
    }
  ]
}
[/block]


9. All **Video Settings** can be be edited in Rev as usual once the video stops recording and processing.

### Use Webex Meetings Live Streaming With a Rev Webcast

As a Webex meeting Host, you can use **Webex Meetings Live Streaming** feature and have it serve as the video source for a **new **Rev Webcast event or a previously **scheduled **Rev Webcast event.

When you select Webex Meetings as a source, you may then **start **and **broadcast **your Webcast directly from your Webex Meetings account. This means you can take advantage of Rev’s Webcast functionality and pair it with a Webex Meeting. Afterwards, you can save the recording and use Rev’s **Video Settings** and metadata.

<h4>Requirements</h4>

- Support for [Webex Meetings Live Streaming](doc:webex-meetings#support-for-webex-meetings-live-streaming) must be enabled
- You _must_ be logged in to a Webex Meeting account that matches an **Event Host** of the Webcast for the Rev event (or a **Rev Account Admin** account)

### Stream to a Rev Scheduled Event

To stream a Webex Meeting to a previously scheduled Rev Webcast:

1. Navigate to the **Event Calendar** and schedule a Rev event as you normally would.

2. Select **Webex Meeting Stream** as the **Video Source**. If you do not see this tab, **Webex Meeting Live Streaming** is not enabled.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/52bc1f7-webexMeetingStreamForEvent.png",
        "webexMeetingStreamForEvent.png",
        1130
      ],
      "align": "center",
      "caption": "With Webex Meetings Live Streaming enabled, you are able to use a Webex Meeting Stream as a source when you scheduled events in Rev"
    }
  ]
}
[/block]


3. Login to your **Webex Meetings** account when you are ready to stream to a Webcast Event in Rev. 

4. Start a meeting.

5. In the **Header **navigation menu, click **Meeting **> **Start Live Streaming**. It is also available in the Dot menu featured at the bottom of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c3bca3a-startWebexLiveStreamingMenu.png",
        "startWebexLiveStreamingMenu.png",
        295
      ],
      "align": "center",
      "caption": "After you start your Webex Meeting, click the Start live streaming option to initiate the Rev menu functions"
    }
  ]
}
[/block]


6. You are prompted to log in to Rev. Remember, you _must_ login to an account that is listed as an **Event Host** on the **Rev Webcast** (or an **Account Admin** account).

7. Select the Rev function you want to initiate; in this case **Existing Webcast**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c5d244-revWebexMenuFunctions.png",
        "revWebexMenuFunctions.png",
        445
      ],
      "align": "center",
      "caption": "After you log in to Rev, tell Webex what you want to do with the Live Stream.  In this case, you will stream to an Existing Webcast."
    }
  ]
}
[/block]


8. Each Webcast that you are authorized to stream to appears in the **Select an Event** drop-down (i.e., those Webcasts where you are an **Event Host** or if you are an **Account Admin**, those Webcasts that are currently available and not streaming from another Webex Meeting).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1b3c637-availableRevWebcasts.png",
        "availableRevWebcasts.png",
        502
      ],
      "align": "center",
      "caption": "Only Rev events that you are a Host of appear in the Select an Event dropdown.  Or, if you are an Admin, events that are not currently in use with another Webex Meeting."
    }
  ]
}
[/block]


9. Click **Start Webcast**. This starts the Webcast in Rev. Depending on the time-frames defined for the Webcast, you may have the following button options available:
   - **Pre-Production**: Webcast automatically starts and broadcasts a Pre-Production Event. (Host a Webcast Event Dry Run)
   - **Main Event**: Webcast automatically starts and broadcasts a Main Event. (Host a Production Webcast)
   - **Overlaps**: If a potential overlap period occurs where either run may be started, you are presented with the option to select which type to stream.

10. Click the **Start Streaming** button to begin streaming your **Webex Meeting** to the **Rev Webcast** you selected. If you selected a Webcast event that has already been started in Rev, you then begin streaming your Webex Meeting to that event. If it has not been started in Rev, Webex Meetings automatically starts it for you at this point and begins broadcasting.

11. Webex Meetings indicates that you are **Live **and **Connected **in the upper right corner of your meeting window.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/82edafa-webexMeetingStatusBox.png",
        "webexMeetingStatusBox.png",
        320
      ],
      "align": "center",
      "caption": "Check your connection status in the upper right corner of your Webex Meetings window"
    }
  ]
}
[/block]


12. If, for any reason, you stop the live stream in your Webex Meeting, attendees will see “**The Webex Meeting Host is not currently live streaming**”. You can stop and start the stream as many times as you need/desire. Rev handles the interruptions with a placeholder image that you can edit out in the final video.

13. Webex Meetings are automatically recorded. Upon ending the Rev Webcast, the **Event Host** is asked to **Save **the recording with the option to discard it if requested.

14. A **Webex Meeting Live Streaming** event automatically ends when the scheduled end time is reached and when there is no longer an active Live stream received from Webex Meeting. At that time, you are given the option to save the recording of your **Webcast **to a **VOD **recording. You are encouraged to use Rev’s **Video Settings** to configure your saved video at that time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/261668d-webexEndEvent.png",
        "webexEndEvent.png",
        704
      ],
      "align": "center",
      "caption": "You have the option to save your recording at the end of your event"
    }
  ]
}
[/block]


### Stream to a New Rev Event

The initial steps to stream to a new Rev event are very similar to streaming to a previously scheduled Rev Webcast.

To stream a Webex Meeting to a new Rev Webcast:

1. Login to your **Webex Meetings** account when you are ready to stream to a Webcast Event in Rev. 

2. Start a meeting.

3. In the **Header **navigation menu, click **Meeting **> **Start Live Streaming**. It is also available in the Dot menu featured at the bottom of the screen.

4. You are prompted to log in to Rev. Remember, you _must_ login to an account that is listed as an **Event Host** on the **Rev Webcast** (or an **Account Admin** account).

5. Select the Rev function you want to initiate; in this case **New Webcast**.

6. A simplified **Rev Webcast form** is displayed that captures the minimum set of _required_ fields to launch a new event in Rev. You may use **inline editing** once the Webcast begins to add more settings if needed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c168ac1-newWebcastLiveStream.png",
        "newWebcastLiveStream.png",
        397
      ],
      "align": "center",
      "caption": "When you choose to Live stream to a new Rev Webcast, you will need to complete some basic settings for Rev first"
    }
  ]
}
[/block]


7. Complete the required fields to start your **Live Stream to a New Webcast**.

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Title",
    "0-1": "Defaults to the **Webex Meetings room name**. You can edit this.",
    "1-0": "Description",
    "1-1": "Defaults to the **description of the Webex meeting**. You can edit this.",
    "2-0": "Start Date & Time / End Date & Time",
    "2-1": "Set to match the **Webex meeting** scheduled details (_you cannot change the Start Date/Time_, however, you can change the End Date/Time). The duration is set to **one hour** by default.",
    "3-0": "Video Source",
    "3-1": "Set to Webex meeting stream. **Not editable**.",
    "4-0": "Host",
    "4-1": "Set to the authenticated Rev user account. **Not editable**.",
    "5-0": "Listing Type",
    "5-1": "Set to **Private **by default. Editable.  \n  \nIf set to Public, you are able to specify an optional password. All other edits should be configured inline."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]


8. Click the **Start Main Event** button. Rev creates the event.

9. You can then click **Start Streaming** when you are ready to stream from your Webex meeting to the **Rev Webcast **.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/621a6e5-startLiveStreamtoNewEvent.png",
        "startLiveStreamtoNewEvent.png",
        402
      ],
      "align": "center",
      "caption": "Once Rev has created the event and you are ready to start streaming your Webex Meeting to the Rev Event, click the Start Streaming button"
    }
  ]
}
[/block]


10. Your **Webex Meeting** window displays a **Live Connected** status in the upper right window and the Rev Webcast begins streaming your meeting.

11. An email with the Webcast details is sent to the creator of the new event.

12. You may stop the stream to the Webcast at any time by clicking **Meeting **> **Stop Streaming** in Webex.

> 🚧 Important!
> 
> Once started, the event becomes an _existing_ event. If you **stop **streaming and start again, you connect to an **existing event** from the Rev menu options. Do _not_ attempt to start a **new event** again.
> 
> If the Webcast is successfully created but the Live stream does not start, the new event is _not_ deleted in Rev. You will need to modify or delete it from Rev first.

The following Rev Webcast **User Engagement** capabilities and **Video Source** settings default to their defined values when creating a new event from a Webex Meeting. 

These default settings can be modified through the **Rev UI/inline editing capabilities** once the Rev event starts.

| Function                  | Value       |
| :------------------------ | :---------- |
| Chat                      | Enabled     |
| Allow Anonymous Questions | Disabled    |
| Polls                     | Disabled    |
| Q&A                       | Disabled    |
| Closed Captions           | Disabled    |
| Auto Associate VODs       | Set to True |
| Redirect VODs             | Set to True |

## Troubleshooting

If you have any issues with your integration, make sure that you are always using the latest version installed.

### Update the Webex Meeting App

As of Rev v7.52, the **Webex Meeting** APIs were updated and the **Scope** permissions were updated to include transcription.  You must make sure that your Webex Meeting app is edited, [scoped correctly](doc:webex-meetings#webex-meeting-app-setup), and saved so that it is the latest version and includes the v7.52 updates.

### Allow Downloading without a Password

This integration requires that **AllowDownloadRecordingWithoutPwd** is enabled for your Webex site. Submit a ticket to the **Webex Provisioning Team** to enable this feature flag if you are having issues.