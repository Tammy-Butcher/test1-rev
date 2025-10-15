---
title: Use LDAP and Active Directory
excerpt: >-
  This guide explains how to configure LDAP and Active Directory for use with
  Rev Cloud and On-Premise installations.  It also provides instructions on
  importing specific groups versus multiple groups from an LDAP Server.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Rev easily imports **LDAP groups** that are set up on a single **Active Directory (AD)** server. This means you can manage your users separately from the Rev portal and specify how often Active Directory syncs back to Rev with updates. 

You can choose to import *all* LDAP groups associated with an AD server or you may select only specific groups to import to make more efficient use of your time.

There are 3 steps to configure Rev so that LDAP groups are imported and synchronized. LDAP configuration *must* be completed before you can import LDAP groups.

1. [Create an API Key](doc:create-an-api-key) to use specifically with the LDAP Connector.

2. Download and [Install Rev Cloud LDAP Connector](doc:install-rev-cloud-ldap-connector). (On-Prem installations may skip this step)

3. [Add LDAP Connector Device](doc:add-ldap-connector-device) in Rev.

<Image alt="Make sure you create an API Key and install Rev Cloud LDAP before you add your LDAP Connector Device" align="center" src="https://files.readme.io/b1d8027-sourceDeviceLDAP.png">
  Make sure you create an API Key and install Rev Cloud LDAP before you add your LDAP Connector Device
</Image>

Once you complete these 3 steps, you may [Import an LDAP Group to Rev](doc:groups#import-an-ldap-group).
