---
title: Webex Teams
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


The **Webex Teams** integration provides a variety of functions with videos and Webcast events in Rev. Rev videos can be posted in a message link to a **Webex Team space** that then open in Rev when clicked by other users in the Team space. Users can **subscribe a Webex Team space** to a specific **Rev category** so that the Team space is alerted each time a video is added to that category with a message containing a link to the new video.

## Requirements

- Rev Cloud
- [Video Conference (VC) Integrations](doc:video-conference-vc-integrations) enabled
- [Cisco Developer Site](https://developer.webex.com/docs/integrations) log in with a **Webex Teams App** created.
- **Client ID** from the Webex Teams App after creation
- **Client Secret** from the Webex Teams App after creation

## Configuration

### Webex Teams App

Enter the following **Rev-specific required information** below during the creation of the Webex Team App.

[block:parameters]
{
  "data": {
    "h-0": "Webex Teams App",
    "h-1": "Rev Configuration",
    "h-2": "Example",
    "0-0": "Redirect URI(s)",
    "0-1": "`<Rev URL>/spark/oauth/cb`",
    "0-2": "`YourOrgsRev.com/spark/oauth/cb`",
    "1-0": "Scopes",
    "1-1": "`meeting:schedules_read`  \nRetrieve your Webex meeting lists and details  \n  \n`meeting:schedules_write`  \nCreate, manage, or cancel your scheduled Webex meetings  \n  \n`spark:all`  \nFull access to your Webex account",
    "1-2": "**Note**: If you have enabled the [Webex Meetings](doc:webex-meetings)  integration, you may use this same Teams App with the `spark:all` scope setting."
  },
  "cols": 3,
  "rows": 2,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


Click the **Add Integration** button to save the **Webex Teams App** and make note of the **Client ID** and **Client Secret** under the **OAuth Settings** section. 

> 👍 Tip
> 
> You can always return to your **Webex Teams App** by clicking your **Profile **image in the **Cisco Dev Center**.

### Rev Portal

Once your Webex Teams App is created, you can enable the integration in the Rev portal.

To enable the Webex Teams integration in Rev:

1. Navigate to **Media Settings** > **Integrations**.

2. Scroll to the **Webex Teams** section.

3. Select the **Webex Teams Integration** checkbox.

4. Enter the **Client ID** provided to you by the App in the **OAuth Settings** section.

5. Enter the **Client Secret** provided to you by the App in the **OAuth Settings** section.

6. Click the **Save **button.  You are now ready to use Webex Teams with Rev.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d396f1c-enableWebexTeams.png",
        "enableWebexTeams.png",
        782
      ],
      "align": "center",
      "caption": "Enable Webex Teams in Rev with information you retrieve from the App you create"
    }
  ]
}
[/block]


## Usage

### Stream a Scheduled Rev Webcast Event to a Webex Team

You can use **Webex Teams** as a _source_ for your Webcast event during event setup. When you select Webex Teams as a source, you may search from a list of teams that you belong to and you are _not_ required to enter a SIP address.

When a Webex Team event is scheduled:

- You must be logged in to at least _one_ **Webex Team** before you may proceed.
- You may switch to a different Webex Team by selecting the **Edit **button next to the selected Team. This causes the search control to appear again so that you may search on a different Webex Team.
- Once the event is created within a Webex Team space, a message in the space displays that the event has been scheduled.
- If the event has not yet started, a message displays a countdown of days, hours, and minutes (as applicable) until it starts.

To create a Webex Teams event in Rev:

1. Navigate to the **Events Calendar** and schedule an event as you normally would.

2. Search for a **Webex Team** as the **Video Source**.

3. You are prompted to log in before you may search for Webex Teams that you currently belong to in the search box.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/25fabc1-webexTeamsVideoSource.png",
        "webexTeamsVideoSource.png",
        1138
      ],
      "align": "center",
      "caption": "To schedule a Webex Teams event, you must select Webex Teams as the Video Source and then log in to a Team that you belong to"
    }
  ]
}
[/block]


