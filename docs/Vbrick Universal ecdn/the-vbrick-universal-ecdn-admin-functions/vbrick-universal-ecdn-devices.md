---
title: Vbrick Universal eCDN Devices
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
The **Devices** option under the Admin menu consists of the supported devices the Account Admins can manage in the Vbrick Universal eCDN.  Most settings here directly mirror Rev settings unless otherwise noted.

> 👍 Tip
> 
> This is only a brief introduction.  Please make sure to review the **More Details** links in each of the following sections.

## Add a DME to Vbrick Universal

DMEs are added as a **Device** and are designated as the **Viewing Destinations** of your video streams on the eCDN.

The **DME Management** menu is where DMEs are added and managed. This module is where most actions and information about your DMEs is conducted and viewed. Account Admins access the DME Management module from **Devices** > [DME Management](doc:manage-dme-devices).

To add a DME to your Vbrick Universal eCDN:

1. Navigate to **Admin** > **Devices** and click the **DME Management** dropdown.
2. Click the **Add DME** button to [add a new DME](doc:add-a-dme) to your eCDN.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d5f2255-addDME.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


**More Details:**

- [Manage and Add DMEs](doc:manage-dme-devices)
- [Add a DME](doc:add-a-dme)

### View DME Network Activity

Use the **Devices** > [DME Network Statistics](doc:view-dme-network-statistics) menu to monitor the overall health, activity, and video usage statistics of each DME in your network. Immediately displayed is health information for each DME including percentages used for **CPU**, **Memory** (including swap space), **Disk space**, and **Throughput**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1fbb3b5-viewDMENetworkActivity.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


**More Details**:

- [View DME Network Statistics](doc:view-dme-network-statistics)

## Add a Presentation Profile to Vbrick Universal

**Presentation Profiles** are used to define **Device** profiles for Webcasts. Account Admins create them to specify video source inputs and destination outputs to easily control devices for an event.

This means that Event Admins and Hosts have a simple and intuitive system already in place when they design and deliver their Webcast Events in the Vbrick Universal eCDN.

To add a **Presentation Profile** to your Vbrick Universal eCDN:

1. Navigate to **Admin** > **Devices** and click the **Presentation Profiles** dropdown.
2. Click the **Add a Presentation Profile** button to [add a new Presentation Profile](doc:add-a-presentation-profile) to your eCDN.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d1c0948-addPresentationProfile.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


**More Details**:

- [Add a Presentation Profile](doc:add-a-presentation-profile)

## Add Source Devices and LDAP Connectors to Vbrick Universal

Use the **Source Devices and LDAP Connectors** module to add, configure, and manage encoders, LDAP connectors, and custom devices.

You often need to have these types of devices added and configured before using them with items such as a Presentation Profile that is used in a Webcast.

To add a **Source Device and/or LDAP Connector** to your Vbrick Universal eCDN:

1. Navigate to **Admin** > **Devices** and click the **Source Devices and LDAP Connectors** dropdown.
2. Click the **Add a Device** dropdown to [add a new source or custom device](doc:add-a-source-or-custom-device) to your eCDN.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/84aa71e-sourceCustomDevices.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


**More Details**:

- [Add an Encoder](doc:add-an-encoder)
- [Add an LDAP Connector](doc:add-ldap-connector-device)
- [Add a Custom Device](doc:add-a-custom-device)

## Add a Zone to Vbrick Universal

Zones are used to create a set of IP address ranges that you then assign specific devices to such as DMEs, Encoders and so forth. This allows you to maintain strict control of your network, bandwidth, and content ingestion by deciding which content is ingested and streamed where on your network.

Zones may also be configured into Vbrick Peer-to-Peer Zones to form peer-assisted, browser-based peer meshes that optimize video retrieval for Live HLS events.

To add a **Zone** to your Vbrick Universal eCDN:

1. Navigate to **Admin** > **Devices** and click the **Zones** dropdown.
2. Click the **Add Zone** button to [add a new zone](doc:add-a-zone) to your eCDN.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3f2915c-addZone.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


**More Details**:

- [Manage and Add Zones](doc:manage-and-add-zones)
- [Add a Zone](doc:add-a-zone)
- [Vbrick Peer-to-Peer Zones](doc:rev-connect-zones)