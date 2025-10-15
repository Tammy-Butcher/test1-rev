---
title: Download a Vbrick Peer-to-Peer Zone Metrics Report
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
Clicking **Download **> **Vbrick Peer-to-Peer - CSV** downloads details about Vbrick Peer-to-Peer zones once the event has ended but _only_ if they are enabled for the event.  If no zones are [Vbrick Peer-to-Peer enabled](doc:rev-connect-zones), this option is not visible.

> 🚧 Important!
> 
> If the **Hide User-Level Analytics** checkbox is enabled under [Content Restrictions](doc:hide-user-level-analytics), neither the **Attendees** nor the **Vbrick Peer-to-Peer** CSV file exports will be available for download, including to Admin accounts.

Each line within the Vbrick Peer-to-Peer report represents one user within a Peer Mesh. In most cases, users join a single **Peer Mesh** for an entire event and, therefore, there is only one entry. However, if a user joins or rejoins one or more Peer Meshes, a line is added for each instance. This provides different user experiences based on membership in different Peer Meshes available to the analyst during review. The **UserID** should be used for grouping information about specific Users – and UserID is the same and used for correlation to the [Webcast Event Attendees](doc:webcast-reports#download-attendee-metrics) report.

If viewed as a table (as in Excel), the first set of columns focus on the **User **(or viewer) characteristics. They include:

- Attendee Full Name (First Name / Last Name)
- Account Username
- UserID
- Email Address
- Session ID
- Zone Name
- IP Address
- Browser Used
- Origin URL

***

Columns after User characteristics focus on **Peer Mesh** data. They include:

**Peer Mesh GUID** - The Peer Mesh GUID is an unique ID representing a Peer Mesh. During analysis, this item can be used in a number of ways to:

- Identify how many Peer Meshes were in this event (by counting unique Peer Mesh GUIDs)
- Identify the timing life cycle of the Peer Mesh with start of this Peer Mesh (earliest Time In) and the end of the Peer Mesh (latest Time Out)
- Grouping within Peer Mesh for analysis of:
- Review User IPs for validation of the Peer Mesh membership (defined within the Zone settings for Peer Mesh)
- Compare Peer Mesh metrics (defined below)

***

**Peer Mesh Shares Out** (number of segments that this viewer provide to another peer)

This is the number of segments that this viewer, in this particular Peer Mesh, has shared to another peer. Higher number represents more sharing. Higher numbers are not necessarily good nor bad, but should be considered if a user is sharing too much. The Samaritan Load measure below expands on this and provides a consistent way to compare different users and their sharing behavior.

***

**Peer Mesh Shares In** (number of segments that this viewer gets from another peer)

This is the number of segments that this viewer got from another another peer. Higher numbers represent getting more shares from peers and a better use of bandwidth.

***

**Origin Gets**

This is the number of segments that this viewer has gone to origin (i.e., not a peer) to retrieve. While it is important that this number be low, it should also be realized that “someone” (some viewer) will have to go to origin to get it. This should always be evaluated in reference to Peer Mesh Shares Out, Peer Mesh Shares In and Total Segments. Having one (or a few) peers bear the load of many Origin Gets is not necessarily indicative of a problem.

***

**Time In**

This is the time viewer enters this Peer Mesh. Viewers may be assigned to different Peer Meshes across an event, so please use this value with Time Out and all analysis should look for multiple entries per user.

***

**Time Out**

Like Time In, This is the time viewer leaves this Peer Mesh. Viewers may be assigned to different Peer Meshes across an event, so please use this value with Time In and all analysis should look for multiple entries per user.

***

**Total Segments In**

This is the number of segments that the viewer requested within the peer mesh. This is the number of **Peer Mesh Shares In** (how many they get from other peers) + **Origin Gets** (this is the number of origin retrievals).

***

The following calculated percentages provide an insight to where (in percentage) the current user (within the peer mesh) is getting content (either via sharing from peers or going to origin), and how much user is sharing. While these are meaningful at the viewer level, they should not be used for an indication of the efficiency across the peer mesh.

**Viewer Peer Mesh Efficiency (Peer Mesh Shares In / Total Segments In) \* 100**

This is a viewer specific calculated measure. It represents the ratio/percentage of **Peer Mesh Shares In** (number of segments this viewer gets from peers) to the **Total Segments In** (total number of segments played, in from peers + origin gets).

In other words: This is the percentage of segments that a viewer got from a peer.

- The higher the value, the more that this viewer is using the peer mesh to get content. The lower the value, the more this viewer is going to origin.

***

**Viewer Peer Mesh Origin Load (Origin Gets / Total Segments In) \* 100** 

This is a viewer specific calculated measure, and the flip side of the Viewer Peer Mesh Efficiency. Meaning **Viewer Peer Mesh Origin Load** + **Viewer Peer Mesh Efficiency** = 100%.

This number represents the ratio/percentage of **Origin Gets** (number of segments this viewer goes to origin for) to the **Total Segments In** (total number of segments played, in from peers + origin gets).

In other words: This is the percentage of segments that a viewer needed to go to origin.

- The higher the value, the more this viewer is going to origin. The lower the value, the more that this viewer is using the peer mesh to get content.

***

**Viewer Peer Mesh Samaritan Load (Peer Mesh Shares Out / Total Segments In ) \* 100** 

This is a viewer specific calculated measure. It represents the ratio of how many times this user has shared with other peers to the total number of segments. This provides a quantitative measure to “How actively does this viewer share?” or “How good a Samaritan is this viewer in this Peer Mesh?”

This number represents the ratio of **Peer Mesh Shares Out** (how many times this user shared to another peer) to **Total Segments In** (total segments that could be shared, Shares IN + Origin Gets). This measure is provided as a ratio/percentage, but can be > 100%.

In other words: This is the percentage of how often this viewer shares to peers.

- Higher numbers mean this viewer is sharing more (supplying segments to more peers.) Lower numbers represent a lack of sharing from this peer.

***

The next set of calculated measures represent Peer Mesh wide characteristics. These are common/duplicated across each User within the Peer Mesh. Meaning, these measures will be the same for all Users within a particular Peer Mesh, and are provided in this manner for direct comparison to the Viewer specific measures identified above.

**Mesh Peer Mesh Share Efficiency = ( Sum(Peer Mesh Shares In) / Sum(Total Segments In))** 

This is a Peer Mesh specific calculated measure. It represents the ratio of how many times all the users got segments from peers to the total number of segments for all users. This provides a quantitative measure to “Is this Peer Mesh sharing efficiently?”

In other words: This percentage represents how often we are sharing.

- Higher numbers mean better sharing within this Peer Mesh. Target should be > 90%. Lower numbers represent a lack of sharing within this Peer Mesh.

Do not confuse **Viewer Peer Mesh Efficiency** with **Mesh Peer Mesh Share Efficiency**. Each metric identifies scope by the first word, either Viewer (the single viewer) or Mesh (the single Peer Mesh) scope.

***

**Mesh Peer Mesh Origin Efficiency = ( Sum(Origin Gets) / Unique (Origin Gets) ) \* 100** 

This is a Peer Mesh specific calculated measure that spans each Cluster. It represents the ratio of how many times (across all the users) there were origin retrievals for a segment to the number of unique segments. This provides a quantitative measure to “Is this the Peer Mesh Cluster going to origin too much?”

In other words: This ratio  represents the number of times we go to origin to get segments against all unique segments for all Peers in Peer Meshes in individual Clusters.

For example, if the metric is 100 – that means we only ever go to origin once per segment (i.e., All Origin Gets == Unique Origin Gets). This implies that the users share that segment optimally between each other within the Peer Mesh (because, otherwise, there would be additional Origin Gets).  

For a Peer Mesh Cluster size of 1, 100 is the optimal result, but rarely achievable due to inherent timing between communicating peers.  For this Cluster size, we strive for an efficiency value of 100-125.  (Meaning, if the metric is 125, this equates to, on average, going to origin 5 times for 4 unique segments.)

For larger Cluster sizes (up to 10), the **Mesh Peer Mesh Origin Efficiency**  could vary more, and lower is better.  But event larger numbers, with multiple Peer Meshes, represents savings.  For example, if you have 10 Peer Meshes non-clustered, then the best measure would be 100 per Peer Mesh -- or, going to origin once per TS segment for each Peer Mesh (sharing across all viewers within mesh).  If those Peer Meshes were clustered, but still have the same go to origin, then the  **Mesh Peer Mesh Origin Efficiency** would equate to 1000.  In practice, anything below that would indicate savings, and our tests often come in around 100-200 for larger Cluster sizes.  Said another way, a measure of 200 is going to origin twice to service your multiple Peer Meshes -- which for 3 or more Peer Meshes is added bandwidth savings.

**Guidance**: 

- If Peer Mesh Cluster size = 1, then strive for **Mesh Peer Mesh Origin Efficiency** value of 100-125
- For larger Cluster size N, then strive for **Mesh Peer Mesh Origin Efficiency** value of (100-125)\*N/2

**Are higher values bad?** Higher values indicate more origin gets across all users, and hence more bandwidth used. High values of this metric are most impactful on Peer Meshes or Peer Mesh Clusters that exist on networks with reduced or restricted bandwidth. Networks with additional bandwidth can service more origin calls on average.

**How do I effect change on Mesh Peer Mesh Origin Efficiency?** There are multiple reasons why this metric could be driven up, and if most often unique per network. A primary cause is network induced latency between Peer Mesh constituents/viewers. A large latency between communicating peers will time-out resulting in more requests driven to origin.

Examine your Vbrick Peer-to-Peer membership rules on the Zones page. Only allow Peer Meshes to be comprised of “close” (restricted to a small geographical/network grouping) viewers.  Remember that mDNS is used by Browsers that are obfuscating address cannot share across sub-nets -- which would also reduce your efficiency. 

Consider the size and structure of your HLS stream. Smaller segment sizes, while reducing latency, increase the communication load across all peers and the network. Larger sizes allow for more time to communicate between peers.

Do not confuse **Viewer Peer Mesh Origin Load** with **Mesh Peer Mesh Origin Efficiency**. Each metric identifies scope by the first word, either Viewer (the single viewer) or Mesh (the single Peer Mesh) scope.

***

**Peering efficiency (Percent of Bytes Saved/ 1- Network Consumption for the user in the event)** 

This includes:

- Peer Cluster (Zone-[group] - [clusterset] - [clusterid]) - displays the last one the user was in.
- Peering Shares Sent
- Peering Shares Received
- Peering Origin Gets
- Total Peering Segments (Total Segments In or Peering Shares Received plus Origin Gets)
- Peering Bytes Saved (For the user in that event) 

If the user was not a member of a peer mesh, these fields are blank.