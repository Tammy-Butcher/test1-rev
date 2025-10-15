---
title: Tag Users in a Video
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
To update **Video Settings** in Rev:

1. Navigate to a video and hover over the **Video Settings** button in the top right corner.

2. Click **Details ** from the options that appear.  Several tabs appear that allow you to create and modify the video's metadata. Select a tab depending on which setting you want to update. 

3. This feature is a **Basic Setting**.

The **In This Video** control is used to tag specific users in a video that are speakers. Once tagged, videos showing specific users can easily be found using Rev’s rich search and filtering capabilities. In This Video tagging can also be extended and [automated](doc:facial-recognition#automated-user-tagging) with the **Rev IQ module’s Facial Recognition** capabilities.

> 🚧 Important!
> 
> Tagged users _must_ have a profile picture uploaded and may _not_ have opted-out in their Profile Settings. Rev users _always_ have the option to opt-out of being tagged in a video even if they have a profile picture uploaded. View: [Your Rev Profile](doc:your-rev-profile)

To tag users in a video:

1. Enter each user you want to tag in the **Find Items** box and click **Done**.

2. Rev will search the Facial Recognition index and, if the user has a valid profile picture uploaded and has _not_ opted-out of tagging in their account settings, will add your tag to the **In this Video** box. 

3. Tag as many users in the video as desired before saving your video settings as normal.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4dc0e28-tagUsersInThisVideo.png",
        "tagUsersInThisVideo.png",
        463
      ],
      "align": "center",
      "caption": "Enter each user you want to tag in the video in the Find Items box of the In This Video control"
    }
  ]
}
[/block]


Each tagged video now has the following functionality:

- [Search and filter](doc:search-and-filter-functions) capabilities to find and filter videos with tagged users.
- [Bulk editing](doc:bulk-edit-video-settings#in-this-video) options to append, replace, and remove tagged users.
- Addition of tagged users to the [Video Basic Information](doc:rev-video-player-features#video-basic-information) and [Pulse](doc:rev-video-player-features#video-pulse) flyout panel(s) on Rev's video player. **Note**: Timeline tagging on these panels to indicate where on the timeline these users appear in the video requires that **Facial Recognition** is activated by your Account Admin.

## Automated User Tagging

**In This Video** tagging is automated with the **Rev IQ module’s Facial Recognition** capabilities. Note that this is a licensed ability that is enabled by your Account Admin first. Once Facial Recognition is activated, Rev tags all users in the video for you automatically with the click of a button.  Timeline tagging on the Rev video player flyout panels is included with Facial Recognition as well.

View the [Facial Recognition](doc:facial-recognition) guide for complete details on configuration and usage.