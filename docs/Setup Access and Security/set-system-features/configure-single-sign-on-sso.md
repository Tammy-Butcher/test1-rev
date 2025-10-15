---
title: Configure Single Sign On (SSO)
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
Rev provides Single Sign On (SSO) functionality via the SAML 2.0 protocol. Use the **Single Sign On** section to configure Rev as the SAML Service Provider if you are using an Enterprise SSO system set up and want to configure it for use with your enterprise Identity Provider server. You should be familiar with SAML and SSO deployment methods before attempting to configure the fields below.

A good, high level overview may be reviewed on the Eclipse open source [SAML2](https://wiki.eclipse.org/SAML2_IdP_Overview_1.0) wiki page.

> 📘 Note
> 
> Rev also provides Single Sign On (SSO) with user provisioning so that user accounts may be created upon log-in \_without \_the need for an LDAP connector deployment. See: Configure Single Sign On (SSO) with User Provisioning Enabled.
> 
> User provisioning must be enabled on the root account by Vbrick Support Services before this feature may be used.

To configure single sign on, navigate to the **Admin >  System Settings > User Security** menu:

1. Scroll to the **Single Sign On** section.
2. Select the **Enable Single Sign On** checkbox and complete the fields that appear.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/38843d0-singleSignOn.png",
        "singleSignOn.png",
        1173
      ],
      "align": "center",
      "caption": "Single Sign On, No User Provisioning"
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Setting",
    "h-1": "Description",
    "0-0": "Enable Single Sign On",
    "0-1": "Select to enable Single Sign On",
    "1-0": "User Provisioning",
    "1-1": "Used to enable **Single Sign On with User Provisioning**.  This checkbox must be configured and enabled by Vbrick Support Services first before it is visible.",
    "2-0": "SAML Identity Location",
    "2-1": "Choose either the **NameIdentifier Element** or **Attribute Element **depending upon which element in the SAML Authentication Response will have the username.  \n  \nNote that if you select **Attribute Element** (default), you must provide the **Identify Attribute Element Name** or Rev will not authenticate.",
    "3-0": "Identity Attribute Element Name",
    "3-1": "If **Attribute Element** is selected as the **SAML Identity Location**, this field must be completed or SSO will not work.  \n  \nThe **Identity Attribute Element Name** is the field in the **SAML Authentication Response (XML) **that contains the username.  \n  \nFor example, in the code below, name is specified as **SFDC_USERNAME**. This is what would be pasted in **Identify Attribute Element Name** field in Rev, as seen in the image above.  \n  \n\\<saml:AttributeStatement>  \n\\<saml:Attribute FriendlyName=\"fooAttrib\" Name=\"**SFDC_USERNAME**\" NameFormat=\"urn:oasis:names:tc:SAML:2.0:attrname-format:unspecified\">  \n\\<saml:AttributeValue xmlns:xs=\"<http://www.w3.org/2001/XMLSchema>\" xmlns:xsi=\"<http://www.w3.org/2001/XMLSchema-instance>\" xsi:type=\"xs:string\">  \n[user101@salesforce.com](mailto:user101@salesforce.com)  \n\\</saml:AttributeValue>  \n\\</saml:Attribute>  \n\\</saml:AttributeStatement>",
    "4-0": "Identity Provider Metadata",
    "4-1": "Paste your **Identity Provider** server’s metadata XML code in this field. You need to obtain the Identity Provider metadata (XML) from your Identity Provider server.",
    "5-0": "Signature Algorithm",
    "5-1": "Options to be used for signing. Select either **SHA1withRSA** or **SHA256withRSA**.",
    "6-0": "Sign SAML Request",
    "6-1": "Only enabled when the URL of the redirect exceeds 2048 characters which may occasionally cause issues with Internet Explorer or IIS/ADFS. Be aware that checking and un-checking this box will require the service provider metadata be re-downloaded to get the latest version again once saved. Contact Vbrick Support Services for assistance with this option.",
    "7-0": "Download Service Provider MetaData",
    "7-1": "This is the Rev Service Provider XML metadata that is provided to the Identity Provider server. It should be downloaded and used with the IDP server similar to how the IDP’s metadata XML is pasted in the **Identity Provider Metadata** field above.",
    "8-0": "Regenerate Cert",
    "8-1": "This will regenerate the **Service Provider’s** certificate and metadata. If you decide to do this, keep in mind you will need to download the Service Provider MetaData again for re-insertion into the IDP server."
  },
  "cols": 2,
  "rows": 9,
  "align": [
    "left",
    "left"
  ]
}
[/block]

The diagram below represents the technical implementation of SSO in Rev.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3daddfe-ssoTechDiagram.png",
        "ssoTechDiagram.png",
        626
      ],
      "align": "center",
      "caption": "Technical implementation of SSO in Rev"
    }
  ]
}
[/block]

- If SSO is enabled without user provisioning, user accounts must be created in Rev manually or through the LDAP connector.
- If an Account Admin creates a user account manually with SSO enabled, the user created is set to **Unlicensed **status until log in and then set to **Active **status. No user or email confirmation is required. If no licenses are available for the Rev account, the user is displayed a message to contact the Account Admin and will not be logged in.
- When SSO is enabled, an SSO login page is created for authentication that is different from the native Rev login page. For example:
  - Rev Native Login Page:http\:/<RevURL>/#/login
  - SSO Login Page: http\:/<RevURL>/SSO/login

### SSO with User Provisioning

Rev provides **Single Sign On (SSO) with user provisioning** so that user accounts may be created upon log-in _without_ the need for an LDAP connector deployment.

To do so, SSO is configured exactly as described above along with additional **Identity Server Provider** fields to map to Rev fields for user account creation.

> 👍 Tip
> 
> This feature must be enabled on the root account by Vbrick Support Services before you may configure SSO with user provisioning.
> 
> You can check this by navigating to the **Accounts **menu and then selecting the **Edit **button on the **Contact **tab to see if the **Enable User Provisioning** checkbox is selected. If it is disabled, you will not be able to select the checkbox in System Settings to configure it and you must contact Vbrick Support Services.

Once the **User Provisioning** checkbox is enabled and selected, the following additional fields should be completed for SSO configuration:

[block:parameters]
{
  "data": {
    "h-0": "Setting",
    "h-1": "Description",
    "0-0": "First Name Attribute Element Name",
    "0-1": "The first name of the user account.",
    "1-0": "Last Name Attribute Element Name",
    "1-1": "The last name of the user account. Similar to **Identity Attribute Element Name** above, this is a required field and must be completed in order to authenticate correctly.",
    "2-0": "Email Attribute Element Name",
    "2-1": "The email of the user account. Similar to **Identity Attribute Element Name** above, this is a required field and must be completed in order to authenticate correctly.  \n  \nCorrect email format must also be used and the field must be unique.",
    "3-0": "Title Attribute Element Name",
    "3-1": "The title of the user account.",
    "4-0": "Phone Attribute Element Name",
    "4-1": "The phone number of the user account."
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]