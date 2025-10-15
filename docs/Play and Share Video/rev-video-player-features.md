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

<PreferredRevSetting />

## Closed Captions, Subtitles, and Multiple Audio Tracks

Users can select [subtitles](doc:video-languages#auto-generate-a-new-subtitle-file), [closed captions](update-advanced-video-settings#enable-closed-captions) (if enabled), and [multiple audio tracks](doc:supported-video-and-audio-formats#multiple-audio-track-support) that are available for the video from the **Languages** icon. Note that the icon only displays the available options to choose from.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/33308798c19df3b175f8489c15839a8cee98b5e272268b63a3ba2fed4bca66b7-languageIconHighlighted.png",
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

## Recommended Videos

If your Rev portal has [Recommended Videos enabled](doc:allow-recommended-videos) by your Account Admin, a grid of recommended videos appears under the video you are currently viewing. These recommendations are based on the video you are currently viewing and videos you have watched in the past.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7cb9bc755129af32dd58b53ff8402c2c80aec16a680f57f1f4acb68ecf60df00-recommendedVideoEnabled.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


Recommended videos are specific to the account that is logged in; If you have not viewed any videos recently then the most popular videos of the last seven days based on portal views is displayed instead.