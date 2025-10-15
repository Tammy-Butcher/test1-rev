---
title: Update DME Software Version
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
Rev allows you to install DME software updates directly so that you do not have to go to the DME itself  to do so and may perform the update from within Rev instead.  You may also do this for one or several DMEs in **Bulk Action**.

The **Current DME Update Version** is always identified at the top of the **DME Management** module.

* If your Admin has not specified a version update this is also noted. Contact your Account Admin to enable this functionality and to provide an update path.
* Once the DME(s) are updated, the new version is verified in the **Version **column.
* Bulk updates are *not *permitted in mobile view.
* During the update process, DME(s) are *not * able to record. The status of the update is displayed in the **Status **column.

To update the software version of one or more DMEs:

1. Navigate to the DME Management module.

2. Note the software version that you will update to at the top of the module to make sure it is correct. If no version is displayed, contact your Account Admin to provide an update path.

3. Select checkboxes to the left of the DMEs you want to add to the schedule.

4. Click the **Bulk Action** > **Update** dropdown.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6bc6cc9-updateDmeSoftware.png",
        "updateDmeSoftware.png",
        1202,
        286,
        "#eff0f1"
      ],
      "caption": "Use Bulk Actions > Update to update the software version of one or more DMEs"
    }
  ]
}
[/block]
5. The progress percentage of each DME's update displays in the **Status **column until it completes.  Once complete, the new version updates in its **Version **column.
[block:callout]
{
  "type": "danger",
  "title": "Warning!",
  "body": "You may *not *use the DME as a recording device during an update.\n\nThere are several reasons why a DME may not automatically update including if:\n\n* The DME is within 3.5 hours of a scheduled event including Preproduction or Lobby time\n* The DME is actively recording as a recording DME\n* The DME has a sync in progress\n\nIn some cases it may take up to 15 minutes before the progress percentage of the DME software update is displayed in the **Status **column. \n\nBe sure to wait until the DME reflects that it is **Active **before administering or using a DME whose software is updated.\n\nFinally, be aware that you may not update or “revert” a DME software version to an older version."
}
[/block]