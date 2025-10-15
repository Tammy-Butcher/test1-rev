---
title: Webcast Settings Dashboard
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
Once an event is created and saved, Event Admins and Hosts may access the **Webcast Settings Dashboard** to manage webcast settings, event invites, reports, and information specific to the different **Listing Types**.  There are settings you are able to edit and manage both before and after the event concludes.  Most settings you are able to [edit during the webcast](doc:edit-settings-during-an-ongoing-webcast) as well.

To access the **Webcast Settings Dashboard**, navigate to [The Event Calendar](doc:the-event-calendar) and edit the event by clicking its name.  Sections that are available before and after events conclude for the different Listing Types are discussed below.

## Webcast Links

The **Webcast** and **Permanent Links** for an event are created when you set up a **Webcast Shortcut** during event set up.  This creates a friendly custom URL for the event for attendees to remember.  These links are configured in the **Basic Settings** section in the [Webcast Shortcut](doc:event-basic-settings#webcast-shortcut) field.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/caf2ff7-webcastLinks.png",
        "webcastLinks.png",
        702
      ],
      "align": "center",
      "caption": "Webcast Shortcuts are configured during event set up to create a more easily remembered URL for attendees"
    }
  ]
}
[/block]

## Event Invitations

Event invitations are managed through your method of choice and are also dependent upon the Listing Type.  Use the **Copy Event Info** button to copy the event details which you can then paste into an email that you can then send to multiple recipients.  It includes the following webcast details:

- Event Name
- Start Date/Time
- End Date/Time
- Event URL

> 📘 Note
> 
> Webcast emails display all [event branding](doc:event-branding) you may have set up.  If you have not configured event branding, emails display [Rev account branding](doc:rev-branding-and-style-guides) instead.

The **Add to My Calendar** button adds the event directly to your system’s default calendar through an iCalendar download once the event is created and saved.   You can then send calendar invites as needed.

For a **Public** event, you can send an invite to a _specific_ registrant by using the [Send Invitation](doc:public-events#early-registrations) link in the **Registrations** table under the **Actions **dropdown.  This is typically used if a registrant has lost an invite, for example.  This can also be used as a way to pre-screen or approve/reject registrants before sending them the email with the details they need to join the event.  The personalized join link included in the email also provides the registrant access to the webcast recording/video-on-demand once the event concludes if they are unable to attend.

> 👍 Tip
> 
> When sending event invitations, consider adding how the attendee will access the event (through the calendar, the URL in the email, etc.) and a point of contact if they have any issues.  This is often where attendees have trouble initially with webcasts.

### Importing Public Event Early Registrations

**Event Hosts** or **Moderators** can quickly import **Public** event early registrations by uploading a CSV file. For example, you might want to import from marketing automation or external event registration platforms that you already use. If the registration (email) already exists for the event, it is updated with any new data. If a line in the CSV file is not formatted correctly or is invalid, the import of that row will fail. You must also specify if you want an email sent to the new registrant (similar to when you initially enabled **Pre-Event Registration** under the **Webcast Settings Dashboard**).

- Only .csv files are accepted
- Field names **must** be in the first row of the file (see sample import below)
- The e-mail field is unique and is also **required**
- If your CSV is invalid (not a CSV) or is not formatted correctly, an error message is displayed and it will not be imported
- Each row in the CSV is either created, updated (if it already exists), or skipped/failed. If a row is not formatted correctly, the entry fails and is skipped.
- There is an upload limitation of 300k rows allowed for this import
- An email, as well as a tray notification, is sent to the uploader as well as to the Event Hosts with a summary of the upload (number of registrants added, updated, not changed, and failed)

> 🚧 Important
> 
> As noted, there is an upload limitation of 300k rows allowed for this import.  You must also make sure that the first row in your CSV is the Header row and includes all the field names (see below).

To import early registrations from a CSV file:

1. Click the **Registrations **button.  This button is _not_ present if you have not enabled early registration or the event is not a **Public **event.

2. Click the **Upload Registrations** button next to the **Download Registrations** dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6c1fc1e-uploadRegistrants.png",
        "uploadRegistrants.png",
        411
      ],
      "align": "center",
      "caption": "Click the Upload Registrants button to upload a CSV file with registrant information"
    }
  ]
}
[/block]

3. Click the **Add File** button to select the CSV you want to use.

