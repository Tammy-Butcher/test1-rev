---
title: Webcast Report Downloads
excerpt: >-
  This guide provides information on the various reports that are available for
  download once a webcast has concluded
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
Event Admins, Hosts, and Moderators can download and view reports about a webcast once it has concluded by clicking the **Reports** tab and then the **Download** button on [The Webcast Landing Page](doc:the-webcast-landing-page). This includes attendee data and [Attendee Engagement](doc:attendee-engagement) feature results.

> 📘 Note
>
> You may need to specify which reports you want to view; **Main Event** or **Pre-Production Event** if you run each type of webcast.

<Image title="downloadsMenu.png" alt={356} align="center" src="https://files.readme.io/943352a-downloadsMenu.png">
  The Download button provides access to all reports generated from the webcast.  If a feature is not enabled, a report is not generated.
</Image>

> 🚧 Important!
>
> If the **Hide User-Level Analytics** checkbox is enabled under [Content Restrictions](doc:hide-user-level-analytics), neither the **Attendees** nor the **Vbrick Peer-to-Peer** CSV file exports in the image above will be available for download, including to Admin accounts.

## Download the Chat Log

Clicking **Download** > **Chat** downloads all **Chat** comments that occurred during a webcast once the event has ended.  The log is placed in your Downloads folder as **comments.txt** and may be opened with any text editor such as Notepad.

## Download the Q\&A Log

Clicking **Download** > **Questions & Answers** downloads all Q\&A submissions and results that occurred during a webcast once the event has ended.  The log is placed in your Downloads folder as **questions.csv**.

The Q\&A log contains:

* Date and timestamp when the question was received
* Question body
* User submitting the question (Full name and user name - for example, Tammy Butcher - tbutcher). Or Anonymous if applicable.
* Status of the question (none, answered, follow-up, declined, replied)
* Moderator direct reply text (if applicable)
* Moderator that replied to the question (Full name). If multiple moderators responded, the last moderator is included in the output file.

## Download Poll Results

Clicking **Download** > **Polls - CSV** downloads all Q\&A submissions and results that occurred during a webcast once the event has ended.  The log is placed in your Downloads folder as **polls.csv**.

The poll.csv contains:

* Event name
* Total number of attendees
* Poll question and all available responses
* Attendee's response to poll question(s) if not anonymous
* Total number of respondents to the poll
* Total number of attendees that did not respond
* If the poll allowed multiple answers
* Number of responses per answer

## Download Attendee Data

Clicking **Download** > **Attendees - CSV** downloads details about all attendees once a webcast has ended.  The log is placed in your Downloads folder as **RevConnectAttendees.csv** or **WebcastAttendees**.csv.

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

        * \*Not&#x65;**:  If there are no matching streams within the  Zone a viewer is assigned (or within any existing hierarchy of Zones from that Zone) the system provisions playback from the Default Zone.  If this happens, the CSV will identify**DefaultZone\*\* in this field.
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

        * Peer Cluster (Zone-: "Metr - ,\
            "h-1": - escription") - displays the last one the user was in.  
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
        * Mesh Peer Mesh Origin Efficiency  

        If the user was not a member of a peer mesh, these fields are blank.
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

## Download Vbrick Peer-to-Peer Zone Metrics

Clicking **Download** > **Vbrick Peer-to-Peer - CSV** downloads details about Vbrick Peer-to-Peer zones once the event has ended but only if they are enabled for the event.  If no zones are [Vbrick Peer-to-Peer enabled](doc:rev-connect-zones), this option is not visible.

