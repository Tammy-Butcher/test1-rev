---
title: DME and Vbrick Multicast Security
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
The **Content Restriction** section provides multiple settings for Vbrick Multicast.  As a reminder, in order to utilize Vbrick Multicast, each viewer must have the agent installed on their PC/Mac.  Please view the [Vbrick Multicast Installation](https://portal.vbrick.com//doc/PDFs/REV/Vbrick%20Multicast%20Install%20Quick%20Reference.pdf) documentation for details.

## Enable Vbrick Multicast Encryption

The **Enable Vbrick Multicast Encryption** feature, when enabled, will force all Vbrick Multicast data payloads to be encrypted. While not required, this setting is highly recommended. There are two specific requirements to use this feature:

1. ALL DMEs must be **DME v3.26** or higher. This requirement ensures that the DMEs do not generate multicast without compliance with this feature.  AND

2. Users must have **Vbrick Multicast Agent (VBM) v2.1** or higher.  Previous versions of VBM will not interoperate with encryption and/or FEC.

Note that after enabling this setting – IF a DME v3.25 (or previous) is detected within the portal, the feature will be disabled.

> 🚧 Important!
> 
> Note below that Rev does _not_ let you enable this feature if any DMEs earlier than v3.26 are detected.



[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6b8c1e0-vbmNotEnabled.png",
        "vbmNotEnabled.png",
        1110
      ],
      "align": "center",
      "caption": "To enable VBM encryption, you must make sure all your DMEs are upgraded to v3.26+"
    }
  ]
}
[/block]

Once all DMEs are of the required version, Rev allows enabling this feature.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e1435e-encryptionEnabled.png",
        "encryptionEnabled.png",
        1207
      ],
      "align": "center",
      "caption": "If all DMEs are v3.26+, you are able to enable VBM encryption and FEC features"
    }
  ]
}
[/block]

> ❗️ Caution!
> 
> Vbrick _strongly_ recommends that you encrypt your Multicast!  This encryption is on by default and should _only_ be disabled for debugging purposes.

## Enable Vbrick Multicast FEC

Distribution of multicast streams utilizes User Datagram Protocol (UDP) as opposed to TCP.  UDP is a best-attempt protocol, and therefore it is susceptible to packet loss. Also, UDP does not guarantee delivery orders – but our agent is tooled to assure in-order delivery.

FEC, or forward error correction, is a method of sending additional overhead within the multicast stream that can be used to fill in or recover lost packets. In other words, with FEC, streams can withstand packet loss and the stream can be fixed. The playback will not be affected.

It should be noted and cautioned, that the distribution pattern of the packet loss may lead to unrecoverable loss.  This means that if there are large gaps of loss, and these gaps exceed the overhead that is included to fix the loss, then we cannot fix the loss.  When these types of losses occur, the player may be affected, but it will continue without user intervention.

In order to accommodate the variety of networks and losses that our customers may have, Vbrick provides 4 levels of FEC encoding.  Choosing one of these levels sets the account FEC level.  The levels are:

- No Error Correction / FEC Disabled.  
- Minimal Error Correction (For networks with low packet loss).
- Moderate Error Correction (Recommended)
- Maximum Error Correction (For very lossy networks)

Each level provides increasing error correction – up to 25% at the **Maximum** level.  However, that number may be misleading, because you could have packet loss of the overhead which reduces your ability to fix.  Each level also increases the stream size accordingly.  The best approach is always to test your network and each of the individual settings.

The basic concept is that you have an account-level FEC setting.  This controls all FEC across the system unless you want to customize FEC at the DME level.

Meaning, each [DME also has a FEC level](doc:add-a-dme#configure-dme-specific-multicast-settings).  Initially, each DME FEC level will be set to the account FEC level (which will be notated as **System Default** in the DME management page).  However, each DME can then override that setting to accommodate its particular networking needs (which will be notated as **Custom** on the DME management page).  This process is referred to as Customized DMEs [for FEC].  For instance, you may have a DME in a very lossy wireless network and want it to be configured for max FEC.  The override setting, or DME FEC level, is discussed on the [DME management page](doc:manage-dme-devices).

Initially setting or [at a later time] changing the account FEC level will have effects depending on the **Scope of Changes** toggle.  This toggle can be **ALL DMEs** or **Non-Customized DMEs**.

- If the **ALL DMEs** toggle is selected, then ALL DMEs will be changed to the new account FEC level setting.  This includes any DME that has been customized – they will be reverted to the system default account FEC level.

- If the **Non-Customized DMEs** toggle is selected, then only the DMEs that are using the account level FEC setting (meaning they have not been customized) will be changed.  This feature is useful if you have customized several DMEs (and you don’t want them to change) but you change the account FEC level.  Only DMEs that are currently using the system default (account FEC level) will change to the new setting.

> 📘 Note
> 
> You must have Vbrick Multicast Encryption enabled in order to utilize FEC.  The system will not allow you to enable FEC until Vbrick Multicast Encryption is enabled.  Also, if you have enabled FEC, but then disable Vbrick Multicast Encryption, you will disable FEC and lose all DME FEC settings.
> 
> Also remember that all users must be using Vbrick Multicast Agent 2.1 (or higher).

## Override Default Local Stream URL

The Vbrick Multicast agent requires a security certificate for secure communication with the browser.  Vbrick provides a certificate in our VBM distribution, but in some situations, customers may wish to provide their own URL and certificate.

Regardless of using Vbrick's certificate or a customer-provided certificate, it is useful to remember that these certificates have a limited expiry date.  Please review your certificate expiry dates regularly. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/393c5c4-vbmLocalStream.png",
        "vbmLocalStream.png",
        1178
      ],
      "align": "center",
      "caption": "Use the Local Stream Host field to override the default URL Local Stream URL in the VBM app"
    }
  ]
}
[/block]

