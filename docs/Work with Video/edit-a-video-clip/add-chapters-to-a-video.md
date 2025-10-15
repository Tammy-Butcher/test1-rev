---
title: Add Chapters to a Video
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
Adding chapters to a video allows viewers to jump to those specific locations on the video’s timeline that you have defined (similar to a bookmark). This means you can create named chapters in long videos to allow immediate access to those areas of the video that viewers may want to immediately jump to so they do not have to guess where the content is they want access to.

The Rev video editor provides two different methods for chaptering your video:

* Manually: Specify where you want a chapter to begin, name it, and add a thumbnail image of your choice for each chapter you define.
* PowerPoint: Upload a PowerPoint presentation to your video and the Rev video editor creates automatic chapters based on where the slides appear.  You can adjust the chapters, including the names, after the upload.

## Add Manual Chapters

To add manual video chapters:

1. Click the **Add** icon and select the **Chapters** option.

<Image align="center" src="https://files.readme.io/4ac2f1d-addManualChapter.png" />

2. The first chapter appears at **00:00** on the timeline. Enter a name for the chapter and new time (if you want to change its location from the beginning of the timeline) to create the first chapter. Do this by adjusting the time next to it. 
3. You can also use the **Actions** dropdown to upload your own image to the chapter. If you do not upload your own image, Rev uses a default image. 
4. Chapter images can be set to display by default in [Video Settings](doc:video-features#show-chapter-images-by-default).  They can also be hidden during playback in the [video player](doc:rev-video-player-features#playback-bar-functions).

<Image title="addChapterOne.png" alt="When you add a chapter, enter a name and the time where you want it to appear" align="center" src="https://files.readme.io/f43c2fc-addChapterOne.png">
  When you add a chapter, enter a name and the time where you want it to appear
</Image>

4. To add a second chapter, repeat the process. Click the location on the timeline where you want the second chapter to appear and then click the **Add** icon and select **Chapter**again. 
   * The **Chapter Title** field appears again so you can fine tune where it will appear on the timeline if desired by adjusting the time next to it. You can again use the **Actions** dropdown to upload another image to the chapter or delete the chapter entirely.
   * Note that PowerPoint chapters can no longer be selected. You may not have both types of chaptering in the same video.
   * You can jump to specific chapters through the **View Chapter** dropdown; your mouse wheel will scroll through if several chapters have been added.  Images that have been added can be displayed or hidden through the **Show Chapter Images** icon.

<Image title="vidWithChapters.png" alt={902} align="center" src="https://files.readme.io/020ada2-showHideChapterImages.png">
  Use the Show Chapter Images icon to display and hide images. Jump to a specific chapter using the Chapter dropdown.
</Image>

5. Continue adding chapters as needed and click the **Save** button (or **Save As New**) to finish editing.  Click the **Undo** or **Reset** button(s) at any time before saving to revert any changes you have made.

> 📘 Note
>
> If you leave a timeline gap between chapters, Rev automatically stretches the preceding chapter’s time to meet your most recently entered chapter’s time so there is no space between chapters.

6. Viewers that play the edited video may now click on the [Video Chapters](doc:rev-video-player-features#video-chapters) flyout in the video player to view and jump to the chapters that are defined.

## Add PowerPoint Slide Chapters

If you use a PowerPoint presentation to define your chapters, each slide is a chapter on the timeline and the chapter is named based on the slide **Title**. The presentation is synced across the length of the video automatically upon upload. 

You may modify and edit the presentation slides to suit your needs once the upload is finished. Once saved, Rev users may jump to a specific slide while viewing the video similar to manually added video chapters.

To add a PowerPoint presentation chapter:

1. Click the **Add** icon and select **Presentation**. Note that if the video already contains chapters a PowerPoint presentation *cannot* be added. You may, however, still upload images to the chapters.

<Image align="center" src="https://files.readme.io/a36466c-addPresentationChapter.png" />

2. You are prompted to upload a PowerPoint presentation file from your hard drive. Only files with the **ppt** or **pptx** extensions are supported. A message is displayed that the presentation is loading. While the PowerPoint is loading, you are not able to edit the video.
3. Once loaded, the first slide of the PowerPoint begins at 00:00 on the timeline and the remainder of the slides are spaced evenly across the span of the entire timeline.
4. The slide titles are the chapter names and, if no slide title is available, the slide number is used instead.

<Image title="addPowerPointChapter.png" alt={502} align="center" src="https://files.readme.io/9fc0d56-addPowerPointChapter.png">
  PowerPoint slide titles are the chapter names (or slide number if not titled)
</Image>

5. Click a slide to edit its name and time attributes. 
   * You may also use the **Actions** dropdown to replace chapter's image, remove a slide image, or delete the chapter entirely.
   * You can jump to specific chapters through the **View Chapter** dropdown; your mouse wheel will scroll through if several chapters have been added.  Images that have been added can be displayed or hidden through the **Show Chapter Images** icon.

6. Continue adding chapters as needed and click the **Save** button (or **Save As New**) to finish editing.  Click the **Undo** or **Reset** button(s) at any time before saving to revert any changes you have made.

## The Chapter Actions Dropdown

The **Actions** dropdown for a chapter allows you to perform the following functions on a chapter once added:

<Image title="actionsDropdown.png" alt={502} align="center" src="https://files.readme.io/8f4d176-actionsDropdown.png">
  Use the Actions dropdown to modify chapter images or to delete a chapter
</Image>

* Upload Image (not shown) Replaces the default image that is added when you add a non-power point chapter.
* Replace a previously uploaded image. If you delete an added image, the chapter remains. If no image has been previously uploaded, you will have an **Upload Image** option to replace the default image.
* Remove an image entirely
* Chapter images can be set to display by default in [Video Settings](doc:video-features#show-chapter-images-by-default).  They can also be hidden during playback in the [video player](doc:rev-video-player-features#playback-bar-functions).
* Delete a chapter. If you delete a chapter, the previous chapter’s length on the timeline will expand to fill the gap left by the deletion.
