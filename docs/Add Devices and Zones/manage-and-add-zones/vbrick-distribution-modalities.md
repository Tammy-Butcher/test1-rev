---
title: Vbrick Distribution Modalities
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
The third section of a zone page allows for specification of the **distribution modalities** allowed within this zone.  Each of the distribution modalities has individual settings. Administrators can select which of the modalities is available within a zone as needed when adding or editing the zone. 

<Image align="center" src="https://files.readme.io/e131c55-distributionModalities.png" />

> 🚧 Important!
>
> When configuring your distribution modalities, please keep in mind the order that **Playback URLs** are attempted (by both Vbrick EVP / Rev, and Vbrick Universal eCDN via SDK).  That is: 
>
> 1. Vbrick Multicast
> 2. Vbrick Peer-to-Peer 
> 3. Vbrick Devices
> 4. Source Unicast
>
> If a modality is not configured for a zone, it is ignored and **Playback URLs** are *not* provisioned. At least one modality *must* be selected for the zone.

Please review the following topics for configuration details:

* [Vbrick Multicast](doc:vbrick-multicast)
* [Vbrick Peer-to-Peer Zones](doc:rev-connect-zones)
* [Vbrick Devices](doc:vbrick-caching-and-devices) 
* [Source Unicast](doc:source-unicast)
