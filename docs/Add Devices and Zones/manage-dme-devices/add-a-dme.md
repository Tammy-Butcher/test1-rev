---
title: Add a DME
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
Account Admins can add DMEs to Rev through the **DME Management** module by clicking the **Add DME** button.  This brings up the **Add a DME** page which allows the initial configuration of a DME.   Not all configurations of a DME can be set during an **ADD** -- only the most common settings are initially displayed.  After _adding_ the DME to Rev, if you click on its name you are then presented with a _full_ list (common and uncommon) of configurable DME settings at that time.

To add a new DME to Rev:

1. Navigate to **Devices **> **DME Management** > **Add DME**.

2. Complete the field or setting(s) described below as needed or required.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f6aae6b-addDme.png",
        "addDme.png",
        802
      ],
      "align": "center",
      "caption": "Click the Add DME button from the DME Management module to add the device to Rev"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Description",
    "0-0": "Device Name",
    "0-1": "This can be a name of your choosing. This is a required field.  \n  \nIf you will have multiple DMEs (common), then it is recommended that you develop a naming scheme.  A name containing the location or Host name/FQDN is recommended.",
    "1-0": "Status",
    "1-1": "The status of your device may be set to **Active **or **Inactive **.  \n  \n**Active** DMEs will, if configured within **Zone**, be used for distribution.  **Inactive** DMEs will not be used when Rev generates playback URLs, but may continue to be used in a DME Mesh or shared cache scenario.  If you do not want your DME used at all, it is recommended that you **Inactive** it and turn it off.",
    "2-0": "MAC Address",
    "2-1": "The MAC Address is required. A quick way to find a DME's MAC Address is to log-in to the DME and navigate to **System Configuration** > **Activate Feature**.  The MAC Address is displayed there."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "left",
    "left"
  ]
}
[/block]


![](https://files.readme.io/7019a80-storageCheckboxes.png "storageCheckboxes.png")

[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Description",
    "0-0": "VOD Playback Device",
    "0-1": "This checkbox is selected by default and enabled if the DME is to be used as a **Video on Demand (VOD) playback device** for serving stored video content.  \n  \nIf more than one DME is designated as storage, then content is pushed to _all_ designated DMEs.  \n  \nIf this box is not selected, then this DME will be **primarily** used for Live distribution.  Addition configuration may be necessary depending on use case.",
    "1-0": "Preposition Content",
    "1-1": "This checkbox specifies which DMEs on the network receive [prepositioned video](doc:add-a-dme#preposition-dme-content-downloads) files for playback; should _only_ be used if you are also using **MESH**.  \n  \nYou can also then set your **download schedule** which becomes visible.  \n  \nNote:  By default this feature is disabled.  There are several different models of caching (see below) that will get content onto DMEs.  Vbrick recommends that you have all your DMEs on v3.29 (or above) and utilize direct VOD caching (i.e., disable this feature).  This eliminates the timing delay necessary  for downloading large files.",
    "2-0": "Video Streams",
    "2-1": "**Name**, **URL**, **Encoding Type**, and **Multicast **are all designated [through the **Advanced **tab > **Add URL** button if adding manually] and are required fields if the DME is intended to be utilized as a **streaming** device.   These streams are later selected on **Presentation Profiles** and **Zones **as viewing destinations.  Additionally, you may also generate your URLs _dynamically_ through the **Create URLs** tab.  You may set these now, or return to the DME edit page to set then later.  \n  \nNote:  In order to playback streams using **HTTPS** within our Rev HTML5 player it is necessary for your DME to have a **Fully Qualified Domain Name (FQDN)** .  This is **highly recommended** and best practices for enterprise-level security postures.  Additionally, that **FQDN** is necessary for Certificate Requests (either in-whole or in-part as with a wildcard CERT.)  Note: DME v3.10 and greater devices are capable of registering **fully qualified domain names** in order to play HTTPS content to the Rev HTML5 video player. Therefore, DME streaming URLs may or may not contain an IP address Hostname.  \n  \nView: [Add DME Video Streams](doc:add-a-dme#add-dme-video-streams) for more details and examples."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "left",
    "left"
  ]
}
[/block]


