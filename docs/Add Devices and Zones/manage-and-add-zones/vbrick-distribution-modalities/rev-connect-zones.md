---
title: Vbrick Peer-to-Peer Zones
excerpt: >-
  This topic provides an overview of how to enable and configure Vbrick
  Peer-to-Peer in a zone.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
**Vbrick Peer-to-Peer** (previously referred to as Rev Connect) is a separately [licensed](doc:rev-license-types-and-add-ons), peer-assisted browser-based solution created by Vbrick for **Live Webcasts** sourced from DMEs or CDN. **Vbrick Peer-to-Peer** addresses the problem of reducing ingress bandwidth often seen while distributing Live Webcasts to reduced bandwidth/reduced viewer locations (such as remote offices). Using [WebRTC technology](https://webrtc.org/), the web-based Rev Player downloads the all software and controls as part of the html page -- there is no additional download, installation, or maintenance necessary.  This feature is fully Account administrator-controlled via zone configuration but is limited to **Rev Cloud** or  **Vbrick Universal eCDN** accounts.

Vbrick Peer-to-Peer optimizes distribution within a zone by creating a cooperating set of viewers' browsers. These browsers (using WebRTC data channels) form a **Peer Mesh**. The peer mesh browsers work together to retrieve content and share it in a peer-to-peer manner. 

For example, during an event/webcast, one of the browsers (within the Peer Mesh) retrieves an HLS segment from **origin** (for example, a DME or CDN).  That browser would then share that segment/content with the other browsers (again, all within the Peer Mesh). Those other browsers, depending upon timing, can then also share that content with even more other browsers still within the peer mesh.  

Ultimately, the overall goal is to limit the number of origin retrievals per segment to as few (e.g., 1) as possible. In this way, a peer mesh that supports 25 browsers/viewers retrieves 1 HLS segment for up to 25 viewers (96% reduction in bandwidth for this example.)  We measure, and provide within each event's **Vbrick Peer-to-Peer** report an efficiency, where 100 = 1:1, or 1 unique fetch per each (1) segment (best case) shared across the Peer Mesh.  This efficiency number can be greatly impacted by Zone and physical network configurations.  Given timing, an Administrator should strive for 100 (1:1) to 125 (5:4) efficiency within the Peer Mesh.  This efficiency is measured as a count of origin against all needs -- **Real-Time Analytics** and **Post-Event Analytics** also provide an Efficiency metric tied to bandwidth savings for added detail.

As illustrated, our **Peer Meshes** are collections of cooperating browsers reducing the number of origin requests. To further reduce ingress bandwidth, Vbrick has extended cooperation from inside **Peer Meshes** only, to sharing between Peer Meshes. This is the concept of **Peer Mesh Clusters** -- which are collections (up to 3) of cooperating Peer Meshes within the same zone. Clusters can provide efficiencies from 125 to 200. Meaning, that for 200 measures, the Cluster (75 peers) would go to **origin** 2 times per segment. Put another way, in this example, we would go to origin 2 times to service 75 viewers (greatly amplifying ingress bandwidth savings.) Configuration of Clusters is transparent to the user and administrator. As always, please test within your environment in order to optimize and qualify the ingress bandwidth savings when using Vbrick Peer-to-Peer.

**View**: [Player and Stream Compatibility](doc:supported-player-and-stream-compatibility) for supported browsers.

## Enable Vbrick Peer-to-Peer for a Zone

Enabling Vbrick Peer-to-Peer is a great way to reduce ingress bandwidth for viewers within a zone for **Live Webcast** events.  As viewers request live playback, ** Peer Meshes** are created and populated within the zone when this feature is enabled.  Viewers share amongst themselves, as outlined above, to reduce bandwidth and there may be efficiency impacts based on number and distribution of ** Peer Meshes** and **Peer Mesh Clusters**.

**Step 1. ** On the **Add a Zone** or **Zone Details** page (both are very similar) you must enable **Vbrick Peer-to-Peer**:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b98f215-enableVbrickPeer2Peer.png",
        "slideDelayForHlsVideo.png",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Description",
    "0-0": "Supports Vbrick Peer-to-Peer",
    "0-1": "Visible if account has purchased **Vbrick Peer-to-Peer**. This enacts peer-sharing between browsers in this zone for **HLS Webcasts** and **Video Conferences**.  \n  \nIf this field is not visible, and you believe it should be, please check that your account has both purchased Vbrick Peer-to-Peer licenses -- see [Rev License Types and Add-Ons](doc:rev-license-types-and-add-ons), and that the Vbrick Peer-to-Peer Licenses have been assigned -- see [View and Edit Account Details](doc:view-and-edit-account-details).  \n  \nDisabled by default. If disabled, then this zone will not utilize Vbrick Peer-to-Peer.  \n  \nOnce enabled, the current zone may be configured as a Vbrick Peer-to-Peer zone and additional controls appear.  \n  \n**View**: [Vbrick Peer-to-Peer Zones](doc:rev-connect-zones)"
  },
  "cols": 2,
  "rows": 1,
  "align": [
    "left",
    "left"
  ]
}
[/block]


