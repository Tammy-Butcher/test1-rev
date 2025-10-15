---
title: View Rev Content in a Microsoft Teams Tab
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


To make Rev portal content visible in a Microsoft Teams **Channel** tab you need to enable and configure the Microsoft Teams Integration option in **Media Settings > Integrations**.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b751c41-msTeams.png",
        "",
        "Enable the Microsoft Teams Integration to view Rev Content in your MS Teams environment"
      ],
      "align": "center",
      "caption": "Enable the Microsoft Teams Integration to view Rev Content in your MS Teams environment"
    }
  ]
}
[/block]


When this option is enabled, your **Teams** tabs will be able to view:

- Rev Event Calendar
- Rev (VOD) videos
- Rev Categories

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4dcc65f-teamsChannelEmbed.png",
        "",
        "View Rev content directly in your Teams environment"
      ],
      "align": "center",
      "caption": "View Rev content directly in your Teams environment"
    }
  ]
}
[/block]


## Requirements

- Rev Cloud
- Microsoft Teams Admin access (for configuration only)

## Installation

For Vbrick Cloud tenants with a Vbrick-owned URL, you can install the app from [Microsoft AppSource](https://appsource.microsoft.com/en-us/product/office/wa200005272?tab=overview). For customers using customer-owned domains, you will need to install the application manually using the instructions below. In either case, you will first have to enable the integration in Rev.

> 📘 Note
> 
> If you disable the Microsoft Teams integration in Rev, Rev content is no longer displayed or shown on Microsoft Teams Channel tabs. However, the Rev tabs themselves remain until you manually remove them.

There are two different methods for installing the **Vbrick Rev Microsoft Teams Tab App**.  The first is by an Account Admins _only_ while the second method can be used by _all_ individual Rev Accounts (no Admin account required). Both methods are described below.

### Method 1: Account Admin Installation

Account Admins (Rev or MS Teams Admins) can add the Vbrick Rev App to a Microsoft Teams Channel Tab directly from Rev by enabling it and then downloading it from **Media Settings** > **Integrations**. Content that may be viewed includes the Rev Webcast Calendar, VOD videos, and Rev Categories.

> 📘 Note
> 
> Using this **MS Teams Channel** tab installation method means that only the Rev _Account Admin's_ portal may be used for content on the Channel tab. This is an important distinction. 
> 
> Other account types that have a valid email address in Rev and the Teams integration enabled in their Rev account may use the **Teams Apps** page (within MS Teams) to install the Vbrick Rev app to their specific Channels as well.

To enable an MS Teams Channel Tab from a Rev portal:

1. Navigate to **Admin > Media Settings > Integrations**.
2. Scroll to the **Microsoft** section.
3. Select the **Microsoft Teams Integration** checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/05c1dd0-msTeamsEnabled.png",
        "enableMsTeamsIntegration.png",
        802
      ],
      "align": "center",
      "caption": "Select the Microsoft Teams Integration checkbox to enable Rev content on Teams Channel tabs"
    }
  ]
}
[/block]


4. Click the **Download the Vbrick Rev app for Microsoft Teams** button and download the **Vbrick Rev app** zip file. Your **Microsoft Teams Admin** uses the zip file to add the Rev app to your Microsoft Teams tenant so that it can be used across _all_ teams. Alternatively, the application package can be uploaded for use with a _specific_ team.

> 👍 Tip
> 
> If you need assistance with installing a custom app in Microsoft Teams, please refer to the Microsoft Teams documentation. The following article may be of assistance:
> 
> - Tenant-wide Deployment: [Publish Apps in the Microsoft Teams Tenant Apps Catalog](https://docs.microsoft.com/en-us/MicrosoftTeams/manage-apps)
> - Specific Team Deployment: [Upload your package into a team using the Apps tab](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/apps-upload#upload-your-package-into-a-team-using-the-apps-tab)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9c63c7-revMsTeamsApp.png",
        "revMsTeamsApp.png",
        722
      ],
      "align": "center",
      "caption": "Rev appears in the Microsoft Teams tenant and can be added to Team Channels"
    }
  ]
}
[/block]


5. After the **Vbrick Rev app** is installed to your Microsoft Teams tenant (or to a specific team), you may add the new Rev tab to your Team channels. The Vbrick Rev tab enables you to:
   1. Share a list of upcoming **Rev Webcast events** with other members of the team.
   2. Share a **video **from the Rev VOD library.
   3. Share a Rev video **category **for quick access to all the videos in that category.
   4. Share a **Rev Channel’s** video collection for quick access to all the videos for that category.

