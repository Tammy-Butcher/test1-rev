---
title: Video Conference, RTMP, and Other Sourced Streams
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
[block:html]
{
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>&#128187; <a href=\"/docs/vbrick-distribution\">Vbrick Distribution</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


Rev Cloud supports many different ways to ingest Live streams, which includes **cloud sourced** streams and local streams that are pushed into DMEs.  

This section covers the **cloud sourced** streams. We group these **cloud sourced** streams into **Single Stream** solutions (Webex Live, RTMP/RTMPS which includes Remote Production systems) and **Dual Stream** solutions (VC / Video Conferencing solutions, SIP, Webex Meeting, MS Teams, and Zoom).  During webcast events, Rev takes in the streams, optionally enriches them (utilizing Rev IQ) and ultimately generates an MBR (multiple bitrate) HLS for Live playback within our HTML 5 player.

This section deals with resolutions and bitrates for both **Single Stream** and **Dual Stream** captures. Remember, as resolution and bitrate are reduced (for example in the **Medium** and more pointedly in the **Low** bitrate) the crispness, readability, and quality of the video are challenged. These characteristics are impacted by a number of issues, not the least of which includes the **expanse** of video (e.g., isolated to a talking-head all the way up to a full landscape view), lighting or lack of lighting, the **degree of motion** within the video (e.g., still life to sports footage), and **font size** when readability of content within the stream is required. If your use case includes playback at the low setting, please test acceptability of both your **Speaker** and **Content** streams at that level.

> 🚧 Important
> 
> All Cloud-based recording (VCI, RTMP, and Webex Streaming) is limited to 10 hours.

## Single Stream  (RTMP/S)

**Single Stream** integration and capture is based around RTMP/RTMPS ingest.  This includes any standards-based **RTMP** generation from encoders or software (e.g., OBS Studio), web-based remote production capabilities (which generates RTMP/RTMPS), and our [Webex Live Integration](doc:webex-meetings#support-for-webex-meetings-live-streaming) (which is also RTMP, and not to be confused with our **Webex Meeting** integration which is **SIP ** based.)

There are two different sets of bitrates used for **Single Stream** / **RTMP/S** encoding and are selected based on the input stream resolution.  One set is used for resolutions **less than 1080 (1920x1080)**, and the second set is for any resolution **1080 or greater**.

For single stream resolutions **less than 1080** (most commonly 720 or lower), the following settings are used:

- **High**: Resolution as provided by stream -- preserving aspect ratio.  Target Bitrate is maximum of RTMP stream bitrate (if signaled within the stream) or 1.5Mbps.  This maintains the resolution and bitrate, so please plan accordingly.
- **Medium**: Resolution 540 (qHD) -- preserving aspect ratio. Target Bitrate is within 700Kbps to 1.0Mbps.  If possible, we will match the source bitrate if it is within that range.
- **Low**: Resolution 432 (FWQVGA) -- preserving aspect ratio. Bitrate targeting 688Kbps

The next set of resolutions and bitrates are for streams of **1080 or greater**.  These streams require greater bitrates to maintain quality.  When providing 1080 streams for ingest, please plan accordingly. 

For single stream resolutions **1080 or greater**, the following settings are used:

- **High**: Resolution 1080 (FHD) -- preserving aspect ratio.  Target Bitrate is maximum of RTMP stream bitrate (if signaled within the stream) or 1.8Mbps.  This maintains the bitrate, so please plan accordingly.
- **Medium**: Resolution 720 (HD) -- preserving aspect ratio. Target Bitrate is within 700Kbps to 1.0Mbps.  If possible, we will match the source bitrate if it is within that range.
- **Low**: Resolution 432 (FWQVGA) -- preserving aspect ratio. Bitrate targeting 688Kbps

It should be noted that Vbrick models streams using **16:9 resolutions **and the bitrates provided above may vary from the targets based on stream characteristics and content.

These three bitrate renditions are created for the captured stream and combined into multi-bitrate (MBR) HLS specification for an adaptive playback within our Adaptive Bitrate Vbrick Rev player. In this way, viewers that may be on congested or reduced bandwidth lines will automatically optimize for playback.

As always, test for acceptance at all bitrates for each stream against your particular needs, and plan accordingly.

## Dual Stream  (SIP/Webex/Zoom/Pexip/MS Teams/Producer)

**Dual Stream** integrations captures Video Conferencing systems that may have two different streams -- both an **Active Speaker** stream and a **Content** stream.  Vbrick provides unique capabilities to capture both streams while keeping them in sync, as well as normalizing the streams to a constant framerate (which is important for services that provide variable or very low framerates).

In order to accomplish ingesting these streams into Rev, Rev must provision a **Listener** to capture and process the dual streams.  The cloud **Listener** joins a VC call as a **SIP** participant (slightly different approach for Microsoft Teams, but conceptually the same).  Once connected and joined,  Rev receives and captures the individual **Speaker** and **Content Share** streams from the VC system.  Rev then enriches the stream (using Rev IQ if configured) and encodes several bitrates for each of the **Speaker**, **Content Share**, and (a generated) **Switched **streams. (Note: The Switched stream is a single stream version that displays the Speaker and then switches into and out of a Content view as content is shared.  This version is necessary for downloads and native mobile players.)

Similar to the single stream approach above, the three streams are automatically encoded into three bitrates – **High**, **Medium**, and **Low**. Each bitrate is actually a resolution specification encoded within a range of bitrates. 

For stream resolutions \<= 720, the settings are: 

- **High**: Resolution 720 (HD) Height fixed, Width calculated reserving original aspect ratio; Bitrate targeting 2.6M to 3.6M
- **Medium**: Resolution 540 (qHD) Height fixed, Width calculated reserving original aspect ratio; Bitrate targeting 1.0M to 2.0M
- **Low**: Resolution 432 (FWQVGA) Height fixed, Width calculated reserving original aspect ratio; Bitrate targeting 640K to 1.4M​

> 📘 Note
> 
> Vbrick models on 16:9 resolutions and the bitrate may vary below the target based on stream content.

The next set of resolutions and bitrates are for streams of 1080 or greater. These streams require greater bitrates to maintain quality. When providing 1080 streams for ingest, please plan accordingly.

For  stream resolutions between 721 and 1080 or greater, the following settings are used:

- **High**: Resolution 1080 (FHD) -- preserving aspect ratio. Target Bitrate is the stream bitrate (if signaled within the stream) or 4 to 8Mbps. These are heavier streams than the 720 so please plan accordingly.
- **Medium**: Resolution 720 (HD) -- preserving aspect ratio. Target Bitrate is within 1Mbps to 1.2Mbps. If possible, we will match the source bitrate if it is within that range.
- **Low**: Resolution 432 (FWQVGA) -- preserving aspect ratio. Bitrate targeting 750Kbps

> 📘 Note
> 
> Streams larger than 1080 will be transcoded and delivered at 1080 using the settings above.

Also, while Vbrick can capture up to 1080p streams, this resolution is negotiated between your VC system and Rev. If you find that your High level streams do not have the 1080 or 720 resolutions, please check the settings within your VC systems.

Note that [Producer](doc:producer-event-set-up) uses these MBR settings but is only single stream with 720 resolution.

As always, test for acceptance at all bitrates for each stream against your particular needs, and plan accordingly.

End points that are currently supported in Rev include:

- [Webex Meetings](doc:webex-meetings)  CMR
- [Webex Live Streaming](doc:webex-meetings#support-for-webex-meetings-live-streaming)
- Cisco CMS, DX, SX
- [Webex Teams](doc:webex-teams) 
- [Zoom](doc:zoom-integration) 
- [Microsoft Teams](doc:microsoft-teams)
- [Pexip](doc:pexip)

For hardware endpoints, Vbrick requires the device to be on the latest firmware/software.  While other systems may work, these are the only systems that Vbrick has qualified and supports through Vbrick Customer Support.  Additionally, Vbrick does not support EOL (End-of-Life) endpoints regardless of any previous support (which may supersede the above list.)

> 📘 Note
> 
> For best playback, VCI utilizing MBR requires a minimum WAN/LAN bitrate of 700Kbps for dual playback of both Speaker and Content (and less for single stream playback) per viewer. At this available WAN/LAN bitrate, the lowest VCI Speaker and Content will be shown. Playback below this threshold is not guaranteed for VCI MBR streams.
> 
> Additionally, for best playback, please configure your sources to be, at least, 5fps (frames per second).  Playback and quality below this threshold is not guaranteed.

## Requirements

- Rev Cloud

## Configuration

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/757b0e5-enableVcRecordingStreaming.png",
        "enableVcRecordingStreaming.png",
        1141
      ],
      "align": "center",
      "caption": "You must enable the Video Address Conference Integration checkbox to use VC/SIP addresses as video sources"
    }
  ]
}
[/block]


