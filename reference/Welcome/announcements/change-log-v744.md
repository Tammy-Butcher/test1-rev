---
title: Change Log (v7.44)
excerpt: ':calendar: Date Added: December 2021'
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## :star2: **New**

### Delete Video Supplemental Files

Rev v7.44 adds the ability to [Delete Video Supplemental Files](ref:deletevideosupplementalfiles). You can specify an individual supplemental file to delete or delete all supplemental files associated with the video.

## :wrench: **Updated/Fixed**

### Get Webcast Comments Log

The [Get Webcast Comments Log](ref:geteventcomments) endpoint response now supports pagination. Two query parameters have been added to facilitate this; **scrollId** and an optional **size** (count) to specify the number of results returned.

* Example: If **totalComments** &gt; **Count/Size**, then provide the **scrollId** returned from the first request to get the next set of comments (e.g. scrollId=n)

### Granular Role API Updates

Rev v7.44 introduces the concept of [Granular Roles and Permissions](doc:roles-and-permissions#granular-roles-and-permissions). Rev Granular roles are used to grant specific permissions to an account while restricting other functions that are normally packaged with the role. This has implications for Vbrick's API as well.

#### Internal Event Host / Internal Media Contributor Roles

Internal roles are restricted from setting ACL controls to **Public** with regard to video or webcasts. Unauthorized exceptions are returned if this is attempted.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Endpoint
      </th>

      <th>
        Role / Restriction
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <ul>
          <li>[Create Webcast](ref:createevent)</li>
          <li>[Update Webcast](ref:editevent)</li>
          <li>[Patch Webcast](ref:patchwebcast)</li>
        </ul>
      </td>

      <td>
        The **Internal Event Host** role (that does not also have the Event Host, Event Admin, or Account Admin roles in addition to this role) may *not* set the event to **Public**. 

        The role may edit an existing event *only* if they are the Internal Event's Host/Event Host (or an Event Admin).

        An unauthorized error is returned if this is attempted.
      </td>
    </tr>

    <tr>
      <td>
        <ul>
          <li>[Upload Video](ref:uploadvideo)</li>
          <li>[Update Video Details/Metadata](ref:editvideo)</li>
          <li>[Update Video Access Control](ref:editvideoaccesscontrol)</li>
          <li>[Patch Video Details/Metadata](ref:editvideopatch)</li>
        </ul>
      </td>

      <td>
        The **Internal Media Contributor** role (that does not also have the Media Contributor, Event Host, Event Admin, Media Admin, or Account Admin in addition to this role) may *not* set a video to **Public**. 

        That means, this role *restricts* the ability to make videos and recordings **Public** even when granted edit permissions by another user account.

        This role may edit a Public video in this case but it may *not* change a Private video to Public.

        An unauthorized error is returned if this is attempted.
      </td>
    </tr>
  </tbody>
</Table>

#### Rev IQ Role

All [Rev IQ](doc:rev-ai) features and functions are now restricted to accounts that have this role.

> 👍 Tip
>
> All Admin accounts include the **Rev IQ** functions.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Endpoint
      </th>

      <th>
        Role / Restriction
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <ul>
          <li>[Create Webcast](ref:createevent)</li>
          <li>[Update Webcast](ref:editevent)</li>
          <li>[Patch Webcast](ref:patchwebcast)</li>
        </ul>
      </td>

      <td>
        Only the Rev IQ role may **Set Live Subtitles to True** when using the webcast endpoints going forward.

        An unauthorized error is returned if this is attempted and the Rev IQ role is not in place.
      </td>
    </tr>

    <tr>
      <td>
        [Transcribe Video](ref:transcribevideo)
      </td>

      <td>
        Only the Rev IQ role can use this endpoint as of v7.44. This only applies if serviceType = Vbrick.

        An unauthorized error is returned if this is attempted and the Rev IQ role is not in place.
      </td>
    </tr>

    <tr>
      <td>
        [Translate Video](ref:translatevideo)
      </td>

      <td>
        Only the Rev IQ role can use this endpoint as of v7.44. 

        An unauthorized error is returned if this is attempted and the Rev IQ role is not in place.
      </td>
    </tr>

    <tr>
      <td>
        [Tag Users in Video](ref:tagusersinvideo)
      </td>

      <td>
        Only the Rev IQ role can use this endpoint as of v7.44. 

        An unauthorized error is returned if this is attempted and the Rev IQ role is not in place.
      </td>
    </tr>
  </tbody>
</Table>

## :+1: Partner Account Updates

### End Webcast API Enhancements

Partner accounts can now delay the true ending of a webcast through the use of a new **gracefulEnd** parameter.

This parameter is available on the [End Webcast](ref:endevent) and [Stop Broadcasting Webcast](ref:pausebroadcastevent) endpoints. It is used to ensure that attendees do not receive the end command before the end of their segment/buffer is reached.

For now, **gracefulEnd** is only available to Partner accounts.