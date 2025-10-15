---
title: Add a Presentation Profile
excerpt: >-
  This guide explains what Presentation Profiles are, how they are used with
  your Webcasts, and best practices for using them with your portal events
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
**Presentation Profiles** are used to define **Device** profiles for Webcasts.  Account Admins create them to specify video source **inputs** and destination **outputs** to easily control devices for a Webcast Event.

This means that Event Admins and Hosts have a simple and intuitive system already in place when they design and deliver their Webcast Events in the Rev portal.

> 📘 Note
>
> **Account Admins** are able to both *create* new Presentation Profiles and *assign* them to Webcast Events.
>
> **Event Admins** and **Event Hosts** are able to assign or update Webcast Events (including the Presentation Profile assigned to it) but *only* if they are also assigned to the event.

To add a Presentation Profile:

1. Navigate to **Devices** > **Presentation Profiles** > **Add a Presentation Profile**.

2. Complete each section of the **Presentation Profile** form and click **Create**.

## Name the Presentation Profile

Begin by creating a unique Name and Description for the Presentation Profile.

* **Name** - Enter a profile Name. This is a required field and must be unique.
* **Description** - Enter a Description that details what the profile will be used for.
* **Status** - The Status of the profile. When Inactive, it will not be visible for use in events.

## Specify Presentation Profile Video Source

A streaming **Video Source** *must* be specified for each Presentation Profile. The available sources are populated in the dropdown by the [source devices](doc:add-a-source-or-custom-device) you have added.

<Image title="presentationProfileVideoSource.png" alt={902} align="center" src="https://files.readme.io/f0b18ed-presentationProfileVideoSource.png">
  Add available Video Sources from the Devices you have added
</Image>

> 👍 Tip
>
> If an **Encoder** is selected in the **Video Source** dropdown, the following conditions must be true:
>
> * The Encoder must be configured in Rev in [Source Devices and LDAP Connectors](doc:add-a-source-or-custom-device#add-an-encoder) object
> * All slots and channels associated with the Encoder have been configured correctly
> * The available slots and channels are displayed in the following format: `<device name>:\<slot #>:\<channel #>`.

## Set a Presentation Profile Viewing Destination

At least one viewing destination must be defined for each profile. Multiple viewing destinations may also be defined if needed or desired.

Any of the following devices may be defined as a viewing destination:

* An Encoder *if that Encoder has also been set as the source in the Video Source section*
* A DME that has been previously added as a Device
* A Custom destination

To add a viewing destination:

1. Click the **Select a Destination** dropdown in the **Destination** section of the **Presentation Profile**.

2. Select a **Device** that has been previously added. All viewing destination streams that are available for that device appear in the **Available Streams** box.

<Image title="availablePresentationProfileStreams.png" alt={902} align="center" src="https://files.readme.io/f7d4ab1-availablePresentationProfileStreams.png">
  Viewing Streams are set for a Device when it is added and appear here to add as Viewing Destinations for a Presentation Profile
</Image>

3. Click the viewing streams you want to add to move them to the **Selected Streams** box. These streams become available in the Presentation Profile as viewing destinations during an event.

> ❗️ Warning!
>
> Presentation Profiles may contain multiple Destinations DME Streams. Vbrick Peer-to-Peer Meshes may use any HLS in the Destination/DMEs for content retrieval. To correctly leverage the Mesh and multiple Destinations, it is important that each Destination has the *same* named and sourced Live Webcast HLS stream for use with Vbrick Peer-to-Peer.

> 📘 Note
>
> An RTSP unicast stream is *required* for recording Live Webcasts in Rev. Make sure that your stream has a keyframe interval between 2 to 5 seconds and do not use B-frames.

> 📘 Note
>
> As a streamline feature, if you include a CDN version stream (from a DME Create URL) into the Presentation Profile, it will automatically be added to the Default Zone.
>
> For example, if you create a stream on a DME called **MyCustomStream**, EVP customers will have the ability to push that stream to CDN (Cloudfront in our cast). Doing this will create a **MyCustomStream-CDN** stream within that DME. If you add **MyCustomStream-CDN** to the Presentation Profile **Destinations**, it will automatically be added to the Default Zone **Devices** (although, it will not be displayed.)

## Rev IQ Enabled Presentation Profiles

To enable [live event subtitles](doc:video-sources#live-event-subtitles), you must use a "Rev IQ-enabled" Presentation Profile for the event. This is accomplished by selecting the **Enable Rev IQ** checkbox.

> 📘 Note
>
> Live subtitles also require a [Rev IQ license](doc:rev-license-types-and-add-ons) and a DME on v3.25 or higher where you have created streams. If you do not have any applicable DMEs this setting is not configurable.

Once enabled, you can then select the DME and DME stream you want to use for your event.

* During the event, the DME pushes an RTMPS stream through an outgoing TCP connection through port(s) 1936, 1937, 1938, or 1939. Please configure the Firewall accordingly. As a reminder, RTMP/RTMPS pushes do *not* utilize proxies even if configured on the DME.
* The stream will have subtitles added via embedded WebVTT that are distributed via [automatic reflection and automatic multicast](doc:automatic-multicast-and-reflection) (if enabled)
* The recommended best practice is to make sure the source stream from your encoder is active before starting the event so the DME is able to push immediately. This means the worst case is that Rev will wait up to 90 seconds. If the Push fails to start in time, Rev will fall back to using the configuration from the Presentation Profile with no subtitles.

![](https://files.readme.io/b999684-presentationProfileRevIq.png "presentationProfileRevIq.png")