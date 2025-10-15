---
title: Vbrick Universal eCDN SDK
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
## Overview

This guide outlines the essential steps for integrating third-party Video Content Management software and Video Players with the Vbrick Universal eCDN SDK. The SDK incorporates Vbrick's advanced Peer-to-Peer and Unicast caching capabilities and enables seamless video streaming and distribution at scale. By following these high-level instructions, you can integrate your player to optimize the video delivery infrastructure and provide a more efficient and enhanced experience for viewers.

## Prerequisites

The **Vbrick Universal eCDN SDK** is available to both **Vbrick EVP** customers and **Vbrick Universal eCDN** customers.  All customers use a provided tenant / cloud-based Vbrick Management Interface to configure the use of this SDK.  The **Vbrick Management Interface** is also commonly referred to **Vbrick Rev**.

> 📘 Note
>
> The initial configuration is slightly different for **Vbrick EVP** customers versus **Vbrick Universal eCDN** customers.
>
> * If you are a **Vbrick EVP Customer** or **Partner**, follow [Enable JWT Authentication](doc:enable-jwt-authentication) to setup JWT in the Vbrick Management Interface. 
> * If you are **Vbrick Universal eCDN Customer** or **Partner**, follow [How To Set Up the Vbrick Universal eCDN](doc:how-to-set-up-the-vbrick-universal-ecdn) to setup and configure your Vbrick Universal eCDN account in Vbrick Management Interface.

You will need the following information from the **Vbrick Management Interface** to continue with the SDK integration:

* **hostName**: Vbrick Rev hostname/URL (management interface tenant URL. Ex. acme.vbrickrev.com )
* **jwtKeyName**: Default is RevConnectDefault (which can be verified within the management interface)
* **apiKey**
* **apiSecret**

## Integration Steps

This section provides step-by-step instructions on how to integrate the SDK into your player page.

1. Load the **Vbrick Universal eCDN SDK**.  The script can be loaded statically (example shown here) or dynamically via **JavaScript** after page load.

```javascript JavaScript
<script type="application/javascript" src="https://static.us.vbrickrev.com/vbrick-ecdn-sdk/v2/vbrick-ecdn.min.js"></script>
```

2. The Vbrick Universal eCDN SDK supports **HLS.js v1+** and **Video.js v7+** video players.

> **HLS.js**
>
> For example, load a compatible version of HLS.js. (HLS.js >= v1.0).

```javascript JavaScript
<script type="application/javascript" src="//cdn.jsdelivr.net/npm/hls.js@latest"></script>
```

```javascript JavaScript
// create a player instance but do not provide a source, yet
Player_Config = {...};
Player_Instance = new Hls(Player_Config);
```

> **Video.js**
>
> For example, load a compatible version of Video.js (v7+).

```javascript
<link rel="stylesheet" href="//unpkg.com/video.js/dist/video-js.min.css" />
<script type="application/javascript" src="//unpkg.com/video.js/dist/video.min.js"></script>
```

```javascript
// create a player instance but do not provide a source, yet
Player_Config = {...}; // see Appendix V for information about overriding native HLS playback!
Player_Instance = videojs(Video_Element, Player_Config, On_Ready_Fn);
```

