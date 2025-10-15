---
title: Unlock a User Account
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
If a user is locked out of their account and is unable to reset the password through the **Forgot Password** link, Account Admins may either unlock the account or reset the password as the case may be. The exception to this is if users are managed by LDAP or Okta. Only local accounts are managed through this interface.

To unlock a user account that is locked out:

1. Navigate to the user account under the [User module](doc:user-accounts).

2. Under **Access Management** > click the **Reset Password** button to generate an entirely new password for the User.  **View**: [Reset a User’s Password](doc:user-accounts#reset-a-users-password).

3. Click **Unlock** to unlock the user account. The previous password will still be in place rather than forcing a password reset.

4. The user account status must be either **Active** or in **Locked Out** status for these two buttons to be present at the same time. It cannot be expired.

<Image title="unlockUserAccount.png" alt="If the user account is Active or Locked Out you may reset the password or unlock the account" align="center" src="https://files.readme.io/89f428b2081fd0a36c99f68385e3ecdb7327160c0b28662f9c0860cda24923b0-unlockUserAccount.png">
  If the user account is Active or Locked Out you may reset the password or unlock the account
</Image>
