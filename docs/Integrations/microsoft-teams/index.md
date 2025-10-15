---
title: Microsoft Teams
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

There are three different integration types available for **Microsoft Teams** in Rev.  Each type features different Teams' functions available once they are enabled and configured in Rev. For example, you can choose to make Rev portal content visible in a Microsoft Teams **Channel** tab and you can also use Microsoft Teams video conferencing as a **video source** in Rev Webcasts.  Microsoft also supports 3rd-party eCDN distribution with **MS Teams Townhall Premium** which means you can configure Vbrick Rev and/or Vbrick Universal eCDN for distribution.

## Microsoft Teams Integration

With the [Microsoft Teams Integration](doc:view-rev-content-in-a-microsoft-teams-tab), you can display Rev information within the Teams APP.  It must be enabled and downloaded.  Further, the download package must be integrated into Teams.

The Rev content in your MS Teams environment) includes:

* Rev Event Calendar
* Rev (VOD) videos
* Rev Categories

This is enabled and downloaded from the Integrations page using the following setting:

<Image alt="Enable the Microsoft Teams Integration to view Rev Content in your MS Teams environment" align="center" src="https://files.readme.io/b751c41-msTeams.png">
  Enable the Microsoft Teams Integration to view Rev Content in your MS Teams environment
</Image>

## Microsoft Teams Video Conferencing

Integrating into [Microsoft Teams Video Conferencing](doc:record-and-stream-microsoft-teams-meetings) provides the ability for Rev to attach to a Teams conference.  Once attached, Rev can stream and record the conference.  

This is enabled on the Integrations page using the following setting:

<Image alt="Enable the Microsoft Teams Video Conferencing integration to record and stream your Teams meetings" align="center" src="https://files.readme.io/ecec8d1-msTeamsVC.png">
  Enable the Microsoft Teams Video Conferencing integration to record and stream your Teams meetings
</Image>

## Vbrick Universal eCDN with Teams

The [Vbrick Universal eCDN with Teams Integration](doc:use-vbrick-universal-ecdn-with-microsoft-teams) is native within Teams.  Meaning, Microsoft Teams (once configured) will automatically us Vbrick for distribution.

This is enabled on the Integrations page using the following setting:

<Image alt="Enable the Vbrick Universal eCDN with Teams integration to use Rev or Vbrick Universal eCDN for distribution" align="center" src="https://files.readme.io/f1c7a78-msTeamsECDN.png">
  Enable the Vbrick Universal eCDN with Teams integration to use Rev or Vbrick Universal eCDN for distribution
</Image>

There are additional Microsoft Teams configurations as describe in [Vbrick Universal eCDN with Teams](doc:use-vbrick-universal-ecdn-with-microsoft-teams).

## Troubleshooting and Known Issues

If you experience any issues during installation or usage of your MS Teams integration, here are some known issues:

* Make sure you update your Vbrick App in Microsoft Teams when new functionality is added.  Particularly if you are missing features that you expect to see.  To update your app, you simply need to reinstall it.
* Minimizing a shared application, or the Windows environment] coverin covering it with other applications may cause Rev to stop showing the content window in live streams and recordings.  This happens because the Microsoft Teams meeting stops sending content data to Rev when a shared application is minimized or hidden.  The recommendation is to not minimize or cover an application that is being shared. 
* In limited cases, some Live and VOD content from Microsoft Teams meetings may not play correctly on MAC Safari. In some cases seeking or a browser refresh may get past the issue. Chrome is recommended for the best user experience on MAC.