View the [Parameter Reference](ref:vbrick-universal-sdk#appendix-a-parameter-reference-for-vbrick-ecdn-sdk) when using the Vbrick Video.js Plugin.

3. Provide **video source URL** and **metadata**.

```javascript
let Source_URL = 'https://host/path/to/originalvideo/source.m3u8';
let Source_Title = '<Source Title>';
let Source_Desc = '<Source Description>';
let Resource_ID = '<Resource Identifier>'; // Resource or Event/Webcast ID
let User_ID = '<User Identifier>';
```

4. Provide Vbrick configuration/credentials. The most common method is to provide a Vbrick Rev **host name**, **API Key**, **API Secret**, and **JWT Key Name**. Refer to the [Parameter Reference](ref:vbrick-universal-sdk#appendix-a-parameter-reference-for-vbrick-ecdn-sdk) for details.

```javascript
let Vbrick_Rev_Config = { // these fields are acquired from Vbrick Rev management UI, may be stored as an object or Base-64-encoded JSON
    hostName: '<Vbrick Rev host name>',
    jwtKeyName: '<Vbrick Rev JWT Key Name generated in Vbrick Rev Management>',
    apiKey: '<API Key generated in Vbrick Rev Management>',
    apiSecret: '<API Secret generated in Vbrick Rev Management>'
};
```

5. Complete Vbrick eCDN Configuration. Refer to the [Parameter Reference](ref:vbrick-universal-sdk#appendix-a-parameter-reference-for-vbrick-ecdn-sdk) for details.

```javascript
let Vbrick_eCDN_Config = {
  verbose: true,
  sourceUrl: Source_URL,
  eventTitle: Source_Title,
  eventDesc: Source_Desc,
  eventId: Resource_ID,
  userId: User_ID,
  rev: Vbrick_Rev_Config
};
```

6. Provide **callback functions**.

```javascript
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
```

7. Provide **links** to the player.

```javascript
Vbrick_eCDN_Config.player = <player instance e.g. player = new Hls(...)>; // required
Vbrick_eCDN_Config.playerRootName = 'Hls'; // optional if supported player can be detected in global scope,
Vbrick_eCDN_Config.playerRoot = window.Hls; // required if supported player factory is an exported module reference...
```

8. Instantiate **RcvrInterface**: this begins the detection and loading sequence.

```javascript
let RIFC = new RcvrInterface(Vbrick_eCDN_Config);
```

9. When the sequence is complete, the **onRcvrReady** callback will be called with the determined source URL which can then be passed to the player.  Subsequently, the **onDone callback** will be called to report the status of the SDK.

## Completed Configuration Example

Once you configure all of the items above, your configuration will look something like the example below.

```javascript
let Source_URL = 'https://acme.com/hls/source.m3u8';
let Source_Title = 'CEO Townhall';
let Source_Desc = 'This is a CEO townhall';
let Resource_ID = '9ca43124-0ccb-4d1e-9a94-9bccf85b9df8'; // Video or Event ID
let User_ID = 'jdoe@acme.com';
let Vbrick_eCDN_Config = {
  verbose: true,
  sourceUrl: Source_URL,
  eventTitle: Source_Title,
  eventDesc: Source_Desc,
  eventId: Resource_ID,
  userId: User_ID,
  player: Player_Instance,
  playerRootName: 'Hls',
  rev: {
      hostName: 'acme.vbrickrev.com',
      jwtKeyName: 'RevConnectDefault,
      apiKey: 'XXXX',
      apiSecret : 'YYYY'
  },
  i_onRcvrReady: function(rifc, src, fmt) {...},
  i_onDone: function(rifc, obj) {...}
};
```

## Appendix A: Parameter Reference for Vbrick Universal eCDN SDK

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Parameter
      </th>

      <th>
        Default
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        sourceUrl
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string indicates the original video source URL.
      </td>
    </tr>

    <tr>
      <td>
        eventId
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string GUID provides a unique identifier for this event/webcast.  

        * \*Best Practice\*\*: The integration should supply a unique identifier for this specific event.
      </td>
    </tr>

    <tr>
      <td>
        eventTitle
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string provides the title of the supplied video source URL.  

        * \*Best Practice\*\*: The integration should supply an appropriate title associated with this specific event.
      </td>
    </tr>

    <tr>
      <td>
        eventDesc
      </td>

      <td>
        empty
      </td>

      <td>
        This optional string provides a brief description for this event.
      </td>
    </tr>

    <tr>
      <td>
        userId
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string provides a unique identifier for the current user.  

        * \*Best Practice\*\*: The integration should supply a unique identifier for this specific user for example email address of the user so that user level analytics can be captured.
      </td>
    </tr>

    <tr>
      <td>
        verbose
      </td>

      <td>
        false
      </td>

      <td>
        When set to true, turns on additional logging in the console.\
        When set to a function, logging is sent to that function instead of the console.
      </td>
    </tr>

    <tr>
      <td>
        debug
      </td>

      <td>
        false
      </td>

      <td>
        When set to true, may turn on more informative messaging in the console as well as enabling some debug features.
      </td>
    </tr>

    <tr>
      <td>
        enableBuffering
      </td>

      <td>
        true
      </td>

      <td>
        When true and used with debug, above, enables an overlay widget that shows buffering and playback statistics.
      </td>
    </tr>

    <tr>
      <td>
        player
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** object reference points to the targeted instance object of the player.
      </td>
    </tr>

    <tr>
      <td>
        playerRoot
      </td>

      <td>
        empty
      </td>

      <td>
        This object reference points to the player factory object.  

        * \*Best Practice\*\*: The integration must supply this reference if the player factory is encapsulated in a module or is otherwise not accessible through its common global scope name.
      </td>
    </tr>

    <tr>
      <td>
        rev
      </td>

      <td>
        empty
      </td>

      <td>
        This object supplies configuration parameters for engaging with Vbrick Rev.
      </td>
    </tr>

    <tr>
      <td>
        rev.hostName
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string provides Vbrick Rev cloud host name.
      </td>
    </tr>

    <tr>
      <td>
        rev.apiKey
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string provides the API Key from Vbrick Rev. This is **optional** if you are generating your JWT in which case you should use the **rev.jwtToken** parameter below instead.
      </td>
    </tr>

    <tr>
      <td>
        rev.apiSecret
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string provides the API Secret associated with the API Key from Vbrick Rev. This is **optional** if you are generating your JWT in which case you should use the **rev.jwtToken** parameter below instead.
      </td>
    </tr>

    <tr>
      <td>
        rev.jwtKeyName
      </td>

      <td>
        empty
      </td>

      <td>
        This **required** string provides the JWT Key Name from Vbrick Rev to use when using Rev to generate a JWT for authentication. This is **optional** if you are generating your JWT in which case you should use **rev.jwtToken** parameter below instead.
      </td>
    </tr>

    <tr>
      <td>
        rev.jwtToken
      </td>

      <td>
        empty
      </td>

      <td>
        This **optional** string is a customer generated JWT. Use this *only* if you are generating your own JWT.  

        * \*Not&#x65;**: View the topic on[JWT Authentication](ref:jwt-authentication) for generating your own JWT. If supplying this then *do not* supply **apiKe&#x79;**,**apiSecre&#x74;**, and**jwtKeyName\*\*.
      </td>
    </tr>
  </tbody>
</Table>

## Appendix B: Using the Vbrick Video Video.js Plugin

If you are using **Video.js plugin** instead of directly integrating with **Video.js player**, you need to follow the below steps.

1. Load **Video.js player source**.
   1. Load player into page before loading plugin into page.
   2. For example, load a compatible version of **Video.js (v7+)**.

```html
<link rel="stylesheet" href="//unpkg.com/video.js/dist/video-js.min.css" />
<script type="application/javascript" src="//unpkg.com/video.js/dist/video.min.js"></script>
```

2. Load **Video.js plugin source**.

```html
<script type="application/javascript" src="https://static.us.vbrickrev.com/vbrick-ecdn-sdk/v2/vbrick-ecdn-plugin-videojs.min.js"></script>
```

3. Provide Vbrick configuration/credentials. View the steps on providing [Vbrick configuration/credentials](ref:vbrick-universal-sdk#integration-steps) above in the integration steps section.

> ❗️ Caution!
>
> * Do *not* set **sourceUrl**, it is passed to the player directly (see below). 
> * Do *not* set the **source** on the player in **onRcvrReady**.
> * Do *not* set the **player** but do set the **playerRoot** if it is not the common global.

```javascript
let Vbrick_eCDN_Config = {
  verbose: true,
  //sourceUrl: Source_URL, // not needed in plugin
  eventTitle: Source_Title,
  eventDesc: Source_Desc,
  eventId: Resource_ID,
  userId: User_ID,
  //player: Player_Instance, // not needed in plugin
  //playerRootName: 'videojs', // not needed in plugin
  rev: {
      hostName: 'hostname.of.local.Rev',
      jwtKeyName: 'keyNameFromRev,
      apiKey: 'apiKeyFromRev',
      apiSecret : 'apiSecretFromRev'
  },
  //i_onRcvrReady: function(rifc, src, fmt) {...}, // not needed in plugin
  i_onDone: function(rifc, obj) {...}
};
```

4. Set up the **player** configuration.

```javascript
let nativeOverride = true; // do not play HLS natively in browsers that support it, like Safari
let Player Config = {
  controls:true,
  autoplay:'muted',
  html5:{
    vhs: { overrideNative: nativeOverride },
    nativeAudioTracks: !nativeOverride,
    nativeVideoTracks: !nativeOverride,
    nativeTextTracks: !nativeOverride
  },
  plugins: {
    vbrickecdn: {
      overlay: true, // optional status overlay
      verbose: true, // optional console logging
      params: Vbrick_eCDN_Config
  }
};
```

5. Instantiate the player.

```javascript
let Player_Instance = videojs(Video_Element, Player_Config, function () {
  this.src(Vbrick_eCDN_Config.fallbackUrl || Source_URL);  // setting the source on the player starts the SDK processing
  this.play(); // 'this' is player instance
});
```

6. The video source is applied to the player internally.
