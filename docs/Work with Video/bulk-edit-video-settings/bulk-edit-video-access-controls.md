---
title: Bulk Edit Video Access Controls
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
Use the [Access Control](doc:video-access-control) dropdown to modify the access control of several videos at once in the [Bulk Editing](doc:bulk-edit-video-settings) interface. Access may be specified to **Public**, **All Users**, or **Users, Groups and Channels** just as if you are setting the Access Control on one video at a time in [video settings](doc:video-access-control). 

To begin:

1. In the **Access Control** dropdown, select which access setting you want to set on the videos you have selected. In the example below, all selected videos will be set to **Public**. 

<Image title="accessControlPublic.png" alt="The Access Control dropdown specifies the what type of access to grant" align="center" src="https://files.readme.io/79ff3cf-publicAccessControl.png">
  The Access Control dropdown specifies the what type of access to grant
</Image>

2. Once the type of access is selected, the **Access Control List** dropdown is used to modify the permissions on it by adding, replacing, or removing them from the selected videos. **Edit Access** to specific users, groups, and channels may also be applied as need.  More details are described in the following sections.

## Add Access

Use **Add** in the **Access Control List** dropdown to *add* additional access or specify **Edit Access** to several videos at once.  Note this does *not* remove or replace any prior access to the video(s) that has already been granted.

For example, two groups will be added to all selected videos in the image below: Human Resources and Training. 

Additionally, the Training group will also be granted **Edit Access** to the videos selected because the Edit Access button next to it is selected.

<Image title="appendAccessControlList.png" alt="Add in the Access Control List adds access to the video(s) that are selected in Bulk Editing" align="center" src="https://files.readme.io/1085d67-addAccess.png">
  Add in the Access Control List adds access to the video(s) that are selected in Bulk Editing
</Image>

## Remove Access

Use **Remove** in the **Access Control List** dropdown to *remove* either view access or  **Edit Access** (or both) from several videos at once. 

For example, in the image below, the Human Resources group will have *both* view and edit access removed from selected videos.  The Training group, however, will have **Edit Access** *only* removed (because it is checked) and still retains view access.

> 🚧 Important!
>
> It is important to understand when using **Remove** that if you have **Edit Access** selected (as seen with the Training group) then the remove function applies *only to the removal of editing access and not the entity’s view access* to the videos selected.  
>
> This is why the Training group in the example below only has edit access removed and not view access while the Human Resources group has both removed.  This is an important distinction.

<br />

<Image title="removeAccessControlList.png" alt="Remove in the Access Control List removes view access to the video(s) OR Edit Access only (if selected)" align="center" src="https://files.readme.io/be3c962-removeAccess.png">
  Remove in the Access Control List removes view access to the video(s) OR Edit Access only (if selected)
</Image>

## Replace Access

Use **Replace** in the **Access Control List** dropdown to *replace* either view access or  **Edit Access** (or both) for several videos at once. 

For example, in the image below, all selected videos will be set to **Users, Groups and Channels** access with only the Human Resources and Training groups granted view access. No **Edit Access** has been granted. 

All prior view and Edit Access on the selected videos *will be wiped and replaced*. It is important to keep this in mind about the Replace function.

<Image title="replaceAccessControlList.png" alt="Replace in the Access Control List replaces view access to the video(s) OR Edit Access (if selected) AND replaces all prior view and edit access" align="center" src="https://files.readme.io/e78aeaf-replaceAccess.png">
  Replace in the Access Control List replaces view access to the video(s) OR Edit Access (if selected) AND replaces all prior view and edit access
</Image>
