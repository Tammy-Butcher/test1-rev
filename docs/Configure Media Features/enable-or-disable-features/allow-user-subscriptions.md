---
title: Allow User Subscriptions
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
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


To globally enable users to subscribe to channel and category content , select the **Allow users to subscribe to channels and categories** checkbox under **Media Settings** > **Features** > **Video Settings**.  This setting is enabled by default.  

Keep in mind:

- Enabling this checkbox allows a user to subscribe to an individual [channel](doc:subscribe-to-a-channel) or [category](doc:subscribe-to-a-category) through a **Subscribe** button.  The button changes to **Unsubscribe** once subscribed to the **channel** or **category**.
- When subscribed, users receive an email and an alert via the [system notification](doc:notifications) tray when new content is available
- Users can also subscribe to a [Webex Teams](doc:webex-teams) category separately, if the integration is enabled.  Note that this integration does _not_ include channels.
- When subscribing to a category, only the top level category in the hierarchy is subscribed to.  **Subcategories** must be subscribed to separately.
- Users are not able to subscribe to **uncategorized** videos and only those videos they have permission to view may be subscribed to
- Users may view their subscription content feed on the [My Subscriptions](doc:my-subscriptions)  page
- If a user is removed from a channel, their subscription to the channel is also removed
- The user profile drop-down includes a [Manage Subscriptions](doc:manage-my-subscriptions) link that allows them to unsubscribe from a channel, category, or Webex Team subscription (if enabled)
- You may customize the [Home Page](doc:the-rev-home-page) with a **My Subscriptions** [carousel](doc:customize-the-home-page#customizing-home-page-carousels) if desired to display all subscription content that is specific to a logged in user