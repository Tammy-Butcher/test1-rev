---
title: Using the AI Search Integration
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
ServiceNow Admins can make sure that their ServiceNow portals are always in-sync with their Vbrick Rev platforms by installing and configuring the **Vbrick Video AI Search Connector** from the [ServiceNow Marketplace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/2a3d530f87b4e1100af91f873cbb35a0/2.0.14). 

Once installed, you can:

* Toggle **Sync Videos** on which syncs and indexes all videos that are **Public** or **All Users** into AI search on an hourly basis. **Private** videos are restricted from AI search.
* Allows you to manually sync all videos that are **Public** or **All Users** into search on-demand by clicking the **Get Updates** button.
* Build custom **Now Assist** skills that can use metadata from videos to recommend relevant videos, summarize video content, or extract custom insights.
* View search logs as needed to verify your syncs.

## Requirements

* **Vbrick Rev Cloud** v7.62+
* **Vbrick Video** app v2.2.5+
* **Vbrick Video AI Search** app v1.0.0+ (installation and configuration options are included in the zip file downloaded with the app just as with the Vbrick Video app)
* **External Content for AI Search** v1.0.0+
* **AI Search Spoke** v2.0.3+
* ServiceNow Integration Hub Action Template - **Data Stream** v1.0.0+
* A Vbrick Rev user account that has an email that matches the email being used in the ServiceNow account.
* The Vbrick Rev account performing the installation/configuration steps must be an Account Admin account on both the Vbrick and ServiceNow instances.
* **Optional**: **Now Assist in AI Search** v11.0.14+ for **Vbrick AI Search Connector 2.0** in **Yokohama Patch 4** to integrate with Now Assist

## Vbrick Video AI Search Connector Usage

Once a ServiceNow admin has installed and configured the **Vbrick Video AI Search Connector** app,  two options are available when you search on Vbrick; **AI Search Logs** and **AI Search Settings**. Using these options, you can configure the app to sync ServiceNow with the Vbrick Rev portal of your choice.  You are also able to verify the sync settings you choose by viewing search logs.

<Image alt="Two new options are available once the Vbrick Video AI Search Connector is installed" align="center" src="https://files.readme.io/97c8eda7ae631c9e9a49501ff1671db1cf4bcaec14563e8098ffc53e54094162-AISearchConnectorOptions.png">
  Two new options are available once the Vbrick Video AI Search Connector is installed
</Image>

**Optional**: You can also choose to configure **Now Assist in AI Search** by searching on Now Assist in the search box.

<Image alt="Select Now Assist Multi-Content Response to enable Vbrick External Content responses in Now Assist for each portal" align="center" src="https://files.readme.io/31a1acc3782329a6ad4aa2be3fad372c2f1586e81d4a4a38328236bd57391188-now_assist_navigation.png" />

Select the **Now Assist Multi-Content Response** to enable Vbrick External Content responses in Now Assist for each portal.

<Image align="center" src="https://files.readme.io/e02f0dc393202977fbfff71c2d6025c3aa8089e844731b5c8cd87660ad2e20af-Set_up_Now_Assist_in_AI_Search.png" />

### AI Search Settings

Clicking the **AI Search Settings** link navigates you to the **Vbrick Video AI Search Sync** page.  Using the auto sync or manual sync features on this page allows you to sync all of your Public or All Users designated videos in Rev to AI search in **ServiceNow Employee Service Center** and keep them up-to-date. 

This means if a video is deleted, is made inactive, marked unlisted, placed on Legal Hold, and so forth they are updated in ServiceNow as well and do not show up in Employee Center searches.

<Image align="center" src="https://files.readme.io/05975793abcaef32f3f1611efe0fbb5fa710d837b9d8cba5096763395514d158-searchSettingsPage.png" />

#### Syncing Videos Automatically to AI Search

When you toggle the **Sync Videos** switch to ON:

* You can select the Rev portal to sync to if you are connected to more than one in the **Select Portal** drop-down that will appear.
* The **Sync Status** of the last sync is present with a link to the logs.
* All videos from Vbrick Rev that are **Public** or **All Users** are indexed into the AI search automatically, every hour. **Private** videos are restricted and *not* synced.
* The videos continue to sync between Rev and ServiceNow every hour which is the default setting.
* The most recent sync's date and time is always shown in the **Last Update** field.

#### Manually Sync Videos to AI Search (Interval Sync)

When you click the **Get Updates** button on the AI Search Sync page:

* All videos from Vbrick Rev that are **Public** or **All Users** are indexed into the AI search just as if the Sync Videos toggle is performing an automatic sync. **Private** videos are still restricted and *not* synced.
* The difference is that the sync is performed on-demand immediately and does wait for the hourly default sync. This is termed an incremental search in the AI Search logs.

After you make your setting selection, notice that when you search the Service Portal for vbrick videos, a tab displays with the most recent videos that have been synced either automatically or incrementally (on-demand).

<Image align="center" src="https://files.readme.io/35b0901e4e722769af99311f514b9d59ed7aa2d1bbc0b2a01a78007c2175e3ba-searchResults.png" />

Notice that the results display:

* Video owner
* Duration
* Total views
* Publish date

If you click the video, you are taken to the video player widget.

> 📘 Note
>
> In this example, the AI Search tab is titled "Vbrick External Content". Your Admin may have configured the tab name differently, such as "Vbrick Videos".  The end result should be the same in that it directly matches what you see in **AI Search logs** as far as synced numbers for the tenant you are viewing.

### Use AI Search Logs to Verify a Sync

Clicking the **AI Search Logs** link allows you to view various tenant logs to verify the automatic and manual syncs that have been made between ServiceNow and your Vbrick Rev portals (if you have more than one linked).

Use the drop-down menu to filter between the various views you want to see (Tenant ID, Start, End, Sync Type, etc.) to easily validate the syncs that have been performed.

> 📘 Note
>
> Click on the **Vbrick AI Search Logs** text to add even more filters such as "Group By", "Rows", and the ability to add favorites.

<Image align="center" src="https://files.readme.io/6681ad06b351c80b30743fed3b84fca46af49a595207b5fb6ca03e50abce7643-searchLogs.png" />

## Toggle Video Sync Off and Delete Videos from AI Search

You can stop the AI sync at any time and remove videos from the search by setting the **Sync Videos** toggle to OFF in **AI Search Settings**. If you do this, your ServiceNow portal will stop syncing with Vbrick Rev and will remove all previously synced videos from the AI search. This can also be verified through the **AI Search Logs**. The **Sync Type** will be noted as delete and the number of items (videos) will be listed.

<Image alt="A delete sync type occurs when you toggle sync off. The videos are removed from AI Search." align="center" src="https://files.readme.io/8f269a2e0c7a514aba94a9a91eb87c23610f8ed799f5d6caf92e8b21e14a9b3c-stopSync.png">
  A delete sync type occurs when you toggle sync off. The videos are removed from AI Search.
</Image>

> 📘 Note
>
> Deleting will remove videos from AI Search but it does not remove them from Rev.
