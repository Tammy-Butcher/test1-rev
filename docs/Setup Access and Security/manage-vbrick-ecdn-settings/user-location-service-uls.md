---
title: User Location Service (ULS)
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
[Zone logic](doc:manage-and-add-zones#zone-logic-flow) in Rev depends on routing users to the correct zone and closest DME to ensure optimal video distribution. This is critical for both Live and Video on Demand (VOD). Consider the distribution of video across organizations with hundreds of DMEs, multiple networks, and sub-nets, serving thousands of viewers. Viewing from the closest DME is paramount.

Additionally, the Vbrick Peer-to-Peer feature can optionally (based on Administrator preference) utilize the user location to facilitate routing and peer sharing across subnets.

To facilitate zone logic and routing, you must designate at least one DME (behind your firewall) as the **USER LOCATION SERVICE URL**.  This is actually the URL to a small script (localip.cgi) that can identify locations behind the firewall.  (e.g., <https://myDME.myCompany.com/cgi-bin/localip.cgi>)   When users log into Rev, this script is called, and the location services DME identifies the user’s location and uses it for video distribution with zone logic. For this reason, you must make sure that the specified DME is accessible to all Rev users behind the firewall.

- In the event that the location services DME is not accessible, you may designate an optional secondary ULS URL.  This is recommended.  When a user plays a video or logs in, Rev accesses the primary ULS DME from that viewer's location and if that access times out, Rev automatically attempts to access the secondary ULS DME instead.  
- Additional security steps must be followed based on whether you are using **Cloud Rev** versus **On Premise Rev**.
- If you are unfamiliar with zone logic, view information on [Zone Logic and Hierarchy](doc:add-a-zone#zone-logic-and-hierarchy) before proceeding.

> 🚧 Important!
> 
> If you are utilizing a dual stack environment for your player browsers, please provision both IPv4 and IPv6 ULS URLs.

## Cloud Hosted Rev

Vbrick is dedicated to ensuring security for cloud-hosted Rev instances which means that all communications are encrypted over TLS connections - thus protecting communication from the customer site to the Cloud. This also means that customer-provisioned security certificates (certs) are necessary for the DME supporting location services specified in Rev.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/53c843b-dmeUserLocationCloud.png",
        "dmeUserLocationCloud.png",
        722
      ],
      "align": "center",
      "caption": "Navigate to System Settings > eCDN Settings to configure a location services DME"
    }
  ]
}
[/block]


> 📘 Note
> 
> Make sure that the user location DME has a qualified customer tls certificate installed.  Failure to have a valid certificate will disable the user location service.  In that case, Rev will utilize any external egress IP it detects for zone logic routing. View the [DME Admin Manual > SSL Certificates](http://portal.vbrick.com/help/dme/3250/index.html#context/Admin/Topic_39) topic for help.

### Configuration

- Select the **Validate User Location** checkbox to configure a location services DME.
- Enter a valid DME URL in the **User Location Service URL** field. This must be the DME’s fully qualified domain name. Alternatively, this may also point to a load balancer that will then point to specific DMEs on your network.
  - For example, a valid URL might be: **<https://mydmename.mycompany.com/cgi-bin/localip.cgi>**  
    Where **mydmename** is the DME hostname, and **mycompany.com** is the enterprise domain.
- You may enter a secondary URL in the **Secondary User Location Service URL** field if desired. This DME is used in the event the first DME is not accessible from a viewer's location.
- Click the **Test **button next to either field to verify that the server(s) are available and retrieving IP addresses correctly.
- When a user plays a video or logs in to Rev, the system validates the user’s location through the Location Service and directs the user to the correct zone.
- The user’s location is cached for the remainder of the session.

## On Premise Rev

To specify a location services DME in an on-premise Rev installation, the exact steps described in cloud-hosted Rev are followed with the following exception:

- A DME customer cert does _not_ need to be installed **unless you are using https**. If you _are_ using https (Vbrick's recommendation), you need to install a tls certificate on the DME and follow the exact steps described above even if using on-premise Rev.