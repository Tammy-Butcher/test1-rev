---
title: Accessibility Features
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
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
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

Vbrick Rev has many accessibility features implemented and continues to add improvements for people using assistive technology so that using Rev is an overall positive experience.  Vbrick is committed to aligning Rev’s interface with the [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.levelaccess.com/understanding-wcag/?utm_campaign=G_S_WCAG_NA\&utm_content=NB_WCAG_2.2_BM\&adset_id=154008223103\&utm_ad=751846716943\&ad_id=751846716943\&utm_id=20745927246\&campaign_id=20745927246\&keyword_id=kwd-1687131591764\&matchtype=e\&device=c\&GeoLoc=9009682\&IntLoc=\&placement=\&network=g\&utm_source=google\&utm_medium=cpc\&utm_term=web%20content%20accessibility%20guidelines%20wcag%202.2\&utm_campaign=G_S_WCAG_NA\&hsa_cam=20745927246\&hsa_grp=154008223103\&hsa_ad=751846716943\&hsa_src=g\&hsa_tgt=kwd-1687131591764\&hsa_kw=web%20content%20accessibility%20guidelines%20wcag%202.2\&hsa_mt=e\&hsa_net=adwords\&hsa_ver=3\&hsa_acc=4319570901\&gad_source=1\&gad_campaignid=20745927246\&gbraid=0AAAAADQ__bxkKUY1YhnY-_2jgcMphBcE9\&gclid=Cj0KCQjwndHEBhDVARIsAGh0g3CyNR8-aFmA_Kb8kpUmDxjxQwf65nva27GKMxsUI9uZW3g46SypGVUaAlSGEALw_wcB). This means ongoing improvements and updates to support accessibility for all users. For example:

* Ensuring all interactive components are accessible via keyboard
* Enhancing accessibility for captioned VOD content
* Ensuring color is not the sole means of communicating information

## Keyboard Navigation

Keyboard navigation and automatic tabbing is implemented in both navigation headers and in the VOD and Webcast sidebar flyouts.

* The `Tab` order proceeds through the navigation, sidebar tabs, and then the body content
* Navigate forward with `Tab`, using `Enter` to make a selection and arrow keys to navigate through content
* Pressing `Shift+Tab` highlights the previously highlighted content (goes back)
* You can use automatic keyboard tabbing to navigate through the following content/areas in Rev:
  * **Home** page carousel and all video pages such as **My Videos**, **All Videos** and **Search** result pages. 
  * Rev's [video player](doc:rev-video-player-features#tab-navigation-support) features

## Audio / Video Controls

Rev supports [closed captioning, transcription services, and subtitles](doc:update-advanced-video-settings#subtitles-translations-and-closed-captions) depending on what your Account admin has enabled and set up.

View the [video player support page](doc:rev-video-player-features) for details on where to toggle them.

## Colors and Contrast

When selecting your [theme colors](doc:apply-ui-branding-and-theme-colors), ensuring appropriate contrast is critical for accessibility. Check to ensure the following color pairs offer sufficient contrast:

* Primary Color and Primary Font Color
* Accent Color and Accent Font Color
* Header Background Color and Header Font Color

> 👍 Tip
>
> View additional accessibility features, such as the ability to change the **System Title**, on the [Customize the Browser Tab](doc:customize-the-browser-tab) topic.

## Browser Tab Accessibility Customizations

You can use the [System Title](doc:customize-the-browser-tab#add-a-custom-system-title) field under the **General Tab**  under the **Branding** menu to customize the Browser tab. It changes the default Vbrick system title and is used for accessibility purposes.
