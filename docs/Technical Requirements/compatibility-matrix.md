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

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "left" }}>
        Rev Versions
      </th>

      <th style={{ textAlign: "left" }}>
        DME Versions
      </th>

      <th style={{ textAlign: "left" }}>
        Encoder Versions
      </th>

      <th style={{ textAlign: "left" }}>
        LDAP Connector Versions
      </th>

      <th style={{ textAlign: "left" }}>
        VBM Agent Versions
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "left" }}>
        Current Rev Cloud Release - {user.revCloud}
      </td>

      <td style={{ textAlign: "left" }}>
        DME - {user.dmeCloud1}
      </td>

      <td style={{ textAlign: "left" }}>
        Encoder - 4.10
      </td>

      <td style={{ textAlign: "left" }}>
        {user.ldap1}\
        {user.ldap2}
      </td>

      <td style={{ textAlign: "left" }}>
        {user.vbmCloud}
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Rev On-Premises Release - 7.64
      </td>

      <td style={{ textAlign: "left" }}>
        DME - 3.35.x
      </td>

      <td style={{ textAlign: "left" }}>
        Encoder - 4.10
      </td>

      <td style={{ textAlign: "left" }}>
        N/A
      </td>

      <td style={{ textAlign: "left" }}>
        2.11
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Rev On-Premises Release - 7.60
      </td>

      <td style={{ textAlign: "left" }}>
        DME - 3.33.x
      </td>

      <td style={{ textAlign: "left" }}>
        Encoder - 4.10
      </td>

      <td style={{ textAlign: "left" }}>
        N/A
      </td>

      <td style={{ textAlign: "left" }}>
        2.7
      </td>
    </tr>
  </tbody>
</Table>

<sup>Please review the Vbrick support agreement for necessary dates associated with On-Premises support and expected update schedules.</sup>
