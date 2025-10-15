---
title: Webcast Data Retention
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
Admins can decide if webcasts should be deleted automatically once concluded and how long the data should be retained afterwards.

To set a webcast data retention policy:

1. Navigate to **Admin > System Settings > Content Restriction**.

2. Select the **Delete Webcasts Automatically** checkbox under the **Webcast Data Retention Policy** section.

3. Specify a number between 3 and 2555 (days) to determine how many days the webcast(s) data is retained afterwards in the **Data Retention Period (Days)** field.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0468968-webcastDataRetention.png",
        "webcastDataRetention.png",
        843
      ],
      "align": "center",
      "caption": "Once a webcast is deleted, all personally identifiable information and all webcast data is removed"
    }
  ]
}
[/block]

When enabled:

- The policy is applied to all existing webcasts based on end date, regardless of whether they were ever run
- If a webcast is older than the policy, it is deleted
- As webcasts pass the data retention expiration period, data is deleted on a daily basis