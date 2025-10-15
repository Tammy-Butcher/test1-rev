---
title: Reset a User Account Security Question
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
If a user account is locked out and the user also incorrectly answers the security question when attempting to reset their password through the **Forgot Password** link, Account Admins may reset the question for the account.

<Image title="maxSecurityQuestionAttempts.png" alt="This user has surpassed the number of attempts configured to answer the security question correctly and needs Account Admin assistance" align="center" src="https://files.readme.io/16995bfc3eb2ef64fd7b12ad175e32c4221301ff88e8a4f2dab42210ae314e32-securityAccountQuestionExceeded.png">
  This user has surpassed the number of attempts configured to answer the security question correctly and needs Account Admin assistance
</Image>

To reset a user account security question:

1. Navigate to the User's account under the [User module](doc:user-accounts).

2. Under **Access Management** > click the **Reset Security Question** button to generate an email to the user that prompts the creation of a new password and security question.

3. This button is only available if the user has incorrectly answered their security question when clicking the (**Forgot Password?**) hyperlink on the login screen. The amount of times they must answer incorrectly is set under **Security Settings**.

<Image title="resetSecurityQuestionButton.png" alt="This button appears if the user incorrectly answers their security question the number of times configured when attempting to reset their password" align="center" src="https://files.readme.io/49700d8f76e2445a1939794b1cc8b324d96ef514b5a2dbb2a4c9ac8c9f0e9645-resetSecurityQuestionButton.png">
  This button appears if the user incorrectly answers their security question the number of times configured when attempting to reset their password
</Image>

4. The reset link stays in effect for 72 hours.

5. If you need to manually send the reset URL, you may do so from the User's **Administrative Actions** section by clicking the **Show** button.
