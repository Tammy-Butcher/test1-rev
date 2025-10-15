---
title: Add a Set Top Box or Additional Display Device
excerpt: >-
  This guide provides a step-by-step reference to setting up Set Top Boxes in
  Rev so that you can stream Live channels.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## Add a Set Top Box

Use the **Set Top Boxes** module to add and configure STBs that have been identified by DMEs in your system. When you designate a DME in your system as an [STB Connector DME](doc:set-up-an-stb-connector-dme) and it receives a **SAP Announcement **from an **Active **STB, it passes on the relevant information needed by Rev. If all information is correct, the STB is automatically created under the **Pending STBs** tab. An Account Admin must then accept those STBs on the tab to configure **Channel Settings** on the **Current STBs** tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5dbabc4-settopBoxes.png",
        null,
        "Use the Set Top Box Management module to accept Pending STBs found by Rev and configure Current STB channels"
      ],
      "align": "center",
      "caption": "Use the Set Top Box Management module to accept Pending STBs found by Rev and configure Current STB channels"
    }
  ]
}
[/block]


STB requirements:

- MF-STB v2.0.1+ (Only Vbrick Multi-Format Set Top Boxes are supported at this time)
- Rev 7.16+
- DME 3.16+ as the STB Connector DME
- Only RTP/RTSP/H.264 unicast/multicast stream formats are supported
- Videos must be Active before they can be streamed
- To use Zones, you must stream the URL through a Presentation Profile

STB workflow for use with Rev:

1. Upload a video through a [URL Link](doc:link-to-video-urls). (This prepares videos for STB use)

2. Prepare a DME as an [STB Connector DME](doc:set-up-an-stb-connector-dme). (This provides a connection between Rev and STBs)

3. Accept a Pending STB. (Find the STBs discovered)

4. Configure Rev Channel Streams for STBs. (Configure previously added video channels)

5. Set a Channel Stream for a Current STB. (Set a channel on your STB)

### Accept a Pending Set Top Box

After a DME is designated as a [Connector STB](doc:set-up-an-stb-connector-dme), it listens for any STBs that are setup and places them under the **Pending STBs** tab for you to accept and then configure in Rev.

Note that the **Host Name**, **IP Address**, and **MAC Address** of the STB are displayed if you need them.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8523969-pendingStbs.png",
        "pendingStbs.png",
        1202
      ],
      "align": "center",
      "caption": "A Connector DME \"listens\" for Set Top Boxes and any it \"finds\" are placed under the Pending STBs tab"
    }
  ]
}
[/block]


To accept a pending STB:

1. Select the checkbox to the left of the STB.

2. Click the **Bulk Actions** dropdown menu and choose **Accept STBs**.

3. The STB is moved immediately to the **Current STBs** tab where you can now configure it. This means it is now available to stream a **Channel**.

4. You also receive a confirmation notice next to the **Pending STBs** tab that the STB(s) have been accepted (or an error message if it is offline).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e8ec6ac-pendingStbAccepted.png",
        "pendingStbAccepted.png",
        505
      ],
      "align": "center",
      "caption": "The STB(s) are accepted if they are not offline"
    }
  ]
}
[/block]


### Add Rev Channels Streams

The **Channel Settings** button is used to add channel streams for Current STBs. You _must_ have previously added an IPTV stream in Rev using the [Add URLs](doc:link-to-video-urls) tab.

To add a Channel stream for a STB to use:

1. Click the **Channel Settings** button on the **Set Top Box Management** module.

2. Each previously configured channel is listed. These are the channels that may now be streamed to a STB through **Devices **> **Current STBs**. You may click the **Edit **(pencil) icon or **Delete **(x) icon as needed.

3. To add a new Channel to use with a **Current STB**, click the **Add Channel** button at the bottom of the channel list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1dd333a-channelSettings.png",
        "channelSettings.png",
        505
      ],
      "align": "center",
      "caption": "Channels here are previously added through the Add Video > Add URLs function first"
    }
  ]
}
[/block]


4. In the **Add Channel** form, enter a **Channel Number **(you may not enter a duplicate) and search for previously added channels in the **Find Items** box to add them.  They do not appear here unless previously added through the **Add Videos** function.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/348a32e-addNewChannel.png",
        "addNewChannel.png",
        505
      ],
      "align": "center",
      "caption": "To prepare a new Channel for use with an STB, you must add it in Channel Settings"
    }
  ]
}
[/block]


5. Click **Done **to add the channel and it is ready for streaming on a **Current STB**. 

### Set a Channel Stream for a Current STB

Once channels have been added to Rev through **Add Videos** and then setup to work with STBs in **Channel Settings**, you are then able to add them to one or more STBs to stream as needed on the **Current STBs** tab.

To set a Channel stream for a Current STB:

1. Click the **Current STBs** tab.

2. Select the checkbox to the left of the STB(s) that you want to stream channel(s) to.

3. Click the **Bulk Action** dropdown and select **Set Channel**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1577343-setChannelStream.png",
        "setChannelStream.png",
        505
      ],
      "align": "center",
      "caption": "Choose the channel to stream in the Set Channel dropdown.  It streams on the channels you selected."
    }
  ]
}
[/block]


4. In the **Set Channel** dropdown, you can select a channel stream to play on the STB. You can also specify if **Closed Captions** are enabled. Note that the video itself must have closed captions for this to function.

5. Click **Save **to stream the channel on the STB(s) you selected.  The **Status **column updates once tuning is complete.

> 📘 Note
> 
> If the Connector DME does not receive updates from an STB, it is marked **Offline **in the **Status **column.
> 
> The MF-STB is a 100 Base-T (100 Mbps) network connection. On 1Gbps network environments, some inexpensive, unmanaged 10/100/1000 Base-T switches (responsible for communicating with the MF-STB) introduce playback issues due to amount of buffering and flow control (specifically for converting 1000 down to 100 Base-T). 
> 
> If you are having playback issues, connect the MF-STB directly to a better managed switch, or investigate a good quality 100 Base-T switch to deploy between the MF-STB and your current managed switch.

## Edit STB Credentials

To edit STB credentials, click the **Name **of the STB on the **Current STBs** tab. You can edit the **Device Name**, **Username**, and **Password**.

> ❗️ Warning!
> 
> If you create a custom password for the STB in Rev and its **control IP** or **Port **is modified in the DME, the STB custom password _will_ have to be re-entered again in REV. 
> 
> Until it is re-entered, the STB’s status will appear as “**Invalid Credentials**”.

## Delete an STB

One or more STBs may be deleted through the **Bulk Action** dropdown on the **Current STBs** tab.  Click the checkbox next to the STB(s) you want to delete and then click **Bulk Action** > **Delete**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/740861f-deleteStb.png",
        "deleteStb.png",
        351
      ],
      "align": "center",
      "caption": "Current STBs that are deleted are moved to the Pending STBs tab"
    }
  ]
}
[/block]


## Set the Status of an STB

The status of one or more STBs may edited through the **Bulk Action** dropdown on the **Current STBs** tab.  Click the checkbox next to the STB(s) you want to edit and then click **Bulk Action** > **Set to Active** or **Set to Inactive**.  The status of the STB is set accordingly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d865bd1-setStatusStb.png",
        "setStatusStb.png",
        335
      ],
      "align": "center",
      "caption": "Use the Bulk Action dropdown to modify the status of the STB as needed"
    }
  ]
}
[/block]


If the STB is set to **Inactive**:

- The current channel is blanked out and is no longer listed for the STB
- The Status column is set to **Inactive**
- Channels may not be set