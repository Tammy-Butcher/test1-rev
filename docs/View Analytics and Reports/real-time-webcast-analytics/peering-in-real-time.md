---
title: Peering in Real-Time
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
The **Peering** tab filters Vbrick Peer-to-Peer peering efficiency in real-time. This is the primary metric for showing the percentage of bandwidth saved when using Vbrick Peer-to-Peer.

<Image border={false} src="https://files.readme.io/6acea2a-peeringTab.png" title="peeringTab.png" />

The Column control filters various ongoing peering analytics in real-time. Selecting the top-level metric selects all the child metrics under it. Some use case examples are detailed below.

## View Efficiency By Peer Cluster

The **Efficiency** column displays the percentage of bandwidth saved by users viewing the live event using Vbrick Peer-to-Peer.

**What to expect?**
The efficiency column should increase with the number of users connected to a peer cluster.

**How can this information be used?**
This information can indicate if there could be a connectivity or sharing issue for users within a cluster or Zone.

***

## View Avg Bitrate By Peer Cluster

The average bitrate being consumed by users within a peer mesh

**What to expect?**
The average bitrate can be influenced by available bandwidth, peering efficiency or even workload or CPU usage of devices in that cluster.

**How can this information be used?**
A lower average bitrate could indicate lower-quality video being delivered within the cluster. This can be influenced by the number of users who can share segments, overall network throughput or by adding an edge cache within that Zone.
