---
title: Vbrick Ramp SDK (Deprecated)
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
> ❗️ Warning!
> 
> **This SDK is deprecated!** Please begin migrating to the new [Vbrick Universal eCDN SDK](ref:vbrick-universal-ecdn-sdk).

## Integration With Vbrick Peer-to-Peer

Third parties video platforms can integrate with the **Vbrick Ramp SDK for Vbrick Peer-to-Peer** to provide eCDN functionality in their video players.  This guide provides the steps to integrate with Vbrick Ramp SDK which uses P2P for streaming live media at scale.

> 📘 Note
> 
> Below example uses **HLS.js player**

### Getting Started

This section describes how to get started with the SDK.

> 👍 Tip
> 
> Scripts can be loaded statically (as shown below) or dynamically by content management.

1. Load the **Vbrick Ramp SDK**. 

```javascript
<script type="application/javascript" src="https://static.us.vbrickrev.com/vbrick-ramp-sdk/rampapi.min.js"></script>
```

2. Load a compatible version of **HLS.js**. HLS.js _must_ be >= v1.0!

```javascript
<script type="application/javascript" src="https://cdn.jsdelivr.net/npm/hls.js@latest"></script>
```

3. Provide source **URL** and **metadata**.

```javascript
let Source_URL = '//host/path/to/original/source.m3u8';
let Source_Title = '<Source Title>';
let Source_Desc = '<Source Description>';
let Resource_ID = '<Resource Identifier>'; // Resource or Event ID
let User_ID = '<User Identifier>';
```

4. Provide **Vbrick Peer-to-Peer** configuration and credentials.
   1. A question mark `?` after the parameter name in the json below denotes that these are _optional_ fields. 
   2. The **jwtToken** can be generated in one of two methods:  a) generate the jwtToken on the backend or b) use a combination of **jwtKeyName**, **apiKey**, and **apiSecret** which is used by the SDK to generate the jwtToken for the user.

```javascript
let Rev_Connect_Config = {
  vendor: 'vbrick',
  magic: { // fields acquired from Vbrick appliance, may be stored as an object or Base-64-encoded JSON
    hostName: '<REV_HOSTNAME>',
    jwtKeyName?: '<REV_CONNECT_JWT_KEY_NAME>',
    apiKey?: '<API_Key>',
    apiSecret?: '<API_Secret>',
    jwtToken?: '<JWT_TOKEN>'
  },
  media: '<optional override URL to internal source for vbrick-rev-connect.js>' // 'std' to use built-in default
};
```

5. Complete the **Vbrick Ramp** configuration.

```javascript
let Vbrick_Ramp_Config = {
  verbose: true,
  allowFallback: true,
  fallbackUrl: Source_URL,
  allowExternStatic: false,
  analtyicsUrl: "",
  extern: Rev_Connect_Config,
  title: Source_Title,
  desc: Source_Desc,
  id: Resource_ID,
  userId: User_ID
};
```

6. Provide callback functions.

```javascript
Vbrick_Ramp_Config.i_onDone = function (rifc, obj) {
  // report on state of SDK
  // rifc: instance of RcvrInterface
  // obj: status object
};
Vbrick_Ramp_Config.i_onRcvrReady = function (rifc, src, fmt) {
  // rifc: instance of RcvrInterface
  // src: source as determined by SDK
  // fmt: may contain the source format, usually undefined
  // provide src to player here
};
```

7. Instantiate **RcvrInterface**: this begins the detection and loading sequence.

```javascript
let RIFC = new RcvrInterface(Vbrick_Ramp_Config);
```

When the sequence is complete, the **onRcvrReady** callback is called with the determined **source URL** which can then be passed to the player.  Subsequently, the **onDone** callback is called to report the status of the SDK.

## SDK Configuration Example

```javascript
let Original_Source_URL = '//hostname/path/to/original/source.m3u8'
let Vbrick_Ramp_Config = {
  verbose: true,
  analyticsUrl: "",
  allowExternStatic: false,
  allowFallback: true,
  fallbackUrl: Source_URL,
  title: Source_Title,
  desc: Source_Desc,
  id: Resource_ID,
  userId: User_ID,
  extern: {
    vendor: 'vbrick',
    media: 'std',
    magic: { // values from Rev configuration
      hostName: '<REV_HOSTNAME>',
      jwtKeyName: '<REV_CONNECT_JWT_KEY_NAME>,
      apiKey: '<REV_API_KEY>',
      apiSecret" : '<BASE64(REV_API_SECRET)>'
    }
    //NOTE: 'magic' may also be supplied here as Base64-encoded JSON
  }
};
```