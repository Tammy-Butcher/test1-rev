---
title: Add or Edit a Zone
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
This topic covers adding a new zone.  Additional topics in this section provide descriptions of adding and configuring the [distribution modalities](doc:vbrick-distribution-modalities) when you are ready.

### **Before You Begin:** Plan Distribution and Zone Architecture

Before adding or editing a zone, please review your [distribution](doc:vbrick-distribution-modalities) and zone [architecture](doc:manage-and-add-zones#zone-hierarchy).  You may wish to include your IT or Network operations teams to make sure you have all the necessary details (e.g., IP ranges) when planning changes to the zones.

### **Step 1.** Add a Zone or Select a Zone to Edit

To add or edit a zone:

1. Navigate to **Admin** > **Devices** > **Zones**:
2. Click **Add Zone** to add a new zone or click a **Zone Name** in the table to edit an existing zone.

You are directed to a **Zone Detail** page that contains three different sections. The visibility of the sections is based on the [customer license](doc:rev-license-types-and-add-ons).  The Zone Detail page is the same for both adding and editing a zone.  The zone sections are outlined in the following table.

| Section               | Viewable By (Customer Type)     | Configure                                                            |
| :-------------------- | :------------------------------ | :------------------------------------------------------------------- |
| Zone Details          | All Vbrick Customers            | Zone Name and IP Addresses used                                      |
| Vbrick Rev Settings   | Vbrick Rev / EVP Customers Only | Rev-related configurations                                           |
| Vbrick Universal eCDN | All Vbrick Customers            | Specifications for all available distribution modalities in the zone |

***

### **Step 2.** Zone Details

All Vbrick customers are able to view the [Zone Details](doc:zone-details) section and should complete the fields for this Zone.  Make sure you understand the Rev settings discussed in the topic completely.

***

### **Step 3.** Vbrick Rev Settings

If you are a Vbrick Rev / EVP customer, the [Vbrick Rev Zone Settings](doc:vbrick-rev-zone-settings) section is visible to you. Make sure you understand the bitrate and override settings described on this topic.

***

### **Step 4.** Vbrick Universal eCDN

All customers can configure the [distribution modalities](doc:vbrick-distribution-modalities) that will be available for this Zone. Also, keep in mind, if you utilize **Zone Hierarchy**, these modalities may also be available to other IP address spaces. Please review the following articles:

* [Vbrick Multicast](doc:vbrick-multicast)
* [Vbrick Peer-to-Peer Zones](doc:rev-connect-zones)
* [Source Unicast](doc:source-unicast)
* [Vbrick Caching and Devices](doc:vbrick-caching-and-devices)

***

### **Step 5** Save and Test

At this point, you have made all your changes.  Click either the **Create** button (if you are creating or adding a new zone) or **Update** button (if you are modifying an existing zone.). They are at the top (and bottom) of the form.  Don't forget to save your work, and test it thoroughly.
