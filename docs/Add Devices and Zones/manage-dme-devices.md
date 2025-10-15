---
title: Manage and Add DMEs
excerpt: >-
  This guide explains how to use the DME Management module to add, configure,
  and manage Vbrick DMEs.  This includes bulk schedule, reboot, and software
  update actions.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:html]
{
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>&#128187; <a href=\"/docs/vbrick-distribution\">Vbrick Distribution</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]

Vbrick's **Distributed Media Engine** (DME) is a versatile, highly-configurable media distribution engine that moves streaming video to and from a wide variety of sources and endpoints. With the DME you can distribute your video to anyone, anywhere, using a variety of robust IP networking options. In Rev, DMEs are added as a **Device **and are designated as the **Viewing Destinations** of your video content on the network.

The **DME Management** module is where DMEs are added and managed.  This module is where most actions and information about your DMEs is conducted and viewed. Account Admins access the DME Management module from **Devices **> **DME Management**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/71c4e72-dmeManagement.png",
        "dmeManagement.png",
        1202
      ],
      "align": "center",
      "caption": "Account Admins use the DME Management module to obtain information and perform configuration options on their DME devices"
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Column",
    "h-1": "Description",
    "0-0": "Name",
    "0-1": "Name or Host name of the DME.",
    "1-0": "Version",
    "1-1": "The current build version of the DME.",
    "2-0": "MAC Address",
    "2-1": "The MAC address of the DME.",
    "3-0": "Scheduled Download",
    "3-1": "Specifies if the DME has scheduled download times.",
    "4-0": "Status",
    "4-1": "The status of the device; **Online**, **Offline**, or **Inactive**.  \n  \nIf Inactive, the DME is not accessible by Rev. During a software update, the progress of the update is also displayed here.",
    "5-0": "Used For Streaming",
    "5-1": "Specifies if the DME is authorized for [streaming](doc:stream-authorization-lockdown) and not in lockdown status.",
    "6-0": "MFSTB",
    "6-1": "Specifies if the DME is designated as a [STB Connector DME](doc:set-up-an-stb-connector-dme).",
    "7-0": "Actions",
    "7-1": "The **Actions **dropdown functions:  \n  \n<li>**Sync Now**: Perform an immediate [synchronization](doc:synchronize-dme-content).</li>  \n<li>**Reboot**: Reboot the selected DMEs. This bulk reboots all selected DMEs or a single DME if only one is selected.</li>  \n<li> **View Log**: View a log of recent actions that have occurred on the device. This is good for troubleshooting if your device is not performing as expected.</li>  \n<li>**Request Logs**: Gathers necessary logs from the DME and sends them securely to Vbrick Support. (Requires DME v3.24+. This can also be completed in **Bulk Actions** with one ore more DMEs selected. Do not complete this action during events as it can be labor intensive. An email and notification is generated when the logs are complete and support is able to view them. </li>  \n<li> **Delete**: When a device is deleted, the content stored on the device is not deleted. However, you may not access it because the association to the device is removed. </li>",
    "8-0": "Bulk Actions",
    "8-1": "Bulk Actions that may be taken on multiple DMEs:  \n  \n<li>**Reboot**: Reboots the selected DMEs. You must have at least one DME selected.</li>  \n<li> **Scheduled Download**: Set up an identical [download schedule](doc:synchronize-dme-content#bulk-schedule-dme-content) for several DMEs at once. </li>  \n<li> **Update**: Update the [software version](doc:update-dme-software-version) for one or more DMEs.</li>  \n<li> **Request Logs**: Request the logs of one or more DMEs be sent to Vbrick Support. Must have v3.24+ of the DME software installed.</li>"
  },
  "cols": 2,
  "rows": 9,
  "align": [
    "left",
    "left"
  ]
}
[/block]