To enable VC/SIP based addressing:

1. Navigate to **Media Settings** > **Integrations**

2. Select the checkbox next to **Enable Video Address Conference Integration**.

3. Enter any [DTMF codes](doc:dtmf-configuration-and-usage) you want to use (optional).

## Usage

### Record a Video Conference

Once configured, Rev Cloud supports recording **Video Conferences** and ingesting them into your standard media workflow. The recordings will capture both active speaker and any content streams (if available).  

Vbrick’s player has been modified to display both streams and allow user control of layout.

To record a video conference:

1. Click the **Live Recording** tab > **Video Address** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/757159c-recordVidConference.png",
        null,
        "The Video Address option under the Recording tab displays all of Rev's native and integrated recording options available"
      ],
      "align": "center",
      "caption": "The Video Address option under the Recording tab displays all of Rev's native and integrated recording options available"
    }
  ]
}
[/block]


2. Enter a **Video Address**.

3. Enter a **Pin / Password** if one is set up.

4. Configure the [DTMF](doc:dtmf-configuration-and-usage#use-dtmf-codes-in-video-recording) codes you want to use with the recording if any. (optional)

5. If a valid **SIP URL/Video Address** is used, Rev connects to the conference room and begins recording when the **Start Recording** button is clicked.

### Schedule a Video Conference Webcast

You can use Rev Cloud to broadcast your video conferencing software so that you take advantage of your video conference while using Rev’s webcast features at the same time. Your video source is your VC SIP address once this is configured . 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7af3fe2-vcStreamWebcastUsage.png",
        "vcStreamWebcastUsage.png",
        1140
      ],
      "align": "center",
      "caption": "The Video Address tab is not visible on a Webcast Event until you enable the Video Address Conference integration"
    }
  ]
}
[/block]


When a VC Live Webcast event is scheduled:

- The event synchronizes and broadcasts what is shared on the Admin’s or Hosts VC screen.
- It must be used throughout the event. In other words, you may not use a video conference as the source for half the event and then switch to a “traditional” source (camera/presentation profile) for the second half of the event. You _must_ use one or the other source per event or an error occurs.
- You may use the configured [DTMF](doc:dtmf-configuration-and-usage#use-dtmf-codes-in-events) codes for the event. (optional)
- When you choose to save the recording at the end of your webcast using this streaming option, it counts against your licensed recording hours.
- When you start a webcast using this streaming option, the webcast is automatically recorded. At the end of the webcast, you are asked if the recording should be saved.
- As noted, this is a Rev Cloud feature only.