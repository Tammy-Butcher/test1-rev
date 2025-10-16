---
title: Analytics FAQ
excerpt: >-
  Frequently Asked Questions are recorded here to assist you in analyzing the
  analytics you collect
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## Webcast Analytics FAQs

### AVERAGE ZONE BIT RATE

**Can you please explain the “average zone” portion of this metric and what is meant?**

> The metric displays an average of the average bit rate in each zone. The average bit rate provides administrators a quick validation that, on average, users are experiencing the intended stream quality.

**Can you please explain what is considered a Great||Good||Bad||Poor value for the metric?**

> The expected bit rate is highly dependent on the underlying source, network and Zone configuration. The delta between “expected” and “actual” is what potentially indicates great/good/poor for customers.

**What is the “Normal” or acceptable (Min/AVG/Max) threshold that is expected for this metric?**

> An administrator that is familiar with underlying network capabilities should be able to compare the average bit rate to the expected bit rate. If the average is significantly different than what is expected it may indicate a misconfiguration of the source, network, DMEs, or zones. For example, an average bit rate of 500Kbps would be great news in the case of an MBR stream source of 500Kbps and 256Kbps because it means most viewers are getting the best stream. 
>
> However, the same average bit rate of 500Kbps would be bad news in the case of an MBR stream source of 1.5Mbit and 500K bit as it would mean that most users received the lower quality stream.

**How does this metric provide information about the “Quality of Experience”?**

> To the extent that the actual bit rate is significantly different (less) than expected it may indicate that viewers had a lower quality viewing experience.

***

### AVERAGE ZONE BANDWIDTH

**Can you please explain the “average zone” portion of this metric and what is meant?**

> This metric displays an average of the average bandwidth in each zone.

**Can you please explain what is considered a Great||Good||Bad||Poor value for the metric? What is the “Normal” or acceptable (Min/AVG/Max) threshold expected for this metric?**

> An administrator familiar with the underlying network capabilities should be able to compare the average bandwidth to the expected bandwidth. If the average is significantly different than expected it may indicate a misconfiguration of the network, DMEs or zones.

**How does this metric provide information about the “Quality of Experience”?**

> To the extent that the actual bandwidth is significantly different (less) than expected it may indicate that viewers had a lower quality viewing experience.

***

### AVERAGE ZONE EXPERIENCED REBUFFERING

**Can you please explain the “average zone” portion of this metric and what is meant?**

> This metric displays an average of the average rebuffering experienced in each zone. Experienced rebuffering events are cumulative from the start of the Webcast and are defined as those rebuffering events that affect a user, typically with a visible “spinner”. This excludes event counts caused by the initial buffering at the beginning of an event.

**Can you please explain what is considered a Great||Good||Bad||Poor value for the metric?**

> A low average rebuffering event count and a low rebuffering duration are indications that end users did not suffer any pauses or spinners while viewing the Webcast. You should also look at these numbers in context of total number of attendees. A small number of rebuffering indicates few people had rebuffering events. The duration reflects the amount of time waiting for rebuffering for those attendees who had rebuffering events. It gives an indication that for those attendees that experienced rebuffering, this is how long (on average), they experienced a pause/spinner.

**What is the “Normal” or acceptable (Min/AVG/Max) threshold expected for this metric? How does this metric provide information about the “Quality of Experience”?**

> High rebuffering event counts may be an indication that a number of attendees experienced pauses and spinners while watching the Webcast.

***

### NUMBER OF EXPERIENCED REBUFFERING EVENTS THAT OCCURRED

**Can you please explain “rebuffering” versus “buffering” when used on analytic reports and dashboards?**

> Rebuffering excludes buffering event counts caused by the initial buffering at the beginning of an event. Experienced rebuffering events are cumulative from the start of the Webcast and are defined as those buffering events that affect a user, typically with a visible “spinner” occurring for a user.

**Can you please explain what is considered a Great||Good||Bad||Poor value for the metric? What is the “Normal” or acceptable (Min/AVG/Max) threshold that expected for this metric? How does this metric provide information about the “Quality of Experience”?**

> Under normal circumstances, a small number per user of rebuffering events is to be expected and typical. A large number (disproportionate to the number of users) may indicate some issues in the playback experience for users.

***

### MULTICAST ERRORS

**Can you please define what is meant by a Multicast Error and how they occur?**

> Often, the multicast error is an indication that a viewer switched from a multicast stream to a unicast stream for viewing the Webcast. Multicast errors are not always result in a failover, however, if that zone has not been configured for failover.

**Is there a place that these “Errors” are logged and stored? If so, how are they accessed? Should we be taking a deeper dive into these “Errors” when they are reported?**

> Vbrick does not currently expose the details of multicast errors / player errors via the Rev administrative UI. Vbrick does extensively log and surface aggregates as part of the analytics displayed for the event. Vbrick is continuously working to enhance Rev’s analytics and diagnostic capabilities and may expose more of the detailed / raw level details of multicast errors (and other player errors) in the future.

**Can you please explain what is considered a Great||Good||Bad||Poor value for the metric? What is the “Normal” or acceptable (Min/AVG/Max) threshold expected for this metric? How does this metric provide information about the “Quality of Experience”?**

> Under normal circumstances, if a Zone and its underlying network are configured for Vbrick multicast, then expect that a good proportion of the total attendees are consuming a multicast stream and a smaller number are consuming a unicast stream, and a small number of multicast error events to occur.

<br />
