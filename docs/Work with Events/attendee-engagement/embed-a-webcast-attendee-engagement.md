---
title: Embed a Webcast Attendee Engagement
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



Vbrick Rev supports embedding content from up to five third-party sites or URLs of your choice.  When you embed content or an attendee engagement in a Rev event, it appears directly in the right-side flyout tab in the Rev webcast.  You control the third-party site or engagement as you normally would on the back-end but your attendees do not have to leave the Rev webcast to view or interact with it.

> ❗️ Caution
> 
> Before you attempt to embed a third-party engagement, make sure your Account Admin has correctly enabled [third-party webcast engagements](doc:allow-webcast-engagement-embeds) in the Admin settings and you have obtained the **embed code** you will need during event setup.

To embed a third-party content or attendee engagement:

1. Edit or create a new event.

2. Scroll to the **Attendee Engagements** section and click the **Enabled** tab next to **Embedded Content**.

3. Click the **Add New** button next to **Manage Embedded Content** to begin adding your first engagement.  You can add up to five URLs or code snippets.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2edd014-enableEmbeddedContent.png",
        "enableEmbeddedContent.png",
        689
      ],
      "align": "center",
      "caption": "Click the Add New button to begin adding your embed code"
    }
  ]
}
[/block]

4. Enter the following fields for the embedded content.  Each field is required.

   - **Name** - This is the name that appears to attendees and that appears on the flyout tab during the webcast.
   - **Embedded Content Code** - The third-party URL or embed code.  Look for this on the application or website that you will be embedding.  This can usually be found in its Admin or Settings section.
   - **Tab Icon** - The icon that is assigned to the flyout tab that can be clicked to open it [during the webcast](doc:manage-embedded-engagements) to present the third-party content.

> ❗️ Caution!
> 
> If your Account Admin has not correctly set up the URL for your embed or if you enter the incorrect embed code here, you will receive an error.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/72a8484-addNewEngagement.png",
        "addNewEngagement.png",
        1125
      ],
      "align": "center",
      "caption": "Make sure you are adding engagements that your Account Admin has set up prior to your event in global settings"
    }
  ]
}
[/block]

5. Click the **Add** button once all fields are complete.  You may add up to five URLs or code snippets to your event.  If you can, it is recommended to specify the height and width of any embed code to be 100% to ensure it fills up the entire dedicated area on the attendee's webcast view.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d8633e-embeddedContentAdded.png",
        "embeddedContentAdded.png",
        1113
      ],
      "align": "center",
      "caption": "You may view and modify engagements after they have been added"
    }
  ]
}
[/block]

6. You may click the **Edit**, **Delete**, or **Preview** links next to an engagement after they have been added.  You may also edit and delete once the webcast has started.  It is strongly recommended you Preview the embed, code snipper or URL before going live to ensure it loads and displays correctly.

7. Your engagements appear on the **Embedded Content** flyout during the webcast.  When you activate them, they appear on their own named tab under the [Embedded Content](doc:manage-embedded-engagements) tab with the icon and name you assigned them.  At that point, all content you send from the third-party URL or site appears there.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f0dff9-manageEmbeddedContent.png",
        "manageEmbeddedContent.png",
        552
      ],
      "align": "center",
      "caption": "All embedded engagements appear under the Embedded Content flyout.  You must activate them and they will appear in their own tab."
    }
  ]
}
[/block]