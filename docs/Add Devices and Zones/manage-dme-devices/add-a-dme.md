---
title: Add a DME
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
Account Admins can add DMEs to Rev through the **DME Management** module by clicking the **Add DME** button.  This brings up the **Add a DME** page which allows the initial configuration of a DME.   Not all configurations of a DME can be set during an **ADD** -- only the most common settings are initially displayed.  After *adding* the DME to Rev, if you click on its name you are then presented with a *full* list (common and uncommon) of configurable DME settings at that time.

To add a new DME to Rev:

1. Navigate to **Devices** > **DME Management** > **Add DME**.

2. Complete the field or setting(s) described below as needed or required.

<Image title="addDme.png" alt={802} align="center" src="https://files.readme.io/f6aae6b-addDme.png">
  Click the Add DME button from the DME Management module to add the device to Rev
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
        Device Name
      </td>

      <td>
        This can be a name of your choosing. This is a required field.  

        If you will have multiple DMEs (common), then it is recommended that you develop a naming scheme.  A name containing the location or Host name/FQDN is recommended.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        The status of your device may be set to **Active**or **Inactive**.  

        * \*Active**DMEs will, if configured within**Zon&#x65;**, be used for distribution.**&#x49;nactive**DMEs will not be used when Rev generates playback URLs, but may continue to be used in a DME Mesh or shared cache scenario.  If you do not want your DME used at all, it is recommended that you**Inactive\*\* it and turn it off.
      </td>
    </tr>

    <tr>
      <td>
        MAC Address
      </td>

      <td>
        The MAC Address is required. A quick way to find a DME's MAC Address is to log-in to the DME and navigate to **System Configuration** > **Activate Feature**.  The MAC Address is displayed there.
      </td>
    </tr>
  </tbody>
</Table>

