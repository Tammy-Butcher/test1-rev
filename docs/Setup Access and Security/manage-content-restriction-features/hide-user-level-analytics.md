---
title: Hide User Level Analytics
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
Some customers have strict personal data policies in place and do not want to display any user-level analytics at all, including to admin accounts. The ability to hide user-level analytics is available for those customers.

To hide user-level analytics:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **User Level Analytics** section and select the **Hide User-Level Analytics** checkbox. This checkbox hides all individual user-level analytics by disabling them.

<Image border={false} src="https://files.readme.io/9963624-hideUserLevelAnalytics.png" title="hideUserLevelAnalytics.png" />

This means that all user tables and CSV downloads across real-time analytics, post-event analytics, and video-on-demand analytics are no longer displayed, _including to Admin accounts_.

When enabled:

* The **Views** tab and **Views CSV** file export are no longer available under the **Reports** > [Videos](doc:videos-system-analytics) tab.
* The [Attendees tab](doc:attendees-in-real-time) is no longer displayed on the [Real-Time Dashboard](doc:real-time-webcast-analytics) during Live webcasts.
* Neither the [Attendees nor Vbrick Peer-to-Peer CSV](doc:webcast-reports) report downloads are available once a webcast has concluded.
