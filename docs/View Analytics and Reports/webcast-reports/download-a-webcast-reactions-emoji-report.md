---
title: Download a Webcast Reactions Emoji Report
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
Once the Webcast has ended, you may download a report that displays the **Reactions/Emojis** that were [used by attendees during the event](doc:add-live-emoji-reactions-to-a-webcast). The Reactions report lets you know exactly what reactions were used in the webcast and at what point. It includes the following columns in a csv file:

* Webcast time: The time segment in two second increments when the reaction is used.  Reflective of the account time zone.
* Reaction / emoji image
* Unicode for the reaction / emoji
* Count (number of time it was used during the event)

Example reactions log

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "left" }}>
        Webcast Time
      </th>

      <th style={{ textAlign: "left" }}>
        Reaction
      </th>

      <th style={{ textAlign: "left" }}>
        Unicode
      </th>

      <th style={{ textAlign: "left" }}>
        Count
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "left" }}>
        date/time
      </td>

      <td style={{ textAlign: "left" }}>
        :smiley:
      </td>

      <td style={{ textAlign: "left" }}>
        1F604
      </td>

      <td style={{ textAlign: "left" }}>
        150
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        date/time
      </td>

      <td style={{ textAlign: "left" }}>
        :smiley:
      </td>

      <td style={{ textAlign: "left" }}>
        1F604
      </td>

      <td style={{ textAlign: "left" }}>
        5
      </td>
    </tr>
  </tbody>
</Table>

To view a reaction log report:

1. Navigate to the [Webcast Landing](doc:the-webcast-landing-page) page again once the event has concluded and click the **Reports** > **Download** button.
2. Click the **Reactions CSV** option.
3. The log is placed in your Downloads folder as **Reactions.csv** (including the event name).
