---
title: Setup Expiration Rules
excerpt: >-
  How to configure your own expiry rules so that videos automatically Inactivate
  or Delete
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
The **Expiration Management** option under the **Media Settings** menu displays expiration rules for video uploads and allows you to define new expiration parameters as needed. Expiration rules are based on days and views. A default rule may be set for all video uploads.

> ❗️ Warning
>
> [Expiration rules](doc:allow-expiration-rules) must be enabled globally under **Media Settings** > **Features** before you may use this functionality.
>
> Once saved, expiration rules may *not* be modified with the exception of **Name**, **Default** rule status, and **Delete** status. 
>
> If you need to modify a rule *setting*, you must re-create the rule and add the videos again (through bulk editing if you have added several videos) and then delete the old rule.

<Image title="expirationManagement.png" alt={1053} src="https://files.readme.io/f1ed871-expirationManagement.png">
  View all rules on the Expiration Management form
</Image>

## Create an Expiration Rule

Expiry Rules are created so that videos may be set to **Inactive** or are **Deleted** from the portal if they meet the following conditions:

* No views after X amount of days
* Set to expire in X days

> 👍 Use Case Example
>
> Expiry Rules can be created to set a video to **Inactive** status if it has not been viewed in 365 days. 
>
> Expiry Rules can be created to make sure all Human Resource videos are set to **Delete** after 5 days.

Click the **Add Expiry Rule** button to create a new rule.  Configuration options appear under existing rules at the bottom of the form.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Option
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Default
      </td>

      <td>
        Sets the default expiration rule. Only one default rule may be set at a time. You may also deselect all rules so that no default is set. 

        If a default rule is set, new uploads are automatically set to expire based on this rule.
      </td>
    </tr>

    <tr>
      <td>
        Name
      </td>

      <td>
        The Expiration Management rule name. Click to edit the name.
      </td>
    </tr>

    <tr>
      <td>
        Rule Type / Days
      </td>

      <td>
        The types of rule you may create.

        * **Number of Days Before Expiry**: Must be greater than zero. The video is visible for the number of days in the **Days**column and then expires and is set to either **Inactive**or **Deleted**.

        * **Number of Days without Views**: Must be greater than zero. The number of days in the **Days**column the video may go *without*being viewed (or partially viewed) before it expires and is set to either **Inactive**or **Deleted**.

        * The **Video Owner** is emailed 7 days prior to video expiration and again upon the actual expiration no matter which rule is created.
      </td>
    </tr>

    <tr>
      <td>
        Delete Upon Expiry
      </td>

      <td>
        If selected, videos are **Deleted**upon expiration.

        If *not*selected, videos are set to **Inactive**status instead.
      </td>
    </tr>

    <tr>
      <td>
        Delete (x)
      </td>

      <td>
        Deletes the Expiry rule. If you delete a rule, videos that are set to expire under that rule will no longer expire.
      </td>
    </tr>
  </tbody>
</Table>
