---
title: Allow User Subscriptions
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
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

To globally enable users to subscribe to channel and category content , select the **Allow users to subscribe to channels and categories** checkbox under **Media Settings** > **Features**.  This setting is enabled by default.  

Keep in mind:

* Enabling this checkbox allows a user to subscribe to an individual [channel](doc:subscribe-to-a-channel) or [category](doc:subscribe-to-a-category) through a **Subscribe** button.  The button changes to **Unsubscribe** once subscribed to the **channel** or **category**.
* When subscribed, users receive an email and an alert via the [system notification](doc:notifications) tray when new content is available
* Users can also subscribe to a [Webex Teams](doc:webex-teams) category separately, if the integration is enabled.  Note that this integration does *not* include channels.
* When subscribing to a category, only the top level category in the hierarchy is subscribed to.  **Subcategories** must be subscribed to separately.
* Users are not able to subscribe to **uncategorized** videos and only those videos they have permission to view may be subscribed to
* Users may view their subscription content feed on the [My Subscriptions](doc:my-subscriptions)  page
* If a user is removed from a channel, their subscription to the channel is also removed
* The user profile drop-down includes a [Manage Subscriptions](doc:manage-my-subscriptions) link that allows them to unsubscribe from a channel, category, or Webex Team subscription (if enabled)
* You may customize the [Home Page](doc:the-rev-home-page) with a **My Subscriptions** [carousel](doc:customize-the-home-page#customizing-home-page-carousels) if desired to display all subscription content that is specific to a logged in user