If Vbrick Peer-to-Peer is not showing, this indicates that your license does not include Vbrick Peer-to-Peer.  Please contact Vbrick Sales or Support for additional details and assistance.

**Step 2: **Once enabled, configure Vbrick Peer-to-Peer for this zone.

Now that you have enabled Vbrick Peer-to-Peer for this zone, you will see additional configurations.  Click the **Supports Vbrick Peer-to-Peer** tab in the **Zone Details** section to configure a Vbrick Peer-to-Peer zone.  Complete the additional options that appear.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/876bd57-vbrickPeer2PeerZoneOptions.png",
        "configureRevConnectZoneOptions.png",
        ""
      ],
      "align": "center",
      "caption": "Additional options to configure a Vbrick Peer-to-Peer zone appear when you enable the Supports Vbrick Peer-to-Peer checkbox"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Option",
    "h-1": "Description",
    "0-0": "Supports Vbrick Peer-to-Peer",
    "0-1": "Visible if the account has purchased Vbrick Peer-to-Peer.  \n  \nIf this field is not visible, and you believe it should be, please check that your account has **both** purchased **Vbrick Peer-to-Peer licenses** -- see [Rev License Types and Add-Ons](doc:rev-license-types-and-add-ons), and that the **Vbrick Peer-to-Peer Licenses have been assigned** -- see [View and Edit Account Details](doc:view-and-edit-account-details).  \n  \nDisabled by default.  If disabled, then this zone will not utilize Vbrick Peer-to-Peer.  \n  \nOnce enabled, the current zone may be configured as a Vbrick Peer-to-Peer zone and additional controls appear.  \n  \nThe default order of **Available Streams** (and enabled) is the following:  \n  \n- Vbrick Multicast (requires VBM agent to be installed)\n- Vbrick Peer-to-Peer (requires licenses applied and available, WebRTC enabled browsers)\n- Unicast Streams",
    "1-0": "Restrict Peer Meshes within IP/IP Ranges",
    "1-1": "Visible when Vbrick Peer-to-Peer is enabled.  \n  \nThis feature (which is one of the more impactful) allows you to control which viewers are added to which Peer Meshes.  This is accomplished based on the zone's IP ranges -- either all viewers within a zone can be peered together (unrestricted) or the viewers can be peered based on each of the zone's IP ranges listed (restricted).  \n  \nIf **Disabled**  (Default), all viewers within this zone can be peered together.  Meaning, that they will be put into the same Peer Meshes (up to the limits).  \n  \nIf **Enabled**, viewers in this zone are eligible to be put into Peer Meshes according to each [line] of the IP Ranges defined for the zone.  This allows zones that can cover several different sub-nets.  However, this has the potential to create multiple Peer Meshes within the zone, which increases ingress bandwidth and can reduce efficiency.  Please review the complete set of your zone IPs before enabling this feature, and consider using additional zones to more fully segment Vbrick Peer-to-Peer viewers for increased efficiency.",
    "2-0": "Fallback to Zone Cache",
    "2-1": "Visible when Vbrick Peer-to-Peer is enabled.  \n  \nThis feature controls the ability for the player to fallback to a **Unicast **stream (if available). If Disabled, the zone only supports **Multicast **or **Vbrick Peer-to-Peer**.  \n  \nThis is useful in the case where you only have enough ingress bandwidth to support the a limited number of Vbrick Peer-to-Peer users.  Meaning, you are trying to optimize the ingress bandwidth to a zone location.",
    "3-0": "Maximum Number of Peer Meshes",
    "3-1": "Visible when Vbrick Peer-to-Peer is enabled.  \n  \nThis allows Administrators to define the **Maximum** number of peer meshes created for the zone.   This is _not_ a reservation, but an **upper limit** on what can be used within the zone based on licensing restrictions for the Rev account.  \n  \nZones enabled for Vbrick Peer-to-Peer are able to concurrently use up to the Account licensed amount of peer meshes. These may be split across several zones. Once at capacity, new viewers/players will fallback to Unicast in accordance to the zone settings.  \n  \n**Setting this to 0 will remove the upper limit.**  \n  \nThis field is required.",
    "4-0": "Use ULS in peer messaging",
    "4-1": "Visible when Vbrick Peer-to-Peer is enabled.  \n  \nVbrick Peer-to-Peer utilizes WebRTC to communicate between peers.  WebRTC uses mDNS between the peers, but mDNS has limitations when spanning sub-nets.  Enabling this feature will direct Rev to securely use the **User Location Service** IP per user vs the mDNS obfuscated IP, and thus support spanning sub-nets.  \n  \nIt is recommended to leave this disabled if your zone does not span sub-nets.  \n  \nDisabled by default.  \n  \nNote: Some cases the Browser can be configured to disable anonymization of IPs which removes mDNS issues, but may introduce PB-based firewall issues. Please test accordingly."
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]


