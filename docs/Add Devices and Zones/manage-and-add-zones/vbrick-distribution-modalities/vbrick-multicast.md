---
title: Vbrick Multicast
excerpt: >-
  This topic provides an overview of how to enable and configure Vbrick
  Multicast in a zone.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Enable Vbrick Multicast for a Zone

<Image align="center" src="https://files.readme.io/841a078-enableVbrickMulticast.png" />

| Field or Setting          | Description                                                    |
| :------------------------ | :------------------------------------------------------------- |
| Supports Vbrick Multicast | Enable to indicate whether or not the zone supports multicast. |

## Vbrick Multicast Requirements in Zone Configuration

When enabling a zone for **Vbrick Multicast**, please be aware of the following requirements:

* Viewers must have the **Vbrick Multicast Agent** installed. A comprehensive [installation guide](https://portal.vbrick.com//help/PDFs/VBM/vbmInstallationGuide.pdf) is located on our Documentation site. 
* The zone *must* have at least one DME that is configured for multicast.  This includes:
  * DME must have sufficient multicast addresses to support maximum expected customer concurrent streams.  Vbrick recommends over provisioning multicast address within each DME.
  * DME must be selected within the zone as a device, and have the necessary multicast streams and/or **Auto Multicast for Cloud Streams** selected.

## Additional Documentation

[Vbrick Multicast Agent Installation Guide](https://portal.vbrick.com//help/PDFs/VBM/vbmInstallationGuide.pdf)

[Vbrick Multicast Agent Release Notes](https://portal.vbrick.com//help/PDFs/VBM/vbmReleaseNotes.pdf) 

> 📘 Note
>
> Expiration dates for SSL certificates are listed in VBM Release notes. Refer to the [Device Compatability Matrix](doc:compatibility-matrix) for VBM versions that are currently supported.