**View**: [Accessing your uploaded configurable tab](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/apps-upload#accessing-your-uploaded-configurable-tab) for details on how to add tabs to your channel from a custom App.

### Method 2: MS Teams Apps Installation

For those users that are _not_ Account Admins that want to install the **Vbrick Rev** app to their specific MS Teams Channels, the app can be installed from the **Teams Apps** list from within MS Teams.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a6d98ff-msTeamsListing.png",
        null,
        "Search for the Vbrick Rev app to install to your Channel tab from the Apps list in MS Teams"
      ],
      "align": "center",
      "caption": "Search for the Vbrick Rev app to install to your Channel tab from the Apps list in MS Teams"
    }
  ]
}
[/block]


To enable an MS Teams Channel Tab from Microsoft Teams:

1. Click the **Apps** icon and search on **Vbrick Rev**.
2. Click the **Vbrick Rev** app to install it.

> 🚧 Important!
> 
> This method does _not_ work for customers who have their own Rev domain name.  Please contact your Vbrick CSM and Account Admin if you need assistance or are in doubt.
> 
> You must have Rev Cloud and a valid email in Rev with the MS Teams integration enabled before you can use this Channel tab installation method.  Otherwise, you will need to have your Account Admin install it directly from Rev.

3. You are prompted to add the app to an existing MS Team first.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/850b1f2-addRevtoMSTeam.png",
        null,
        "You will be prompted to add the Vbrick Rev app to an existing MS Team"
      ],
      "align": "center",
      "caption": "You will be prompted to add the Vbrick Rev app to an existing MS Team"
    }
  ]
}
[/block]


4. You will need to log in with a valid email account associated with a Rev portal. If you have access to more than one Vbrick Rev portal, click the **Verify** button.  You can then choose the portal you want to use by clicking the **Visit** link and the **Sign In** button.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f70948e-revAccountLogin.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


5. Once you select a Team, you are prompted to select a **Channel** to configure.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c02e0c5-addRevtoMSTeamsChannel.png",
        null,
        "You will select an initial Channel and begin setting up individual tabs"
      ],
      "align": "center",
      "caption": "You will select an initial Channel and begin setting up individual tabs"
    }
  ]
}
[/block]


6. You are then able to add your tabs as you normally would by adding the **Resource Type** and adding a **Tab Name**.
7. Use the type-ahead search function to view a list of what you can add from the **Vbrick Rev portal** that you signed in to.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6c8260f-addChanneltoMSTeams.png",
        null,
        "The Resource Type determines what Rev functionality appears on your new tab"
      ],
      "align": "center",
      "caption": "The Resource Type determines what Rev functionality appears on your new tab"
    }
  ]
}
[/block]


> 👍 Tip
> 
> When you select the **Post to Channel about this tab** checkbox all new content that is added to a tab, or even new tab creation itself, is announced in your channel to all your members so that they are aware of updates.

8. The Vbrick Rev-hosted content you select is embedded directly into the a new Teams Tab.  Example seen below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ad4c1a5-teamsChannelEmbed.png",
        null,
        "Rev content is embedded seamlessly into your MS Teams channel"
      ],
      "align": "center",
      "caption": "Rev content is embedded seamlessly into your MS Teams channel"
    }
  ]
}
[/block]


## View and Use the Vbrick Personal Tab in Teams

Once installation is complete and you are logged in, you are also able to view the** Vbrick Rev Personal **tab that displays the Rev tenant you have signed in to and directly mimics the Rev **Video** page UI itself.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6695731-addPersonalTab.png",
        null,
        "The Vbrick Personal Tab displays the VOD page of the tenant you log in to"
      ],
      "align": "center",
      "caption": "The Vbrick Personal Tab displays the VOD page of the tenant you log in to"
    }
  ]
}
[/block]


You can use the Vbrick Personal tab to **Search** for a specific tab or use the **Media** dropdown just as you would in Rev to view **My Videos** or **All Videos**.  If you have the correct permissions, you can use the **Upload** tray directly from your Microsoft Teams client to upload new videos.

You can right-click the **Personal Tab** to pin it to the left side of your app so it stays in place when you navigate away from the tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d93c6d9-pinPersonalTab.png",
        null,
        "Right+click on the app to pin it to your Personal Tab"
      ],
      "align": "center",
      "caption": "Right-click on the app to pin it to your Personal Tab"
    }
  ]
}
[/block]


> 📘 Note
> 
> You may need to reinstall the Vbrick Rev app to obtain this feature as with any new functionality that Rev has added.