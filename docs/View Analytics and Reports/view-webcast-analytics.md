---
title: View Webcast Analytics
excerpt: >-
  Rev provides comprehensive webcast analytics detailing attendee trends, usage
  metrics, and viewing quality of experience.  This guide describes what is
  available and how to use each to provide better webcasts for your audience.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
Once each webcast has concluded, Event and Account Admins may access a **Webcast Analytics Dashboard** from the [Webcast Settings Dashboard](doc:webcast-settings-dashboard) by clicking the **Reports **button.  Webcast Analytics provide insight to the types of attendees that viewed the event, their quality of experience, and their viewing tendencies and trends while the webcast was ongoing.
[block:callout]
{
  "type": "success",
  "title": "Tip",
  "body": "The **Reports **button contains *both ***Main Event** and **Pre-Production** report access. If the Main Event has not yet started, only Pre-Production events are available. If no Pre-Production dry runs are conducted, only the Main Event report is displayed.\n\nIf no Webcasts have occurred yet, the drop-down displays, “No reports are currently available” until one has concluded."
}
[/block]
There are three tabs on the Webcast Analytics Dashboard.  Each is described below.

## Engagement Analytics

Provides general attendee and viewing trend information for the webcast.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/069bb94-engagementAnalytics.png",
        "engagementAnalytics.png",
        1202,
        215,
        "#f0f0f0"
      ],
      "caption": "The top KPIs under the Engagement Analytics tab displays Attendee viewing trends"
    }
  ]
}
[/block]
* **Attendees **(internal versus public). Includes the Estimated number of Webcast attendees entered during the event setup if this field was utilized.
* **Total Viewing Time** (internal versus public)
* **Average Viewing Time**
* **Attendee Trends** (sessions by time/duration). View how many attendees/sessions are connected to the event at any given time. This allows you to see when people connect/drop-off.
* **Top 15 Zones** used to connect to the event
* **Web Browsers** used
* **Device Types** used

## Quality of Experience

Displays metrics related to how well the attendee stayed "connected" to the webcast and zone/stream usage analysis.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c57fbcd-qualityOfExperience.png",
        "qualityOfExperience.png",
        1800,
        274,
        "#000000"
      ],
      "caption": "The top KPIs under the Quality of Experience tab display details related to the viewing experience"
    }
  ]
}
[/block]
* **Average Zone Bit Rate Kbps** (for all zones)
* **Experienced Rebuffering** (%)
* **Average Rebuffering Duration** (in seconds)
* **Experienced Errors** (per total attendees)
* **Peering Efficiency** (bandwidth saved for all users in peer mesh)
* **Average Zone Bit Rate** (for all zones, kbps)
* **Average Zone Bandwidth** (for all zones, mbps)
* **Rebuffering Duration** (%)
   * Bars represent the total number of rebuffering events by zone
   * Dot on each bar represents rebuffering duration
* **Video Player** (type used and numbers by zone)
* **Video Stream** (type and number of streams by zone)
* **Experienced Errors** (per total attendees)

## Users

Allows you to filter and view **User **data before you download the [Webcast Attendees](doc:webcast-reports#download-attendee-metrics) report by using the **Columns **control to pick and choose which metrics you want to view.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6b42a46-users.png",
        "users.png",
        1202,
        453,
        "#dddddd"
      ],
      "caption": "Filter and view user data by using the Columns control"
    }
  ]
}
[/block]
The specific filters available in the Columns control:
* **Metrics**
   * Experienced Errors
   * Experienced Rebuffering Count
   * Experienced Rebuffering Duration
   * Multicast Errors
* **Session**
   * Exit Time
   * Last Device
   * Last Playback URL
   * Removed
   * Session Start Time
   * Session Time
   * Viewing Start Time
   * Viewing Time (HH:MM:SS)
* **System**
   * Browser
   * Device Type
   * IP Address
   * Platform
   * Platform Version
   * Zone
* **User**
   * Attendee Type
   * Email
   * Full Name
   * User Name
   * User Type