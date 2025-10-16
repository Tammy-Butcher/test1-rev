---
title: Zones in Real-Time
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
The **Zones** tab filters data in real-time by zone.

<Image title="zonesTab.png" alt={1799} align="center" src="https://files.readme.io/9d414be-zonesTab.png">
  Use the Column control to filter Zone metrics in the Real-Time Dashboard
</Image>

The **Column** control filters various ongoing zone analytics in real-time. Selecting the top level metric selects all the child metrics under it. Some use case examples are detailed below.

## View Number of Attendees By Zone

**ZONE NAME**

Displays the name of the network Zone. A Zone represents a set of IP address ranges and is configured by the administrator to model the routing of video stream requests to the most appropriate device to serve the content (typically a DME). An administrator for example may define a Zone to represent a wireless network and use a separate Zone to define the wired network.

**What to expect?**\
An event administrator should expect to see all Zones participating in the Webcast to be represented in the list.

**How can this information be used?**\
An event administrator can leverage the list of Zones to verify that the expected zones are represented. Should expected Zones not be represented, it may be an indication that there is a misconfiguration of the Zone or network improperly routing users to the wrong Zone.

**ATTENDEES**

Displays the total count of attendees currently viewing the Webcast per Zone. Please note that the count may include attendees who have recently left the Webcast (within 3 minutes of leaving).

**What to expect?**\
Under normal circumstances the total number of attendees in the Zone should match the administrator’s expectations for typical attendance for a Webcast in that Zone.

**How can this information be used?**

An event administrator can gauge if the number of attendees in the Zone matches the expectations they had for that Zone. A significantly smaller number or larger number may indicate an incorrectly configured Zone routing or network.

A larger number of attendees on a Zone than expected may indicate a need to add additional DMEs or increase the size of the DME in the Zone.

## View Average Bit Rate By Zone

The **Avg. Bit Rate (Kbps)** column displays the average bit rate across Webcast viewers per Zone. The average bit rate can give administrators a quick validation that on average users are experiencing the intended stream quality.

**What to expect?**\
The expected bit rate is highly dependent on the underlying network and Zone configuration.

**How can this information be used?**\
An administrator that is familiar with the underlying network capabilities of the Zone should be able to compare the average bit rate to the expected bit rate. If the average is significantly different than what would be expected it may indicate a misconfiguration of the network, DME or zone and may be an indication that users on that Zone may be experiencing a lower quality stream.

## View Number of Experienced Rebuffering Events By Zone

The **Experienced Rebuffering Count** column displays the number of buffering events that have occurred in each zone since the start of the Webcast (by zone). Rebuffering events are those that actually affect a user’s experienced versus those that do not. This is normally indicated visibly through the display of a progress spinner. This excludes spinner event counts caused by the initial buffering at the beginning of an event.

**What to expect?**\
Under normal circumstances a number of rebuffering events is to be expected, typically a small number per user in the Zone. A large number (disproportionate to the number of users in the Zone) may indicate some issues in the playback experience for users in that Zone.

**How can this information be used?**\
An event administrator can leverage this information to get an idea of the overall experience a set of users have had in watching the Webcast in that Zone.

View: [Configure a Rebuffering Threshold for Webcasts](https://rev.readme.io/docs/enable-or-disable-features#configure-rebuffering-threshold-for-webcast-events)

## View Number of Unicast and Multicast Streams

The **Unicast Connections** and **Multicast Connections** columns display the number of unicast and multicast streams in each zone during the webcast.

**UNICAST**

Displays the total count of Webcast viewers in the Zone leveraging a unicast stream to consume the Webcast.

**What to expect?**\
Under normal circumstances, if a Zone and its underlying network has been configured for Vbrick multicast, then one should expect that a good proportion of the total attendees in the Zone would be consuming a multicast stream and a smaller number to be consuming a unicast stream.

**How can this information be used?**\
An event administrator can gauge if the number of attendees in the Zone consuming a unicast stream matches the expectations they had for that Zone. A significantly larger number of unicast streams than expected (when expectations were for larger number of multicast streams) may be an indication of misconfigured Zone or network.

**MULTICAST**

Displays the total count of Webcast viewers leveraging a multicast stream to consume the Webcast.

**What to expect?**\
Under normal circumstances, if a Zone and its underlying network has been configured for Vbrick multicast, then one should expect that a good proportion of the total attendees would be consuming a multicast stream and a smaller number to be consuming a unicast stream.

**How can this information be used?**\
An event administrator can gauge if the number of attendees in the Zone consuming a multicast stream matches the expectations they had for that Zone. A significantly larger number of unicast streams than expected (when expectations were for larger number of multicast streams) may be an indication of misconfigured Zone or network.

An event administrator may also look to the multicast failover statistic in conjunction with this metric.

## View Number of Multicast Error Events

The **Multicast Error Events** column displays the number of multicast error events that have occurred in each zone since the start of the Webcast. A multicast error is an indication that a viewer switched from a multicast stream to a unicast stream for viewing the Webcast.

**What to expect?**\
Under normal circumstances, if a Zone and its underlying network has been configured for Vbrick multicast, then one should expect that a good proportion of the total attendees would be consuming a multicast stream and a smaller number to be consuming a unicast stream, so would expect a small number of multicast error events.

**How can this information be used?**\
A high number may be an indication that the multicast setup for the network may not be configured correctly.

## View Number of Users By Vbrick Peer-to-Peer Zone

The **Vbrick Peer-to-Peer Meshes** and **Vbrick Peer-to-Peer Viewers** columns displays the number of viewers using Vbrick Peer-to-Peer in existing peer meshes (that have been created) per zone.

Vbrick Peer-to-Peer needs to be enabled and the Zone needs to be configured to use Vbrick Peer-to-Peer for this column to display. This column shows both the number of Vbrick Peer-to-Peer viewers (users) and the number of peer meshes.

**What to expect?**\
The column is formatted with two numbers:

* Vbrick Peer-to-Peer Viewers / # Peer Meshes

The number of **Vbrick Peer-to-Peer Viewers** is provided first. These are the viewers, in the Zone, that are currently utilizing Vbrick Peer-to-Peer. The number of peer meshes is indicated by the second number. For example, 12/2 indicates that there are 12 viewers spread across 2 peer meshes in the associated zone.

The number of **Peer Meshes** can range from 0 up to the maximum number of Peer Meshes defined within the Zone. Each Peer Mesh can support a limited number of viewers, and they are not guaranteed to have equal (in number) membership of viewers.

**How can this information be used?**\
An event administrator can leverage this information to see, in real time, the use of Vbrick Peer-to-Peer and how many Peer Meshes have been created. Detailed information and metrics can be downloaded from the Vbrick Peer-to-Peer Zone Report at the end of the event.