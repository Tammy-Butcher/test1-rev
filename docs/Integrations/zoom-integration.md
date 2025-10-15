---
title: Zoom
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


Vbrick integrates with **Zoom ** in three ways.  First, you are able to use a **Zoom Meeting** as the **video source** for a Vbrick Webcast. Second, you can easily record a Zoom Meeting and then apply all of the metadata and user and role-based settings available once it has concluded and it is stored as Video-on-Demand content in your Vbrick portal.  Finally, you are able to import your Zoom recordings automatically or directly from the **Upload** tray in Rev.

## Requirements

- Rev Cloud
- [Video Conference (VC) Integrations](doc:video-conference-vc-integrations) enabled
- A Zoom Meeting account that has an email that matches the email being used in the Rev account for Webcast Event setup and streaming, recording, and importing. (if using this [functionality](doc:zoom-integration#stream-a-zoom-meeting-to-a-scheduled-rev-webcast-event)).
- A **Zoom Meeting Pro Account** with at least one **Room Connector/SIP license**.
- Make sure you have the [latest version](doc:zoom-integration#update-the-zoom-integration) of the _Vbrick Rev_ Zoom App installed.

## Configuration

To enable and install Zoom in Rev:

1. Navigate to **Media Settings** > **Integrations**.  Scroll to the **Zoom Meetings** section.

2. Select the **Zoom Meetings Integration** checkbox.

3. Click the **Install Zoom Integration** button.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ac8f747-enableZoomIntegration.png",
        "enableZoomIntegration.png",
        "enable the zoom integration"
      ],
      "align": "center",
      "caption": "Click the Zoom Meetings Integration checkbox and the Install Zoom Integration button to begin your installation"
    }
  ]
}
[/block]


> 🚧 Important!
> 
> If you are currently running two separate Rev accounts and attempting to install and associate the same Zoom account to both, it may be necessary to reinstall the Zoom integration on your first Rev portal in some circumstances.
> 
> Zoom only supports one integration per one Rev portal at this time.

4. You are redirected to the **Zoom Login** page where you need to authorize Rev with access to your Zoom account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/61c9f63-authorizeZoom.png",
        "authorizeZoom.png",
        503
      ],
      "align": "center",
      "caption": "You must grant Rev access to your Zoom account the first time you log in after you enable the integration"
    }
  ]
}
[/block]


5. Once authorized, the Vbrick Rev app is installed from the Zoom marketplace automatically. Keep in mind that you may return to the **Integrations **page to uninstall the integration at any time by clicking the **Uninstall Zoom Integration** button that is now available.

6. Enter any [DTMF codes](doc:dtmf-configuration-and-usage) you want to use (optional).

7. You can also choose to [automatically import](doc:import-zoom-meetings-to-rev) your Zoom meetings (optional).

## Usage

Once you have installed and configured the integration, you are ready to use Zoom with Rev.

- [Stream a Zoom Meeting to a Rev Webcast Event](doc:stream-a-zoom-meeting-to-a-rev-webcast-event)
- [Record a Zoom Meeting as a New Rev VOD](doc:record-a-zoom-meeting-as-a-new-rev-vod) 
- [Import Zoom Meetings to Rev](doc:import-zoom-meetings-to-rev) 

## Troubleshooting

If you have any issues with your integration, make sure that you are using the latest version of the _Vbrick Rev_ Zoom App.

### Update the Zoom Integration

1. Navigate to **Media Settings** > **Integrations**.  Scroll to the **Zoom Meetings** section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/25a7eca-updateZoomApp.png",
        null,
        "You must make sure you have the latest Zoom app installed for feature updates"
      ],
      "align": "center",
      "caption": "Make sure you have the latest Zoom app installed"
    }
  ]
}
[/block]


2. Click the **Uninstall Zoom Integration** button.  Note that you can force the uninstallation if you are not the original installer.
3. Reinstall the **Zoom Integration** again as described in [Configuration](doc:zoom-integration#configuration).  This ensures you are installing the latest version with all updates.

### Verify Your Email Address

Make sure that your email address matches and is exactly the same for the three accounts below.  If it does not, your integration will not work correctly:

1. Zoom Account
2. Zoom Marketplace
3. Rev Account