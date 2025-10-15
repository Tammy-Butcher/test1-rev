---
title: Change Log (v7.52)
excerpt: ':calendar: Date Added: April 2023'
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## :wrench: **Updated/Fixed**

### Custom Public Registration Terms

_For Rev and Vbrick Distribution_

As part of this release, you are now able to customize the "Consent to the capture of my information" text that attendees are required to accept before registering for and joining a [Public Event with Registration](doc:public-events#customizable-consent-text). 

To support this feature, the following endpoints are updated with the **isCustomConsentEnabled** and **consentVerbiage** parameters.

- [Create Webcast](ref:createevent)

- [Update Webcast](ref:editevent)

- [Patch Webcast](ref:patchwebcast)

- [Get Webcast Details](ref:getevent)

**Requirements for use:**

- **isCustomConsentEnabled** must be set to true (default is false).
- **consentVerbiage** must be modified to contain the updated text you want to use.  If left blank, a 400 error is returned.
- The event must be **Public** and the **registrationType** must equal **Registration** (and _not_ Anonymous)

Note that all users who make this change become Data Controllers for their organization and, as such, get recorded by username, first name, last name, and timestamped with when the change was made.