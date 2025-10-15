---
title: View DME Network Statistics
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
Use the **Devices **> **DME Network Statistics** menu to monitor the overall health, activity, and video usage statistics of each DME in your network.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e43e54f-dmeNetworkStatsMenu.png",
        null,
        null
      ],
      "align": "center",
      "caption": "Use DME Network Statistics to monitor the health and activity of each DME in your portal"
    }
  ]
}
[/block]

Immediately displayed is health information for each DME including percentages used for **CPU**, **Memory **(including swap space), **Disk **space, and **Throughput**. The bar colors associated with health information are described in the table below.

If **DME Stream Authorization **is enabled, the **Used For Streaming** column displays either **Streaming **or **Error **depending upon if content is being sent to the DME.  **View**: [DME Stream Authorization Lockdown Management](doc:stream-authorization-lockdown)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2900293-dmeNetworkActivity.png",
        "dmeNetworkActivity.png",
        1202
      ],
      "align": "center",
      "caption": "Many columns are clickable and many labels may be rolled over for more details"
    }
  ]
}
[/block]

Clicking the **DME Name** displays a dropdown of more information about that specific appliance including **IP Address**, **MAC** address, and software **Version **(some data is not available for older DMEs prior to v3.6)

Four buttons also display that allow you to edit DME settings:

- **DME Administration**: Links to the DME Admin interface so you may edit settings as needed in the DME. You must know your DME Admin login information. Note: DME v3.14+ has implemented preventions that thwart Cross-Site Request Forgery (CSRF) prevention. Customers that select the DME Administration button may see a 500 error. If this occurs, click the reload the browser page and gain direct access.
- **Rev Configuration**: Links to DME **Device **settings in Rev for editing.
- **View Log**: Server logs for this DME. You are able to view specific actions that occur with the **Show Details** button on the log.
- **Reboot**: Reboots the DME.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b47422e-dmeNetworkTransratingStreams.png",
        "dmeNetworkTransratingStreams.png",
        1202
      ],
      "align": "center",
      "caption": "Click a specific DME Name to obtain more detailed information"
    }
  ]
}
[/block]

Admins can also view the following point in time server **Stream **usage information for each DME:

- Percentage of total available streams used by **incoming **versus **outgoing **streams

Admins can view the following point in time **Multi-Protocol Server (MPS)** server stream usage information for each DME:

- Percentage of total available streams used by **incoming **versus **outgoing **streams.

Admins can view a breakdown of Stream information for each streaming server, including:

- Number of **incoming **streams
- Number of outgoing **unicast **streams
- Number of outgoing **multicast **streams

Admins can view the percentage of usage of **Transrating Streams** for each DME (N/A is displayed if transrating is not licensed on the DME).

Admins can view the number of **Recordings **occurring on each DME.

DME versions prior to v3.6 do not display throughput or MPS server stream usage. If data cannot be retrieved from a DME because it is an older version, an indicator is displayed.

The table below illustrates the threshold values that are used for the health data that is reported for the DME. Each measure is a snapshot value (not trended) that the DME samples every 60 seconds.  The DME reports asynchronously every 60 seconds to Rev -- so there may be a lag in the reporting.  For these values, each threshold is indicated by color and corresponds to the following values: Normal (no color change), Caution (yellow), Alert (red).

[block:parameters]
{
  "data": {
    "h-0": "Health Data Reported",
    "h-1": "Normal",
    "h-2": "Caution",
    "h-3": "Alert",
    "0-0": "Throughput (reported in Mbps and percentage of outgoing (TX) bitrates against license)",
    "0-1": "\\< 60%",
    "0-2": "60% - 90%",
    "0-3": "> 90%",
    "1-0": "CPU Usage (reported in percentage across cores)",
    "1-1": "\\< 70%",
    "1-2": "70 - 80%",
    "1-3": "> 80%",
    "2-0": "Memory Usage (reported as aggregate total and percentage)",
    "2-1": "\\< 50%",
    "2-2": "50 - 85%",
    "2-3": "> 85%",
    "3-0": "Disk Space (reported as total and percentage)",
    "3-1": "\\< 75%",
    "3-2": "75 - 85%",
    "3-3": "> 85% or \\< 32GB whichever is smaller",
    "4-0": "Current Pulls",
    "4-1": "1 - N",
    "4-2": "",
    "4-3": "",
    "5-0": "Current Pushes",
    "5-1": "1 - N",
    "5-2": "",
    "5-3": "",
    "6-0": "Current VOD Retrievals (reported as number, with total allowance, and percentage of total)",
    "6-1": "\\< 70%",
    "6-2": "70 - 85%",
    "6-3": "> 85%",
    "7-0": "Current Live Retrievals (reported as number, with total allowance, and percentage as total)",
    "7-1": "\\< 70%",
    "7-2": "70 - 80%",
    "7-3": "> 80%",
    "8-0": "Overall DME Health (calculated status = max status  Data Reported\",  \n    \"h-1\": \"Norm, as well as specific services running on the DME.  Additional status details can be found on DME.)",
    "8-1": "",
    "8-2": "",
    "8-3": "",
    "9-0": "DME Mesh Status (count of reachable peers, total peers, percentage reachable) status based on percentage reachable",
    "9-1": "> 50%",
    "9-2": "20 - 50%",
    "9-3": "\\< 20%"
  },
  "cols": 4,
  "rows": 10,
  "align": [
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]