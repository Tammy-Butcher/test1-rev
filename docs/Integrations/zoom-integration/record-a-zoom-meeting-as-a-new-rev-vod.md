---
title: Record a Zoom Meeting as a New Rev VOD
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


Similar to **Video Conference** recording, Rev Cloud also supports recording Zoom meetings and ingesting them into your standard media workflow with the Zoom integration enabled. The recordings capture both active speakers and any content streams (if available). Vbrick’s player displays both streams and allows the user control of the layout.

To record a Zoom meeting:

1. Click the **Live Recording** tab > **Zoom Meeting** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d879f63-recordZoomMeeting.png",
        null,
        "Click the Recording tab and then select the Zoom Meeting option"
      ],
      "align": "center",
      "caption": "Click the Recording tab and then select the Zoom Meeting option"
    }
  ]
}
[/block]


2. Type in the **Zoom Meeting ID** or **Zoom Meeting URL**.

3. If the meeting is password protected, you must enter the **H323/SIP numeric password** for the meeting into the **Password ** field.

4. Configure the [DTMF](doc:dtmf-configuration-and-usage#use-dtmf-codes-in-video-recording) codes you want to use with the recording if any. (optional)

5. Click the **Start Recording** button. If a valid Zoom Meeting is used, Rev connects and begins recording.

6. When the **Stop **button is pushed, Rev uploads the video to Rev and disconnects.  You can then modify and control the [Video Settings](doc:updating-video-settings) and metadata in Rev as you normally would.