3. After each setting is configured, click the **Create **button to add the DME Device.

4. The DME  status state should flip from **Uninitialized **to **Active **after a few seconds. If it does not, check your **MAC Address** field and/or the DME initial configuration steps such as the API Key and Host fields. **View**: [Getting Started - Devices](doc:getting-started-with-rev-devices) 

5. Once status is **Active**, the DME is ready to use with your Rev portal.

6. Account Admins are sent an email notification if any DME goes into **Warning **or **Offline ** status so that they may pro-actively troubleshoot it.

> 📘 Note
> 
> During normal operation, a DME's heartbeat to Rev occurs about once every 15 seconds to accept commands and/or send status updates.  If a DME is **Inactive** or **Offline** for more than 8 hours, the heartbeat frequency is reduced to once per **hour**. If a DME is **Inactive** or **Offline** for more than 7 _days_, the frequency is reduced to once per day.  
> 
> Reduced frequency heartbeats affect how long it takes a DME to re-activate or achieve online status so it may take as long as 24 hours to re-activate a DME that has been inactive for a long time.  
> 
> To quickly get a DME back to normal, 15-second heartbeats, you can use the DME VBAdmin interface to disable or enable Rev's interface and connection with it. View the DME help topic, [Enable and Configure the Rev Interface](https://dmedocs.vbrick.com/docs/enable-and-configure-the-rev-interface) for details.  

## DME Caching Methods Explained

At the heart of the DME is a shared caching system -- distributed across all connected DMEs.  There are several ways to get content into those caches which we discuss here.

To understand the caching models, it is useful to understand the general playback flow utilizing Rev.  When a viewer's browser requests playing a video it is provisioned a number of playback URLs from Rev.  These playback URLs are Zone specific, meaning if viewers are in different Zones they may get different URLs.  In other words, Rev will provide URLs that point the DMEs within the viewer's Zone.  The player reaches out to the DME for the video, and the DME will attempt to service that request.

### The Ultimate Fallback Method (Legacy)

The **Ultimate Fallback** feature is a legacy feature that allowed the player to request content from a local DME (and the DME Mesh) and, failing that, fell back to retrieving content from Rev.  In this legacy use case, the player requested the content from the local DME.  The local DME did not have the content, so all the "sisters" (or peer) DMEs were queried for the content.  If none of the "sisters" had it, and the requesting DME did not have it, then the request failed back to the player.  The player then played back from Rev (Cloud).  At this point, however, the requesting DME (who did not have the content) requested the content from Rev.  Rev provided the content to the requesting DME and all other DMEs were set as pre-positioned.  The next requestor received the content from the DME or DME Mesh.

### The First-Time VOD Caching Method (Recommended)

Beginning with Rev v7.53 and DME 3.29 the system utilizes a new caching method called **First-Time Caching VOD Caching**. The DME will no longer fallback but instead retrieves the VOD HLS _piece_ to service the request (and does not request the entire VOD.) This piece is then in the DME's cache going forward. This feature begins to remove the dependency on "ultimate fallback" and the DME acts more like a caching engine and treats VOD assets individually. You can still manually preposition, you can still set up preposition, but our recommendation is to no longer do this with our new caching algorithm.

> 👍 Tip
> 
> If you are using **Prepositioned Content**, you should make sure that all DMEs in your network are able to communicate with at least _one_ DME that has _all_ prepositioned content.  
> 
> If you are not using **Prepositioned Content**, then requests that go to DMEs will utilize the **DME Mesh** and **Ultimate Fallback** but _only_ if you are using DMEs that are not upgraded to **v3.29+**.  Playback will continue and content that is viewed will still make its way onto DMEs for local serving.  Having DMEs that are highly connected will optimize the use of the **DME Mesh** or **Ultimate Fallback**.
> 
> DMEs that are upgraded to v3.29+ now use **First Time VOD Caching** instead which is much more efficient.

## Preposition DME Content Downloads

Even with  **First-Time Caching VOD Caching** or **Ultimate Fallback**, there are use cases that requires content initially resident on DMEs.  This is called prepositioning and is set at the DME level.

