---
title: Vbrick Rev Zone Settings
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The second section within a zone page is **Vbrick Rev Settings**.  These settings are specific only to customers that are licensed for **Vbrick Rev / EVP** and are not visible for other customers.  You can select and configure the settings as necessary when adding or editing the zone.  They are defined below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cd117f4-revSettings.png",
        "",
        "Section 2 of Zone page:  Vbrick Rev Settings\n\n"
      ],
      "align": "center",
      "caption": "Section 2: Vbrick Rev Settings"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Description",
    "0-0": "Rendition Selection for Auto Unicast for Cloud Streams",
    "0-1": "Renditions are the different bitrate streams within a multi-bitrate (MBR) stream.  \n  \nThis feature allows Administrators to select which bitrates (High, Medium, and Low) will be served within this Zone.  At least one bitrate must be selected, but any mix will work and provide the appropriate MBR stream.  This feature is restricted to Vbrick sourced Cloud Streams.  \n  \nThis feature requires all DMEs within the zone to be **DME v3.28** or higher.  If not, it will only allow full MBR (all renditions) to be selected otherwise.",
    "1-0": "Override Account Slide Delay Setting",
    "1-1": "The **Override Account Slide Delay** setting allows you to override the Rev portal slide delay settings that are defined globally under **Media Settings** > **Slide Delay**. If this has not been defined globally or has been disabled, this checkbox does not appear.  \n  \nIf the checkbox is checked, then an additional setting, **Delay in Seconds**, is available.  Set the new delay in the **Delay in Seconds** field.  If no value is used here, the account level setting is used in **Media Settings**.  \n  \n**View**: [Add Slide Delay for Webcast Event Live Video](doc:allow-webcast-features#configure-webcast-rebuffering-thresholds)"
  },
  "cols": 2,
  "rows": 2,
  "align": [
    "left",
    "left"
  ]
}
[/block]