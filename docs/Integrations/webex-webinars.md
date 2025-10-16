---
title: Webex Webinars
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
## Requirements

* Rev Cloud
* [Cisco Control Hub](https://www.webex.com/control-hub.html) log in
* **API Key** from an Account Admin user account (after creation)
* **API Secret** from an Account Admin user account (after creation)

## Configuration

To host in Webex Webcast view using your existing eCDN setup, you need to enable the Webex Webinar Integration first.

1. Enable the **Webex Webinars Integration** in **Media Settings** > **Integrations**.

<Image align="center" alt={1111} border={false} caption="Enable the Webex Webinars Integration setting under the Media Settings menu to begin" title="enableWebexEvents.png" src="https://files.readme.io/1293f56-enableWebexWebinars.png" />

2. Generate an **Account Admin** API key and secret to use in the **Cisco Control Hub**.

<Image align="center" alt={868} border={false} caption="Save your generated Account Admin API key and secret" title="generateAPIKey.png" src="https://files.readme.io/628d3e0-generateAPIKey.png" />

> 🚧 Important!
>
> Note that this is an _user_ API key and _not_ a **device** key.  See [Create a User API Key](https://revdocs.vbrick.com/docs/user-accounts#create-a-user-api-key) if you are not sure how to generate this for an **Account Admin**.

3. Navigate to your **Cisco Control Hub** and enable the **Webcast Service** and  **eCDN through Rev** functions.

4. Enter the following information from Rev:

   * Vbrick Rev **URL**:
   * Account Admin **API Key**
   * Account Admin **API Secret**

You are now ready to begin scheduling Webex Webinars.

> 📘 Note
>
> For complete details on how to use Webex Webinars or additional help, view [Cisco Help](https://help.webex.com/en-us/landing/ld-7srxjs-WebexWebinars/#Get-Started) or contact your Cisco Account Manager.
