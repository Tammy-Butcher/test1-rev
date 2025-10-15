---
title: Allow Local DME Accounts
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
[block:html]
{
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>&#128187; <a href=\"/docs/vbrick-distribution\">Vbrick Distribution</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]
Vbrick DMEs have their own account management system.  This allows Administrators to maintain the credentials independent of other systems.  While this is a legacy capability, we continue to support it for various customer use cases.  DMEs are configured with these accounts activated by default.

In **System Settings** under **DME Accounts** Rev provides the ability to allow Account Administrators to enable or disable the local accounts for DMEs v.3.27 and above.  This includes the local Admin and ReadOnly accounts, and impacts the ability to authenticate into VBAdmin (DME web interface).  Without local accounts, supporting features will not be available and they include VBShell (ssh interface), and supporting capabilities (FTP). 

Once disabled, access to the DME web interface VBAdmin will be authenticated by Rev (as the **Identity Provider (IDP)**.)  The DME v.3.27+ login page has a "Login using Rev" button which will redirect the user to their Rev instance (the one the DME is configured for), and after authentication, send the user back to the DME.  Only System Administrator accounts will be granted access to the DME using this method.     It should be noted, that this method of authentication by Rev into the DM is also available even if local accounts are enabled.

This optional feature supports security postures where local DMEs cannot have accounts.  
  
[block:callout]
{
  "type": "warning",
  "title": "Important!",
  "body": "This functionality requires **DME v3.27+** and **Rev v7.47+**.  In addition, **DME hostnames** must also be resolvable via DNS."
}
[/block]


For the example below, the Enable button is selected.  Note that the supporting text will identify the number of Account Administrators who will continue to have access to this DME.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c02b8c3-dmeAccounts.png",
        "dmeAccounts.png",
        1161,
        373,
        "#ececec"
      ],
      "caption": "When enabled, DME local accounts are used instead of using Rev as the Identity Provider in your ecosystem"
    }
  ]
}
[/block]
As a reminder, if you do not allow local DME accounts (disable this setting) then each DME that you want to use must be connected to Rev and only Account Admins are able to log into those DMEs.
[block:callout]
{
  "type": "danger",
  "title": "Caution!",
  "body": "If you disable this setting and also lose access to Rev, there is no way to authenticate to your DMEs."
}
[/block]


This is a account wide feature -- once set, it will apply to all DMEs.  However, we understand that there are times when you may want ssh or ftp access, or even just standard VBAdmin access.  For this case, we have provided an override on each of the REV DME pages called **Local Accounts Override**.   Please see [override this setting](doc:override-dme-local-account-setting) on *specific* DMEs if needed.