---
title: Change Log (v7.48)
excerpt: ':calendar: Date Added: August 2022'
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

### Content Subscriptions
*Rev Only*

There are three new content subscription APIs that build on our last release and subscription endpoints.  They are:

* [Get Subscriptions](ref:subscriptions) - This API returns the channel and category subscriptions for the user making the API call.

* [Get Notifications](ref:getnotifications) - This API returns the subscription notifications of the user making the call.  The **unread** parameter can be set to true which then returns only the unread notifications.

* [Update Notifications](ref:notifications-1) - This API marks a specified notification Id as read.  If a specific notification is not provided, then all notifications for the user are marked read.

### Administration APIs

* The [Get Assignable Categories](ref:assignable-categories) API returns a list of categories that can be assigned in VOD settings. Category name, id, and its full path is returned.

* The [Get Expiration Rules](ref:expiration-rules) API returns an array of all expiration rules including the name and Id parameters such as rule name, type, and description among others.

### Authentication APIs

* A new [Extend Login Session for All Authentication Methods](ref:extendusersession) now extends the current user login session regardless of the authentication method used and includes preventing the user API key sessions and JWT authentication sessions from timing out.  
[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "[Extend API Key Session](ref:extendapikeysessiontimeout) and [Extend User Login Session](ref:extendsessiontimeout) have been deprecated as a result of this addition."
}
[/block]
## :wrench: **Updated/Fixed**

The [Get Video Transcription Files](ref:getvideotranscriptionfiles) and [Download Transcription File](ref:downloadvideotranscriptionfile) APIs have been updated to get a list of, and download, transcription file(s) via API when the user only has view rights.   **Note**: Previously to do this edit rights were required.

The [Get User By ID](ref:getuser), [Get User by Username](ref:getuserbyusername), and [Get User By Email](ref:getuserbyemailaddress)  APIs have been updated so that it can be easily seen what **Access Control Level** permissions the user has for video and webcast settings.  The responses returned for a user now specify **permissions** which are flags that include the following Booleans:

* canUpload
* canCreateEvents
* canCreatePublicWebcasts
* canCreateAllUsersWebcasts
* canCreatePublicVods
* canCreateAllUsersVods

Webcast APIs have been updated in preparation for the upcoming **Producer** functionality in Q4 2022.  Updates include the ability to add Producer as a **videoSourceType** and the corresponding **presenterIds**.  The following APIs are updated:

* [Create an Event](doc:create-event) 
* [Update Webcast](ref:editevent)
* [Patch Webcast](ref:patchwebcast)
* [Get Webcast Details](ref:getevent)
* [Get Webcasts By Time Range](ref:geteventslist)
[block:callout]
{
  "type": "warning",
  "title": "Important!",
  "body": "While the webcast updates are visible at this time, they are not functional until the Producer functionality is released in Q4 of 2022."
}
[/block]