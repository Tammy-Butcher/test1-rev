---
title: Create a Video Template
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
[Video Settings](doc:updating-video-settings) templates allow you to save common settings for videos that can be used again for future video uploads without the need to set them again from scratch which can be error prone.

For example, certain categories [that are not restricted] of videos that are uploaded frequently often use this feature for time and efficiency and may include training videos or townhall videos that need the same settings each time.

> 👍 Tip
> 
> Account or Media Admins manage all templates as well as specify a default template that automatically populates each time that a new video is uploaded to Rev.

## Video Template Exclusions

When a video template is created, most settings are saved “as is” including the template creator and the date it is created. This allows tracking of template security and future template enhancements. There are notable exceptions that are _not_ saved in a video template and that must be saved in any new upload _manually_. They are:

- Title
- Description
- Thumbnail
- SRT (Subtitle) File
- Supplemental Files that may be attached
- URLs (Live/Linked)
- Publish Date

## Adding a New Video Template

To add a new video template to Rev:

1. Navigate to a previously uploaded video.

2. Click the **Video Settings** > **Details **dropdown.

3. Review the [Video Settings](doc:updating-video-settings) that you want to keep in your template.

4. Click the **Save As Template** button at the bottom left of the form.

5. Use a descriptive name for your template in the **Save As Template** dialogue box. This must be a unique name or an error will generate.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3c9fe3-saveVideoTemplate.png",
        "saveVideoTemplate.png",
        502
      ],
      "align": "center",
      "caption": "The Save As Template button saves all currently applied settings (minus listed exclusions) into a video template"
    }
  ]
}
[/block]

6. You may now apply this template as a default template for all uploaded videos or to select videos that are uploaded as needed.

7. The video has the settings you saved in the template immediately applied when this template is used.

### Expiration Rules and Video Templates

It is important to note that video [Expiration](doc:update-basic-video-settings#set-an-expiration-date-or-rule) settings are ignored in a template if they are defined as a fixed **Date **as opposed to a **Rule**. 

For example, if you attempt to save the setting in the image below to a video template, the **Expiration **setting would actually be set to **None **when the template is applied to a video instead of the intended April date.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f45fb6e-expirationDateNotSavedExample.png",
        "expirationDateNotSavedExample.png",
        442
      ],
      "align": "center",
      "caption": "Expiration Dates cannot be saved as part of a video template since they are fixed."
    }
  ]
}
[/block]

**Expiration Rules**, on the other hand, are applied as expected when a video template is created and saved.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f7e177-expirationRulesSaved.png",
        "expirationRulesSaved.png",
        438
      ],
      "align": "center",
      "caption": "Expiration Rules are different since they are not \"fixed\".  They can be saved into the template and applied as normal."
    }
  ]
}
[/block]

If a [default](doc:setup-expiration-rules#create-an-expiration-rule) account expiration rule is set (at the account level), the video template expiration rule overrides the default setting. Expiration rules are applied in the following order for videos:

1. If a default video template is applied, the template’s video settings are applied first. This includes the **Expiration **setting used so long as it is a **Rule **and not a **Date **as specified above.

2. If the video template does _not_ have an **Expiration Rule** set, then the account’s [default](doc:setup-expiration-rules#create-an-expiration-rule) **Expiration Rule** is set (if an account-wide default rule has been configured). 

3. If no default account-level **Expiration Rule** is set or if the video template **Expiration **is set to **Date **(rather than **Rule**), then the Expiration setting is set to **None **when the template is applied to a video.

## Apply a Template to a Video

Any saved video template can be applied to a video’s settings to save time and reduce errors when adding or updating [Video Settings](doc:updating-video-settings). Templates may be applied to newly uploaded videos or to any previously saved videos.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/24eeb4b-videoTemplatesButton.png",
        "videoTemplatesButton.png",
        502
      ],
      "align": "center",
      "caption": "Click the Templates button to apply a previously saved video template to any video"
    }
  ]
}
[/block]

To apply a template, navigate to the video, and click the **Templates **button under **Video Settings**.  It is visible under both the **Basic **and **Advanced **tab(s).

## Set a Default Video Template

Account or Media Admins may specify a [Video Settings](doc:updating-video-settings) template to be the **default template** applied for all new videos that are uploaded. 

This means that the settings in the template are automatically populated and admins have control over which settings for new videos are enabled or disabled by default. For example, specific categories and tags could be automatically set for certain videos.

All video templates are managed by clicking **Video Templates** under the **Media Settings** menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a66251-manageVideoTemplates.png",
        "manageVideoTemplates.png",
        1202
      ],
      "align": "center",
      "caption": "Access the Video Templates module under Media Settings to Rename, Delete, or set a Default video template"
    }
  ]
}
[/block]

Use the **Video Templates** module to rename, delete, and set a default video template under the **Actions **menu.

> 📘 Note
> 
> Rev includes a **Standard Template** out-of-the-box for new accounts or for those accounts that are upgraded from Rev versions prior to the template feature release. 
> 
> The Standard Template reflects “hard coded” Rev defaults for a new video upload in terms of enabled settings and is set as the default template. This template may be deleted by an Account Admin or may be cleared as the default template as desired.