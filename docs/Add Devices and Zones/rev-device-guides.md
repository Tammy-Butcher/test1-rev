---
title: Rev Device Guides
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: the-rev-home-page
      title: The Rev Home Page
    - type: basic
      slug: rev-video-guides
      title: Rev Video Guides
    - type: basic
      slug: rev-event-guides
      title: Rev Event Guides
    - type: basic
      slug: rev-channel-guides
      title: Rev Channel Guides
    - type: basic
      slug: configure-access-and-permissions
      title: Rev Access and Security Guides
    - type: basic
      slug: rev-branding-and-style-guides
      title: Rev Branding and Style Guides
    - type: basic
      slug: analytics-and-reports-guides
      title: Analytics and Reports Guides
    - type: basic
      slug: supported-video-and-audio-formats
      title: Video and Audio Formats
    - type: basic
      slug: rev-integration-guides
      title: Rev Integration Guides
---
Devices are external components that “talk” to Rev and may include Vbrick Encoders/Decoders, Distributed Media Engines (DMEs), LDAP servers, and Set Top Boxes. Once configured, devices are placed in zones.  Using devices and zones in Rev, you are able to maintain strict control of your network, bandwidth, and content ingestion easily and intuitively.

This set of guides explains how to link and configure the various devices that work with Rev and then place them in zone hierarchies to set up your entire streaming ecosystem.
[block:html]
{
  "html": "<link\n\thref=\"https://fonts.googleapis.com/icon?family=Material+Icons\"\n\trel=\"stylesheet\"\n/>\n<link\n\thref=\"https://fonts.googleapis.com/css?family=Open+Sans:400,600\"\n\trel=\"stylesheet\"\n/>\n\n<div class=\"card-menu\">\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Devices</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">timeline</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/getting-started-with-rev-devices\">Initial Setup</a>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Devices</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">devices_other</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/add-a-source-or-custom-device\"\n\t\t\t\t\t>Add a Source or Custom Device</a\n\t\t\t\t>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Devices</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">source</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/use-ldap-and-active-directory-with-rev\"\n\t\t\t\t\t>Use LDAP & Active Directory</a\n\t\t\t\t>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Devices</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">date_range</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/add-a-presentation-profile\">Add Presentation Profiles</a>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Devices</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">device_hub</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/manage-dme-devices\">Manage & Add DMEs</a>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Devices</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">devices</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/add-a-set-top-box-or-additional-display-device\"\n\t\t\t\t\t>Set Up Display Devices & Set Top Boxes</a\n\t\t\t\t>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Zones</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">mediation</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/manage-and-add-zones\">Configure Rev Zones</a>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\n\t<div class=\"card\">\n\t\t<div class=\"card-header\">Devices</div>\n\t\t<div class=\"card-main\">\n\t\t\t<i class=\"material-icons\">engineering</i>\n\t\t\t<div class=\"main-description\">\n\t\t\t\t<a href=\"/docs/device-maintenance\">Device Maintenance</a>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n</div>\n\n<style>\n\tbody {\n\t\tfont-family: \"Open Sans\", sans-serif;\n\t}\n\n\t.card-menu {\n\t\tdisplay: flex;\n\t\tflex-flow: row wrap;\n\t\tjustify-content: center;\n\t\talign-items: middle;\n\t}\n\n\t.card {\n\t\twidth: 150px; \n\t\tdisplay: flex; \n\t\tflex-direction: column; \n\t\tborder: 1px solid #4fb9e7; \n\t\tborder-radius: 4px; \n\t\toverflow: hidden; \n\t\tmargin: 5px; \n\t}\n\n\t.card:hover {\n\t\tbox-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);\n\t}\n\n\t.card-header {\n\t\tcolor: #1d9dd5;\n\t\ttext-align: center;\n\t\tfont-size: 12px;\n\t\tfont-weight: 600;\n\t\tborder-bottom: 1px solid #7ccbed;\n\t\tbackground-color: #b8e3f5;\n\t\tpadding: 5px 10px;\n\t}\n\n\t.card-main {\n\t\tdisplay: flex; \n\t\tflex-direction: column; \n\t\tjustify-content: center; \n\t\talign-items: center; \n\t\tpadding: 15px 0; \n\t}\n\n\t.material-icons {\n\t\tfont-size: 36px;\n\t\tcolor: #1d9dd5;\n\t\tmargin-bottom: 5px;\n\t}\n\n\t.main-description {\n\t\tcolor: #1d9dd5;\n\t\tfont-size: 12px;\n\t\ttext-align: center;\n\t\ttext-decoration: none;\n\t}\n\n\t.main-description a {\n\t\ttext-decoration: none;\n\t\tcolor: #1d9dd5;\n\t}\n</style>"
}
[/block]