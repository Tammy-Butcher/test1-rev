---
title: Vbrick Universal eCDN SDK Integration Steps
description: >-
  This recipe provides step-by-step instructions on how to integrate the SDK
  into your player page.
hidden: false
recipe:
  color: '#ffffff'
  icon: ▶️
---
```javascript JavaScript
<script type="application/javascript" src="https://static.us.vbrickrev.com/vbrick-ecdn-sdk/v2/vbrick-ecdn.min.js"></script>
<script type="application/javascript" src="//cdn.jsdelivr.net/npm/hls.js@latest"></script>
Player_Config = {...};
Player_Instance = new Hls(Player_Config);
<link rel="stylesheet" href="//unpkg.com/video.js/dist/video-js.min.css" />
<script type="application/javascript" src="//unpkg.com/video.js/dist/video.min.js"></script>
Player_Config = {...};
Player_Instance = videojs(Video_Element, Player_Config, On_Ready_Fn);
let Source_URL = 'https://host/path/to/originalvideo/source.m3u8';
let Source_Title = '<Source Title>';
let Source_Desc = '<Source Description>';
let Resource_ID = '<Resource Identifier>';
let User_ID = '<User Identifier>';
let Vbrick_Rev_Config = {
    hostName: '<Vbrick Rev host name>',
    jwtKeyName: '<Vbrick Rev JWT Key Name generated in Vbrick Rev Management>',
    apiKey: '<API Key generated in Vbrick Rev Management>',
    apiSecret: '<API Secret generated in Vbrick Rev Management>'
};
let Vbrick_eCDN_Config = {
  verbose: true,
  sourceUrl: Source_URL,
  eventTitle: Source_Title,
  eventDesc: Source_Desc,
  eventId: Resource_ID,
  userId: User_ID,
  rev: Vbrick_Rev_Config
};
Vbrick_eCDN_Config.i_onDone = function (rifc, obj) {
  // report on state of SDK
  // rifc: instance of RcvrInterface
  // obj: status object
  rifc.verbose && rifc.logger('Vbrick RcvrInterface DONE', rifc.interpretState(obj));
};
Vbrick_eCDN_Config.i_onRcvrReady = function (rifc, src, fmt) {
  // rifc: instance of RcvrInterface
  // src: source as determined by SDK. this will be empty when there is an error
  // fmt: may contain the source format, usually undefined
  // -- provide src to player here --
  // - hls.js: rifc.player.loadSource(src);
  // - video.js: rifc.player.src(src);
};
Vbrick_eCDN_Config.player = <player instance e.g. player = new Hls(...)>; // required
Vbrick_eCDN_Config.playerRootName = 'Hls'; // optional if supported player can be detected in global scope,
Vbrick_eCDN_Config.playerRoot = window.Hls; // required if supported player factory is an exported module reference...
let RIFC = new RcvrInterface(Vbrick_eCDN_Config);
```

# Load the Vbrick Universal eCDN SDK.

<!-- javascript@1 -->

The script can be loaded statically or dynamically via JavaScript after page load.

# Load a compatible version of HLS.js.

<!-- javascript@2-4 -->

The Vbrick Universal eCDN SDK supports HLS.js v1+ and Video.js v7+ video players. 

Note that HLS.js >= v1.0.

Create a player instance, but do not provide a source yet.

# Load a compatible version of Video.js.

<!-- javascript@5-8 -->

The Vbrick Universal eCDN SDK supports HLS.js v1+ and Video.js v7+ video players. 

Note that Video.js >= v7+.

Create a player instance, but do not provide a source yet.

View the [Parameter Reference](ref:vbrick-universal-ecdn-sdk#appendix-a-parameter-reference-for-vbrick-universal-ecdn-sdk) when using the Vbrick Video.js Plugin.

# Provide video source URL and metadata.

<!-- javascript@9-13 -->

The Resource_ID is normally the resource or Event/Webcast ID

# Provide Vbrick configuration credentials.

<!-- javascript@14-19 -->

The most common method is to provide a Vbrick Rev host name, API Key, API Secret, and JWT Key Name. 

These fields are acquired from the Rev portal and may be stored as an object or Base-64-encoded JSON.

Refer to the [Parameter Reference](ref:vbrick-universal-ecdn-sdk#appendix-a-parameter-reference-for-vbrick-universal-ecdn-sdk) for details.

# Complete Vbrick eCDN Configuration.

<!-- javascript@20-28 -->

Refer to the [Parameter Reference](ref:vbrick-universal-ecdn-sdk#appendix-a-parameter-reference-for-vbrick-universal-ecdn-sdk) for details.

# Provide callback functions.

<!-- javascript@29-42 -->



# Provide links to the player.

<!-- javascript@43-45 -->



# Instantiate RcvrInterface.

<!-- javascript@46 -->

This begins the detection and loading sequence.

# Sequence Complete

<!-- javascript@1-46 -->

When the sequence is complete, the **onRcvrReady** callback will be called with the determined **source URL** which can then be passed to the player. 

Subsequently, the **onDone** callback will be called to report the status of the SDK.