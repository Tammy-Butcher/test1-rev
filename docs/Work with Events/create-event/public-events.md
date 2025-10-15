---
title: Public Events
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



Rev allows creation of **Public **events that do not require attendees to log in or to authenticate with Rev first. To create a Public webcast, set the **Listing Type** to **Public** in the [Attendees](doc:attendees) section when you create the event.

When a webcast is Public:

- It appears in the [event calendar](doc:the-event-calendar) denoted by a **World Wide Web** icon as a visual indicator
- Account and Event Admins may enable or disable public access to the event at any time
- Event Hosts may choose one of two join methods for attendees:
  - **Anonymous**: No registration is required and no attendee information is collected
  - **Registration**: Allows guests to register for an event in advance or during the event
- The Password field may be used to set a unique password for the event for both types of join methods
- Public Webcasts are a [licensed feature](doc:rev-license-types-and-add-ons) and have viewing hours configured. Admins may check how many hours remain on the **Account Admin Dashboard** under the [Usage](doc:usage-system-analytics) tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3bd9cc6-publicEventType.png",
        "publicEventType.png",
        1125
      ],
      "align": "center",
      "caption": "You can specify that a Password and custom Webcast Registration Fields be used when you set up a Public Event; or attendees can join anonymously."
    }
  ]
}
[/block]

## Public Event Passwords

If you specify a password for a Public event:

- Passwords are case sensitive
- Passwords allow letters, numbers, and special characters
- There is no minimum length

The password that is created is included in the event invitation text that is created in clear text. If no password is specified, that is also be noted.

## Anonymous Attendees for Public Events

If **Anonymous** is selected as the **Attendee Join Method** when you create the **Public** event, no registration information is requested from the attendee in order for them to join.  You are able to toggle between Anonymous and Registration join methods at any point up until the webcast starts.  You should also note that no registration email or event details are sent to anonymous attendees as they are joined directly to the event.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c6b8e3-anonymousEvent.png",
        "anonymousEvent.png",
        1123
      ],
      "align": "center",
      "caption": "When Anonymous is selected as the join method, registration fields are removed and a Guest name is randomly generated"
    }
  ]
}
[/block]

When an attendee clicks the Join URL of a Public event set to Anonymous:

- The attendee is joined using a unique display name of **Guest-xxxxxx**. This is a randomly generated 6-character alpha/hex string for display purposes in attendee engagement functions such as Chat, Polls, Q&A
- Attendees appear on the [Webcast Attendee Report](doc:webcast-reports#download-attendee-data) with the generated guest name and all other user-specific columns are left blank
- Logged in Rev User Accounts may also join anonymous events.  These accounts do _not_ use Public Viewing Hours.

## Webcast Registration Fields for Public Events

If custom [Webcast Registration Fields](doc:add-custom-fields#public-webcast-registration-fields) are created and enabled for Public events, Account and Event Admins can specify which of those are displayed on the Login form.  

The Login form can be previewed during event setup using the **Preview the Login Screen** link.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2dc9914-publicWebcastPreview.png",
        "publicWebcastPreview.png",
        402
      ],
      "align": "center",
      "caption": "Click Preview the Login Screen to preview how the webcast registration and login screen will appear to Public event attendees"
    }
  ]
}
[/block]

Use the [Event Branding](doc:event-branding) section to modify text and background colors of the Login form if desired.  

You may also click and drag the handle to the right of a registration fields to rearrange the order they appear on the event registration form.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ceaaad-arrangeWebcastFields.png",
        "arrangeWebcastFields.png",
        702
      ],
      "align": "center",
      "caption": "You can select the fields you want to include and arrange them in the order you want them displayed."
    }
  ]
}
[/block]

> 📘 Note
> 
> Selecting the checkbox next to a custom field includes it on the **Login Screen**. However, you may _not _ deselect a custom registration field that has been designated as **required ** by an Admin when it is initially configured. 
> 
> **View**:  [Add Custom Fields](doc:add-custom-fields) for details on how to create custom webcast fields.

