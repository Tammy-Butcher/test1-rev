---
title: Auto Multicast and Unicast for Cloud Streams
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
A DME may be configured to automatically create a **Vbrick Multicast** version *and/or* provide an HLS unicast MBR version (reflection) specifically for Cloud-sourced events or webcasts (such as from RTMP ingest or Video Conferencing Integration (VCI) streams). These abilities are identified within each DME as special streams named **Auto Multicast for Cloud Streams** and **Auto Unicast for Cloud Streams**. This means that these DMEs may be included within particular **Zones** with these special streams to provide increased capabilities for shaping distribution.  

> 👍 Tip
>
> As best practice, please keep your DMEs and Vbrick Multicast Agent at the most current supported version.  DMEs must be **v3.23+** (preferably higher) and viewers must be using the [Vbrick Multicast Agent](https://portal.vbrick.com//doc/PDFs/REV/Vbrick%20Multicast%20Install%20Quick%20Reference.pdf) **v1.2+** (preferably the most recent version) to receive the multicast within their browsers.

Automatic multicast and reflection *greatly* expands the reach of your Cloud-sourced events and Webcasts. This capability includes all RTMP ingest, WebEx Live, and all [Vbrick video conference integrations](doc:video-conference-vc-integrations).

## Auto Unicast for Cloud Streams

By default, each DME is already configured and will have the **Auto Unicast for Cloud Streams** as a selectable stream for your distribution configuration.  Further, by default, **Auto Unicast for Cloud Streams** will be included as a selected stream (both for existing configurations, and going forward it will be added to the **Selected Streams** within a **Zone** if the DME is selected.)  

This stream, within a DME and selected for use within a Zone, allows Rev to provide **HLS MBR** unicast streams (for Cloud-sourced events, but pulled into the DME and provided locally) to players.  This reduces your ingress bandwidth greatly by providing the unicast MBR stream from the DME (pulling from the Cloud and saving corporate <Glossary>bandwidth</Glossary>).  **Auto Unicast for Cloud Streams** does *not* require multicast settings.

Additionally, each Zone can specify which of the renditions will be served to viewers. (Each bitrate stream within the HLS MBR is a **rendition**.) Please review [Adding a new Zone](doc:add-a-zone#zone-details) for additional details.

## Auto Multicast for Cloud Streams

In addition to **Auto Unicast for Cloud Streams**, DMEs can be configured to create a multicast streams from a Cloud-sourced event/webcast by use of the stream named **Auto Multicast for Cloud Streams**.  This stream, within a DME and selected for use within a Zone, allows Rev to direct the DME to pull the stream and generate multicast for our Vbrick Multicast agent to receive (and playback within the viewers' browsers).  This approach reduces both your LAN and ingress <Glossary>bandwidth</Glossary> usage.

> 📘 Note
>
> If both **Auto Multicast for Cloud Streams** and **Auto Unicast for Cloud Streams** are configured, then viewers/browsers within the Zone who cannot take advantage of multicast will fall back and receive a *reflected* unicast MBR stream from the DME.

## Initial Multicast Configuration

*Before* you configure automatic multicast and/or reflection for your DMEs in Rev:

1. Make sure all multicast viewers have (at the very least) **VBM Agent v1.2+** installed and have an valid security certificate (included within the install, but can be customized per account.)  **Vbrick strongly recommends that you use most recent version of VBM.**  Also, keep in mind and plan for the fact security certificates have limited **expiry date**.

2. Coordinate with your Network Administrators to get a block of **Multicast IP Addresses** (you need this to configure it in Rev).

3. Enable and configure **Auto Multicast for Cloud Streams** settings on the appropriate **DME(s)**.  (See definitions of fields below.)

4. Once the DME is enabled for **Auto Multicast for Cloud Streams**, Rev can be configured in two ways:
   * Utilize **Auto Multicast for Cloud Streams** for live, Cloud-sourced streams
   * Use a **Custom Device** and automatically multicast **3rd party HLS streams** through a **Presentation Profile**.   

Each method is described in more detail below.

> 👍 Tip
>
> If you do not see the **Enable Automatic Multicast for Cloud Streams** checkbox, make sure that the DME Device you are configuring has the v3.23+ build installed and that VBM v1.2+ is also installed on the viewer's machine.

<Image title="enableAutomaticMulticast.png" alt={1133} align="center" src="https://files.readme.io/edb0618-enableAutomaticMulticast.png">
  You must have the correct DME and VBM software builds installed before this setting is visible in a DME Device
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
        Multicast IP Addresses
      </td>

      <td>
        Enter the range of **IP Addresses** (IPv4, IPv6, ranges or CIDR) for use during Automatic Multicasting. Best practices for assigning are described below.  

        Note that every DME that enables this feature requires a set of multicast addresses. These are the addresses that Rev assigns to each new automatic multicast as they are created. Rev keeps track, and does not distribute duplicate multicast addresses within an account. Best practices is to provide a large number of multicast addresses.
      </td>
    </tr>

    <tr>
      <td>
        Port / Port Range
      </td>

      <td>
        Enter a single port or range of ports.\
        Best practice is to enter a **single port**. This is because if there are two different multicast streams on a given multicast IP with different ports, then each device (think router, switch, or end consumer) has to receive the two streams. This creates unnecessary overhead. Therefore, while multiple ports are supported, best practice is to use one port and provision many multicast IPs.  

        For simplicity, Vbrick recommends the default value: `4444`
      </td>
    </tr>

    <tr>
      <td>
        Packet Size
      </td>

      <td>
        Set the **packet size** for the multicast. This is an advanced feature and the recommendation is to accept the default.  

        The default value: `4096`
      </td>
    </tr>

    <tr>
      <td>
        Rendition Selection for Auto Multicast for Cloud Streams
      </td>

      <td>
        When the DME pulls a remote HLS stream (either for Video Conference streams or 3rd party HLS), it must decide which rendition or specific bitrate to convert to multicast.  A multiple bitrate (MBR) stream can have a number of bitrates to choose from. This setting, which applies to all automatic multicast generated from this DME, defines which rendition.  

        If the HLS stream has only one rendition, it is used.  Otherwise, it will use either the **High Bitrate** or **Low Bitrate** rendition based on this setting.  

        If you need to separate HLS into multiple different automatic multicasts based on bitrate, then the best practice is to set up different DMEs – one to always generate **High Bitrate** multicast, and the other to generate **Low Bitrate** multicast.  This is because only one rendition can be selected to automatically multicast and this setting applies to *all* streams automatically multicast from this DME.  

        Please review the use of these DMEs within the appropriate zones and use the Automatic Multicast stream from each DME accordingly.  

        This is not to be confused with the Zone based rendition selection for unicast -- these are two very different features.
      </td>
    </tr>
  </tbody>
</Table>

## Multicast Address Assignment - Best Practices

Many factors must be considered when designing a multicast address infrastructure since Ethernet switch implementations can significantly vary between vendors. Furthermore, multicast addressing techniques rely on an Ethernet to IP Address mapping rule, which does not guarantee a unique physical address. In fact, it is possible to create multicast addresses that differ from an IP perspective, but overlap when presented to the Ethernet network. Addresses created in this situation can cause significant network and operational problems.

Specifically, multiple IP Addresses are mapped into the same physical layer address. For example, all IP multicast addresses with the same or differing first octet, and the second octet differing by exactly 128, map to the same physical address (`226.5.5.4`, `227.5.5.4`, and `228.133.5.4` all map to the same physical address).

Another factor to keep in mind when assigning multicast addresses is that `224.x.x.x` is a range containing reserved addresses, particularly in the range `224.0.0.x`. For example, `224.0.0.1` is the 'all hosts' multicast address and `224.0.0.2` is the 'all routers' reserved address. Other `224.0.0.x` numbers are reserved for RIP, OSPF, DVMRP, etc. Here are some recommended rules for multicast IP Address assignment:

1. Do not use 224 in the first octet since many of these are reserved. (Vbrick encoders enforce this rule.)

2. Use a digit between (225–239) for the first octet and standardize it for each network.

3. In the second octet, either use numbers from 1–127, or 129–255, do *not* mix ranges on a given network.

> 👍 Use Case Example
>
> Random range within the 239 space.
>
>    `239.110.1.0-239.110.1.255` 
>
> * This range provides for 255 multicast addresses. (Depending on the number of simultaneous multicast streams you have.) 
> * Best practices is to provision many multicast addresses (they are not used until needed) and are recycled after use. 
> * For simplicity of network administration and stream identification, if you have multiple DMEs generating automatic multicast streams, you can use the same range and Rev provisions unique addresses (within that range) each time. 
> * Make sure you work with your Network Administrator to receive the block of multicast addresses.

## Use Automatic Multicast with Video Conferences

To use automatic multicast with **Live Video Conference streaming**, configure streams as you normally on the DME by enabling **Vbrick Multicast** when you add a video stream. Now every VCI stream is automatically multicast from the DME. 

**Zones** that have multicast viewers should also include the DME with multicast enabled as a destination (and the stream title **Automatic Multicast**). These Zone then use that DME for multicast.

**View**: [Add a Dynamic Stream](doc:manage-dme-devices#section-add-a-dynamic-stream)

## Use Automatic Multicast with Custom Devices

You can also configure custom **HLS URLs** to be used for Automatic Multicast and Reflection by associating a **Custom Device** (which has these HLS URLs) with the DME. These streams can then be utilized in a **Presentation Profile** to for reflection and automatic multicasting during a Webcast. This means you can allow 3rd party HLS streams (and encoders) to utilize the automatic multicast feature.

> 🚧 Important!
>
> There are some HLS streams and tags that are *not* supported.  View the DME Help topic, **Rev Initiated Multicast and Reflection**.

To configure Automatic Multicast streams on a DME:

1. Click the **Custom Devices** tab in the **Video Streams** section.

2. Click the **Add Custom Device** button and complete the selections as follows.

<Image title="customDevicesTab.png" alt={802} align="center" src="https://files.readme.io/6539e6e-customDevicesTab.png">
  The Custom Devices tab is available on DME Devices that have DME v3.23+ installed
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
        Select Custom Device
      </td>

      <td>
        * \*Custom Devices\*\* already created appear in the dropdown. Only HLS streams can be used for this feature so the Custom Device must also have one or more HLS streams.  
        * \*View\*\*: [Add a Custom Device](doc:add-a-source-or-custom-device#add-a-custom-device)
      </td>
    </tr>

    <tr>
      <td>
        Select Stream Name
      </td>

      <td>
        Each stream has a unique name (when you created the Custom Device). Here you select the appropriate name for the URL stream you want to use for multicast and/or reflection. Custom Devices can contain multiple HLS streams.  

        Note that you may *not* use the same name more than once.
      </td>
    </tr>

    <tr>
      <td>
        Enable DME Reflection
      </td>

      <td>
        Select this checkbox if you want the DME to reflect the stream(s). Clicking this creates a new stream in the DME (the name is listed within the user interface.)  

        This stream *must* be included within the **Presentation Profile** (with the DME as the destination) to generate automatic reflection through the DME.  

        Including the Custom Device as a destination within the Presentation Profile uses the stream(s) as it does today – unicast.  

        * \*Not&#x65;**: At least one of the**Enable DME Reflection or Enable Automatic Multicast\*\* checkboxes *must* be selected.
      </td>
    </tr>

    <tr>
      <td>
        Enable Automatic Multicast during webcast
      </td>

      <td>
        Select this checkbox to enable automatic multicasting during Webcasts.  Clicking this creates a new stream in the DME (the name is listed within the user interface.)  

        This stream *must* be included within the **Presentation Profile** (with the DME as the destination) to generate automatic multicast from this DME.  

        Including the Custom Device as a Destination within the Presentation Profile will use the stream(s) as it does today – unicast.  

        * \*Not&#x65;**: At least one of the**Enable DME Reflection or Enable Automatic Multicast\*\* checkboxes *must* be selected.
      </td>
    </tr>
  </tbody>
</Table>

## Add Automatic Multicast and Reflection Streams in Zones

After you have set up your Rev devices, make sure the **Supports Multicast** checkbox is selected on your Zone(s) to enable selection of your DME configured for automatic multicast. Those streams that you enabled for automatic multicast and reflection are now available.

<Image title="autoMulticastStreamedZones.png" alt={722} align="center" src="https://files.readme.io/4f395d9-autoMulticastStreamedZones.png">
  Automatic Multicast streams are noted by a distinct icon in Rev Zones
</Image>
