---
title: Change Log (v7.43)
excerpt: ':calendar: Date Added: October 2021'
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

### Register Attendees for an Upcoming Public Webcast

Rev v7.43 adds the ability for an Account, Event, or Media Admin (as well as Event Hosts for a Webcast) to enable [pre-registration](doc:public-events#allow-early-registration-for-public-events) for an upcoming **Public Webcast**.  Also included with this feature is the ability to manage those registrations via API. 

> 🚧 Important!
>
> Make sure you first enable Public webcast pre-registration through existing webcast APIs that are also now [updated](ref:change-log-v743#wrench-updatedfixed) in support of the feature in v7.43.

Once you enable pre-registration on a new or existing Public webcast, you can manage your registrations with the following new registration endpoints:

* [Add Guest Registration](ref:createguestwebcastuser)
* [Update Guest Registration](ref:editguestuser-1)
* [Patch Guest Registration](ref:patchguestuser)
* [Delete Guest Registration](ref:deleteguestuser)
* [Get Guest Registration](ref:getguestuser)
* [Get All Registrations for a Webcast](ref:getguestusers)

### Add Video Comments

An [Add Video Comments](ref:addcomments) endpoint is now available. This is a new **POST** action endpoint that performs exactly as the existing **PUT** action except you can now specify a **commentId**.  

* This means that a user is able to add a root level video comment (no commentId specified) or reply to an existing (parent) comment if a commentId is specified.

* When a **commentId** is passed, the new comment is created as a **child** comment of the passed commentId. Note that the **parent** comment *must* exist or an unauthorized error is returned.

* Managing [video comments](doc:rev-video-player-features#video-comments), and the permissions required to do so, is now consistent with the UI.

> ❗️ Caution
>
> The existing [Update Video Comment](ref:submitcomments) will be deprecated in a future release.  Please plan accordingly and use **Add Video Comments** (POST) going forward.

### Delete Video Comments

A [Delete Video Comments](ref:deletevideocomments) endpoint is now available.  This endpoint deletes *all* comments (if no **commentIds** are specified) associated with a given **videoId**.  Otherwise, it will delete only the **commentIds** specified.

## :wrench: **Updated/Fixed**

### Public Webcast Registration Updates

To use the new [Public Events Pre-Registration](doc:public-events#allow-early-registration-for-public-events) feature released in Rev v7.43, it must first be enabled. The following endpoints have ben updated to include the **allowPreRegistration** and **emailToPreRegistrants** attributes to support this new feature:

* [Create Webcast](ref:createevent) 
* [Update Webcast](ref:editevent) 
* [Get Webcast Details](ref:getevent) 
* [Patch Webcast](ref:patchwebcast) 

Once pre-registration is enabled, use the new registration management endpoints to view and manage registrations programmatically via our API.

### Video Owner Updates

The new [Video Owner](doc:update-basic-video-settings#video-owner) field updates in Rev v7.43 are now updated in applicable video endpoints.  These include:

* [Upload Video](doc:upload-video)
* [Update Video Details/Metadata](ref:editvideo) 
* [Patch Video Details/Metadata](ref:editvideopatch) 
* [Get Video Details/Metadata](ref:getvideosdetails) 
* [Migrate Video](ref:migratevideo) 

[Video Search](ref:searchvideo) also now accounts for the **owners** and **ownerIds** attributes.

### Webcast Q\&A Report Updates

A new  **whenReplied** attribute is now returned in the [Get Webcast Q\&A Report](ref:geteventquestions) endpoint so that you know exactly when a user question was responded to.  This attribute returns the date and time that a question was replied to.  If the question was not replied to, and for all instances prior to this update, it returns null.

## :tada: **We've Got Style!**

You may have noticed some changes around here!  We've got some new style.  Check out all the new changes and features on our [API style update](changelog:api-reference-and-design-updates-october-2021).
