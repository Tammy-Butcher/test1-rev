---
title: Add an Encoder
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
Encoders are normally designated as a video streaming *source* of your network or, in other words, where your video is input *from*.

To add an encoder select **Add an Encoder** from the **Add a Device** dropdown and complete the required fields.  Click the **Create** button to save the encoder. After a few seconds, the Encoder status should flip from **Uninitialized** to **Active**. 

If the status does not change, check the **MAC Address** field to ensure it is correct and the encoder configuration steps such as the **API Key** and **Host** fields. 

**View**: [Getting Started With Rev Devices](doc:getting-started-with-rev-devices) 

<Image title="addEncoder.png" alt={1174} src="https://files.readme.io/eaaf971-addEncoder.png">
  Your encoders do not need video streams added if you are using DMEs as video destinations
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field Name
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
        The status of the encoder may be set to **Active**or **Inactive**upon adding it to Rev.
      </td>
    </tr>

    <tr>
      <td>
        MAC Address
      </td>

      <td>
        The **MAC Address** is required. Copy the MAC Address for an Encoder from the **Monitor**> **Network**page in the Encoder's UI.
      </td>
    </tr>

    <tr>
      <td>
        Video Streams
      </td>

      <td>
        Click the **Add URL** button to add the **Name**, **URL**, **Encoding Type**, and **Multicast**specification of a video stream.  These are required fields if the encoder is intended to be utilized as a streaming device for Live events and Webcasts. 

        These video streams are later selected on **Presentation Profiles** as viewing *destinations*.

        * *Note\*\*: The*exception *to this scenario is if you are using the*DME *as a video*destination\*. In this case, you do not need to add a URL for the encoder because the DME is providing the video destination URLs instead of the encoder.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Note
>
> Account Admins are sent an email notification if any DME or Encoder goes into **Warning** or **Offline** status so that they may pro-actively troubleshoot the device.
