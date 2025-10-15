---
title: Browser, OS, and Device Compatibility
excerpt: >-
  This table details supported browsers, operating systems, and device
  compatibility in the Rev portal
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
[block:parameters]
{
  "data": {
    "h-0": "Device",
    "h-1": "OS",
    "h-2": "Browser",
    "0-0": "PC",
    "0-1": "Windows 11  \nWindows 10 Enterprise  \nWindows 10 Pro",
    "0-2": "Firefox 129+  \nChrome 127+¹  \nEdge 127+¹",
    "1-0": "Mac",
    "1-1": "macOS 13.0: Ventura  \nmacOS 14.0: Sonoma",
    "1-2": "Safari 17+  \nFirefox 129+  \nChrome 127+²  \nEdge 127+",
    "2-0": "iPhone, iPad",
    "2-1": "iOS 17.0+",
    "2-2": "Native Browser",
    "3-0": "Android",
    "3-1": "Android 13.0+",
    "3-2": "Chrome Only",
    "4-0": "Chromebook",
    "4-1": "Chrome OS",
    "4-2": "Chrome Only"
  },
  "cols": 3,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


<sup>1: Rev supports CHIPS/cookieless login in Google Chrome and Microsoft Edge as of v7.58. This means that Rev will continue to work seamlessly when embedded in other applications, without any login interruptions.</sup>

<sup>2 : The Mac Chrome browser video decoder displays some instabilities when playing HLS streams with identified data loss. This is a rare occurring issue that manifests as a “stall” or stopping of the playback. Disabling Chrome Hardware Acceleration fixes the issue. Disable this from Chrome by visiting the URL “chrome://settings”, then navigating to Advanced > System > “Use hardware acceleration when available” and toggling as necessary. This issue only effects Mac Chrome users and does not affect Windows users.</sup>