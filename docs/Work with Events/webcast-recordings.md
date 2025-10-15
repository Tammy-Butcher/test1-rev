---
title: Webcast Recordings
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



This section contains settings that specify how you want the video recording of your webcast to be handled once it has concluded.

> 📘 Note
> 
> Visibility and behavior of functions in this section is configured in [Webcast Recording Settings](doc:webcast-recording-settings) by an Account Admin.  It may also be disabled and/or hidden depending upon the video source used, as in the case of using an [existing video](doc:video-sources#existing-video-sourced-events) as a source.

## Automatically Record a Webcast

You can specify that a webcast begins to record automatically as soon as you begin broadcasting the event.  To do so, make sure the **Automatic Recording** tab in this section is set to **Enabled**.  You may always pause and restart the recording at any time during the broadcast when using this setting.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bbb65d8-automaticRecording.png",
        "automaticRecording.png",
        502
      ],
      "align": "center",
      "caption": "Enable automatic recording to set the webcast to record automatically as soon as the Event Host broadcasts the event"
    }
  ]
}
[/block]

> 📘 Note
> 
> For this feature to work as described, [Webcast Recording Settings](doc:webcast-recording-settings) must be set to **Allow**.

## Link and Redirect Webcast Recordings to Completed Events

Linking and redirecting Webcast recordings offers attendees the ability to seamlessly transition from viewing a live webcast to its recording once it has completed. Event Hosts control _when_ it is redirected so that it may be edited before it is viewed if desired.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/964c401-linkRedirect.png",
        "linkRedirect.png",
        402
      ],
      "align": "center",
      "caption": "These two settings specify to link the webcast recording to the completed event and then to redirect attendees to the linked recording once you are done editing it"
    }
  ]
}
[/block]

**Link ** a webcast recording to a completed event by enabling the **Associate and link webcast recording with the completed event** tab. You can enable it once the webcast has started or during set up.

When a webcast recording is **linked ** to a completed event:

- The event recording is automatically associated to the completed event for both manual and automated webcasts
- In the event that multiple recordings took place during the webcast, the _last_ recording is associated upon event completion

**Redirect ** attendees to a linked webcast recording by enabling the **Redirect attendees to linked webcast recording for the completed event** tab.

When attendees are redirected to a linked Webcast recording:

- Attendees visiting the event link after the webcast has completed (and event linking has been enabled) are redirected to the recorded video
- If this setting is disabled, attendees visiting the event link after the Webcast has completed are redirected the **Webcast Landing Page** instead
- Keep in mind that the video must be also viewable by the attendee. That is, **Active**, not in a **Legal Hold**, part of an **Approval Process**, and so forth.

Account and Event Admins may use the **Edit **icon from the **Webcast Landing Page** to edit either setting link/redirect at any time. 

For example, you may decide to edit the event recording to a more professional version (or to remove sensitive information) and disable redirecting while doing so.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1d54f2-landingPageLinkRedirect.png",
        "landingPageLinkRedirect.png",
        722
      ],
      "align": "center",
      "caption": "You can disable redirecting from the Webcast Landing Page if needed to make necessary adjustments"
    }
  ]
}
[/block]

## Select the Uploader for the Recording

The creator of the event is specified as the **Uploader ** by default but it may be changed to any system user during set up and is _not _ limited to the Hosts or Moderators of the event.

At least one uploader is required but no more than one may be selected.  This field is required and may \_not \_be edited during the webcast.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d6be9de-uploader.png",
        "uploader.png",
        640
      ],
      "align": "center",
      "caption": "The creator of an event is selected as the Uploader by default but may be changed"
    }
  ]
}
[/block]