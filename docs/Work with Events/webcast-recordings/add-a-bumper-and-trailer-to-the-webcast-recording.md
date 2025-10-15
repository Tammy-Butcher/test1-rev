---
title: Add a Bumper and Trailer to the Webcast Recording
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
Bumper videos are appended to the front of another video, such as company logo. Trailer videos are added at the end such as when the credits roll. Adding a **Bumper** and/or a **Trailer** to recordings is common.  When setting up a webcast, you can automatically add a **Bumper**, **Trailer**, or both.  After the event, the system will merge selected **Bumper** and **Trailer** videos into the video recording.

**Bumper** and **Trailer** selections can also be saved in [webcast templates](doc:create-a-webcast-template) so they only need to be added once if desired.

<Image alt="Pre and Post-Roll clips are added to the beginning and end of webcast recordings" align="center" src="https://files.readme.io/e17eefb45496d4cc6aedfe5989d67768ef2bd911f7fdafe94eeea61fe94af628-addPrePostRoll.png">
  Bumper and Trailer clips are added to the beginning and end of webcast recordings
</Image>

To do this, in the **Event Webcast Recordings** section, select the **Bumper** or **Trailer** dropdown(s) and select a video.  As a security feature, the dropdown only shows videos for which you have edit access. Filter the videos by using the **My Videos** and **All Videos** tabs. 

Consider using Rev's [Video Editor](doc:merge-videos) to edit the recording further as needed.

> 📘 Note
>
> When a **Bumper** or **Trailer** clip is added they will be delineated by a slice in the video editor to assist with any additional editing when needed.

## Single-Stream Versus Dual-Stream Recordings and VCI-Based Events

In order to save space, the current approach to dual-stream (VCI) recordings *with no content streams* is to reduce a *speaker-only* stream to a single-stream video.  

This means that if you specify dual-stream **Bumper** or **Trailer** clips (and your recording *only* contains a speaker-stream and *no* content stream) then only the **Bumper** or **Trailer** switching stream with the recording speaker-stream is used. This results in a single-stream recording as designed.  

If you wish to maintain content streams in any **Bumper** or **Trailer**, the you will need to display some content during the main recording.

## Limitations and Use Cases

There are some limitations when using **Bumper** or **Trailer** during event set-up.

* Rev's video editor does not mix streams when stitching clips. This means if mismatched **Bumper** or **Trailer** are added and an error is generated, they will not be added.

[VCI-based events](doc:video-conference-vc-integrations) have further use cases you should be aware of. Particularly when it comes to displaying content streams as mentioned in the section above.

* You should *only* add dual-stream bumper and trailer in the event you are uncertain if the event shares dual or single streams.
* If the VCI webcast does *not* have a content stream and there *is* a dual stream bumper and trailer added, the webcast recording will be merged into a single-stream video when concluded. 
* If the VCI webcast does *not* have a content stream and there is *not* bumper and trailer added during event set-up, the webcast recording will continue with its current behavior and will be converted to a single-stream video when concluded. The original video remains an MP4 file.
