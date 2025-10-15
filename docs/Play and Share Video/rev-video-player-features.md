---
title: Rev Video Player Features
excerpt: How to use the Rev video player controls and flyout panel functions
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
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


There are several features on the Rev video player that may appear depending on what has been enabled or configured.  In addition to the player window, there are flyout panels that may be clicked  that contain additional information.

> 👍 Tip
> 
> The **accent color** specified in the [Branding](doc:fonts-colors-and-logo#reset-primary-and-accent-colors) section is also applied to the Rev Video Player.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a991cba-playerWindowFeatures.png",
        "playerWindowFeatures.png",
        1351
      ],
      "align": "center",
      "caption": "Some icons that appear on the player window depend on the Rev features that have been activated"
    }
  ]
}
[/block]


## Player Window Icons

[block:parameters]
{
  "data": {
    "h-0": "Setting",
    "h-1": "Description",
    "0-0": "1",
    "0-1": "The video [Status](doc:update-basic-video-settings#video-status) setting. Communicates information such as **Inactive **videos or videos that need approval if part of an **Approval Process**.",
    "1-0": "2",
    "1-1": "Depicts a video under [Legal Hold](doc:the-legal-hold-setting). This means it may not be viewed or edited through video settings.",
    "2-0": "3",
    "2-1": "Denotes that the video is [Unlisted](doc:update-advanced-video-settings#unlist-this-video) at the present time.",
    "3-0": "4",
    "3-1": "Indicates the video is a **360-video**.",
    "4-0": "5",
    "4-1": "**Plays **and **Pauses **the current video. Returns to last known timestamp for system users until the user has completed watching the video.  [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.",
    "5-0": "6",
    "5-1": "Skip **Back** and **Forward** ten seconds during video playback.  [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.",
    "6-0": "![](https://files.readme.io/0cbe13d-muteIcon.png)",
    "6-1": "Indicates that a video’s sound is muted. Also acts as a toggle to turn audio on and off. [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.  \n  \nNote that if videos or [playlists](doc:playlists) are set to autoplay, be aware that they play unmuted when possible. If not possible, they start muted. This also applies to Webcasts."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "left",
    "left"
  ]
}
[/block]


## Playback Bar Functions

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d6bf7aa-playbackBarIcons.png",
        "playbackBar.png",
        "The icons that appear on the playback bar are standard video player functions along with Rev specific features"
      ],
      "align": "center",
      "caption": "The icons that appear on the playback bar are standard video player functions along with Rev specific features"
    }
  ]
}
[/block]


