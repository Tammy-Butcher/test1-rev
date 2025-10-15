---
title: RTMP/RTMPS Event Set Up
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
An **RTMP **or **RTMPS Stream** can be used as a source for a Rev event. In this case, Rev Cloud natively accepts (using a cloud listener) and ingests an RTMP or RTMPS stream (1080-resolution streams supported), optionally enriches it with [Rev IQ](doc:rev-ai), creates [multiple bitrates](doc:video-conference-vc-integrations), and delivers via directly from CDN or optionally utilizing [DME automatic multicast and reflection](doc:automatic-multicast-and-reflection). Distribution is fully controlled at the Zone level, and any RTMP or RTMPS ingested by Rev is automatically securely available from the CDN within the Default Zone without additional configuration.  

RTMP and RTMPS streaming is useful if you are utilizing or integrating with a service and/or encoder that outputs RTMP or RTMPS. Current advancements in remote or cloud-based video production often utilizes RTMP/RTMPS and this ingest method makes distributing those productions easy and convenient.

When using an RTMP or RTMPS source, Rev provides the location where the stream should be pushed *to*. This is done during event set up where Rev provisions a **Push URL** and **Stream Key**. The Push URL represents the destination; where the RTMP or RTMPS stream is pushed *to*. The Stream Key is necessary and provided for extra security. 
[block:callout]
{
  "type": "warning",
  "title": "Important!",
  "body": "Note that Rev also starts the **cloud listener** for the Push URL at the event **Start time**. This means that the listener is *not *available (or even IP resolvable) *before *the event begins. \n\nAs a result, pushing to the RTMP or RTMPS URL before the event starts will fail -- as the instance and its IP are not defined. When the listener has been provisioned, a **Waiting for Stream** message is displayed in the Host event UI and you can then begin your external RTMP or RTMPS push to the Push URL at that time."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23686cc-rtmpWebcast.png",
        "rtmpWebcast.png",
        902,
        247,
        "#ddeef8"
      ]
    }
  ]
}
[/block]
Once **RTMP/RTMPS Stream** is selected as the Video Source, the **Push URL** and **Stream Key** are generated automatically and may be copied using the copy buttons. 

Note that both of these can only be used on one Rev event at a time are not usable outside of a webcast. Click the **Regenerate URL and Key** button if needed.

These steps add an RTMP or RTMPS Stream to your event. However, there are some logistics and timing that should be taken into account. Consider the following as a model for running an RTMP or RTMPS sourced Event.

1. Create your event and configure it for **RTMP **or **RTMPS**.

2. At the time of your event (or during Lobby Time), **Start** the Webcast (but do *not* **Broadcast**). Starting the Webcast begins the process of provisioning the listener as described above.  

3. Once the listener provisioning process is complete (and the hostname IP resolvable), the **Waiting for Stream** message is displayed in the Host Event UI.  At this time you can begin your external RTMP or RTMPS push to the **Push URL**.
[block:callout]
{
  "type": "success",
  "title": "Use Case Example",
  "body": "A big use case is the employing the Vbrick encoder or an external RTMP source to supply the video of your event. Our 9000 Encoders work very well for this use case, and are integrated into the stop/start processes of event. \n\nIf you are using a 3rd party or external service (like an encoder or remote production toolset) --  please test. Once you've tested, test again. And lastly, test. Focus on the start/stop transitions of getting the streams to communicate to Rev and to the end players.\n\nAlso, By now you will have noticed that each event generates a new and unique **Push URL** and **Stream Key**.  There is no ability to change these settings (this is by design to avoid collisions and spoofing). So every new event changes the **Push URL** and **Stream Key** and must also be changed on the RTMP or RTMPS capture device or service. This approach supports higher security profiles.  However, if you find that you want to use a consistent **Push URL** and **Stream Key** (because you don't want to update your encoders or RTMP source), then save your event as a Template.  Templates save the **Push URL** and **Stream Key**, and can be applied to new events, and hence, will have the same RTMP or RTMPS configuration."
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "If you are pushing a stream to Rev from behind a firewall, you may need to open ports 1936, 1937, 1938 and 1939 for outgoing TCP connections. \n\nFlash browser playback for RTMP streams has been deprecated and is not available through Rev. While this service uses the RTMP protocol, it uses RTMP for distribution and not presentation. This continues to be a very common method for distributing video with low latency, from encoders to cloud based presentation/producer tools."
}
[/block]