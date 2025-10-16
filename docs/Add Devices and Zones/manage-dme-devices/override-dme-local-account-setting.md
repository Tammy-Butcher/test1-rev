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
As a reminder, Account Administrators can disable all local accounts on their DMEs as a global account setting.  This directs all DMEs to enable/disable the accounts -- and new DMEs added later will honor the setting as well.

This setting can be overridden on a DME-by-DME basis (to turn it on specifically) on the Rev DME page.  To override the global [DME Accounts](doc:dme-accounts) setting for a specific DME once you have added and saved it, use the **Local Accounts Override** setting.

<Image alt={913} border={false} caption="This setting allows you to override the global DME Accounts setting on a specific DME" title="dmeAccountsOverride.png" src="https://files.readme.io/d58e91b-dmeAccountsOverride.png" />

If your system has local accounts disabled, but you need local account access -- then use this feature to enable local accounts.  Vbrick _does_ recommend, however, that you reset it back to **Use System Default** when your access is no longer needed.

This setting is only available on DMEs with v3.27+ installed.

> 🚧 Caution
>
> If this setting is disabled the DME may not be deleted.
