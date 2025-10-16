---
title: Facial Recognition
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
**Facial Recognition** extends the functionality of Rev's manual user tagging in a video so that users can automate the process.  It also extends the interactive functionality of the [Video Information](doc:rev-video-player-features#video-information) and [Video Transcript](doc:rev-video-player-features#video-transcript) flyout panel(s) on the Rev video player so that viewers can see _who_ is in a video and _what_ is being said (in real-time) as the video is playing.  In short, the Facial Recognition integration has the ability to turn thousands of hours of video content into easily found information for your viewers easily and quickly.

## Requirements

* You must have a **Rev AI license** and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available to use Facial Recognition feature(s).
* Facial Recognition is _disabled_ by default and must be enabled.
* A valid profile picture is required. Users may decide to opt-out at any time, even if this functionality is enabled, by updating their [Profile Settings](doc:your-rev-profile).

## Configuration

To enable Facial Recognition:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Select the **Allow tagging of users in a video using profile pictures** checkbox next to the **Enable Facial Recognition** label. If this checkbox is not visible, **Rev AI Hours** licensing must be purchased and applied first.

3. Click **Save Changes**.

* Rev builds a search index based on profile pictures that are uploaded. This index is updated continuously to account for additions and deletions to profile pictures.
* Rev "predicts" the speakers that appear in a given video (based on profile pictures of those users that have not opted-out or deleted their profile image).
* Search and filter capabilities to find and filter videos with tagged users.
* Bulk editing options to append, replace, and remove tagged users.

## Usage

### Automated User Tagging

A [Tag Users in this Video](doc:tag-users-in-a-video) button is now visible on the **In this Video** form in **Video Settings**. When clicked, Rev automatically tags users found in the video in place of using the **Find Items** control to manually tag users. If **Facial Recognition** is disabled, individuals must be _manually_ tagged once more using **Find Items**.

<Image align="center" alt={447} border={false} caption="The Tag Users In This Video button automates the tagging process by finding the users in the video for you. But only when Facial Recognition is enabled." title="inThisVideoButton.png" src="https://files.readme.io/aaf3af9-tagUsers.png" />

> ❗️ Warning!
>
> In This Video tagging does _not_ function with **Live** videos (although it will function with video conferenced sourced recordings afterwards). Transcoding _must_ be completed on VOD videos before you may tag them. Larger videos may not be automatically tagged at this time due to technical limitations (2+ hours long / 8GB +).

### Interactive Rev Player Flyout Panel Functions

The [Video Information](doc:rev-video-player-features#video-information) flyout panel features timeline tagging notated by an **arrow >** next to each profile picture.

Clicking the profile image highlights where the speaker appears in the video on the video player playback bar. **Note**: Profile images are still displayed here even if Facial Recognition is not activated though they are not active and/or clickable.

<Image align="center" alt={322} border={false} caption="Profile pictures with an arrow next to them may be clicked to display where this person appears in the video when Facial Recognition is enabled" title="videoBasicInfoFlyout.png" src="https://files.readme.io/d09cf4f52beb893aec80f91e02a8b248b9abef90f39b985005fb0176f769fafa-inThisVideoTag.png" />

The [Transcript](doc:rev-video-player-features#video-transcript) flyout panel on the video player now displays and highlights each user's profile image as they appear (notated by an **arrow >** next to each profile picture) along with audio transcript highlighting (if SRT file is uploaded) _in real-time_.

Clicking the profile image highlights _where_ on the playback timeline the speaker appears.  **Note**: Profile images are still displayed on the panel even if Facial Recognition is not activated though they are not interactive and they do not highlight in real-time along with the audio.

<Image align="center" alt={392} border={false} caption="Each profile picture highlights in real-time along with the audio transcript on the Transcript flyout when Facial Recognition is enabled" title="interactivePulse.png" src="https://files.readme.io/8243a1ff3930419f84f02053257b69c5b2191d5b22eb10672e3ff34597a0ce9c-transcriptSpeakerHighlight.png" />

> 🚧 Important!
>
> Remember, users may always opt-out of Facial Recognition by modifying their Profile Settings even when it is active.  This may affect some results.
