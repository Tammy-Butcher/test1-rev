---
title: Screen Share and Record
excerpt: >-
  How to use Rev to share and record yourself or your screen directly from your
  browser
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Easily create knowledge-sharing videos and captures directly from your browser using Rev's **Screen Recording** functionality without the need to install any additional tools.  This feature is invoked from Rev's main page within the **Upload** menu (including in the **Channel** view).

> 👍 Tip
> 
> This feature is only available in Rev Cloud for those Rev users that have media creation/upload rights.  To use this feature, you need to add the <https://*.vci.vbrickrev.com> URL to your [Allowed Lists](doc:rev-required-urls-and-allowed-lists).

Rev's **Screen Recording** capability utilizes WebRTC technology to securely capture content in the cloud.  We support the use of WebRTC browsers on PCs and Macs while mobile/tablet devices with WebRTC are limited to capturing only the camera.  

> 🚧 Important!
> 
> This feature requires access to your webcam, microphone and screenshare.  While you may give access and select between webcam and/or screenshare -- you must give access to the microphone.  Please use the mute if you do not want to record your microphone.

Once captured, a **dual-stream** recording (like VCI recordings) is created that takes advantage of our dual-stream playback. The dual-stream recording is generated as an MBR (Multi-Bitrate) recording using the same resolutions/bitrates as Video Conferencing Integration (VCI) recordings. You can select and record one of your desktops, an application, or a tab within your browser.  You can also select and record a Webcam and microphone.  These selections are made before the recording begins and cannot be changed mid-recording.

> 🚧 Important!
> 
> While recording is in progress, you can pause the recording.  Keep in mind that this pause is limited to 20 minutes, and if you do not respond or continue, the recording will complete.

Once finished, the recording is processed into Rev as a Rev video--taking advantage of all of Rev's features like workflows, access controls (including Channel access controls), and enrichment.  Additional details follow. 

To screen share and record content in Rev:

1. In the **Upload Tray**, Click the **Live Recording** tab and make sure **Screen Recording** is selected.

2. Click the **Start** button to open a **Capture** window.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a166dc-screenRecording.png",
        null,
        "The Screen Recording tab allows screen sharing and recording directly from Rev"
      ],
      "align": "center",
      "caption": "The Screen Recording tab allows screen sharing and recording directly from Rev"
    }
  ]
}
[/block]


> 📘 Note
> 
> If the **Recording** tab is not visible, contact your Account Admin to enable [Video Conference Integrations](doc:video-conference-vc-integrations)

## Toggle Screen Sharing and Web Camera Options

Begin by deciding what content you are going to record to a video.  In addition to a web camera and microphone, you can choose to capture system screens, application windows, and/or browser tabs. These are provided visually as two captures -- and are combined into one dual-stream video recording.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9f3c10-blankScreenShare.png",
        null,
        "You can enable screen sharing or your webcam or both when you enable Screen Recording"
      ],
      "align": "center",
      "caption": "You can enable screen sharing or your webcam or both when you enable Screen Recording"
    }
  ]
}
[/block]


When you toggle the **Screen **switch to **On**, you are able to see which options are available to record (share) depending on the browser you are using and what you have open.  The images below represent one browser's implementation of the video source selection.  Because we are utilizing WebRTC as the underpinnings for capturing the content, the actual look may be different from supported browser to supported browser.

> 🚧 Important!
> 
> The ability to capture audio from  either your browser or system is limited to certain browsers and Operating Systems. If your system supports this feature, an **audio** checkbox is displayed and you have the ability to toggle that audio on/off.  
> 
> This is not to be confused with your microphone audio which is selected and recorded differently.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4e4aef7-screenShareSelect.png",
        "screenShareSelect.png",
        600
      ],
      "align": "center",
      "caption": "Toggle the Screen option to On to view your screen sharing options"
    }
  ]
}
[/block]


The **Camera ** option is used to toggle your **Webcam** to record a video speaker.  Notice you are able to use automatic default options for both your webcam and microphone or you can manually choose from the dropdown menus specific options that may be available on your computer.  

> 👍 Tip
> 
> If you do not see your camera or microphone, please exit the interface and check your system settings (specifically, check for availability of your devices and make sure they are not being used by other system applications) -- and then re-enter the **Screen Recording** tool.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f4e1dcf-chooseWebCamOptions.png",
        "chooseWebCamOptions.png",
        793
      ],
      "align": "center",
      "caption": "Choose your Webcam options to record a speaker along with your selected screen share"
    }
  ]
}
[/block]


## Record Your Shared Content to a Rev VOD

Once you have selected your sharing and recording options, click the **Record** button to begin recording your video. 

The following actions occur when you click **Record**: 

1. A **Connecting** message appears.  
2. Once Rev is connected and is ready to begin recording, Rev counts down from three and then begins to record your video with the options you selected.  
3. A **Recording ** message is displayed across the top of your **Capture** window.

> ❗️ Caution!
> 
> Since this tool is using browser-based technologies, do not close the browser or log out of Rev.  
>  Either of these actions will terminate the recording.  Also, you should not close any application or browser tab that is being recorded during the recording.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7719b21-recordContent.png",
        "recordContent.png",
        702
      ],
      "align": "center",
      "caption": "The Finish button saves your video recording and uploads it to Rev where you can edit it."
    }
  ]
}
[/block]


**Recording Controls** are displayed on the bottom of the Capture window and the length of the recording in progress is displayed in view beside the button options. You have the option to **Delete** and/or **Pause** your recording at any time.  Click the **Finish **button to stop recording.  Rev uploads the video and you can edit as you normally would and share it across the Rev platform.

## Camera and Microphone Access

Please note that the first time you access the **Capture** window, Rev requests access to your Camera and Microphone.  If you inadvertently block it or, for example, **Cancel** the window because you are not ready to begin, this may block access and you may not be able to use this function again until you allow access again in your browser settings and cookies.

To allow Rev access to your Camera and Microphone, click the Camera option in the upper right corner.  You can click the **Always allow** option or click the **Manage** button to manage your cookie settings (this is browser dependent).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4aabd9b-cameraMicrophoneAccess.png",
        "cameraMicrophoneAccess.png",
        412
      ],
      "align": "center",
      "caption": "You must make sure that you allow Rev access to camera and microphone to use this function.  If you accidentally block Rev, click the microphone in the upper right corner of the Rev Share window."
    }
  ]
}
[/block]


> 👍 Tip
> 
> It is very important that you test this feature within your environment.  There are differences in browsers and internet connections that can impact the quality.  As always, please verify the quality and flow before using within event.  Please review the [Rev Screen Share and Webcam Best Practices](doc:rev-screen-share-and-webcam-best-practices).