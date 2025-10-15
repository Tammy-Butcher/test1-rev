---
title: View and Edit Account Details
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
The **Accounts ** menu under [Admin Menu Options](doc:admin-menu-options) consists of tabs and data created to assist Account Admins in maintaining Rev portal account setting information.

**Contact **and **Billing **data about your organization is entered and maintained here. **Note**: By default, Billing information is the same as Contact.  You can disable this on the Contact tab. **Licensing**, add-ons, and timezone attributes are also tracked here along with additional portal details.

Finally, **Child Accounts** are created here that can contain the features and functionality of the "main" portal (parent) account yet can also have separate user accounts, branding, and so forth.

To view your Vbrick Rev account information, click the **Edit** button on the **Contact** and/or **Billing** tab(s).  Each setting is described below.

## Account Name and Account Host Name Settings

The **Account Settings** section identifies the account name for your Vbrick Rev portal and also provides important information such as your **Account Host Name**, **Maximum File Upload Size**, and **User Provisioning** information.

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Account Name (Required)",
    "0-1": "The root (parent) account name. Normally the organization name.",
    "1-0": "Account Host Name (Required)",
    "1-1": "The IP or URL address of the account. Use extreme caution when changing. This field is tied to the FQDN that is initially set up upon installation of Rev. If this is modified, you need to provision the new DNS first and then point the new Account Host Name at the new DNS.  \n  \nIt is \\_strongly \\_recommended that you contact Vbrick Support Services if you need to modify this field since you could deny access to your Rev media management portal if you do not modify this field correctly.",
    "2-0": "Account Timezone",
    "2-1": "The timezone that the various time based settings of your Rev account will be based on.",
    "3-0": "Maximum File Upload Size",
    "3-1": "The maximum upload size (in GBs) allowed for file uploads to Rev.  Set to 0 if unlimited.",
    "4-0": "Enable User Provisioning",
    "4-1": "Display only, not editable in Rev-cloud. Used by Vbrick to [enable user provisioning](doc:configure-single-sign-on-sso#sso-with-user-provisioning) for use with SSO."
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]


## Account License Information

The **License Information** section provides information on what License Type you have purchased and what modules you have installed.

| Field               | Description                                                                                                                                                                                                            |
| :------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| License Type        | Specifies the [license type](doc:rev-license-types-and-add-ons) applied to your Rev account; Active Users, Concurrent Users, Named Users, Hours, or Distribution Hours.                                                |
| Modules             | Specifies if you have purchased the full Vbrick Rev client (default) or if you have purchased a separate [Vbrick Distribution](doc:vbrick-distribution) or [Vbrick Ramp eCDN](doc:what-is-the-vbrick-ramp-ecdn)module. |
| Licensed User Count | If your Rev account has a **Users** license applied, the number of user accounts that may be created on the account, including child accounts.                                                                         |
| Licensed Hours      | If your Rev account has an **Hours **license applied or add-on hours applied, the number of viewing/recording hours allotted, used, and expiration dates.                                                              |

## Video Daily Automatic Import Limit for an Account

The **Daily Automatic Import Limit (In Hours)** setting provides the total allowed hours versus what has been allocated for an account.

## Rev IQ Licensed Credits for an Account

This section displays the number of **Rev IQ Credits** that have been applied to the account along with the number used and expiration date.  

Rev IQ credits are used for [Facial Recognition](doc:facial-recognition) functionality. Three IQ credits are equivalent to 1 hour of Facial Recognition processing time.

## Vbrick Peer-to-Peer Account Settings

This section displays the **Peer Mesh Allotment** for [Vbrick Peer-to-Peer](doc:rev-connect-zones) (display only for Rev cloud) and the ability to enable **Vbrick Peer-to-Peer** zones.

## ECDN Options for Your Account

If the **Vbrick Ramp eCDN** checkbox is enabled in this section, Rev allows additional Ramp distribtuion elements (OmniCache nodes) and the ability to use Ramp distribution technologies with Rev.  Existing **Vbrick eCDN** features will continue to be available but only _one_ distribution type per Rev zone may be selected.

## Contact and Billing Details for an Account

