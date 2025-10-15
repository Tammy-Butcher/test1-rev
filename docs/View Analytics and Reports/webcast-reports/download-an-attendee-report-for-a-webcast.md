---
title: Download an Attendee Report for a Webcast
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
Once the Webcast has ended, you may download details about attendees. The log is placed in your Downloads folder as a CSV file and includes the name of your event.

> 🚧 Important!
>
> If the **Hide User-Level Analytics** checkbox is enabled under [Content Restrictions](doc:hide-user-level-analytics), neither the **Attendees** nor the **Vbrick Peer-to-Peer** CSV file exports will be available for download, including to Admin accounts.

To include pre-production data in your report download, click the **Attendees - CSV (With Pre-Production Events)** link. Otherwise, clicking the **(Main Event)** link only includes production webcast data.

> 📘 Note
>
> There may be cases where attendee data in the CSV is not fully available:
>
>    a. An attendee was not in an active zone\
>    b. An attendee left the event prior to the start of broadcasting
>
> You can preview this data on the **Webcast Analytics Dashboard** under the [Users](doc:view-webcast-analytics#users) tab.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Metric
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        User Type
      </td>

      <td>
        * \*Internal/Registered Guest/Guest\*\*.  

        Specifies if the user is an internal system user account, a user who registered with an email account, an anonymous guest.
      </td>
    </tr>

    <tr>
      <td>
        Name
      </td>

      <td>
        Attendee’s **First Name** / **Last Name**  

        This is left blank for **anonymous** attendees.
      </td>
    </tr>

    <tr>
      <td>
        Username
      </td>

      <td>
        The Rev **Account** log in.  

        For Public **Registered Guest** attendees, this is a concatenation of name + email address.  

        For anonymous **Guest** Public attendees, this is a randomly generated 6-character name beginning with Guest-xxxxxx.
      </td>
    </tr>

    <tr>
      <td>
        UserID
      </td>

      <td>
        The Rev internal unique ID for the user consuming the webcast. This is auto-generated for Public/external attendees when they authenticate.
      </td>
    </tr>

    <tr>
      <td>
        Email Address
      </td>

      <td>
        Valid **Email**address of the user.  

        This is left blank for **anonymous** attendees.
      </td>
    </tr>

    <tr>
      <td>
        Session ID
      </td>

      <td>
        The Rev internal unique ID for the web session. This is a concatenation of the webcast GUID and the run number (0 for the Main Event, 1 for Pre-Production).  

        A new session ID is only generated for the same user if a new authorization token is generated. For example, if the user logs out and logs back in or switches devices.
      </td>
    </tr>

    <tr>
      <td>
        Zone Name
      </td>

      <td>
        The **Zone Name** that the attendee was assigned to based on their IP Address and the account zone configuration. This is useful for determining what device and stream the attendee was viewing and spotting patterns among attendees of the same zone.  

        * \*Not&#x65;**:  If there are no matching streams within the  Zone a viewer is assigned (or within any existing hierarchy of Zones from that Zone) the system provisions playback from the Default Zone.  If this happens, the CSV will identify**Default Zone\*\* in this field.
      </td>
    </tr>

    <tr>
      <td>
        IP Address
      </td>

      <td>
        The **IP Address** of the user consuming the webcast.
      </td>
    </tr>

    <tr>
      <td>
        Browser
      </td>

      <td>
        The type of browser/user agent that the user was using when consuming the webcast such as Firefox, Chrome, IE and so forth. Note that this is the browser that the session was registered on, not the browser version which can be found in the **User Agent** string.
      </td>
    </tr>

    <tr>
      <td>
        Vbrick Peer-to-Peer User Data
      </td>

      <td>
        The following fields are included for all Vbrick Peer-to-Peer events:  

        * Peer Cluster (Zone-: "Metric - ,\
            "h-1": - Description") - displays the last one the user was in.
        * Origin URL
        * Peer Mesh GUID
        * Peer Mesh Shares Out
        * Peer Mesh Shares In
        * Origin Gets
        * Time In
        * Time Out
        * Total Segments In
        * Peering Bytes Saved
        * Peering Efficiency
        * Viewer Peer Mesh Efficiency
        * Viewer Peer Mesh Origin Load
        * Viewer Peer Mesh Samaritan Load
        * Mesh Peer Mesh Share Efficiency
        * Mesh Peer Mesh Origin Efficiency If the user was not a member of a peer mesh, these fields are blank.
      </td>
    </tr>

    <tr>
      <td>
        Device Type
      </td>

      <td>
        PC or Mobile
      </td>
    </tr>

    <tr>
      <td>
        User Agent
      </td>

      <td>
        The specific **Browser/User Agent**version used such as Windows NT 6.1, Chrome 75, Safari 537.36, etc.
      </td>
    </tr>

    <tr>
      <td>
        Platform/Platform Version
      </td>

      <td>
        Platform is the generic Operating System *type* used (such as Windows, MacOS, Android, and so forth) while Platform Version is the specific Operating System *version* used (such as Windows 10, macOS 10.14 Mojave, Android 9.0).
      </td>
    </tr>

    <tr>
      <td>
        Attendee Type
      </td>

      <td>
        Last known **Role**of the user: Host, Moderator, Attendee, Account Admin.  

        Note: This column will be blank if this is an old webcast.
      </td>
    </tr>

    <tr>
      <td>
        Session Start Time
      </td>

      <td>
        * When\_ the Attendee enters the webcast regardless if it is broadcasting or not.
      </td>
    </tr>

    <tr>
      <td>
        Stream Start Time
      </td>

      <td>
        The first time an Attendee *receives* a stream during a Live event.
      </td>
    </tr>

    <tr>
      <td>
        Exit Time
      </td>

      <td>
        When an attendee leaves the event or is disconnected for more than 5 minutes or if the event is ended by the Event Host and is not restarted.  

        Note: If the attendee *disconnects* instead of leaving the webcast, the **Exit Time** will be the last known event for that attendee (usually the last heartbeat received from the player.
      </td>
    </tr>

    <tr>
      <td>
        Viewing Time
      </td>

      <td>
        The total viewing time from **Stream Start Time** to **Exit Time** in HH:MM format. If the time is shorter than the **Webcast Time**, this indicates that the Attendee left the event early.
      </td>
    </tr>

    <tr>
      <td>
        Session Time
      </td>

      <td>
        Total time from **Session Start Time** to **Exit Time** in HH:MM format. If the time is shorter than the **Webcast Time**, this indicates the Attendee left the event early.
      </td>
    </tr>

    <tr>
      <td>
        Number of Buffering Events
      </td>

      <td>
        Displays the total count of buffering events the user experienced during the webcast. Buffering events are an indication that the video player buffered some amount of the stream.  

        Note that while the number of buffering events does include all negligible buffering events which are defined as being less than 500 milliseconds (configurable), it does not include the initial buffering events.
      </td>
    </tr>

    <tr>
      <td>
        Number of Rebuffering Events
      </td>

      <td>
        Rebuffering events are those defined buffering events that affect a user with a visible “spinner”. The spinner appears 500ms (configurable) after the buffering event starts. This count is a subset of the number of total buffering events.
      </td>
    </tr>

    <tr>
      <td>
        Rebuffering Duration
      </td>

      <td>
        The cumulative amount of rebuffering duration experienced by a user in seconds.
      </td>
    </tr>

    <tr>
      <td>
        Removed
      </td>

      <td>
        Marked **TRUE**or **FALSE**and indicates if an attendee was removed from the webcast by a Host or Admin.
      </td>
    </tr>

    <tr>
      <td>
        Experienced Errors
      </td>

      <td>
        How often attendee views a player error message with no fallback options in place.
      </td>
    </tr>

    <tr>
      <td>
        Start Time (of the webcast)
      </td>

      <td>
        The time that the Event Host initiated the webcast (not necessarily the defined Start Time in set up).
      </td>
    </tr>

    <tr>
      <td>
        Event Type (Main Event versus Pre-Production)
      </td>

      <td>
        Attendees will have a different session ID for the Main Event and for Individual Pre-Production Runs (i.e., separate lines in the CSV download).
      </td>
    </tr>

    <tr>
      <td>
        Custom Registration Field(s)
      </td>

      <td>
        If defined, will appear before each source device column along with the data collected for each.  

        Note: These columns only appear for **Public**webcasts that are using custom registration fields. The columns are dynamic depending on how many custom registration fields are selected. These apply to Registered Guest users only. The fields will be empty for internal users and anonymous attendees.
      </td>
    </tr>

    <tr>
      <td>
        Device (1..n)
      </td>

      <td>
        The name of the source device(s) for the content stream. Each time an attendee’s player connects to a stream, these columns will list the source device of the stream, the playback URL, the time the playback started, and the type of the event.
      </td>
    </tr>

    <tr>
      <td>
        Poll (1...n)
      </td>

      <td>
        For each poll published, two columns are created that contain the Poll question, the response date/time for the question, and validation of the responses.  Attendee's responses for each question are the rows under the question(s).
      </td>
    </tr>
  </tbody>
</Table>

For each playback device/stream(1..n), there will be a playback URL and start time column and an indicator if a Vbrick Peer-to-Peer mesh is used.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Device(1..n)
      </th>

      <th>
        Attributes
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Device 1
      </td>

      <td>
        * \*Device Name\*\* - Source device of the stream. This could be a DME or CDN device.
      </td>
    </tr>

    <tr>
      <td>
        Playback1 URL
      </td>

      <td>
        Direct playback **URL**for the stream that was accessed. Use for determining what type of stream was being viewed (multicast, unicast, HLS, etc.)
      </td>
    </tr>

    <tr>
      <td>
        Playback Started1
      </td>

      <td>
        The time the that the playback was started using UTC date:time format.
      </td>
    </tr>

    <tr>
      <td>
        Type1
      </td>

      <td>
        The **type**of event that occurred.  

        * **Initial** - When the attendee’s player first accesses the stream, including exiting and rejoining the Webcast or when the Event Host starts broadcasting.
        * **AutoSwitch** - When the current stream fails for some reason and the Player automatically falls back to the next available streams, including Multicast Failover.
        * **ManualSwitch** - When the attendee manually uses the stream selector option on the Player to switch to a different stream (if configured with multiple options).
      </td>
    </tr>

    <tr>
      <td>
        Vbrick Peer-to-Peer
      </td>

      <td>
        True/False
      </td>
    </tr>
  </tbody>
</Table>
