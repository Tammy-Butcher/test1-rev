---
title: Hosts and Moderators
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


## Choose an Event Host

Every webcast must have a designated **Event Host** to start and run it even if the [Listing Type](doc:create-event#understanding-event-listing-types) is **Private **or **Public**.  There may be up to three hosts assigned per webcast. An Event Host is typically selected during event set up and the event creator is the default host assigned.

> 🚧 Important!
> 
> The **Event Host** role may _only_ control those events they are **assigned** to whereas Account Admin roles can control all events as needed. **Event Admin** roles can edit webcast settings but cannot start/stop the webcast.
> 
> The **Event Host** role may _only_ **edit **those events they **create **whereas Account/Event Admin roles can edit all events as needed.
> 
> This is an important distinction to keep in mind.
> 
> **Event Moderator** [tasks and permissions](doc:roles-and-permissions#section-events) are different from those of an Event Host and they may only control event features such as polls and chat but do not control the event itself.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/72d505d-eventHost.png",
        "eventHost.png",
        802
      ],
      "align": "center",
      "caption": "Event Hosts who create an event can edit it or delete it; Event Hosts assigned to an event can control it."
    }
  ]
}
[/block]


- Note that only accounts with the Event Admin, Event Host, or Account Admin [roles](doc:roles-and-permissions#section-events) appear in the **Event Host Find Items...** control and can be added as Event Hosts for an event
- All Event Hosts assigned are able to control the webcast slides if an Event Moderator has not been assigned (they may only edit the events they create)
- If the Event Host that creates the event is unable to reach the webcast, additional hosts or admins assigned may control the webcast
- If no Event Host or admin is able to reach the webcast, it is automatically ended on its own after 60 minutes of its scheduled end time

> ❗️ Warning!
> 
> The Event Host added **first **is the “owner” of the event (and appears **last ** as a result in the host list if more than one is added).
> 
> In the example below, the Event Host “Tammy Butcher” is the actual owner of the event. Be aware of this if you add more than one host to your webcast and add the person you want to “own” the event first.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/80674b8-hostOwner.png",
        "hostOwner.png",
        802
      ],
      "align": "center",
      "caption": "The Event Host added first in Find Items is the “owner” of the event and appears last in the list; Tammy is this event's owner."
    }
  ]
}
[/block]


## Choose Event Moderator(s)

**Event Moderators** are used to manage and control the “behind the scene” event features that have been set up by an Event Admin or Event Host such as [polls](doc:managing-webcast-polls) and [Q&A](doc:qa-module-management) sessions. This allows the Event Host(s) to focus on controlling the webcast itself.

For example, you may have an webcast where a large panel of speakers are presenting and several hundreds of attendees are expected. This type of event would expect to draw several questions at once during a Q&A session. A moderation team to manage the question queues and polls for the speakers would be the ideal set up in this case.

It is important to note that moderators are not able to modify or control the event \_configuration \_itself.

> 👍 Tip
> 
> Unlike the Event Host, any user may be added as an Event Moderator. You do not have to be any certain functional role in Rev to be assigned as a moderator.
> 
> Several Event Moderators may be assigned to an event while only 3 Event Hosts may be assigned at a time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b883c45-eventModerators.png",
        "eventModerators.png",
        722
      ],
      "align": "center",
      "caption": "When adding moderators, you can also designate those people who can control slides for you"
    }
  ]
}
[/block]


- Designate a moderator to control the presentation slides (instead of the Event Host) by clicking the **Control Slides** tab. Only \_one \_moderator at a time may control the slides. 
- The Control Slides button is only be visible after the moderator has been added by clicking the **Done **button first and saving the moderator to the event's configuration.

## Event Host Versus Event Moderator Tasks

[block:parameters]
{
  "data": {
    "h-0": "Event Host (Three per webcast)",
    "h-1": "Event Moderator (Unlimited)",
    "0-0": "Event Hosts are able to perform **all ** the tasks of an Event Moderator  \n  \nThey can also:  \n  \n- Create an event  \n- Edit an event (if they create it)  \n- Delete an event (if they create it)  \n- Start an event  \n- Stop an event  \n- Pause an event  \n- Broadcast an event  \n- Record an event  \n- View/remove attendees  \n- All Account Admins are able to access/control webcast functions  \n- All Event Admins are to edit webcast settings but they cannot start/stop the webcast",
    "0-1": "Event Moderators **cannot ** perform the tasks of an Event Host.  \n  \nThey can:  \n  \n- View/remove attendees  \n- View and manage the poll interface during webcast  \n- View and manage the Q&A interface during webcast  \n- View the event invitation text during webcast  \n- Download the chat report after webcast  \n- Download the Q&A report after webcast  \n- Access the webcast dashboard  \n- Toggle the webcast layout  \n- Control the presentation (if designated, only one moderator at a time)"
  },
  "cols": 2,
  "rows": 1,
  "align": [
    "left",
    "left"
  ]
}
[/block]