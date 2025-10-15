---
title: Add a Custom Device
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
Rev supports adding a Custom Device that you may configure as either a source or a destination (or both) in addition to using Vbrick’s Encoders and DMEs.

To add a Custom Device select **Add Custom Device** from the **Add a Device** dropdown and complete the required fields.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e0f9e42-addCustomDevice.png",
        "addCustomDevice.png",
        1202,
        586,
        "#f0f2f3"
      ],
      "caption": "Rev supports custom devices as video sources or viewing destinations through the Custom Device control"
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "0-0": "Name",
    "1-0": "Status",
    "2-0": "IP Address",
    "3-0": "Capabilities",
    "4-0": "Video Streams",
    "h-0": "Field",
    "h-1": "Description",
    "0-1": "This can be a name of your choosing. This is a required field. Descriptive location or Host name is recommended.",
    "1-1": "The status of your device may be set to **Active **or **Inactive **.",
    "2-1": "The **IP address** of where your device is located.  This is a required field.",
    "3-1": "At least *one *capability is required. You must designate that the device is either a **Video Stream Source** or a **Video Stream Viewing Destination** (or both). \n\nIf you designate the device as a **Video Stream Viewing Destination**, then **Video Streams** are required.",
    "4-1": "**Name**, **URL**, **Encoding Type**, and **Multicast **are all designated [through the **Add URL** button] and are required fields if the device is intended to be utilized as a viewing destination device. \n\nThese streams are later selected on **Presentation Profiles** as viewing destinations or can also be used for automatic multicast viewing."
  },
  "cols": 2,
  "rows": 5
}
[/block]
## HLS Stream Preparation for Automatic Multicast and Reflection

To optimize the use of **Custom Devices** features, the **HLS **stream should meet certain specifications.

Review DME Online Help on stream specifications in the [Rev Initiated Multicast and Reflection](https://portal.vbrick.com/help/dme/3240/index.html#page/AdminGuide/OutputConfiguration.10.12.html#) topic.