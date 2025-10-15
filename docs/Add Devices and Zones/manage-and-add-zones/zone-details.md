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

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2896e49-zoneDetails.png",
        "zoneDetails.png",
        1105
      ],
      "align": "center",
      "caption": "Section 1:  Zone Details"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field or Setting",
    "h-1": "Description",
    "0-0": "Zone Name",
    "0-1": "A descriptive name for the zone; normally indicative of where the zone covers or what types of devices it houses. This is a required field. ",
    "1-0": "IP Addresses",
    "1-1": "Both **IPv4** and **IPv6** address are accepted.   Multiple addresses can be entered.  They can be entered in as single addresses, as a range IPAddress-IPAddress, or as a range defined with Classless Inter-Domain Routing (CIDR) notation.  (Ranges can not span both IPv4 AND IPv6 ranges simultaneously.)  \n  \n**IPv4 Spanning Examples**: 168.222.108.0-168.222.108.255 **or** 168.222.108.0/24  \n  \nThese addresses, which should be unique across account zones, are used to delineate zone membership.  Meaning, ff a User's **IP Address** falls into the range specified, the zone is used for that User and content is served from that zone and device.  \n  \nThis field is important when setting up Zone logic and hierarchy.  This field is required."
  },
  "cols": 2,
  "rows": 2,
  "align": [
    "left",
    "left"
  ]
}
[/block]