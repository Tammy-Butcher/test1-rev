---
title: Real-Time Webcast Analytics
excerpt: >-
  Understand the quality of the streaming experience in real-time for your Live
  webcasts using Rev's Real-Time Dashboard.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
Rev provides access to a **Real-Time Dashboard** during your Live webcasts. This allows you to gain insights on streaming <<glossary:bit rate>> and user <<glossary:bandwidth>> to understand network performance and optimize video for any location and device.

> 📘 Note
> 
> The Real-Time Dashboard is a Rev Cloud only feature.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7549cf8-realTimeDashIcon.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


When the **Real Time Dashboard** icon is clicked, the dashboard opens in a separate window from the ongoing webcast.

## Webcast Key Performance Indicators

The webcast **Key Performance Indicators (KPIs)** are displayed at the top of the dashboard and let you easily compare performance across webcast currently in progress. With KPIs, you can quickly visualize the number of attendees, rebuffering, and any errors that are occurring immediately.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c6b2219-dashboardKPI.png",
        "dashboardKPI.png",
        1795
      ],
      "align": "center",
      "caption": "Live Webcast Key Performance Indicators (KPIs) are displayed first"
    }
  ]
}
[/block]


### Current Attendees

Displays the number of attendees currently viewing the Webcast. Please note that the count may include attendees who have recently left the Webcast. You can also see a line chart that shows the trend of attendees in the Webcast.

**What to expect?**  
Under normal circumstances the total number of attendees should match the typical attendance for a Webcast.

**How can this information be used?**  
An administrator can leverage the total number of attendees to get a quick read on the current state of the Webcast in comparison to the expected number of attendees. If the number of attendees is significantly lower than expected number, it may indicate an issue with the Webcast.

<hr>

### Experienced Rebuffering (%)

Percentage of seconds of rebuffering over total Viewing Time.

**What to expect?**  
This metric gives you a sense for the amount of time users are spending rebuffering. Ideally this number is less than .5% and a reading over 1% could indicate a problem with users receiving the video.

**How can this information be used?**  
This metric can be compared with previous Webcasts to determine whether video delivery is improving. Elevated rebuffering is often localized to a specific Zone, subnet or device type. You can sort by rebuffering duration on the Zone, Device or Attendee table to troubleshoot. Offering an appropriate bitrate version of the stream for users with low bandwidth can help to resolve buffering issues.

<hr>

### Average Experienced Rebuffering Duration

**Average duration of experience rebuffering.**

**What to expect?**  
This metric provides a sense of how long users wait to begin streaming again after going into a rebuffer state. You can also see a bar chart showing the distribution of buffers of different durations.

**How can this information be used?**  
In Live Event scenarios, users understand that they will see the rebuffering spinner at times. Monitoring this metric can give you a sense of how long users have to wait before their stream begins playing again. Ideally any buffering will be under 10s long and buffering for over 30s at a time could indicate a problem. You can monitor this across events to see if video buffering improves.

<hr>

### Experienced Errors (per total attendee)

Ratio of the total number of Experienced Errors divided by the Total Attendees. You can also see a distribution that shows the number of attendees that have experienced one or more errors.

**What to expect?**  
This metric reflects how often users see an error message and could not play back a stream, which generally reflects a compatibility or configuration issue.

**How can this information be used?**  
This metric can help to pinpoint issues where users have a configuration issue such as not being able to reach the stream as configured by Zone logic, incompatibility with their device or browser or other configuration issues. The goal should be to keep this metric as low as possible, but .25 is a common number across the cloud platform. Numbers over .50 could indicate a problem. Often, these issues are contained to one Zone or even one user.

<hr>

### Peering Efficiency

Peering efficiency displays the Total Network Bytes divided by the Total Media Bytes across your event.

**What to expect?**  
The peering efficiency metric shows the percentage of bandwidth savings for all users viewing the live event via Vbrick Peer-to-Peer. Keep in mind that this metric improves as the number or users in a peer mesh increases.

**How can this information be used?**  
This is a headline metric that indicates how well peering is working across an entire event. A low peering efficiency could be an indication to look at the peering tab to see how many users are using peering and whether there might be an issue with connectivity between peers based on network or browser issues.