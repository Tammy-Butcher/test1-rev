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

<Image
  alt="Section 2 of Zone page:  Vbrick Rev Settings

"
  align="center"
  src="https://files.readme.io/cd117f4-revSettings.png"
>
  Section 2: Vbrick Rev Settings
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field or Setting
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Rendition Selection for Auto Unicast for Cloud Streams
      </td>

      <td>
        Renditions are the different bitrate streams within a multi-bitrate (MBR) stream.  

        This feature allows Administrators to select which bitrates (High, Medium, and Low) will be served within this Zone.  At least one bitrate must be selected, but any mix will work and provide the appropriate MBR stream.  This feature is restricted to Vbrick sourced Cloud Streams.  

        This feature requires all DMEs within the zone to be **DME v3.28** or higher.  If not, it will only allow full MBR (all renditions) to be selected otherwise.
      </td>
    </tr>

    <tr>
      <td>
        Override Account Slide Delay Setting
      </td>

      <td>
        The **Override Account Slide Delay** setting allows you to override the Rev portal slide delay settings that are defined globally under **Media Settings** > **Slide Delay**. If this has not been defined globally or has been disabled, this checkbox does not appear.  

        If the checkbox is checked, then an additional setting, **Delay in Seconds**, is available.  Set the new delay in the **Delay in Seconds** field.  If no value is used here, the account level setting is used in **Media Settings**.  

        * \*View\*\*: [Add Slide Delay for Webcast Event Live Video](doc:allow-webcast-features#configure-webcast-rebuffering-thresholds)
      </td>
    </tr>
  </tbody>
</Table>
