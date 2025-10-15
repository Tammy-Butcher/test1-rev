---
title: Facial Recognition
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
  <li>&#128736; <a href="/docs/rev-ai">Rev IQ Module</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

**Facial Recognition** extends the functionality of Rev's manual user tagging in a video so that users can automate the process.  It also extends the interactive functionality of the [Video Basic Information](doc:rev-video-player-features#video-basic-information) and [Video Pulse](doc:rev-video-player-features#video-pulse) flyout panel(s) on the Rev video player so that viewers can see *who* is in a video and *what* is being said (in real-time) as the video is playing.  In short, the Facial Recognition integration has the ability to turn thousands of hours of video content into easily found information for your viewers easily and quickly.

## Requirements

* You must have a **Rev AI license** and [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available to use Facial Recognition feature(s).
* Facial Recognition is *disabled* by default and must be enabled. 
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

A [Tag Users in this Video](doc:tag-users-in-a-video) button is now visible on the **In this Video** form in **Video Settings**. When clicked, Rev automatically tags users found in the video in place of using the **Find Items** control to manually tag users. If **Facial Recognition** is disabled, individuals must be *manually* tagged once more using **Find Items**.

<Image title="inThisVideoButton.png" alt={447} align="center" src="https://files.readme.io/aaf3af9-tagUsers.png">
  The Tag Users In This Video button automates the tagging process by finding the users in the video for you. But only when Facial Recognition is enabled.
</Image>

> ❗️ Warning!
>
> In This Video tagging does *not* function with **Live** videos (although it will function with video conferenced sourced recordings afterwards). Transcoding *must* be completed on VOD videos before you may tag them. Larger videos may not be automatically tagged at this time due to technical limitations (2+ hours long / 8GB +).

### Interactive Rev Player Flyout Panel Functions

The [Video Basic Information](doc:rev-video-player-features#video-basic-information) flyout panel now features timeline tagging notated by an **arrow >** next to each profile picture. 

Clicking the profile image highlights where the speaker appears in the video on the video player playback bar. **Note**: Profile images are still displayed here even if Facial Recognition is not activated though they are not active and/or clickable.

<Image title="videoBasicInfoFlyout.png" alt={322} align="center" src="https://files.readme.io/9d5757b-videoBasicInfoFlyout.png">
  Profile pictures with an arrow next to them may be clicked to display where this person appears in the video when Facial Recognition is enabled
</Image>

The [Pulse](doc:rev-video-player-features#video-pulse) flyout panel on the video player now displays and highlights each user's profile image as they appear (notated by an **arrow >** next to each profile picture) along with audio transcript highlighting (if SRT file is uploaded) *in real-time*.

Clicking the profile image highlights *where* on the playback timeline the speaker appears.  **Note**: Profile images are still displayed on the panel even if Facial Recognition is not activated though they are not interactive and they do not highlight in real-time along with the audio.

<Image title="interactivePulse.png" alt={392} align="center" src="https://files.readme.io/bbd787b-interactivePulse.png">
  Each profile picture highlights in real-time along with the audio transcript on the Pulse flyout when Facial Recognition is enabled
</Image>

> 🚧 Important!
>
> Remember, users may always opt-out of Facial Recognition by modifying their Profile Settings even when it is active.  This may affect some results.
