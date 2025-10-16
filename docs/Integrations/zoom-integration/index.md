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
Vbrick integrates with **Zoom** in three ways.  First, you are able to use a **Zoom Meeting** as the **video source** for a Vbrick Webcast. Second, you can easily record a Zoom Meeting and then apply all of the metadata and user and role-based settings available once it has concluded and it is stored as Video-on-Demand content in your Vbrick portal.  Finally, you are able to import your Zoom recordings automatically or directly from the **Upload** tray in Rev.

Rev currently does not integrate with Zoom Meetings Breakout rooms.

## Requirements

* Rev Cloud
* [Video Conference (VC) Integrations](doc:video-conference-vc-integrations) enabled
* A Zoom Meeting account that has an email that matches the email being used in the Rev account for Webcast Event setup and streaming, recording, and importing. (if using this [functionality](doc:zoom-integration#stream-a-zoom-meeting-to-a-scheduled-rev-webcast-event)).
* A **Zoom Meeting Pro Account** with at least one **Room Connector/SIP license**.
* Make sure you have the [latest version](doc:zoom-integration#update-the-zoom-integration) of the _Vbrick Rev_ Zoom App installed.

## Configuration

To enable and install Zoom in Rev:

1. Navigate to **Media Settings** > **Integrations**.  Scroll to the **Zoom Meetings** section.

2. Select the **Zoom Meetings Integration** checkbox.

3. Click the **Install Zoom Integration** button.

<Image align="center" alt="enable the zoom integration" border={false} caption="Click the Zoom Meetings Integration checkbox and the Install Zoom Integration button to begin your installation" title="enableZoomIntegration.png" src="https://files.readme.io/ac8f747-enableZoomIntegration.png" />

> 🚧 Important!
>
> If you are currently running two separate Rev accounts and attempting to install and associate the same Zoom account to both, it may be necessary to reinstall the Zoom integration on your first Rev portal in some circumstances.
>
> Zoom only supports one integration per one Rev portal at this time.

4. You are redirected to the **Zoom Login** page where you need to authorize Rev with access to your Zoom account.

<Image align="center" alt={503} border={false} caption="You must grant Rev access to your Zoom account the first time you log in after you enable the integration" title="authorizeZoom.png" src="https://files.readme.io/61c9f63-authorizeZoom.png" />

5. Once authorized, the Vbrick Rev app is installed from the Zoom marketplace automatically. Keep in mind that you may return to the **Integrations** page to uninstall the integration at any time by clicking the **Uninstall Zoom Integration** button that is now available.

6. Enter any [DTMF codes](doc:dtmf-configuration-and-usage) you want to use (optional).

7. You can also choose to [automatically import](doc:import-zoom-meetings-to-rev) your Zoom meetings (optional).

## Usage

Once you have installed and configured the integration, you are ready to use Zoom with Rev.

* [Stream a Zoom Meeting to a Rev Webcast Event](doc:stream-a-zoom-meeting-to-a-rev-webcast-event)
* [Record a Zoom Meeting as a New Rev VOD](doc:record-a-zoom-meeting-as-a-new-rev-vod)
* [Import Zoom Meetings to Rev](doc:import-zoom-meetings-to-rev)

## Troubleshooting

If you have any issues with your integration, make sure that you are using the latest version of the _Vbrick Rev_ Zoom App.

### Update the Zoom Integration

1. Navigate to **Media Settings** > **Integrations**.  Scroll to the **Zoom Meetings** section.

<Image align="center" alt="You must make sure you have the latest Zoom app installed for feature updates" border={false} caption="Make sure you have the latest Zoom app installed" src="https://files.readme.io/25a7eca-updateZoomApp.png" />

2. Click the **Uninstall Zoom Integration** button.  Note that you can force the uninstallation if you are not the original installer.
3. Reinstall the **Zoom Integration** again as described in [Configuration](doc:zoom-integration#configuration).  This ensures you are installing the latest version with all updates.

### Verify Your Email Address

Make sure that your email address matches and is exactly the same for the three accounts below.  If it does not, your integration will not work correctly:

1. Zoom Account
2. Zoom Marketplace
3. Rev Account
