---
title: Configure a Rebuffering Threshold
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
The **Experienced Rebuffering Threshold** setting is used to configure a rebuffering threshold for Webcast events and is normally set by Vbrick. Please consult with Vbrick Support/Operations before modifying this value to avoid any adverse effects.

To set a rebuffering threshold:

* Set a value between 0 and 5000 in the **Experienced Rebuffering Threshold (milliseconds)** field.
* The default value is 500.

<Image title="experiencedRebuffering.png" alt={694} align="center" src="https://files.readme.io/3f345bf-experiencedRebuffering.png">
  This setting configures rebuffering thresholds for Webcast events and should not be reset without first consulting Vbrick first
</Image>

Keep in mind:

* Any buffering event that exceeds this threshold may be viewed on the Real Time Analytics Dashboard
* Buffering events that are less than the configured threshold are not counted
* It does not matter whether buffering happens at the start of playback or in the middle
