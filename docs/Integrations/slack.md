---
title: Slack
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


Vbrick integrates with **Slack ** via a provisioned server setup, Vbrick's Slack app, and Slack bot creation. Once installed, you can:

- **Search** for Vbrick-hosted videos directly within a Slack channel without needing to leave the channel.
- View a Vbrick-hosted **video** in a Slack channel using its **URL** or in the channel itself using the **Share** tab.  The video can be **Public** or **Private**.  If it contains a password, users are redirected to the Vbrick web player to complete authentication first before they may view the video.
- View a Vbrick-hosted **webcast** in a Slack channel using its **URL** or in the channel itself using the **Share** tab.  The event can be **Public** or **Private**.  If the webinar requires registration, attendees are prompted to sign-in and register before attending the event. If the attendee is already registered, they will join the event immediately.

## Requirements

- Vbrick Rev Cloud Admin account
- Slack Developer account
- Admin approval is required to add a Vbrick video Slack bot to a Slack workspace or channel after you install the integration
- Rev API Key and Secret (used when creating and configuring a Slack bot)
- JWT authentication
- Allow Sharing of Metadata for Private Videos must be enabled in Rev

## Installation

To enable and install the **Slack** integration with Vbrick Rev:

1. Configure Rev Tenant settings:
   1. Create an [API Key](doc:create-an-api-key) in Rev for use with Slack. Note the **key** and **secret** for when you configure the Slack bot later during this installation.
   2. [Enable](doc:enable-jwt-authentication) and add a new [JWT authentication](ref:jwt-authentication) certificate.
   3. Navigate to **Admin** > **System Settings** > **Content Restriction**.  Scroll to the **Sharing and Embedding** section. Make sure [Allow Sharing of Metadata for Private Videos](doc:private-metadata-sharing) is enabled.

2. Provision Slack App server, download the app and configure settings for Slack integration. Navigate to the [Vbrick GitHub](https://github.com/vbrick/slack-app) for detailed instructions and examples.

> 🚧 Important!
> 
> An Account Admin must perform the installation steps.

3. Configure the slash / command you want to use for your channel for the video-search app.  For the purposes of this topic, we are using`/video-search` but you can use something specific to your organization if you prefer.
4. You will be able to create the command on the [App Management](https://api.slack.com/apps) page of your Slack Developer account.
5. For details view the [Implementing Slash Commands](https://docs.slack.dev/interactivity/implementing-slash-commands) documentation on Slack.

### Add the Slack Bot to your Slack Workspaces and Channels

Once you have installed the Slack integration and configured your Slash command, next you need to add the Slack Bot to your Slack workspaces and channels.  There are a few different methods to achieving this.

1. Navigate to a Slack channel.
2. Click the **More Actions** menu in the upper right menu and then click **Edit Settings**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/641b0ada1004029b795a1c70cde858814cbb3ac02954b35661f4f9a323873c36-slackEditSettings.png",
        "",
        "Edit Settings allows you to add a Slack bot to an entire workspace"
      ],
      "align": "center",
      "caption": "Edit Settings allows you to add a Slack bot to an entire workspace"
    }
  ]
}
[/block]


3. Click the **Integrations** tab > **Add an App**.
4. Search for the name or partial name of the slash command you configured in the previous section in the **Search** box.
5. You are then able to add the slash configurations you set to appear for your tenant in the workspace of your choice. Click the **Add** button next to the app and workspace you want to add the Slack bot to.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d9dfd1c9867b31f07dafd47702f4bc6dc50eb3703aafe8ef358d786c46f0f31c-addSlackApps.png",
        "",
        "Click the Add button next to app and workspace to Add the selected Slack bot"
      ],
      "align": "center",
      "caption": "Click the Add button next to app and workspace to Add the selected Slack bot"
    }
  ]
}
[/block]


6. If you would rather add the bot directly to a specific **Channel** instead, navigate directly to the channel and type `@your-bot-slash-name` to "invite" the Slack bot to the channel directly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/723ffac2c5d768ef64d56dcb6ca8bc7a509214e87507c54d4880d39064962603-inviteBot2Channel.png",
        "",
        "Invite the slack bot with the @symbol. Use the slash name you gave it during installation."
      ],
      "align": "center",
      "caption": "Invite the slack bot with the @symbol. Use the slash name you gave it during installation."
    }
  ]
}
[/block]


## Usage

Once the Vbrick app and bot are installed to your particular workspaces and channels, you are ready to search and view videos and events.  Each use case is described below.

### Search for Vbrick-Hosted Videos in Slack

To search for a Vbrick-hosted video:

