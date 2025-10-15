---
title: Set Portal Password Rules
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
**User Password Parameters** are configured using three predefined rules; **Basic**, **Medium**, and **Strong**. You may also create your own **Custom **password rule if desired.

This is the type of password that will be required of your users to set and then use when logging in to your portal so consider your choice carefully.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/686ca5e-passwordRules.png",
        "passwordRules.png",
        1723
      ],
      "align": "center",
      "caption": "Select the type of password that will be required to log in to your portal"
    }
  ]
}
[/block]

To set a password rule:

1. Navigate to **Admin > System Settings > User Security**.

2. Scroll to the **User Password Parameters** section.

3. Select a **Password Complexity Rule**.
   - Basic
   - Medium
   - Strong
   - Custom

4. If you select **Custom Password**, you are able to define your own set of parameters for the rule.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7cd5e7d-customPassword.png",
        "customPassword.png",
        402
      ],
      "align": "center",
      "caption": "Mix and match your own parameters for a new rule if you select Custom"
    }
  ]
}
[/block]

## Set Lockout Rules

**User Lockout Settings** specify how many incorrect log in attempts are allowed by a user before they are locked out and their password must be reset.

When a password is reset through the **(Forget Password?)** hyperlink, the security question that was set up upon account creation must be answered correctly. User Lockout Settings also dictate how many attempts to answer the security question may be answered incorrectly before it must also be reset. You may also designate a lockout period of time and a time interval for locking out a user if needed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c768274-userLockoutSettings.png",
        "userLockoutSettings.png",
        402
      ],
      "align": "center",
      "caption": "Configure the rules for resetting a password before a user is locked out"
    }
  ]
}
[/block]

To configure lockout settings:

1. Navigate to **Admin > System Settings > User Security**.

2. Scroll to the **User Lockout Settings** section.

3. Enter the number of times a user may enter the incorrect password or security question before being locked out in the **Invalid login attempts allowed** field. The default is 5. Any number between 1 and 100 may be entered. If this field is set to 0, the user is never locked out.

> 👍 Tip
> 
> If a user exceeds the number of attempts here, this message is displayed:
> 
> _“You reached the limit for incorrect login attempts. You must reset your password to access your account or contact your administrator.”_

3. Select the **Users can reset their password** checkbox if users may reset their own passwords from the login form (through the **Forgot Password? **hyperlink). Otherwise, an Account Admin resets the password of all locked out users.

> 👍 Tip
> 
> When the **Forgot Password?** hyperlink is selected on the login screen, this message is displayed:
> 
> _“An email has been sent to your email address to reset your password. The email may take a few minutes to be received. If you do not receive an email, please contact your administrator.”_

4. Set the period of time that users are locked out if the password is entered incorrectly in the **Lockout period (minutes)** field. In the image above, if the password is entered incorrectly 3 times, the user is locked out for 10 minutes before they can try again. The default value is 0 which means no waiting period.

> 🚧 Important!
> 
> If the user attempts to use the **Forgot Password?** hyperlink _during_ the Lockout period, no email message is received and the user will need to contact an Admin to unlock or reset the Password.
> 
> If **Forgot Password?** is used _after_ the Lockout period, an email is received normally and the password can be reset without Admin assistance.
> 
> As noted, if the Lockout period is set to 0, there is no waiting period and the email is sent immediately.

5. If you want the user locked out after the password is entered incorrectly within a specified time interval, use the **Invalid attempt period (minutes)** field. In the image above, the user is locked out when the password is entered incorrectly 3 times within 15 minutes.

## Set Session Inactivity and Timeout Settings

**Session Settings** specify how long a user’s session may remain inactive before they are logged out of the system automatically.

To configure session settings:

1. Navigate to **Admin > System Settings > User Security**.

2. Scroll to the **Session Settings** section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6c447e0-sessionInactivity.png",
        "sessionInactivity.png",
        620
      ],
      "align": "center",
      "caption": "Specify how long a user may remain inactive before they are logged out"
    }
  ]
}
[/block]

- Enter the number of minutes a user may remain inactive in **Session Inactivity Timeout (in minutes)**. The default setting is 30 minutes.
- You may enter between 15 and 480 minutes (up to 8 hours) as a valid setting.
- If a user is logged out due to inactivity, they are returned to the login page with the message, “Your session has expired due to inactivity. Please log in again.”.