You can designate which DMEs in your video ecosystem have content prepositioned immediately (downloaded to the DME immediately after upload) or schedule content (by day of the week and time) by selecting the **Preposition Content** checkbox. This option is only available for DMEs that are also selected as a **VOD Playback Device**.

> 📘 Note
> 
> This feature is used with the DME's Mesh caching configuration View the [Mesh with Rev Caching Configuration](https://dmedocs.vbrick.com/docs/rev-mesh-caching-configuration) topic in DME Online help.

Rev uses [zone logic](doc:add-a-zone#zone-logic-flow) to route content requests by users to the closest DME. If the DME closest to the user does not have the requested content (either in the cache or on the disk), _that_ DME requests the content from all “sister” DMEs (peer DMEs that are reachable). 

If the content is available (the DME uses the first "sister" that responds), then the content is retrieved from that "sister" and cached on the requesting DME.  It is now cached and available for the _next_ user requesting it (with no need to go back out to all other DMEs). 

Initially, the only “sister” DMEs that have the content are the prepositioned DMEs. Subsequently, as the content becomes available on more DMEs based on user content requests, _any_ DME that has cached a copy of the content becomes a sister DME that other DMEs can then retrieve content from.

This means that content is only pushed to a handful of DMEs initially, so _fewer_ downloads are pushed through the cloud and into the network for Rev Cloud customers.

To preposition DME content and schedule downloads, make sure both the **VOD Playback Device** and **Preposition Content** checkboxes are selected.  Both are required.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6dd66ad-prepositionContent.png",
        "prepositionContent.png",
        907
      ],
      "align": "center",
      "caption": "The Scheduled Download control appears when the Preposition Content checkbox is selected"
    }
  ]
}
[/block]


The **Scheduled Download** control appears when the **Preposition Content **checkbox is selected. This allows you to specify when this DME receives video files so that network traffic is managed by timezone, day of the week, and even by the hour if necessary. 

The example DME schedule above only has video pushed to it on Saturday and Sunday between the hours of 3:00 a.m. and 7:00 a.m. eastern time.

> 👍 Tip
> 
> If no schedule is set, content is always pushed to the DME as soon as it is finished transcoding.
> 
> You can also _choose_ how content is synced once the DME is added and saved; immediately or scheduled. **View**: [Synchronize DME Content](doc:manage-dme-devices#synchronize-dme-content)

There are several instances where a DME will trigger a **Rev Mesh** update. They are:

- If any DME reports a new **Hostname **or **IP** to Rev
- If any DME reports a new **software version** number (including **build**)
- If any DME reports a change in** http / https serving status** to Rev
- If any DME **preposition status** is changed (enabled or disabled) on Rev
- If any DME status (**Active **or **Inactive**) is modified
- If any DME **VOD Playback Device** setting or status is modified

## Configure DME Specific Multicast Settings

The following settings allow configuration of DME specific multicast settings.  Again, this requires the [Vbrick Multicast Agent](https://portal.vbrick.com//doc/PDFs/REV/Vbrick%20Multicast%20Install%20Quick%20Reference.pdf) be installed on the viewer's PC or Mac.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd7a36e-dmeFecSettings.png",
        "dmeFecSettings.png",
        1306
      ],
      "align": "center",
      "caption": "When VBM is installed on a viewer's PC or Mac, you can configure DME specific multicast settings"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Description",
    "0-0": "Customized FEC Settings",
    "0-1": "Allows the selection of an FEC level (different from the account FEC level set on the [Security](doc:dme-and-vbrick-multicast-security#vbrick-multicast) page).  Modifying this changes the FEC used for VBM streams configured at Rev as well as cloud ingested (VCI/RTMP) multicast streams.  \n  \nReminder:  This feature is only available if the account has enabled [Encryption](doc:dme-and-vbrick-multicast-security#enable-vbrick-multicast-encryption).",
    "1-0": "Enable Auto Multicast for Cloud Streams",
    "1-1": "Sets the DME to provide streams that can be used in **Zones** and **Presentation Profiles** that will automatically pull cloud based streams (VCI/RTMP) and configured custom devices when using the stream **Auto Multicast for Cloud Streams**.",
    "2-0": "Multicast IP Addresses",
    "2-1": "A set of addresses (within the local multicast IP range) that will be used for multicast streams.  These IP ranges are specific and should be provided by your IT/Networking group.  (Do not make these IPs up or chose your own, as you may stomp over another existing stream.)",
    "3-0": "Port / Port Range",
    "3-1": "Ports that will be combined with the Multicast IP Addresses.  It is recommended that only ports (and not Port Ranges) are used.",
    "4-0": "Packet Size",
    "4-1": "The size of the multicast packets.  Recommendation is 4096.",
    "5-0": "Rendition Selection for Auto Multicast for Cloud Streams",
    "5-1": "Renditions are the different bitrate streams within a multi-bitrate (MBR) stream.  \n  \nThe origin cloud stream is typically an MBR stream but only one bit rate will be used for multicasting.  This setting controls whether the DME will use the highest or lowest bit rate from the origin MBR to create the multicast stream.  \n  \nNote that only one rendition may be selected and it applies to all auto multicast streams created by this DME."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]