4. Select a **Webex Team** that you want to use as the source. Note, this field is _not_ a drop-down. You must type in the name of the Webex Team that you want to use and Rev finds it for you.

5. The event synchronizes and broadcasts what is shared on the Admin or Host's screen to the selected **Webex Team window** once the event is started.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fd9b64c-webexTeamScheduledEvent.png",
        "webexTeamScheduledEvent.png",
        514
      ],
      "align": "center",
      "caption": "What is displayed on the Event Host or Admin's screen will stream to the selected Webex Team window once the event begins"
    }
  ]
}
[/block]


6. The event recording utilizes all of Rev’s standard event settings and features.

7. As noted, click the **Edit **control to the right of the Team name if you want to select a different Webex Team.

### Record a Webex Teams Meeting as a New Rev VOD

Similar to **Video Conference** recording, Rev Cloud also supports recording Webex Teams meetings and ingesting them into your standard media workflow with the **Webex Teams integration** enabled. The recordings capture both active speaker and any content streams (if available). Vbrick’s player displays both streams and allows user control of layout.

To record a Webex Teams meeting:

1. Click the **Live Recording** tab > **Webex Teams** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3837118-recordWebexTeams.png",
        null,
        "Click the Recording tab and then select the Webex Teams option"
      ],
      "align": "center",
      "caption": "Click the Recording tab and then select the Webex Teams option"
    }
  ]
}
[/block]


2. Type the team name in the** Select a Webex Teams Space** search box to select a Webex Team meeting to record (the teams you belong to appear to select from).

> 📘 Note
> 
> You are prompted to log in to Webex Teams before you are able to begin recording.

3. If a valid team is used, Rev connects and begins recording.

4. When the **Stop **button is pushed, Rev uploads the video to Rev and disconnects.

### Share a Video to a Webex Team Space

You can also share a video to a Webex Team space once you have enabled this integration.  A message with a link to the video appears in the space that, when clicked, opens the video in Rev.

To share a video to a Webex Team space:

1. Navigate to the video you want to share and click the [Sharing](doc:share-a-video) flyout to display sharing options that have been enabled.

2. Click the **Link **> **Share To Webex Teams** button.

3. If you want the video to play from the beginning, leave the **Start at:** checkbox unchecked. Otherwise, select the **Start at:** checkbox to specify where on the timeline you want to start sharing the video. To select a different time, deselect the checkbox, select a different time on the timeline, and then check the **Start at:** checkbox again to choose the new time (or enter it manually).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dfd0582-shareToWebexTeamsButton.png",
        "shareToWebexTeamsButton.png",
        392
      ],
      "align": "center",
      "caption": "Click the Share To Webex Teams button to share the video to the Team space"
    }
  ]
}
[/block]


4. You are prompted to log-in to Webex Teams if you are not already logged in. You are also required to grant permissions to **post **and **delete ** the first time you attempt to either subscribe to a category or share a video to the Webex Team space. This is a one-time occurrence and you are only required to grant this permission once.

5. Once logged in, select the **Webex Team space** you want to link the video to in the **Select a Webex Team Room** drop-down. All Webex user spaces you belong to appear in this drop-down.

6. You are also able to attach any additional messaging you want to note about the video in the **Your Message** text box.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/10fb476-shareVideoToWebexTeams.png",
        "shareVideoToWebexTeams.png",
        534
      ],
      "align": "center",
      "caption": "Select the Webex Team(s) and enter any messaging you want to pass along before you send the video to the Webex Teams space"
    }
  ]
}
[/block]


7. A link to the video, along with any message you entered, appears in the Webex Team space you select. Any user in the same room may click on the hyperlink to view the video.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d2ddf7c-sharedVideoinWebexTeams.png",
        "sharedVideoinWebexTeams.png",
        471
      ],
      "align": "center",
      "caption": "The message and a link to the shared video displays in the Webex Teams space(s) you selected"
    }
  ]
}
[/block]


Notes about sharing video to Webex Teams and Rev permissions:

