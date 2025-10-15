---
title: Browser, OS, and Device Compatibility
excerpt: >-
  This table details supported browsers, operating systems, and device
  compatibility in the Rev portal
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "left" }}>
        Device
      </th>

      <th style={{ textAlign: "left" }}>
        OS
      </th>

      <th style={{ textAlign: "left" }}>
        Browser
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "left" }}>
        PC
      </td>

      <td style={{ textAlign: "left" }}>
        Windows 11\
        Windows 10 Enterprise\
        Windows 10 Pro
      </td>

      <td style={{ textAlign: "left" }}>
        Firefox 143+\
        Chrome 141+¹\
        Edge 141+¹
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Mac
      </td>

      <td style={{ textAlign: "left" }}>
        macOS 26.0 Tahoe\
        macOS 15.6: Sequoia
      </td>

      <td style={{ textAlign: "left" }}>
        Safari 26.1+\
        Firefox 143+\
        Chrome 141+²\
        Edge 140+
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        iPhone, iPad
      </td>

      <td style={{ textAlign: "left" }}>
        iOS 18.6+
      </td>

      <td style={{ textAlign: "left" }}>
        Native Browser
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Android
      </td>

      <td style={{ textAlign: "left" }}>
        Android 13.0+
      </td>

      <td style={{ textAlign: "left" }}>
        Chrome Only
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Chromebook
      </td>

      <td style={{ textAlign: "left" }}>
        Chrome OS
      </td>

      <td style={{ textAlign: "left" }}>
        Chrome Only
      </td>
    </tr>
  </tbody>
</Table>

<sup>1: Rev supports CHIPS/cookieless login in Google Chrome and Microsoft Edge as of v7.58. This means that Rev will continue to work seamlessly when embedded in other applications, without any login interruptions.</sup>

<sup>2 : The Mac Chrome browser video decoder displays some instabilities when playing HLS streams with identified data loss. This is a rare occurring issue that manifests as a “stall” or stopping of the playback. Disabling Chrome Hardware Acceleration fixes the issue. Disable this from Chrome by visiting the URL “chrome://settings”, then navigating to Advanced > System > “Use hardware acceleration when available” and toggling as necessary. This issue only effects Mac Chrome users and does not affect Windows users.</sup>

> 🚧 Important!
>
> Beginning with **Chrome 142**, there are additional security restrictions regarding **Local Network Access**.  This controls the ability of websites to send requests to servers on a user's local network or loopback and will prompt users to allow or deny connections when these restrictions are enabled.
>
> To avoid disruptions, view our topic on [Local Network Access Best Practices](doc:local-network-access-best-practices) for both Chrome and Edge.
