---
title: Q&A Module Management
excerpt: >-
  This guide gets you started on managing your own highly interactive Q&A
  session for your webcasts
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If [Q\&A](doc:attendee-engagement#enable-qa-for-an-event) is enabled during event setup, moderated question ques are available to both the **Event Host** and **Event Moderators** by clicking the **Q\&A** button. 

<Image title="qaIcon.png" alt={34} align="center" src="https://files.readme.io/13722c4-qaIcon.png">
  The QA icon allows Hosts and Moderators to manage all incoming questions from attendees
</Image>

This means webcast attendees are able to ask questions during the webcast and, unlike the chat interface, they can be separated into different "inbox queues" depending upon how you want them addressed. 

## Q\&A Queues and Functions

There are three question queues in the **Q\&A** module; the **Inbox** , **Speaker** , and **Closed** queues.  Each functions and is managed differently.

<Image title="qaInboxTabs.png" alt="Q&A tabs available for Hosts and Moderators; each one performs a different function" align="center" src="https://files.readme.io/2fbdf67-qaInboxTabs.png">
  Q\&A tabs available for Hosts and Moderators; each one performs a different function
</Image>

If the Q\&A module is not open at the time, a visual indicator (in the form of a number) appears next to the icon to alert the Host/Moderator that questions are present.  As new questions are asked, they are also noted next to the queue tabs.

<Image title="qaInboxTabsNewQuestions.png" alt="New questions are noted next to queue tabs so that Moderators can keep up with them" align="center" src="https://files.readme.io/157c84b-qaInboxTabsNewQuestions.png">
  New questions are noted next to queue tabs so that Moderators can keep up with them
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Queue
      </th>

      <th>
        Function
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Inbox
      </td>

      <td>
        New questions submitted by attendees are placed in the **Inbox**queue.  

        The Host or Moderator view all questions in the Inbox and then decide upon the appropriate action to take with it.  

        This includes:\
        a. Responding directly to the attendee\
        b. Flagging the question for follow-up\
        c. Moving the question to the **Speaker**queue\
        d. Moving the question to the **Closed**queue (i.e., closing the question)
      </td>
    </tr>

    <tr>
      <td>
        Speaker Queue
      </td>

      <td>
        Questions that are filtered to this queue are intended for the **Speaker**(presenter) of the webcast to answer.  Clicking the **Queue**icon on an Inbox question moves it to this queue.  

        Note that Moderators / Hosts are still expected to moderate and mark appropriately how the question is handled by the Speaker once in this queue.
      </td>
    </tr>

    <tr>
      <td>
        Closed Queue
      </td>

      <td>
        Questions that appear here have been answered (responded to), marked for **Follow up**, or have been marked **Closed**. Additional actions may be taken upon them if needed after they are in the Closed queue.
      </td>
    </tr>
  </tbody>
</Table>

<Image title="openFullQueWindow.png" alt="Use the Open in a New Window icon to open a separate browser window (from Rev) for the question queues" align="center" src="https://files.readme.io/fec60fc-openFullQueWindow.png">
  Use the Open in a New Window icon to open a separate browser window (from Rev) for the question queues
</Image>

During large events, it is often easier to manage the Q\&A queues in a separate interface or window, particularly when you have several attendees and moderators.  Use the **Open in a New Window** icon to open the Q\&A module in a new browser window or tab so that only this interface is visible if desired.  This may make it easier to view and manage.  Just simply close the window or tab if you want to go back to managing questions within the Rev webcast.

<Image title="qaWindowFullScreenMode.png" alt="The Q&A Module is often easier to manage in full screen mode" align="center" src="https://files.readme.io/82164d0-qaWindowFullScreenMode.png">
  The Q\&A Module is often easier to manage in full screen mode
</Image>

> 👍 Tip
>
> If more than one **Event Moderator** is assigned to an event, the Q\&A interface **dynamically** updates as incoming questions are evaluated and actions are performed on them. Moderators are aware of what actions other moderators are taking on each question in **real-time** via on-screen messaging displayed by Rev.

## Moderate the Inbox Queue

New questions that are asked during the webcast event appear in the **Inbox** queue first. Both the Event Host and Event Moderators have access to the Inbox queue.

<Image title="qaInbox.png" alt="New questions appear in the Inbox first. As additional questions are asked, refresh the queue by clicking the New Question button. Those questions are then added to the bottom of the list." align="center" src="https://files.readme.io/98512f7-qaInbox.png">
  New questions appear in the Inbox first. As additional questions are asked, refresh the queue by clicking the New Question button. Those questions are then added to the bottom of the list.
</Image>

New questions appear on the bottom of the list. However, as additional new questions come in, the list *requires* a manual refresh to view them by using the **New Questions** button (seen in the image above). Those questions are then moved to the bottom of the **Inbox** list.

Each question is assigned a starting number when it is received (starting with 1). This number is maintained with the question when it is moved to a different queue for consistency and easy referral throughout the question’s “lifecycle”. 

This is why there appears to be a "gap" in question numbers in the image below.  Questions 2 and 3 have had some sort of action taken on them and/or are in different queues.

<Image title="qaInboxNumberConsistency.png" alt={352} align="center" src="https://files.readme.io/dfcb32a-qaInboxNumberConsistency.png">
  Each question in the queue keeps its number throughout its lifecycle, even when moved out of the queue as #2 and #3 have been in this Inbox which is why they are not displayed
</Image>

There are 1 of 4 actions that may be performed on an **Inbox** question.

<Image title="questionActions.png" alt={352} align="center" src="https://files.readme.io/57248d3-questionActions.png">
  The actions you may take on an Inbox question
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Action
      </th>

      <th>
        Result
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Follow up
      </td>

      <td>
        Moves the question to the **Closed**queue and marks it as “flagged for follow up” for the Q\&A report.
      </td>
    </tr>

    <tr>
      <td>
        Reply
      </td>

      <td>
        Replies directly to the attendee that asked the question or to **all**event attendees if the **Publish to All** checkbox is selected. The question and its reply is also moved to the **Group Questions** tab for all attendees to view if **Publish to All** is checked.  

        No other attendee is able to view the reply if the **Publish to All** checkbox is *not* selected.  

        Moves the question to the **Closed**queue.
      </td>
    </tr>

    <tr>
      <td>
        Queue
      </td>

      <td>
        Moves the question to the **Speaker**queue to be answered. New questions appear at the bottom of the Speaker queue list similar to how the Inbox functions.
      </td>
    </tr>

    <tr>
      <td>
        Close
      </td>

      <td>
        Moves the question to the **Closed**queue and marks it as “closed” for the Q\&A report.
      </td>
    </tr>
  </tbody>
</Table>

<Image title="moderatorReplyToAll.png" alt={502} align="center" src="https://files.readme.io/d6594ed-moderatorReplyToAll.png">
  If more than one Moderator is present, all other moderators are alerted that this moderator is answering this question
</Image>

## Moderate the Speaker Queue

Moderators filter questions that appear in the Inbox to the speaker **Queue** when appropriate.  This is often the case when it is intended that the Speaker take questions "on-the-fly" or conduct "Q\&A" sessions after a presentation.

<Image title="qaSpeaker.png" alt={352} align="center" src="https://files.readme.io/18639e4-qaSpeaker.png">
  The Speaker queue functions very similar to the Inbox except the actions you take on questions are slightly different in some cases
</Image>

> 🚧 Important!
>
> The **Speaker** queue functions *exactly* as the **Inbox** queue does with new questions appearing on the bottom as they come in from attendees.
>
> However, you may drag and drop question order in the Speaker queue (their number stays the same) and actions that may be taken on them are also different.

There are 1 of 4 actions that may be performed on a **Speaker** question.

<Image title="speakerActions.png" alt={352} align="center" src="https://files.readme.io/78ec54f-speakerActions.png">
  The actions you may take on a Speaker question
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Action
      </th>

      <th>
        Result
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Follow-up
      </td>

      <td>
        Moves the question to the **Closed**queue and marks it as “flagged for follow up” for the Q\&A report.
      </td>
    </tr>

    <tr>
      <td>
        Reply
      </td>

      <td>
        Replies directly to the attendee that asked the question or to **all**event attendees if the **Publish to All** checkbox is selected. The question and its reply is also moved to the **Group Questions** tab for all attendees to view if **Publish to All** is checked.  

        No other attendee is able to view the reply if the **Publish to All** checkbox is *not* selected.  

        Moves the question to the **Closed**queue.
      </td>
    </tr>

    <tr>
      <td>
        Answered
      </td>

      <td>
        Assumes the speaker verbally responds to the question during the webcast and moves the question to the **Closed**queue and marks it as “answered” for the Q\&A report.
      </td>
    </tr>

    <tr>
      <td>
        Decline
      </td>

      <td>
        Moves the question to the **Closed**queue and marks it as “declined” for the Q\&A report.
      </td>
    </tr>
  </tbody>
</Table>

## Moderate the Closed Queue

Questions that appear in the **Closed** queue have had some sort of action taken on them. You may filter the queue (from full screen mode) or take additional actions on them as needed.

<Image title="qaClosed.png" alt="The actions that have been taken on Closed questions are denoted by the icons next to the question and by the colored boxes under the question" align="center" src="https://files.readme.io/8fb6fe0-qaClosed.png">
  The actions that have been taken on Closed questions are denoted by the icons next to the question and by the colored boxes under the question
</Image>

The action taken on each question is noted through text and an associated icon next to the question. Rolling over the icon displays the action taken on the question.

There are 1 of 4 actions that may be performed on a **Closed** question.

<Image title="closedActions.png" alt="Click the Closed Actions dropdown menu in the upper right corner of each question to access Closed actions you may take" align="center" src="https://files.readme.io/b7ab518-closedActions.png">
  Click the Closed Actions dropdown menu in the upper right corner of each question to access Closed actions you may take
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Action
      </th>

      <th>
        Result
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Queue
      </td>

      <td>
        Moves the question back to the **Speaker**queue.
      </td>
    </tr>

    <tr>
      <td>
        Answered
      </td>

      <td>
        Changes the status to “answered” for the Q\&A report.
      </td>
    </tr>

    <tr>
      <td>
        Follow-up
      </td>

      <td>
        Changes the status to “flagged for follow up” for the Q\&A report.
      </td>
    </tr>

    <tr>
      <td>
        Reply
      </td>

      <td>
        Replies directly to the attendee that asked the question or to all event attendees if the **Publish to All** checkbox is selected. No other attendee is able to view the reply if the Publish to All checkbox is *not* selected.  

        If it is selected, the question and its reply is also moved to the **Group Questions** tab for all attendees to view.
      </td>
    </tr>
  </tbody>
</Table>

## Publish and Remove Questions from Public View

When an Event Host or Event Moderator replies to a question in any Q\&A queue the option exists to make the reply public to *all* event attendees by checking the **Publish to All** checkbox. 

<Image title="moderatorReplyToAll.png" alt={502} align="center" src="https://files.readme.io/b2582b1-moderatorReplyToAll.png">
  The Publish to All checkbox submits a question anonymously for all attendees to view
</Image>

> 👍 Tip
>
> All questions that are made public are done so *anonymously*. The User name is not associated to the question on the **Group Questions** tab.

A question that has previously been made public in this manner may also be *removed* from public view and the **Group Questions** tab through the **Closed** queue.

To remove a question that was previously published for all to view:

1. Navigate to the **Closed** queue and find the question.

2. Use the **Closed** queue **Action** dropdown controls to the right of the question and click **Reply**.

3. Uncheck the **Publish to All** checkbox and click **Save**.

4. The question no longer appears under the **Group Questions** tab.