4. Click the **Automatically e-mail new or updated users** checkbox if you want an email generated to the registrants.

5. Click the **Submit** button to upload your registrants.

> ❗️ Warning!
> 
> While some of the fields described in the table below are optional in your upload, you **must** include each field in your first row as the **Header** row (seen in yellow below) or an error will occur.
> 
> You must save the file encoded in the UTF-8 format. Otherwise certain characters may not be displayed correctly.
> 
> There is a limitation of 300k rows allowed.

**Important Notes About Custom Webcast Registration Fields and CSV Imports**

If you use custom **Webcast Registration Fields**, it is important that they are formatted in your csv file exactly as they appear in Rev during event setup, especially if they are **Required** fields. Otherwise, your import will fail.  The correct way to format a custom webcast registration field in your csv is **(Custom) field name**, including any punctuation you may have used as in the example below, **(Custom) Type of Business:** 

![](https://files.readme.io/52dc0b5-formatWebcastFields.png "formatWebcastFields.png")

If the formatting does not match the field is ignored.  If the field is **Required ** in Rev (as in the example above) and the formatting does not match exactly, the import fails completely and your registrants are not uploaded.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4ec08d2-registrantCSVSample.png",
        "registrantCSVSample.png",
        1084
      ],
      "align": "center",
      "caption": "Download the sample CSV file to get started. The top row of fields (Header row) is required with correctly matching formatting."
    }
  ]
}
[/block]

[Download ](https://portal.vbrick.com/help/PDFs/REV/earlyRegistrationImport.csv) a sample CSV file.

| Field                         | Description                                                                                                                                                                                                          |
| :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                          | Registrant name. This is required.                                                                                                                                                                                   |
| E-mail                        | Valid email address.  This is required and must also be unique or the registrant is updated instead of created.                                                                                                      |
| (Custom) Custom Field Name(s) | Add the custom fields you want to include.  Note that they must also exist in Rev and be formatted exactly as they appear in Rev.  Best practice is to include all custom fields that are in Rev during event setup. |

> 👍 Tip
> 
> Once the import finishes, you will receive an email and a notification that summarizes the import including any failed imports.

## Review Early Registrations for Public Events

Event Hosts and Moderators are able to review early registrations and even remove (unregister) one or more registrants if needed before a **Public** webcast begins.  

To review early registrations:

1. Click the **Registrations **button.  This button is _not_ present if the event is not a **Public **event.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e13feb9-registrationManagementForm.png",
        "registrationManagementForm.png",
        1827
      ],
      "align": "center",
      "caption": "The Registrations button opens the Registrations Management form that displays all early registrations for Public events"
    }
  ]
}
[/block]

2. The **Registrations** table appears.  It includes:
   - registrant's name
   - registrant's e-mail
   - date/time registered
   - user type (licensed user/guest)
   - status (emailed/if an email was sent, attended/if the event is over and registrant attended)
   - custom registration fields (if configured)

3. The **Columns** component controls what is viewed on the table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e1bb642-earlyRegistrationColumn.png",
        "earlyRegistrationColumn.png",
        298
      ],
      "align": "center",
      "caption": "Select which fields to view on the Registration Management table"
    }
  ]
}
[/block]

4. The **Actions** dropdown allows a Host to perform actions on _one_ specific early registrant. 

   - **Copy Event Info** is identical to clicking the **Copy Event Info** button for an [Event Invitation](doc:public-events#event-invitations) except that it is _specific_ to that _one_ registrant instead of for the entire event. This is because it provides a personalized join link that is unique to each registrant.  This ensures when they return to view the live event, they won't have to enter their information again.  It also enables them to return after the event to view the webcast recording/video-on-demand afterward (if enabled). 
   - **Send Invitation** automatically sends a personalized e-mail invitation to a specific registrant
   - If you **Remove (Unregister)** a user, it is as if they never registered for the event and their personalized join link will now no longer allow them access to enter the live event 
   - Note that the **Actions** column becomes unavailable once the webcast ends

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/67b9e35-earlyRegistrationActions.png",
        "earlyRegistrationActions.png",
        219
      ],
      "align": "center",
      "caption": "Use the Actions dropdown menu to perform designated actions on a specific registrant"
    }
  ]
}
[/block]

