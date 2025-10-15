---
title: Private Events
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
When you want *only *invited attendees to have access to your webcast, set the **Listing Type** to **Private** in the [Attendees](doc:attendees) section. You can then specify which licensed Rev users or groups have access to view and attend in the **Find Items** box control.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d21ddbf-privateEventType.png",
        "privateEventType.png",
        700,
        500,
        "#fafbfb"
      ],
      "caption": "A private event only allows those users and groups you specify in the Find Items control to attend"
    }
  ]
}
[/block]
When a webcast is private:

* It does not appear in the **Upcoming Events** carousel on the user's [Home Page](doc:the-rev-home-page) unless the user (or a group the user belongs to) is invited
* It does not appear in the [Event Calendar](doc:the-event-calendar) unless the user (or a group the user belongs to) is invited
* Access should be granted to groups or individuals when scheduling the event and *before *they try to access the event. Otherwise, the invited attendees are not able to access the event. In other words, you may distribute the event invitation and then go back and add additional attendees; however, you will then need to grant access *before *the event begins and before they try to access the event. Otherwise, the new invited attendees are not be able to attend.
* Event and Account Admins are *always *able to see, edit, and join private events through the calendar and carousel
* If a user has been granted access to a private event through a group and is subsequently removed from that group, the event no longer appears on the user’s **Event Calendar** and the user is not be able to access the event