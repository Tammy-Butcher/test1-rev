---
title: WebRTC and Vbrick Peer-to-Peer Compatibility
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
Several components of Vbrick Rev utilize WebRTC technologies including [Webcam and Screenshare](doc:host-a-self-produced-webcast), [Producer](doc:produce-an-event), and [Vbrick Peer-to-Peer Zones](doc:rev-connect-zones).  WebRTC was selected because of its adoption of strict security models while affording browser-to-browser communications and secure access to webcams and screen shares.  WebRTC is a well-adopted set of technologies – used by Google Hangoust/Meet/Duo, Facebook Messenger, GoTo Meeting, Discord, and Snapchat among others.

This topic discusses **WebRTC** and **Vbrick Peer-to-Peer** compatibility.  Each browser has an implementation of WebRTC and provides browser-specific settings.  These settings  allow IT teams (or less commonly browser users) to customize their level of security based on their specific security posture.  These settings can also affect the efficiency of Vbrick Peer-to-Peer.

> 🚧 Important!
>
> In most cases, if default settings are adopted then Vbrick Peer-to-Peer works correctly, and there is no action necessary.  Please test your Vbrick Peer-to-Peer zones, utilizing samples from each of the IP set(s) defined within the zone, to verify the feature.  It is only when there are difficulties utilizing Vbrick Peer-to-Peer that you may need to further investigate.  These settings do not impact our Webcam and Screenshare features.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Browser
      </th>

      <th>
        WebRTC Implementation/Settings
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Edge
      </td>

      <td>
        Edge behavior for WebRTC connectivity is affected by the system/registry values of the Policy Settings  **WebRtcLocalhostIpHandling** and **WebRtcLocalIpsAllowedUrls**.  Please review Microsoft documentation on [Policy Settings](https://docs.microsoft.com/en-us/deployedge/microsoft-edge-policies).  

        If **WebRtcLocalhostIpHandling** is set default/not set/set to *default public and private* interfaces, and **WebRtcLocalIpsAllowedUrls** is default or matches your Rev domain (e.g., ‘mycompany.vbrick.com’) then Vbrick Peer-to-Peer can connect to each other and will work appropriately.  The IPs may be anonymized depending on the settings.  

        If **WebRtcLocalhostIpHandling** is set to *default public interface only*, then Vbrick Peer-to-Peer cannot function.  

        Note that Microsoft's documentation regarding the "default" setting for **WebRtcLocalhostIpHandling** is not accurate – the local IP address is not exposed in this case unless there is a **WebRtcLocalIpsAllowedUrls** entry that matches the domain that the browser has loaded.
      </td>
    </tr>

    <tr>
      <td>
        Chrome
      </td>

      <td>
        Chrome works exactly the same way as Edge, except that the policy setting **WebRtcLocalhostIpHandling** is named **WebRtcIPHandling** instead.
      </td>
    </tr>

    <tr>
      <td>
        Safari
      </td>

      <td>
        The setting of relevance is located under **Develop** > **WebRTC** > **Disable ICE Candidate Restrictions**.  

        However, Vbrick Peer-to-Peer will work if this setting is selected or not – it only controls if the IP is anonymized.
      </td>
    </tr>

    <tr>
      <td>
        Firefox
      </td>

      <td>
        The Firefox [WebRTC wiki page](https://wiki.mozilla.org/Media/WebRTC/Privacy) maintains a comparison of their WebRTC settings.  

        Vbrick Peer-to-Peer requires local candidates – so any preference that does not support local candidates would block Vbrick Peer-to-Peer.  

        Further, anonymization of the IP address in Firefox is controlled by media.peerconnection.ice.obfuscate\_host\_addresses.  

        For additional control, Firefox does provide a blocklist media.peerconnection.ice.obfuscate\_host\_addresses.blocklist on their Wiki.
      </td>
    </tr>
  </tbody>
</Table>

For more information:

* [WebRTC.org](https://webrtc.org/) for general WebRTC information and access to their detailed guides
* Visit browser help (for specific browsers) for support and details as needed

> 📘 Note
>
> Regardless of browser you use, if the Vbrick Peer-to-Peer viewers are spanning sub-nets you may wish to enabled the **Use ULS in Peer Meshing** in the [Vbrick Peer-to-Peer Zones](doc:rev-connect-zones). 
>
> Remember to test your Vbrick Peer-to-Peer deployment, and test each IP range defined within your Vbrick Peer-to-Peer enabled Zones.
