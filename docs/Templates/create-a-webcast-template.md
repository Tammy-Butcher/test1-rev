---
title: Create a Webcast Template
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
Webcast templates allow you to save common event settings that you are then able to use again for future webcasts without having to create them from scratch which can be error-prone.

For example, a quarterly CEO townhall event may need certain settings arranged and repeated for security and Q&A whereas a smaller departmental monthly staff meeting may have a different set of settings. Webcast templates may be created for each type.

Account Admins manage all webcast templates as well as specify a default webcast template that automatically populates each time that a new webcast is created.

> 👍 Tip
> 
> A webcast template is different from [duplicating an event](doc:duplicate-a-webcast) in that you can pick and choose which settings and metadata are applied to new events by enabling or disabling them and then saving them as a template.
> 
> When you duplicate an event, most settings are copied to the duplicated event as is. This includes the metadata for the webcast such as its name, description, tags, and categories which you may not want on a new event.

## Webcast Template Exclusions

When a webcast template is created, most settings are saved “as is” including the template creator and the date it is created. This allows tracking of template security and future template enhancements. There are notable exceptions that are not saved in a webcast template and that must be saved in any new event manually. They are:

- Video Source section. This should be unique and updated for each event.
- Start Date and Time which is defaulted to the current date and time
- Event PowerPoint presentation (if attached)
- Event templates and duplicated events do not carry over the **Estimated Attendees** field (users should enter the new estimate so a more accurate number is obtained).

## Adding a New Webcast Template

To add a new webcast template to Rev:

1. Navigate to [The Event Calendar](doc:the-event-calendar).

2. [Create an Event](doc:create-event) or edit a previously scheduled event.

3. Review the [Event Settings](doc:configure-event-settings) that you want to keep in your template.

4. Click the **Save As Template** button at the bottom left of the form.

5. Use a descriptive name for your template in the **Save As Template** dialogue box. This must be a unique name or an error will generate.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cd3d707-saveWebcastTemplate.png",
        "saveWebcastTemplate.png",
        502
      ],
      "align": "center",
      "caption": "The Save As Template button saves all currently applied settings (minus listed exclusions) into a webcast template"
    }
  ]
}
[/block]

6. You may now apply this template as a default template for all new events as needed.

7. The event has the settings you saved in the template immediately applied when this template is used.

> 📘 Note
> 
> If custom [public webcast registration](doc:add-custom-fields#public-webcast-registration-fields) fields are added to the event _after _ a webcast template is created (and are marked to be included in every webcast), they are automatically added/updated with the template.
> 
> The **Event Creator** is not automatically added as an **Event Host**.

## Apply a Template to a Webcast

Any saved webcast template can be applied to an event's settings to save time and reduce errors when adding or updating Event Settings. Templates may be applied to newly created events or to any previously scheduled events.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9608054-webcastTemplatesButton.png",
        "webcastTemplatesButton.png",
        502
      ],
      "align": "center",
      "caption": "Click the Templates button to apply a previously saved webcast template to any event"
    }
  ]
}
[/block]

To apply a template, navigate to the event, and click the **Templates **button in the top left of the form.

## Set a Default Webcast Template

Account or Event Admins may specify a webcast template to be the default template applied for all new events that are created.

This means that the [Event Settings](doc:event-basic-settings) in the template are automatically populated and admins have control over which settings for new events are enabled or disabled by default. For example, specific categories and tags could be automatically set for certain types of webcasts along with certain [attendee engagement](doc:attendee-engagement) features.

All webcast templates are managed by clicking **Webcast Templates** under the **Media Settings** menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9a6a11a-manageWebcastTemplates.png",
        "manageWebcastTemplates.png",
        1202
      ],
      "align": "center",
      "caption": "Access the Webcast Templates module under Media Settings to Rename, Delete, or set a Default webcast template"
    }
  ]
}
[/block]

Use the **Webcast Templates** module to rename, delete, and set a default webcast template under the **Actions **menu.

> 📘 Note
> 
> Rev includes a **Standard Template** out-of-the-box for new accounts or for those accounts that are upgraded from Rev versions prior to the template feature release.
> 
> The **Standard Template** reflects “hard coded” Rev defaults for a new event in terms of enabled settings and is set as the default template. This template may be deleted by an Account Admin or may be cleared as the default template as desired.