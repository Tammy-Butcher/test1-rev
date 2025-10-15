---
title: RTMP/RTMPS Event Set Up
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
An **RTMP** or **RTMPS Stream** can be used as a source for a Rev event. In this case, Rev Cloud natively accepts (using a cloud listener) and ingests an RTMP or RTMPS stream (1080-resolution streams supported), optionally enriches it with [Rev IQ](doc:rev-ai), creates [multiple bitrates](doc:video-conference-vc-integrations), and delivers via directly from CDN or optionally utilizing [DME automatic multicast and reflection](doc:automatic-multicast-and-reflection). Distribution is fully controlled at the Zone level, and any RTMP or RTMPS ingested by Rev is automatically securely available from the CDN within the Default Zone without additional configuration.  

RTMP and RTMPS streaming is useful if you are utilizing or integrating with a service and/or encoder that outputs RTMP or RTMPS. Current advancements in remote or cloud-based video production often utilizes RTMP/RTMPS and this ingest method makes distributing those productions easy and convenient.

When using an RTMP or RTMPS source, Rev provides the location where the stream should be pushed *to*. This is done during event set up where Rev provisions a **Primary Push URL** and **Primary Stream Key**. The Primary Push URL represents the destination where the RTMP or RTMPS stream is pushed *to*. The Primary Stream Key is necessary for extra security. 

> 🚧 Important!
>
> Note that Rev also starts the **cloud listener** for the Push URL ONLY at the event **Start time** (which includes pre-production). This means that the **cloud listener** is *not* available (or even IP resolvable) *before* the event begins. 
>
> As a result, pushing to the RTMP or RTMPS URL before the event starts will fail -- as the instance and its IP are not defined. When the listener has been provisioned, a **Waiting for Stream** message is displayed in the Host event UI and you can then begin your external RTMP or RTMPS push to the Push URL at that time.

<Image title="rtmpWebcast.png" align="center" src="https://files.readme.io/d069b8ea6edae55f433c263b336821f2b4a38ddeab9715936f76ac003afb8931-rtmpWebcast.png" />

Once **RTMP/RTMPS Stream** is selected as the Video Source, the **Primary Push URL** and **Primary Stream Key** are generated automatically and may be copied using the copy buttons. 

You can also choose to enable a **Backup Stream** which then generates a **Backup Push URL** and **Backup Stream Key** in the event an issue occurs with your Primary Stream.  By enabling a Backup Stream, this creates RTMP stream redundancy which duplicates all services, recordings, and applications of a Webcast's features. 

<Image align="center" src="https://files.readme.io/e3798919961cad5ac040d8b3e284387be0c0c80147322bff05a552189a05b8b6-rtmpSwitch2BackupStream.png" />

This means that Event Hosts are able to toggle back and forth between the Primary and Backup streams as needed when hosting the event for increased reliability and uptime. This means that you have less failure points during high-profile live events and/or mission critical broadcasts.

Note that both of these can only be used on *one* Rev event at a time are not usable outside of a webcast. You can click the **Regenerate URL and Key** button(s) if needed which will change the value in the fields.

> 📘 Note
>
> The **Backup Stream** feature is disabled by default and has licensing and recording implications.  Make sure you review both before you enable this feature.

The following steps add an RTMP or RTMPS stream to your event. There are some logistics and timing that should be taken into account. Consider the following as a model for running an RTMP or RTMPS sourced event.

1. Create your event and configure it for **RTMP** or **RTMPS**. 

2. Decide if you want to enable a Backup Stream for the event taking into consideration that this feature is designed for two concurrent streams and full redundancy. It also has licensing requirements that you should consider.

3. At the time of your event (or during Lobby Time), **Start** the Webcast (but do *not* **Broadcast**). Starting the Webcast begins the process of provisioning the listener as described above.  

4. Once the listener provisioning process is complete (and the hostname IP resolvable), the **Waiting for Stream** message is displayed in the Host Event UI.  You can now begin your external RTMP or RTMPS push to the **Push URL**.