5. You can perform the same actions in the **Actions** dropdown on several registrants at once using the **Bulk Actions** drop-down and selecting the registrants you want to perform the action on in the registrant table.  You can select 'All' registrants by selecting the top-level checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7246906-bulkEditRegistrants.png",
        "bulkEditRegistrants.png",
        1830
      ],
      "align": "center",
      "caption": "The Bulk Action dropdown works exactly as the Bulk Edit videos interface"
    }
  ]
}
[/block]

6. Use the **Download Registrations** button to download a report of the registered attendees to the **Public **event in csv format.  This list can be used for import into your preferred marketing or event management platforms.  The csv includes all the fields and functions included in the **Registrations** table.

## Manage Access and VOD Recordings for Public Events

If you enabled automatic registration emails, the registrant may click the link in the email received to log in to the webcast on the date and time the **Public **webcast begins and does not need to enter their information again. If this email is misplaced, send the registrant a new invitation through the **Send Invitation** link on the  **Actions** dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5bf3c7a-earlyRegistrantEmail.png",
        "earlyRegistrantEmail.png",
        485
      ],
      "align": "center",
      "caption": "Early registrations need only to click the link in the email received to log directly into the webcast"
    }
  ]
}
[/block]

This same link may be used by registrants to view the VOD recording of the webcast once it concludes regardless of whether or not they attend the Live webcast.  [Webcast Recordings](doc:webcast-recordings) must be enabled and linked for the event for this to work correctly.

> 📘 Note
> 
> If the webcast link is accessed before the scheduled Start and/or Lobby Time of the webcast, a summary of the event is provided with an option to add the event to the registrant's calendar.

If early registration is _not_ enabled, or for those that did not register, the **Guest Registration** form is displayed when the webcast URL is clicked.  

The user must either log in (if a licensed account) or **Sign in as a guest** based on the fields configured during the event setup.  Notice that the branding and background image selected during setup are also used.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/00a2e56-guestSignIn.png",
        "guestSignIn.png",
        654
      ],
      "align": "center",
      "caption": "A Guest Registration form is used for Public events that do not use early registration and/or for non-licensed accounts"
    }
  ]
}
[/block]

Attendees need to complete all fields including a **Display Name**, **Email**, and **Password ** (if included) before they may click the **Sign in as a guest** button. This includes any custom fields that are configured as "required". 

If attendees do not remember the password, they may refer to the event invitation email. Attendees may also use a Rev licensed user account and log in to any Public event if they have one.

> 🚧 Important!
> 
> Public webcast attendees are made aware that Vbrick captures a **Display Name** and **Email Address** that is used in certain webcast features and reports. This use _must_ be consented to _before_ the guest sign in is completed.

## Embed an Event

If enabled, the [Embed](doc:embed-a-webcast) button is present next to the **Webcast Link** so that the webcast can be embedded on 3rd-party Websites or portals.

## Duplicate a Webcast

Use the [Duplicate Webcast](doc:duplicate-a-webcast) button to copy the event and quickly set up features and technical settings without needing to create them again.  Note that this is not quite the same as creating a [Webcast Template](doc:create-a-webcast-template).  Both features, however, save you time if using many of the same features for several webcasts.

## Webcast Reports

The [Webcast Analytics Dashboard](doc:view-webcast-analytics) is available to view once the event concludes by clicking the **Reports **button. 

The **Reports** button contains _both_ **Main Event** and **Pre-Production** report access. If the Main Event has not yet started, only Pre-Production events are available. If no Pre-Production dry runs are conducted, only the Main Event report is displayed.

If no Webcasts have occurred yet, the drop-down displays, “No reports are currently available” until one has concluded.

## View Webcast Details During the Event

When you start the webcast, the **URL** and its **Password **(if created) is displayed under the **Webcast Information** icon. A link to download the PowerPoint presentation slides is included here as well if downloads are allowed during the event setup.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a035ab5-eventDetails.png",
        "eventDetails.png",
        383
      ],
      "align": "center",
      "caption": "Click the Webcast Information icon to obtain the event details again if you need them, including the Webcast URL and Password"
    }
  ]
}
[/block]

> 👍 Tip
> 
> If the [Show Event Sharing Link](doc:event-basic-settings#show-event-sharing-link) setting is disabled in [Event Basic Settings](doc:event-basic-settings), the webcast URL is not displayed on the **Event Details** panel.