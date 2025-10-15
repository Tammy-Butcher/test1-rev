---
title: Prepare a Dry Run
excerpt: >-
  This guide demonstrates how to prepare and host a pre-production webcast. This
  allows you to test event settings and features before you broadcast the Main
  Event with actual attendees.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
The [Pre-Production](doc:event-basic-settings#pre-production) setting is enabled in webcast settings and allows Event Admins and Hosts to run one or more test runs (dry runs) of the event before the **Main Event**. Once the Pre-Production setting is enabled, additional option(s) to configure a dry run event become available.

> 🚧 Important!
>
> Dry runs are *not* visible to the Main Event attendees. Those attendees are kept unaware of the test runs and the event appears as if it has not yet started.

## Configuration

To prepare and host a dry run:

1. Select **Enabled** tab next to **Pre-Production** in the [Event Basic Settings](doc:event-basic-settings) section. 

<Image title="preproductionSettings.png" alt={1132} src="https://files.readme.io/0971623-preproductionSettings.png">
  Enable the Pre-Production tab in Event Basic Settings to prepare your dry run
</Image>

2. Enter a **Pre-Production Time Duration** in hours and minutes (00:00). This is the period of time *before* the start of the **Main Event** that the **Event Host** can run one or more test runs (dry runs).

> 👍 Use Case Example
>
> If the webcast starts at 9:00 a.m. and you enter 30 minutes in this field, you may conduct dry runs and test the event beginning at 8:30 a.m. until the start of the Main Event at 9:00 a.m.

3. Enter **Pre-Production Attendees** to help you test the event.

> 📘 Note
>
> **Pre-production Attendees** are *separate* from Main Event attendees. This means that you can select different people to participate in testing the dry run versus attending the Main Event if desired.

## Starting and Broadcasting

During the Pre-Production window, a **Start Pre-Production** button is visible instead of a **Start Webcast** button when an Admin or Host clicks on the event. Note:  You must have configured and saved your event first.

Webcast links are only visible if the [Show Event Sharing Link](doc:event-basic-settings#show-event-sharing-link) is enabled during event set up.

<Image title="startPreproductionButton.png" alt={1202} src="https://files.readme.io/a1df1c3-startPreproductionButton.png">
  When pre-production time is enabled and active, a Start Pre-Production button is available
</Image>

You still need to **Broadcast** your pre-production event for your pre-production attendees to view it just as you would a Main Event once you start it.

<Image title="broadcastPreproductionEvent.png" alt={1202} src="https://files.readme.io/feb1262-broadcastPreproductionEvent.png">
  Broadcast your dry run just as you would a production run so your attendees can view it
</Image>

> 👍 Tip
>
> To end your dry run and start your **Main Event**, click the **End Pre-Production** button. You are returned to the event settings page where you can click the **Start Webcast** button as you normally would at the event's regular **Start Time**.

Dry Run Notes:

* This setting is disabled by default.
* If the Main Event **Start Time** is modified, the **Pre-Production Duratio**n (and total event time) are updated accordingly automatically (once the event is saved).
* Webcast reservations for technical resources (DMEs, Presentation Profiles, etc.) include the total event time plus any pre-production time needed/set.
* DMEs may not be [updated](doc:update-dme-software-version) during pre-production.
* During a dry run, Event Admins and Hosts are able to start and stop pre-production broadcasting and there are on-screen indicators to all roles that a dry run/pre-production event is in progress versus the Main Event.
* [Webcast analytics reports](doc:webcast-reports) are differentiated by “Main Event” versus “Pre-Production” where necessary.

## Pre-Production FAQs

**Do attendees of the Main Event see what the Pre-Production attendees see?**

Only designated **Pre-Production Attendees** can see the event during a pre-production dry run. Any actions that you take while in pre-production will only affect those designated attendees. This allows you peace of mind when doing a test run of your event.

**How do I end Pre-Production and go directly into the Main Event?\&#xA;**\
To start the **Main Event** webcast, click on the **End Pre-Production** button and then click **Start Webcast** on the [event settings](doc:host-a-production-webcast#viewing-event-hosting-details) form at its designated **Start Time**. This launches the webcast and you can broadcast the event whenever you are ready.

**Do changes I make during Pre-Production impact the Main Event?**

Yes, the pre-production feature allows you to test, change, and save the settings of your event. You do not need to remember the changes and apply them anywhere else because it’s the same event.

**How long of a Pre-Production test should I run?**

You can test your webcast for up to 72 hours before it starts. Most test their event either the day before or the day of the Main Event. However, you have the flexibility to test your Event in Pre-Production for multiple days before it begins.

**Should I test my event in Pre-Production?**

In addition to added confidence when you start your Main Event, there are scenarios where pre-production testing is recommended:

* You want to broadcast your dry run test to a set of attendees
* You are setting up a new **Presentation Profile** and want to make sure it works as anticipated

**How are analytics reported for Pre-Production?**

Analytics for the pre-production session are reported separately. This allows you to clearly see the attendees and performance of your Main Event Webcast. View [Real-Time Analytics and Webcast Report Downloads](doc:view-real-time-analytics-and-webcast-report-downloads) for more information.
