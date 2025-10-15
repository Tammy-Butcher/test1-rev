---
title: Manage Audio Tracks for a Video
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
The **Name** and **Subtitles** columns display the **default transcription language** and voice **Audio Track** on the top row of the **Languages** tab. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fe5d300851f32cda5583232b516a442c82b1e856f03a08f2eee9ac91b98a18fe-languageActionsMenu.png",
        "",
        "The Actions menu to the right of each row details what actions can be performed on specific rows"
      ],
      "align": "center",
      "caption": "The Actions menu to the right of each row details what actions can be performed on specific rows"
    }
  ]
}
[/block]


The **Actions** menu to the right of each row allows you to take the following actions, depending upon the row:

- Edit Language
- Download Subtitles
- Delete Subtitles
- Set Default Audio (if not already the default audio track)
- Delete Audio (if not the default audio track)

## Edit, Download, or Delete Subtitles or Audio Tracks on a Video

You can edit any subtitle or audio track file by using the **Actions** menu next to the row.

For example, to edit, download, or delete a subtitle file:

1. Click the **Actions** menu next to the row on the **Languages** tab.  
2. Click **Edit Language** to change the audio track's language.  You may only update the original transcription file and _not_ the subtitle file that was a default translation based on the original (default) transcription file. What does this mean?  In the example below, we want to edit the currently named "French" Audio Track. This file is a translation file that was created when the video was uploaded and is based on the original English transcription file.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/05b1eea4805f79593e16622c0eab37a178072e49701d085b7fb9279954f3b5a5-editFrenchLanguage.png",
        "",
        "To modify a row's transcription language, select Edit Language"
      ],
      "align": "center",
      "caption": "To modify a row's transcription language, select Edit Language"
    }
  ]
}
[/block]


3. When **Edit Language** is selected for the French language row, the "Name" and "Subtitles" fields are cleared and now labeled  **Unknown**  so that you can select the new language **Name** and **Subtitles** you want to use for this Audio Track instead.  The _original_ French Subtitles file is moved to the bottom of your list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e480797ced2691a53838a69f670145b4ff6e706abddd44ca756f2d952cfe8514-editFrenchInProgress.png",
        "",
        "When you select Edit Language, a new row is created to modify while the original row is moved to the bottom of the Language table"
      ],
      "align": "center",
      "caption": "When you select Edit Language, you are editing the Name and Subtitles for that Audio Track. Note there is no Edit Language option in the menu when no Audio Track is present."
    }
  ]
}
[/block]


4. Click the **Select** button to choose the new language. You can then click the **Add** button in the **Subtitles** row to auto-generate or add your own transcription file. At this point you are also able to add a new voice **Audio Track** for the original file as well.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9ecdba90ff273f73a18db1a6dc8877bee9c483950d95fbea1c80f4549719bd14-addFrenchSubtitleUpdate.png",
        "",
        "Once the new language is selected, click the Add button to update or add a new transcription file."
      ],
      "align": "center",
      "caption": "Once the new language is selected, click the Add button to update or add a new transcription file"
    }
  ]
}
[/block]


5. Click the **Save** button.  One the video finishes processing, the new subtitle file is available along with the audio track. Note that the original row will need to have a new audio track generated at this point as mentioned above.
6. You can also use this menu to **Download** or **Delete** subtitle and voice audio files.  Please note that if you delete a subtitle file, this action is not saved until you click the **Save** button. **Note**: You may _not_ delete _all_ audio tracks.  A video must retain at least one.
7. A **Cancel** option may appear for rows that have a pending action. Selecting Cancel will cancel any pending tasks associated with that row.
8. Finally, you can choose to change the default subtitle and audio track by selecting [Set Default Audio](doc:set-the-default-audio-track-for-a-video)  next to a row that is not already the default. All actions will be designated **Pending** until the **Save** button is clicked.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d552518df81acbc1e4499b6b585626aa1557eca237f0af50099937258026c355-pendingDefaultAudioChange.png",
        "",
        "You make a new row the default language. It will be Pending Default until you save the video."
      ],
      "align": "center",
      "caption": "You make a new row the default language. It will be Pending Default until you save the video"
    }
  ]
}
[/block]