---
title: Devices in Real-Time
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
The **Devices** tab filters data in real-time by device.

<Image title="devicesTab.png" alt="1800" align="center" src="https://files.readme.io/38ae8b7-devicesTab.png">
  Use the Column control to filter Device metrics in the Real-Time Dashboard
</Image>

The **Column** control filters various ongoing device analytics and status updates in real-time. Selecting the top level metric selects all the child metrics under it. Some use case examples are detailed below.

## View DME Status By Zone

The DME **Status** column displays icons indicating DME status in each zone. This icon is an indicator for all DMEs in the applicable zone. Hovering over the icon will display a tool tip indicating the status for the zone.

If there are no DMEs in the zone, this column will be empty.

**DME STATUS INDICATOR**

A red, yellow, green indicator highlighting a potential issue with one or more DMEs contained in the Zone and may indicate a need for an administrator to investigate / drill down to get more details.

**What to expect?**\
Under normal circumstances the Zones and their DMEs should all reflect green (normal) indicators.

**How can this information be used?**\
An event administrator can use the Zone statistics and DME status to narrow down to areas of the Rev eCDN that may require attention. Note that it is possible that temporary spikes in CPU or memory usage could result in DME showing as yellow or red. In that circumstance, it is important to keep an eye on such status and check if they were temporary in nature or appear constant as these may indicate an actual issue that the Admin should investigate.

Status color indicators for the DMEs in each zone are defined as follows:

| Icon        | Status Meaning                                                                                                                                                                                               |
| :---------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Normal      | Only displayed if *all* DMEs in the zone return a status of **Normal**.                                                                                                                                      |
| Caution     | Displayed if the overall status for at least *one* DME in the zone returns a **Caution** alert (and *none* return a **Red** alert).                                                                          |
| Alert       | A **Red** alert for the zone will *always* be displayed if the overall status for at least *one* DME in the zone returns a **Red** Alert (regardless of the overall status of *all* other DMEs in the zone). |
| Unavailable | If Rev has not received a DME status update for the last three minutes or if the DME is uninitialized then the DME column will display as **Unavailable**.                                                   |

Clicking a **Caution** or **Red** alert within a zone expands the DME **Status** window so that you are able to view active DMEs in the zone to view more details.

<hr />

**CPU STATUS INDICATOR**

CPU status represents a recent snapshot (updated every 60 seconds or so) of CPU utilization on the DME.

**What to expect?**\
CPU utilization below 50% is viewed as normal. CPU utilization will be shown in yellow when it reaches between 50% and 85% and will be shown in red when above 85%. Both of these are indications that a host administrator should pay attention to the CPU utilization and monitor if CPU utilization remains high over time.

**How can this information be used?**\
An event administrator should investigate cases where CPU utilization stays above normal for an extended period of time as this may indicate a need to better distribute load across other DMEs or a possible upgrade to the DME to a larger system is needed.

<hr />

**MEMORY STATUS INDICATOR** 

Memory status represents a recent snapshot (updated every 60 seconds or so) of memory utilization on the DME.

**What to expect?**\
Memory utilization below 50% is viewed as normal. Memory utilization will be shown in yellow when it reaches between 50% and 85% and will be shown in red when above 85%. Both of these are indications that a host administrator should pay attention to Memory utilization and monitor if Memory utilization remains high over time.

**How can this information be used?**\
An event administrator should investigate cases where Memory utilization stays above normal for an extended period of time as this may indicate a need to better distribute load across other DMEs or a possible upgrade to the DME to a larger system is needed.

<hr />

**THROUGHPUT (MBPS) STATUS INDICATOR**

Throughput represents a recent snapshot (updated every 60 seconds or so) of MPS throughput on the DME.

**What to expect?**\
Throughput utilization below 60% of licensed throughput is viewed as normal. Throughput utilization will be shown in yellow when it reaches between 61% and 90% and will be shown in red when above 91%. Both of these are indications that a host administrator should pay attention to the Throughput utilization and monitor if utilization remains high over time.

**How can this information be used?**\
An event administrator should investigate cases where Throughput utilization stays above normal for an extended period of time as this may indicate a need to better distribute load across other DMEs or a possible upgrade to the DME to a larger system is needed.

<hr />

## View Devices By Zone

The **Device** column details the types of devices which are connected to the Webcast.

**How can this information be used?**\
An event administrator can monitor the types of devices in use and compare to their expectations.