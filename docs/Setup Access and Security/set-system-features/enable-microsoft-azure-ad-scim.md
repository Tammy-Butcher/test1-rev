---
title: Enable Microsoft Azure AD SCIM
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
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>&#128187; <a href=\"/docs/vbrick-distribution\">Vbrick Distribution</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


Vbrick Rev supports integration of the **System for Cross-Domain Identify Management** (SCIM) user management API to enable automatic provisioning of users and groups between **Vbrick Rev** and **Azure Active Directory** (Azure AD). Once configured, Azure AD automatically provisions and deprovisions users and groups to Rev.

## Prerequisite Criteria

Before enable **Microsoft Azure AD SCIM** in Rev and begin configuration, review the following criteria to make sure you understand program features and criteria.

- You should have access to your **Azure Active Directory Administrator** who can install the Vbrick Rev Cloud application.

> 🚧 Important!
> 
> If you already have an [LDAP Connector](doc:add-ldap-connector-device) configured in Rev you need to ensure that the **SAMAccountName** in your **Active Directory (AD)** matches the **Username** in **Azure AD**. Further, you should _not_ have both LDAP Connector and Azure SCIM provisioning enabled simultaneously.  View the scenarios below.

### Configuration Scenarios

| Customer Type                      | Existing LDAP Connector | Existing SAML SSO | Existing LDAP Login | Action                                                                                                                                                                                                                                                       |
| :--------------------------------- | :---------------------- | :---------------- | :------------------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Existing Vbrick Rev Cloud Customer | Yes                     | Yes               | No                  | 1. Disable **LDAP Connector**  2. Install **Vbrick Rev Cloud App** in Azure AD.  3. Configure **User and Group provisioning** in the App.4\. Existing **SAML SSO** should work but you can also configure SAML SSO in the same App.                          |
| Existing Vbrick Rev Cloud Customer | Yes                     | No                | Yes                 | 1. Disable **LDAP Connector**. This also disables the LDAP login.  2. Install the **Vbrick Rev Cloud App** in Azure AD.  3. Configure **User and Group provisioning** in the App.4\. Configure **SAML SSO** in the App.                                      |
| Existing Vbrick Rev Cloud Customer | No                      | Yes               | No                  | 1. Install **Vbrick Rev Cloud App** in Azure AD.  2. Configure **User and Group provisioning** in the App if you want automated user and group sync from Azure AD.3\. Existing **SAML SSO** should work but you can also configure SAML SSO in the same App. |
| New Vbrick Rev Cloud Customer      | No                      | No                | No                  | 1. Install **Vbrick Rev Cloud App** in Azure AD.  2. Configure **User and Group Provisioning** in the App.3\. Configure **SAML SSO** in the same App.                                                                                                        |

## Rev Configuration

Once you have disabled all LDAP Connectors and have reviewed your configuration scenarios, you are ready to configure the integration:

1. Navigate to **Admin > System Settings** > **User Security** and scroll to the **SCIM Configuration** section.
2. Click the **Enabled** checkbox next to the **Enable SCIM** setting.  Select **Azure** from the dropdown in the provider setting. You are now ready to generate your token.  Keep in mind you will need to copy and save the token and the URL that are generated in the next step.

   [block:image]{"images":[{"image":["https://files.readme.io/8e74c36d11ffbdcb0786fbfd1e2b684779a117e3e014a0b3949c931adc1a3c8b-image.png",null,"Make sure you copy the token you generate in this section"],"align":"center","caption":"Make sure you copy the token you generate in this section"}]}[/block]

   <br />
3. Click the **Generate Token** button. **Copy** the token that is generated and then click **Ok**. Make sure you keep the copied token somewhere you can access it again.

   [block:image]{"images":[{"image":["https://files.readme.io/6210b0cff30b2001b78a27a8e9c295694b29c09ee2ecd440e3284e67eef8a225-image.png",null,"The SCIM token is needed when you configure your Azure App"],"align":"center","sizing":"90% ","caption":"The SCIM token is needed when you configure your Azure App"}]}[/block]

   <br />

> 🚧 Important!
> 
> Make sure you copy the token that is generated along with the Token URL seen below!  You will need both when you install Vbrick Rev Cloud app in Azure!

4. After your token is generated, you will also need the token **Account/Tenant URL** that is now visible.  Copy it and save it as well for later use.

   [block:image]{"images":[{"image":["https://files.readme.io/1a9351229548ff7d6dcc282d94658c667f0ad6beabbd3793206b90a6954e4647-image.png",null,"Copy and save the tenant URL"],"align":"center","caption":"Copy and save the tenant URL"}]}[/block]

   <br />

## Azure AD App Configuration

Once you have generated your token and copied your tenant URL, you are ready to configure automatic user provisioning.

1. Login to [Home - Microsoft Azure](https://portal.azure.com/#home) with appropriate credentials.
2. Add Vbrick Rev from the **Azure AD application gallery** to begin user provisioning to Rev.  Complete documentation is available to [configure and scope the app](https://learn.microsoft.com/en-us/azure/active-directory/saas-apps/vbrick-rev-cloud-provisioning-tutorial).

## SCIM Users and Groups

Once automatic provisioning begins from Azure AD, SCIM users are groups are identified with SCIM labels.

> 📘 Note
> 
> You can assign new Rev roles and groups to a SCIM group and user but **edits** to SCIM groups and users or **deprovisioning** (i.e., removal if a user leaves the company) _must_ be handled via Azure AD.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a826edb-scimGroup.png",
        null,
        "Groups that have been added via Azure AD are identified with a SCIM Group label"
      ],
      "align": "center",
      "caption": "Groups that have been added via Azure AD are identified with a SCIM Group label"
    }
  ]
}
[/block]


The same is true with users that have added with Azure AD.  You can give them new role assignments and assign them to additional Rev groups but they must be added and removed from Rev via Azure AD.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7596b9a-scimUser.png",
        null,
        "Users that have been added via Azure AD are identified with a SCIM Group Assignment"
      ],
      "align": "center",
      "caption": "Users that have been added via Azure AD are identified with a SCIM Group Assignment"
    }
  ]
}
[/block]


> 📘 Note
> 
> The initial sync cycle takes longer to perform than subsequent updates.  Each sync cycle takes approximately 40 minutes to complete as long as the Azure AD provisioning service is running.

## Additional References

For more details on this integration, how it works, and frequently asked questions, view the following additional links:

- [Automate User Provisioning and Deprovisioning to SaaS (Software as a Service) Applications with Azure Active Directory](https://learn.microsoft.com/en-us/azure/active-directory/app-provisioning/user-provisioning)
- [Managing User Account Provisioning for Enterprise Apps](https://learn.microsoft.com/en-us/azure/active-directory/app-provisioning/configure-automatic-user-provisioning-portal)
- [What is Application Access and Single Sign-On with Azure Active Directory](https://learn.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-single-sign-on)