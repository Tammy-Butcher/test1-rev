---
title: Video Player Flyout Panels
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
To the right of the Rev video player window are Rev’s video panel icons.  Clicking an icon opens its associated flyout panel with specific functions and metadata for that video.  What appears in each panel depends on what has been configured or enabled in Rev by your Account Admin. The table below describes each panel in brief with a link to more detailed descriptions.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "left" }}>
        Icon
      </th>

      <th style={{ textAlign: "left" }}>
        Flyout Panel Descriptions
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/5ecab1dbebaace1357e02e2b8e41810bf709ad9ba1ff3c5ea2777bf35fd78c5e-videoInformationIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Video Information Panel](doc:rev-video-player-features#video-information)

        When this icon is clicked, the flyout panel reveals various metadata about the video you are viewing and also includes video settings that may have been enabled for the video.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/b380628112f2a7dbfe1c11d1fb7d8591ee3916e67fb17aa055066ace62f13c38-videoCommentsIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Comments Panel](doc:rev-video-player-features#video-comments)

        Provides a means for you to leave and view comments on the video.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/5edc8e3bfc6466651aa7b57fe408e663180f0e0f00914127b96b8719e4c86431-videoSharingIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Sharing Panel](doc:rev-video-player-features#video-sharing)

        Link or embed the video you are viewing.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/3d8a7622223f1163ca45ad8ba1c4f86dd944e1b8f851ce7e50eab476a29c3d71-videoTranscriptIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Transcript Panel](doc:rev-video-player-features#video-transcript)

        Displays tagged users in the video (if enabled) and the video transcript (if available).
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/d25f88171653c2434fe64d3cac31f9d1c1cc6f99631b5a24ea129dcf32495aa2-videoAssistantIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Video Assistant Panel](doc:rev-video-player-features#generative-ai-video-assistant)

        Provide access to the Rev Generative AI Assistant (if enabled).
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/c8e9d2fabfb351a8929b3b291c199ffeb0bb228d8efee184583f0483f91e126a-videoPlaylistIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Add to Playlist Panel](doc:rev-video-player-features#video-playlists)

        Opens playlist options for the video; including the ability to add to an existing playlist and the ability to create a new playlist.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/3596a8db586766256b81e58ff58deb74491db5d748e14ab7a214132957a8fc83-videoChaptersIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Chapters Panel](doc:rev-video-player-features#video-chapters)

        Opens the Chapters panel if the video contains chapters which then allows you to jump to different chapters that have been defined in the video.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        ![](https://files.readme.io/4732b03ed2877c620b47002a74eca09b125e13dfcd252a2b43724ede358cdf52-videoReportsIcon.png)
      </td>

      <td style={{ textAlign: "left" }}>
        [Reports Dashboard](doc:rev-video-player-features#video-reports)

        Opens the Reports Dashboard for the video.
      </td>
    </tr>
  </tbody>
</Table>

> 👍 Tip
>
> Some icons may or may not appear in your player depending on what features have been enabled for your portal.

## Video Information

The **Video Information** panel contains various metadata about the video along with various video settings that may have been enabled.

<Image
  align="center"
  alt="The various video settings and metadata that have been configured appear on this panel

"
  border={false}
  caption="The Information Panel (partial view) contains the various metadata and video settings that have been enabled for the video"
  title="videoBasicInfoPanel.png"
  src="https://files.readme.io/389b5419de52f5409f0d46abf94e61b0a75ab767b3a317f63fe895d04d987806-infoPanel.png"
  width="smart"
/>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Setting
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Title
      </td>

      <td>
        The video [title](doc:update-basic-video-settings#title-and-description) that is given in video settings
      </td>
    </tr>

    <tr>
      <td>
        ![](https://files.readme.io/96f859003a928ecc198b1724bfe115eb0c86d887f0575245a31c236e38751ffd-downloadVideo.png)
      </td>

      <td>
        [Download](doc:update-basic-video-settings#enable-comments-ratings-and-downloading) the video (if enabled).  Not visible if this feature has not been enabled for the video.
      </td>
    </tr>

    <tr>
      <td>
        ![](https://files.readme.io/6e5af2f1bceb9a0ef001978679493de851aa964591449437e34386ff5b80a670-exportLMS.png)
      </td>

      <td>
        [Export a Video for a Learning Management System (LMS)](doc:export-a-video-for-a-learning-management-system-lms) if you have the correct permissions.  Not visible if you do not have an Admin or LMS Exporter role.
      </td>
    </tr>

    <tr>
      <td>
        Description
      </td>

      <td>
        The [description](doc:update-basic-video-settings#title-and-description) that is entered in video settings. Includes a disclaimer if it was auto-generated by Rev's Generative AI features.
      </td>
    </tr>

    <tr>
      <td>
        Total Views
      </td>

      <td>
        Total number of views (including **Last Viewed** date and time based on user’s time zone)
      </td>
    </tr>

    <tr>
      <td>
        Owner
      </td>

      <td>
        The [video owner](doc:video-owner) is the uploader by default but a video owner can also be assigned that is not the original uploader.
      </td>
    </tr>

    <tr>
      <td>
        Upload Date
      </td>

      <td>
        The date and time that the video was [uploaded](doc:upload-video).
      </td>
    </tr>

    <tr>
      <td>
        In This Video
      </td>

      <td>
        Users that are [tagged](doc:update-basic-video-settings#tag-users-in-a-video) in a video.

        Timeline tagging that highlights on the timeline where in the video speakers are present is available _only_ if [Facial Recognition](doc:facial-recognition) is enabled (disabled by default).

        * Profile pictures that have tagging enabled are indicated by an arrow > next to their image. If enabled, click the profile picture to highlight the range the speaker appears on the timeline.

        * Users may opt-out of [tagging](doc:update-basic-video-settings#tag-users-in-a-video) any time by updating their [Profile Settings](doc:your-rev-profile#update-your-profile-image).
      </td>
    </tr>

    <tr>
      <td>
        Categories
      </td>

      <td>
        [Categories](doc:update-basic-video-settings#categories-and-tags) the video belongs to; clicking a category will take you to the Category archive page and display all videos that belong to that specific category.
      </td>
    </tr>

    <tr>
      <td>
        Tags
      </td>

      <td>
        [Tags](doc:update-basic-video-settings#categories-and-tags) the video has been assigned; clicking a tag will take you to a search results page and display all videos that have been tagged with that specific tag.
      </td>
    </tr>

    <tr>
      <td>
        Custom Fields
      </td>

      <td>
        [Custom fields](doc:update-basic-video-settings#use-a-custom-field), if defined, appear beneath the Tags field.
      </td>
    </tr>

    <tr>
      <td>
        Rating
      </td>

      <td>
        [Rate](doc:update-basic-video-settings#enable-comments-ratings-and-downloading) the video from 1 to 5 stars and view ratings that have already been applied.

        The **Rating**indicates the "average rating received" while the the **Total Ratings** is the "total number of ratings" received on the video to date.
      </td>
    </tr>

    <tr>
      <td>
        Supplemental Files
      </td>

      <td>
        If [supplemental files](doc:update-advanced-video-settings#attach-a-supplemental-file) are attached to the video they are downloaded from this panel.
      </td>
    </tr>

    <tr>
      <td>
        Inappropriate Content
      </td>

      <td>
        Flag or report video for inappropriate content.

        Click the **Report**icon to flag the video for inappropriate content.  Account and Media Admins will receive a notification in Rev and an email so that the video may be reviewed.
      </td>
    </tr>

    <tr>
      <td>
        Password Protected Notification
      </td>

      <td>
        If the video is a [Public](doc:create-event#schedule-a-public-event) video and **Password**protected, it is noted on this panel.
      </td>
    </tr>

    <tr>
      <td>
        Approval Process Stage
      </td>

      <td>
        Present if the video is part of an [Approval Process](doc:define-an-approval-process)
      </td>
    </tr>

    <tr>
      <td>
        Uploader
      </td>

      <td>
        The [video owner](doc:video-owner) is the person who uploads the video but this can be reassigned.
      </td>
    </tr>
  </tbody>
</Table>

## Video Comments

Use the **Video Comments** flyout panel to enter a comment on a video and view/sort all previously entered comments.  If a comment is replied to, the commenter is notified in the [Notifications](doc:notifications) tray.

Only Account and Media Admin account(s) can delete all user comments in addition to their own comments.

<Image align="center" alt={401} border={false} caption="Use the Comments flyout to enter rich text comments (including emojis) on VODs" title="commentsFlyout.png" src="https://files.readme.io/de1842e5402fbaf17fffb9fb3c9738fc45f5c2ac6bcfcb70a8c0c0018d5bde95-videoCommentsFlyout.png" />

## Video Sharing

Use the **Video Sharing** flyout panel to access [sharing](doc:share-a-video) and [embedding](doc:embed-a-video) options that may be enabled for a video.

<Image align="center" alt={372} border={false} caption="The Sharing flyout panel is used to both share and obtain embed code for Rev videos" title="sharingFlyout.png" src="https://files.readme.io/644c8997c747a21dcc800eba45ed97145225ffa13f9b7194137dcb7519e0fdc5-videoSharingFlyout.png" />

## Video Transcript

The **Video Transcript** flyout displays speakers that are tagged [In This Video](doc:tag-users-in-a-video). When combined with the Rev IQ module’s [Facial Recognition](doc:facial-recognition) capabilities, it also highlights each speaker interactively (during playback) as they appear in real-time along with audio transcript highlighting and on the timeline if their profile image is clicked. Profile pictures that have tagging enabled are indicated by an arrow > next to their image.

<Image align="center" alt={537} border={false} caption="The Video Transcript flyout highlights each tagged speaker as they appear in the video along with their audio when used with Rev's Facial Recognition license" title="videoPulseFlyoutPanel.png" src="https://files.readme.io/5f0885672ab70d99d12eb99bd5fbb173435268c67164124e2d73a84a48a45579-videoTranscriptFlyout.png" />

This interactivity requires an [SRT transcript file uploaded](doc:update-advanced-video-settings#subtitles-translations-and-closed-captions) (for audio transcripts) and a Rev IQ license purchased (for timeline tagging).

The **Video Transcript** flyout also features the ability to **Search** videos for text in [audio transcripts](doc:search-and-filter-functions#speech-search-results) (SRT files) and any tagged users.

### Quick Edit or Delete a Subtitle in the Transcript Flyout

User accounts that have video edit rights are able to quickly correct transcripts directly in the **Video Transcript** flyout by clicking the **Edit** icon that appears next to a transcript line.  When clicked, the text of the subtitle may be edited or deleted as needed.

<Image align="center" alt={502} border={false} caption="Click the Edit (pencil) icon next to a subtitle that you want to edit.  Be sure you click the Save icon to save any changes you make." title="videoPulseEdits.png" src="https://files.readme.io/27ffc4f190fe905c9236d1fd58d5176eadb01c910976b901f69386ca72c0574c-videoTranscriptEdit.png" />

To edit or delete a transcript in the Video Transcript flyout:

1. Click the **Transcript** icon in the video player.

2. Click the **Edit** icon next to the subtitle you want to correct.  If the icon does not appear when hovering next to the subtitle, you do not have edit rights.

3. **Edit** the subtitle text as needed.  Note that you can also edit the time field if needed.

4. Click the **Delete** icon to remove the text.  This may _not_ be undone so use caution.

> 👍 Tip
>
> You can only have one line open in edit mode at a time.

5. Click the **Save** icon to save your changes.  When you save the subtitle edits, the version of the file in search is also updated.

## Generative AI Video Assistant

The **Video Assistant** flyout panel allows you to interact with a video's transcript using a Generative AI chat interface to ask questions about a video through a series of prompts. This allows you to receive a quick overview and insights about its content.  Timestamps are included if content is found in the video that directly relates to the questions you ask and clicking on a timestamp will jump you to the place in the video where the content is found. Your conversation history is saved for 90 days unless you clear it or the transcript is modified.

Keep in mind that certain requirements must be met when using this feature. The video must have an [English transcript](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings), you must have the Rev IQ [Video Assistant](doc:vbrick-assistant) enabled, and you must have [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available.

<Image align="center" alt="The Video Assistant flyout allows you to interact with an AI chatbot and ask questions about a video" border={false} caption="The Video Assistant flyout allows you to interact with an AI chatbot and ask questions about a video." src="https://files.readme.io/6fd62c3102fc2ff81d4e07f2c5fe2505b55409e7e041677cdcd87ec8bc6e7049-videoAssistantFlyoutRevPlayer.png" />

> 🚧 Important!
>
> The **Vbrick Assistant** and **Transcript Summarization** features are only available on US-based portals at this time and require **English** transcripts to function. Please contact [Vbrick Support](mailto:support@vbrick.com) if you need assistance.

## Video Playlists

The [Add to Playlist](doc:playlists) flyout panel provides the ability to create and add videos to playlists.

<Image align="center" alt={537} border={false} caption="Create and add videos to playlists in the Add to Playlist flyout panel" title="playlistFlyout.png" src="https://files.readme.io/0153c121a34ed79a06560d564be468c749c80335dc2679755f841d5eb0a58d5b-playlistsFlyout.png" />

## Video Chapters

The **Chapters** flyout allows you to view and navigate between a video's chapters. It is only present in those videos that have chapters defined in the [video editor](doc:edit-a-video-clip).  When you click the **Chapter** icon, the flyout appears and allows you to navigate to the chapters that have been defined.  Think of chapters as bookmarks that allow a user to quickly navigate to content that is specifically relevant or of interest to them.

<Image align="center" alt="If chaptering is added, navigate to a chapter either through the Chapter flyout or through the Chapter dropdown" border={false} caption="If chaptering is added, navigate to a chapter either through the Chapter flyout or through the Chapter overlay in the video window" src="https://files.readme.io/53b58e89e2576bc6b5bef026be65640d8cd85def869405498f89350e82eca1b4-chapterFlyout.png" />

In addition to the Chapter flyout, you can also use the **Chapter overlay** in the player window to select a chapter to jump to or the **Chapter skip** icon in the playback bar to skip forward and back between chapters.

If images have been added to the chapter, you can toggle them on and off using the **Show Chapter Images** icon on the video playback bar. This icon is not present if no images have been added to the chapter.

## Video Reports

<Image align="center" border={false} src="https://files.readme.io/6e45d2429e3994ebffb482e81520ef076cace632f18bd88ea2d37f98ff340449-videoReportsIcon.png" />

The **Reports** flyout displays the [Video Analytics Dashboard](doc:video-analytics-dashboard) that provides detailed analytics and reports for the video.  It is only visible to Account and Media Admins.
