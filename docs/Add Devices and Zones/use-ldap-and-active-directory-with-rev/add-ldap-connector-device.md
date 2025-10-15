---
title: Add LDAP Connector Device
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
You must create a means for Rev to communicate with **Active Directory** and **LDAP groups**. This is accomplished by adding an **LDAP Connector Device** in Rev and then running that connector on a Host or through a **Direct Connection** if you have an **On-Premise** installation. Be aware that the connector will *always* need to be running on the Host you choose for importing and synchronizing your LDAP groups and users if you do not have a **direct connection** enabled.

To add an LDAP Connector Device:

1. Navigate to the **Devices** > **Source Devices and LDAP Connectors**.

2. Click **Add a Device** > **Add an LDAP Connector**.

3. Complete each section of the form as described below.

> 📘 Note
>
> Depending on the **Directory Type** you choose, most fields are completed for you when adding an **LDAP Connector**. If you intend to modify those fields and are unsure of exact values, consult the documentation for more information:
>
> * [Active Directory](https://social.technet.microsoft.com/wiki/contents/articles/13752.wiki-active-directory-domain-services-ad-ds-portal.aspx)

### Add as a Direct Connection

> 📘 Note
>
> Adding LDAP as a Direct Connection is for use with On-Premise installs or Rev Cloud depending on how **Status** and **MAC Address** settings are configured (both are explained below).

Complete the **Device Name** section first as either a **Direct Connection** (normally for **On-Premise** installations) or for use with the **LDAP Connector for Rev Cloud** that you previously downloaded and installed. 

You need to *inactivate* **Direct Connection** and enter at least one **MAC Address** (of the laptop/server of the previously installed connector) for use with Rev Cloud.

This example has **Direct Connection** in **Inactive** status since Rev Cloud is in use.

<Image title="directConnectionForCloud.png" alt={673} align="center" src="https://files.readme.io/42d818d-directConnectionForCloud.png">
  Make sure Direct Connect is Inactive if you plan to use an installed LDAP Connector for Rev Cloud
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field Name
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Device Name
      </td>

      <td>
        The unique **Device Name** you use to import your LDAP groups. This is a required field.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        Designates whether or not your connector is currently **Active**or **Inactive**.
      </td>
    </tr>

    <tr>
      <td>
        Direct Connection
      </td>

      <td>
        Enabled by default. This setting is used for **On-Premise** Rev installations to provide a direct connection to Active Directory.  

        If this setting is enabled, you are *not* required to download and install the Rev Cloud LDAP Connector. To use *only* Rev Cloud, this setting is *disabled* and you *are* required to download and install the Rev Cloud LDAP Connector.  

        You *are* required to enter at least one **MAC Address** which is used to run one or more LDAP Connectors.
      </td>
    </tr>

    <tr>
      <td>
        Allow LDAP Authentication for Users
      </td>

      <td>
        Enabled by default. Specifies if User Accounts will use LDAP authentication.  

        If disabled, user/group sync will use LDAP while user authentication will use SAML.  

        View: Disable LDAP Authentication for Users.
      </td>
    </tr>
  </tbody>
</Table>

### Add Connector Nodes

 When you disable **Direct Connection**, you are able to enter a **MAC Address** for each **Connector Node** for each **LDAP Connector for Rev Cloud** you install and plan to use. 

Set the **Status** per Node or through the entire **LDAP Connector Device** as desired (unless there are no Active nodes). If more than one Node is configured, Rev distributes tasks among the available Nodes.

<Image title="addConnectorNodes.png" alt={807} align="center" src="https://files.readme.io/d3d8b28-addConnectorNodes.png">
  Set MAC Address and Status for each LDAP Connector for Rev Cloud (or On-Premises) in use
</Image>

The **MAC Address** for the **Connector Node** is *required* if **Direct Connection** is **Inactive** and you are unable to create the connector without it if you plan to run your connector on a Host. This is normally the address of the **Host** you plan to run your connector from or the previously entered connector Host location. This is easily obtained by entering the command `getmac` from a command prompt. The MAC Address is the first line with no dashes.

You may add additional nodes by clicking the **Add Connector Node** button. Further, you may change the **Status** of each node at will by clicking the **Active** and **Inactive** buttons.

> ❗️ Warning!
>
> The **LDAP Connector for Rev Cloud** version in use is displayed under each **MAC Address**. It is *not* recommended that different versions of the connector be in use at the same time. 
>
> The first two MAC Addresses of each node you add may be viewed on the main **Source Devices and LDAP** page under the **Network Address** column.

<Image title="connectorNodeStatus.png" alt={270} align="center" src="https://files.readme.io/2124c60-connectorNodeStatus.png">
  LDAP Status state from the Source Devices and LDAP module page
</Image>

LDAP Connector Status depends on the following node states:

* **Active**: If LDAP Connector is Active and all Active LDAP nodes are online. 
* **Warning\<# of offline nodes/# of active LDAP nodes>**: If LDAP Connector is Active and at least one Active LDAP node is offline: 
* **Offline**: If LDAP Connector is Active and all Active LDAP nodes are offline/importing.
* **Inactive**: If LDAP Connector is Inactive. 

### LDAP Server Settings

Once you decide how you are going to run the connector, complete the **LDAP Server Settings** section of the device.

<Image title="ldapServerSettings.png" alt={773} align="center" src="https://files.readme.io/41efda7-ldapServerSettings.png">
  Selecting a Directory Type automatically populates recommended Server Mapping defaults
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Directory Type
      </td>

      <td>
        Required field. The directory type that the **LDAP Connector** supports; Note that when you choose a directory type, the **LDAP Server Mapping** fields are automatically populated with the recommended default settings for that type.
      </td>
    </tr>

    <tr>
      <td>
        LDAP Server Host
      </td>

      <td>
        Required field. The **IP address** or name of the **Host**.
      </td>
    </tr>

    <tr>
      <td>
        Port
      </td>

      <td>
        Required field. The default port is **389**. Use **636**if using **SSL**.
      </td>
    </tr>

    <tr>
      <td>
        SSL
      </td>

      <td>
        Indicates the LDAP connection is over SSL if selected.
      </td>
    </tr>

    <tr>
      <td>
        TLS v1.2
      </td>

      <td>
        Enables TLS v1.2 support. *Must have SSL enabled first before this becomes available*.
      </td>
    </tr>

    <tr>
      <td>
        Username
      </td>

      <td>
        Required field. The user name/password to connect to LDAP Server.  

        Note: Click the **Change Username and Password**button to access Credentials.
      </td>
    </tr>

    <tr>
      <td>
        Password
      </td>

      <td>
        Required field. The user name/password to connect to LDAP Server.  

        Note: Click the **Change Username and Password** button to access Credentials.
      </td>
    </tr>
  </tbody>
</Table>

> 👍 Tip
>
> This example uses **Active Directory** as the **Directory Type** when creating an LDAP Connector.
>
> Selecting **Generic LDAP** is much the same process.

### LDAP Server Mapping

Most of the **LDAP Server Mapping** section is populated with recommended default values and formats when you choose a **Directory Type** in the **LDAP Server Settings** section. The example below displays the server mappings for **Active Directory**. These fields may be modified if needed. Most fields are required.

<Image title="ldapServerMapping.png" alt={772} align="center" src="https://files.readme.io/678d9e9-ldapServerMapping.png">
  Server Mapping defaults are recommended by the Directory Type selected in Server Settings
</Image>

> 🚧 Caution
>
> if you change the **Root Scope** field in the **LDAP Server Mapping** section after you have already imported Groups and Users, you are required to re-import your LDAP Group.

### LDAP Groups Specification

The **LDAP Groups Specification** section is used to import *specific* LDAP groups only and is only visible if the **Specify Groups to Import** checkbox is selected in the previous **LDAP Server Mapping** section.

If you are an organization with hundreds (or even thousands) of LDAP groups, importing them all takes a considerable amount of time. You may use the **Specify Groups to Import** checkbox to enter the LDAP group you want to import instead. 

This opens the **LDAP Groups Specification** section where you may enter the **Distinguished Name (DN)** of the LDAP group import as seen in the example below.

<Image title="ldapGroupsSpecification.png" alt={682} align="center" src="https://files.readme.io/6a77484-ldapGroupsSpecification.png">
  Use this option to import specific groups instead of all groups
</Image>

By default, the **Specify Groups to Import** checkbox is deselected which means that *all* LDAP groups associated with your **Active Directory** server are retrieved and displayed for potential import when you click the **Add Groups** action for an **LDAP Connector Device** or from the **Import Group From LDAP** button from the **Groups** module (image below).

<Image title="importGroupsFromLdap.png" alt={607} align="center" src="https://files.readme.io/22fb954-importGroupsFromLdap.png">
  Once your LDAP Connector Device is set up, you have the option to import Groups from LDAP from the Group module as well but only if the Specify Groups to Import checkbox is disabled
</Image>

> ❗️ Warning!
>
> * You must enter the LDAP **DN Name** exactly as it appears. If it is misspelled or entered incorrectly it will not import. It is not case sensitive.
> * If you use this method, you may no longer use the **Add Groups** action for an LDAP Connector device or the **Import Group From LDAP** button from the **Groups** module until the **Specify Groups to Import** checkbox is once again *disabled*.
> * If the checkbox is deselected and you want to import new groups, then the **Reset Connector Sync** button must be used to **manually sync** the connector; or you may also wait until the next scheduled sync interval has been performed. View: **LDAP Server Synchronization Settings**.

### User Record Mapping

Similar to the **LDAP Server Mapping** section, the **User Record Mapping** section is populated with recommended default values and formats when you choose a **Directory Type** in the **LDAP Server Settings** section. 

The image below displays the user record mappings for **Active Directory**. These fields may be modified if needed. Most fields are required.

<Image title="userRecordMapping.png" alt={802} align="center" src="https://files.readme.io/bc4ecd1-userRecordMapping.png">
  User Record Mapping default values are populated when a Directory Type is selected in the Server Settings section
</Image>

> 🚧 Caution
>
> You must have the **LDAP Connector v7.30+** deployed to map the **User Profile Image** field. This must be a jpeg format image no larger than 5MB or an error will be generated.

### Merge Users

This checkbox determines how to treat duplicate Users. The **Merge LDAP and non-LDAP users** checkbox is disabled by default. When enabled, the LDAP connector processes and merges the incoming User *even if the user currently exists* in Rev.

When disabled, a “duplicate User” error is generated instead.

<Image title="mergeUsersCheckbox.png" alt={811} align="center" src="https://files.readme.io/5575098-mergeUsersCheckbox.png" />

Keep in mind:

* The incoming User is treated as an update and this is *permanent and not reversible*.
* The update *only* occurs if **both** username and email address match.
* The source of the User is modified and set to LDAP.
* If the Rev User had additional roles, those are retained.
* If the Rev User was manually **Suspended**, that User remains Suspended.
* **Active** and **Unlicensed** status states remain unchanged.
* LDAP fields override Rev user field values, including any blank fields.
* As noted, if this checkbox remains disabled, then the LDAP connector continues to display an error message for any duplicate username/email addresses found.

### LDAP Server Synchronization Settings

Use the **LDAP Server Synchronization Settings** section to specify the sync interval from Active Directory to Rev. You can also specify how **Suspended** user accounts are treated during syncs and in accordance with LDAP groups edits.

Sync intervals are specified in minutes or hours. The *recommended* interval is **24 hours**; particularly if importing and/or syncing large groups of users so you do not tie up server resources during peak usage time by your end users. Note that you must specify a **synchronization interval**.

Select the **Delete Suspended Users Who have never logged in** checkbox to delete those LDAP accounts that were synced and imported but then subsequently never logged in to Rev. An example of this may include a user account that is created and imported but then leaves the company before logging in.

<Image title="ldapServerSyncSettings.png" alt={642} align="center" src="https://files.readme.io/57c9d53-ldapServerSyncSettings.png">
  Use this section to determine how often LDAP Server synchronizes with Rev
</Image>

Select **Do not suspend users when removed from all LDAP groups or LDAP group is removed** if you want to disable the suspension of users when users are removed from the LDAP group/groups that are being synced with Rev. 

The following rules apply for this setting when enabled:

* When removing users from all groups in LDAP they are removed from groups but not suspended in Rev.
* When a group is no longer selected for an LDAP import in the Connector users are not automatically suspended.
* This option is disabled by default. Also note that for those users already suspended in Rev, this option has no effect and does not change their status.

Finally, if your sync needs to be reset for any reason, you may use the **Reset Connector Sync** link in the **Actions** drop-down on the **Source Devices and LDAP Connector** module.
