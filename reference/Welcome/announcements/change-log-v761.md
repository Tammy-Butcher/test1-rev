---
title: Change Log (v7.61)
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## :star2: **New**

### Sensitive Content Flag in Video Endpoints

There is now a **sensitiveContent** flag for our video endpoints that completely removes a video from search and most views within the platform. This boolean flag is set to **false** by default and must be enabled through Vbrick support before use. It can be set and is returned in the following endpoints:

- [Upload Video](ref:uploadvideo-1)
- [Add Video Link](ref:createvideolink-1)
- [Update Video Details/Metadata](ref:updatevideo)
- [Patch Video Details/Metadata](ref:editvideopatch)
- [Migrate Video](ref:migratevideo)
- [Get Video Details/Metadata](ref:getvideosdetails)
- [Search Videos](ref:searchvideo)

## :wrench: **Updated/Fixed**

### Video Editing Updates

The [Edit Video](ref:editvideo) endpoint has been updated this release to support the new [Merge Video](doc:merge-videos)  feature released in v7.61. With the addition of the **videoId** parameter, you can insert an existing clip into the video you are currently editing by setting the **start** and **end** time where the identified clip should be merged.

### Media Uploader and Internal Media Uploader Updates for Role Endpoints

With the introduction of the new **Media Uploader** and **Internal Media Uploader** [roles](doc:roles-and-permissions), all endpoints that use the **roleType** parameter are now able to select these values.

In addition to this, the **channelRoleType** now includes the **Uploader**.

### Search Video Endpoint Update

When using the **owners** parameter with the [Search Videos](ref:searchvideo) endpoint, **username** is now used as the search criteria instead of firstname and lastname.