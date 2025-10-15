---
title: Delete, Replace, or Deactivate Videos
excerpt: How to use the various options in Rev to make videos invisible to users
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

There are several methods of removing videos from Rev or making them invisible to viewers.  They include:

* deactivate
* unlist
* replace
* delete

Each method has its own consequences and should be carefully considered before using.

## Deactivate a Video

**Deactivating** a video is the least drastic of methods as it simply hides a video from other viewers without deleting it entirely. This preserves the video (and its associated metadata) for future use should it be needed again.  When you deactivate a video, you are simply setting it to [Inactive](doc:video-status) status.

The following attributes are set for a deactivated/inactive video:

* No longer included in active **Category** counts.
* Only available within **My Videos** for the user that uploaded or owns the video.
* Only viewable outside of **My Videos** by users with an Admin or Approver role.
* For users without the Admin or Approver role, **Inactive** videos are:
  * Hidden in Global Search.
  * Hidden in video lists of all videos for a user.
  * Hidden in all **Playlists**.
  * Hidden in all **Home Page** carousels

## Unlist a Video

[Unlisting](doc:unlist-a-video) a video is similar to deactivating it except it prevents it from being displayed to *all* viewers who do not have edit rights within the Rev UI including those with Approver role access.

This includes the following areas:

* All Videos / Browse Categories view(s)
* Dashboard carousels including the Featured Video carousel
* Channels
* Playlists
* Global Search

## Replace a Video

You may **Replace** an existing video with a new version if you have Edit Access or are a Media or Account Admin role. 

<Image alt="The Replace Video option is available if you have the correct permissions or role assigned to your account" align="center" src="https://files.readme.io/8a1fc52-replaceVideo.png">
  The Replace Video option is available if you have the correct permissions or role assigned to your account
</Image>

You are able to choose a new video file to upload from your hard drive when you select this option. The new video file must match the to-be-replaced or old video file.  This can be verified by downloading the old video.  If the old video is only downloadable as mp4, then the replacement video must be mp4.  If the old video can be downloaded as a zip file, then the new video must also be a zip file and have the same number of streams (either single or dual) as the old video.

The selected file will replace the current video file.

You may cancel and restore the original video until it has finished uploading by clicking the **Restore original video** button on the upload dialogue box. Once it has finished uploading, you may *not* use the restore function.

The following attributes are set for the replaced video:

* The video is transcoded based on existing transcoding presets for adding video.
* The video is distributed to DMEs marked as pre-positioned DMEs.
* A new thumbnail is generated from the *new* video file.
* The video is set to **Inactive**.
* If the replaced video is part of an Approval Process and is in Pending Approval or Rejected status, the new video will be reset to Approval Required and needs to be submitted for approval again once the upload is complete.
* If the video upload fails, you may upload a new video or use the old video file.
* Once the new video is uploaded and ready for playback, the old video is deleted from Rev storage and DMEs so that older content is not accessed (and to reduce storage space).

## Delete a Video

If you are a Media or Account Admin you have the option to **Delete** videos in Rev.  The option to delete a video is found at the bottom of the **Video Settings** dropdown.

> ❗️ Warning!
>
> This action can not be undone.  Proceed with caution.

When a video is deleted:

* It is removed from all **Playlists**.
* **Category** count is updated.
* All associated metadata, comments, ratings, etc. are removed.
* All video transcripts are deleted.  This includes any **Rev IQ** generated transcripts that are part of the video.
* If the video is **embedded**, any viewer trying to play the video receives an error in the future.

> 📘 Note
>
> Video analytics associated with the video are *not* removed. They are preserved for historical reporting purposes.