| Field                    | Description                                                                         |
| :----------------------- | :---------------------------------------------------------------------------------- |
| First Name               | First name of your Rev portal manager.                                              |
| Last Name                | Last name of your Rev portal manager.                                               |
| Contact Email (required) | Must be in the format for a _valid_ email address ([xyz@abc.de](mailto:xyz@abc.de)) |
| Address Line 1           | Address line one.                                                                   |
| Address Line 2           | Address line two.                                                                   |
| Country                  | Country                                                                             |
| State                    | If Country is other than the USA, State will be a free-form text field.             |
| City                     | City                                                                                |
| Postal Code              | Zip Code / Postal Code                                                              |
| Phone Number             | Valid phone number where your Rev portal manager may be reached.                    |
| Preferred Language       | View [Supported Languages](doc:supported-languages)                                 |

# Portal Child Accounts

The **Child Accounts** functionality allows Account Admins to create a portal child account within the parent account domain. The advantage of this is that the child account acts as an entirely separate domain with its own set of users, groups, permissions, and roles. It functions and acts as its own entity which means that it also has different content as well since it has its own URL.

For example, you could make your root or parent account your corporate organization account and then create separate child accounts for each regional office with users, groups, content, and so forth applicable to each individual regional office (or child account).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/45da84f-childAccountsModule.png",
        "childAccountsModule.png",
        855
      ],
      "align": "center",
      "caption": "Child Accounts are entirely separate portal sites with the same functionality"
    }
  ]
}
[/block]


## Add a Child Account

Click the **Add Account** button in the **Child Accounts** section of the **Accounts **menu to create a new child account in your portal.

> ❗️ Warning!
> 
> You may create multiple layers of child accounts. However, be aware that admin access for managing child accounts is \_only \_accessible through the **parent ** Account Admins that create it. Admins of other domains are \_not \_able to access it including the Root Account Admins.

![](https://files.readme.io/e7f9ca4-addChildAccount.png "addChildAccount.png")

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Account Name (Required)",
    "0-1": "The account name. Normally the organization name. This may not be a duplicate name under the same parent account.",
    "1-0": "Account Host Name (Required)",
    "1-1": "The IP or URL address of the account. The host name must create a unique Web address across the entire root account.  \n  \nFurther, it may only contain lower case letters, numbers, and hyphens.",
    "2-0": "Timezone (Required)",
    "2-1": "The timezone that the various time based settings of your Rev account will be based on.",
    "3-0": "Enable User Provisioning",
    "3-1": "Specify if [user provisioning](doc:manage-security-parameters#sso-with-user-provisioning) should be enabled for SSO.",
    "4-0": "License Type (Required)",
    "4-1": "Specifies the [license type](doc:rev-license-types-and-add-ons) applied to your Rev account.",
    "5-0": "Licensed User Count (Required)",
    "5-1": "If your Rev account has a type of User license applied, the number of user accounts that may be created (or active) on the account.",
    "6-0": "Licensed Hours (Required)",
    "6-1": "If your Rev account has an Hours license applied, the number of viewing/recording hours allotted, used, and expiration dates."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "left",
    "left"
  ]
}
[/block]


Complete **Contact **and **Billing **information and if additional [add-on components](doc:rev-license-types-and-add-ons) have been licensed, you may allocate them as needed/desired.

Click **Create** to add the new child account.

## Navigating Between Child and Parent Account

Click the **Child Account** name in the **Accounts **column to switch to the child account where you may create entirely new Users, Groups, System Settings, and so forth if desired.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02777da-clickChildAccountName.png",
        "clickChildAccountName.png",
        806
      ],
      "align": "center",
      "caption": "Clicking a Child Account in the Accounts column immediately accesses Admin functions for that account"
    }
  ]
}
[/block]


A **Parent Account** dropdown menu option is created as well that allows you to switch back and forth between (all) child accounts once created.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3329077-childAccountMenu.png",
        "childAccountMenu.png",
        352
      ],
      "align": "center",
      "caption": "Use the Parent Account dropdown menu option to quickly access admin features of your Child Account(s)"
    }
  ]
}
[/block]


### Delete a Child Account

You can delete child accounts for your portal as long as the account does not have its own children. If you have an account hierarchy, you must delete from the bottom up (accounts without child accounts first).

Child Accounts are deleted from the Parent Account under the **Actions **column using the **Delete **tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/14e9bcd-deleteChildAccount.png",
        "deleteChildAccount.png",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


> ❗️ Warning!
> 
> This process is irreversible! **All **data and processes associated with the child account will be lost forever.
> 
> Child accounts do **not **share content with the parent account. The child account is a fully partitioned separate account. If you delete a child account, content on the parent account is not deleted.