## Add DME Video Streams

DMEs are caching and streaming edge-devices deployed on customer networks where content is distributed and viewed.  One of Rev’s primary capabilities is to provide live streaming out to player pages – and it does that through mapping named streams through its distribution configuration.  Meaning, these named streams are used within [Presentation Profiles](doc:add-a-presentation-profile) and [Zones](doc:manage-and-add-zones) to control and define where the streams are provided.

Named streams are specified within the Rev **DME Management** module.  Administrators are able to create named streams that represent physical streams on each DME.  This means a stream called <code>StreamExample</code> could be defined on Rev.  That <code>StreamExample</code>, and its different flavors of distribution (**RTMP**, **RTSP**,  **Multicast**, etc.), are then specified within **Presentation Profiles** and **Zones**.  A stream that matches that name still needs to be provisioned within the DME itself (as either a push or pull from a source.)

Video streams on a DME are set up manually or dynamically by the DME itself. There are several methods to creating named streams (outlined below).  These include: 

- Creating them dynamically for **CDN** distribution
- Creating them manually by providing a source URL
- Utilizing saved [Custom Device](doc:add-a-source-or-custom-device) streams

> 📘 Note
> 
> An **RTSP **unicast stream is required for recording live webcasts in Rev. Make sure that your stream has a keyframe interval between 2 to 5 seconds and do _not_ use B-frames. 
> 
> Please see your individual Encoder (stream source) documentation for setting information.

### Add a Dynamic Stream

The **Create URLs** tab under **Video Streams** is used to create your own dynamic named streams for playback URLs in Rev. 

> 🚧 Important!
> 
> CDN streams are added dynamically at the start of the event.  AWS is used for CDN distribution for customers.  Contact Vbrick Support if you need assistance.

Click the **Add URL** button to add a new stream.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/898490b-dynamicVideoStream.png",
        "dynamicVideoStream.png",
        902
      ],
      "align": "center",
      "caption": "Click the Create URLs tab to dynamically generate a video stream"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Description",
    "0-0": "Name",
    "0-1": "This is the stream name. The stream name must be unique within the DME that you are currently adding. If you are setting up several DMEs to distribute the same stream, consider a naming scheme using the same stream name as a prefix within the name across each DMEs so that you can easily trace the stream.  \n  \nStream names must be alphanumeric and contain no spaces. Stream names are not case sensitive.",
    "1-0": "Enable Vbrick Multicast",
    "1-1": "Select if you want to enable Vbrick multicast streams. You must have DME software v3.18 or greater before this may be configured.  \n  \nOnce selected, enter the following to automatically configure Vbrick multicast streams:  \n  \n- **Multicast IP Address**: (required) Must between <code>224.0.0.0</code> and <code>239.255.255.255</code>\n- **Multicast Port**: Default is <code>4444</code>\n- **Packet Size**: (entry 1000 to 8192) in Bytes, default: <code>4096</code>Please note that the IP Address and Port cannot be duplicated across multiple streams.  Consult your Networking/IT department for appropriate address.HLS streaming options are independent of Vbrick multicast streams  \n  \nIf the IP Address, Port, or Packet Size values fail, Rev displays a configuration failure message and requests that you edit the values again.  \n  \nViewers PC/Mac must have the **Vbrick Multicast Agent** installed to receive the streams.",
    "2-0": "Enable HLS generation",
    "2-1": "Select if you want to create an HLS stream. This is required for mobile devices. The default is no.",
    "3-0": "Enable CDN distribution during Rev Event",
    "3-1": "You must have the **Enable HLS generation** checkbox enabled before this becomes visible.  \n  \nYour DMEs must be updated to **v3.25** or greater before you can configure CDN streams or they _must _ be set to **Inactive** status if they do not have v3.25 or greater installed."
  },
  "cols": 2,
  "rows": 4,
  "align": [
    "left",
    "left"
  ]
}
[/block]


