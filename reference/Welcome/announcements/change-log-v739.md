---
title: Change Log (v7.39)
excerpt: ':calendar: Date Added: February 2021'
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## :star2: **New**

* [Get System Health](ref:system-health) checks the status of Rev health as shown on the **Rev System Health** page. The response should be a 200 OK unless there is a problem which is then displayed as a 503 error.

* [Get Maintenance Schedule](ref:maintenance-schedule) returns **Rev’s scheduled maintenance windows** (by date/time) for the current year.

* [Get Rev IQ Credits Usage](ref:getaccountiqcreditsusage) tracks how **Rev IQ credits** are used.

* [Search Webcasts By Custom Field/Date Range](https://revdocs.vbrick.com/reference#searchwebcasts) endpoint has been added to allow you to query by **custom field** (id or name) and **custom field value** and/or **date range** to return a list of webcasts within those filtered parameters.

* [Delete Webcasts By Custom Field or Date Range](https://revdocs.vbrick.com/reference#deleteevents) deletes all events for a given date range or custom field. Use the [Get Delete Webcasts Job Status](https://revdocs.vbrick.com/reference#getdeletewebcastsjobstatus) endpoint to check on the status of any bulk delete.

* [Upload Video Presentation Chapters](https://revdocs.vbrick.com/reference#uploadpresentationfile) is a new endpoint to create **video chapters with presentation file uploads** (similar to creating chapters in a video with a presentation in the Rev video edit interface). You can also use the [Get method](https://revdocs.vbrick.com/reference#getvideopresentationstatus) to retrieve the **status **of the presentation file upload.

## :wrench: **Updated/Fixed**

[Create Webcast](ref:createevent) and [Update Webcast](ref:editevent) endpoints are updated with the following:

* In support of the new event setting [Show Event Sharing Link](https://revdocs.vbrick.com/docs/event-basic-settings#show-event-sharing-link). A new parameter is now available that, when true, hides the **webcast URL** on the **Webcast Landing** page (both Admin and Attendee view) and on the **Event Details** page displayed to attendees while it is broadcasting. This option is **false **by default and the URL is displayed.

* A new **eventAdmins** array of users has been added who will be **Webex Hosts and Co-hosts** (called **event admins** in the Rev UI).

* A new **moderators **array that is equivalent to **panelists **in Webex.