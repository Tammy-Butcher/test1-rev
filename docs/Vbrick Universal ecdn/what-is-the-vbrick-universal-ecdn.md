---
title: What is the Vbrick Universal eCDN?
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
[block:html]
{
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n  <li>&#128736; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Universal eCDN</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


Vbrick is proud to offer the **Vbrick Universal eCDN** as a distinct product that provides the ability to distribute your stream or 3rd party originating system streams (EVPs and VCs such as WebEx or Microsoft Teams) through native and bespoke integrations [Microsoft Teams](doc:microsoft-teams) and [Webex Webinars](doc:webex-webinars).  This is achieved using the [Vbrick Universal eCDN SDK](ref:vbrick-universal-ecdn-sdk).  This allows you to use your own systems and players, but distribute the streams over Vbrick's world-class distribution technologies.

Customers have access to a web-based online **Vbrick Management Interface** that provides all controls, analytics, and the management of each of the distribution modalities.  This secure interface is your portal to controlling your distribution.

Vbrick provides several different distribution modalities:  **Vbrick Peer-to-Peer**, **Vbrick Edge Caching**, and **Vbrick Multicast**.  Vbrick believes that no one modality is sufficient for the various network needs and topologies.  Customers can pick and choose which of the modalities they use and for which parts of their network.  Currently, **Vbrick Universal eCDN** provides both **Vbrick Peer-to-Peer** and **Vbrick Edge Caching**.  

- **Vbrick Peer-to-Peer** is a peer mesh where browsers share video and reduce ingress bandwidth.  This solution  interoperates with the **Vbrick Edge Caching** engines, though they are not required (they just greatly further reduce ingress bandwidth.)  The specification of Vbrick Peer-to-Peer occurs within the management interface
- **Vbrick Edge Caching** is a software VM that can be housed anywhere within the customer enterprise.  These cache and serve content.  While caching is the primary feature, there are many additional features -- please explore the Vbrick DME.
- **Vbrick Multicast** is coming to **Vbrick Universal eCDN** in a future release.  

> 📘 Note
> 
> Current **Vbrick Enterprise Video Platform (EVP)** customers have full access, utilizing the existing Vbrick EVP Multicast capabilities.
> 
> Features made available within **Vbrick Universal eCDN** are also available to **Vbrick Enterprise Video Platform (EVP)** customers.
> 
> Please contact [Vbrick Support](http://vbrick.com/support/) for additional information.

> 👍 Tip
> 
> The **Vbrick Universal eCDN** is currently expanding its feature set and capabilities. It will continue to be updated with new features and functions with every release.  Keep checking this section for ongoing updates each release!

## Requirements

### Account Setup

Before you can begin using the **Vbrick Universal eCDN**, the following account setup requirements should be met.

- A Vbrick provisioned **Vbrick Universal eCDN** account must be acquired.
- Vbrick will then provision a cloud tenant (by the customer's region).
  - Tenant will be configured with the [Vbrick Universal eCDN module](doc:rev-license-types-and-add-ons#modules) activated.
  - Tenant will have an associated [Concurrent Users](doc:rev-license-types-and-add-ons#concurrent-users) license based on the contract.

If you have questions, please work with your Vbrick Sales representative for this.

### URLs and Allowed Lists

**Vbrick Universal eCDN **utilizes a cloud-based control portal.  All streaming and streaming configurations utilize the portal.  This requires that both Admin and end user’s browsers (either internal or external to customer networks) and DMEs installed (within customers networks) are able to access these various service URLs.  

There are several different technologies that may impede or restrict access to these URLs. 

For example: Customers may leverage browser, proxy, or firewall lists to restrict URLs that can be accessed from an end user’s browser and may have networking restrictions that limit the DME.  Customers that have these types of network controls _must_ provide access or reachability.

The **Vbrick Universal eCDN **Allowed Lists are identified within [Required URLs and Allowed Lists](doc:rev-required-urls-and-allowed-lists) 

### User Setup

Access to the tenant is user-role specific.  The following is a minimum configuration:

- At least one **Account Admin** role assigned who can configure the **Vbrick Universal eCDN** so that it works correctly with the **Vbrick Universal SDK**.  

This will be provisioned by Vbrick with the cloud tenant.

## Certified Players

The Vbrick Universal eCDN is designed and developed to work with your players (either MS Teams players or bespoke player configurations). Vbrick works diligently to identify and qualify players – both the underlying player technologies (like hls.js or video.js) and/or player technologies utilized within 3rd-party systems (such as Microsoft Teams or Webex players).  While other player technologies may work with Vbrick Universal eCDN, the following list represents the players and technologies that we have tested and qualified to date.

[block:parameters]
{
  "data": {
    "h-0": "Player Technology",
    "h-1": "Certification Notes",
    "0-0": "hls.js",
    "0-1": "Certified for all modalities (Multicast, Peer-to-Peer, Unicast, and Source).  Vbrick certifies the latest version of hls.js technology.  \n  \nThis certification covers the current hls.js base technology utilized in bespoke players or 3rd party solutions.  Certification covers the general, common, and approved use and deployment of the hls.js technology and should be tested.  \n  \nAny necessary SDK modification based on hls.js version or deviations of use or deployment will be considered on a case-by-case basis within the context of our development process.  \n  \nVbrick _always_ recommends using the current version of this technology, as well as conforming to the general, common, and approved uses.",
    "1-0": "Microsoft Teams ",
    "1-1": "Certified for all modalities.  \n  \nThis certification covers the current Microsoft Teams Azure Player for both HLS (that utilizes hls.js) and DASH (that utilizes video.js).   \n  \nAdditionally, this certification covers the current Microsoft Teams playback within a browser for both HLS (that utilizes hls.js) and DASH (that utilizes video.js).   \n  \nPlease be aware of your Microsoft Teams tenant settings and capabilities.  Microsoft continues to innovate and is actively migrating customers from DASH to HLS (over 2025) while also discontinuing some related products.  Vbrick Universal eCDN SDK covers both protocols during this migration such that you should see no changes.",
    "2-0": "Webex Player",
    "2-1": "Certified for all modalities.  \n  \nThis certification covers the current Webex player (that utilizes hls.js) with native Vbrick integration.",
    "3-0": "video.js",
    "3-1": "This certification covers the current video.js base technology for use with HLS as utilized in bespoke players or 3rd party solutions.  Certification covers the general, common and approved use and deployment of the video.js technology with HLS and should be tested.  \n  \nAny necessary SDK modification based on video.js version or deviations of use or deployment will be considered on a case-by-case basis within the context of our development process.  \n  \nVbrick _always_ recommends using the current version of this technology, as well as conforming to the general, common and approved uses.",
    "4-0": "Brightcove",
    "4-1": "This certification covers the current Brightcove base technology for use with LIVE HLS as utilized in bespoke players or 3rd party solutions.  Certification covers the general, common and approved use and deployment of LIVE HLS sources and should be tested.  \n  \nAny necessary SDK modification based on Brightcove versions or deviations of use or deployment will be considered on a case-by-case basis within the context of our development process.  \n  \nVbrick _always_ recommends using the current version of this technology, as well as conforming to the general, common and approved uses.   \n  \nNotes:  \n  \n1. Currently, Brightcove playback is not available for Safari browsers when using Vbrick Universal eCDN.  We are investigating a fix for this. \n2. Brightcove utilizing Vbrick Universal eCDN is limited to LIVE streams.  We anticipate adding VOD playback in our next release. "
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]




## Key Components

It is important to understand the components of the eCDN and what you can expect to see when you log in for the first time.

- Upon login, the **Vbrick Management Interface** (for the **Vbrick Universal eCDN**) displays a calendar in List view.  It will show all streams (called events) that have _previously_ happened.  Because this is an _unscheduled_ eCDN, there is no capability to create streaming events. 
- Account Admins have access to [Admin Menu Options](doc:admin-menu-options) to configure the eCDN, set up user accounts, and configure Zones, DMEs, and Vbrick Peer-to-Peer settings. This provides the necessary integrations so that the SDK can dynamically stream video.
- [Real-Time Webcast Analytics](doc:real-time-webcast-analytics) can be viewed for currently active streams (events). [Webcast Report Downloads](doc:webcast-reports) for previous events are also available.

## Available Roles

A set of Rev [Roles and Permissions](doc:roles-and-permissions) are available in the **Vbrick Universal eCDN**.  Each defined user will have one or more of these roles, and ultimately the union of permissions. 

To access this list, an Account Admin navigates to the **Users** dropdown menu and then select the **Roles** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fba66e1-roles.png",
        null,
        "The Roles and Permissions displayed here are available for use"
      ],
      "align": "center",
      "caption": "The Roles and Permissions displayed here are available for use"
    }
  ]
}
[/block]