| Function | Description                                                                                                                                                                                                                                                                                                                                                          |
| :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1        | **Play** / **Pause** toggle. [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.                                                                                                                                                                                                                                                                |
| 2        | Current playback head timestamp / total video length                                                                                                                                                                                                                                                                                                                 |
| 3        | Skip **Back** and **Forward** ten seconds. [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.                                                                                                                                                                                                                                                  |
| 4        | **Skip Chapter**; only visible when chapters are added in the [The Video Editor Interface](doc:the-video-editor-interface).  This icon skips to the beginning of the next chapter in the video.  If you are already playing the last chapter, it skips to the end of the video. [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.             |
| 5        | **Mute** and **volume** control. [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.                                                                                                                                                                                                                                                            |
| 6        | **Show Chapter Images**; only visible when chaptering (with image support) is present in the video. This is added in the [Video Editor](doc:edit-a-video-clip) when adding chapters . [Hotkey](doc:rev-video-player-features#player-hotkey-support)  supported.                                                                                                      |
| 7        | Toggle [audio tracks](doc:supported-video-and-audio-formats#multiple-audio-track-support), [subtitles](doc:video-languages) and [closed captions](doc:subtitles-translations-and-closed-captions) for the video (if available and enabled). [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.                                                 |
| 8        | View optional [transcoded video instances](doc:update-advanced-video-settings#view-transcoded-video-instances) (if configured) and variable playback speeds; Dependent upon browser support. MP4 and HLS videos may be played at 1.0x, 1.25x, 1.5x, and 2.0x in HTML5 players. To ensure proper playback, the player must receive an https link as the playback URL. |
| 9        | Full-screen control. [Hotkey](doc:rev-video-player-features#player-hotkey-support) supported.                                                                                                                                                                                                                                                                        |
|          | (not shown) [Webcast Layout Controls](doc:webcast-layout-controls)   for video-conferenced sourced videos that allow you to specify how slides versus video appear on your screen.                                                                                                                                                                                   |

> 👍 Tip
> 
> Hovering over the playback timeline with your mouse displays a thumbnail preview of what is occurring in that location of the video.

## Closed Captions, Subtitles, and Multiple Audio Tracks

Users can select [subtitles](doc:video-languages#auto-generate-a-new-subtitle-file), [closed captions](update-advanced-video-settings#enable-closed-captions) (if enabled), and [multiple audio tracks](doc:supported-video-and-audio-formats#multiple-audio-track-support) that are available for the video from the **Languages** icon. Note that the icon only displays the available options to choose from.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f25b12d-languageIcon.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


## 360-Degree Playback

Two additional playback features are present if you have uploaded a 360-degree video. Note that 360-degree video is not supported on mobile devices at this time.

[block:parameters]
{
  "data": {
    "h-0": "Function",
    "h-1": "Description",
    "0-0": "![](https://files.readme.io/3a7b9ae-360Icon.png)",
    "0-1": "**360-degree directional control**: Rev supports 3 different methods to pan your 360-degree video [uploads](doc:upload-video):  \n  \n- Click and hold the arrow on the directional control to pan the video in that direction.\n- You may also use the arrow keys on your keyboard.\n- Finally, you can click and drag on the video itself to pan in a specific direction.",
    "1-0": "![](https://files.readme.io/3391899-reset360.png)",
    "1-1": "**Reset control**: Clicking Reset returns the video to its original perspective. This is the perspective seen when the video begins playback. Reset is displayed on the directional control once you begin panning the video."
  },
  "cols": 2,
  "rows": 2,
  "align": [
    "left",
    "left"
  ]
}
[/block]


## Player Hotkey Support

The Rev video player allows you to control the video player using only your keyboard.

[block:parameters]
{
  "data": {
    "h-0": "Button / Function",
    "h-1": "Key",
    "0-0": "Play / Pause (Toggle)",
    "0-1": "Space  \nEnter  \nK",
    "1-0": "Back (Skip Back 10 seconds)",
    "1-1": "Left arrow  \nJ",
    "2-0": "Forward (Skip forward 10 seconds)",
    "2-1": "Right arrow  \nL",
    "3-0": "Skip Chapter",
    "3-1": "Alt + right arrow (forward)  \nAlt + left arrow (back)",
    "4-0": "Mute / Unmute (toggle)",
    "4-1": "M",
    "5-0": "Volume",
    "5-1": "Up/down arrow",
    "6-0": "Show Chapter Images",
    "6-1": "I",
    "7-0": "Closed Captions Menu",
    "7-1": "C",
    "8-0": "Settings Menu",
    "8-1": "S  \n  \n**Note:** Settings menu displays all keyboard shortcuts",
    "9-0": "Full Screen",
    "9-1": "F  \nesc (when in full screen to escape out of full screen)",
    "10-0": "Dual Stream Menu",
    "10-1": "D"
  },
  "cols": 2,
  "rows": 11,
  "align": [
    "left",
    "left"
  ]
}
[/block]


## Tab Navigation Support

The Rev video player supports tabbed navigation based on the Tab order below (if the control is displayed).  Note that to reverse navigate the order, use `Shift+Tab`.  Player hot key support for specific controls is observed in the table above. View the [Accessibility Features](doc:accessibility-features) topic for more details.

- Large Skip Back
- Large Play/ Pause
- Large Skip Forward
- Small Play/Pause
- Small Skip Back
- Small Skip Forward
- Mute/Unmute 
- Volume
- Layout
- CC
- Settings
- Full Screen

## Video Player Flyout Panels

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fd4262a-flyoutPanelIcons.png",
        null,
        "The video player flyout icons access the various flyout panels and metadata about each video"
      ],
      "align": "center",
      "caption": "The video player flyout icons access the various flyout panels and metadata about each video"
    }
  ]
}
[/block]


To the right of the video player window are Rev’s flyout panel icons.  Clicking an icon opens its associated panel with specific functions and metadata for that video.  What appears in each panel depends on what has been configured or enabled in Rev.

> 👍 Tip
> 
> Some icons may or may not appear depending on what features have been enabled for your portal.

### Video Basic Information

The **Video Basic Information** flyout contains various metadata about the video along with various video settings that may have been enabled.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37473d2-videoBasicInfoPanel.png",
        "videoBasicInfoPanel.png",
        "The various video settings and metadata that have been configured appear on this panel\n\n"
      ],
      "align": "center",
      "sizing": "smart",
      "caption": "The various video settings and metadata that have been configured appear on this panel"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Setting",
    "h-1": "Description",
    "0-0": "Title",
    "0-1": "The video [title](doc:update-basic-video-settings#title-and-description) that is given in video settings",
    "1-0": "![](https://files.readme.io/aa66650-downloadVideo.png) ",
    "1-1": "[Download](doc:update-basic-video-settings#enable-comments-ratings-and-downloading) the video (if enabled).  Not visible if this feature has not been enabled for the video.",
    "2-0": "Description",
    "2-1": "The [description](doc:update-basic-video-settings#title-and-description) that is entered in video settings.",
    "3-0": "Total Views",
    "3-1": "Total number of views (including **Last Viewed** date and time based on user’s timezone)",
    "4-0": "Owner",
    "4-1": "The [video owner](doc:update-basic-video-settings#video-owner).  This is the uploader by default but a video owner can also be assigned that is not the original uploader.",
    "5-0": "Upload Date",
    "5-1": "The date and time that the video was [uploaded](doc:upload-video).",
    "6-0": "In This Video",
    "6-1": "Users that are [tagged](doc:update-basic-video-settings#tag-users-in-a-video) in a video.  \n  \nTimeline tagging that highlights on the timeline where in the video speakers are present is available _only_ if [Facial Recognition](doc:facial-recognition) is enabled (disabled by default).  \n  \n- Profile pictures that have tagging enabled are indicated by an arrow > next to their image. If enabled, click the profile picture to highlight the range the speaker appears on the timeline.\n\n- Users may opt-out of [tagging](doc:update-basic-video-settings#tag-users-in-a-video) any time by updating their [Profile Settings](doc:your-rev-profile#update-your-profile-image).",
    "7-0": "Categories",
    "7-1": "[Categories](doc:update-basic-video-settings#categories-and-tags) the video belongs to; clicking a category will take you to the Category archive page and display all videos that belong to that specific category.",
    "8-0": "Tags",
    "8-1": "[Tags](doc:update-basic-video-settings#categories-and-tags) the video has been assigned; clicking a tag will take you to a search results page and display all videos that have been tagged with that specific tag.",
    "9-0": "Custom Fields",
    "9-1": "[Custom fields](doc:update-basic-video-settings#use-a-custom-field), if defined, appear beneath the Tags field.",
    "10-0": "Rating",
    "10-1": "[Rate](doc:update-basic-video-settings#enable-comments-ratings-and-downloading) the video from 1 to 5 stars and view ratings that have already been applied.  \n  \nThe **Rating **indicates the \"average rating received\" while the the **Total Ratings** is the \"total number of ratings\" received on the video to date.",
    "11-0": "Supplemental Files",
    "11-1": "If [supplemental files](doc:update-advanced-video-settings#attach-a-supplemental-file) are attached to the video they are downloaded from this panel.",
    "12-0": "Inappropriate Content",
    "12-1": "Flag or report video for inappropriate content.  \n  \nClick the **Report **icon to flag the video for inappropriate content.  Account and Media Admins will receive a notification in Rev and an email so that the video may be reviewed.",
    "13-0": "Password Protected Notification",
    "13-1": "If the video is a [Public](doc:create-event#schedule-a-public-event) video and **Password **protected, it is noted on this panel.",
    "14-0": "Approval Process Stage",
    "14-1": "Present if the video is part of an [Approval Process](doc:define-an-approval-process)"
  },
  "cols": 2,
  "rows": 15,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Video Comments

Use the **Video Comments** flyout panel to enter a comment on a video and view/sort all previously entered comments.  If a comment is replied to, the commenter is notified in the [Notifications](doc:notifications) tray. 

Only Account and Media Admin account(s) can delete all user comments in addition to their own comments.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/38facca-commentsFlyout.png",
        "commentsFlyout.png",
        401
      ],
      "align": "center",
      "caption": "Use the Comments flyout to enter rich text comments (including emojis) on VODs"
    }
  ]
}
[/block]


