---
title: Manage and Add Zones
excerpt: >-
  This section explains Rev zones and how to create them into logical zone
  hierarchies. It also includes details of how to create a Vbrick Peer-to-Peer
  zone to form a peer mesh for Live HLS events.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
**Zones** are a programmatic way of grouping viewers such that distribution modalities can be applied selectively with the ultimate goal of provisioning correct **Playback URLs** (These URLs are the video location and control parameters for each the various distribution modalities defined within the zone.)  In this way, customers can control the distribution and playback for their users with respect to their internal and external networking needs.

This section explains how to create zone and configure distribution modalities for both Live and VOD assets.

## What are Zones?

Vbrick products focus on delivering video (both Live and VOD) to our customers efficiently.  To do this, Vbrick needs some level of grouping within and across customers’ networks.  This grouping allows Vbrick to provide distribution tailored to the customers and viewers needs.

**Zones** are an abstract grouping mechanism based on IP ranges.  Viewers are grouped and matched to zone (by IP) that will provide one or more distribution modalities.  A [distribution modality](doc:vbrick-distribution-modalities) is a technology for distributing video.  Vbrick provides the following modalities: Vbrick Multicast, Vbrick Peer-to-Peer, Vbrick Unicast Caching, and Origin playback.

The first zone to consider is the [Default Zone](doc:manage-and-add-zones#the-default-zone) which is automatically created and catches all viewers with IPs that are not defined within other customer defined zones.  This zone is normally reserved for users viewing from the Internet and *not* from within a customer’s enterprise.

In addition to the Default Zone, you can additional zones through the **Devices** > **Zones** menu by **Adding a Zone**. This simple process includes providing a name and a set of unique IP (IPv4 and/or IPv6) address ranges for the users/viewers.  Then, different distribution modalities can be selected and configured for that zone. For details, view [Add or Edit a Zone](doc:add-a-zone).

You can create zones as a flat structures or develop a hierarchy of parent-child zones.  A [zone hierarchy](doc:manage-and-add-zones#zone-hierarchy) can provide for fallback in URL playback provisioning.

## The Default Zone

A **Default Zone** is automatically created when an account is created and initialized. This zone will define the distribution modalities for all users not assigned to other, customer defined zone.  For example, if you define a zone named East Coast for IPs 10.0.0.0/8 (IPv4), then all users with IPs starting with “10” will utilize that zone – any other IP, will utilize the Default Zone.

The Default Zone, because of it’s nature to service internet users, has some special properties.  The Default Zone does not support Vbrick Multicast because Multicast cannot transit the Internet.  Additionally, the Default Zone does not support Vbrick Peer-to-Peer because end users are supplying their own bandwidth.  Vbrick DMEs or Custom Devices can be added to the Default Zone (to provide specific streams), and Vbrick recommends removing Auto Unicast, and setting the DME as Live Only.

Multiple CDN streams can be added to the Default Zone (to support Presentation Profile streams) which will provide random provisioning of the streams to players, as well as, a redundant capability for fallback.

## Zone Hierarchy

Zones can be defined within a flat structure or within a hierarchy of parent-child zones.  Placing zones in a hierarchy gives the added benefit of providing fallback to parent zones when there are no playback URLs.  Falling back to a parent can change the distribution modalities as well.

Vbrick recommends configuring your zones to address all possible IP ranges within your network.

Vbrick recommends that customers define their zone hierarchy to provide a fail-over for content distribution if your modalities or devices in a specific zone fail for any reason.

To illustrate this, consider following the **zone hierarchy** for Company XYZ in the image below.  Zones are defined for locations named **Florida**, **New England**, **New York City**, etc -- matching their corporate physical location and network configuration.  Each of those zones can have unique IP ranges and can utilize different modalities – for example, **Florida** could use Multicast and Unicast Caching, while **New England** uses Peer-2-Peer.  

The key concept here is that each zone can use any combination of the modalities.  And, if there is a device failure in a zone, such as in **Washington, DC**, then viewers will be provisioned **playback URLs** from the parent **East Coast** zone and so forth on up the zone hierarchy.

The **zone hierarchy** is used by the **zone logic flow** (seen below).

<Image title="zoneLogic.png" alt="Example **Zone Hierarchy** (from **Admin >> Devices >> Zone **page.)" align="center" src="https://files.readme.io/e1e03d0-zoneLogic.png">
  Example **zone hierarchy** (from **Admin > Devices > Zone** page.)
</Image>

## Zone Logic Flow

We use the term **zone logic flow** (or shorter as **zone logic**) to mean the process of searching the zones and provisioning playback capabilities for users within their zone.  This process also includes any fail-over (to parent zones or origin).

In order to accomplish this process, players/web pages will identify and pass the video request and the users IP (or egress IP depending on your configuration) to the Vbrick service.  The service, in turn, searches for the appropriate zones (by user's IP addresses and starting at the child most node and going up the zone hierarchy).  Once the user's zone is located, the zone’s configuration will be used to define a set of **Playback URLs**.  These URLs are the video location and control parameters for each the various distribution modalities defined within the Zone.  

If no matching modalities (and hence, no **Playback URLs**) are found within the zone, then the parent zone will be used.  This continues up the tree until some playback URLs are found, or there are no more zones for consideration.

To illustrate this, with the example above and the user’s IP within the **Washington, DC** zone:

1. If there are modalities available within that zone – the player will be provisioned with associated **Playback URLs**.
2. If there are NO modalities available that can be provisioned – the system will check the **Fallback to Source** setting for the zone.
   1. If the **Fallback to Source** is **ENABLED** and there is a source (origin) URL -- the system will provision only the source URL as **Playback URLs**.  In this example, the player would go directly to source/origin.
      1. Presentation Profile events do not have source URLs.
   2. If the **Fallback to Source** is **DISABLED**, the system will use the **East Coast** (parent zone) to define **Playback URLs**.  (The system will continue to evaluate zones up the hierarchy (United States, North America), until it finds available modalities and provisions playback URLs -- and the process will honor the **Fallback to Source** setting in each zone.)

## Special Zone Logic Flow Considerations

**Device Availability**.  It should be noted, that zones may contain modalities that may not be currently available.  For example, Vbrick keeps real time track of the DMEs , and if the DME loses connection to Vbrick Rev for an extended time it will be marked Offline.  Once a Vbrick DME is considered Offline, it will no longer be provisioned or used for users in configured zones. (Note: Once the DME regains connectivity with Vbrick Rev, it will then be used for distribution.)

> 👍 Tip
>
> If multiple DMEs are assigned to a zone, *all* DMEs are considered before the next zone in the hierarchy is attempted.

**Vbrick Rev Video On Demand**.  For VOD files, Rev "fails up" to the Rev File Store (Vbrick Cloud for cloud customers) as a last resort if all the DMEs in your configured hierarchy are offline.

**Fallback to Source**.  This additional control, specified at the zone level, will terminate any fail-over to the parent process if enabled.  This means that players will be directed to go directly to source.  This may happen in the matching zone or any parent zone that has this feature enabled.  Vbrick recommends top level zones and default zone to enable this feature to assure playback.  *This feature is enabled by default -- so, if your distribution architecture relies on zone hierarchy fail-over, please review the setting.*

**IP not Found during Zone Logic search.**  As mentioned above, if the user’s IP is not found in any zone, that user will be provisioned by the Default Zone.  In this case, please consider enabling Fallback to Source in the default zone.

**Zone Logic Flow Fail-over vs Player Fail-over.** The **zone Logic flow** is strictly about providing the **Playback URLs** to the player.  The **Playback URLs** (only for the modalities within the zone) will be used/attempted by the player in the following priority order with Player Fail-over:  Multicast, Peer-to-Peer, Edge Caching, Source (or origin).  It is important not to conflate the zone logic flow fail-over with player fail-over.

> 🚧 Caution
>
> Rev Cloud Users behind a corporate firewall appear as if they are coming from the same external IP address. 
>
> Having the internal IP helps better utilize the zone hierarchy with the zone logic flow to achieve maximum benefits.  Vbrick provides the ability, within the Vbrick DMEs, to obtain an internal IP address but it must be configured.  Please view: [The DME User Location Service](doc:user-location-service-uls)

> ❗️ Warning!
>
> If the zone hierarchy is not setup, then Rev only returns the playback URL for the user's exact matched zone (which may or may not provide Fallback to Source.)
>
> After zone logic flow has searched for appropriate zones and playback URLs, if none are found, then the user is displayed the following message: “Playback of this video is not available at this time. Please try again later.”
