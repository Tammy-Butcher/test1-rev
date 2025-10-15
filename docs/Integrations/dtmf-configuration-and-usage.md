---
title: DTMF Configuration and Usage
excerpt: >-
  Rev can utilize dual tone multi-frequency codes with certain integrations. 
  Learn what that is and how to use it in your meetings.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

Rev provides the ability to inject **Dual Tone Multi-Frequency (DTMF)** codes into (DTMF capable) Video Conference events. DTMF codes are numerical codes (a legacy from phone systems) used for things like providing a numeric passcode to online meetings or guiding you through a menu system to direct you where to go.  These codes can be used at the beginning of an event or recording.  Multiple codes may be used depending on customer requirements.

It is recommended that you review the specific DTMF codes associated with each Video Conference system you utilize -- each system has unique codes.  Rev does not qualify the codes but injects them via the Rev VCI connection to effect changes to the VC streams captured for distribution and recording.

Currently, the following integrations with Rev are DTMF supported:

* [Pexip](doc:pexip) 
* [Video Conference, RTMP, and Other Sourced Streams](doc:video-conference-vc-integrations) 
* [Zoom](doc:zoom-integration) 
* Webex Calls (through [VC integration](doc:video-conference-vc-integrations))

The process to using DTMF injections in events and recordings is:

1. Configure the characters and codes you want to use in your specific integration.
2. Add and enable the codes in your events as needed -- either to happen at the beginning of the event or with timing controlled by a Host during an event.
3. Add and enable the codes in your recordings as needed.

## DTMF Integration Configuration

On the **Media Settings** > **Integrations** page within Rev, each of the DTMF capable integrations has two additional \[optional] fields:  **Default Initial DTMF Codes** and **DTMF Codes To Reject**. For example, Zoom's section is displayed below.

* **Default Initial DTMF Codes** - Defines a series of codes (separated by a space, e.g., #11 #114) that will be injected at the beginning of an event or recording for the integration source.  During Event Setup, these codes will be prefilled into the event and/or recording, but they may also be modified or removed during at that time.  

* **DTMF Codes To Reject** - Defines a collection of codes that cannot be used (by the Host) during the event. This rejection list is not applied to the initial DTMF codes. As with the default codes, multiple codes may be entered if separated by a space.

<Image title="codeConfig.png" alt={1138} align="center" src="https://files.readme.io/740627a-codeConfig.png">
  Zoom's sample DTMF configuration
</Image>

As mentioned above, each integration has its own [DTMF characters and codes](doc:dtmf-configuration-and-usage#integration-code-documentation) that can be used. A **DTMF Code** is just a string of DTMF characters.

| DTMF Characters |
| :-------------- |
| `0-9`           |
| `*`             |
| `#`             |
| `A-D`           |

## Integration Code Documentation

Each integration has documentation for DTMF codes that may be used currently.  Please keep current with codes associated with your VC system.  The links below are just starting points, and not intended as complete descriptions of the available codes. 

| Integration | Documentation                                                                                                        |
| :---------- | :------------------------------------------------------------------------------------------------------------------- |
| Pexip       | [Pexip DTMF Keypad Controls](https://docs.pexip.com/admin/dtmf_controls.htm)                                         |
| Zoom        | [Zoom Controls](https://support.zoom.us/hc/en-us/articles/202405539-H-323-SIP-Room-Connector-Dial-Strings)           |
| Webex       | [Webex Layout Controls](https://help.webex.com/en-us/article/zp1dhab/Webex-Rooms-%7C-Video-Stream-Layouts#id_135883) |

### Use DTMF Codes in Events

You can customize DTMF codes for use in events to set up pins and passwords and change the layout of the webcast.  Changing the layout will not change other meeting attendees' layout, but it will change the layout and how it appears to attendees.

Also, if you do not want any DTMF injection to happen by the Host during an event, we recommend **Display DTMF Controls** be **Disabled**.  This will hide it from the Host UI. 

<Image title="dtmfEventSetup.png" alt={1157} align="center" src="https://files.readme.io/4f35d18-dtmfEventSetup.png">
  An example of using DTMF codes with a Zoom event in Rev
</Image>

### Use DTMF Codes in Video Recording

Similar to events, once DTMF codes are configured in your integration of choice, you can also use them in VOD recordings and meetings for the integration.  The upload icon allows for **Live Recording**.  DTMF code injection is also added to Recordings for DTMF-capable sources at the beginning of the event (but not during the event).  Again, you are provided with PIN and initial DTMF codes.

* **Initial DTMF Codes** - These are the codes you [configured for the integration](doc:dtmf-configuration-and-usage#configuration) you are using and that are injected once Rev connects to the VCI call.  Once again, you must separate multiple codes with a space.

<Image alt="DTMF codes are injected once Rev connects to the VCI call" src="https://files.readme.io/8656d0f-dtmfCodes.png">
  DTMF codes are injected once Rev connects to the VCI call
</Image>
