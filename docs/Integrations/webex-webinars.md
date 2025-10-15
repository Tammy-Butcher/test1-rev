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
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
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

## Requirements

* Rev Cloud
* [Cisco Control Hub](https://www.webex.com/control-hub.html) log in
* **API Key** from an Account Admin user account (after creation)
* **API Secret** from an Account Admin user account (after creation)

## Configuration

To host in Webex Webcast view using your existing eCDN setup, you need to enable the Webex Webinar Integration first.

1. Enable the **Webex Webinars Integration** in **Media Settings** > **Integrations**.

<Image title="enableWebexEvents.png" alt={1111} align="center" src="https://files.readme.io/1293f56-enableWebexWebinars.png">
  Enable the Webex Webinars Integration setting under the Media Settings menu to begin
</Image>

2. Generate an **Account Admin** API key and secret to use in the **Cisco Control Hub**.  

<Image title="generateAPIKey.png" alt={868} align="center" src="https://files.readme.io/628d3e0-generateAPIKey.png">
  Save your generated Account Admin API key and secret
</Image>

> 🚧 Important!
>
> Note that this is an *user* API key and *not* a **device** key.  See [Create a User API Key](https://revdocs.vbrick.com/docs/user-accounts#create-a-user-api-key) if you are not sure how to generate this for an **Account Admin**.

3. Navigate to your **Cisco Control Hub** and enable the **Webcast Service** and  **eCDN through Rev** functions.

4. Enter the following information from Rev:

   * Vbrick Rev **URL**:
   * Account Admin **API Key**
   * Account Admin **API Secret**

You are now ready to begin scheduling Webex Webinars.

> 📘 Note
>
> For complete details on how to use Webex Webinars or additional help, view [Cisco Help](https://help.webex.com/en-us/landing/ld-7srxjs-WebexWebinars/#Get-Started) or contact your Cisco Account Manager.
