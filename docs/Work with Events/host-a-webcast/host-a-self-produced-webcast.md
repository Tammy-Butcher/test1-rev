---
title: Present a Webcam and Screenshare Event
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
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]



There are two methods for hosting a **Webcam and Screenshare** event; You can [schedule it](doc:video-sources#webcam-and-screenshare-events) and then host it as you normally would or you can use the [Go Live](doc:host-a-self-produced-webcast#use-the-go-live-button) button and host an event "on-the-fly" with no scheduling involved.  Both are discussed in this topic.

> 👍 Tip
> 
> It is very important that you test this feature within your environment.  There are differences in browsers and internet connections that can impact the quality.  As always, please verify the quality and flow before using within event.  Please review the [Rev Screen Share and Webcam Best Practices](doc:rev-screen-share-and-webcam-best-practices).

## Host a Scheduled Webcam and Screenshare Event

When you schedule a [Webcam and Screenshare](doc:webcam-and-screenshare-events) event, many of the same controls you use when you [Host a Production Webcast](doc:host-a-production-webcast) for managing attendees and invites are still used. 

In addition to that, hosting the event itself is also similar.  Hosts should be aware of the [configuration settings](doc:webcam-and-screenshare-events#configuration-settings) for hosting a self-produced event.

You will need to click the **Start Webcast** button manually (if automated settings are not enabled) just as you would any other event from the [Webcast Settings Dashboard](doc:webcast-settings-dashboard).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e2681b3-startWebcast.png",
        "startWebcast.png",
        1841
      ],
      "align": "center",
      "caption": "If automated settings are disabled, start the event manually from the Webcast Settings Dashboard by clicking the Start Webcast button"
    }
  ]
}
[/block]

### Start the Event

When you start the event, you are presented with final hosting preparation details.  You are able to finalize what you want to begin sharing as far as screen, camera, and microphone options using [Rev Sharing Control Options](doc:rev-sharing-control-options).

> 👍 Tip
> 
> You are not broadcasting or recording the webcast at this point.  This is indicated by the messaging at the top of the event.  You will need to click the **Broadcast** button and **Ready** toggle switch to begin once you have finalized your preparations.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1887b5-broadcastSetup.png",
        "broadcastSetup.png",
        1204
      ],
      "align": "center",
      "caption": "The webcast begins by prompting you to begin sharing either your screen, your camera or your audio"
    }
  ]
}
[/block]

Once you share your camera and microphone, you are ready to broadcast and record the event if you are satisfied with how it appears.

### Broadcast and Record the Event

Once you have selected all sharing options, you may now choose to record and/or broadcast the event to attendee.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8f727b0-selfProducedEventWindow.png",
        "selfProducedEventWindow.png",
        1204
      ],
      "align": "center",
      "caption": "Use the media control buttons to make adjustments or to stop sharing altogether at any time"
    }
  ]
}
[/block]

Notice that, initially, attendees can still not view the event.  This is noted by the messaging at the top of the webcast.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0423b92-noBroadcast.png",
        "noBroadcast.png",
        947
      ],
      "align": "center",
      "caption": "The webcast does not begin broadcasting to attendees until you click the Broadcast button"
    }
  ]
}
[/block]

If you want to **Record** your webcast, you must toggle the **Not Ready** switch to **Ready**.  Messaging will switch to **Ready to Record**.  You may then click the **Broadcast** button to begin broadcasting your event to attendees.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/347c971-webcastReadyMessaging.png",
        "webcastReadyMessaging.png",
        1396
      ],
      "align": "center",
      "caption": "To record, toggle to Ready, and then click Broadcast to begin broadcasting to attendees"
    }
  ]
}
[/block]

Keep in mind that you may change your screen share at any time, stop sharing, and stop your camera and microphone as well.

When you are ready to end your event, click the **End Event** button as you normally would.

## Use the Go Live Button

An alternative to scheduling a live webcast is to use the **Go Live** button to begin broadcasting to an audience immediately.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f32e71b-goLiveButton.png",
        "goLiveButton.png",
        549
      ],
      "align": "center",
      "caption": "Use the Go Live button to begin broadcasting to an audience immediately"
    }
  ]
}
[/block]

When you click **Go Live**, the following fields/functions are available:

[block:parameters]
{
  "data": {
    "h-0": "Field/Function",
    "h-1": "Description",
    "0-0": "Title",
    "0-1": "The webcast **Title**.  This default's to the Presenter and the date and time they are Live.",
    "1-0": "Estimated Duration",
    "1-1": "How long you plan to present or \"be live\".  \n  \nThe default time is 1 hour.  Should you need less time than this, you may end your live stream early.",
    "2-0": "Audience",
    "2-1": "Who has permissions to view your live event; Similar to all Rev events, you may create a [Private](doc:private-events), [All Users](doc:all-users-events), or a [Public](docs/public-events) event.",
    "3-0": "Custom Fields",
    "3-1": "If both the **Publicly Displayed** and **Include in Webcast Event Settings** are set to **True**, then the field is displayed for use/configuration in **Go Live** settings as in the \"Recommended Viewing\" [custom field](doc:add-custom-fields) example above.",
    "4-0": "Templates",
    "4-1": "Use to select a pre-configured [Webcast Template](doc:create-a-webcast-template).",
    "5-0": "More Settings",
    "5-1": "Switches to the traditional event set up screen in the Event Calendar where you can schedule a **Webcam and Screenshare** event or any other kind of event if needed."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]

Once you have configured your **Go Live** settings, click the **Next **button to [Start the Event](doc:host-a-self-produced-webcast#start-the-event).  

Starting a **Go Live** event performs exactly as described above when hosting a scheduled event.

> 👍 Tip
> 
> It is very important that you test this feature within your environment.  There are differences in browsers and internet connections that can impact the quality.  As always, please verify the quality and flow before using within event.  Please review the [Rev Screen Share and Webcam Best Practices](doc:rev-screen-share-and-webcam-best-practices).