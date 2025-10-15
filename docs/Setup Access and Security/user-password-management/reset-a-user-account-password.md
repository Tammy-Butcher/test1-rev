---
title: Reset a User Account Password
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
There may be times when you need to manually reset a user's password. Note that if Users are managed through **LDAP** or **Okta**, passwords and security options are not editable or managed through the Rev portal. This topic refers to local user account passwords only.

To reset a user account password in Rev:

1. Navigate to the User's profile under the [User module](doc:user-accounts).

2. Under the **Access Management** section click the **Reset Password** button. This button is only available if the account status is **Active** and is not **Locked Out**.

3. A reset password email is then sent to the User with a link to reset their password.

4. The account status is then set to **Awaiting Password Reset**.

<Image title="awaitingPasswordResetStatus.png" alt={296} align="center" src="https://files.readme.io/9d275350e492735a07dc85e9007f92b200469b6b99f1a56dd712a0368da81e4b-awaitingPasswordReset.png">
  User account status changes to Awaiting Password Reset after the Password Reset button is clicked that prompts an email to be sent to the User
</Image>

> 🚧 Important!
>
> You may not use the **Reset Password** button if the password is already expired via the password expiration rule. The user may login and reset their own password through the login screen.

5. The user must answer their **security question** to reset their password including if the password is being reset via expiration. Password complexity rules set for the system still apply.

6. The password reset link remains in effect for 72 hours.

7. To manually send the password URL, click the **Show** button (similar to obtaining the confirmation URL manually).

> 👍 Tip
>
> The button functions available in **Access Management** vary based on the user account status and what the Account Admin has configured for portal security. 
>
> A few use case(s) include: 
>
> * **Unlicensed** status and you are able to obtain the **User Confirmation URL** to complete the registration process.
>
> * **Locked Out** status and you are able to **Unlock** the account.
>
> * **Expired** status and how long ago the user's password expired.
