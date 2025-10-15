---
title: Allow Webcast User Engagement Features
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
The **Webcast User Engagement** section under the **Admin** > **Media Settings** > **Features** menu option displays the attendee engagements that Account Admins can allow globally in Rev for use in webcast events by an **Event Host** during event setup.

> 🚧 Important
>
> If these settings are *disabled*, they are *not* be visible or selectable during event setup by an Event Host.

<Image align="center" src="https://files.readme.io/eeabde912bcd3e02dd0f328c6b522670971fa5d4b8327eefeb144f70a68240ce-webcastUserEngagementSection.png" />

<br />

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        User Engagement
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Allow Chat on Webcasts
      </td>

      <td>
        If you have the **Allow Chat on Webcasts** option checked, the [Enable Chat](doc:add-chat-to-a-webcast)  toggle becomes available during event setup. This allows Event Admins and Hosts to decide whether or not they want to add Rev’s Chat feature for attendees on their Webcast events.
      </td>
    </tr>

    <tr>
      <td>
        Allow Polls on Webcasts
      </td>

      <td>
        If you have the **Allow Polls on Webcasts** option checked, the [Enable Polls](doc:add-a-poll-to-a-webcast)  toggle becomes available during event setup. This allows Event Admins and Hosts to decide whether or not they want to add Poll functionality to their Webcast events for attendees to view and answer.
      </td>
    </tr>

    <tr>
      <td>
        Allow Q\&A on Webcasts
      </td>

      <td>
        If you have the **Allow Q\&A on Webcasts** option checked, the [Enable Q\&A](doc:add-qa-to-a-webcast)  toggle becomes available during event setup. This allows Event Admins and Hosts to decide whether or not they want Rev’s Q\&A features available on their Webcast events.
      </td>
    </tr>

    <tr>
      <td>
        Send a Message/Link (Banner) to all Attendees
      </td>

      <td>
        When you enable **Send a Message/Link (Banner) to all Attendees**, you add the ability for Events Admins and Hosts to [Add a Live Event Banner](doc:add-links-to-a-webcast)  to a webcast during event setup.  A scrollable webcast banner, including URLs, can be configured to overlay the event during a live webcast or to automatically appear once the event has concluded. If the banner is overlaid live during the webcast, it can be clicked and closed by attendees.
      </td>
    </tr>

    <tr>
      <td>
        Embed Content
      </td>

      <td>
        Displays embedding status for content. This settings is enabled or disabled in **System Settings** > **Content Restriction**.
      </td>
    </tr>

    <tr>
      <td>
        Allow moderators to expel users from a webcast
      </td>

      <td>
        If you have the **Allow moderators to expel users from a webcast** option checked, moderators are able to [remove and restore webcast attendees](doc:host-a-production-webcast#viewing-and-removing-attendees)  just as Event Admins and Event Hosts can. This setting is enabled by default.
      </td>
    </tr>

    <tr>
      <td>
        Allow Emoji Reactions in Webcast
      </td>

      <td>
        When you have the **Allow Emoji Reactions in Webcast** option checked, an Event Host can add the ability for attendees to [use reactions or emojis](doc:add-live-emoji-reactions-to-a-webcast) :smiley: during a Live event. This setting is enabled by default.  

        In addition to enabling reactions for use in events, the **Required seconds in between reaction submissions** can also be specified.  The default setting is 2 seconds.  This is so that you can control how frequently an attendee can react. For example, if you are running a webcast that has a very large number of attendees, you may want to bump this interval up so that the viewing window is not flooded with emojis.
      </td>
    </tr>
  </tbody>
</Table>
