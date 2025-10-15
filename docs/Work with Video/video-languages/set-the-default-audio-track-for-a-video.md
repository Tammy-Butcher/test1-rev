---
title: Set the Default Audio Track for a Video
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
When a video is first uploaded, Rev attempts to detect the language code of its **Audio Track** where it is then merged with its default **Transcription** language in the top row of the **Languages** tab.   When they match, the first row appears similar to the image below as the default language.

<Image alt="Rev attempts to automatically detect the audio track in an uploaded video" align="center" src="https://files.readme.io/e93e2c1ddc186d871c479123a30c1653d83b14590db610447da843d9d40f0cb1-mergedAudioSubtitleTrack.png">
  Rev attempts to automatically detect the voice audio track in an uploaded video
</Image>

There are certain [supported video types](doc:supported-file-types) that do not have a language code in their file which is what Rev needs to detect the audio track.  When this occurs, the top row of the **Languages** table returns **Unknown** instead as seen in the image below.

<Image alt="Unknown is returned if the video language cannot be detected by Rev" align="center" src="https://files.readme.io/5836f40af5b9a05d6de3aeba97d7d38e515ed7b098cf30bfc542697c256a35cd-unknownAudioTrack.png">
  Unknown is returned if the video language code cannot be detected by Rev; frequently seen in webcast recordings or a legacy or historical video type
</Image>

This issue is quickly corrected by clicking the **Select** button and then choosing the language used in the video (which is most often the **Automatic Transcription Language**).  The language **Name** will switch to **Pending Save** until you click the **Save** button. Once saved, the **Audio Track** is then merged with the transcription file on the top row as expected and becomes the default voice audio track.  

If you have added alternative Audio Tracks to the video, you can also change the default track by using the **Actions** menu to the right of the row and clicking the **Set Default Audio** option.  Upon saving, the new row and language becomes the default audio and is moved to the top row.

<Image align="center" src="https://files.readme.io/ad07dfd1b46de6927a7ceab970da077d7100bcfc675768b775bfc44470eabfbb-setDefaultAudio.png" />

> 📘 Note
>
> Additional video format types that do *not* have a language code specified in the file (along with legacy/historical videos and those created by Rev via webcast recording) include the following:
>
> * avi
> * flv
> * mp3
> * mpg (mpeg-1)
> * mp4
>
> These video types will require a manual selection of a default audio track as described in this topic.
