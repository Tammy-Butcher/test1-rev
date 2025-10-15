---
title: Stream Authorization Lockdown
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
Enabling [DME Stream Authorization Lockdown](doc:dme-and-vbrick-multicast-security#enable-dme-stream-authorization-lockdown) places all DMEs in a lockdown state where playback of Live or VOD HLS assets *requires *authorization. When enabling (or disabling) this feature, Rev directs each DME to change its **Stream Authorization** state.

There are several configuration items that are necessary for a DME to enter this state. Most are automatically handled by the DME when this setting is enabled in Rev.  This includes:

* All DME **Network Time Protocol (NTP)** synchronization fields are enabled and set so that all DMEs have a consistent time. NTP uses UDP port 123, so please plan accordingly. Customers that restrict traffic through **Proxy **should consult network support staff. DMEs that cannot sync time are not able to participate in content sharing.
* All DMEs are set to distribute content via **HTTPS** only.
* All DMES are checked to ensure that a valid security cert is in place.

If all three properties are met or set successfully, the DME returns a success message to Rev and is placed into a lockdown state.

DMEs that are *not *successfully placed into a lockdown state do not receive playback URLs from Rev. Rev automatically provides authorization encoded into the playback URLs for those DMEs that are in a lockdown state. DMEs receive the request, validate the security token, and subsequently authorize the stream.

Admins may put their entire systems into and out of this lockdown state as needed or required.

The **DME Management** and **DME Network Statistics** modules are used to check on the status of each DME once this setting is enabled. As noted, DMEs that cannot enter the lockdown state are not used for content delivery. This feature provides even higher level security than the existing user/video access level currently provided in Rev.

In addition to using the two modules above, DMEs that are used for streaming when this setting is enabled may also be edited and have their authorization viewed as seen below. If the DME is not authorized, an error will be seen instead.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/84b69d4-dmeUsedForStreaming.png",
        "dmeUsedForStreaming.png",
        807,
        361,
        "#ededee"
      ],
      "caption": "A DME authorized for streaming displays a notification"
    }
  ]
}
[/block]