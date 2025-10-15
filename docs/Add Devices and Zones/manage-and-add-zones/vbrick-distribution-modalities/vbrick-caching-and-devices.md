---
title: Devices
excerpt: >-
  This topic provides an overview of how to enable and configure Vbrick caching
  devices (DMEs) and streams in a zone.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Add Devices to a Zone

The **Devices**  section allows the specification of what type of device and streams to use in the zone.  If your Account Admin enables the [Vbrick Universal eCDN](doc:ecdn-options) option, you also have access to the **Vbrick Universal eCDN** streams which allows the use of **Vbrick Peer-to-Peer** for caching and distribution with your zone. 

<Image alt="Select a Device in the dropdown and then choose Available Streams to add to the Selected Streams column for Users to access in the Zone" align="center" src="https://files.readme.io/aae1b1c-vbrickECDNDevices.png">
  Select a Device in the dropdown and then choose Available Streams to add to the Selected Streams column for Users to access in the Zone
</Image>

Add **Devices** to your **Zones** by selecting a device in the dropdown under the **Selected Streams** section.  Use the **Available Streams** and **Selected Streams** to choose which **Viewing Destinations** are available to **Users** in the Zone.

* **Live Only** - Select this checkbox if you want to configure a DME Device as a **Live Only DME**. This option is disabled by default.  **Note**: This is a Rev restriction only. This means that Rev will not direct players to retrieve VOD directly from this DME. However, please note that the DMEs will continue to operate and share within the DME Mesh as currently designed.
* **Available Streams** - Streams available on the device that are specified as Viewing Streams. Click to add it to the Selected Streams column. It is then used as a Viewing Stream in the Zone by Users.

> 📘 Note
>
> Streams are only loaded or created when you click the **Customize** button. This is to support efficient loading for those devices that have several streams.

* **Selected Streams** - Streams that are selected as Viewing Streams from the Device on the Zone. Note: When using a Custom Device based on Automatic Multicast, only select one to be used PER DME. You can include multiple DMEs (as destinations) each with a single associated Custom Device for any load balancing or multicast network bifurcation needs.
