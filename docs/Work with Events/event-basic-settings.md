---
title: Event Basic Settings
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
The event **Basic Settings** section contains fields that make it easier to find your event such as categories and tags.  This is also where you can set up a [dry runs](doc:prepare-a-dry-run) before your main event.

<Image title="nameDescription.png" alt={943} src="https://files.readme.io/ca96410-nameDescription.png">
  Title, Webcast Shortcut, and Description all assist in identifying the event and how to find it for attendees
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Setting
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Title (required)
      </td>

      <td>
        A descriptive title for the webcast.
      </td>
    </tr>

    <tr>
      <td>
        Description
      </td>

      <td>
        Extended description for the webcast that displays as part of the launch page before the event starts and as part of the [Event Details](doc:webcast-attendee-features#view-webcast-details) section after the event starts. This also becomes part of the invitation text to attendees so be aware of what is included in this field. 

        You may use the **Rich Text Editor** controls to customize the Description field including font size, color, formatting, and the ability to open a hyperlink to a new page if desired. As noted, this text formatting is displayed in the invitation text as well as on the event launch page and guest login (if enabled).
      </td>
    </tr>

    <tr>
      <td>
        Start Date / Time (required)
      </td>

      <td>
        The start date may not be after the end date/time. Time is defaulted to 9:00 a.m. (if not on monthly view). If navigated from weekly or daily view, the default is the time selected from calendar. This may not be after the end date/time.
      </td>
    </tr>

    <tr>
      <td>
        End Date / Time (required)
      </td>

      <td>
        The default end date is the same as the start date. The end date may not be before the start date/time. Time is defaulted to add one hour to the start time. This may not be before the start date/time.
      </td>
    </tr>

    <tr>
      <td>
        Timezone
      </td>

      <td>
        No time zone is selected by default because the time zone is assumed to be that of the user’s browser. The **Event Host** can manually specify a time zone for the event if scheduling an event on behalf of someone in another time zone. If manually specified, all Administrator accounts that can access the event details will see the event in the manually specified time zone.
      </td>
    </tr>
  </tbody>
</Table>

## Webcast Shortcut

The **Webcast Shortcut** field is used to create a friendly custom URL for the event that is easy for attendees to remember. 

> 👍 Tip
>
> This Webcast Shortcut URL may be used for multiple events so long as they do not conflict in date or time within the same 24-hour time frame.

Modify the **Webcast Shortcut** field with the friendly name you want to use. Your Rev URL is auto-completed for you based on the shortcut you enter.

* You may only use letters, numbers and dashes
* The shortcut must be a value between 5 and 50 characters in length
* It may not be assigned to another webcast whose pre-production time and lobby time start and end time overlap
* Webcast shortcuts may not be edited once the event starts

<Image title="webcastShortcut.png" alt={945} src="https://files.readme.io/ab766ed-webcastShortcut.png">
  When you enter an easy shortcut, Rev automatically creates the URL for you
</Image>

Once created, the custom URL is displayed on the [Webcast Settings Dashboard](doc:webcast-settings-dashboard) before the event begins and on the [Event Details](doc:webcast-attendee-features#view-webcast-details) form after it starts.  (To display on **Event Details**, the [Show Event Sharing Link](doc:event-basic-settings#show-event-sharing-link) must be enabled during set up).

Also note that if a webcast shares a custom URL with other events, clicking on it displays a **Select Event** drop-down. This drop-down contains each event that shares the URL and may be subsequently browsed through to select the webcast you specifically want to work with.

<Image title="selectEventLink.png" alt={734} src="https://files.readme.io/4c4d35c-selectEventLink.png">
  You may use the shortcut for multiple events so long as they do not overlap in the same 24-hour timeframe
</Image>

The **Permanent Link** , which is the permanent URL, always goes directly to a specific webcast. 

## Lobby Time

**Lobby Time** refers to the how soon attendees may access a webcast prior to its broadcast. The default Lobby Time is 15 minutes (required) and may be modified by up to a maximum of 2 hours (120 minutes) during event set up. 

Attendees are directed to [The Webcast Landing Page](doc:the-webcast-landing-page) and are presented a message stating that the webcast has not started along with the start date and time.  There is a Landing Page for dry runs and main events denoted by a banner across the top.

<Image title="lobbyTime.png" alt={1103} src="https://files.readme.io/42246ab-lobbyTime.png">
  Lobby time allows attendees to access the webcast details for a period of time before it actually broadcasts
</Image>

> ❗️ Warning!
>
> If you are testing events before broadcasting them and [Prepare a Dry Run](doc:prepare-a-dry-run-event), the **Lobby Time** should be shorter in duration than the **Pre-Production Time Duration**. That is, if your Lobby Time is set to 30 minutes, then your Pre-Production Time Duration should be *more* than 30 minutes.
>
> Once the webcast *begins*, including Lobby time, only the webcast controls may be modified.  No other webcast settings may be changed at that point.  This includes DMEs associated to the event.

## Show Event Sharing Link

The **Show Event Sharing Link** option is used to hide or display the **webcast sharing URL** on the [Event Details](doc:webcast-attendee-features#view-webcast-details) page that is displayed to attendees while it is broadcasting.  This setting is enabled by default.

<Image title="showEventSharingLink.png" alt={612} src="https://files.readme.io/08a9a89-showEventSharingLink.png">
  To hide the webcast URL on the Webcast Landing page and Event Details form, disable this setting
</Image>

## Pre-Production

Enable the **Pre-Production** tab if you want to conduct one or more test runs (dry runs) of your event *prior* to the scheduled start time of the main (production) event. 

<Image title="enablePreProduction.png" alt={716} src="https://files.readme.io/16dce7c-enablePreProduction.png">
  The Pre-Production setting allows you to conduct "dry-runs" of your event hours or even days before it is scheduled to begin
</Image>

When enabled, the following settings are visible:

* **Pre-Production Time Duration**: Time duration, prior to the official start time of the event, during which you are able to finalize settings and perform test runs (dry runs) of the event.
* **Pre-Production Attendees**: People that are participating in the dry run of the event. Hosts and Moderators are automatically part of a dry run.

**View**: [Prepare a Dry Run](doc:prepare-a-dry-run-event) for steps on running a dry run of your event before you host the main event.

## Categories and Tags

Add your event to the various categories and tags that are in Rev in the **Categories** and **Tags** controls. This makes your final webcast recording more easily found through searches and on the [Browse Categories](doc:user-menu-options#videos) menu option as well. 

Once your recorded webcast becomes a VOD asset after the webcast has concluded, the resulting video retains the categories and tags you have set.

> 📘 Note
>
> You are only able to view categories you have permission to view if the category has been designated a restricted category.

## Custom Fields

If **custom** fields are added (and then set to display) in webcast events by an Account Admin, they display beneath the **Tags** field. If they are also required, they display a red asterisk next to them.

[Custom fields](doc:add-custom-fields#section-usage) allow you to add custom metadata to a webcast event that is specific to your organization. 

In the example below, two custom fields are configured for events: Additional Notes and Recommended For.

<Image title="customFields.png" alt={806} src="https://files.readme.io/849750c-customFields.png">
  Custom fields allow you to collect or convey additional data specific to your organization or events
</Image>
