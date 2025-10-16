---
title: Enable Okta SCIM
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
Vbrick Rev supports the integration of the **System for Cross-Domain Identify Management** (SCIM) user management API to enable automatic provisioning of users and groups between **Vbrick Rev** and **Okta**. Once configured, Okta automatically provisions and deprovisions users and groups to Rev.

## Prerequisites

Before you enable **Okta SCIM** in Rev and begin configuration, review the following criteria to make sure you understand programmable features and required criteria.

* You should have access to your **Okta Administrator** who can install the Vbrick Rev Cloud application in Okta.
* Learn about how the [Provisioning service](https://help.okta.com/en-us/content/topics/provisioning/lcm/con-okta-prov.htm) works on the Okta Docs site.
* Determine what data (user/group) fields to map between Okta and Vbrick Rev Cloud.

> 🚧 Important!
>
> If you already have an [LDAP Connector](doc:add-ldap-connector-device) configured in Rev, make sure that the **SAMAccountName** in your **LDAP** matches the **Username** in **Okta**. 
>
> Further, you should *not* have *both* **LDAP Connector** and **Okta SCIM provisioning** enabled simultaneously.  Review the use case scenarios below.

## Supported Features

The **Vbrick Okta SCIM** integration supports the following features:

* Create users
* Update user attributes
* Deactivate users
* Create groups
* Update group attributes
* Delete groups

### Configuration Scenarios

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Customer Type
      </th>

      <th>
        Existing LDAP Connector
      </th>

      <th>
        Existing SAML SSO
      </th>

      <th>
        Existing LDAP Login
      </th>

      <th>
        Action
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Existing Vbrick Rev Cloud Customer
      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>
        No
      </td>

      <td>
        * Disable **LDAP Connector**. 
        * Install **Vbrick Rev Cloud App** in Okta. * Configure **User and Group provisioning** in the App. * Existing **SAML SSO** should work but you can also configure SAML SSO in the same App.
      </td>
    </tr>

    <tr>
      <td>
        Existing Vbrick Rev Cloud Customer
      </td>

      <td>
        Yes
      </td>

      <td>
        No
      </td>

      <td>
        Yes
      </td>

      <td>
        1. Disable **LDAP Connector**. This also disables the LDAP login. 2. Install the **Vbrick Rev Cloud App** in Okta. 3. Configure **User and Group provisioning** in the App. 4. Configure **SAML SSO** in the App.
      </td>
    </tr>

    <tr>
      <td>
        Existing Vbrick Rev Cloud Customer
      </td>

      <td>
        No
      </td>

      <td>
        Yes
      </td>

      <td>
        No
      </td>

      <td>
        1. Install **Vbrick Rev Cloud App** in Okta. 2. Configure **User and Group provisioning** in the App if you want automated user and group sync from Okta.3. Existing **SAML SSO** should work but you can also configure SAML SSO in the same App.
      </td>
    </tr>

    <tr>
      <td>
        New Vbrick Rev Cloud Customer
      </td>

      <td>
        No
      </td>

      <td>
        No
      </td>

      <td>
        No
      </td>

      <td>
        1. Install **Vbrick Rev Cloud App** in Okta. 2. Configure **User and Group Provisioning** in the App. 3. Configure **SAML SSO** in the same App.
      </td>
    </tr>
  </tbody>
</Table>

## Rev Configuration

Once you have disabled all LDAP Connectors and have reviewed your configuration scenarios, you are ready to configure the integration:

1. Navigate to **Admin > System Settings** > **User Security** and scroll to the **SCIM Configuration** section.
2. Click the **Enabled** checkbox next to the **Enable SCIM** setting.  
3. Select **OKTA** from the dropdown in the provider setting. You are now ready to generate your token.  Keep in mind you will need to copy and save the token and the URL that are generated in the next step.

   <Image alt="Make sure you copy the token you generate in this section" align="center" src="https://files.readme.io/1c9aedc111b37f6347ab823d68b92571e9a663886c4827d8b09bef39b31d9a86-enableScim.png">
     Make sure you copy the token you generate in this section
   </Image>

   <br />
4. Click the **Generate Token** button and **Copy** the token that is generated. 
5. Click **Ok**. Make sure you keep the copied token somewhere you can access it again.

<Image alt="The SCIM token is needed when you configure your Okta App.  Make sure you copy and save it." align="center" src="https://files.readme.io/9540ded071ed71ea6ee8b0bb9aefd9b34986ef65ca0998363826bb56f63f78db-confirmScimToken.png">
  The SCIM token is needed when you configure your Okta App.  Make sure you copy and save it.
</Image>

<br />

> 🚧 Important!
>
> Make sure you copy the token that is generated along with the Tenant domain/hostname seen below!  You will need both when you install Vbrick Rev Cloud app in Okta!

6. After your token is generated, you will also need the **Tenant URL** that is now visible.  Copy just the domain/hostname part from the URL and save it as well for later use.

<Image alt="Copy and save the tenant URL" align="center" src="https://files.readme.io/3f531170409d2cbdf973b24b967e110cb80e8cfeb9a659f064a60ee305c49d65-scimTenantURL.png">
  Copy and save the tenant domain
</Image>

## Okta App Configuration

Once you have generated your token and copied your tenant URL, you are ready to configure automatic user provisioning in Okta.

1. Sign in to your Okta admin dashboard.
2. Navigate to **Applications** > **Applications** > **Browse App Catalog**.
3. Search for [Vbrick Rev Cloud](https://www.okta.com/integrations/vbrick-rev-cloud/) using the search bar and click on the **Vbrick Rev Cloud** app.
4. Click **Add Integration**.
5. In the Vbrick Rev Cloud app, on the **General Settings**, enter the Vbrick Rev Tenant domain/hostname that was saved above when you generated your token.
6. Click **Provisioning** tab and then **Integration**. 
7. Click **Configure API integration**, check **Enable API Integration** and enter the token that was saved from the above step. 
8. In the Provisioning To App, enable **Create Users**, **Update User Attributes** and **Deactivate Users**. Uncheck **Set password when creating new users**.  
9. Click the **Assignments** and assign any users or groups that you would like to have access to Vbrick Rev Cloud. Make sure to configure Provisioning before configuring Assignments.
10. Make sure to uncheck **Import Group** as its not supported.
11. Click **Save**.

## SCIM Users and Groups

Once automatic provisioning begins from Okta, SCIM users are groups are identified with **SCIM** labels.

> 📘 Note
>
> You can assign new Rev roles and groups to a SCIM group and user but **edits** to SCIM groups and users or **deprovisioning** (i.e., removal if a user leaves the company) *must* be handled via Okta.

<Image alt="Groups that have been added via Azure AD are identified with a SCIM Group label" align="center" src="https://files.readme.io/d4e7f56c35b39d3dc333566a9466478ab127d01e7355431bc776ed285d075647-scimGroups.png">
  Groups that have been added via Okta are identified with a SCIM Group label
</Image>

The same is true with users that have added with Okta.  You can give them new role assignments and assign them to additional Rev groups but they must be added and removed from Rev via Okta.

<Image alt="Users that have been added via Azure AD are identified with a SCIM Group Assignment" align="center" src="https://files.readme.io/7596b9a-scimUser.png">
  Users that have been added via Okta are identified with a SCIM Group Assignment
</Image>

## Note

* Link Group feature is not supported in Okta Vbrick Rev Cloud app.
* When pushing a group from Okta that already exists in Vbrick Rev, you might see a duplicate group name error. You can ignore this error as the group already exists in Vbrick Rev.