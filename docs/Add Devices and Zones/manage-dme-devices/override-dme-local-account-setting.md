---
title: Override DME Local Account Setting
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

As a reminder, Account Administrators can disable all local accounts on their DMEs as a global account setting.  This directs all DMEs to enable/disable the accounts -- and new DMEs added later will honor the setting as well.  

This setting can be overridden on a DME-by-DME basis (to turn it on specifically) on the Rev DME page.  To override the global [DME Accounts](doc:dme-accounts) setting for a specific DME once you have added and saved it, use the **Local Accounts Override** setting.

<Image title="dmeAccountsOverride.png" alt={913} src="https://files.readme.io/d58e91b-dmeAccountsOverride.png">
  This setting allows you to override the global DME Accounts setting on a specific DME
</Image>

If your system has local accounts disabled, but you need local account access -- then use this feature to enable local accounts.  Vbrick *does* recommend, however, that you reset it back to **Use System Default** when your access is no longer needed.

This setting is only available on DMEs with v3.27+ installed.  

> 🚧 Caution
>
> If this setting is disabled the DME may not be deleted.
