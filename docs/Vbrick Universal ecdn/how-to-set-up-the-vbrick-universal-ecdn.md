---
title: How To Set Up the Vbrick Universal eCDN
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: rev-connect-zones
      title: Vbrick Peer-to-Peer Zones
    - type: basic
      slug: user-location-service-uls
      title: User Location Service (ULS)
    - type: basic
      slug: create-an-api-key
      title: Create an API Key
    - type: endpoint
      slug: jwt-authentication
      title: JWT Authentication
---
Once you have access to your Vbrick Universal eCDN you will need to log in with an **Account Admin** account to configure your **Vbrick Universal eCDN** tenant (via the **Vbrick Management Interface**) to begin live streaming from the [VBrick Universal eCDN SDK](ref:vbrick-universal-ecdn-sdk). 

## Key Concepts

There are a few key concepts that are necessary for configuring your use of **Vbrick Universal eCDN**.

[Distribution Modalities](doc:vbrick-distribution-modalities). **Vbrick Universal eCDN** is a collection of distribution technologies and methods we call **Distribution Modalities**.  These include: **Vbrick Multicast**, **Vbrick Peer-to-Peer**, edge caching using **Vbrick Devices**, and **Source Unicast**.  These work together or independently based on your configuration.

[Zones](doc:manage-and-add-zones).  Vbrick uses the concept of **Zones** (groupings of where viewers/browsers will be) for defining the distribution capabilities.  With Zones, you can configure, "Zone A will only use peer-to-peer", or "Zone B will use multicast and unicast fallback", etc.  Administrators define who is going to be in a Zone by **IP ranges** and distribution by available modalities.