### Video Sharing

Use the **Video Sharing** flyout panel to access [sharing](doc:share-a-video) and [embedding](doc:embed-a-video) options that may be enabled for a video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f522f9b-sharingFlyout.png",
        "sharingFlyout.png",
        372
      ],
      "align": "center",
      "caption": "The Sharing flyout panel is used to both share and obtain embed code for Rev videos"
    }
  ]
}
[/block]


### Video Pulse

The **Video Pulse** flyout displays speakers that are tagged [In This Video](doc:update-basic-video-settings#tag-users-in-a-video). When combined with the Rev IQ module’s [Facial Recognition](doc:facial-recognition) capabilities, it also highlights each speaker interactively (during playback) as they appear in real-time along with audio transcript highlighting and on the timeline if their profile image is clicked. Profile pictures that have tagging enabled are indicated by an arrow > next to their image.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44a2c64-videoPulseFlyoutPanel.png",
        "videoPulseFlyoutPanel.png",
        537
      ],
      "align": "center",
      "caption": "The Video Pulse Flyout highlights each tagged speaker as they appear in the video along with their audio when used with Rev's Facial Recognition license"
    }
  ]
}
[/block]


This interactivity requires an [SRT transcript file uploaded](doc:update-advanced-video-settings#subtitles-translations-and-closed-captions) (for audio transcripts) and a Rev IQ license purchased (for timeline tagging).

The **Video Pulse** flyout also features the ability to **Search **videos for text in [audio transcripts](doc:search-and-filter-functions#speech-search-results) (SRT files) and any tagged users.

<h4> Quick Edit or Delete a Subtitle in the Pulse Flyout </h4>

User accounts that have video edit rights are able to quickly correct transcripts directly in the **Video Pulse** flyout by clicking the **Edit **icon that appears next to a transcript line.  When clicked, the text of the subtitle may be edited or deleted as needed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/204d89c-videoPulseEdits.png",
        "videoPulseEdits.png",
        502
      ],
      "align": "center",
      "caption": "Click the Edit (pencil) icon next to a subtitle that you want to edit.  Be sure you click the Save icon to save any changes you make."
    }
  ]
}
[/block]


