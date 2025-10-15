---
title: Video and Audio Formats
excerpt: Supported video and audio file types that you may upload to the Rev portal
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
- MP3
- M4A
- MP4
- FLV \*
- F4V \*
- MKV \*
- MOV \*
- WMV (VC-1) \*
- MPEG-1 \*
- MPEG-2 \*
- MTS \*
- OGV \*
- TS \*

<sup>\* These file types must be transcoded first and are not playable in their original formats.</sup>

# Support for Subtitles and Closed Captions

Users can upload MP4 videos with [accessibility-features](accessibility-features) such as closed captions and multiple audio tracks.

## Closed Caption Support

Rev supports the **CEA-608** and **708** closed caption formats embedded into MP4s. Note that for the CC menu to show in the player, the [Closed Caption](doc:subtitles-translations-and-closed-captions) must be enabled in the video settings.

## Multiple Audio Track Support

If you upload a video that has multiple audio tracks, Rev's [transcoding presets](manage-transcoding-settings#transcoding-preset-default-settings) automatically detects each track and transcodes them accordingly.  You are then able to use translation and subtitle features as you normally would once the video is uploaded.  During playback, users can use the **CC** button to select the multiple audio and subtitle languages that have been applied.

### Android and iOS Native Player Notes

<h4>Android</h4>

- The Rev video player is an HTML5 player and audio tracks can be played and selected normally
- If you change to full screen, you are not able to select a separate track.  The first track selected continues to play.

<h4>iOS</h4>

- The native player does not display the Audio section in the CC Menu
- The device's language that is set is what audio plays, if available
- If no tracks match the device language, it plays the first track instead which should be the video default track