- The video must be in **Active **status to be shared.
- Rev permissions are still applied when users view a video. That means, if the video is **Public**, users can view the video without logging in. If not, viewers are prompted to log in prior to accessing the video. Further, if the user has not been granted permission to view the video, the user is _not_ able to do so regardless of logging in.
- You _must_ be logged in to the Webex Team space to post to the room. If you leave the space, you are _not_ able to post to the space.

### Subscribe a Rev Category to a Webex Team Space

You can subscribe a Rev category to a Webex Team space once you have enabled this integration. This means that when a video is added to a category, Webex users with access to the space are notified that a new video has been added to that category and they are also able to view a feed of that content under [My Subscriptions](doc:my-subscriptions).

To subscribe a Rev category to a Webex Team space:

1. Navigate to the category you want to subscribe to through **Media** > **Browse Categories**.

2. Click the **Subscribe** button.

3. Click the **Subscribe via Webex Teams** toggle.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/568cb32-subscribeCategoryToWebexTeams.png",
        "subscribeCategoryToWebexTeams.png",
        1814
      ],
      "align": "center",
      "caption": "When you subscribe a category to a Webex Team, each time a new video is added to the category, the Team space is alerted"
    }
  ]
}
[/block]


4. You are prompted to log-in to Webex Teams if you are not already logged in. You are also required to grant permissions to **post **and **delete ** the first time you attempt to either subscribe to a category or share a video to the Webex Team space. This is a one-time occurrence and you are only required to grant this permission once.

5. Once logged in, select the Webex Team space you want to subscribe the category to in the **Select a Webex Teams Space** drop-down. All your Webex Team spaces appear in this drop-down.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/198ad23-webexTeamsDropdown.png",
        "webexTeamsDropdown.png",
        687
      ],
      "align": "center",
      "caption": "All Webex Teams you are a member of appear in this dropdown once you are logged in"
    }
  ]
}
[/block]


6. The Webex Team space you select is notified each time a new video is added to the category.

7. Click the **Unsubscribe** button in the **Browse Categories** form to stop the category subscription at any time.  You may also view and unsubscribe from the [Manage Subscriptions](doc:manage-my-subscriptions) page.

Notes on subscribing categories to a Webex Team:

- If a category is deleted, the subscription is removed.
- Subcategories are not subscribed to by virtue of subscribing to the category. To subscribe to the subcategory, you must go directly to the subcategory page and subscribe it independently of the parent category.
- Category subscriptions are _user-based_. This means that:
  - More than one person can subscribe a Webex Team space to the same category. _If multiple users subscribe the same category to the same space, multiple messages will appear in the space_.
  - If the user that subscribed to a category leaves the Webex Team space, updates are no longer posted to that space (the Webex APIs prevent users from posting to spaces that they are not in).
  - If the user that subscribed the category is suspended, the category is unsubscribed and updates are no longer be posted to the Webex space unless another user has also subscribed the category.
  - Users can only subscribe a category to **one** Webex Team space at a time.

## Best Practices When Working with Webex Teams

Webex Teams is a cloud based enterprise collaboration suite. Rev can stream/record an existing call that has originated within a Webex Team space with the following caveats:

1. Vbrick Rev requires that a Webex Team space must have at least _one_ active video participant before the streaming/recording is initiated from Rev. Starting streaming/recording to an inactive space may produce poor to failed video.
   - **Best Practice**: Have at least one participant in the space at least **30 seconds** before initiating the streaming/recording on Rev.

2. Vbrick Rev does not support Webex Team Point-to-Point calls – these are calls directly to a Webex Team user. Vbrick Rev supports Webex Team space calls and direct calls to H/W endpoints.

3. Webex allows participants to “take over” the content share if another participant is sharing. In rare occurrences, Webex does not forward the new content share.
   - **Best Practice**: When multiple participants utilize content to share, each participant should end their content share before the next participant begins sharing.
   - **Note**: If your content share is not showing, stop your content share and then restart it to fix.

4. Lastly, the **Webex Team SIP address**, required to initiate a call from Rev to a Webex Team space, can be found on the **Schedule a Meeting** page on the WebEx Teams application, under **Join by video system**.