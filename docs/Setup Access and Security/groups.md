---
title: Groups
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
**Groups** are sets of Rev users that often need to perform similar functions or tasks. Groups may be granted view or edit access to specific videos.

You may add new groups from the Rev interface or import them from LDAP. You must have the Account Admin role to manage groups. LDAP must be configured and an [LDAP Connector](doc:use-ldap-and-active-directory-with-rev) must be set up to import groups from LDAP.

To access the Groups module:

1. Navigate to **Users** > **Groups** menu in the [Admin Menu Options](doc:admin-menu-options). 

<Image alt="The Groups Menu is accessible to Account Admins under the Users Header Navigation Menu" align="center" src="https://files.readme.io/253fa38-groupsMenuDropdown.png">
  The Groups Menu is accessible to Account Admins under the Users Header Navigation Menu
</Image>

2. The **Groups** module is displayed. Use it to add, edit, and import LDAP groups to your portal.

## Add or Edit a Group

Most groups are imported and managed through LDAP and Active Directory. You may also add and edit groups through the **Groups** module in Rev.

To add a new group, click the **Add Group** button on the **Groups** module. You may edit a group by clicking its name.

Enter a **Group Name** and click **Create Group** to save the group.  **Users** and **Roles** are not needed to initially create the group.

## Add a User or Role to a Group

Use the **Role Assignment** and **User Assignment** sections to assign (or remove) roles and users to a group as needed.

Keep in mind that if you have imported your group from LDAP, you may \_not \_add users to it from Rev. You must edit it from LDAP to add or remove users.

Roles are assigned to a group so that certain permissions are enabled for several Users at once (all Users assigned to the Group). Moving a Role from the **Assigned Roles** column back to the **Available Roles** column removes that role (and all associated permissions) from the group.

<Image title="assignRoleToGroup.png" alt={1202} align="center" src="https://files.readme.io/58fe389-assignRoleToGroup.png">
  Each Role in the Role Assignment section will be given to Users assigned to this Group
</Image>

To add users to a Group, type the User's **First**, **Last**, or **Username** in the **Find Items** box. Click the user and then **Done** to add the user to the **User Assignment** section. This adds the user to the group upon saving.

To remove a user from a group, click the X next to the user name.

<Image title="assignUserToGroup.png" alt={1095} align="center" src="https://files.readme.io/62e86ec-assignUserToGroup.png">
  Users added to the User Assignment section are added to the Group
</Image>

## LDAP Groups

### Import an LDAP Group

Once you have [configured LDAP](doc:use-ldap-and-active-directory-with-rev) and set up an LDAP Connector, you may import LDAP groups to Rev. Once imported, LDAP groups may be managed directly from the Rev user interface in \_limited \_fashion.

If you have not configured Rev for LDAP import or if your [LDAP Connector](doc:add-ldap-connector-device) is not running on your host or through a direct connection, you are not able to import. 

> 📘 Note
>
> The import method described in this topic retrieves and displays several LDAP groups associated with the **Active Directory** server. If you only want to import a few specific groups, you may set up your LDAP Connector device to only import the groups that you specify to save time. **View**: [LDAP Groups Specification](doc:add-ldap-connector-device#ldap-groups-specification).

To import an LDAP group:

1. Navigate to **Users** > **Groups** and click the **Import Group From LDAP** button. This button is \_not \_visible if your connector is set up to only import specific groups.

2. Select an **LDAP Connector** you previously set up (in the **Devices** menu) from the dropdown.

3. You are presented with a list of Groups available for import.  Click a **Group Name** to display any **Child Groups** it contains.

<Image title="ldapGroupList.png" alt={807} align="center" src="https://files.readme.io/a4c7a78-ldapGroupList.png">
  All groups associated with a chosen LDAP Connector (setup in the Devices menu) are displayed
</Image>

4. Remove the **Groups/Child Groups** you do not want to import by clicking the **X** next to the group.

5. Click the **Import** button once you remove all unwanted groups from the form. All remaining groups are imported.

6. Each imported group appears in the **Groups** module. The user accounts contained in the LDAP groups are also imported to the **Users** module.

7. The group is regularly synchronized based on the setting defined when creating the LDAP Connector (and assuming your LDAP Connector Runtime exe is running on your host if you do not have a direct connection enabled). You may manually sync the group again if needed by re-importing it at any time with any updates.

### Edit an LDAP Group

Edit an LDAP Group by clicking on its name in the **Groups** module like any other Rev group. However, the attributes you may edit are very limited since LDAP groups should be managed, for the most part, from LDAP itself.

The **Group Name** and **User Assignment** sections in the LDAP group are displayed when edited. However, you may not edit these sections from Rev. You must return to LDAP to edit these group attributes and then re-import the group.

<Image title="groupNameUserAssignmentLdap.png" alt={806} align="center" src="https://files.readme.io/bc8e8d8-groupNameUserAssignmentLdap.png">
  You may view Group Name and User Assignment sections for an LDAP group in Rev but you must edit them in LDAP and re-import them
</Image>

LDAP groups also contain a **Role Assignment** section which may be edited within Rev. Note that if the group is updated through LDAP (re-imported) that this assignment does \_not \_change. In other words, you may \_only \_edit **Role Assignment** through Rev.

<Image title="LdapRoleAssignmentRev.png" alt={806} align="center" src="https://files.readme.io/8121ab4-LdapRoleAssignmentRev.png">
  Role Assignment for LDAP Groups is only updated through Rev and does not change even if edited in LDAP
</Image>

### Delete or Suspend an LDAP Group

You may not delete an LDAP group or user from Rev as you would a Rev created group (from the **Group** or **User** module, **Actions** column).

There are two methods to removing an LDAP group from Rev:

1. Remove the group from Rev by deselecting it from the group import screen and perform an import again.

2. Remove the group from LDAP itself and perform an import again.

**View**: [Import an LDAP Group](doc:groups#import-an-ldap-group)

When you delete a group, whether through Rev or LDAP, user data and accounts are preserved (not deleted). However, they may be placed in a suspended state.

Suspended LDAP users are removed from a suspended state when:

* The group is re-imported to Rev
* The user is added to another group in LDAP and the new group is imported 
* The only time that imported users are deleted from Rev is if the LDAP Connector itself is deleted

You may manually suspend an LDAP user as you would a Rev created user. To activate it, you simply press the **Activate** button in the **Actions** column on the **User** module as you would a Rev user.

LDAP users that are not manually suspended (through the **Actions** dropdown) and that may be automatically suspended (and then deleted as a result in some cases) include:

* Those accounts that are created and imported but then never log-in. An example of this may be a user that leaves the company before logging-in.
* These accounts may be permanently deleted upon an LDAP sync by selecting **Delete Suspended Users Who have never logged in** checkbox under the **LDAP Server Synchronizations Setting** section on the LDAP Connector device. Please keep in mind that if this checkbox is enabled, the **Suspended** account deletions are permanent and only include those accounts that have \_never \_been logged in; \_not \_the manually suspended accounts through the **Users** module and described above.
* Those accounts that are suspended as a result of removal from an LDAP group or an LDAP group is removed during an LDAP sync. You have the option to disable this suspension setting by selecting **Do not suspend users when removed from all LDAP groups** or LDAP group is removed. **View**: **LDAP Server Synchronization Settings**
