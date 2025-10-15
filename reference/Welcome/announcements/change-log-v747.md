---
title: Change Log (v7.47)
excerpt: ':calendar: Date Added: June 2022'
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

Rev APIs now support the ability to [Subscribe to a Channel or Category](ref:subscribe) . The **id** and **type** (channel/category) is required when subscribing.  

Once subscribed, use the [Unsubscribe to a Channel or Category](ref:unsubscribe) endpoint to unsubscribe to a specific channel or category.

### Get Categories for a User
*Rev Only*

The new [Get Categories for User](ref:getcategoriesforuser) API displays the number of videos in a category based on the video permissions inside the category or subcategory.  

This is similar to the [Get Categories](ref:getcategories) with a few differences:

* A **count** of the videos for each category is included based on the user's **accessControl**
* Only one level of the hierarchy at any time is displayed
* A **restricted** Boolean flag is included indicating if the category is restricted/secure

If no **parentCategoryId** is included, only the root level categories are returned along with uncategorized.  Unauthenticated users are only returned if **Public** viewing is enabled.

### Get User Location Service

This new [Get User Location Service](ref:user-location) endpoint checks if the **ULS** (user location service) is enabled.  

Also included are the **primary** and **secondary** URLs (if enabled).  If not enabled, no URLs are returned.

### Get User Profile Image

A new property, **profileImageUri**, has been added to the **Owner** section of the [Search Videos](ref:searchvideo) API that may be downloaded with the new [Get User Profile Image](ref:getuserprofileimage) endpoint.  

The **key** needed is the image **id** returned in the Owner section.

## :wrench: **Updated/Fixed**

### Anonymous Webcasts

The following APIs have been updated to allow for support of a new parameter, **attendeeJoinMethod**, when the **accessControl** is equal to **Public**.  The attendeeJoinMethod can be either **registration** or **anonymous**.  If it is not specified, it defaults to registration.  

  * [Create Webcast](ref:createevent) 
  * [Update Webcast](ref:editevent) 
  * [Patch Webcast](ref:patchwebcast) 
  * [Get Webcast Details](ref:getevent) 
  * [Get Webcasts By Time Range](ref:geteventslist) 
  * [Search Webcasts By Custom Field or Date Range](ref:searchwebcasts) 

When **anonymous** is specified, no user details are collected. View: [Anonymous Attendees for Public Events](doc:public-events#anonymous-attendees-for-public-events) topic for more details.

### Pexip Updates

The following endpoints have been updated to include Pexip as a videoSourceType:

  * [Create Webcast](ref:createevent) 
  * [Update Webcast](ref:editevent) 
  * [Patch Webcast](ref:patchwebcast) 
  * [Get Webcast Details](ref:getevent) 
  * [Get Webcasts By Time Range](ref:geteventslist) 

View: [Pexip](doc:pexip) integrations topic for details on usage.

### Get Channels for User

The [Get Channels For User](ref:getuserchannels) API has been updated to display only the channels and number of videos in a channel based on the user's access control for that page.  For example, a Media Viewer role with no **edit access** will *only* see the count of **Active** videos.

### Search Videos

The [Search Videos](ref:searchvideo) endpoint now has an optional **filter** parameter that allows you to filter search results based on two values:

* mySubscriptions - returns all categories and/or channels the user is subscribed to
* myRecommendations - applies recommendation logic which boosts search results based on recent viewing history using up to the last 10 videos viewed by a user

### API Permission Updates

#### canEdit Permission Updates

The **canEdit** permission is now returned in the following endpoints:

  * [Get Video Details/Metadata](ref:getvideosdetails)
  * [Search Videos](ref:searchvideo) 
  * [Get Channels For User](ref:getuserchannels) 

This is a Boolean value that, when true, means that a user can edit an object.  Note that an admin user always returns a value of true but this does not mean that every one can edit.

#### canUpload and canCreateEvents Permission Updates

The **canUpload** and **canCreateEvents** permission(s) are now returned in the [Get User By ID](ref:getuser) endpoint.  These are Boolean values to determine whether or not a user can upload videos or create events.  Note that these values do no account for the Media Viewer role with channel upload permissions.