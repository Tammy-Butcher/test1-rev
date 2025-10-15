---
title: View DME Network Statistics
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
Use the **Devices** > **DME Network Statistics** menu to monitor the overall health, activity, and video usage statistics of each DME in your network.

<Image alt="Use DME Network Statistics to monitor the health and activity of each DME in your portal" align="center" src="https://files.readme.io/e43e54f-dmeNetworkStatsMenu.png">
  Use DME Network Statistics to monitor the health and activity of each DME in your portal
</Image>

Immediately displayed is health information for each DME including percentages used for **CPU**, **Memory** (including swap space), **Disk** space, and **Throughput**. The bar colors associated with health information are described in the table below.

If **DME Stream Authorization** is enabled, the **Used For Streaming** column displays either **Streaming** or **Error** depending upon if content is being sent to the DME.  **View**: [DME Stream Authorization Lockdown Management](doc:stream-authorization-lockdown)

<Image title="dmeNetworkActivity.png" alt={1202} align="center" src="https://files.readme.io/2900293-dmeNetworkActivity.png">
  Many columns are clickable and many labels may be rolled over for more details
</Image>

Clicking the **DME Name** displays a dropdown of more information about that specific appliance including **IP Address**, **MAC** address, and software **Version** (some data is not available for older DMEs prior to v3.6)

Four buttons also display that allow you to edit DME settings:

* **DME Administration**: Links to the DME Admin interface so you may edit settings as needed in the DME. You must know your DME Admin login information. Note: DME v3.14+ has implemented preventions that thwart Cross-Site Request Forgery (CSRF) prevention. Customers that select the DME Administration button may see a 500 error. If this occurs, click the reload the browser page and gain direct access.
* **Rev Configuration**: Links to DME **Device** settings in Rev for editing.
* **View Log**: Server logs for this DME. You are able to view specific actions that occur with the **Show Details** button on the log.
* **Reboot**: Reboots the DME.

<Image title="dmeNetworkTransratingStreams.png" alt={1202} align="center" src="https://files.readme.io/b47422e-dmeNetworkTransratingStreams.png">
  Click a specific DME Name to obtain more detailed information
</Image>

Admins can also view the following point in time server **Stream** usage information for each DME:

* Percentage of total available streams used by **incoming** versus **outgoing** streams

Admins can view the following point in time **Multi-Protocol Server (MPS)** server stream usage information for each DME:

* Percentage of total available streams used by **incoming** versus **outgoing** streams.

Admins can view a breakdown of Stream information for each streaming server, including:

* Number of **incoming** streams
* Number of outgoing **unicast** streams
* Number of outgoing **multicast** streams

Admins can view the percentage of usage of **Transrating Streams** for each DME (N/A is displayed if transrating is not licensed on the DME).

Admins can view the number of **Recordings** occurring on each DME.

DME versions prior to v3.6 do not display throughput or MPS server stream usage. If data cannot be retrieved from a DME because it is an older version, an indicator is displayed.

The table below illustrates the threshold values that are used for the health data that is reported for the DME. Each measure is a snapshot value (not trended) that the DME samples every 60 seconds.  The DME reports asynchronously every 60 seconds to Rev -- so there may be a lag in the reporting.  For these values, each threshold is indicated by color and corresponds to the following values: Normal (no color change), Caution (yellow), Alert (red).

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Health Data Reported
      </th>

      <th>
        Normal
      </th>

      <th>
        Caution
      </th>

      <th>
        Alert
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Throughput (reported in Mbps and percentage of outgoing (TX) bitrates against license)
      </td>

      <td>
        \< 60%
      </td>

      <td>
        60% - 90%
      </td>

      <td>
        > 90%
      </td>
    </tr>

    <tr>
      <td>
        CPU Usage (reported in percentage across cores)
      </td>

      <td>
        \< 70%
      </td>

      <td>
        70 - 80%
      </td>

      <td>
        > 80%
      </td>
    </tr>

    <tr>
      <td>
        Memory Usage (reported as aggregate total and percentage)
      </td>

      <td>
        \< 50%
      </td>

      <td>
        50 - 85%
      </td>

      <td>
        > 85%
      </td>
    </tr>

    <tr>
      <td>
        Disk Space (reported as total and percentage)
      </td>

      <td>
        \< 85
      </td>

      <td>
        85 - 90%
      </td>

      <td>
        > 90% or \< 32GB whichever is smaller
      </td>
    </tr>

    <tr>
      <td>
        Current Pulls
      </td>

      <td>
        1 - N
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Current Pushes
      </td>

      <td>
        1 - N
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Current VOD Retrievals (reported as number, with total allowance, and percentage of total)
      </td>

      <td>
        \< 70%
      </td>

      <td>
        70 - 85%
      </td>

      <td>
        > 85%
      </td>
    </tr>

    <tr>
      <td>
        Current Live Retrievals (reported as number, with total allowance, and percentage as total)
      </td>

      <td>
        \< 70%
      </td>

      <td>
        70 - 80%
      </td>

      <td>
        > 80%
      </td>
    </tr>

    <tr>
      <td>
        Overall DME Health (calculated status = max status  Data Reported",\
            "h-1": "Norm, as well as specific services running on the DME.  Additional status details can be found on DME.)
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        DME Mesh Status (count of reachable peers, total peers, percentage reachable) status based on percentage reachable
      </td>

      <td>
        > 50%
      </td>

      <td>
        20 - 50%
      </td>

      <td>
        \< 20%
      </td>
    </tr>
  </tbody>
</Table>
