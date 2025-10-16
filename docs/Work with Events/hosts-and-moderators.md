---
title: Hosts and Moderators
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
## Choose an Event Host

Every webcast must have a designated **Event Host** to start and run it even if the [Listing Type](doc:create-event#understanding-event-listing-types) is **Private** or **Public**.  There may be up to three hosts assigned per webcast. An Event Host is typically selected during event set up and the event creator is the default host assigned.

> 🚧 Important!
>
> The **Event Host** role may _only_ control those events they are **assigned** to whereas Account Admin roles can control all events as needed. **Event Admin** roles can edit webcast settings but cannot start/stop the webcast.
>
> The **Event Host** role may _only_ **edit** those events they **create** whereas Account/Event Admin roles can edit all events as needed.
>
> This is an important distinction to keep in mind.
>
> **Event Moderator** [tasks and permissions](doc:roles-and-permissions#section-events) are different from those of an Event Host and they may only control event features such as polls and chat but do not control the event itself.

<Image align="center" alt={802} border={false} caption="Event Hosts who create an event can edit it or delete it; Event Hosts assigned to an event can control it." title="eventHost.png" src="https://files.readme.io/72d505d-eventHost.png" />

* Note that only accounts with the Event Admin, Event Host, or Account Admin [roles](doc:roles-and-permissions#section-events) appear in the **Event Host Find Items...** control and can be added as Event Hosts for an event
* All Event Hosts assigned are able to control the webcast slides if an Event Moderator has not been assigned (they may only edit the events they create)
* If the Event Host that creates the event is unable to reach the webcast, additional hosts or admins assigned may control the webcast
* If no Event Host or admin is able to reach the webcast, it is automatically ended on its own after 60 minutes of its scheduled end time

> ❗️ Warning!
>
> The Event Host added **first** is the “owner” of the event (and appears **last** as a result in the host list if more than one is added).
>
> In the example below, the Event Host “Tammy Butcher” is the actual owner of the event. Be aware of this if you add more than one host to your webcast and add the person you want to “own” the event first.

<Image align="center" alt={802} border={false} caption="The Event Host added first in Find Items is the “owner” of the event and appears last in the list; Tammy is this event's owner." title="hostOwner.png" src="https://files.readme.io/80674b8-hostOwner.png" />

## Choose Event Moderator(s)

**Event Moderators** are used to manage and control the “behind the scene” event features that have been set up by an Event Admin or Event Host such as [polls](doc:managing-webcast-polls) and [Q&A](doc:qa-module-management) sessions. This allows the Event Host(s) to focus on controlling the webcast itself.

For example, you may have an webcast where a large panel of speakers are presenting and several hundreds of attendees are expected. This type of event would expect to draw several questions at once during a Q&A session. A moderation team to manage the question queues and polls for the speakers would be the ideal set up in this case.

It is important to note that moderators are not able to modify or control the event _configuration _itself.

> 👍 Tip
>
> Unlike the Event Host, any user may be added as an Event Moderator. You do not have to be any certain functional role in Rev to be assigned as a moderator.
>
> Several Event Moderators may be assigned to an event while only 3 Event Hosts may be assigned at a time.

<Image align="center" alt={722} border={false} caption="When adding moderators, you can also designate those people who can control slides for you" title="eventModerators.png" src="https://files.readme.io/b883c45-eventModerators.png" />

* Designate a moderator to control the presentation slides (instead of the Event Host) by clicking the **Control Slides** tab. Only _one _moderator at a time may control the slides.
* The Control Slides button is only be visible after the moderator has been added by clicking the **Done** button first and saving the moderator to the event's configuration.

## Event Host Versus Event Moderator Tasks

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Event Host (Three per webcast)
      </th>

      <th>
        Event Moderator (Unlimited)
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Event Hosts are able to perform **all** the tasks of an Event Moderator

        They can also:

        * Create an event
        * Edit an event (if they create it)
        * Delete an event (if they create it)
        * Start an event
        * Stop an event
        * Pause an event
        * Broadcast an event
        * Record an event
        * View/remove attendees
        * All Account Admins are able to access/control webcast functions
        * All Event Admins are to edit webcast settings but they cannot start/stop the webcast
      </td>

      <td>
        Event Moderators **cannot** perform the tasks of an Event Host.

        They can:

        * View/remove attendees
        * View and manage the poll interface during webcast
        * View and manage the Q&A interface during webcast
        * View the event invitation text during webcast
        * Download the chat report after webcast
        * Download the Q&A report after webcast
        * Access the webcast dashboard
        * Toggle the webcast layout
        * Control the presentation (if designated, only one moderator at a time)
      </td>
    </tr>
  </tbody>
</Table>
