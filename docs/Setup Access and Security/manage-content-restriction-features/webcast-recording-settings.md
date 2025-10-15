---
title: Webcast Recording Settings
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
The **Webcast Recording** section determines how webcast and meeting recordings are handled and displayed in the portal. You can specify if it is allowed, required, or disabled entirely. Depending on the setting selected, Rev’s UI is modified in both events setup and in the upload tray **Recording** tab when recording video conferences.

For example, if webcast recording is set to required, the Event Host no longer needs to remember to click the **Record** button when broadcasting begins because Rev automatically records all webcasts. The **Webcast Recording** section in the event setup is no longer visible as a result.  How each setting affects the recording function and UI display is described in the table below.

<Image title="enableWebcastRecording.png" alt={502} align="center" src="https://files.readme.io/7f31f80-enableWebcastRecording.png">
  The Webcast Recording setting determines how webcast and meeting recordings are handled in Rev; the default setting is to allow recording.
</Image>

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Allow
      </th>

      <th>
        Disable
      </th>

      <th>
        Require
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Use this option to give Hosts a choice to record.
      </td>

      <td>
        Use this option to disable recording entirely.
      </td>

      <td>
        Use this option to have all webcasts begin recording automatically when Hosts begin broadcasting.
      </td>
    </tr>

    <tr>
      <td>
        The [Recording](doc:stream-and-record-video) tab in the video upload tray is visible.
      </td>

      <td>
        The [Recording](doc:stream-and-record-video) tab in the video upload tray is *not* visible.
      </td>

      <td>
        The [Recording](doc:stream-and-record-video) tab in the video upload tray is visible.
      </td>
    </tr>

    <tr>
      <td>
        Webcast recording is optional. The [Webcast Recording](doc:webcast-recordings) section in an event setup is visible.
      </td>

      <td>
        All webcasts are created with recording disabled. The [Webcast Recording](doc:webcast-recordings) section in an event setup is *not* visible.
      </td>

      <td>
        All webcasts are created with recording required and automatic. The [Webcast Recording](doc:webcast-recordings) section in an event setup is *not* visible.
      </td>
    </tr>

    <tr>
      <td>
        The **Automatic Recording** tab is visible during event setup.  

        * If disabled, the Event Host is able to manually start and stop recording the webcast.  

        * If the automatic recording tab is enabled, the webcast automatically begins recording when the Event Host begins broadcasting. The Host can choose to stop and start recording at any time.  

        * Automatic recording is enabled by default, but can also be set via a [template](doc:create-a-webcast-template).
      </td>

      <td>
        The [Record](doc:host-a-production-webcast#recording-the-webcast) button is *not* visible during a webcast.  

        * If a [template](doc:create-a-webcast-template) is applied with recording options set, it is overridden with recording options disabled.  
        * If an API user attempts to enable recording or start recording during a webcast, an error is generated.
      </td>

      <td>
        * As soon as the Event Host begins **Broadcasting**,  the webcast records automatically.  
        * If a [template](doc:create-a-webcast-template) is applied with recording options set, it is overridden with recording options required.  
        * If an API user attempts to disable recording during setup or stop recording during a webcast, an error is generated.
      </td>
    </tr>
  </tbody>
</Table>

> 🚧 Important!
>
> Some webcast video sources will disable and/or hide the **Webcast Recording** section of an event even if it is enabled in the **Webcast Recording Settings** described in this topic.  This includes using an [existing video](doc:video-sources#existing-video-sourced-events) as a video source.
