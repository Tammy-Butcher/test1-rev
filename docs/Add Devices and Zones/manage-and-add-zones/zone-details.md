---
title: Zone Details
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
The first section, **Zone Details**, contains the primary information defining the Zone -- **Zone Name** and **IP Addresses**.

<Image title="zoneDetails.png" alt={1105} align="center" src="https://files.readme.io/2896e49-zoneDetails.png">
  Section 1:  Zone Details
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field or Setting
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Zone Name
      </td>

      <td>
        A descriptive name for the zone; normally indicative of where the zone covers or what types of devices it houses. This is a required field. 
      </td>
    </tr>

    <tr>
      <td>
        IP Addresses
      </td>

      <td>
        Both **IPv4** and **IPv6** address are accepted.   Multiple addresses can be entered.  They can be entered in as single addresses, as a range IPAddress-IPAddress, or as a range defined with Classless Inter-Domain Routing (CIDR) notation.  (Ranges can not span both IPv4 AND IPv6 ranges simultaneously.)  

        * \*IPv4 Spanning Example&#x73;**: 168.222.108.0-168.222.108.255**or\*\* 168.222.108.0/24  

        These addresses, which should be unique across account zones, are used to delineate zone membership.  Meaning, ff a User's **IP Address** falls into the range specified, the zone is used for that User and content is served from that zone and device.  

        This field is important when setting up Zone logic and hierarchy.  This field is required.
      </td>
    </tr>
  </tbody>
</Table>
