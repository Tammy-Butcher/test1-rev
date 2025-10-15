---
title: Device Compatibility Matrix
excerpt: >-
  The current supported version(s) of all Vbrick devices and compatibility
  matrix.  Contact Vbrick Support if you need assistance with upgrading.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
As always, please review current DME, Encoder, LDAP connector, and VBM agent versions within your specific environment.

For cloud customers, Vbrick deploys Rev several times a year which includes new versions of the LDAP Connector. Cloud Rev is always tested with the previous two versions of **LDAP Connector**. Vbrick recommends that Rev Cloud customers verify that they are using the most recent LDAP Connector.

Additionally, there may be new releases of the **Vbrick Multicast (VBM)** agents/software. The VBM agent ships with a security certificate from Vbrick (unless a customer provides their own security certificate). All certificates, either provided by Vbrick or customer provided, are expiry limited (by use in browsers) to **397** days.  Please review your certificate expiry date and plan accordingly.

[block:parameters]
{
  "data": {
    "h-0": "Rev Versions",
    "h-1": "DME Versions",
    "h-2": "Encoder Versions",
    "h-3": "LDAP Connector Versions",
    "h-4": "VBM Agent Versions",
    "0-0": "Current Rev Cloud Release - <<revCloud>>",
    "0-1": "DME - <<dmeCloud1>>",
    "0-2": "Encoder - <<cloudEncoder1>>",
    "0-3": "<<ldap1>>  \n<<ldap2>>",
    "0-4": "<<vbmCloud>>",
    "1-0": "Rev On-Premises Release - 7.64",
    "1-1": "DME - 3.35.x",
    "1-2": "Encoder - 4.10",
    "1-3": "N/A",
    "1-4": "2.11",
    "2-0": "Rev On-Premises Release - 7.60",
    "2-1": "DME - 3.33.x",
    "2-2": "Encoder - 4.10",
    "2-3": "N/A",
    "2-4": "2.7"
  },
  "cols": 5,
  "rows": 3,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


<sup>Please review the Vbrick support agreement for necessary dates associated with On-Premises support and expected update schedules.</sup>