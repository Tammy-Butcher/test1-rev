---
title: Local Network Access Best Practices
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
## Local Network Access in Chrome

**Chrome 142** has included additional security restrictions regarding **Local Network Access**.  This controls the ability of websites to send requests to servers on a user's local network or loopback. 

For example, in **IPv4**, this impacts `10.0.0.0/8`, `172.16.0.0/12`, and `192.168.0.0/16` address spaces, and for loopback `127.0.0.0/8`and`169.254.0.0/16`.  View [Local Area Network Access](https://wicg.github.io/local-network-access/#non-public-ip-address-blocks) for a complete list, which includes **IPv6**.   Enterprises utilizing these spaces will be directly impacted -- for both Vbrick and other services they may use.

View: [LNA Adoption Guide for Chrome](https://docs.google.com/document/d/1QQkqehw8umtAgz5z0um7THx-aoU251p705FbIQjDuGs/edit?tab=t.0#heading=h.v8oobsqxbxxy)

With these restrictions enabled, Chrome will prompt users to **Allow** or **Deny** connections to local network devices. Connecting to local services (Allow) is *essential* for Vbrick and viewers using our player and/or **Universal eCDN** technologies. Currently, zoning and distribution via **Multicast Agent**, **DMEs**, and **Peer-to-Peer** connections all *require* local access.

View: [Permission Prompts for LNA | Developer Guide](https://developer.chrome.com/blog/local-network-access)

If Enterprises take *no* action, Chrome will prompt users to allow access to local services. If allowed, playback will occur as normal. If denied, then playback may be impacted.

To avoid this confusion and forced user interaction, **Chrome Enterprise** has provided a policy to specify an allowlist for local services. This means that **LocalNetworkAccessAllowedForUrls** can be used to suppress the popup for a list of local URLs.

View: [Chrome Enterprise Policy List & Management | Documentation](https://chromeenterprise.google/policies/#LocalNetworkAccessAllowedForUrls)

Vbrick *highly* recommends using this Chrome Enterprise policy to allowlist your **DMEs** (including DMEs that support User Location Services), `localstreaming.vbrick.com` (or customized **Vbrick Multicast** streaming URL), and IP sets utilizing **Peer-to-Peer** or Presenters within a **Producer** event. (While these restrictions do not currently curtail WebRTC connections, it is in the future planning.)

## Local Network Access in Edge

Edge, like Chrome, also supports **Local Network Access** features.

The **Edge Browser Network Policy** settings provides several settings that control these features:

* [LocalNetworkAccessAllowedForUrls](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-browser-policies/localnetworkaccessallowedforurls). Allows sites to make local network and loopback requests.
* [LocalNetworkAccessBlockedForUrls](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-browser-policies/localnetworkaccessblockedforurls).  Blocks sites from making network or loopback requests
* [LocalNetworkAccessRestrictionsEnabled](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-browser-policies/localnetworkaccessrestrictionsenabled).  Overrides to block all network or loopback requests.

Vbrick *highly* recommends setting **LocalNetworkAccessAllowedForUrls**  to allowlist your **DMEs** (including DMEs that support User Location Services), `localstreaming.vbrick.com` (or customized **Vbrick Multicast** streaming URL), and IP sets utilizing **Peer-to-Peer** or Presenters within a **Producer** event. (While these restrictions do not currently curtail WebRTC connections, it is in the future planning.)
