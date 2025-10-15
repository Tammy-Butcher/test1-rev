---
title: Create an API Key
excerpt: How to create and manage API Keys for Rev Devices
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
API Keys are created in Rev to link external devices to Rev such as a DME.  You can also create [User-level API keys](doc:user-accounts#create-a-user-api-key) to manage authentication and authorization that respect the role/permission of the user that the key belongs to when responding to the API calls.

> 👍 Tip
>
> You \_must \_create an API key for each type of device you plan to use with Rev (including LDAP Connectors) before you add the device in the **Device** module. 
>
> Once the API key is created, you then enter the key in the **Rev API** field in the **Device** profile.

The **API Keys** menu option displays the API keys in use with Rev devices. You are also able to add and delete API Keys as needed.

<Image title="apiKeyModule.png" alt={1202} align="center" src="https://files.readme.io/ea4d16b-apiKeyModule.png">
  Click System Settings > API Keys to add a new API Key to Rev
</Image>

To add an API Key:

1. Navigate to **Admin > System Settings** > **API Keys**.

2. Click the **Add Key** button.

<Image title="addApiKey.png" alt={902} align="center" src="https://files.readme.io/b28a86e-addApiKey.png">
  The Add Key button adds a new key for a new device.  This should be done before you add the new device in the Device module.
</Image>

3. Enter a descriptive API Key **Name**.

4. Enter the API **Key**. You may use any combination of letters and numbers of your choice.

> ❗️ Warning!
>
> It is \_highly \_recommended that symbols and special characters are \_not \_used in the **Key** field.

5. Enter any **Authorized Redirect URIs** needed if you plan to use any integrations and the [OAuth](ref:a-oauth) API. This field is checked to ensure that the redirect URIs specified in the authorization and token request match and provides an additional security check to make sure that the correct user is making the request. Multiple URIs may be provided but at least one \_must \_match the authorization request to be redirected.

6. Click **Create** to save your key.

7. Use this same key in the device you plan to add and link to Rev. Each device will have a Rev UI section to complete the API Key field and link it to Rev.

8. Use the **Show** link on the API Module main display to view the API’s **Secret** that is generated for use with Rev’s [Authorization](ref:authorization-1) API if needed.

> 📘 Note
>
> While an API Key is required for every device created in Rev, you do not have to create separate API Keys for each device. This is a distinction that is often overlooked.
>
> For example, you may create one API Key that is used for each location you have, such as Headquarters (or the United States), and then use that same API Key for each device in that location if that is your preference. 
>
> Then you may create a different API Key for a location in the UK or training rooms and use that key for the devices in only those locations.
