---
title: AI-Content Analysis
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
If you have enabled [Content Analysis Workflows](doc:content-analysis-workflows) and have [Rev IQ credits](doc:rev-license-types-and-add-ons#licensed-add-on-components) available, you can also add AI-Content Analysis to your process as part of a step or as an entirely independent step. This step is designed to identify and flag sensitive content within transcripts. This includes personally identifiable information (PII), account numbers, credentials, and custom keywords.

## Enable AI-Content Analysis for your Approval Step

To get started:

1. Toggle the switch next to **AI-Content Analysis** label to on.  If this section is not visible, you need to make sure it has been enabled globally by an Account Admin.

> 📘 Note
>
> The video must have a transcript to use this feature.

<Image align="center" src="https://files.readme.io/4791888-enableContentAnalysis.png" />

2. Notice that once you toggle AI-Content Analysis on, you must choose at least one option as part of the approval process.

## Choose an AI-Content Analysis Tool

### Sensitive Data Discovery

This setting is used to automatically search for **personally identifiable information (PII)** such as account numbers, credentials, addresses, passports, and so forth.  Financial information such as credit card numbers, bank accounts, and taxpayer information would also be included in this.  If any sensitive data is found, and this setting is enabled, approvers at the associated step level will be notified.

### Particular Keywords

You can specify **keywords or phrases** that you want to search for by enabling the **Particular Keywords** toggle.  When this is toggled on, a box appears for you to enter the keywords. You are able to enter up to 500 characters. To enter a keyword or phrase and add a new one, press the **Enter** key.  If the keyword or phrase is found in the video transcript, approvers at the associated step level will be notified.

<Image align="center" src="https://files.readme.io/c2eceee-keywordSearch.png" />

## Option to Bypass Approvers

If AI-Content Analysis is enabled for a particular step, you have the option to bypass the approvers associated with that step and automatically approve the video at the step level if the Content Analysis detects no issues. If **Bypass Approver if No Issues Are Detected** is toggled **ON** in a multi-step workflow, and there are *no* issues detected for the AI Content Analysis step, that step will be considered automatically approved, approvers will be skipped, and the video will move on to the next step in the workflow. 

If **Bypass Approver if No Issues Are Detected** is toggled **ON** for a single-step workflow and/or it is **ON** for the last step in a workflow AND there are *zero* issues detected by the analysis, the video will be automatically approved and published after that step. 

This also means that, if you want a **User** or **Group** to have the final approval step, you need to make sure that the **Bypass Approver if No Issues Are Detected** toggle remains in the **OFF** position.

<Image alt="In this approval step, final approval is always left to the users and groups" align="center" src="https://files.readme.io/f67a972-bypassApproverOff.png">
  In this approval step, final approval is always left to the users and groups
</Image>

In this case, **Users** and **Groups** in the **Approvers** box are *always* required to approve (or reject) the content in this step no matter the outcome of the AI-Content analysis that is performed.

If you toggle this switch to the **ON** position, the only time the Approvers are required to intervene is in the event the AI detects an issue with the content (i.e., where issues are found such as sensitive material or a specified keyword is found).  

If no issues are found, the Approvers are bypassed and the approval process continues to the next step or approves the video as the case may be.

<Image alt="In this approval step, final approval is only passed to the users and groups if an issue is detected by Rev's Generative AI" align="center" src="https://files.readme.io/cbb7dd4-bypassApproverOn.png">
  In this approval step, final approval is only passed to the users and groups if an issue is detected by Rev's Generative AI
</Image>
