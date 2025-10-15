---
title: Suspend a User Account
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
Suspended user accounts may not log in and, if the account is logged in at the time the account is suspended, they are logged out immediately. If a user attempts to log in after the account is suspended, an error message informs them that their account is suspended and to contact an Account Admin.

* You may not suspend your own account.
* Consider suspending accounts as opposed to deleting them.
* Suspended accounts are noted in the **Status** column of the Users module.
* An LDAP User may be suspended if the source of the account is removed (the LDAP group). View: **Delete or Suspend an LDAP Group or User**
* Users that are suspended manually through this drop-down are not deleted when an LDAP sync is run again if the **Delete Suspended Users** checkbox is enabled. (View: **LDAP Server Synchronization Settings** for details on how to delete users that have never logged in to Rev and are suspended.)

<Image title="suspendedUserStatus.png" alt="The Status column in the Users module denotes the Suspended status" align="center" src="https://files.readme.io/a339967f6fe0193c7ed92b98bb0bf8659019aed121936d76c7851680e468e283-userAccountStatusColumn.png">
  The Status column in the Users module denotes the Suspended status
</Image>

To suspend a User:

1. Navigate to the User's account under the [User module](doc:user-accounts).

2. In the **Actions** dropdown, click the **Suspend User** link. This is a toggle and switches to **Activate User** if/when you need to reactivate the User.

<Image title="suspendUserLink.png" alt={274} align="center" src="https://files.readme.io/7c1d42d-suspendUserLink.png">
  Clicking Suspend User suspends the User account and then switches to Activate User in the event you need to reactivate the account
</Image>
