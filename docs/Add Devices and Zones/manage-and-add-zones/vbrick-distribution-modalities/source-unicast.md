---
title: Source Unicast
excerpt: >-
  This topic provides an overview of how to enable and configure Source Unicast
  settings within a zone.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The **Source Unicast** distribution modality provides the **Fallback to Source** feature.  This setting controls the ability for a user within a zone to either fallback to source (or origin) or to utilize the **zone hierarchy** in the event no Playback URLs are available. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73ba3d1-sourceUnicastSection.png",
        "",
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
    "0-0": "Fallback to Source",
    "0-1": "If **enabled**, this feature allows Rev to provision a source (or origin) URL as a **Playback URL** for a zone.  As a reminder, if the source URL is provided as **Playback URL**, then the there will be no **zone hierarchy** failover because a distribution modality (Source Unicast or origin) is available.  \n  \nThis is useful in the case of a zone not having additional available distribution modalities.  This has the side effect of NOT utilizing the zone hierarchy.  \n  \nIf **disabled**, this feature stops Rev from provisioning a source (or origin) URL as a **Playback URL** for a zone.  In this case, if there are no other distribution modalities then Rev will utilize the **zone hierarchy** to find Playback URLs.  \n  \nThis feature is **enabled** by default for new zones."
  },
  "cols": 2,
  "rows": 1,
  "align": [
    "left",
    "left"
  ]
}
[/block]


At the release of this feature, **Fallback to source** is enabled by default.

## Special Source Unicast Considerations

### Provisioning Playback URLs.

As noted above, if **Fallback to Source** is **Enabled**, then Rev provisions the source URL within the set of **Playback URLs **for the player.   The player then uses that URL accordingly.

When we say **source**, we mean the _cloud based streams_ (as provided by Vbrick EVP / Rev or video conferencing solutions) as the source, or _source urls_ (as provided by developers when using the Vbrick Universal eCDN SDK.)  For example, while we may be watching a Microsoft Teams meeting stream from the DME, but it's source would be in the (Microsoft) cloud.

It should be noted that **Presentation Profile** events that do not include **DME** CDN pushes (either through custom stream configuration or via **Rev IQ **enrichment) do not have sources.  In this case, this setting is ignored and the system utilizes the **zone hierarchy** if necessary.  If there are associated CDN pushes or enriched streams, then those are used as source URLs and will be supplied if **Fallback to Source** is **enabled**.

As a reminder, there may be other distribution modalities that are provisioned based on the zone configuration.  There are many different ways to configure the zone; here are more examples to illustrate the use of **Fallback to Source**.

Consider the example where the **Playback URLs** are provisioned with both a multicast and origin URLs.  (Meaning the Zone is configured for multicast and has **Fallback to Source** enabled.) In this case, the player would first try to view the video with multicast, and if that fails, it would then go to origin.  (This is an example of the player fallback, not the **Playback URLs** provisioning fallback.) Just because this feature is enabled, other **Playback URLs** will not be ignored.

In another example, there may be no other available distribution modalities except **Fallback to Source**.  (Meaning the Zone is ONLY configured with **Fallback to Source** enabled.). In this case, the Playback URLs set would only include the origin URL.  Players would go to source.

### When Should I Disable Fallback to Source?

**Fallback to Source** is a safety enablement -- meaning, if there are no additional distribution modalities (or they fail during playback), the player will go to origin and playback.  There are situations, mostly around broadband usage and reduced network capacity, where you would not want a group of viewers to go to origin and consume bandwidth.  In that case, it is best to try to configure your Zones to target these viewers, and disable the **Fallback to Source**.  This can be a very effective method for controlling network bandwidth.

> 🚧 Important!
> 
> **Initial Action May Be Required**
> 
> At the release of this feature, June 2023, the **Fallback to source** setting is **Enabled** by default for all existing customer Zones.  
> 
> If **Enabled**,  the source URL is provided as **Playback URL**, then the there will be no **Zone Hierarchy** failover (because the distribution modality **Source Unicast** (origin ULR) is available.  
> 
> If your Zone architecture relies on **Zone Hierarchies** to provision **Playback URLs** from parent-zones, then please review and address this setting within the appropriate Zones.