---
title: Required URLs and Allowed Lists
excerpt: >-
  This topic presents the URLs required, by data center, to access the Rev Cloud
  portal and how to make sure your Allowed List is updated if needed
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Accessing **Rev Cloud** requires that both end user’s browsers (either internal or external to customer networks) and DMEs installed (within customers networks) are able to access various Rev service URLs. There are several different technologies that may impede or restrict access to these URLs.  For example, customers may leverage browser, proxy, or firewall lists to restrict URLs that can be accessed from an end user’s browser, and may have networking restrictions that limit the DME. 

Customers that have these types of network controls must provide access or reachability.  Along with adding your **Main Rev URL** to the listed sites, it is important to review and add the **Data Center URLs** below to the **Allowed List** sites. 

> 👍 Tip
> 
> When possible, it is more preferable to add a generic `*.*.vbrickrev.com`, `*.us.vbrickrev.com`, `*.eu.vbrickrev.com`, `*.au.vbrickrev.com` allowed listing rule.

Note that your Rev Welcome e-mail contains the **Main Rev URL** that you use to access Rev or it may be a custom URL if you requested that instead. 

The URLs are listed by data center of your portal (i.e., where you are hosted).  Note which data center you are hosted, and allow access to those sites _in addition to_ your Main Rev URL.  Please contact [Vbrick Support](https://portal.vbrick.com/open-a-case/) if you have any questions.

## North American Data Center

### Rev Browser URL / Domain Access Details

| Used By User (Browser)                 | Description                                                                                                                  |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <https://media.us.vbrickrev.com>       | This domain delivers all VOD and Live Streaming content from Vbrick cloud CDN.                                               |
| <https://static.us.vbrickrev.com>      | This domain delivers all Vbrick Rev portal static content (HTML, JS, CSS, Font etc.).                                        |
| <https://northamerica.rev.vbrick.com>  | This domain is used for Microsoft Teams, Webex, and Zoom integrations.                                                       |
| <https://webexlive.rev.vbrick.com>     | This domain is used when using Webex Live Streaming feature.                                                                 |
| <https://rev-connect.us.vbrickrev.com> | This domain is used for Vbrick Peer-to-Peer (RevConnect) distribution.                                                       |
| <https://*.vci.vbrickrev.com>          | This domain is used for Video Conference Integration (VCI) i.e. Microsoft Teams, Webex, Zoom. Pexip etc. and RTMP streaming. |
| <https://grs.vbrickrev.com>            | This domain is used for Microsoft Teams, Webex and Zoom integrations and Vbrick Mobile App.                                  |

### DME Domain Access Details

| Used By DME                                                                                                     | Description                                                                                                       |
| :-------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------- |
| <https://media.us.vbrickrev.com>                                                                                | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 |
| <https://dme-update.us.vbrickrev.com>                                                                           | This domain is used to update DME from Vbrick Rev cloud.                                                          |
| <https://media-alt.us.vbrickrev.com>                                                                            | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 |
| <https://vbrick-prod01-dme-logs.s3.amazonaws.com> & <https://vbrick-prod01-dme-logs.s3.us-east-1.amazonaws.com> | This domain is used to send DME logs to Vbrick Rev cloud i.e. "Request Logs" feature.                             |
| <https://gs-streaming-prod01.s3.amazonaws.com> & <https://gs-streaming-prod01.s3.us-east-1.amazonaws.com>       | This domain is used by DME to push live streaming content to Vbrick Rev cloud for cloud delivery of that content. |

## EU Data Center

### Rev Browser URL / Domain Access Details

| Used By User (Browser)                 | Description                                                                                                                  |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <https://media.eu.vbrickrev.com>       | This domain delivers all VOD and Live Streaming content from Vbrick cloud CDN.                                               |
| <https://static.eu.vbrickrev.com>      | This domain delivers all Vbrick Rev portal static content (HTML, JS, CSS, Font etc.).                                        |
| <https://europe.eu.vbrickrev.com>      | This domain is used for Microsoft Teams, Webex, and Zoom integrations.                                                       |
| <https://webexlive.eu.vbrickrev.com>   | This domain is used when using Webex Live Streaming feature.                                                                 |
| <https://rev-connect.eu.vbrickrev.com> | This domain is used for Vbrick Peer-to-Peer (RevConnect) distribution.                                                       |
| <https://*.vci.vbrickrev.com>          | This domain is used for Video Conference Integration (VCI) i.e. Microsoft Teams, Webex, Zoom. Pexip etc. and RTMP streaming. |
| <https://grs.vbrickrev.com>            | This domain is used for Microsoft Teams, Webex and Zoom integrations and Vbrick Mobile App.                                  |

### DME Domain Access Details

| Used By DME                                                                                                        | Description                                                                                                       |
| :----------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------- |
| <https://media.eu.vbrickrev.com>                                                                                   | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 |
| <https://dme-update.eu.vbrickrev.com>                                                                              | This domain is used to update DME from Vbrick Rev cloud.                                                          |
| <https://media-alt.eu.vbrickrev.com>                                                                               | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 |
| <https://vbrick-prod02-dme-logs.s3.amazonaws.com> & <https://vbrick-prod02-dme-logs.s3.eu-central-1.amazonaws.com> | This domain is used to send DME logs to Vbrick Rev cloud i.e. "Request Logs" feature.                             |
| <https://gs-streaming-prod-02.s3.amazonaws.com> & <https://gs-streaming-prod-02.s3.eu-central-1.amazonaws.com>     | This domain is used by DME to push live streaming content to Vbrick Rev cloud for cloud delivery of that content. |

## AU Data Center

### Rev Browser URL / Domain Access Details

| Used By User (Browser)                 | Description                                                                                                                  |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <https://media.au.vbrickrev.com>       | This domain delivers all VOD and Live Streaming content from Vbrick cloud CDN.                                               |
| <https://static.au.vbrickrev.com>      | This domain delivers all Vbrick Rev portal static content (HTML, JS, CSS, Font etc.).                                        |
| <https://asiapacific.au.vbrickrev.com> | This domain is used for Microsoft Teams, Webex, and Zoom integrations.                                                       |
| <https://webexlive.au.vbrickrev.com>   | This domain is used when using Webex Live Streaming feature.                                                                 |
| <https://rev-connect.au.vbrickrev.com> | This domain is used for Vbrick Peer-to-Peer (RevConnect) distribution.                                                       |
| <https://*.vci.vbrickrev.com>          | This domain is used for Video Conference Integration (VCI) i.e. Microsoft Teams, Webex, Zoom. Pexip etc. and RTMP streaming. |
| <https://grs.vbrickrev.com>            | This domain is used for Microsoft Teams, Webex and Zoom integrations and Vbrick Mobile App.                                  |

### DME Domain Access Details

| Used By DME                                                                                                          | Description                                                                                                       |
| :------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------- |
| <https://media.au.vbrickrev.com>                                                                                     | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 |
| <https://dme-update.au.vbrickrev.com>                                                                                | This domain is used to update DME from Vbrick Rev cloud.                                                          |
| <https://media-alt.au.vbrickrev.com>                                                                                 | This domain delivers VOD and Live Streaming content from Vbrick cloud CDN to DME.                                 |
| <https://vbrick-prod03-dme-logs.s3.amazonaws.com> & <https://vbrick-prod03-dme-logs.s3.ap-southeast-2.amazonaws.com> | This domain is used to send DME logs to Vbrick Rev cloud i.e. "Request Logs" feature.                             |
| <https://gs-streaming-prod-03.s3.amazonaws.com> & <https://gs-streaming-prod-03.s3.ap-southeast-2.amazonaws.com>     | This domain is used by DME to push live streaming content to Vbrick Rev cloud for cloud delivery of that content. |

<br />

> 📘 Note
> 
> For DME [Live Subtitles](doc:video-sources#live-event-subtitles) and [RTMP(S) sourced webcasts](doc:video-sources#rtmprtmps-sourced-events), you may need to open outgoing TCP traffic on ports 1936, 1937 ,1938, and 1939.  The hostname for the cloud destination will be \*.vci.vbrickrev.com but please note this connection does not use HTTP or HTTPS so it will not work through a proxy.  
> 
> For [Rev Producer](doc:producer-event-set-up) and [Screen Share and Record](doc:screen-share-and-record), you may need to open additional outgoing TCP and UDP traffic on ports 27768 to 31768.