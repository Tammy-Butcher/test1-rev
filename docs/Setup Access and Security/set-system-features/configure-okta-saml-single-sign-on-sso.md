---
title: Configure Okta SAML Single Sign On (SSO)
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
## Prerequisites

Before setting up **Okta SAML SSO**, you must enable Single Sign On authentication on your Vbrick Rev tenant. Refer to the [Configure Single Sign On (SSO)](doc:configure-single-sign-on-sso) topic for complete details on setting up SAML SSO and SAML User (Just-In-Time) provisioning. SAML User provisioning is not enabled by default, and you need to contact [Vbrick Support](mailto:support@vbrick.com) to enable it.

## Supported Features

The **Vbrick Okta SAML** integration currently supports the following features:

* SP-initiated SSO
  * SSO Sign-in can be initiated from Vbrick Rev Cloud via https\://\<Vbrick\_Rev\_Domain>
* JIT (Just-In-Time) User Provisioning

## Configuration Steps

To configure Okta SAML SSO, complete the following steps:

1. Add Vbrick Rev Cloud from the **Okta App Catalog**.
   1. Sign in to your Okta admin dashboard.
   2. Navigate to Applications > Applications > Browse App Catalog. 
   3. Search for **Vbrick Rev Cloud** using the search bar and click on the **Vbrick Rev Cloud** app. ([https://www.okta.com/integrations/vbrick-rev-cloud/](https://www.okta.com/integrations/vbrick-rev-cloud/))
   4. Click **Add Integration**.
   5. In the Vbrick Rev Cloud app, on the **General Settings**, enter the Vbrick Rev Tenant domain/hostname.
   6. Click the **Assignments** and assign any users or groups that you would like to have access to Vbrick Rev Cloud.
2. Provide the Okta Integration information to your Vbrick Rev tenant.
   1. Sign in to your Vbrick Rev tenant as an **Account Admin**.
   2. Navigate to **Admin** > **System Settings** > **User Security**.
   3. Under **SAML Single Sign On** section:
      1. Enable Single Sign On
      2. Select **NameIdentifier Element** for SAML Identity Location
      3. If SAML User Provision is enabled:
         1. Enter **firstName** for First Name Attribute Element Name
         2. Enter **lastName** for Last Name Attribute Element Name
         3. Enter **email** for Email Attribute Element Name
         4. Copy the **Okta IDP metadata XML** in Identity Provider Metadata
         5. Select **SHA256withRSA** for Signature Algorithm
         6. Enable **Sign SAML Request**
         7. Enable **SAML Response Signed**

<Image align="center" src="https://files.readme.io/96ce759a21c3ffa08af34e679d8b8608219fde5caa63d2261d0803b9406aef66-setupSSO.jpg" />

## SP-initiated SSO

The sign-in process is initiated from Vbrick Rev Cloud

1. From your browser, navigate to the https\://\<Vbrick\_Rev\_Domain> sign-in page.
2. Enter your Okta credentials and click "Sign in with Okta".
3. If your credentials are valid, you are redirected to the Vbrick Rev Cloud.

## Notes

The following SAML attributes are used by this integration:

| Name      | Okta Value     |
| :-------- | :------------- |
| firstName | user.firstName |
| lastName  | user.lastName  |
| email     | user.email     |

<br />

> 📘 Note
>
> Refer to the [Configure Single Sign On (SSO)](doc:configure-single-sign-on-sso) topic for detailed SSO information.
