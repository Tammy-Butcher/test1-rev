---
title: License Types and Modules
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
When your Rev portal is initially configured, a **License Module** and **License Type** is purchased and configured depending on your organizational needs. Additional licensing and **Add-On Components** may also be purchased and applied to the license, depending upon the types purchased.

> 👍 Tip
> 
> Rev Cloud licenses are managed and applied by Vbrick. However, you may add and manage your own [Child Accounts](doc:view-and-edit-account-details#portal-child-accounts) within the scope of that license.

## Modules

There are four different types of modules you can activate in Rev.  Depending on the module purchased, various license types are available to apply. 

[block:parameters]
{
  "data": {
    "h-0": "Rev Module Name",
    "h-1": "Description",
    "h-2": "Available License Types",
    "0-0": "Vbrick Rev (Full)",
    "0-1": "Provides customers the ability to use the full breadth of Live, Video On-Demand, IPTV and access to eCDN capabilities, including peer delivery, edge caching and multicast.",
    "0-2": " **Named User** and **Active User**.  \n  \nSome customers may also have **Hours-based** licenses.",
    "1-0": "Vbrick Video On-Demand",
    "1-1": "Provides customers the ability to use video on-demand capabilities, including screen recording, upload, meeting recording, video portal and embedding capabilities.",
    "1-2": "**Named User** and **Active User**.",
    "2-0": "Vbrick Universal eCDN",
    "2-1": "Provides customers the ability to use eCDN capabilities for live video and video on-demand caching. This includes access to peer delivery, edge caching and multicast, depending upon licensing. Includes the ability to use native eCDN integrations in 3rd party streaming platforms.",
    "2-2": "**Concurrent** and **ELA**.",
    "3-0": "Vbrick Distribution",
    "3-1": "Provides customers the ability to use eCDN capabilities for live video and video on-demand caching. This includes access to peer delivery, edge caching and multicast, depending upon licensing. Also includes the ability to use available video conference integrations and RTMP as a source.",
    "3-2": "**Named User**, **Active User**, and **Hours-Based**"
  },
  "cols": 3,
  "rows": 4,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


## License Types

The table below describes the various license types available to apply to the Rev modules.

> 🚧 Important!
> 
> This documentation always attempts to remain up-to-date.  However, you should _always_ check with your Account Manager _before_ making any major licensing decisions or purchases.

| License Type            | Description                                                                                                                                                                                                                                                                                      |
| :---------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Active User License     | All viewing and recording (Rev and guest accounts) is dictated solely by the **maximum number** of licensed users who log in during a **calendar month** during the course of an annual term. Active Users licenses do not have a hard cap, but overages could result in an additional purchase. |
| Named User License      | Viewing and recording is dictated by the number of **user accounts** purchased. All guest/external viewing (non-Rev accounts) is dictated by the number of **add-on component hours** purchased for guest viewing.                                                                               |
| Concurrent User License | Purchased for use with the Vbrick Universal eCDN module. Concurrent users licenses do not have a hard cap, but overages could result in an additional purchase.                                                                                                                                  |
| Hours-Based License     | All viewing and (some) recording (Rev and guest accounts) is dictated solely by the **number of hours** purchased.  This license is available for Vbrick Distribution.                                                                                                                           |

## Licensed Add-On Components

Additional **Add-On Components** may be purchased and applied to either license type at any time. These are required for certain functions in Rev as noted below.

[block:parameters]
{
  "data": {
    "h-0": "Add-On",
    "h-1": "Description",
    "0-0": "Hours",
    "0-1": "For customers with **Hours-based** accounts, one hour is consumed per user hour of video viewing.  \n  \nFor customers with **User-based **accounts, hours are only consumed for public/unauthenticated viewing at a rate of one hour per hour of video viewing.  \n  \nHours are also consumed for live event streaming or recordings sourced via RTMP, video conferencing, producer, and screen recordings.  In this case, hours are consumed at a rate of three (3) hours per hour of usage.   \n  \nFor example, if a Webcast is 2 hours long, then 6 hours will be consumed.  The entirety of the event, including any pre-production or overflow is included.   Auto-ingesting of Webex Meetings videos also counts toward hours consumed at a rate of 1 per hour of meeting recording.  \n  \nHours can be purchased for additional [Guest](doc:manage-security-parameters#enable-guest-portal-access) viewing on User-based licenses. One hour is consumed per user hour of video viewing.  \n  \nNote:  If [RTMP redundancy](doc:rtmprtmps-event-set-up) is enabled, hours consumption is doubled because two streams are utilized.",
    "1-0": "Vbrick Peer-to-Peer Peer Meshes",
    "1-1": "Used to specify the **Peer Mesh Allotment** and add [Vbrick Peer-to-Peer](doc:rev-connect-zones) enabled zones to Rev. Each peer mesh supports 25 concurrent users viewing a live event. Included with Rev EVP, Vbrick Universal, and Vbrick Distribution licenses.",
    "2-0": "Rev AI",
    "2-1": "Used to allocate **Rev IQ Credits** which can then be used to enable and use **AI & Machine Learning** components in Rev.  \n  \nThis includes such features as [Facial Recognition](doc:facial-recognition) and [Vbrick Transcription and Translation](doc:rev-iq-transcription-and-translation) services."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Rev IQ Credits

When using the [Rev AI](doc:rev-ai) add-on component, credit consumption is calculated either based on each hour of video processing or tokens, dependent on the type of AI powering the processing. “Hour” refers to the length of time associated with the video being processed. “Token” refers to unique digital assets (like text) that enable the interaction with and creation of content by AI models. 

The table below details how many **Rev IQ Credits** are required for hour-based processing per Rev AI feature. Please make sure you confirm this with your Vbrick Account Manager.

| Rev AI Hours Feature                                       | Rev IQ Credits Required |
| :--------------------------------------------------------- | :---------------------- |
| Facial Recognition (per 1 hour)                            | 3                       |
| Rev IQ VOD Transcription (per 1 hour)                      | 1                       |
| Rev IQ VOD Voice Generation (per 1 hour)                   | 1                       |
| Rev IQ Live Transcription (per 1 hour)                     | 2                       |
| Rev IQ Translation - Live or VOD (per language per 1 hour) | 1                       |
| Rev IQ Workflow Content Analysis (per 50 AI steps)         | 1                       |

> 📘 Note
> 
> If you have [RTMP Redundancy](doc:rtmprtmps-event-set-up) enabled, Rev IQ Live Transcription is counted as two streams and twice the subtitles.

The table below details how many **Rev IQ Credits** are required for token-based processing per token type for the generative AI [Video Assistant](doc:vbrick-assistant) feature.

| Cost                                        | Rev IQ Credits |
| :------------------------------------------ | :------------- |
| 1,000 Embedding Tokens (Process Transcript) | 0.0005         |
| 1,000 Input Tokens (Process Question)       | 0.0085         |
| 1,000 Output Tokens (Produce Answer)        | 0.028          |

The table below details how many **Rev IQ Credits** are required for token-based processing per token type for the generative [Video Metadata Generation](doc:video-title-description-and-tags#use-vbrick-generative-ai-for-automatic-video-metadata-generation) features.

| Cost                                                               | Rev IQ Credits |
| :----------------------------------------------------------------- | :------------- |
| 1,000 Input Tokens (Process Transcript)                            | 0.0057         |
| 1,000 Output Tokens (Produce Titles, Descriptions, Tags, Chapters) | 0.0187         |

The table below details _approximations_ of **Rev IQ consumption** based on average usage and will vary based on actual usage. Actual usage can be tracked via the [Get Rev IQ Credits Usage](ref:getaccountiqcreditsusage) API.

| Rev AI Tokens Feature                                              | Rev IQ Credits |
| :----------------------------------------------------------------- | :------------- |
| Titles (approximately every 70 hours)                              | 1              |
| Descriptions (approximately every 10 hours)                        | 1              |
| Tags (approximately every 70 hours)                                | 1              |
| Chapters (approximately every 10 hours)                            | 1              |
| Generate All Metadata (approximately every 10 hours)               | 1              |
| Video Assistant (approximately every 20 short conversations)       | 1              |
| Video Assistant (approximately every 10 long conversations)        | 1              |
| Multimedia Analysis - Images (approximately every 130 1-MP images) | 1              |
| Multimedia Analysis - PDF (approximately every 25 3-page docs)     | 1              |

### Vbrick Distribution: Rev IQ

Vbrick's Rev IQ add-on offering uses artificial intelligence (AI) to help users navigate and understand the video content they need across all your video assets. Access to the Live [Transcription and Translation](doc:rev-iq-transcription-and-translation) features that make up Rev IQ require the _full_ Vbrick Rev product.

| Feature                  | Vbrick Distribution |
| :----------------------- | :------------------ |
| Live Video Transcription | 2                   |
| Live Video Translation   | 1                   |

## Usage Tracking

- The [Account Admin Dashboard](doc:view-system-analytics#videos) keeps track of all **System Analytics** including hours, users, and active user log-ins allotted and used under the **Usage **tab.
- Portals that have a **Monthly Active Users** license activated will display an additional graph depicting **Monthly Active Users** (versus the current user licenses allotted to the portal). Active users is indicative for the month being referenced and can be greater than 100% in this case if the active count for the month exceeds the license count purchased.
- Email notifications are sent to Account Admins when an account has reached **75%** and **100%** usage of its allotted viewing hours for both **Users** and **Hours** based accounts.  For **Monthly Active Users**, if the active count exceeds the licensed user count, an email notification is also sent.
- When an account is switched from Hours based to Users/Active Users based, Rev switches all users in **Active **status to **Unlicensed **status.