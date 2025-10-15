---
title: Embed a Video
excerpt: How to embed a Rev video on 3rd-party Websites or portals
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


The embed feature in Rev provides the code necessary to place the video player on 3rd-party Websites or portals. This means that your viewers are not required to use the Rev portal to view your videos.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8fe1a61-shareIcon.png",
        null,
        "Click the Sharing icon to access the flyout panel"
      ],
      "align": "center",
      "caption": "Click the Sharing icon to access the flyout panel"
    }
  ]
}
[/block]


When you embed a video:

- It must be in [Active](doc:update-basic-video-settings#video-status) status
- Its [Access Level](doc:update-basic-video-settings#video-access-control) must be set to **Public **(it may be viewed anonymously).  Otherwise, if Access Control is set to **Private**, viewers are required to log-in to Rev before viewing embedded videos.
- Your Account Admin must [enable this feature](doc:allow-embeds) before it is available

> 🚧 Important!
> 
> Both Safari and Chrome **Incognito **mode block 3rd-party cookies by default, which causes issues with some embedding features. For all functions to work as expected, it is _highly_ recommended that 3rd-party cookies be enabled.
> 
> Safari also requires that **Prevent cross-site tracking** is unchecked (under **Privacy** settings) before embedding functions correctly.

To embed a video:

1. Navigate to the video and access the [Sharing](doc:rev-video-player-features#video-sharing) flyout panel.

2. Click the **Embed** tab for embedding options.  The [Link](doc:share-a-video) tab is used for sharing video URLs via copying, emailing, and Webex Teams. 

3. The embed code displays along with a preview of your embed.  Embedding options are displayed below the code and can be modified as needed, including any custom embed options such as styling and playback controls.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b879bd-embedTabSelected.png",
        "videoEmbedPreview.png",
        1847
      ],
      "align": "center",
      "caption": "Click the Embed tab from the Sharing flyout panel to access embed coding options"
    }
  ]
}
[/block]


4. Click the **Copy** text to copy the embed code to the clipboard. Note that not all browsers support this function. The text will not be present if your browser does not support clipboard copy.
5. If you want the video to play from the beginning, leave the **Start at:** field _unchanged_. Otherwise, specify where on the timeline you want to start playing the video when embedded. To select a different time, select a different time on the timeline or manually enter the new time.

> 📘 Note
> 
> Rev supports CHIPS/cookieless login in Google Chrome and Microsoft Edge as of v7.58. This means that Rev will continue to work seamlessly when embedded in other applications, without any login interruptions.

## Custom Embed Options

Toggling and modifying custom embed options updates the embed code URL.  Click the **Reset** link to return the options to the default values at any time.

### Layout

Choose how you want to embed the video and select its sizing options.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ccde693-embedLayout.png",
        "embedLayout.png",
        383
      ],
      "align": "center",
      "caption": "Embed layout options specify how the embed generates and at what size"
    }
  ]
}
[/block]


**Pop-out player** - This is toggled off by default.

- **Off**: Generates an iFrame containing the video that can be added to a Website page
- **On**: Generates a thumbnail image of the video that can be added to a Website page (when clicked, opens the video in a new page)

| Size             | Width  | Height                                                 |
| :--------------- | :----- | :----------------------------------------------------- |
| Small            | 560    | 315                                                    |
| Medium (default) | 640    | 360                                                    |
| Large            | 853    | 480                                                    |
| Responsive       |        |                                                        |
| Custom           | custom | Calculate height for 16:9 ratio - divide width by 1.78 |

> 👍 Tip
> 
> If you want to embed a video on a mobile Web page or need the video player to work on responsive Web pages, select the **Responsive **option. 
> 
> Please note that the minimum supported size for a video embed is 375px x 210px and a full webcast is 375px x 375px, but larger viewports are recommended whenever possible.

```html
<div style="position: relative; height: 0; padding-bottom: 56.25%;">
<iframe allowfullscreen="" frameborder="0" height="100%" src="&lt;playback URL&gt;" style="position: absolute; left: 0px; top: 0px;" width="100%"></iframe>
</div>
```

### Tabs

Click the **Show Tabs** toggle if you want to embed the same user engagement and AI features that are displayed on the Rev video player.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/243e0cc-enableTabs.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


Each tab that is enabled displays on the embedded video under the play bar functions.  Note that if a feature requires authentication (such as comments, playlists, and so forth) it will only display if logged in.

### Styling

Use the **Styling** section to specify how the embedded player appears. All toggles are off by default.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b5ae315-embedStyling.png",
        "embedStyling.png",
        411
      ],
      "align": "center",
      "caption": "Use styling to apply custom styles and colors to the embedded player"
    }
  ]
}
[/block]


- **Player accent color**: By default, this field is populated by the branding accent color used in the portal. Enter a new hexadecimal color or use the color picker wheel to use a custom accent color for the embedded video player.

### Controls

Specify which controls you want to appear on the embedded player.  All controls are on by default.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d74114-embedControls.png",
        "embedControls.png",
        473
      ],
      "align": "center",
      "caption": "Toggle the All controls switch to specify that all available controls are visible on the player"
    }
  ]
}
[/block]


- **All controls**:  Toggles all controls on or off
- **Center buttons**: Hides main play button, skip forward, skip back
- **Play bar**: Play and pause buttons, scrubber, timestamp, skip forward, skip back
- **Closed captions**: Closed caption control
- **Settings**: Toggles the settings icon on the player that contains playback source, playback speed, and keyboard shortcut control(s)
- **Fullscreen**:  Permits full screen option
- **Layouts**: (not pictured) Only displays if video is a dual player or contains chapters

### Playback

Specify playback options available on the embedded video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29a216a-embedPlayback.png",
        "embedPlayback.png",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


- **Loop**:  Loops playback.  Not displayed for Live video.
- **Autoplay**: Toggle if you want the video to autoplay when accessed. 

> 🚧 Important!
> 
> If your videos and playlists are set to autoplay, be aware that they play unmuted when possible. If not possible, they play muted. This also applies to Webcasts.

- **Hide chapters**: Toggle if you want video chapters to be hidden (Only displayed if the video contains chapters).
- **Force closed captions**: Only displayed if closed captions are available

> 📘 Note
> 
> For VCI embeds, only switched stream playback is supported. Dual stream playback is not supported.