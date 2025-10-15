---
title: Export a Video for a Learning Management System (LMS)
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
Rev videos can easily be viewed, tracked, and managed in a Learning Management System (LMS) with the export to LMS feature in Rev. You must be an Account or Media Admin or have the [LMS Exporter](doc:video-permissions#media-and-video-granular-roles-and-permissions) role before you may view and use this feature.

The export supports the following:

* It is [SCORM 2004 4th edition format](https://scorm.com/scorm-explained/technical-scorm/scorm-2004-overview-for-developers/) compliant
* You can set the **Completion Percentage** required. It is set to 80% by default.
* You can toggle if **Speed Changes** (while viewing) are allowed. It is set to Off by default.

To export a video for an LMS:

1. Navigate to the video you want to export.
2. Open the[ Information](doc:video-player-flyout-panels#video-information) flyout panel.
3. Click the **Export for LMS** button.  If it is not visible, you do not have the correct permissions.

<Image align="center" src="https://files.readme.io/470f2006b605a30dbdf8732e4f2e357129562473396d56633736518ae22f04f4-exportLMSButton.png" />

4. You will be asked what percentage of the video the learner is required to complete. The default is 80%.

<Image align="center" src="https://files.readme.io/6f29ccbac6c218a49f9c7d829cabb6e8fb3030dcaf3cb7705697f8d7f8978be6-scormDefaultSettings.png" />

5. You will also be able to set if speed changes are allowed while the learner is viewing the video (fast forward, etc.). The default is set to no.
6. A zip file with the name of your video + LMS is downloaded to your **Downloads** folder that you can use to import into your LMS.
