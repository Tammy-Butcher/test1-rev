---
title: Change Log (v7.51)
excerpt: ':calendar: Date Added: February 2023'
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

### Producer Webcast API Enhancements

*Rev Only*

As part of Producer's new [Background feature](changelog:release-notes-v751-februarymarch-2023) and the ability to upload custom backgrounds and streaming layouts, there are also two new APIs for uploading and deleting **Producer** backgrounds:

* [Upload Producer Background Image](ref:uploadproducerwebcastbackgroundfile) - Uploads a custom image file for use as a background in a Producer webcast layout. Accepted image files are png, jpeg, and jpg.  Gif and animated gifs are not accepted at this time.

* [Delete Producer Background Image](ref:deleteproducerbackgroundimage) - Deletes a specified background image for a Producer webcast layout. If images are not specified, then all custom layout background images for that webcast are deleted.

* [Get Webcast Details](ref:getevent) - This API is updated to now return the **producerBgImages** object when a custom background is used to display applicable Producer webcast backgrounds and metadata.

## :wrench: **Updated/Fixed**

### Hiding Detailed Analytics

In the v7.51 release, Account Admins are able to hide all detailed **individual user-level analytics** by disabling them at the account level under the new [User Level Analytics](doc:hide-user-level-analytics) section under the **Content Restriction** menu. If this toggle is enabled for an account, the following endpoints now return a 401 error as a result:

* [Get Video Report](ref:getvideoreport) 
* [Get Video Watch Report](ref:uservideocompletion) 
* [Get Webcast Attendees Report](ref:getposteventsessions) 
  * **Note**: Totals are returned but the session array is not. Includes deprecated version.
* [Get Users By Login Date](ref:loginreport) 
* [Get Webcast Attendees in Realtime](ref:getrealtimeattendeessearchrequest) 
  * **Note**: Totals are returned but the attendees array is not.

> 🚧 Important!
>
> Audit service detailed analytics must be disabled manually.

### Video Upload and Migration Updates

You are now able to upload and migrate a video from outside of Rev and retain the video's total view count.  A new parameter, **legacyViewCount**, can be used to track and retain the *original* view count of outside videos when porting them to Rev.

Use **legacyViewCount** with the following endpoints to retain its total view count:

* [Upload Video](ref:uploadvideo-1) 
* [Migrate Video](ref:migratevideo) 

As users in Rev begin to view the video, the legacyViewCount parameter is then used to increment:

* **viewCount** in [Search Videos](ref:searchvideo) 
* **totalViews** in [Get Video Details/Metadata](ref:getvideosdetails)

> 📘 Note
>
> These views are not reflected in video analytics.

### Get (Deleted) Video Comments

A new parameter now allows admin accounts to view unredacted deleted comments on the [Get Video Comments](ref:getvideocomments) endpoint.  The **showAll** parameter is set to false by default.

When toggled to true, if the account is an *admin* account (Account Admin or Media Admin):

* Return unredacted comment values with text, userName, firstName, lastName, and date.
* There are three new response values as part of the addition:
  * **isRemoved** - true/false to signify a deleted comment
  * **deletedBy** - user name that deleted the comment
  * **deletedWhen** - date and time the comment was deleted

If **showAll** is false, the endpoint performs exactly as it does today with only *redacted* values appearing.

### Get Webcast Comments Log Update

A new **htmlComment** parameter is now returned in the [Get Webcast Comments Log](ref:geteventcomments) endpoint to capture the rich text comments that may be included in webcast chats.  Please note:

* If no HTML is used in the comment, the text is passed in text only exactly as it is today.
* If there is rich text used in the comment, both the regular text as well as the HTML tags are used.

### API Structure and Documentation Updates

To provide more structure and consistency in the data that is returned in our APIs, the [Get Webcast Q\&A Report](ref:geteventquestions) API has been updated to include the following objects in the main response body:

* **userName** - This is the username of the user submitting the question.
* **repliedUserName** - This is the username of the user who replies to the question, if applicable.

This change makes the endpoint more consistent with other API object conventions.  So that this is a non-breaking change, the existing **askedBy** and **repliedBy** objects will remain in place.

The [Get Zone Devices](ref:getzonedevices) endpoint description has been updated to reflect that it returns all of the devices that *can be assigned to any zone* rather than all of the devices *in a zone*.  This was confusing and has been clarified.
