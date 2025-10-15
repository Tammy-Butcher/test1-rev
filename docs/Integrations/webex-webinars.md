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
[block:html]
{
  "html": "\n<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


## Requirements

- Rev Cloud
- [Cisco Control Hub](https://www.webex.com/control-hub.html) log in
- **API Key** from an Account Admin user account (after creation)
- **API Secret** from an Account Admin user account (after creation)

## Configuration

To host in Webex Webcast view using your existing eCDN setup, you need to enable the Webex Webinar Integration first.

1. Enable the **Webex Webinars Integration** in **Media Settings** > **Integrations**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1293f56-enableWebexWebinars.png",
        "enableWebexEvents.png",
        1111
      ],
      "align": "center",
      "caption": "Enable the Webex Webinars Integration setting under the Media Settings menu to begin"
    }
  ]
}
[/block]


2. Generate an **Account Admin** API key and secret to use in the **Cisco Control Hub**.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/628d3e0-generateAPIKey.png",
        "generateAPIKey.png",
        868
      ],
      "align": "center",
      "caption": "Save your generated Account Admin API key and secret"
    }
  ]
}
[/block]


> 🚧 Important!
> 
> Note that this is an _user_ API key and _not_ a **device** key.  See [Create a User API Key](https://revdocs.vbrick.com/docs/user-accounts#create-a-user-api-key) if you are not sure how to generate this for an **Account Admin**.

3. Navigate to your **Cisco Control Hub** and enable the **Webcast Service** and  **eCDN through Rev** functions.

4. Enter the following information from Rev:

   - Vbrick Rev **URL**:
   - Account Admin **API Key**
   - Account Admin **API Secret**

You are now ready to begin scheduling Webex Webinars.

> 📘 Note
> 
> For complete details on how to use Webex Webinars or additional help, view [Cisco Help](https://help.webex.com/en-us/landing/ld-7srxjs-WebexWebinars/#Get-Started) or contact your Cisco Account Manager.