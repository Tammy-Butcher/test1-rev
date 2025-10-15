---
title: Add Custom Fields
excerpt: >-
  The use of custom fields on videos and during webcast registration is another
  way of making your video portal stand out by collecting and displaying
  information specific to your organization. This guide demonstrates how to
  configure and use custom fields in Rev.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
**Custom fields** provide the ability to display and collect data in Rev that are specific to your organization only. 

There are two types of custom fields in Rev; those that are used when **uploading videos** and those that are used during **public webcast registrations**.

Custom fields display on the Rev interface just as default fields do if visibility is enabled. You may also specify if they are required or optional just as "normal" Rev fields are required or optional. Finally, searching and bulk edits may also be performed on custom fields and they may be saved as part of your [video](doc:create-a-video-template) and [webcast](doc:create-a-webcast-template) templates.

There are two steps to using your own custom fields in Rev; creating them and then using them on a video upload or with a public webcast.

## Create a Custom Field

To create a custom field specifically for your organization:

1. Navigate to **Admin > System Settings > Custom Fields**.
2. There are two sections, **Custom Fields** for videos and **Public Webcast Registration Fields**.  
3. Use the **Add **button in either section to create the field you want to use.

### Video Upload Fields

<h4>Configuration</h4>

Click the **Add Custom Field** button in the **Custom Fields** section to add a new field for use when a new video is uploaded.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fad24db-customVideoFields.png",
        "customVideoFields.png",
        1114
      ],
      "align": "center",
      "caption": "Fields configured in the Custom Field section can be used with new video uploads"
    }
  ]
}
[/block]

1. Enter the **Name **of the field. This is the label displayed in **Video Settings**. This is a required field and must be unique.

2. Enter the **Type**.
   - **Text **- A text field is displayed to the video owner.
   - **Pick List** - You are able to enter options that the video owner chooses from after the video is uploaded.

3. **Required**.  The default setting for this is no.  This tab determines whether the custom field \_must \_be populated/completed by the video owner when editing Video Settings before saving the video.

4. **Publicly Displayed**. The default setting for this is yes. This field determines whether or not the custom field is visible to users that are \_not \_editing Video Settings.

5. **Include in Webcast Event Settings**. The default setting for this is no. This setting determines if the custom field is also usable during event setup.

<h4>Usage</h4>

When video custom fields are created, they appear beneath the **Description **field in Basic [Video Settings](doc:video-custom-fields) for the video owner to use. Just as with default field settings, required fields are marked by a red asterisk.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3f5902d-configuredCustomVideoFields.png",
        "configuredCustomVideoFields.png",
        350
      ],
      "align": "center",
      "caption": "Fields added in the Custom Fields section appear in video Basic Settings for video owners to complete"
    }
  ]
}
[/block]

If the **Publicly Displayed** tab is set to true, the field is also visible on the [Video Basic Information](doc:rev-video-player-features#video-basic-information) flyout to all users that view the video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6add357-customVideoFieldsBasicInfoPanel.png",
        "customVideoFieldsBasicInfoPanel.png",
        352
      ],
      "align": "center",
      "caption": "If Publicly Displayed is enabled, the fields appear on the Video Basic Information flyout panel"
    }
  ]
}
[/block]

If the **Include in Webcast Event Settings** tab is enabled, the fields also appear in the [Event Basic Settings](doc:event-basic-settings) to configure.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7e5ce31-customVideoFieldsIncludeinWebcasts.png",
        "customVideoFieldsIncludeinWebcasts.png",
        502
      ],
      "align": "center",
      "caption": "If Include in Webcast Event Settings is enabled, the fields appear in event Basic Settings to configure"
    }
  ]
}
[/block]

### Public Webcast Registration Fields

<h4>Configuration</h4>

Click the **Add Registration Field** button in the **Public Webcast Registration Fields** section to add a new field for use when a [Public webcast](doc:create-event#schedule-a-public-event) is hosted. 

By default, **name **and **email address** are collected for **Guest **users when signing in to a public webcast. To collect additional information, you must create custom registration fields.

![](https://files.readme.io/2cdf84f-webcastRegistrationFields.png "webcastRegistrationFields.png")

1. Enter the **Name **of the field. This is the label displayed to attendees to provide details about the field. This is required and must be unique among registration fields.

2. Enter the **Type**.
   - **Text **- A text field is displayed to the attendees.
   - **Pick List** - You are able to enter options that the attendee chooses from.

3. **Required**.  The default setting for this is no.  This tab determines whether the registration field _must_ be populated/completed by the attendee before joining the webcast.

4. **Included in All in Webcasts**. The default setting for this is no. This setting determines if the custom field is visible in all Public webcasts automatically. Event Admins and Event Hosts are able to specify if a registration field is visible on a Public webcast sign in forms during event set up.  If this setting is enabled, the field is automatically included removing that choice during event set up.

<h4>Usage</h4>

The custom fields created in **Webcast Registration Fields** section appear in the **Attendees **section during event set up for an Event Admin or Event Host to select as part of the sign in form when creating a [Public](doc:create-event#schedule-a-public-event) webcast.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/da27dcd-customWebcastFieldsSetUp.png",
        "customWebcastFieldsSetUp.png",
        1059
      ],
      "align": "center",
      "caption": "Event Admins / Hosts can select the registration fields they want to include and preview them"
    }
  ]
}
[/block]

Fields are arranged in the desired order by clicking and dragging.  If the field checkbox is deselected, it does not appear on the registration sign in form.  However, if the Account Admin has specified that this field is **Included in All Webcasts** when creating the custom field, the field is not able to be deselected and is _always_ included.

Click the **Preview the Login Screen** to get an idea of how your sign in form appears to Guest attendees.  If the **Required **checkbox is configured by the Account Admin then the field is required by attendees before they may sign in to the webcast.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/055482a-publicWebcastPreview.png",
        "publicWebcastPreview.png",
        811
      ],
      "align": "center",
      "caption": "Required fields must be completed before a Guest can sign in to a Public webcast"
    }
  ]
}
[/block]

## Configuration Tips for Custom Fields

- Account Admins can edit all settings with the exception of the **Type **attribute
- If the **Required **attribute is changed from **No **to **Yes**, the custom field is required the next time a User edits the video or webcast
- The custom field may be deleted by clicking the **Delete **button. This also deletes _all_ content associated with the field.
- You may order the way the custom fields display to Users by clicking the up and down arrows. You may also order **Pick List** items in the same manner.