## Early Registration for Public Events

When you create a **Public** event, early registration is enabled by default.  If you want early registrants to receive an email with the live event details and their personalized join link you need to select the **Automatically E-mail Event Details** checkbox.  If this option is _not_ selected, and your attendees are registering more than 15 minutes _prior_ to start time, you will need to manually send event invitations/emails from the [Webcast Settings Dashboard](doc:webcast-settings-dashboard).  Registrants/attendees who are registering/joining _within_ 15 minutes of start time will be brought directly into the webcast.

The combination of settings you use here depends on how you are advertising the webcast and prefer attendees to register and join.

For example:

- 'At start time, click here to register and join'  OR
- 'Click here to register (and rsvp in advance so we know you plan on attending).  Once registered, check your email for a calendar invite and click your link to join'

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6c8e665-allowEarlyRegistration.png",
        "allowEarlyRegistration.png",
        1124
      ],
      "align": "center",
      "caption": "Select the Allow Early Registration checkbox to allow attendees to register before the Webcast date"
    }
  ]
}
[/block]

When a registrant is provided event details (either automatically or manually):

- Attendees can register for the event before the scheduled date and time of the webcast (as soon as the event invite link is provided).
- As noted, registrants automatically receive an e-mail with the event details (and a link to the webcast) if the **Automatically E-mail Event Details** checkbox is checked.  If you disable this checkbox, you _must_ manually send an Invitation Email to each registrant via the Actions menu on the **Registrations** tab or by copying the event info into an e-mail.
- Registrants are able to view [webcast recordings](doc:webcast-recordings#automatically-record-a-webcast) (if enabled) at the conclusion of the event using the same event link provided to them to register regardless of whether or not they attend the Live webcast.
- Early registration settings for an event are copied over to [Webcast Templates](doc:create-a-webcast-template) but any subsequent registrants for the event are _not_ copied or duplicated.
- Event Hosts can review and [manage early registrations](doc:webcast-settings-dashboard#review-early-registrations-for-public-events) on the **Registrations** tab on the [Webcast Settings Dashboard](doc:webcast-settings-dashboard) before the webcast begins.

## Customizable Consent Text

When you create a **Public** Event with a **Join Method** of **Registration** (as opposed to **Anonymous**) all attendees are required to provide their consent to the recording of their registration details before they may enter a webcast.  Attendee consent is requested in the form of a checkbox beneath the **Webcast Registration** fields.  

![](https://files.readme.io/f95cdd8-publicRegistrationText.png)

Default Consent text is provided for all scheduled events.  If you want to customize this text, begin by contacting [Vbrick Support](https://vbrick.com/support/) to request the ability to customize the Public Registration page 'Consent Verbiage'.   Once approved, a new toggle becomes available under the Webcast Registration Fields called **Customize Consent Verbiage**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/298579b-customizeConsentText.png",
        null,
        "Contact Vbrick Support if you want to create your own custom consent text for Public event registration consent"
      ],
      "align": "center",
      "caption": "Contact Vbrick Support if you want to create your own custom consent text for Public event registration events"
    }
  ]
}
[/block]

Click the **Enabled** tab and modify the default text to the new consent text you want to display to and have all attendees consent to prior to registering for an event.  You will need to acknowledge that by customizing this verbiage you are assuming the role of data controller for all user-entered data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/669af52-dataControllerPublicEvents.png",
        null,
        "When you change the consent text, you effectively become the Data Controller for your organization!"
      ],
      "align": "center",
      "caption": "When you change the consent text, you effectively become the Data Controller for your organization!"
    }
  ]
}
[/block]

> ❗️ Warning!
> 
> It is important to note that when you modify this text you, and not Vbrick, are now considered the **Data Controller** for your organization.  Data privacy regulations are far reaching and have legal implications.  You should be aware of this before you make this change.