To edit or delete a transcript in the Video Pulse flyout:

1. Click the **Pulse **icon in the video player.

2. Click the **Edit **icon next to the subtitle you want to correct.  If the icon does not appear when hovering next to the subtitle, you do not have edit rights.

3. **Edit **the subtitle text as needed.  Note that you can also edit the time field if needed.

4. Click the **Delete **icon to remove the text.  This may not be undone so use caution.

> 👍 Tip
> 
> You can only have one line open in edit mode at a time.

5. Click the **Save **icon to save your changes.  When you save the subtitle edits, the version of the file in search is also updated.

### Generative AI Video Assistant

The **Video Assistant** flyout panel allows you to interact with a video's transcript using a Generative AI chat interface to ask questions about a video through a series of prompts. This allows you to receive a quick overview and insights about its content.  

Keep in mind that certain requirements must be met when using this feature. The video must have an [English transcript](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings), you must have the Rev IQ [Video Assistant](doc:vbrick-assistant) enabled, and you must have [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4bf2bc-videoAssistantFlyout.png",
        "",
        "The Video Assistant flyout allows you to interact with an AI chatbot and ask questions about a video"
      ],
      "align": "center",
      "caption": "The Video Assistant flyout allows you to interact with an AI chatbot and ask questions about a video."
    }
  ]
}
[/block]


> 🚧 Important!
> 
> The **Vbrick Assistant** and **Transcript Summarization** features are only available on US-based portals at this time and require **English** transcripts to function. Please contact [Vbrick Support](mailto:support@vbrick.com) if you need assistance.

### Video Playlists

The [Playlists](doc:playlists) flyout panel provides the ability to create, edit, and manage playlists.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb2e5bf-playlistFlyout.png",
        "playlistFlyout.png",
        537
      ],
      "align": "center",
      "caption": "Access and manage playlists on the Playlist flyout panel"
    }
  ]
}
[/block]


### Video Chapters

<br />

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1124b8-chapterIcon.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


The **Chapters **flyout allows you to view and navigate between a video's chapters. It is only present in those videos that have chapters defined in the [video editor](doc:edit-a-video-clip).  When you click the **Chapter** icon, the flyout appears and allows you to navigate to the chapters that have been defined.  Think of chapters as bookmarks that allow a user to quickly navigate to content that is specifically relevant or of interest to them.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e23d8a-chapterUIInterface.png",
        "",
        "If chaptering is added, navigate to a chapter either through the Chapter flyout or through the Chapter dropdown"
      ],
      "align": "center",
      "caption": "If chaptering is added, navigate to a chapter either through the Chapter flyout or through the Chapter overlay in the video window"
    }
  ]
}
[/block]


In addition to the Chapter flyout, you can also use the **Chapter overlay** in the player window to select a chapter to jump to or the **Chapter skip** icon in the playback bar to skip forward and back between chapters.  

If images have been added to the chapter, you can toggle them on and off using the **Show Chapter Images** icon on the video playback bar. This icon is not present if no images have been added to the chapter.

### Video Reports

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50e2841-videoReports.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


The **Reports **flyout displays the [Video Analytics Dashboard](doc:video-analytics-dashboard) that provides detailed analytics and reports for the video.  It is only visible to Account and Media Admins.