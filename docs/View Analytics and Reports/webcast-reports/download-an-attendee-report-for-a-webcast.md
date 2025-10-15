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
>    a. An attendee was not in an active zone  
>    b. An attendee left the event prior to the start of broadcasting
> 
> You can preview this data on the **Webcast Analytics Dashboard** under the [Users](doc:view-webcast-analytics#users) tab.

[block:parameters]
{
  "data": {
    "h-0": "Metric",
    "h-1": "Description",
    "0-0": "User Type",
    "0-1": "**Internal/Registered Guest/Guest**.  \n  \nSpecifies if the user is an internal system user account, a user who registered with an email account, an anonymous guest.",
    "1-0": "Name",
    "1-1": "Attendee’s **First Name** / **Last Name**  \n  \nThis is left blank for **anonymous** attendees.",
    "2-0": "Username",
    "2-1": "The Rev **Account** log in.  \n  \nFor Public **Registered Guest** attendees, this is a concatenation of name + email address.  \n  \nFor anonymous **Guest** Public attendees, this is a randomly generated 6-character name beginning with Guest-xxxxxx.",
    "3-0": "UserID",
    "3-1": "The Rev internal unique ID for the user consuming the webcast. This is auto-generated for Public/external attendees when they authenticate.",
    "4-0": "Email Address",
    "4-1": "Valid **Email **address of the user.  \n  \nThis is left blank for **anonymous** attendees.",
    "5-0": "Session ID",
    "5-1": "The Rev internal unique ID for the web session. This is a concatenation of the webcast GUID and the run number (0 for the Main Event, 1 for Pre-Production).  \n  \nA new session ID is only generated for the same user if a new authorization token is generated. For example, if the user logs out and logs back in or switches devices.",
    "6-0": "Zone Name",
    "6-1": "The **Zone Name** that the attendee was assigned to based on their IP Address and the account zone configuration. This is useful for determining what device and stream the attendee was viewing and spotting patterns among attendees of the same zone.  \n  \n**Note**:  If there are no matching streams within the  Zone a viewer is assigned (or within any existing hierarchy of Zones from that Zone) the system provisions playback from the Default Zone.  If this happens, the CSV will identify **Default Zone** in this field.",
    "7-0": "IP Address",
    "7-1": "The **IP Address** of the user consuming the webcast.",
    "8-0": "Browser",
    "8-1": "The type of browser/user agent that the user was using when consuming the webcast such as Firefox, Chrome, IE and so forth. Note that this is the browser that the session was registered on, not the browser version which can be found in the **User Agent** string.",
    "9-0": "Vbrick Peer-to-Peer User Data",
    "9-1": "The following fields are included for all Vbrick Peer-to-Peer events:  \n  \n- Peer Cluster (Zone-: \"Metric - ,  \n    \"h-1\": - Description\") - displays the last one the user was in.\n- Origin URL\n- Peer Mesh GUID\n- Peer Mesh Shares Out\n- Peer Mesh Shares In\n- Origin Gets\n- Time In\n- Time Out\n- Total Segments In\n- Peering Bytes Saved\n- Peering Efficiency\n- Viewer Peer Mesh Efficiency\n- Viewer Peer Mesh Origin Load\n- Viewer Peer Mesh Samaritan Load\n- Mesh Peer Mesh Share Efficiency\n- Mesh Peer Mesh Origin Efficiency If the user was not a member of a peer mesh, these fields are blank.",
    "10-0": "Device Type",
    "10-1": "PC or Mobile",
    "11-0": "User Agent",
    "11-1": "The specific **Browser/User Agent **version used such as Windows NT 6.1, Chrome 75, Safari 537.36, etc.",
    "12-0": "Platform/Platform Version",
    "12-1": "Platform is the generic Operating System _type _ used (such as Windows, MacOS, Android, and so forth) while Platform Version is the specific Operating System _version_ used (such as Windows 10, macOS 10.14 Mojave, Android 9.0).",
    "13-0": "Attendee Type",
    "13-1": "Last known **Role **of the user: Host, Moderator, Attendee, Account Admin.  \n  \nNote: This column will be blank if this is an old webcast.",
    "14-0": "Session Start Time",
    "14-1": "_When_ the Attendee enters the webcast regardless if it is broadcasting or not.",
    "15-0": "Stream Start Time",
    "15-1": "The first time an Attendee _receives_ a stream during a Live event.",
    "16-0": "Exit Time",
    "16-1": "When an attendee leaves the event or is disconnected for more than 5 minutes or if the event is ended by the Event Host and is not restarted.  \n  \nNote: If the attendee _disconnects_ instead of leaving the webcast, the **Exit Time** will be the last known event for that attendee (usually the last heartbeat received from the player.",
    "17-0": "Viewing Time",
    "17-1": "The total viewing time from **Stream Start Time** to **Exit Time** in HH:MM format. If the time is shorter than the **Webcast Time**, this indicates that the Attendee left the event early.",
    "18-0": "Session Time",
    "18-1": "Total time from **Session Start Time** to **Exit Time** in HH:MM format. If the time is shorter than the **Webcast Time**, this indicates the Attendee left the event early.",
    "19-0": "Number of Buffering Events",
    "19-1": "Displays the total count of buffering events the user experienced during the webcast. Buffering events are an indication that the video player buffered some amount of the stream.  \n  \nNote that while the number of buffering events does include all negligible buffering events which are defined as being less than 500 milliseconds (configurable), it does not include the initial buffering events.",
    "20-0": "Number of Rebuffering Events",
    "20-1": "Rebuffering events are those defined buffering events that affect a user with a visible “spinner”. The spinner appears 500ms (configurable) after the buffering event starts. This count is a subset of the number of total buffering events.",
    "21-0": "Rebuffering Duration",
    "21-1": "The cumulative amount of rebuffering duration experienced by a user in seconds.",
    "22-0": "Removed",
    "22-1": "Marked **TRUE **or **FALSE **and indicates if an attendee was removed from the webcast by a Host or Admin.",
    "23-0": "Experienced Errors",
    "23-1": "How often attendee views a player error message with no fallback options in place.",
    "24-0": "Start Time (of the webcast)",
    "24-1": "The time that the Event Host initiated the webcast (not necessarily the defined Start Time in set up).",
    "25-0": "Event Type (Main Event versus Pre-Production)",
    "25-1": "Attendees will have a different session ID for the Main Event and for Individual Pre-Production Runs (i.e., separate lines in the CSV download).",
    "26-0": "Custom Registration Field(s)",
    "26-1": "If defined, will appear before each source device column along with the data collected for each.  \n  \nNote: These columns only appear for **Public **webcasts that are using custom registration fields. The columns are dynamic depending on how many custom registration fields are selected. These apply to Registered Guest users only. The fields will be empty for internal users and anonymous attendees.",
    "27-0": "Device (1..n)",
    "27-1": "The name of the source device(s) for the content stream. Each time an attendee’s player connects to a stream, these columns will list the source device of the stream, the playback URL, the time the playback started, and the type of the event.",
    "28-0": "Poll (1...n)",
    "28-1": "For each poll published, two columns are created that contain the Poll question, the response date/time for the question, and validation of the responses.  Attendee's responses for each question are the rows under the question(s)."
  },
  "cols": 2,
  "rows": 29,
  "align": [
    "left",
    "left"
  ]
}
[/block]


For each playback device/stream(1..n), there will be a playback URL and start time column and an indicator if a Vbrick Peer-to-Peer mesh is used.

[block:parameters]
{
  "data": {
    "h-0": "Device(1..n)",
    "h-1": "Attributes",
    "0-0": "Device 1",
    "0-1": "**Device Name** - Source device of the stream. This could be a DME or CDN device.",
    "1-0": "Playback1 URL",
    "1-1": "Direct playback **URL **for the stream that was accessed. Use for determining what type of stream was being viewed (multicast, unicast, HLS, etc.)",
    "2-0": "Playback Started1",
    "2-1": "The time the that the playback was started using UTC date:time format.",
    "3-0": "Type1",
    "3-1": "The **type **of event that occurred.  \n  \n- **Initial** - When the attendee’s player first accesses the stream, including exiting and rejoining the Webcast or when the Event Host starts broadcasting.\n- **AutoSwitch** - When the current stream fails for some reason and the Player automatically falls back to the next available streams, including Multicast Failover.\n- **ManualSwitch** - When the attendee manually uses the stream selector option on the Player to switch to a different stream (if configured with multiple options).",
    "4-0": "Vbrick Peer-to-Peer",
    "4-1": "True/False"
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]