1. Type the command `/video-search` (or whatever you named your app) followed by a search term such as the name of the video.
2. If there are no results, a "No results found" message is returned.
3. Otherwise, the top 20 results are returned in a video pop-up sorted by Title.
4. You are able to view the video of your choice in the pop-up or click the **Share in Channel** button to share the video with the rest of the Slack channel.  
5. For example, `/video-search ecdn` might yield the result below using our test case.  Notice that `ecdn` is in the title name.  Other match cases are listed below the top result.
6. You can play and view the video directly in the window or you can click the **Share in Channel** button to share it with the rest of the channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/34d6f3591aa40f8fa8f60b92bd58af12a2d1441ee37c6e7062c4d2608e06953b-searchResults.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


### View Vbrick Videos in Slack

There are two methods to view videos in a Slack channel:

1. Search for and then view the video as described in the [Search usage](doc:slack#search-for-vbrick-hosted-videos-in-slack) section above.
2. Copy the video URL from Rev and then paste it in the Slack channel. You can also use the video **Share** flyout panel and the **Copy** button to obtain its URL.  Either method yields the same result that can be pasted into the Slack channel for viewing.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0288853d0e81d289605626cfcb824fcf5c35c77f5f97e6d9d4197c7d7a8ca1cc-shareFlyoutCopy.png",
        "",
        "Obtain the video's URL in Rev to paste in the Slack channel"
      ],
      "align": "center",
      "caption": "Obtain the video's URL in Rev to paste in the Slack channel"
    }
  ]
}
[/block]


3. Once you have found the video you want to view by either method above, it appears in a pop-up modal with two viewing options:
   1. Click the **Play** button. This plays the video directly in the pop-up modal for you to view.
   2. Click the **View on Web** button.  This opens the video in the Rev player.
4. If the video that is shared is **Private** (assuming the tenant allows private metadata sharing), an **Authenticate** button displays before the video may be viewed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9a28e1493b1b76a02e3c87461249e11ba71562701222110688bc4329c4b0e231-privateVideoShared.png",
        "",
        "If Private videos are shared, viewers must Sign In to Rev first before viewing"
      ],
      "align": "center",
      "caption": "If Private videos are shared, viewers must Sign In to Rev first before viewing"
    }
  ]
}
[/block]


5. As noted above, if the video requires a password, viewers will also be redirected to Rev to enter the password before they may view it.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74ff46f957624da367c57ff0e0462c6eac8d8749a734b43a06c5945ee4b1048d-passwordVideoShared.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


> 🚧 Important!
> 
> The video must be **Active** or it will not appear in search returns.

### View Vbrick Live Webcasts in Slack

Similar to videos, you can share a webcast in a Slack channel using the same two methods of copying and pasting the **URL** or by using the **Event Details** flyout panel during the webcast to share the webcast link. The Slack integration supports both **Public** and **Private** events (anonymous, password, and registration required).

1. Navigate to the event you want to share by copying its **URL** to the Slack channel or by using the share link on the **Event Details** flyout panel once it is being broadcast. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de2718f73f03bda2a357b45bbc657a973ff84a79e5998774a8a83e773d53da23-eventDetailsFlyout.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


#### View a Public Event Anonymously in a Slack Channel

1. If the webcast is a **Public** event that you are joining **anonymously**, it appears displaying its title in a pop-up modal.
2. At the bottom of the window, a **Join on Web** button is displayed.
3. Clicking this button opens it in the default Web browser, allowing you to join and participate.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/14b9f4c31ef1433ab07dd6f2eb4f85bd4f1bf20643472c4d0f3fa344c7ec4b88-joinPublicAnon.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


#### View a Public Event that Requires Registration in a Slack Channel

1. If the webcast requires registration before viewing, the webcast title appears in a pop-up modal with two buttons that display: **Sign In** and **Register**.
   1. If **Sign In** is clicked and the user has access, the event opens with a **Join on Web** button.  Assuming the user is authenticated, the user joins the webcast on the default browser when this button is clicked.
   2. If **Register** is clicked, a link to **Register Now** opens in the default browser allowing the user the register before they may join the event.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/128bb7997283ef087d8b09d89e330be5fa788bde58c3c314f22acac6174ec317-joinPublicRegister.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


#### View a Private Event in a Slack Channel

1. If a **Private** event is shared in a Slack channel a message is displayed stating: "Sign in to join this private event." along with a **Sign In** button.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db1eacc2a4899d3f4b36998e961dd04e00cb05615ef9b61d3aa8bb29032dcc34-joinPrivate.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


2. If the user has access to view the event, the webcast title and player is displayed along with a **Join on Web** button when the Sign In button is clicked.
3. They are then are able to join the event once authenticated.