---
title: The Screen Recorder
excerpt: How to record and share your screen directly from your browser
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Easily create knowledge-sharing videos and captures directly from your browser using the **Screen Recorder** without the need to install any additional tools.  This feature can be invoked from within the **Upload** tray under the **Live Recording** tab or by using the **Screen Recorder** icon in the Header navigation.

<Image align="center" src="https://files.readme.io/999d6820ddb66290250b8673317c1845768d9928b02c88ee5d854d8d9e879b62-screenRecorder.png" />

The screen recording capability utilizes WebRTC technology to securely capture content in the cloud.  We support the use of WebRTC browsers on PCs and Macs while mobile/tablet devices with WebRTC are limited to capturing only the camera.  

Once captured, a **dual-stream** recording is created that takes advantage of our dual-stream playback. The dual-stream recording is generated as an MBR (Multi-Bitrate Recording) using the same resolutions/bitrates as [Video Conferencing Integration (VCI)](doc:video-conference-vc-integrations) recordings. 

You can select and record one of your desktops, an application, or a tab within your browser.  You can also select and record a webcam and microphone.  These selections are made before the recording begins and cannot be changed mid-recording.

Once finished, the recording is processed into Rev as a Rev video--taking advantage of all of Rev's features like workflows, access controls (including Channel access controls), and enrichment.

## Requirements

