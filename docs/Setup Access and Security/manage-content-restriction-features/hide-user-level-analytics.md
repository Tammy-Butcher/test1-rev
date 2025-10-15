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
[block:html]
{
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>&#128187; <a href=\"/docs/vbrick-distribution\">Vbrick Distribution</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


Some customers have strict personal data policies in place and do not want to display any user-level analytics at all, including to admin accounts. The ability to hide user-level analytics is available for those customers. 

To hide user level analytics:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **User Level Analytics** section and select the **Hide User-Level Analytics** checkbox. This checkbox hides all individual user-level analytics by disabling them.

![](https://files.readme.io/9963624-hideUserLevelAnalytics.png "hideUserLevelAnalytics.png")

This means that all user tables and CSV downloads across real-time analytics, post-event analytics, and video-on-demand analytics are no longer displayed, _including to Admin accounts_.

When enabled:

- The **Views** tab and **Views CSV** file export are no longer available under the **Reports** > [Videos](doc:videos-system-analytics) tab.
- The [Attendees tab](doc:attendees-in-real-time) is no longer displayed on the [Real-Time Dashboard](doc:real-time-webcast-analytics) during Live webcasts.
- Neither the [Attendees nor Vbrick Peer-to-Peer CSV](doc:webcast-reports) report downloads are available once a webcast has concluded.