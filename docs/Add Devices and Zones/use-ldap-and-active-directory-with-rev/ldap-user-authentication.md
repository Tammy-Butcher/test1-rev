---
title: LDAP User Authentication
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
**LDAP User Authentication** is enabled for log-in with LDAP credentials by default.

If disabled, this means that users and groups still use LDAP sync.  However, Users are authenticated through SAML instead.  If a User attempts to use LDAP credentials, an error message is received.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/059a490-disableLdapAuthentication.png",
        "disableLdapAuthentication.png",
        705,
        203,
        "#ecece8"
      ],
      "caption": "When authentication is disabled as seen here, Users are authenticated through SAML instead of LDAP"
    }
  ]
}
[/block]