* This feature is only available in Cloud Rev for those users that have Media creation and upload permissions.
* In the Admin > Media Settings > Integrations menu, you must have **Webcam & Screenshare, Screen Recording, and Producer** enabled under the [Additional Video Sources](doc:additional-video-sources#allow-screen-recording) section enabled. If this is not enabled, the Screen Recorder icon is not visible in the Header navigation nor are you able to launch it from the Upload tray.
* To use the Screen Recorder, you *must* make sure you add the [https://\*.vci.vbrickrev.com](https://*.vci.vbrickrev.com) URL to your [Required URLs and Allowed Lists](doc:rev-required-urls-and-allowed-lists).
* Access to your webcam, microphone, and screenshare is necessary. You will be able to select between your webcam and/or screenshare.  
* You may mute your microphone if you do not want to record it.
* You *must* enable either a screen or a camera (or both).  You cannot have both disabled and record audio only.

<Image align="center" src="https://files.readme.io/1eb77c7be167343902515331b027f9658db1ffe159578dc8a1c483b08b2235a9-enableScreenCamera.png" />

> 🚧 Important!
>
> While recording is in progress, you can pause the recording.  Keep in mind that this pause is limited to 20 minutes, and if you do not respond or continue, the recording will complete.

## Usage

To screen share and record content:

1. Click the **Screen Recorder** icon in the Header navigation. Alternatively, you can also click the [Upload](doc:adding-video) icon > **Live Recording** tab and then make sure **Screen Recording** is selected.

2. The **Screen Recorder** is launched in a separate tab where you can begin making your initial selections for your recording.

<Image align="center" src="https://files.readme.io/4cc8afb171d720a30c9b880410fc5ca082aa3d6bcae679eec2a088dc2166c334-initialLaunch.png" />

## Toggle Screen Sharing On

Begin by deciding what screen content you are going to share and record to a video.  In addition to a web camera and microphone, you can choose to capture system screens, application windows, and/or browser tabs. These are provided visually as two captures -- and are combined into one dual-stream video recording.

When you switch the **No Screen** toggle to on, a pop-up window appears and you are able to see which options are available to record as part of your video depending on the browser you are using.  Note that the actual look of your pop-up may be different from supported browser to supported browser.

<Image alt="Toggle Screen options to view browser tab and window options you have open or to share your entire screen" align="center" src="https://files.readme.io/c4683f364581404445f1ef85cee25573dd2ce5b010249fa2bc078aad1b867a6d-contentShareOptions.png">
  Toggle Screen options to view browser tab and window options you have open or to share your entire screen
</Image>

You are able to switch between the browser tab(s), the browser window, and your entire screen.

> 🚧 Important!
>
> The ability to capture audio from either your browser or system is limited to certain browsers and Operating Systems. If your system supports this feature, an **audio** checkbox is displayed and you have the ability to toggle that audio on/off.  
>
> This is *not to be confused* with your microphone audio which is selected and recorded differently. This audio is your browser's audio if any exists and may conflict with microphone audio if you plan to use it.  Be aware of this and set the toggle accordingly.

## Toggle Your Webcam On

Next, the **Camera** option is used to toggle your **webcam** so that you can record a video speaker if desired.  Your default camera option will be automatically selected for you and you can manually choose from the dropdown menu additional camera options if any are available on your computer.  

> 👍 Tip
>
> If you do not see your camera or microphone, please exit the interface and check your system settings (specifically, check for availability of your devices and make sure they are not being used by other system applications) -- and then re-enter the **Screen Recorder** tool.

<Image alt="Your default camera is pre-selected for you and you are also able to choose permissions for it" align="center" src="https://files.readme.io/7359eac70dc76933b389d462012375eb074144ed7b46cc3915508b292bd0a0a4-previewCamera.png">
  Your default camera is pre-selected for you and you are also able to choose permissions for it
</Image>

## Toggle Your Microphone On

If you want to record yourself speaking during the video, toggle the microphone on to enable it during the video recording.

<Image alt="Your default microphone is also pre-selected for you and recording levels can be seen in the toggle box" align="center" src="https://files.readme.io/cde42e2c990a5769bd656bd7c236f0b1ed6b2616bc1beebe5019a88e53cc6763-previewAudio.png">
  Your default microphone is also pre-selected for you and recording levels can be seen in the toggle box
</Image>

Just as with your webcam, your default microphone is pre-selected for you and you are able to change it.  Notice that your microphone feedback levels are also dynamically displayed for you in the toggle box.

> 👍 Tip
>
> You can change any of your selected recording options before you begin recording by choosing **See Options**. Once you begin recording, they may not be changed.

## Camera and Microphone Permissions

Please be aware that the first time you access the Screen Recorder, Rev requests access to your camera and microphone as seen in the image above.  If you inadvertently block it or **Cancel** the window because you are not ready to begin, this may block access and you may not be able to use this function again until you allow access in your browser settings and cookies.

To allow Rev access to your camera and microphone, click the site permissions/info icon in your browser URL.  You can click the **Always allow** option or click the **Reset permission** button to manage your cookie settings (this is browser dependent).

<Image title="cameraMicrophoneAccess.png" alt={412} align="center" src="https://files.readme.io/164f075dbc9cd04563ddeba67296efcbdcd7564c4128300c34d97facf71d4a58-resetPermissions.png">
  You must make sure that you allow Rev access to camera and microphone to use this function.  If you accidentally block Rev, click the site info icon in your browser's URL.
</Image>

## Record Your Shared Content to a Rev VOD

Once you have selected your sharing and recording options, click the **Start Recording** button to begin recording your video. 

The following actions occur when you click **Record**: 

1. A **Connecting** message appears and a countdown from three appears to indicate recording is about to start.  

<Image align="center" src="https://files.readme.io/e3e8b10923201cc206f00041b51ed887c41f925702cd9b45419eca5263576b68-recordCountdown.png" />

2. Rev then begins to record your video with the options you selected.  
3. A **Recording** message is displayed across the top of your **Capture** window along with how long you have been recording.

<Image align="center" src="https://files.readme.io/e8d3e395a3f9b975d7ffca3c82297d3a94adfcafb1d2f3b089caec28ee14385d-endRecording.png" />

> ❗️ Caution!
>
> Since this tool is using browser-based technologies, do not close the browser or log out of Rev.\
>  Either of these actions will terminate the recording.  Also, you should not close any application or browser tab that is being recorded during the recording.

**Recording Controls** are displayed on the bottom of the capture window. You have the option to **Start Over** and/or **Pause** your recording at any time.  Click the **End Recording** button to stop recording.  Rev uploads the video and you can edit as you normally would and share it across the Rev platform.

> 👍 Tip
>
> It is very important that you test this feature within your environment.  There are differences in browsers and internet connections that can impact the quality.  As always, please verify the quality and flow before using within event.  Please review the [Rev Screen Share and Webcam Best Practices](doc:rev-screen-share-and-webcam-best-practices).
