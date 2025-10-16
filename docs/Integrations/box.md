---
title: Box
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
**Box** is a secure, AI-powered, collaboration and content management platform that Vbrick integrates with if you configure and then enable it on your Rev portal. Once the Box integration is enabled, Rev-based roles with **upload permissions** are able to **manually import** Box videos directly from the **Upload tray** in Rev to their Rev portal.

## Requirements

* Rev Cloud and an Account Admin account
* A Box account that has Admin or Co-Admin permissions
* Note that you will be creating a custom app that is designed specifically for importing supported [video and audio files](doc:supported-video-and-audio-formats) from Box to Rev. The created app is _not_ eligible for publication on the **Box Integrations** page.

## Configuration

There are two steps to configure the Box integration for use with Rev. You must first create a custom Vbrick app for Box and then enable Rev to work with the created app.

### Create a Custom Vbrick App for Box

To begin, create a custom Vbrick app that is designed for importing videos from Box to Rev.

1. Log-in to [Box](http://box.com/) as an Admin or a Co-Admin user account.
2. Select **Dev Console** on the left navigation sidebar.

<Image align="center" border={false} src="https://files.readme.io/14c20a88a2ebb9580c9e962e3a0221058c3060889f7b2fcfffffa33050c65f16-devConsoleButton.png" />

3. On the Dev Console page, the default view is **My Platform Apps**. This page displays all apps created by your organization.
4. Click the **Create Platform App** button to create a new app for **Vbrick**.

<Image align="center" border={false} src="https://files.readme.io/f01cd94ee40df8bf5930f1fbe0bdbbc04f2be19ac366d6868145061cb9dfc58f-createPlatformAppButton.png" />

5. Choose **Custom App** as the platform app type.

<Image align="center" border={false} src="https://files.readme.io/60891ee60538ec0e1085c708397a307e8f14ff59dfed36db1038d65ca0df8db6-createCustomApp.png" />

6. A **Custom App** wizard appears for entering the app details. Enter the required information for the listed fields (step 1 of 2), then click **Next**.
   1. App Name
   2. Description
   3. Purpose: Automation
   4. Who is building this application?: Partner
      1. **Change this field from Partner to Vbrick**

<Image align="center" alt="Change Partner to Vbrick and click Next" border={false} caption="Change Partner to Vbrick and click Next" src="https://files.readme.io/b91496b989d006dc5ebce3755bc1ce53945752f6d2149a781d992c7998f0e7a0-requiredFields.png" />

7. On the **Custom App** wizard page (step 2 of 2), choose **Server Authentication (Client Credentials Grant)** as the authentication method. Click **Create App** to finalize the **Vbrick app** creation.

<Image align="center" border={false} src="https://files.readme.io/f1972935b6450255a5df1eded8165ce3d019b4daac6982c085627a70c3d870dd-serverAuthentication.png" />

> 📘 Note
>
> Currently, the only authentication method available for importing videos from Box to Rev is **Server Authentication (Client Credentials Grant)**.
>
> Note that apps using this authentication method currently cannot be published on Box's integrations page.

8. After confirming the custom Vbrick app creation, you are directed to the configuration page. The **Configuration** page displays all details set in the app creation wizard for additional configuration and review.

<Image align="center" border={false} src="https://files.readme.io/cddf81a94344f7e289386a9229f5a994cd16146f840bf62dd09555f64677fa43-configTab.png" />

**Access Levels**

Scroll to the **App Access Level** section on the **Configuration** page and choose **App + Enterprise Access** to set appropriate access.

<Image align="center" border={false} src="https://files.readme.io/0a17a01d8615d04f53f6ca79c9c50512e4a432c6c265b69cbf76756901e865ee-appEnterpriseAccess.png" />

**Application Scopes**

Scroll to the **Application Scopes** section on the **Configuration** page and select the required **Application Scopes** noted below. _All other scopes should remain unchecked_.

* **Content Actions**
  * Read all files and folders stored in Box
  * Write all files and folders stored in Box
* **Administrative Actions**
  * Manage Users

<Image align="center" alt="All other scopes should remain unchecked other than the ones selected here" border={false} caption="All other scopes should remain unchecked other than the ones selected here" src="https://files.readme.io/28e5240af5786dec047545a2c53a668e9cbd7ab1a49bf608c62c9a15a930f0f0-applicationScopes.png" />

**Advanced Features**

Scroll to the **Advanced Features** section on the **Configuration** page and select the required scopes noted below. _All other scopes should remain unchecked_.

* Make API calls using the as-user header

<Image align="center" border={false} src="https://files.readme.io/320746b69db6a2ff225bf669a47dfa60666c454ed16e1155ff7da11d20615010-advancedFeatures.png" />

> 📘 Note
>
> To confirm all the updates to the app’s configuration, select **Save Changes**.

**Authorization**

To activate the custom Vbrick app and enable API calls, click the **Authorization** tab to access the Authorization page. Click the **Review and Submit** button and verify the submission details before confirming.

<Image align="center" border={false} src="https://files.readme.io/432805c54c034be9010c7b8505978a4f3e0a00c842663212f38ccc9277b0209e-authorizationTab.png" />

The submission request is forwarded to the Admin or Co-Admin for approval or denial, with an email notification sent to the requester.

<Image align="center" border={false} src="https://files.readme.io/32a583b06b10d492d3f5d37d32c56a939bc72454b2f875817ee0796a3f058ec7-reviewSubmission.png" />

When the custom app is confirmed, listing details will also be noted on the **Authorization** page.

> 🚧 Important!
>
> Be aware that if the app's configuration is modified, you must re-submit it for authorization again.

### Retrieve Credentials for Rev Integration

Once your custom Vbrick app is approved, you need to obtain the credentials you will need to enable it in Rev as your next step.

1. Navigate to the **General Settings** tab and save the **Enterprise ID**.

<Image align="center" border={false} src="https://files.readme.io/472c8396ec79e46e100ff5e6663329fd4d583ffea263cac8c9f8caea69a8a44d-enterpriseID.png" />

2. Navigate to the **Authorization** tab and in the **OAuth 2.0 Credentials** section, copy the **Client ID** and **Client Secret** (which are generated when you click **Fetch Client Secret**).

<Image align="center" border={false} src="https://files.readme.io/b767c076b99c0b5628f1c423f1b4b0df1e7a44fe2eedac7c9b6bf35b8cf88295-clientID.png" />

> 📘 Note
>
> The **Client Secret** details are only visible after completing code verification as part of two-factor authentication (2FA).

### Enable Box in Rev

After you have retrieved your Vbrick app credentials, you are ready to enable the integration in Rev. This will allow the manual import of Box videos directly from the **Upload** tray in Rev from a linked Box account.

To enable Box in Rev:

1. Navigate to **Admin** > **Media Settings** > **Integrations**.
2. Scroll to the **Box** section and select the **Enabled** checkbox.
3. Enter the credentials you saved when creating the custom Vbrick app (see above).

<Image align="center" border={false} src="https://files.readme.io/51d47dfe148e7c000acab47947f86b44dcaa698757908944ecff9d47560d4c44-revEnable.png" />

Your users are now ready to manually import videos directly from the **Upload** tray in Rev from their Box account.

The following roles in Rev have import permissions once the integration is enabled:

* Account Admin
* Media Admin
* Media Contributor
* Media Uploader
* Channel Admin
* Channel Contributor
* Channel Uploader
* Internal Media Contributor
* Internal Media Uploader

## Usage

### Manually Import Box Videos

You can quickly and easily import one or more Box videos into your Rev portal.

To manually import a video from your Box account:

1. Click the **Upload Tray** > **Import** tab > **Box Import** icon.

<Image align="center" border={false} src="https://files.readme.io/16d95a0d36155232440b22d321676fbcff1a2d163f9cbd63d02e5e4376cffc44-uploadTray.png" />

2. If you are not already logged in, you are prompted to log-in to your Box account.
3. Once you log-in, a list of [supported video or audio files](doc:supported-video-and-audio-formats) from the last 180 days (or 100 most recent videos) appears.

<Image align="center" border={false} src="https://files.readme.io/c1d24cd60f1bc42eb569d824dbd0e606e773fe0c2bc609d3302ebc4d440b98b7-boxImport.png" />

4. Use the checkboxes to select the videos you want to import to Rev from your Box account.
5. Click the **Import** button to proceed.

> 👍 Tip
>
> If a video is deleted from Rev, it must be re-imported from Box.
