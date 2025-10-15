---
title: Bulk Editing Features
excerpt: How to modify the metadata of several videos at once
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
You may bulk edit video settings and metadata to save time when edits on multiple videos at once are needed. You may only bulk edit videos if you have Account Admin, Media Admin, or Edit Access [permissions](doc:roles-and-permissions) to them. 

To use bulk transcription and AI metadata creation, you must have the [Rev IQ user role](doc:granular-roles-and-permissions) and your Rev portal must have [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available.

> 👍 Tip
> 
> There is a **1000 **video maximum cap that can be edited at once. You must have bulk video editing permissions before you may perform the operations described in this guide.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2481164-bulkEditIcon.png",
        "bulkEditIcon.png",
        "The Bulk Edit icon appears in most Media menu dropdown options"
      ],
      "align": "center",
      "caption": "The Bulk Edit icon appears in most Media menu dropdown options"
    }
  ]
}
[/block]


Bulk editing functions are accessed through the **Bulk Edit** icon that appears with right navigation icons under most [Media](doc:user-menu-options#the-media-menu) menu dropdown options.

When you click the **Bulk Edit** icon, videos appear in list form for selection. Videos are selected for bulk editing by selecting the checkbox to the left of the video. Click the topmost checkbox to select all videos in the displayed list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d13a1e90ea9844ee1c052168fa8207c94d0b752f7d9fca24ee34b0f171b2542-bulkEditUI.png",
        "bulkEditUI.png",
        "Selecting a checkbox next to a video selects it for inclusion in the bulk edit"
      ],
      "align": "center",
      "caption": "Selecting a checkbox next to a video selects it for inclusion in the bulk edit"
    }
  ]
}
[/block]


When you click the **Bulk Edit** (pencil) icon, there are six icons in the right navigation bar that perform various functions that are explained below.

| Icon                                                                                                                               | Feature                                                                                                                                                                                                                                                               |
| :--------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![](https://files.readme.io/4ae48228f8429411d2fb1fe5fb3ed36cb00694f62de0bba5317191b3b417745e-filterIcon.png)                       | The **Filters** icon. Applies a filter to the list of videos to narrow down the list you want to apply bulk edits to.                                                                                                                                                 |
| ![](https://files.readme.io/94035f8101193036e2926bb6a3f97f31f68626f5b8a6518b8306c9e6df10f428-autoGenTranscriptionMetadataIcon.png) | The **Auto Generate Transcription & Metadata** icon.  The default interface when the Bulk Edit icon is clicked.  Generates transcription and AI metadata for several videos at once.  You must have the Rev IQ role and Rev IQ credits available to use this feature. |
| ![](https://files.readme.io/6da7d3dff49191b54c60a8e15d51c174fcb1ebb90443806204c48e47c727d74c-bulkEditIcon.png)                     | The **Edit Videos** icon.  Allows you to edit various video settings on several videos at once.                                                                                                                                                                       |
| ![](https://files.readme.io/89b0f66afb0a58c0e620d43951c297a2e68aedc43339af3d0aac9f277f93ff0e-deleteVideos.png)                     | The **Delete Videos** icon.  Deletes the checked videos in the list.  Use with caution.                                                                                                                                                                               |
| ![](https://files.readme.io/969cb490cbeb16218cdd794424b17610b14cd2c3898f346cdcf731fc5e619d26-legalHoldIcon.png)                    | The **Legal Hold** icon.  Apply a legal hold to the selected videos in the list.                                                                                                                                                                                      |
| ![](https://files.readme.io/e32f7de050d508c6ffb4f6a3a5c26ae31cebc1c0bb174c1d559f8c496cc1e566-cancelBulkEditIcon.png)               | The **Cancel Bulk Editing** icon.  Cancels all editing in progress that has not been saved.                                                                                                                                                                           |
| ![](https://files.readme.io/a436475b8c145dad8853d7cc4a7dea8cd6ded86503d5cfa5a441d634e41453aa-downloadInventoryReportsIcon.png)     | The **Download Inventory Reports** icon.  Downloads all inventory reports or reports for the selected videos in the list.                                                                                                                                             |

## Bulk Edit and Auto Generate Functions

When available, the following features generally behave in the following manner during a bulk edit process unless otherwise noted:

- **Add** adds to whatever is already in place on the video.  No setting already in place is modified.
- **Replace **completely removes a current setting and replaces the configuration with your new setting.
- **Remove **deletes a current setting entirely and nothing new is added.

When you use the **Auto Generate Transcription & Metadata** features, the generate and replace features may vary depending on the field in use.  View the [Bulk Transcription and AI Metadata Creation](doc:bulk-transcription-and-ai-metadata-creation) topic for details.

> 👍 Tip
> 
> If you are unsure of the results of a bulk edit, **test **your settings on **one** video first before applying it to multiple videos!