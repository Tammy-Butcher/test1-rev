---
title: Add a Custom Device
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
Rev supports adding a Custom Device that you may configure as either a source or a destination (or both) in addition to using Vbrick’s Encoders and DMEs.

To add a Custom Device select **Add Custom Device** from the **Add a Device** dropdown and complete the required fields.

<Image title="addCustomDevice.png" alt={1202} src="https://files.readme.io/e0f9e42-addCustomDevice.png">
  Rev supports custom devices as video sources or viewing destinations through the Custom Device control
</Image>

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
        Name
      </td>

      <td>
        This can be a name of your choosing. This is a required field. Descriptive location or Host name is recommended.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        The status of your device may be set to **Active**or **Inactive**.
      </td>
    </tr>

    <tr>
      <td>
        IP Address
      </td>

      <td>
        The **IP address** of where your device is located.  This is a required field.
      </td>
    </tr>

    <tr>
      <td>
        Capabilities
      </td>

      <td>
        At least *one*capability is required. You must designate that the device is either a **Video Stream Source** or a **Video Stream Viewing Destination** (or both). 

        If you designate the device as a **Video Stream Viewing Destination**, then **Video Streams** are required.
      </td>
    </tr>

    <tr>
      <td>
        Video Streams
      </td>

      <td>
        * \*Nam&#x65;**,**&#x55;R&#x4C;**,**&#x45;ncoding Typ&#x65;**, and**Multicast **are all designated \[through the**Add URL\*\* button] and are required fields if the device is intended to be utilized as a viewing destination device. 

        These streams are later selected on **Presentation Profiles** as viewing destinations or can also be used for automatic multicast viewing.
      </td>
    </tr>
  </tbody>
</Table>

## HLS Stream Preparation for Automatic Multicast and Reflection

To optimize the use of **Custom Devices** features, the **HLS** stream should meet certain specifications.

Review DME Online Help on stream specifications in the [Rev Initiated Multicast and Reflection](https://portal.vbrick.com/help/dme/3240/index.html#page/AdminGuide/OutputConfiguration.10.12.html#) topic.
