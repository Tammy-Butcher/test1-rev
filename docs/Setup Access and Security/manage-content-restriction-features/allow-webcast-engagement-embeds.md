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
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

To allow your Hosts and Moderators to display embedded third-party content, you must first explicitly enable that functionality.  You must also specify *which* third-party sites/domains are allowed to be embedded so that your portal remains secure.  The ability to show **Allow Embedded Content** is disabled by default.

To allow webcast content embedding:

1. Navigate to **Admin > System Settings** > **Content Restriction**.

2. Scroll to the **Webcast User Engagement** section and click the **Allow Embedded Content** checkbox to enable the setting.

<Image title="allowWebcastEmbeds.png" alt={589} align="center" src="https://files.readme.io/d18da42-allowWebcastEmbeds.png">
  This setting must be enabled to embed third-party user engagements in your events
</Image>

3. You must accept the Warning disclaimer message that appears before you are able to proceed.

<Image title="webcastEmbedWarning.png" alt={680} align="center" src="https://files.readme.io/5cf754b-webcastEmbedWarning.png" />

4. Once enabled, a pre-populated list of popular engagements is already in place for Hosts and Moderators to choose from when they set up their events.

<Image title="urlEmbeds.png" alt={767} align="center" src="https://files.readme.io/23b7cd2-urlEmbeds.png">
  Add the URLs of the sites you want to embed in your events
</Image>

5. Add additional third-party domains as needed following the format seen with one engagement per line.

> ❗️ Caution!
>
> During event setup, the Host or Moderator is only allowed to embed engagements that are included on the allowed list of Domains/URLs you add here.  Note that wildcard characters are permissible.  
>
> If an attempt is made to add embed code from an engagement that is *not* provided here, the embed *will* fail.

When *enabled*:

* An [Embedded Content](doc:embed-a-webcast-attendee-engagement) tab becomes visible during event set up and may be toggled by Hosts and Moderators in the **Attendee Engagements** section.

<Image title="embeddedContentAdded.png" alt={1113} align="center" src="https://files.readme.io/2b4b49d-embeddedContentAdded.png">
  This section only appears during event setup if the Allow Embedded Content checkbox is selected in User Security Settings
</Image>

* Hosts and Moderators may only embed the third-party domains or URLs that are specified per the **Allow Embedded Content** URLs in the image above as noted.

* Embedded Content will appear for event attendees in a specific [Engagements](doc:manage-embedded-engagements) flyout window (per embed) when the webcast is broadcast and they are individually activated.
