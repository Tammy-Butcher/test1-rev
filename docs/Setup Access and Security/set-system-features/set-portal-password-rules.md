---
title: Set Portal Password Rules
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
> 🚧 Important!
> 
> This topic covers several features that control the configuration of password rules for **local accounts** within Rev. These features do not cover accounts associated with external ADs. These include defining complexity rules, setting duration-based expiration dates, and creating inactivity timers. These features help keep your Rev portal and user accounts safe.

## Set a Password Complexity Rule

**User Password Parameters** are configured by selecting from three increasingly complex, predefined rules: **Basic**, **Medium**, and **Strong**.  You may also create your own **Custom **password rule if desired.

This rule defines the complexity of local account passwords that users must adhere to when setting passwords.  Once set, their passwords are used to log in to your portal, so consider your choice carefully.

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


To set a password complexity rule:

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


## Set a Local Password Expiration Rule

You can also set a local password expiration rule that specifies that after a certain amount of days a user must reset their password.  Keep in mind this is not about blocking users from logging in or out but keeping passwords refreshed for current system users. The default setting is 0 days which means that no password expiration rule is set.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f5a14eb6016821fac0748ee4d02e773aa6850eb5a5f26aa1a10ee707762d1720-passwordExpiry.png",
        "",
        "Entering a number in the Password Expiry fields means that a user is required to reset their password each time that number of days elapses since their last login"
      ],
      "align": "center",
      "caption": "Entering a number in the Password Expiry fields means that a user is required to reset their password each time that number of days elapses since their last login"
    }
  ]
}
[/block]


To set a password expiry rule:

1. Navigate to **Admin > System Settings > User Security**.

2. Scroll to the **User Password Parameters** section.

3. Enter a **Password Expiry (in Days)** number between 0 and 365.  This number is user-specific in that it keeps track of the expiration period for that user based on each **Licensed User's** last password change plus the expiration period you enter here as the user's **password expiration date**. When the password expiration date is reached, the user is required to reset their password on their next log-in and then the count resets and begins again.

4. If you change this setting, it _resets_ all Active Licensed Users' **password expiration dates** to reflect the new entry.  For example, if you change the setting to 15, this means that _every_ Licensed User's password will expire in 15 days _regardless_ of their current expiration date.

5. If you do _not_ set a **Password Expiry** number in this field and leave the number at the default setting of **0**, no password expiration occurs.

> 👍 Tip
> 
> The **Password Expiry** feature is for _local_ Rev accounts and does not function for LDAP or Okta imported accounts. It is intended solely to drive users to periodically change their passwords as a security measure and, as such, provides an easy means for users to log-in and do so.
> 
> When you first enable this feature, user passwords may expire quickly depending on a user's last change date and the **Password Expiry** setting number you choose. This is expected and allows you to baseline account passwords going forward.

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