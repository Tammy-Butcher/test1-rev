---
title: Manage and Add DMEs
excerpt: >-
  This guide explains how to use the DME Management module to add, configure,
  and manage Vbrick DMEs.  This includes bulk schedule, reboot, and software
  update actions.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
</div>

<style>
  
 .feature {
list-style-type: none;
   text-indent:10px;
   width: 60%;
   margin: 10px 10px;
   padding-top: 5px;
   padding-bottom: 15px;
   padding-left:10px;
display: block;
   background-color:#F6F3F3;
   border-radius: 10px;
   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;
   
}
  
</style>
`}</HTMLBlock>

Vbrick's **Distributed Media Engine** (DME) is a versatile, highly-configurable media distribution engine that moves streaming video to and from a wide variety of sources and endpoints. With the DME you can distribute your video to anyone, anywhere, using a variety of robust IP networking options. In Rev, DMEs are added as a **Device** and are designated as the **Viewing Destinations** of your video content on the network.

The **DME Management** module is where DMEs are added and managed.  This module is where most actions and information about your DMEs is conducted and viewed. Account Admins access the DME Management module from **Devices** > **DME Management**.

<Image title="dmeManagement.png" alt={1202} align="center" src="https://files.readme.io/71c4e72-dmeManagement.png">
  Account Admins use the DME Management module to obtain information and perform configuration options on their DME devices
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Column
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
        Name or Host name of the DME.
      </td>
    </tr>

    <tr>
      <td>
        Version
      </td>

      <td>
        The current build version of the DME.
      </td>
    </tr>

    <tr>
      <td>
        MAC Address
      </td>

      <td>
        The MAC address of the DME.
      </td>
    </tr>

    <tr>
      <td>
        Scheduled Download
      </td>

      <td>
        Specifies if the DME has scheduled download times.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        The status of the device; **Online**, **Offline**, or **Inactive**.  

        If Inactive, the DME is not accessible by Rev. During a software update, the progress of the update is also displayed here.
      </td>
    </tr>

    <tr>
      <td>
        Used For Streaming
      </td>

      <td>
        Specifies if the DME is authorized for [streaming](doc:stream-authorization-lockdown) and not in lockdown status.
      </td>
    </tr>

    <tr>
      <td>
        MFSTB
      </td>

      <td>
        Specifies if the DME is designated as a [STB Connector DME](doc:set-up-an-stb-connector-dme).
      </td>
    </tr>

    <tr>
      <td>
        Actions
      </td>

      <td>
        The **Actions**dropdown functions:  

        <li>**Sync Now**: Perform an immediate [synchronization](doc:synchronize-dme-content).</li>  
        <li>**Reboot**: Reboot the selected DMEs. This bulk reboots all selected DMEs or a single DME if only one is selected.</li>  
        <li> **View Log**: View a log of recent actions that have occurred on the device. This is good for troubleshooting if your device is not performing as expected.</li>  
        <li>**Request Logs**: Gathers necessary logs from the DME and sends them securely to Vbrick Support. (Requires DME v3.24+. This can also be completed in **Bulk Actions** with one ore more DMEs selected. Do not complete this action during events as it can be labor intensive. An email and notification is generated when the logs are complete and support is able to view them. </li>  
        <li> **Delete**: When a device is deleted, the content stored on the device is not deleted. However, you may not access it because the association to the device is removed. </li>
      </td>
    </tr>

    <tr>
      <td>
        Bulk Actions
      </td>

      <td>
        Bulk Actions that may be taken on multiple DMEs:  

        <li>**Reboot**: Reboots the selected DMEs. You must have at least one DME selected.</li>  
        <li> **Scheduled Download**: Set up an identical [download schedule](doc:synchronize-dme-content#bulk-schedule-dme-content) for several DMEs at once. </li>  
        <li> **Update**: Update the [software version](doc:update-dme-software-version) for one or more DMEs.</li>  
        <li> **Request Logs**: Request the logs of one or more DMEs be sent to Vbrick Support. Must have v3.24+ of the DME software installed.</li>
      </td>
    </tr>
  </tbody>
</Table>