5. View the [Best Practices](doc:rtmprtmps-event-set-up#best-practices) section below to take full advantage of the RTMP redundancy feature.

> 📘 Note
>
> If you are pushing a stream to Rev from behind a firewall, you may need to open ports 1936, 1937, 1938 and 1939 for outgoing TCP connections. 
>
> Flash browser playback for RTMP streams has been deprecated and is not available through Rev. While this service uses the RTMP protocol, it uses RTMP for distribution and not presentation. This continues to be a very common method for distributing video with low latency, from encoders to cloud based presentation/producer tools.

If you enable a **Backup Stream**, the Event Host is easily able to toggle from the **Primary Push URL** to the **Backup Push URL** and then back again by using the **Event Details** flyout and then clicking the switch button if a problem occurs with the stream that is being used at the time.

<Image alt="Use the Switch button to toggle between streams (if necessary) when a Backup Stream is enabled" align="center" src="https://files.readme.io/31daf91c89475d5b62964c5d9cac4317eb4943434abd77d5534d0624506090e1-rtmpBackupStreaming.png">
  Use the Switch button to toggle between streams (if necessary) when a Backup Stream is enabled
</Image>

> 🚧 Important!
>
> When switching streams, audio settings for both the Host/Admin players and the Attendee's players revert to default audio settings. For example, this means that if a player is muted, it will unmute each time a stream is switched.

## Use Case Tips

You can use a Vbrick encoder or an external RTMP source to supply the video of your event.  Vbrick's 9000 encoders work well and are integrated into the stop/start processes of events.

Please note that if you are using a 3rd party or external server (such as an encoder or remote production toolset), make sure you thoroughly test it before your event. There is *no* ability to *change* the settings once the event begins other than switching the stream(s) (this is by design to avoid collisions and spoofing). 

This also means that every *new* event changes the **Push URLs** and **Stream Keys** and, as a result, must also be changed on the RTMP or RTMPS capture device or service.  This approach supports higher security profiles.

If you find that you want to use a consistent Push URL and Stream Key to avoid updating encoders or RTMP sources continually, you can save your event as a template.  [Webcast templates](doc:create-a-webcast-template) save the Push URLs and Stream Keys and can then be applied to new events which means the new event will have the same RTMP or RTMPS configuration.

## Backup Stream VOD Recording Considerations

If you enable the **Backup Stream** feature it is important to understand that recording features associated with the event apply to *both* RTMP ingest stream recordings. This means that even though there is only *one* event, there may be *two* recordings.  The implications are:

* Two recordings is twice the [Viewing Hours](doc:rev-license-types-and-add-ons#license-types) for licensing.
* Two streams is twice the subtitles – both counted against [Rev IQ Credits](doc:rev-license-types-and-add-ons#rev-iq-credits).
* The **Backup VOD** is named with the event title and includes “backup” attached at the end.  Only if the recording is provided.
* The completed [event link](doc:link-and-redirect-a-webcast-recording-to-a-completed-event) will point to *last used* stream in the Webcast.
* If the **Backup Stream** feature is enabled and you do *not* need to switch streams at any time, the backup recording is deleted and only one recording is saved so that duplicates do not occur. However, you are still charged for the associated recording costs on your license for the [viewing hours](doc:rev-license-types-and-add-ons#license-types) and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) for the secondary stream.

## Best Practices

The **Backup Stream** feature is designed to create redundant RTMP streams.  That means it is designed for two *concurrent* streams: a primary and a backup. Please start your streams *simultaneously* and ensure they are available during the event.  The Event will initially be set to the **Primary Stream**.

This also means that a best practice for RTMP redundancy to occur requires redundancy *all the way from the camera*.  This means you should have an *entirely separate* camera and encoder pushing to the **Backup Push URL** from the camera and encoder that is pushing to your **Primary Push URL**.  This is the *only* way that you can remove single points of failure from the event to the Rev RTMP ingest servers.