**To override default Local Stream URL:**

1. Decide on a **Local Stream Host** FQDN that will resolve to 127.0.0.1 (localhost).  Use this to provision a security certificate.  Note:  You will need to distribute this certificate to all clients in the field.  Please review the installation guide below.

2. Navigate to **System Settings** > **Content Restriction**. Scroll to the **Vbrick Multicast** section.

3. Select the **Enabled **checkbox in the **Override default Local Stream URL** section. 

4. Provide a **Local Stream Host** URL, which will need to resolve to 127.0.0.1 (ref: your local DNS)

> ❗️ Caution
> 
> This setting should not be modified without contacting Vbrick Support.  Please view the [Vbrick Multicast Installation](https://portal.vbrick.com//doc/PDFs/REV/Vbrick%20Multicast%20Install%20Quick%20Reference.pdf) documentation for details.

## DME Stream Authorization Lockdown

When enabled, the **DME Stream Authorization Lockdown** places all DMEs in a lockdown state where playback of Live or VOD HLS assets requires Rev authorization. Rev automatically provides authorization encoded into the playback URLs. Admins may put their entire systems into and out of this lockdown state as needed or required.

### Pre-Configuration Requirements

_Before_ you enable this setting, complete the following steps:

1. Make sure all DMEs are updated to **v3.21.x** or later. DMEs that are on previous versions may corrupt the ability of the **Stream Authorization** feature.

2. For distribution, make sure all DMEs are _Pushing_ streams from DME to DME when Stream Authorization is enabled.

   - As part of the DME Stream Authorization feature, DMEs will no longer serve RTMP, RTSP, or TS. Any DME that is actively \_Pulling \_an RTMP / RTSP / or TS from another DME will fail. DMEs may still continue to \_Push \_RTMP / RTSP / TS to other DMEs.
   - For example, DME-1 is pulling RTMP-Stream2 from DME-2. When Stream Authorization is enabled, that pull will fail. DME-2 will need to be reconfigured to \_Push \_RTMP-Stream2 to DME-1 in order to get the stream on DME-1.

3. Configure your [Recording DMEs](doc:set-dme-recording-options) for Stream Authorization.

   - Rev currently supports two Recording DMEs. Streams that need to be recorded must be native on the Recording DME (they cannot be _Pulled_). Make sure all streams that need to be recorded are _Pushed _(from origin) to the Recording DMEs. The recording will fail if the stream is not provisioned to the recording DME.

4. If you are utilizing a DME for the **Rev **> **User Security** > **User Location** feature, confirm that the DME URL is using HTTPS.

5. Once you have completed all the preceding steps, you are ready to enable DME Stream Authorization.

### Configuration

To enable DME Stream Authorization Lockdown:

1. Navigate to **System Settings** > **Content Restriction**. Scroll to the **Vbrick Multicast** section.

2. Select the **Enabled **checkbox in the **DME Stream Authorization Lockdown** section. Note: If this section is not visible, contact Vbrick Customer Support to review availability.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f0a0022-enableDmeLockdown.png",
        "enableDmeLockdown.png",
        773
      ],
      "align": "center",
      "caption": "Select the Enabled checkbox next to DME Stream Authorization Lockdown only after completing the pre-flight checklist first"
    }
  ]
}
[/block]

3. When enabling (or disabling) this feature, Rev directs each DME to change its **Stream Authorization** state. There are several configuration items that are necessary for a DME to enter this state including enabling **NTP **services, forcing **HTTPS content sharing**, and validating the DME’s **Security Cert**. If these are not set correctly, the DME will not be used to distribute content which means that Rev will not point users to that DME for content playback.  **View**: [DME Stream Authorization Lockdown Management](doc:stream-authorization-lockdown)

4. It may take several moments for the DMEs to report back a successful lockdown status. The status state can always be reviewed on the **DME Management** and **DME Network Statistics** page(s). 

5. Test fully. Test DME configured distribution and make sure your streams are propagating through the system correctly with Pushes. Test that your Recordings are happening for all necessary streams.

Keep in mind:

- Only authorized viewers will be able to see a particular video asset once enabled
- Streams will be authorized on a per-user, public, or all users level
- Stream Authorization does not support "Appending" HLS streams.  All HLS streams, configured at the DME level, should be "Rolling".
- Individual levels will receive individual tokens to thwart sharing
- This setting is disabled by default

> 📘 Note
> 
> There is additional complexity and computation necessary for implementing stream authorization.   Please test your stream configurations before your events, especially for high-use live events.