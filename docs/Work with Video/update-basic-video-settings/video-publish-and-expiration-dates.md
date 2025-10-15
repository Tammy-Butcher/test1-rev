---
title: Video Publish and Expiration Dates
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

## Set a Publish Date

When a video is set to **Active **status, the Publish Date is automatically set to the **Current Date**. No Expiration Date or Rule is set. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dae9444-publishDate.png",
        "publishDate.png",
        352
      ],
      "align": "center",
      "caption": "Videos with an Active status have the Publish Date set to the Current Date automatically"
    }
  ]
}
[/block]


To publish the video in the future, you must make the status **Inactive**. Videos that have a future Publish Date become Active at 12:00 a.m on the date selected. The owner of the video is notified via email that the video is Active when it is published.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4b1370-futurePublishDate.png",
        "futurePublishDate.png",
        352
      ],
      "align": "center",
      "caption": "A future Publish Date can only be set on videos with an Inactive status"
    }
  ]
}
[/block]


## Set an Expiration Date or Rule

Expiration Dates may be set by date or by a rule that your Admin creates such expiration occurring when videos have not been viewed after 30 days.

If an **Expiration Date** is set, the video is set to **Inactive **status at 12:00 a.m. on that date. At that point, it is _not_ accessible or visible to other user accounts with the exception of Account Admins. 

If the **Delete When Expires** checkbox is checked, the video is _deleted_ when it expires instead of set to **Inactive **status.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d426f8d-expireDateDelete.png",
        "expireDateDelete.png",
        352
      ],
      "align": "center",
      "caption": "The video will be deleted on the Expiration Date that has been set"
    }
  ]
}
[/block]


If an **Expiration Rule** is set, the video is set to **Inactive **status at 12:00 a.m. on that date or it is deleted on that date depending upon the parameters the Admin sets. At that point, it is _not _ accessible or visible to other user accounts with the exception of Account Admins (if set to Inactive).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e2db622-expireRuleInactive.png",
        "expireRuleInactive.png",
        352
      ],
      "align": "center",
      "caption": "The video will be set to Inactive status when it does not receive any views after a specific amount of days"
    }
  ]
}
[/block]


- You are only able to set an expiration date or rule for videos that are set to **Active **status.
- Videos that have expiration dates set may be viewed on the [Expirations](doc:user-menu-options#the-media-menu) menu by Admins and Media Contributors.
- The video is not deleted from the system when expired, only set to **Inactive **status unless the **Delete When Video Expires **checkbox is selected or it is set to delete in the expiry rule by the Admin.
- If the video is set to expire by an expiry rule and that rule is deleted, it no longer expires.
- If a video expires while a user is viewing it, the user may complete watching the video. When a new session is started, however, the video will then be expired.
- The owner is emailed 7 days prior to video expiration and again upon the actual date of expiration.
- If you set a video to **Active **status and do not set an Expiration Date or Rule, the **Publish Date** is automatically set for the Current Date it is made **Active**.