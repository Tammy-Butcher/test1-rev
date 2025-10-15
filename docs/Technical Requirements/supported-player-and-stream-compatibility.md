---
title: Player and Stream Compatibility
excerpt: >-
  The supported stream types the Rev portal plays in current compatible
  browsers.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
| Stream Type              | Edge Chromium | Chrome | Firefox | Safari | iOS   | Android |
| :----------------------- | :------------ | :----- | :------ | :----- | :---- | :------ |
| Vbrick Multicast ¹       | HTML5         | HTML5  | HTML5   | HTML5  |       |         |
| Vbrick Peer-to-Peer ²    | HTML5         | HTML5  | HTML5   | HTML5³ |       |         |
| HLS                      | HTML5         | HTML5  | HTML5   | HTML5  | HTML5 | HTML5   |
| MP4 Progressive Download | HTML5         | HTML5  | HTML5   | HTML5  | HTML5 | HTML5   |

<sup>1 : Vbrick Multicast playback requires the installation of the Vbrick Multicast (VBM) Agent for Windows or Mac to be installed from the Support Download Portal.</sup>

<sup>2, 3 : Vbrick Peer-to-Peer can only be utilized from within Rev using the Vbrick Rev HTML5 player or via the SDK with Vbrick Universal eCDN. While it is supported on Mac Safari, it is NOT supported on iOS Safari.</sup>

> 📘 Note
> 
> Vbrick currently does _not_ support **video-only** or **audio-only** _Live_ streams.
> 
> Audio-only _VOD_ streams _are_ currently supported.
> 
> Note that Vbrick Encoders can be set up to add silent audio if the source does not have audio.

> 👍 Tip
> 
> **Vbrick** in the table above refers to browser plug-ins that are used to play the stream type. To use these plug-ins, users may need to grant permission for them to run in the browser.