- If a Vbrick Peer-to-Peer zone is used during a Webcast, it is noted in the **Webcast Attendees Report** once the event has ended.
- If you use a Vbrick Peer-to-Peer zone during a Webcast Event, a Vbrick Peer-to-Peer zone report may be downloaded once the event concludes.

## Special Vbrick Peer-to-Peer Considerations in Zone Configurations

**Improve efficiency with a DMEs.**  Efficiency can additionally be improved by adding a DME (configured with **Automatic Unicast for Cloud Streams**) to the same zone as Peer-to-Peer.  In this configuration, peering clients utilize the DME for playback.  The DME goes to origin on their behalf and reduces the bandwidth needs for events with higher numbers of **Peer Meshes** and **Peer Mesh Clusters**.  In other words, there is no sharing between clusters, so by using a DME, we don't have increased origin accesses based on clusters.  Consider using only a single DME within a Vbrick Peer-to-Peer zone, as using multiple DMEs will reduce efficiency by (1) increasing calls to origin, and (2) bifurcating/trifurcating/etc the Peer Mesh limiting sharing.

**Sub-Net Support.**  Peering utilizes WebRTC and peering across sub-nets possibly introduces mDNS issues.

**Allow Lists. ** Vbrick Peer-to-Peer utilizes specific cloud-based URLs to support signaling. Please review your [allow-lists](doc:rev-required-urls-and-allowed-lists) against the URLs.

> ❗️ Warning!
> 
> This is a rule that _must_ be followed. **Presentation Profiles** may contain multiple Destinations/DMEs. Peer meshes may use any HLS in the Destination/DMEs for content retrieval.
> 
> To correctly leverage the Mesh and multiple Destinations, it is important that _each_ Destination has the same named and sourced Live Webcast HLS stream for use with Vbrick Peer-to-Peer.