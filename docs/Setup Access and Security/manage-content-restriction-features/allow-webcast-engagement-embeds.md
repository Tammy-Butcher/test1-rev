---
title: Allow Webcast Engagement Embeds
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
To allow your Hosts and Moderators to display embedded third-party content, you must first explicitly enable that functionality.  You must also specify _which_ third-party sites/domains are allowed to be embedded so that your portal remains secure.  The ability to show **Allow Embedded Content** is disabled by default.

To allow webcast content embedding:

1. Navigate to **Admin > System Settings** > **Content Restriction**.

2. Scroll to the **Webcast User Engagement** section and click the **Allow Embedded Content** checkbox to enable the setting.

<Image align="center" alt={589} border={false} caption="This setting must be enabled to embed third-party user engagements in your events" title="allowWebcastEmbeds.png" src="https://files.readme.io/d18da42-allowWebcastEmbeds.png" />

3. You must accept the Warning disclaimer message that appears before you are able to proceed.

<Image align="center" alt={680} border={false} src="https://files.readme.io/5cf754b-webcastEmbedWarning.png" title="webcastEmbedWarning.png" />

4. Once enabled, a pre-populated list of popular engagements is already in place for Hosts and Moderators to choose from when they set up their events.

<Image align="center" alt={767} border={false} caption="Add the URLs of the sites you want to embed in your events" title="urlEmbeds.png" src="https://files.readme.io/23b7cd2-urlEmbeds.png" />

5. Add additional third-party domains as needed following the format seen with one engagement per line.

> ❗️ Caution!
>
> During event setup, the Host or Moderator is only allowed to embed engagements that are included on the allowed list of Domains/URLs you add here.  Note that wildcard characters are permissible.
>
> If an attempt is made to add embed code from an engagement that is _not_ provided here, the embed _will_ fail.

When _enabled_:

* An [Embedded Content](doc:embed-a-webcast-attendee-engagement) tab becomes visible during event set up and may be toggled by Hosts and Moderators in the **Attendee Engagements** section.

<Image align="center" alt={1113} border={false} caption="This section only appears during event setup if the Allow Embedded Content checkbox is selected in User Security Settings" title="embeddedContentAdded.png" src="https://files.readme.io/2b4b49d-embeddedContentAdded.png" />

* Hosts and Moderators may only embed the third-party domains or URLs that are specified per the **Allow Embedded Content** URLs in the image above as noted.

* Embedded Content will appear for event attendees in a specific [Engagements](doc:manage-embedded-engagements) flyout window (per embed) when the webcast is broadcast and they are individually activated.
