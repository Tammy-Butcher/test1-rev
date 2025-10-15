---
title: Set Up an STB Connector DME
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
If you want to display video assets from Rev to a **Vbrick MF-STB (Multi-format Set Top Box)**, you must do so with a DME that acts as a connector between Rev and the STB.

> 👍 Tip
> 
> Vbrick MF-STBs are also referred to as simply Set Top Boxes, or STBs.

STBs send out periodic multicast **SAP (Session Announcement Protocol)** messages and the DME is able to “listen” for them. These messages contain the information necessary for the DME and Rev to connect and communicate with the STB.

You must designate which DMEs are the **STB Connector** so that they “listen” for STBs in your network. The DMEs actively communicate the found STBs \_to \_Rev where they then appear under **Devices **> **Set Top Boxes** > **Pending STBs** for you to configure.  DMEs must be **Active **and set up correctly before you can set it as an STB Connector DME.

To designate a DME as a STB Connector DME:

1. Navigate to **Devices **> **DME Management** and edit the DME you want to designate as the STB Connector. Remember, each STB is sending out SAP announcements and for Rev to see and use the STB, it must be reachable/visible by a STB Connector DME. STBs that cannot reach a DME cannot be integrated with Rev.

2. Select the **Set Top Box Control** check box. Each of the fields below are auto-discovered for STBs in your network.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c2935ec-stbCheckbox.png",
        "stbCheckbox.png",
        505
      ],
      "align": "center",
      "caption": "When the Control Set Top Boxes checkbox is selected, the STB fields are auto discovered by Rev"
    }
  ]
}
[/block]

- **IP Address** - The IP Address is the **SAP Announcement IP Address ** where the STB multicasts their SAP announcements. The DME uses the SAP Announcement IP address and Port to receive STB information.
- **Port **- The port the STB uses along with the SAP Announcement IP Address to send out the information for each STB. The DME  uses the SAP Announcement IP address and Port to receive STB information.
- **User Name** - The default User Name that is used for initial communication between the DME and STB. If STBs have unique User Names or Passwords, those can be customized from the **Set Top Box Management** module in Rev by editing the STB credentials.
- **Password **- The default Password that is used for initial communication between the DME and STB. If STBs have unique User Names or Passwords, those can be customized from the **Set Top Box Management** module  in Rev by editing the STB credentials.

3. Click **Update **save the DME as a **DME Connector**. The DME begins “listening” for set top boxes on the network and each one found appears on the **Devices **>  **Set Top Boxes** > **Pending STBs** tab. 

4. You can accept any of those found as **Current STBs** and configure channel settings.

5. You can see at a glance which DMEs are **STB Connector DMEs** in the **MFSTB **column on the **DME Management** module.

> 🚧 Important!
> 
> **A Note on STB SAP broadcasts:**
> 
> These SAP announcements are multicast and \_cannot \_go over the general Internet. Therefore, a local DME is necessary to intercept them and send them to Rev. Rev \_cannot \_communicate directly to the STB as noted. 
> 
> If your STBs are on a **non-multicast** network, then a **direct connection** needs to be made between each STB and DME.
> 
> This means, for each non-multicast network STB:
> 
> - You need to **SSH/login** to each STB and edit the /data/config.txt file. 
> - Change the `stb.sap.packet.addr` parameter from the default multicast IP Address of `224.2.133.134` to the IP Address of your **STB Connector DME** and then reboot. 
> 
> You can keep the **default ** `224.2.133.134` **IP Address** setting and the default `9876` **Port **setting in the **Set Top Box Control** section of the STB Connector DME's device settings in Rev's configuration (seen below).
> 
> This feature only works with the Vbrick MF-STB on **v2.0.1** or greater.