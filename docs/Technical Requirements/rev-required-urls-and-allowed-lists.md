---
title: Required URLs and Allowed Lists
excerpt: >-
  This topic presents the URLs required, by data center, to access the Rev and
  Vbrick Universal eCDN Cloud portals and how to make sure your Allowed Lists
  are updated
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Accessing **Rev Cloud** or the **Vbrick Universal eCDN** requires that both Admin and end user’s browsers (either internal or external to customer networks) _and_ DMEs installed (within customers networks) are able to access various service URLs. 

There are several different technologies that may impede or restrict access to these URLs.  

For example, customers may leverage browser, proxy, or firewall lists to restrict URLs that can be accessed from an end user’s browser, and may have networking restrictions that limit the DME. Customers that have these types of network controls must provide access or reachability.

Along with adding your **Main Rev URL** and **Main Vbrick Universal eCDN URL** to the listed sites, it is important to review and add the **Data Center URLs** below to the **Allowed List** sites. 

> 👍 Tip
> 
> When possible, it is more preferable to add a generic `*.*.vbrickrev.com`, `*.us.vbrickrev.com`, `*.eu.vbrickrev.com`, `*.au.vbrickrev.com` allowed listing rule.
> 
> Keep in mind that browsers and DMEs (both internal and external) should also have access to 3rd-party systems where your streams will originate.

Note that your Rev Welcome e-mail contains the **Main Rev URL** that you use to access Rev or it may be a custom URL if you requested that instead. 

