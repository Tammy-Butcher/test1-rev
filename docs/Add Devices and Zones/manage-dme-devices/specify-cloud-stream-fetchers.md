---
title: Specify Cloud Stream Fetchers
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
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

One of the major benefits of using local DMEs is that the DME can pull (or **Fetch**) live streams from the cloud to deliver locally.  This can greatly reduce the <Glossary>ingress bandwidth</Glossary>, so only the DME is pulling the live stream and not the individual viewers.  Once the live stream is within the DME, then several different distribution methods are available (Vbrick Multicast, Unicast, sourcing Vbrick Peer-to-Peer) allowing for customized configuration.

Fetchers are the internal DME processes that support Rev events by pulling cloud-sourced streams into the DME.  Fetchers are started automatically when multicast is involved, and can be started on demand by browser requests.  Again, Fetchers only support events and not VOD.  Once the streams are available within the DME, then **Auto Unicast** and/or **Auto Multicast** are available for sourcing local viewers per configuration.

> 📘 Note
>
> See [Video Conference, RTMP, and Other Sourced Streams](doc:video-conference-vc-integrations) for specifications of single and dual cloud-sourced streams.

Account Administrators can further specify where fetchers will pull/source the stream.  Meaning, fetchers can be configured to pull the live stream from the cloud CDN or pull the live stream from another DME.  In this way, Administrators can more effectively control the flow of live streams through their networks for optimization of LAN and ingress bandwidth.  They may choose certain DMEs to always pull from the cloud (which is useful for remote offices/DMEs), or to pull from adjacent DMEs (which reduces ingress bandwidth.)

Both a primary and secondary fetcher can be configured on the Rev DME page (specific to each DME. ) The options are called **Primary Fetching Location** and **Secondary Fetching Location**.  The secondary location is used as fallback if the primary location is not available. Specifying these features gives Administrators more control of data flow through their network.  

Fetching locations (Primary or Secondary) can be set to pull from the Cloud (by selecting the **Cloud Fetching** in dropdown), or to pull from a **peer DME** (by selecting a DME in dropdown).  If you pull from a peer DME, that peer DME has to have a FQDN and a valid tls certificate, as well as access to the stream as well.  It is possible to set up cascading DMEs, each pulling from another DME, but *ultimately* a DME should pull from the *Cloud*.  

> 🚧 Caution!
>
> Rev will not allow a fetcher configuration that introduces a cycle or loop within the fetcher map.   
>
>    For example:   DME-A fetches from DME-B; DME-B fetches from DME-A.
>
> This configuration creates a loop, which ultimately cannot source the stream and will not work.  The Rev system will not allow you to create a loop.

**Fetcher Configuration Example**  Consider an example with 2 DMEs named **atta LocalNet** and **bttb LocalNet**.  In this example, let's look at the configuration for **bttb Localnet**.

<Image title="cloudFetch1.png" alt={1086} align="center" width="smart" src="https://files.readme.io/5fdd6ca-cloudFetch1.png">
  If the atta LocalNet stream is unavailable or has difficulties, Cloud Fetching is the fallback
</Image>

In this example, **bttb Localnet** configured **Primary Fetching Location** is set to another DME named **atta LocatNet**, and its **Secondary Fetching Location** is set to **Cloud Fetching**.  

When an event is started, 

1. Rev provisions the Viewers (within the appropriate Zone, with the **bttb Localnet** DME) playback URLs  for the live stream.  These playback URLs point to the **bttb Localnet** DME while identifying the live stream.
2. The Viewers' browser will then request the URL from  **bttb Localnet**.
3. The **bttb Localnet** DME gets a browser request and will identify the live stream and start/use a fetcher to retrieve the stream.  The DME will use the **Primary Fetching Location** (currently set to DME **atta LocalNet**) as the source to get the live stream.  Also,  the fetcher will fallback to the **Secondary Fetching Location**, **Cloud Fetching**, if there are difficulties with the **Primary Fetching Location**.   

Based on networking needs, Administrators have options with this feature.  For example, they can: 

* Make either Primary or Secondary Fetching Locations(s) pull from the Cloud
* Create cascades of DMEs (as long as one ultimately pulls from the Cloud)
* Use (or not use) a Secondary locations (a Primary location *is* necessary)
* Just stick with the default Primary pulling from the Cloud with no Secondary

As always, please test configurations as reachability may be an issue.

> 📘 Note
>
> All existing and newly added DMEs default to this standard configuration:
>
> * **Primary Fetcher Location**: Cloud Fetching
> * **Secondary Fetcher Location**: Not Defined
>
> If you do not want to re-specify the fetcher locations, then no action is necessary.

Finally, as noted above, **DMEs v3.26 and previous versions** utilize a single fetcher, standard configuration, from the Cloud by default.  These DMEs *cannot* be configured for Primary and Secondary Fetching locations – and the option is disabled on the as seen in the image below.

<Image title="cloudFetch2.png" alt={1095} align="center" width="smart" src="https://files.readme.io/a724166-cloudFetch2.png">
  DMEs that do not have v3.27+ cannot be configured for Primary and Secondary Fetching.  Secondary appears as 'Not Defined', seen here.  This is the default configuration.
</Image>