When the DME is saved or updated:

- An **RTMP ** stream is created and enabled using the provided stream name.
- An **RTSP **stream is created and enabled using the provided stream name.

If the additional checkboxes are enabled (VBM / HLS / CDN):

- If **Vbrick Multicast** is enabled, a Multicast stream with -VBM appended is created.
- If **HLS **is enabled, an HLS stream is created and enabled using the stream name.
- If CDN distribution was enabled for Rev events, the CDN HLS stream will be visible and using your stream name.

Some of these are displayed in the image below.  Corresponding playback URLs are also shown.  In some cases, as with Stream Lockdown, the playback URLs will not work outside the context of a Vbrick player.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d26767e-dynamicStreamsCreated.png",
        "dynamicStreamsCreated.png",
        902
      ],
      "align": "center",
      "caption": "Saving or updating the DME device creates the streams for you based on what checkboxes you have enabled"
    }
  ]
}
[/block]


> ❗️ Warning!
> 
> If for any reason one or more of the URLs cannot be created, none of the URLs will be created and an error message will be displayed.

**Presentation Profiles** and **Zones **also list the different available streams created to select as Viewing Destinations.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/093d62d-addStreamsToDevices.png",
        "addStreamsToDevices.png",
        902
      ],
      "align": "center",
      "caption": "Move created streams to the Selected Streams box on Presentation Profiles and in Zones to use them"
    }
  ]
}
[/block]


### Add a Manual Stream

The **Advanced **tab is used to link existing streams with stream names for playback URLs in Rev.  These are stream URLs that are associated with a stream name that can be used within **Presentation Profiles** and **Zones **for distribution. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d78b764-manualVideoStream.png",
        "manualVideoStream.png",
        1659
      ],
      "align": "center",
      "caption": "Click the Advanced tab to manually add a video stream to the DME"
    }
  ]
}
[/block]


Click the **Add URL** button to add a new stream.

[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Descriptioin",
    "0-0": "Name",
    "0-1": "This is the stream name. The stream name must be unique within the DME that you are currently adding. If you are setting up several DMEs to distribute the same stream, consider a naming scheme using the same stream name as a prefix within the name across each DMEs so that you can easily trace the stream.  \n  \nStream names must be alphanumeric and contain no spaces. Stream names are not case sensitive.",
    "1-0": "URL",
    "1-1": "The URL of your video stream. Copy the source URLs to this field.",
    "2-0": "Encoding Type",
    "2-1": "The encoding type that will be used; select from the drop-down menu.",
    "3-0": "Is Multicast",
    "3-1": "Select if your video will be multicast."
  },
  "cols": 2,
  "rows": 4,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Add a Custom Device Stream

You may also add a manual stream from an existing [Custom Device](doc:add-a-source-or-custom-device) you have configured. This creates a link from the custom device to the DME so that Automatic Multicast and Reflection of an external stream can be utilized.

**View**: [Automatic Multicast and Reflection](doc:automatic-multicast-and-reflection) > [Custom Device Streams](doc:automatic-multicast-and-reflection#use-automatic-multicast-with-custom-devices)