[Vbrick Universal eCDN SDK](ref:vbrick-universal-ecdn-sdk).  Vbrick provides a software development kit (SDK) as a javascript package which gets included within the html player.  The SDK initiates and provides the appropriate distribution modalities to the html player.  Customers have two methods for working with the SDK -- either they modify their existing player's html page to include and utilize the Vbrick distribution modalities, and/or they take advantage of Vbrick's  existing native integrations.  The native integrations are configured within third party solutions, and customers need not work directly with the SDK (because you already are, it's under the covers).  If you need to work directly with our SDK however, please view the [Vbrick Universal eCDN SDK](ref:vbrick-universal-ecdn-sdk) topic.

[Distributed Media Engine](https://dmedocs.vbrick.com) **Vbrick DME** or **DME**.  The DME is a software (virtual machine) server that is installed within the customers' enterprise.  This server provides the **Vbrick Edge Caching** capabilities.

[User Location Service](doc:user-location-service-uls).  To best assign your viewers to a **Zone**, you may wish to set up a ULS server.  This is a **DME** that players ping to define their IP addresses.  Knowing the IP addresses of the players allows Administrators to more discretely define the **Zone** boundaries, and more fully control and optimize the bandwidth usage.  While this is optional, Vbrick recommends setting up a ULS server.

## Configuration Steps Overview

To initially configure your environment, an **Account Admin** performs the following steps:

1. Set up your distribution network.
   1. Add DME(s) per your network and use cases.
   2. Add User Location Service. 
   3. Configure Zones (defining who gets what kind of distribution).
2. Configure the authorization.
   1. Verify JWT Authentication Certificate.
   2. Verify Universal eCDN API Key.
3. Configure Use.
   1. Configure available native integrations.
   2. Develop bespoke integrations with our SDK.

> 👍 Tip
> 
> Once configured, you may not need to reconfigure unless there is a change in your network topology or distribution use case.  At this point, you will have the ability to include the SDK within your developed webpage and player or to utilize a 3rd party integration that will automatically include the SDK within your webpage.

## Configured Workflow Overview

As an example, to illustrate the process of the SDK, once configured the (simplified) flow is :

A viewer/end-user lands on either your page or the page of a 3rd party integration.

1. The viewer's player page will load.
2. The player page will load the Vbrick Universal eCDN SDK (which is a js include).
3. The player page will provide the payload/stream source information to the SDK. Note: This will happen automatically with native integrations.
4. The SDK will identify the viewer's IP (if possible, again this is at your discretion and network configuration).
5. The SDK will communicate with the Vbrick Universal eCDN, sending the IP and payload.
6. The Vbrick Universal eCDN will:
   1. Locate the matching Zone, based on the SDK-provided IP.
   2. Using the Zone, identify the appropriate distribution modalities.
   3. Generate and respond with the appropriate playback URLs for modalities.
7. If peer-to-peer is to be utilized, the SDK will contact Vbrick Universal eCDN to get a peering configuration.
8. The SDK will provide appropriate playback URLs to the player.
9. The SDK will periodically report real-time player analytics to Vbrick Universal SDK.

> 📘 Note
> 
> If you are a **Vbrick EVP Customer** or **Partner** and want to use the [Vbrick Universal SDK](ref:vbrick-universal-sdk), you need only to enable **JWT Authentication**.
> 
> However, if you are a **Vbrick Universal eCDN Customer** or **Partner**, you must _also_ setup and configure your account by completing the steps below.

To get started, each step is described in more detail in the sections below.

## Detailed Configuration Steps

### Add DMEs

DMEs must be added to the system before they can be used within a Zone or for edge caching.

Please review [Vbrick Universal eCDN Devices](doc:vbrick-universal-ecdn-devices).

### Configure the User Location Service

Next, configure the user location service.

1. Navigate to **System Settings** > **eCDN Settings** and scroll down to the **User Location** section.
2. Select the **Validate User Location** checkbox and then enter a **User Location Service URL**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cd0d755-userLocationURL.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


3. HTTPS URL should point to a FQDN with  /cgi-bin/localip.cgi on an existing, reachable (by all players ) DME 
   1. <https://LondonDME-01-HQ.mycomanyname.com/cgi-gin/localip.cgi>
4. View the topic on [User Location Service (ULS)](doc:user-location-service-uls) for complete details on configuration.

### Configure Zones

In most cases, you will define several **Zones**.  Each zone is bound by a set of IPs/IP-Ranges defining the viewers within the zone, and the selection of the distribution modalities.  If you add multiple modalities, each will be tried (by the SDK/player) in the following order (by Zone settings): Multicast, Peer-to-Peer, Caching/Unicast, Origin.

To create a **Zone** in your tenant:

1. Navigate to **Devices** > **Zones** and then click the **Add Zone** button to create a new zone.
2. Name your **Zone** systematically and meaningfully.
3. Configure the correct **IP Addresses**.  
   1. This field takes IPs, IP ranges, and CIDR notation, both IPv4 and IPv6).  Placing your IP ranges on new lines will allow you to configure different peering relationships.

#### Define Distribution Modalities for a Zone

To define the distribution modalities for this Zone, make the following configurations.

##### Vbrick Peer-to-Peer

If you want the **Zone** to utilize **Vbrick Peer-to-Peer** you must enable it.  View the [Vbrick Peer-to-Peer Zones](doc:rev-connect-zones) topic for complete details if needed

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b441234-enablePeer2Peer.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


##### Vbrick Multicast

If you want the **Zone** to utilize **Vbrick Multicast**  you must enable it.  View the [Vbrick Multicast](doc:vbrick-multicast) topic for complete details if needed

Reminder:  **Vbrick Universal eCDN** does not support **Vbrick Multicast** yet.

##### Vbrick Edge Caching

If you want the **Zone** to utilize **Vbrick Edge Caching** / **DME** they must be included in the **DEVICES** section.  (Note:  You will need the DME added before it can be selected on this step.)  View the [Vbrick DME](doc:add-a-dme) topic for complete details on adding a DME to your Devices section.

### Verify JWT Authentication Certificate

The Vbrick Universal eCDN uses [JWT authentication](ref:jwt-authentication) for user account access. Please verify that you have an Encryption and Signing Certificate named **RevConnectDefault**.  This is required for access.

When your Vbrick Universal eCDN tenant is created, a default Vbrick Peer-to-Peer certificate is also created.  You can use this certificate or create your own as needed. 

To verify or create a new JWT authentication certificate:

1. Navigate to **System Settings** > **User Security** and scroll to the **JWT Authentication** section.
2. Verify that the **RevConnectDefault** certificate already in place with a corresponding Signing and Encryption certificate.  If it exists, skip to end.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2034760-revConnectDefaultCert.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


3. If this does not exist, please add it.  Click the **Add New** button to create a new certificate.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec887ef-addNewCert.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


4. On the popup, you will have the option to auto-generate a Signing Certificate or to paste in your own.
5. Don't forget to click Save.

At this point, you now have a certificate that will be used for authentication to view materials on your Vbrick Universal eCDN.

### Verify Universal eCDN API Key

Additionally, you will need to [create an API key](doc:create-an-api-key) that is to be used specifically for the **Vbrick Universal eCDN** and the integrations it uses.

1. Navigate to **System Settings** > **API Keys** 
2. Verify that there is an API key named UNIVERSAL_ECDN, if so skip to end.
3. If this does not exist, please add it.  Click the **Add Key** button to create a new API key.
4. Make sure the key is named **UNIVERSAL_ECDN** and that you provide a unique key text (the secret will be generated, but you can view it there if necessary)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/099bbac-addAPIKey.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


At this point, you now have a UNIVERSAL_ECDN API key that will be used in the integrations.

### Finalize Usage Options

At this point, you have configured your network and distribution options and set up the credentials (JWT and API key) necessary to gain access.  Now you need to finalize how to get streams pushing through **Vbrick Universal eCDN**.

Two different approaches can be used and you can use one or both depending on your needs.  

First, you can **configure available native integrations**.  With this approach, you configure your **Vbrick Universal eCDN** and (in this case) Microsoft.  This results in players in a Microsoft Teams event distributing over the **Vbrick Universal eCDN**.  Please review  [Vbrick Universal eCDN Media Settings](doc:vbrick-universal-media-settings) for more details.

The second method is to **develop bespoke integrations with our SDK**.  We provide the details on getting started at:   [Vbrick Universal eCDN SDK](reference:vbrick-universal-ecdn-sdk).