The URLs are listed by data center of your portal (i.e., where you are hosted).  Note which data center where you are hosted and allow access to those sites _in addition to_ your **Main Rev URL** and/or **Main Vbrick Universal eCDN URL**.  Please contact [Vbrick Support](https://portal.vbrick.com/open-a-case/) if you have any questions or need help identifying your hosting data center.

## North American Data Center

### Rev Browser URL / Domain Access Details

| Used By User (Browser)                 | Description                                                                                                                  | Used in Vbrick Universal eCDN |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- | :---------------------------- |
| <https://media.us.vbrickrev.com>       | This domain delivers all VOD and Live Streaming content from Vbrick cloud CDN.                                               | No                            |
| <https://static.us.vbrickrev.com>      | This domain delivers all Vbrick Rev portal static content (HTML, JS, CSS, Font etc.).                                        | Yes                           |
| <https://northamerica.rev.vbrick.com>  | This domain is used for Microsoft Teams, Webex, and Zoom integrations.                                                       | Yes                           |
| <https://webexlive.rev.vbrick.com>     | This domain is used when using Webex Live Streaming feature.                                                                 | Yes                           |
| <https://rev-connect.us.vbrickrev.com> | This domain is used for Vbrick Peer-to-Peer (RevConnect) distribution.                                                       | Yes                           |
| <https://*.vci.vbrickrev.com>          | This domain is used for Video Conference Integration (VCI) i.e. Microsoft Teams, Webex, Zoom. Pexip etc. and RTMP streaming. | No                            |
| <https://grs.vbrickrev.com>            | This domain is used for Microsoft Teams, Webex and Zoom integrations and Vbrick Mobile App.                                  | Yes                           |

### DME Domain Access Details

| Used By DME                                                                                                     | Description                                                                                                       | Used in Vbrick Universal eCDN |
| :-------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------- | :---------------------------- |
| <https://media.us.vbrickrev.com>                                                                                | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 | No                            |
| <https://dme-update.us.vbrickrev.com>                                                                           | This domain is used to update DME from Vbrick Rev cloud.                                                          | Yes                           |
| <https://vbrick-prod01-dme-logs.s3.amazonaws.com> & <https://vbrick-prod01-dme-logs.s3.us-east-1.amazonaws.com> | This domain is used to send DME logs to Vbrick Rev cloud i.e. "Request Logs" feature.                             | Yes                           |
| <https://gs-streaming-prod01.s3.amazonaws.com> & <https://gs-streaming-prod01.s3.us-east-1.amazonaws.com>       | This domain is used by DME to push live streaming content to Vbrick Rev cloud for cloud delivery of that content. | No                            |

## EU Data Center

### Rev Browser URL / Domain Access Details

| Used By User (Browser)                 | Description                                                                                                                  | Used in Vbrick Universal eCDN |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- | :---------------------------- |
| <https://media.eu.vbrickrev.com>       | This domain delivers all VOD and Live Streaming content from Vbrick cloud CDN.                                               | No                            |
| <https://static.eu.vbrickrev.com>      | This domain delivers all Vbrick Rev portal static content (HTML, JS, CSS, Font etc.).                                        | Yes                           |
| <https://europe.eu.vbrickrev.com>      | This domain is used for Microsoft Teams, Webex, and Zoom integrations.                                                       | Yes                           |
| <https://webexlive.eu.vbrickrev.com>   | This domain is used when using Webex Live Streaming feature.                                                                 | Yes                           |
| <https://rev-connect.eu.vbrickrev.com> | This domain is used for Vbrick Peer-to-Peer (RevConnect) distribution.                                                       | Yes                           |
| <https://*.vci.vbrickrev.com>          | This domain is used for Video Conference Integration (VCI) i.e. Microsoft Teams, Webex, Zoom. Pexip etc. and RTMP streaming. | No                            |
| <https://grs.vbrickrev.com>            | This domain is used for Microsoft Teams, Webex and Zoom integrations and Vbrick Mobile App.                                  | Yes                           |

### DME Domain Access Details

| Used By DME                                                                                                        | Description                                                                                                       | Used in Vbrick Universal eCDN |
| :----------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------- | :---------------------------- |
| <https://media.eu.vbrickrev.com>                                                                                   | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 | No                            |
| <https://dme-update.eu.vbrickrev.com>                                                                              | This domain is used to update DME from Vbrick Rev cloud.                                                          | Yes                           |
| <https://vbrick-prod02-dme-logs.s3.amazonaws.com> & <https://vbrick-prod02-dme-logs.s3.eu-central-1.amazonaws.com> | This domain is used to send DME logs to Vbrick Rev cloud i.e. "Request Logs" feature.                             | Yes                           |
| <https://gs-streaming-prod-02.s3.amazonaws.com> & <https://gs-streaming-prod-02.s3.eu-central-1.amazonaws.com>     | This domain is used by DME to push live streaming content to Vbrick Rev cloud for cloud delivery of that content. | No                            |

## AU Data Center

### Rev Browser URL / Domain Access Details

| Used By User (Browser)                 | Description                                                                                                                  | Used in Vbrick Universal eCDN |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- | :---------------------------- |
| <https://media.au.vbrickrev.com>       | This domain delivers all VOD and Live Streaming content from Vbrick cloud CDN.                                               | No                            |
| <https://static.au.vbrickrev.com>      | This domain delivers all Vbrick Rev portal static content (HTML, JS, CSS, Font etc.).                                        | Yes                           |
| <https://asiapacific.au.vbrickrev.com> | This domain is used for Microsoft Teams, Webex, and Zoom integrations.                                                       | Yes                           |
| <https://webexlive.au.vbrickrev.com>   | This domain is used when using Webex Live Streaming feature.                                                                 | Yes                           |
| <https://rev-connect.au.vbrickrev.com> | This domain is used for Vbrick Peer-to-Peer (RevConnect) distribution.                                                       | Yes                           |
| <https://*.vci.vbrickrev.com>          | This domain is used for Video Conference Integration (VCI) i.e. Microsoft Teams, Webex, Zoom. Pexip etc. and RTMP streaming. | No                            |
| <https://grs.vbrickrev.com>            | This domain is used for Microsoft Teams, Webex and Zoom integrations and Vbrick Mobile App.                                  | Yes                           |

### DME Domain Access Details

| Used By DME                                                                                                          | Description                                                                                                       | Used in Vbrick Universal eCDN |
| :------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------- | :---------------------------- |
| <https://media.au.vbrickrev.com>                                                                                     | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 | No                            |
| <https://dme-update.au.vbrickrev.com>                                                                                | This domain is used to update DME from Vbrick Rev cloud.                                                          | Yes                           |
| <https://vbrick-prod03-dme-logs.s3.amazonaws.com> & <https://vbrick-prod03-dme-logs.s3.ap-southeast-2.amazonaws.com> | This domain is used to send DME logs to Vbrick Rev cloud i.e. "Request Logs" feature.                             | Yes                           |
| <https://gs-streaming-prod-03.s3.amazonaws.com> & <https://gs-streaming-prod-03.s3.ap-southeast-2.amazonaws.com>     | This domain is used by DME to push live streaming content to Vbrick Rev cloud for cloud delivery of that content. | No                            |

<br />

> 📘 Note
> 
> For DME [Live Subtitles](doc:video-sources#live-event-subtitles) and [RTMP(S) sourced webcasts](doc:video-sources#rtmprtmps-sourced-events), you may need to open outgoing TCP traffic on ports 1936, 1937 ,1938, and 1939.  The hostname for the cloud destination will be \*.vci.vbrickrev.com but please note this connection does not use HTTP or HTTPS so it will not work through a proxy.  
> 
> For [Rev Producer](doc:producer-event-set-up) and [Screen Share and Record](doc:screen-share-and-record), you may need to open additional outgoing TCP and UDP traffic on ports 27768 to 31768.