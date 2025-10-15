---
title: Upload Users and Groups via CSV File
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
You may quickly upload and edit multiple **Users** and **Groups** at once using a .csv file if you need to do so without an LDAP import.  If the groups you associate in the .csv do not already exist, they are created during the process.

> ❗️ Warning!
>
> You *must* save the file encoded in the **UTF-8** format. Otherwise certain characters may not be displayed correctly.
>
> There is a limitation of 300k rows allowed.

* Only .csv files are accepted
* Field names must be in the first row of the file (see sample below)
* Certain fields must be unique and are also required (noted below)
* Users are **Unlicensed** and do not count toward your licenses until logged in
* Users are assigned to the **Media Viewer** role only

## Format the User Account CSV File Upload

As noted, only .csv files are accepted and you must make sure it is formatted correctly. The sample .csv file seen here is described in the table below.

> ❗️ Warning!
>
> While some of the fields described in the table below are optional in your upload, you **must** include each field in your first row as the **Header** row (seen in yellow below) or an error will occur.

<Image title="sampleCsvFile.png" alt={700} align="center" src="https://files.readme.io/17c9f29-sampleCsvFile.png">
  The CSV file must be saved in UTF-8 format as described below or the Users will not upload correctly
</Image>

[Download ](https://portal.vbrick.com//doc/rev/csvusers.csv) a sample CSV file.

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
        Title Row (Row 1)
      </td>

      <td>
        Field names (UniqueId, Username, Lastname, Firstname, and so forth) must appear in **Row 1** (highlighted above) and may **not**be changed.
      </td>
    </tr>

    <tr>
      <td>
        Uniqueid
      </td>

      <td>
        This is a required field and must be unique. You may use your employee ID or any unique ID of your choosing.
      </td>
    </tr>

    <tr>
      <td>
        Username
      </td>

      <td>
        This is a required field and must be unique. This will be used to log in to Rev.
      </td>
    </tr>

    <tr>
      <td>
        Lastname
      </td>

      <td>
        Required field. Last name of the user account.
      </td>
    </tr>

    <tr>
      <td>
        Firstname
      </td>

      <td>
        First name of the user account. Not required.
      </td>
    </tr>

    <tr>
      <td>
        Title
      </td>

      <td>
        Title of the user account. Not required.
      </td>
    </tr>

    <tr>
      <td>
        PhoneNumber
      </td>

      <td>
        Phone number of the user account. Not required.
      </td>
    </tr>

    <tr>
      <td>
        Email
      </td>

      <td>
        This field must be unique if used. Not required. Email address of the user account. This field must also be a correct email-format ([name@subdomain.top-level-domain](mailto:name@subdomain.top-level-domain))
      </td>
    </tr>

    <tr>
      <td>
        GroupNames
      </td>

      <td>
        Optional field. Group(s) to associate the user accounts to. If the groups do not exist they will be created if the **Create Groups** checkbox is selected. More than one group should be separated by a semicolon.
      </td>
    </tr>

    <tr>
      <td>
        Action
      </td>

      <td>
        Optional field. Use **d** to delete the user account. Use **s** to suspend the user account.  

        Leave blank to create the user account with the defaults specified.  

        Delete or suspend applies to user accounts already existing in Rev.
      </td>
    </tr>
  </tbody>
</Table>

For each row:

* If a user row is missing a required field, the user account is not created.
* If a user account with the same email address already exists in Rev, the new user account is not created.
* If a user account with the same username already exists in Rev, the new user account is not created.

## Upload the User Account CSV File

Once the CSV file is formatted correctly, click the **Upload Users** button to begin the upload process.

> 🚧 Important!
>
> As noted, there is a limitation of 300k rows allowed.

<Image title="uploadUsers.png" alt={446} align="center" src="https://files.readme.io/77ab67f-uploadUsers.png">
  Use the Upload Users button to upload your CSV file once you are confident it is formatted correctly
</Image>

* Click the **Create Groups** checkbox if you are creating new groups.
* If your Users should be added to the Groups in the GroupNames column (in addition to existing groups they already belong to), select **Append**. This means you are *editing* Users.
* Select **Replace** to add Users to the Groups specified in GroupNames column and remove them from all other groups they previously belonged to. This means that *only* those groups in the .csv file are associated to the user account going forward.
* Click the **Submit** button when you are ready to upload your file. Users receive an email notification to log in and verify their accounts through the usual process unless you are using SSO.
* You receive a notification in Rev and through email once your upload is complete stating how many Users and Groups are created or if there were any errors.

> 📘 Note
>
> [Child accounts](doc:view-and-edit-account-details#add-a-child-account) are not permitted to modify account Users by using the upload .csv feature from the Parent account.
>
> If there is a need to modify Users in a child account via the .csv upload method, then those changes should be made directly in that child account.

> 👍 Tip
>
> The **Submit** button does not become available until you have attached a CSV file.
>
> If you plan on adding or editing several accounts, the upload feature allows a test on one row. A test upload is recommended *before* creating several groups or deleting/suspending several accounts to make sure your settings and .csv file accomplish what you intend.
