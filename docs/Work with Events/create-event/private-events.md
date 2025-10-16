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
When you want _only_ invited attendees to have access to your webcast, set the **Listing Type** to **Private** in the [Attendees](doc:attendees) section. You can then specify which licensed Rev users or groups have access to view and attend in the **Find Items** box control.

<Image alt={700} border={false} caption="A private event only allows those users and groups you specify in the Find Items control to attend" title="privateEventType.png" src="https://files.readme.io/d21ddbf-privateEventType.png" />

When a webcast is private:

* It does not appear in the **Upcoming Events** carousel on the user's [Home Page](doc:the-rev-home-page) unless the user (or a group the user belongs to) is invited
* It does not appear in the [Event Calendar](doc:the-event-calendar) unless the user (or a group the user belongs to) is invited
* Access should be granted to groups or individuals when scheduling the event and _before_ they try to access the event. Otherwise, the invited attendees are not able to access the event. In other words, you may distribute the event invitation and then go back and add additional attendees; however, you will then need to grant access _before_ the event begins and before they try to access the event. Otherwise, the new invited attendees are not be able to attend.
* Event and Account Admins are _always_ able to see, edit, and join private events through the calendar and carousel
* If a user has been granted access to a private event through a group and is subsequently removed from that group, the event no longer appears on the user’s **Event Calendar** and the user is not be able to access the event
