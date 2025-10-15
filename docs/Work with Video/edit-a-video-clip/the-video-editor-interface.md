---
title: The Video Editor Interface
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
The video editor appears when you access **Video Settings** and click **Edit Video** is clicked.  Each section of the interface is numbered in the diagram below so that its functions can be briefly described.  For more detailed steps on using the feature, view the individual topics dedicated to each one.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/837ace4de29b68eee6de7a766c0677fe41e40e386075a12a17a57214025aeb73-videoEditorInterface.png",
        "",
        "The Rev Video Editor Interface"
      ],
      "align": "center",
      "caption": "The Rev Video Editor Interface"
    }
  ]
}
[/block]


1. **Video Player Window and Player Controls**: The top portion of the video editor is fixed and displays the normal Rev video player and player controls. Use this window to view your video and any edits you make.
2. **Timeline and Thumbnail View**: Displays the full timeline of the video as video thumbnails. Defaults to minutes and seconds format (mm:ss). If the video is an hour in length or longer, the timeline displays in (hh:mm:ss) format. Note that the thumbnail view can be manipulated by the scale and position slider (#3) and by any slices you add (#4).
3. **Scale and Position Slider**: This slider control is fixed at the bottom of the interface beneath the timeline and thumbnail view (#2). It adjusts the timeline's scale and allows you to zoom in and out on the thumbnails for more granular time editing as needed. It is particularly useful when editing longer videos as it allows you to view the entire clip. To use the slider:
   1. Adjust the left and right circle controls on the slider as needed to scale the video timeline.
   2. Left-click and drag the slider to the position in the video that you want to view and/or edit.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c1e3a7-scaleControl.png",
        "scaleControl.png",
        "scale controls"
      ],
      "align": "center",
      "caption": "Use the left and right circle \"handles\" to adjust the timeline scale. Then left click and drag the middle of the scale to position the playback head to the position on the timeline where to want to edit."
    }
  ]
}
[/block]


4. **Video Slice and Video Delete Icons**: The video slice icon allows you to create video clips at various points you define in the video (depending upon how many slices you create). Your first slice always creates a clip based upon the beginning of the video and each subsequent slice is created based upon the slices around it. 
   1. For example, in the image below, four video clips are effectively created based on three slices made. These clips can now be deleted using **Delete** icon, moved to a different area on the timeline, or even extended and reduced as needed by dragging the handles on each end of the clip.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/09a9491f28fea82a1e469719f98110f6ccbf50072a78fddb1b55843d30c2bac5-sliceAndDeleteIcons.png",
        "",
        "Each time you make a slice, a new video clip is created that you can manipulate by moving, deleting, or extending/reducing on the timeline"
      ],
      "align": "center",
      "caption": "Each time you make a slice, a new video clip is created that you can manipulate by moving, deleting, or extending/reducing on the timeline"
    }
  ]
}
[/block]


5. **Video Editor Interface Icons**: The video editor interface icons are located to the right of the editor and are explained in detail in the table below from top to bottom.

[block:parameters]
{
  "data": {
    "h-0": "Video Editing Icons",
    "h-1": "Function",
    "0-0": "Clips",
    "0-1": "Merge pre-existing video clips in Rev to the video you are currently editing.  \n  \n- **All Video**: Merge from All Videos you currently have access to view.\n\n- **My Videos**: Filter by just your own videos and merge them into the timeline where you define.\n\n- **Search Videos**:  Filter videos you want to merge by specific keywords.",
    "1-0": "Add",
    "1-1": "Add items to a video. You can add the following items:  \n  \n- **Presentation**: Adds PowerPoint presentation chapters to the video. Note this is different from attaching a standalone supplemental presentation file to a video. In this instance you are syncing the presentation slides to the video timeline that then act as named chapters. These chapters can subsequently be edited and manipulated on the timeline.\n\n- **Chapter**: Add chapters to a video (with no slides) at specified points on the timeline so that other users may jump to those points in time you have defined.",
    "2-0": "Save",
    "2-1": "Allows you to **Save **the edited version of the video or **Cancels **all edits (if not saved first) without saving changes.  Also allows you to select **Save As New** which saves the video as a new video. Includes the title and video template selections (if applied). This is treated as a new video and goes through any approval processes if necessary.  \n  \n**Note:** If you have [Rev Transcription and Translation](doc:rev-iq-transcription-and-translation) enabled, you will be able to use these features to generate or re-generate (as the case may be) transcription and metadata settings for your edited video.",
    "3-0": "Download",
    "3-1": "Downloads the original video to your hard drive (if downloading is enabled). _You are highly advised to do this before editing so you have a saved copy._  \n  \nFor dual stream recordings, you are presented with two download options:  \n  \n- **HLS zip file** for local backup and recovery\n- **MP4 file** for local viewing and sharing",
    "4-0": "Cancel",
    "4-1": "**Cancels **all edits without saving changes and exits the video editor.",
    "5-0": "Undo",
    "5-1": "Undo the last action taken on the clip.",
    "6-0": "Redo",
    "6-1": "Redo the last undone action taken.",
    "7-0": "Reset",
    "7-1": "Resets the video back to its original state at any point in the editing process (if it has not been saved). Or resets the video back to its last saved point."
  },
  "cols": 2,
  "rows": 8,
  "align": [
    "left",
    "left"
  ]
}
[/block]


> ❗️ Warning!
> 
> **Once you edit then save a video the original video is lost. You are _always_ advised to download a copy of the original first! **
> 
> If you do not have the option to [download an original copy](doc:allow-downloads#allow-downloads-for-video-backup) of your video first, speak to your Account Admin about enabling this function before you edit.