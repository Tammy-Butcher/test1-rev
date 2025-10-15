---
title: Customize the Home Page
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
Access Rev's Branding options through the **Admin > System Settings > Branding** menu option.

[The Rev Home Page](doc:the-rev-home-page) is displayed when a user first logs in. Rev considers the **Home Page** comprised of three parts:

a. Header\
b. Featured Video Carousel\
c. Home Page Carousels

You can customize the [Header](doc:customize-the-portal-header) and [Featured Video](doc:customize-the-featured-video-playlist) look and feel with optional template selections.

You can do the same with the Home Page itself and the **Home Page Carousels** that are displayed by choosing different template options under the **Home Page** tab on the **Branding** menu.

## Classic Home Page Template

The **Classic Home Page** template is the default template until changed. You may display up to seven carousels that appear stacked under the **Featured Video** playlist.

<Image title="classicHomePagePreview.png" alt={1075} align="center" src="https://files.readme.io/d1bd0c5-classicHomePagePreview.png">
  Preview of the Classic Home Page template with default carousels displayed
</Image>

## Carousels With Sidebar Home Page Template

When this template is selected, you must select from 3 sidebar sections in addition to your carousels. The **Sidebar** sections appear to the right of your carousels and under your **Featured Video**.

<Image title="sidebarHomePagePreview.png" alt={1151} align="center" src="https://files.readme.io/5ea5dbd-sidebarHomePagePreview.png">
  Preview of the Carousels With Sidebar Home Page template with 2 sidebars selected; Channels and Events.
</Image>

The sidebar selections that may be made are:

* **Events** (Upcoming events specific to the User's access levels)
* **Channels** (Specific to the logged in user’s channels only)
* **Categories** (Top level category display only if categories are enabled)
* **None** (no sidebar is displayed)

<Image title="homePageSideBar.png" alt={352} align="center" src="https://files.readme.io/0af2738-homePageSideBar.png">
  Select what items appear in the Sidebar when choosing the Carousels With Sidebar Home Page template
</Image>

> 📘 Note
>
> The first Home Page Sidebar dropdown is **required** and may *not* be set to **None** similar to the first carousel option.

## Customizing Home Page Carousels

### Setting Carousel Display Order

Up to seven carousels may be configured to appear on the Home Page. Four are displayed by default:

* **Recently Added Videos**
* **Upcoming Events**
* **Recommended for You** - Displays video recommendations based on popularity, freshness, and the user’s viewing history.
* **Continue Watching** - Includes videos that have only been partially viewed. Those videos that have been completely viewed are not displayed

### Additional Carousel Display Options

You can reorder carousels as needed.  You can also set additional display options on some carousels:

* **Channel Videos** - Displays all the videos of the selected Channel. You may select multiple Channel Video carousels to display on the Home Page if desired.
* **Channel List** - Displays the Channels the user is a member of, if applicable. No Channel is displayed if the user is not a member of a Channel.
* **Playlist** - All playlists \[a user] creates and the **Featured Playlist** available to set in this field. Note that both **Static** and **Dynamic** playlists can be set here.
* **Subscriptions** - Displays content that a user has [subscribed](doc:my-subscriptions) to if enabled.

> 👍 Tip
>
> The carousels display in the order you select in the dropdowns. To disable the carousel, select **None**.  Setting a carousel to **None** results in it not displaying.

### Setting Carousel Sort Order

The following types of carousels on the Home Page can have their sort order modified:

* **Category**
* **Live Videos**
* **Channel Videos**

![](https://files.readme.io/11ce4d2-applySortOrder.png)

Selecting the above type of carousel allows you to apply a sort order to it in a dropdown below it.  The sort order options are:

* Recommended (default)
* Upload Date
* Views
* Title

### Carousel Usage Tips

* One carousel is *always* required and may not be set to None
* The same value may *not* be set in more than one carousel
* The same category or channel may *not* be selected for multiple carousels
* Carousel videos are sorted based on the user’s viewing history first and then by videos that are more popular and recently uploaded.
* If **Continue Watching** is set as a carousel, and a video is accessed as a direct link (rather than the carousel), keep in mind that the progress is not displayed as opposed to if it is accessed via the Continue Watching carousel.

> ❗️ Warning!
>
> Be aware that the [Access Control](doc:update-basic-video-settings#video-access-control) level of the videos in the selected carousel are in effect. In other words, if you add a **Private** video to a carousel, some users may not be able to view it based on their permissions/access.
>
> If the [Add URLs](doc:enable-or-disable-features#allow-videos-added-via-url) option has been disabled in **Media Settings**, you will not be able to add a **Live Videos** carousel as a Home Page setting.
