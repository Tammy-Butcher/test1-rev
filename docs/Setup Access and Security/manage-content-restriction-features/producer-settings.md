---
title: Producer Settings
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
## Allow Guest Presenters for Producer Webcasts

Guest presenters can be invited to a Producer webcast but this must be enabled first.

To allow Guest presenters in a Producer Webcast:

1. Navigate to **Admin > System Settings > Content Restriction**.
2. Scroll to the **Producer Settings** section and select the **Enable External Presenters for Producer** checkbox.  This setting is enabled by default.

<Image align="center" alt={856} border={false} caption="When this setting is enabled, you can invite external presenters that do not have a Rev account to a Producer event" title="producerSettings.png" src="https://files.readme.io/89b8e30-producerSettings.png" />

When this setting is enabled:

* A new section becomes available during [Producer Event Set Up](doc:producer-event-set-up) in the **Hosts, Presenters, and Moderators** section called **External Event Presenters**.
* Hosts and Moderators may add External Event Presenters and include their **Name**, **Title**, and **Email** address.
* An External Event Presenter is not required to have a Rev Account. These presenter types are considered **Guest** presenters.  A valid email address is required.
* The Guest presenters are invited to attend and present in the Producer event through their email account via a separate URL (than the webcast attendees receive when invited to the event).
* Should anything change about the event (date, time, cancellation and so forth), the Guest presenters are notified via this same email.
* You can also invite Guest presenters when you [host a producer event](doc:produce-an-event) and via API.
