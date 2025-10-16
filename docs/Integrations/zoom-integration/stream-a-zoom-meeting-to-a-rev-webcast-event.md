---
title: Stream a Zoom Meeting to a Rev Webcast Event
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
You can use a Zoom meeting as a **video source** for your Webcast event once you have installed and enabled the Zoom meeting Integration. When you select Zoom as a Video Source, starting your Rev Webcast event also starts your scheduled Zoom meeting.

This means you can take advantage of Rev’s Webcast functionality and pair it with the Zoom meeting. Afterward, you can then save the recording and use Rev’s video settings and metadata features.

> 👍 Tip
>
> You must be logged in to a Zoom Meeting account that has an email that **matches** the email being used in the Rev account for the Webcast Event setup.

To stream a Zoom meeting to a Rev webcast event:

1. Schedule the Rev event as you normally would. **View**: [Scheduled Webcasts](doc:webcast-listing-types-and-video-sources#scheduled-webcasts)

2. Select **Zoom** as the source in the [Video Sources](doc:video-sources)  section.

3. Configure the [DTMF](doc:dtmf-configuration-and-usage#use-dtmf-codes-in-events) codes you want to use with the event if any. (optional)

4. Enter a **Zoom meeting** or **Zoom meeting URL** in the source field.

> 📘 Note
>
> All previously scheduled Zoom meetings automatically appear in the Video Source drop-down. Meetings that are scheduled in the past do not appear.
>
> You may also enter a **Zoom Meeting ID** or **URL** if you do not have any meetings scheduled when you create your Webcast. The meeting ID requires a number between 9 and 11 digits.

5. If a password has been set for the Zoom meeting, you must enter the **H323/SIP numeric Password** for the meeting.

<Image align="center" alt={1157} border={false} caption="Once you have configured your Zoom Meeting in your Rev Webcast, starting the Rev Event also starts the Zoom Meeting" title="zoomWebcast.png" src="https://files.readme.io/9cfac73-zoomWebcast.png" />

6. Start the **Rev event** and the **Zoom meeting** when ready.  Starting the Rev event also starts the Zoom meeting although ideally the endpoint (Zoom meeting) should be started first before beginning your Rev meeting.

7. Once the Zoom meeting starts, an “Initializing” message appears in the Webcast window while Rev and Zoom connect. Note that initialization may take up to a minute for video from Zoom to display in Rev.

8. Once your Zoom conference video appears, you may begin broadcasting your event as you would any other Rev webcast.

9. You may end the event in either Rev or Zoom. The video appears in Rev with the **Zoom Meeting Name** if you choose to save the recording. You may modify its metadata and Video Settings as you would any other video.
