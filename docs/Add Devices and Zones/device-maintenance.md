---
title: Device Maintenance
excerpt: Tips on how to view, read, maintain, and obtain logs of your Rev devices
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## View Device Status

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1fc0077-statusColumn.png",
        "statusColumn.png",
        139
      ],
      "align": "center",
      "caption": "Every Device module features a Status column"
    }
  ]
}
[/block]

The **Status **of a device determines if it is available for use. After a device is created, Rev attempts to communicate with the new device using the specified **MAC Address** and **API Key** associated with the device.

For Rev to communicate with the device and receive a heartbeat, this must be true:

- A valid [API Key](doc:create-an-api-key) must be passed
- The **MAC Address** must be correct when you add the device

Device status states are:

- **Active**: The device is Active in Rev and sending heartbeats.
- **Inactive**: The device is Inactive in Rev.
- **Warning**: The device is Active but has not sent a heartbeat in 45 seconds (3 heartbeat intervals).
- **Offline**: The device is Active in Rev, but has not sent a heartbeat in 5 minutes.

> 📘 Note
> 
> If the status of a device remains **Uninitialized **after you have added it, Rev is not detecting your device. Double check the **MAC Address** and **Rev Server URL** of your device and make sure you have followed the device set up configuration steps correctly. 
> 
> **View**: [Getting Started - Devices](doc:getting-started-with-rev-devices)

## View and Request Device Logs

Device logs keep a record of events that occur for each device starting with the date the device is added to Rev. The device status is also updated based on Rev communication with the device. 

For example, if no heartbeat is detected and the device goes offline, this may be viewed in the device logs and the device is set to Offline status.

> 🚧 Important!
> 
> Device log entries are kept for a maximum of 60 days.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3069d90-viewLogDropdown.png",
        "viewLogDropdown.png",
        191
      ],
      "align": "center",
      "caption": "Each module has an Actions dropdown where various actions may be taken on the Device such as viewing its log"
    }
  ]
}
[/block]

Device log entries are accessed by clicking **View Log** under the **Actions **dropdown of the Device.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0f061c5-deviceLog.png",
        "deviceLog.png",
        1064
      ],
      "align": "center",
      "caption": "Click the Show Details button to view specific details about a log line entry"
    }
  ]
}
[/block]

| Log Entry | Description                                                                                                                                                                                                                                                              |
| :-------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Last Sync | This column indicates the last time the server was synced with your system. In the case of an LDAP server, this sync interval is specified when you add your LDAP device.                                                                                                |
| Status    | Indicates the success or failure of the activity that occurred.                                                                                                                                                                                                          |
| Activity  | Indicates the activity itself and what occurred; the most recent activity is listed first with the date the device is added listed at the bottom of the log. The device log shows the date and time the device goes offline and back online if this occurs, for example. |

You can also use the **Request Logs** menu item to send device logs to Vbrick Support. You must have DME **v3.24+** for this functionality.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2fe187a-requestLogsDropdown.png",
        "requestLogsDropdown.png",
        191
      ],
      "align": "center",
      "caption": "The Request Logs feature is often used to assist Vbrick Support"
    }
  ]
}
[/block]

This function gathers all the logs for one or more DME devices (under **Bulk Actions**) during support calls and troubleshooting to send to Vbrick Support. Once the logs are automatically collected and sent to Support, you are notified through email and the Rev [Notifications](doc:notifications) icon. Note this can be a labor-intensive process so you should not prompt this during events.

## Delete a Device

Delete a device from the a module by clicking the **Delete **link in the **Actions **column dropdown menu. Keep in mind that once you delete a device, you also delete the **Device Log** associated with it. You must add the device again if you intend to use it again and the log will \_not \_be restored.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1c4cd3-deleteDeviceDropdown.png",
        "deleteDeviceDropdown.png",
        192
      ],
      "align": "center",
      "caption": "Some actions are not reversible if you Delete a device.  You may also just set its status to Inactive."
    }
  ]
}
[/block]

When a device is deleted:

- Rev is disabled under that device's UI.  
  - For example, **System Configuration** > **Rev Interface** in the DME so that heartbeats are no longer sent to the DME if the deleted device is a DME. If the DME is Offline, the command is queued.
  - For example, **General **> **Vbrick Rev Interface** so that heartbeats are no longer sent to the Encoder if the deleted device is an Encoder. If the Encoder is Offline, the command is queued.

> 👍 Tip
> 
> A device may not be deleted if it is being used in a zone or presentation profile.

## Set a Device to Inactive

You may inactivate a device from the Devices module by editing the device and clicking the **Inactive **icon. Keep in mind that once a device is inactive it is no longer available for use and the media stored on this device is not accessible. You must activate the device again if you intend to use it and its stored content again on your video network.

When a device is **Inactive**:

- It is no longer visible in any **Presentation Profile** that has already been created.
  - Alternative: Keep the device **Active **but indicate it is **Inactive **and not to be used.
- Any **Presentation Profile** already using the device is not be usable, including any that are only using this device.

## Reboot a Device

You are able to reboot most hardware devices directly from Rev by using the **Reboot **option under the **Actions **dropdown menu of the Device. Anyone using the device is immediately booted and unable to access it until the reboot is completed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/64715c6-rebootDeviceDropdown.png",
        "rebootDeviceDropdown.png",
        189
      ],
      "align": "center",
      "caption": "Most Devices are able to be rebooted directly from Rev in the Actions dropdown"
    }
  ]
}
[/block]