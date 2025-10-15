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
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
  <li>&#128736; <a href="/docs/rev-license-types-and-add-ons">Vbrick Universal eCDN</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

Vbrick is proud to offer the **Vbrick Universal eCDN** as a distinct product that provides the ability to distribute your stream or 3rd party originating system streams (EVPs and VCs such as WebEx or Microsoft Teams) through native and bespoke integrations [Microsoft Teams](doc:microsoft-teams) and [Webex Webinars](doc:webex-webinars).  This is achieved using the [Vbrick Universal eCDN SDK](ref:vbrick-universal-ecdn-sdk).  This allows you to use your own systems and players, but distribute the streams over Vbrick's world-class distribution technologies.

Customers have access to a web-based online **Vbrick Management Interface** that provides all controls, analytics, and the management of each of the distribution modalities.  This secure interface is your portal to controlling your distribution.

Vbrick provides several different distribution modalities:  **Vbrick Peer-to-Peer**, **Vbrick Edge Caching**, and **Vbrick Multicast**.  Vbrick believes that no one modality is sufficient for the various network needs and topologies.  Customers can pick and choose which of the modalities they use and for which parts of their network.  Currently, **Vbrick Universal eCDN** provides both **Vbrick Peer-to-Peer** and **Vbrick Edge Caching**.  

* **Vbrick Peer-to-Peer** is a peer mesh where browsers share video and reduce ingress bandwidth.  This solution  interoperates with the **Vbrick Edge Caching** engines, though they are not required (they just greatly further reduce ingress bandwidth.)  The specification of Vbrick Peer-to-Peer occurs within the management interface
* **Vbrick Edge Caching** is a software VM that can be housed anywhere within the customer enterprise.  These cache and serve content.  While caching is the primary feature, there are many additional features -- please explore the Vbrick DME.
* **Vbrick Multicast** is coming to **Vbrick Universal eCDN** in a future release.  

> 📘 Note
>
> Current **Vbrick Enterprise Video Platform (EVP)** customers have full access, utilizing the existing Vbrick EVP Multicast capabilities.
>
> Features made available within **Vbrick Universal eCDN** are also available to **Vbrick Enterprise Video Platform (EVP)** customers.
>
> Please contact [Vbrick Support](http://vbrick.com/support/) for additional information.

> 👍 Tip
>
> The **Vbrick Universal eCDN** is currently expanding it's feature set and capabilities. It will continue to be updated with new features and functions with every release.  Keep checking this section for ongoing updates each release!

## Requirements

Before you can begin using the Vbrick Universal eCDN, the following prerequisites are required:

* A Vbrick provisioned cloud tenant that has the [Vbrick Universal eCDN module](doc:rev-license-types-and-add-ons#modules) activated and a [Concurrent Users](doc:rev-license-types-and-add-ons#concurrent-users) license type purchased.  Please work with your Vbrick Sales representative for this.
* At least one **Account Admin** role assigned who can configure the **Vbrick Universal eCDN** so that it works correctly with the **Vbrick Universal SDK**.  This will be provisioned by Vbrick with the cloud tenant.

## Certified Players

The Vbrick Universal eCDN is designed and developed to work with your players (either MS Teams players or bespoke player configurations). Vbrick works diligently to identify and qualify players – both the underlying player technologies (like hls.js or video.js) and/or player technologies utilized within 3rd-party systems (such as Microsoft Teams or Webex players).  While other player technologies may work with Vbrick Universal eCDN, the following list represents the players and technologies that we have tested and qualified to date.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Player Technology
      </th>

      <th>
        Certification Notes
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        hls.js
      </td>

      <td>
        Certified for all modalities (Multicast, Peer-to-Peer, Unicast, and Source).  Vbrick certifies the latest version of hls.js technology.  

        This certification covers the current hls.js base technology utilized in bespoke players or 3rd party solutions.  Certification covers the general, common, and approved use and deployment of the hls.js technology and should be tested.  

        Any necessary SDK modification based on hls.js version or deviations of use or deployment will be considered on a case-by-case basis within the context of our development process.  

        Vbrick *always* recommends using the current version of this technology, as well as conforming to the general, common, and approved uses.
      </td>
    </tr>

    <tr>
      <td>
        Microsoft Teams Azure Player
      </td>

      <td>
        Certified for all modalities.  

        This certification covers the current Microsoft Teams Azure Player for both HLS (that utilizes hls.js) and DASH (that utilizes video.js).   Microsoft is migrating from DASH to HLS and our SDK will cover both to support this migration.
      </td>
    </tr>

    <tr>
      <td>
        Webex Player
      </td>

      <td>
        Certified for all modalities except Multicast.  

        This certification covers the current Webex player (that utilizes hls.js) with native Vbrick integration.  

        Vbrick and Webex are working together to support Multicast soon.
      </td>
    </tr>

    <tr>
      <td>
        video.js
      </td>

      <td>
        Currently undergoing testing for Certification for Video.js with HLS streams for all modalities.  

        This certification covers the current video.js base technology for use with HLS as utilized in bespoke players or 3rd party solutions.  Certification covers the general, common and approved use and deployment of the video.js technology with HLS and should be tested.  

        Any necessary SDK modification based on video.js version or deviations of use or deployment will be considered on a case-by-case basis within the context of our development process.  

        Vbrick *always* recommends using the current version of this technology, as well as conforming to the general, common and approved uses.
      </td>
    </tr>
  </tbody>
</Table>

## Key Components

It is important to understand the components of the eCDN and what you can expect to see when you log in for the first time.

* Upon login, the **Vbrick Management Interface** (for the **Vbrick Universal eCDN**) displays a calendar in List view.  It will show all streams (called events) that have *previously* happened.  Because this is an *unscheduled* eCDN, there is no capability to create streaming events. 
* Account Admins have access to [Admin Menu Options](doc:admin-menu-options) to configure the eCDN, set up user accounts, and configure Zones, DMEs, and Vbrick Peer-to-Peer settings. This provides the necessary integrations so that the SDK can dynamically stream video.
* [Real-Time Webcast Analytics](doc:real-time-webcast-analytics) can be viewed for currently active streams (events). [Webcast Report Downloads](doc:webcast-reports) for previous events are also available.

## Available Roles

A set of Rev [Roles and Permissions](doc:roles-and-permissions) are available in the **Vbrick Universal eCDN**.  Each defined user will have one or more of these roles, and ultimately the union of permissions. 

To access this list, an Account Admin navigates to the **Users** dropdown menu and then select the **Roles** option.

<Image alt="The Roles and Permissions displayed here are available for use" align="center" src="https://files.readme.io/fba66e1-roles.png">
  The Roles and Permissions displayed here are available for use
</Image>