![](https://files.readme.io/7019a80-storageCheckboxes.png "storageCheckboxes.png")

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
        VOD Playback Device
      </td>

      <td>
        This checkbox is selected by default and enabled if the DME is to be used as a **Video on Demand (VOD) playback device** for serving stored video content.  

        If more than one DME is designated as storage, then content is pushed to *all* designated DMEs.  

        If this box is not selected, then this DME will be **primarily** used for Live distribution.  Addition configuration may be necessary depending on use case.
      </td>
    </tr>

    <tr>
      <td>
        Preposition Content
      </td>

      <td>
        This checkbox specifies which DMEs on the network receive [prepositioned video](doc:add-a-dme#preposition-dme-content-downloads) files for playback; should *only* be used if you are also using **MESH**.  

        You can also then set your **download schedule** which becomes visible.  

        Note:  By default this feature is disabled.  There are several different models of caching (see below) that will get content onto DMEs.  Vbrick recommends that you have all your DMEs on v3.29 (or above) and utilize direct VOD caching (i.e., disable this feature).  This eliminates the timing delay necessary  for downloading large files.
      </td>
    </tr>

    <tr>
      <td>
        Video Streams
      </td>

      <td>
        * \*Nam&#x65;**,**&#x55;R&#x4C;**,**&#x45;ncoding Typ&#x65;**, and**Multicast **are all designated \[through the**Advanced **tab >**&#x41;dd URL**button if adding manually] and are required fields if the DME is intended to be utilized as a**streaming**device.   These streams are later selected on**Presentation Profiles**and**Zones **as viewing destinations.  Additionally, you may also generate your URLs*dynamically* through the **&#x43;reate URLs\*\* tab.  You may set these now, or return to the DME edit page to set then later.  

        Note:  In order to playback streams using **HTTPS** within our Rev HTML5 player it is necessary for your DME to have a **Fully Qualified Domain Name (FQDN)** .  This is **highly recommended** and best practices for enterprise-level security postures.  Additionally, that **FQDN** is necessary for Certificate Requests (either in-whole or in-part as with a wildcard CERT.)  Note: DME v3.10 and greater devices are capable of registering **fully qualified domain names** in order to play HTTPS content to the Rev HTML5 video player. Therefore, DME streaming URLs may or may not contain an IP address Hostname.  

        View: [Add DME Video Streams](doc:add-a-dme#add-dme-video-streams) for more details and examples.
      </td>
    </tr>
  </tbody>
</Table>

3. After each setting is configured, click the **Create** button to add the DME Device.

4. The DME  status state should flip from **Uninitialized** to **Active** after a few seconds. If it does not, check your **MAC Address** field and/or the DME initial configuration steps such as the API Key and Host fields. **View**: [Getting Started - Devices](doc:getting-started-with-rev-devices) 

5. Once status is **Active**, the DME is ready to use with your Rev portal.

6. Account Admins are sent an email notification if any DME goes into **Warning** or **Offline** status so that they may pro-actively troubleshoot it.

## DME Caching Methods Explained

At the heart of the DME is a shared caching system -- distributed across all connected DMEs.  There are several ways to get content into those caches which we discuss here.

To understand the caching models, it is useful to understand the general playback flow utilizing Rev.  When a viewer's browser requests playing a video it is provisioned a number of playback URLs from Rev.  These playback URLs are Zone specific, meaning if viewers are in different Zones they may get different URLs.  In other words, Rev will provide URLs that point the DMEs within the viewer's Zone.  The player reaches out to the DME for the video, and the DME will attempt to service that request.

### The Ultimate Fallback Method (Legacy)

The **Ultimate Fallback** feature is a legacy feature that allowed the player to request content from a local DME (and the DME Mesh) and, failing that, fell back to retrieving content from Rev.  In this legacy use case, the player requested the content from the local DME.  The local DME did not have the content, so all the "sisters" (or peer) DMEs were queried for the content.  If none of the "sisters" had it, and the requesting DME did not have it, then the request failed back to the player.  The player then played back from Rev (Cloud).  At this point, however, the requesting DME (who did not have the content) requested the content from Rev.  Rev provided the content to the requesting DME and all other DMEs were set as pre-positioned.  The next requestor received the content from the DME or DME Mesh.

### The First-Time VOD Caching Method (Recommended)

Beginning with Rev v7.53 and DME 3.29 the system utilizes a new caching method called **First-Time Caching VOD Caching**. The DME will no longer fallback but instead retrieves the VOD HLS *piece* to service the request (and does not request the entire VOD.) This piece is then in the DME's cache going forward. This feature begins to remove the dependency on "ultimate fallback" and the DME acts more like a caching engine and treats VOD assets individually. You can still manually preposition, you can still set up preposition, but our recommendation is to no longer do this with our new caching algorithm.

> 👍 Tip
>
> If you are using **Prepositioned Content**, you should make sure that all DMEs in your network are able to communicate with at least *one* DME that has *all* prepositioned content.  
>
> If you are not using **Prepositioned Content**, then requests that go to DMEs will utilize the **DME Mesh** and **Ultimate Fallback** but *only* if you are using DMEs that are not upgraded to **v3.29+**.  Playback will continue and content that is viewed will still make its way onto DMEs for local serving.  Having DMEs that are highly connected will optimize the use of the **DME Mesh** or **Ultimate Fallback**.
>
> DMEs that are upgraded to v3.29+ now use **First Time VOD Caching** instead which is much more efficient.

## Preposition DME Content Downloads

Even with  **First-Time Caching VOD Caching** or **Ultimate Fallback**, there are use cases that requires content initially resident on DMEs.  This is called prepositioning and is set at the DME level.

You can designate which DMEs in your video ecosystem have content prepositioned immediately (downloaded to the DME immediately after upload) or schedule content (by day of the week and time) by selecting the **Preposition Content** checkbox. This option is only available for DMEs that are also selected as a **VOD Playback Device**.

> 📘 Note
>
> This feature is used with the DME's Mesh caching configuration View the [Mesh with Rev Caching Configuration](https://dmedocs.vbrick.com/docs/rev-mesh-caching-configuration) topic in DME Online help.

Rev uses [zone logic](doc:add-a-zone#zone-logic-flow) to route content requests by users to the closest DME. If the DME closest to the user does not have the requested content (either in the cache or on the disk), *that* DME requests the content from all “sister” DMEs (peer DMEs that are reachable). 

If the content is available (the DME uses the first "sister" that responds), then the content is retrieved from that "sister" and cached on the requesting DME.  It is now cached and available for the *next* user requesting it (with no need to go back out to all other DMEs). 

Initially, the only “sister” DMEs that have the content are the prepositioned DMEs. Subsequently, as the content becomes available on more DMEs based on user content requests, *any* DME that has cached a copy of the content becomes a sister DME that other DMEs can then retrieve content from.

This means that content is only pushed to a handful of DMEs initially, so *fewer* downloads are pushed through the cloud and into the network for Rev Cloud customers.

To preposition DME content and schedule downloads, make sure both the **VOD Playback Device** and **Preposition Content** checkboxes are selected.  Both are required.

<Image title="prepositionContent.png" alt={907} align="center" src="https://files.readme.io/6dd66ad-prepositionContent.png">
  The Scheduled Download control appears when the Preposition Content checkbox is selected
</Image>

The **Scheduled Download** control appears when the **Preposition Content** checkbox is selected. This allows you to specify when this DME receives video files so that network traffic is managed by timezone, day of the week, and even by the hour if necessary. 

The example DME schedule above only has video pushed to it on Saturday and Sunday between the hours of 3:00 a.m. and 7:00 a.m. eastern time.

> 👍 Tip
>
> If no schedule is set, content is always pushed to the DME as soon as it is finished transcoding.
>
> You can also *choose* how content is synced once the DME is added and saved; immediately or scheduled. **View**: [Synchronize DME Content](doc:manage-dme-devices#synchronize-dme-content)

There are several instances where a DME will trigger a **Rev Mesh** update. They are:

* If any DME reports a new **Hostname** or **IP** to Rev
* If any DME reports a new **software version** number (including **build**)
* If any DME reports a change in **http / https serving status** to Rev
* If any DME **preposition status** is changed (enabled or disabled) on Rev
* If any DME status ( **Active**or **Inactive**) is modified
* If any DME **VOD Playback Device** setting or status is modified

## Configure DME Specific Multicast Settings

The following settings allow configuration of DME specific multicast settings.  Again, this requires the [Vbrick Multicast Agent](https://portal.vbrick.com//doc/PDFs/REV/Vbrick%20Multicast%20Install%20Quick%20Reference.pdf) be installed on the viewer's PC or Mac.

<Image title="dmeFecSettings.png" alt={1306} align="center" src="https://files.readme.io/dd7a36e-dmeFecSettings.png">
  When VBM is installed on a viewer's PC or Mac, you can configure DME specific multicast settings
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
        Customized FEC Settings
      </td>

      <td>
        Allows the selection of an FEC level (different from the account FEC level set on the [Security](doc:dme-and-vbrick-multicast-security#vbrick-multicast) page).  Modifying this changes the FEC used for VBM streams configured at Rev as well as cloud ingested (VCI/RTMP) multicast streams.  

        Reminder:  This feature is only available if the account has enabled [Encryption](doc:dme-and-vbrick-multicast-security#enable-vbrick-multicast-encryption).
      </td>
    </tr>

    <tr>
      <td>
        Enable Auto Multicast for Cloud Streams
      </td>

      <td>
        Sets the DME to provide streams that can be used in **Zones** and **Presentation Profiles** that will automatically pull cloud based streams (VCI/RTMP) and configured custom devices when using the stream **Auto Multicast for Cloud Streams**.
      </td>
    </tr>

    <tr>
      <td>
        Multicast IP Addresses
      </td>

      <td>
        A set of addresses (within the local multicast IP range) that will be used for multicast streams.  These IP ranges are specific and should be provided by your IT/Networking group.  (Do not make these IPs up or chose your own, as you may stomp over another existing stream.)
      </td>
    </tr>

    <tr>
      <td>
        Port / Port Range
      </td>

      <td>
        Ports that will be combined with the Multicast IP Addresses.  It is recommended that only ports (and not Port Ranges) are used.
      </td>
    </tr>

    <tr>
      <td>
        Packet Size
      </td>

      <td>
        The size of the multicast packets.  Recommendation is 4096.
      </td>
    </tr>

    <tr>
      <td>
        Rendition Selection for Auto Multicast for Cloud Streams
      </td>

      <td>
        Renditions are the different bitrate streams within a multi-bitrate (MBR) stream.  

        The origin cloud stream is typically an MBR stream but only one bit rate will be used for multicasting.  This setting controls whether the DME will use the highest or lowest bit rate from the origin MBR to create the multicast stream.  

        Note that only one rendition may be selected and it applies to all auto multicast streams created by this DME.
      </td>
    </tr>
  </tbody>
</Table>

## Add DME Video Streams

DMEs are caching and streaming edge-devices deployed on customer networks where content is distributed and viewed.  One of Rev’s primary capabilities is to provide live streaming out to player pages – and it does that through mapping named streams through its distribution configuration.  Meaning, these named streams are used within [Presentation Profiles](doc:add-a-presentation-profile) and [Zones](doc:manage-and-add-zones) to control and define where the streams are provided.

Named streams are specified within the Rev **DME Management** module.  Administrators are able to create named streams that represent physical streams on each DME.  This means a stream called <code>StreamExample</code> could be defined on Rev.  That <code>StreamExample</code>, and its different flavors of distribution (**RTMP**, **RTSP**,  **Multicast**, etc.), are then specified within **Presentation Profiles** and **Zones**.  A stream that matches that name still needs to be provisioned within the DME itself (as either a push or pull from a source.)

Video streams on a DME are set up manually or dynamically by the DME itself. There are several methods to creating named streams (outlined below).  These include: 

* Creating them dynamically for **CDN** distribution
* Creating them manually by providing a source URL
* Utilizing saved [Custom Device](doc:add-a-source-or-custom-device) streams

> 📘 Note
>
> An **RTSP** unicast stream is required for recording live webcasts in Rev. Make sure that your stream has a keyframe interval between 2 to 5 seconds and do *not* use B-frames. 
>
> Please see your individual Encoder (stream source) documentation for setting information.

### Add a Dynamic Stream

The **Create URLs** tab under **Video Streams** is used to create your own dynamic named streams for playback URLs in Rev. 

> 🚧 Important!
>
> CDN streams are added dynamically at the start of the event.  AWS is used for CDN distribution for customers.  Contact Vbrick Support if you need assistance.

Click the **Add URL** button to add a new stream.

<Image title="dynamicVideoStream.png" alt={902} align="center" src="https://files.readme.io/898490b-dynamicVideoStream.png">
  Click the Create URLs tab to dynamically generate a video stream
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
        Name
      </td>

      <td>
        This is the stream name. The stream name must be unique within the DME that you are currently adding. If you are setting up several DMEs to distribute the same stream, consider a naming scheme using the same stream name as a prefix within the name across each DMEs so that you can easily trace the stream.  

        Stream names must be alphanumeric and contain no spaces. Stream names are not case sensitive.
      </td>
    </tr>

    <tr>
      <td>
        Enable Vbrick Multicast
      </td>

      <td>
        Select if you want to enable Vbrick multicast streams. You must have DME software v3.18 or greater before this may be configured.  

        Once selected, enter the following to automatically configure Vbrick multicast streams:  

        * **Multicast IP Address**: (required) Must between <code>224.0.0.0</code> and <code>239.255.255.255</code>  
        * **Multicast Port**: Default is <code>4444</code>  
        * **Packet Size**: (entry 1000 to 8192) in Bytes, default: <code>4096</code>  

        Please note that the IP Address and Port cannot be duplicated across multiple streams.  Consult your Networking/IT department for appropriate address.  

        HLS streaming options are independent of Vbrick multicast streams  

        If the IP Address, Port, or Packet Size values fail, Rev displays a configuration failure message and requests that you edit the values again.  

        Viewers PC/Mac must have the **Vbrick Multicast Agent** installed to receive the streams.
      </td>
    </tr>

    <tr>
      <td>
        Enable HLS generation
      </td>

      <td>
        Select if you want to create an HLS stream. This is required for mobile devices. The default is no.
      </td>
    </tr>

    <tr>
      <td>
        Enable CDN distribution during Rev Event
      </td>

      <td>
        You must have the **Enable HLS generation** checkbox enabled before this becomes visible.  

        Your DMEs must be updated to **v3.25** or greater before you can configure CDN streams or they *must* be set to **Inactive** status if they do not have v3.25 or greater installed.
      </td>
    </tr>
  </tbody>
</Table>

When the DME is saved or updated:

* An **RTMP** stream is created and enabled using the provided stream name.
* An **RTSP** stream is created and enabled using the provided stream name.

If the additional checkboxes are enabled (VBM / HLS / CDN):

* If **Vbrick Multicast** is enabled, a Multicast stream with -VBM appended is created.
* If **HLS** is enabled, an HLS stream is created and enabled using the stream name.
* If CDN distribution was enabled for Rev events, the CDN HLS stream will be visible and using your stream name.

Some of these are displayed in the image below.  Corresponding playback URLs are also shown.  In some cases, as with Stream Lockdown, the playback URLs will not work outside the context of a Vbrick player.

<Image title="dynamicStreamsCreated.png" alt={902} align="center" src="https://files.readme.io/d26767e-dynamicStreamsCreated.png">
  Saving or updating the DME device creates the streams for you based on what checkboxes you have enabled
</Image>

> ❗️ Warning!
>
> If for any reason one or more of the URLs cannot be created, none of the URLs will be created and an error message will be displayed.

**Presentation Profiles** and **Zones** also list the different available streams created to select as Viewing Destinations.

<Image title="addStreamsToDevices.png" alt={902} align="center" src="https://files.readme.io/093d62d-addStreamsToDevices.png">
  Move created streams to the Selected Streams box on Presentation Profiles and in Zones to use them
</Image>

### Add a Manual Stream

The **Advanced** tab is used to link existing streams with stream names for playback URLs in Rev.  These are stream URLs that are associated with a stream name that can be used within **Presentation Profiles** and **Zones** for distribution. 

<Image title="manualVideoStream.png" alt={1659} align="center" src="https://files.readme.io/d78b764-manualVideoStream.png">
  Click the Advanced tab to manually add a video stream to the DME
</Image>

Click the **Add URL** button to add a new stream.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field or Setting
      </th>

      <th>
        Descriptioin
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Name
      </td>

      <td>
        This is the stream name. The stream name must be unique within the DME that you are currently adding. If you are setting up several DMEs to distribute the same stream, consider a naming scheme using the same stream name as a prefix within the name across each DMEs so that you can easily trace the stream.  

        Stream names must be alphanumeric and contain no spaces. Stream names are not case sensitive.
      </td>
    </tr>

    <tr>
      <td>
        URL
      </td>

      <td>
        The URL of your video stream. Copy the source URLs to this field.
      </td>
    </tr>

    <tr>
      <td>
        Encoding Type
      </td>

      <td>
        The encoding type that will be used; select from the drop-down menu.
      </td>
    </tr>

    <tr>
      <td>
        Is Multicast
      </td>

      <td>
        Select if your video will be multicast.
      </td>
    </tr>
  </tbody>
</Table>

### Add a Custom Device Stream

You may also add a manual stream from an existing [Custom Device](doc:add-a-source-or-custom-device) you have configured. This creates a link from the custom device to the DME so that Automatic Multicast and Reflection of an external stream can be utilized.

**View**: [Automatic Multicast and Reflection](doc:automatic-multicast-and-reflection) > [Custom Device Streams](doc:automatic-multicast-and-reflection#use-automatic-multicast-with-custom-devices)
