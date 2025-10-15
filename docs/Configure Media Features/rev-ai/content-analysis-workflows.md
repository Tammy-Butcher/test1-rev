---
title: Content Analysis Workflows
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
[block:html]
{
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n <li>&#128736; <a href=\"/docs/rev-ai\">Rev IQ Module</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


Enable **Content Analysis Workflows** to include an AI-powered content analysis tool in [Content Approval Processes](doc:create-an-approval-process) you have defined for your video uploads. You can have [Rev's AI-Content Analysis](doc:ai-content-analysis) tool detect custom keywords and sensitive data such as financials and so forth that you do not want available for Public consumption. It helps reduce human error and safeguards your content when defining your approval processes. You must have Rev IQ credits available when using this feature.

## Requirements

- You must have a **Rev AI license** and [Rev IQ credits](doc:rev-license-types-and-add-ons#licensed-add-on-components) available to use the Content Analysis Workflows feature(s).
- Content Analysis Workflows is _disabled_ by default and must be enabled. 

## Configuration

To enable Content Analysis Workflows:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Select the **Allow for AI Content Analysis to be included in Workflows** checkbox next to the **Content Analysis Workflows** label. If this checkbox is not visible, **Rev AI Hours** licensing must be purchased and applied first.

3. Click **Save Changes**.

- You can now build a workflow step into your [Approval Processes](doc:ai-content-analysis) that includes sensitive data discovery and custom keyword flagging

## Usage

### Enable AI-Content Analysis for your Approval Step

An **AI-Content Analysis** toggle switch is now visible when you create an [Approval Process](doc:create-an-approval-process). Toggle this switch to the ON position to add **Sensitive Data Discovery** and **Particular Keywords** as part of your [AI-Content Analysis](doc:ai-content-analysis) step.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5a4c1f0-enableContentAnalysis.png",
        "inThisVideoButton.png",
        447
      ],
      "align": "center",
      "caption": "Toggle the AI-Content Analysis switch ON to begin adding it as part of your Approval Process"
    }
  ]
}
[/block]


### Review AI-Content Analysis Alerts on the Review Flyout Panel

You can review any violations or flags on the **Compliance Alert** tab on the **Review flyout panel**. Notice that the tab specifies exactly where in the video the violation occurs with a corresponding icon on the timeline itself.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/724b107-complianceAlertTab.png",
        "videoBasicInfoFlyout.png",
        322
      ],
      "align": "center",
      "caption": "Use the Review icon to access the Compliance Alerts tab for your AI-Content Analysis review"
    }
  ]
}
[/block]