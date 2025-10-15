---
title: Embed a Webcast
excerpt: How to embed a Rev webcast on 3rd-party Websites or portals
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The embed feature in Rev provides the code necessary to place the webcast video player on a 3rd-party Websites or portals. How the webcast functions depends on its **Listing Type**.

When you embed a webcast:

- Its [Listing Type](doc:create-event#understanding-event-listing-types) can be set to **Public**, **All Users**, or **Private**
- When set to **Private** or **All Users**, attendees must log-in to Rev before viewing the webcast even if the webcast is embedded on a 3rd-party portal
- When set to **Public**, a form displays on the embedded Webcast where attendees can either log-in, register, or choose to attend as a Guest and the event functions as a Rev [Public webcast](doc:create-event#schedule-a-public-event). Any [Event Branding](doc:event-branding) that is configured remains in place.
- Your Account Admin must [enable embedding](doc:enable-or-disable-features#allow-embeds) before this tab (and ability) is available

> 🚧 Important!
>
> Both Safari and Chrome **Incognito** mode block 3rd-party cookies by default, which causes issues with some embedding features. For all functions to work as expected, it is _highly_ recommended that 3rd-party cookies be enabled.

To embed a webcast:

1. Create and/or navigate to the webcast you want to embed. Once the webcast is saved, the **Embed** tab is available (if enabled).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74f5008-embedTab.png",
        "embedTab.png",
        1202
      ],
      "align": "center",
      "caption": "If embedding is enabled, use the Embed tab to access the embed code snippet to embed your Rev webcasts"
    }
  ]
}
[/block]

2. Click the **Embed** tab for embedding options.

3. The embed code for the webcast displays. Click the **Options** button to modify embed settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a54157-embedWebcast.png",
        "embedWebcast.png",
        666
      ],
      "align": "center",
      "caption": "Select the size you want and then click the Copy button to copy the embed code"
    }
  ]
}
[/block]

4. The **Copy** button copies the code you set for embedding. Medium size is the default option.

| Size       | Width  | Height                                                 |
| :--------- | :----- | :----------------------------------------------------- |
| Small      | 560    | 315                                                    |
| Medium     | 640    | 360                                                    |
| Large      | 853    | 480                                                    |
| Responsive |        |                                                        |
| Custom     | custom | Calculate height for 16:9 ratio - divide width by 1.78 |

If you want to embed a webcast on a mobile Web page or need the video player to work on responsive Web pages, select the **Responsive** option.

When this option is selected, the embed code changes to the code below and the height/width boxes are hidden.

```html
<div style={{ position: "relative", height: "0", paddingBottom: "56.25%" }}>
  <iframe allowfullscreen="" frameborder="0" height="100%" src="<playback URL>" style={{ position: "absolute", left: "0px", top: "0px" }} width="100%"></iframe>
</div>
```

> 📘 Note
>
> Rev supports CHIPS/cookieless login in Google Chrome and Microsoft Edge as of v7.58. This means that Rev will continue to work seamlessly when embedded in other applications, without any login interruptions.