Each line within the Vbrick Peer-to-Peer report represents one user within a Peer Mesh. In most cases, users join a single **Peer Mesh** for an entire event and, therefore, there is only one entry. However, if a user joins or rejoins one or more Peer Meshes, a line is added for each instance. This provides different user experiences based on membership in different Peer Meshes available to the analyst during review. The **UserID** should be used for grouping information about specific Users – and UserID is the same and used for correlation to the [Webcast Event Attendees](doc:webcast-reports#download-attendee-metrics) report.

If viewed as a table (as in Excel), the first set of columns focus on the **User** (or viewer) characteristics. They include:

* Attendee Full Name (First Name / Last Name)
* Account Username
* UserID
* Email Address
* Session ID
* Zone Name
* IP Address
* Browser Used
* Origin URL

<hr>

Columns after User characteristics focus on **Peer Mesh** data. They include:

**Peer Mesh GUID** - The Peer Mesh GUID is an unique ID representing a Peer Mesh. During analysis, this item can be used in a number of ways to:

* Identify how many Peer Meshes were in this event (by counting unique Peer Mesh GUIDs)
* Identify the timing life cycle of the Peer Mesh with start of this Peer Mesh (earliest Time In) and the end of the Peer Mesh (latest Time Out)
* Grouping within Peer Mesh for analysis of:
* Review User IPs for validation of the Peer Mesh membership (defined within the Zone settings for Peer Mesh)
* Compare Peer Mesh metrics (defined below)

<hr>

**Peer Mesh Shares Out** (number of segments that this viewer provide to another peer)

This is the number of segments that this viewer, in this particular Peer Mesh, has shared to another peer. Higher number represents more sharing. Higher numbers are not necessarily good nor bad, but should be considered if a user is sharing too much. The Samaritan Load measure below expands on this and provides a consistent way to compare different users and their sharing behavior.

<hr>

**Peer Mesh Shares In** (number of segments that this viewer gets from another peer)

This is the number of segments that this viewer got from another another peer. Higher numbers represent getting more shares from peers and a better use of bandwidth.

<hr>

**Origin Gets**

This is the number of segments that this viewer has gone to origin (i.e., not a peer) to retrieve. While it is important that this number be low, it should also be realized that “someone” (some viewer) will have to go to origin to get it. This should always be evaluated in reference to Peer Mesh Shares Out, Peer Mesh Shares In and Total Segments. Having one (or a few) peers bear the load of many Origin Gets is not necessarily indicative of a problem.

<hr>

**Time In**

This is the time viewer enters this Peer Mesh. Viewers may be assigned to different Peer Meshes across an event, so please use this value with Time Out and all analysis should look for multiple entries per user.

<hr>

**Time Out**

Like Time In, This is the time viewer leaves this Peer Mesh. Viewers may be assigned to different Peer Meshes across an event, so please use this value with Time In and all analysis should look for multiple entries per user.

<hr>

**Total Segments In**

This is the number of segments that the viewer requested within the peer mesh. This is the number of **Peer Mesh Shares In** (how many they get from other peers) + **Origin Gets** (this is the number of origin retrievals).

<hr>

The following calculated percentages provide an insight to where (in percentage) the current user (within the peer mesh) is getting content (either via sharing from peers or going to origin), and how much user is sharing. While these are meaningful at the viewer level, they should not be used for an indication of the efficiency across the peer mesh.

**Viewer Peer Mesh Efficiency (Peer Mesh Shares In / Total Segments In)\* 100**

This is a viewer specific calculated measure. It represents the ratio/percentage of **Peer Mesh Shares In** (number of segments this viewer gets from peers) to the **Total Segments In** (total number of segments played, in from peers + origin gets).

In other words: This is the percentage of segments that a viewer got from a peer.

* The higher the value, the more that this viewer is using the peer mesh to get content. The lower the value, the more this viewer is going to origin.

<hr>

**Viewer Peer Mesh Origin Load (Origin Gets / Total Segments In)\* 100** 

This is a viewer specific calculated measure, and the flip side of the Viewer Peer Mesh Efficiency. Meaning **Viewer Peer Mesh Origin Load** + **Viewer Peer Mesh Efficiency** = 100%.

This number represents the ratio/percentage of **Origin Gets** (number of segments this viewer goes to origin for) to the **Total Segments In** (total number of segments played, in from peers + origin gets).

In other words: This is the percentage of segments that a viewer needed to go to origin.

* The higher the value, the more this viewer is going to origin. The lower the value, the more that this viewer is using the peer mesh to get content.

<hr>

**Viewer Peer Mesh Samaritan Load (Peer Mesh Shares Out / Total Segments In )\* 100** 

This is a viewer specific calculated measure. It represents the ratio of how many times this user has shared with other peers to the total number of segments. This provides a quantitative measure to “How actively does this viewer share?” or “How good a Samaritan is this viewer in this Peer Mesh?”

This number represents the ratio of **Peer Mesh Shares Out** (how many times this user shared to another peer) to **Total Segments In** (total segments that could be shared, Shares IN + Origin Gets). This measure is provided as a ratio/percentage, but can be > 100%.

In other words: This is the percentage of how often this viewer shares to peers.

* Higher numbers mean this viewer is sharing more (supplying segments to more peers.) Lower numbers represent a lack of sharing from this peer.

<hr>

The next set of calculated measures represent Peer Mesh wide characteristics. These are common/duplicated across each User within the Peer Mesh. Meaning, these measures will be the same for all Users within a particular Peer Mesh, and are provided in this manner for direct comparison to the Viewer specific measures identified above.

**Mesh Peer Mesh Share Efficiency = ( Sum(Peer Mesh Shares In) / Sum(Total Segments In))** 

This is a Peer Mesh specific calculated measure. It represents the ratio of how many times all the users got segments from peers to the total number of segments for all users. This provides a quantitative measure to “Is this Peer Mesh sharing efficiently?”

In other words: This percentage represents how often we are sharing.

* Higher numbers mean better sharing within this Peer Mesh. Target should be > 90%. Lower numbers represent a lack of sharing within this Peer Mesh.

Do not confuse **Viewer Peer Mesh Efficiency** with **Mesh Peer Mesh Share Efficiency**. Each metric identifies scope by the first word, either Viewer (the single viewer) or Mesh (the single Peer Mesh) scope.

<hr>

**Mesh Peer Mesh Origin Efficiency = ( Sum(Origin Gets) / Unique (Origin Gets) )\* 100** 

This is a Peer Mesh specific calculated measure that spans each Cluster. It represents the ratio of how many times (across all the users) there were origin retrievals for a segment to the number of unique segments. This provides a quantitative measure to “Is this the Peer Mesh Cluster going to origin too much?”

In other words: This ratio  represents the number of times we go to origin to get segments against all unique segments for all Peers in Peer Meshes in individual Clusters.

For example, if the metric is 100 – that means we only ever go to origin once per segment (i.e., All Origin Gets == Unique Origin Gets). This implies that the users share that segment optimally between each other within the Peer Mesh (because, otherwise, there would be additional Origin Gets).  

For a Peer Mesh Cluster size of 1, 100 is the optimal result, but rarely achievable due to inherent timing between communicating peers.  For this Cluster size, we strive for an efficiency value of 100-125.  (Meaning, if the metric is 125, this equates to, on average, going to origin 5 times for 4 unique segments.)

For larger Cluster sizes (up to 10), the **Mesh Peer Mesh Origin Efficiency**  could vary more, and lower is better.  But event larger numbers, with multiple Peer Meshes, represents savings.  For example, if you have 10 Peer Meshes non-clustered, then the best measure would be 100 per Peer Mesh -- or, going to origin once per TS segment for each Peer Mesh (sharing across all viewers within mesh).  If those Peer Meshes were clustered, but still have the same go to origin, then the  **Mesh Peer Mesh Origin Efficiency** would equate to 1000.  In practice, anything below that would indicate savings, and our tests often come in around 100-200 for larger Cluster sizes.  Said another way, a measure of 200 is going to origin twice to service your multiple Peer Meshes -- which for 3 or more Peer Meshes is added bandwidth savings.

**Guidance**: 

* If Peer Mesh Cluster size = 1, then strive for **Mesh Peer Mesh Origin Efficiency** value of 100-125
* For larger Cluster size N, then strive for **Mesh Peer Mesh Origin Efficiency** value of (100-125)\*N/2

**Are higher values bad?** Higher values indicate more origin gets across all users, and hence more bandwidth used. High values of this metric are most impactful on Peer Meshes or Peer Mesh Clusters that exist on networks with reduced or restricted bandwidth. Networks with additional bandwidth can service more origin calls on average.

**How do I effect change on Mesh Peer Mesh Origin Efficiency?** There are multiple reasons why this metric could be driven up, and if most often unique per network. A primary cause is network induced latency between Peer Mesh constituents/viewers. A large latency between communicating peers will time-out resulting in more requests driven to origin.

Examine your Vbrick Peer-to-Peer membership rules on the Zones page. Only allow Peer Meshes to be comprised of “close” (restricted to a small geographical/network grouping) viewers.  Remember that mDNS is used by Browsers that are obfuscating address cannot share across sub-nets -- which would also reduce your efficiency. 

Consider the size and structure of your HLS stream. Smaller segment sizes, while reducing latency, increase the communication load across all peers and the network. Larger sizes allow for more time to communicate between peers.

Do not confuse **Viewer Peer Mesh Origin Load** with **Mesh Peer Mesh Origin Efficiency**. Each metric identifies scope by the first word, either Viewer (the single viewer) or Mesh (the single Peer Mesh) scope.

<hr>

**Peering efficiency (Percent of Bytes Saved/ 1- Network Consumption for the user in the event)** 

This includes:

* Peer Cluster (Zone-\[group] - \[clusterset] - \[clusterid]) - displays the last one the user was in.
* Peering Shares Sent
* Peering Shares Received
* Peering Origin Gets
* Total Peering Segments (Total Segments In or Peering Shares Received plus Origin Gets)
* Peering Bytes Saved (For the user in that event) 

If the user was not a member of a peer mesh, these fields are blank.
