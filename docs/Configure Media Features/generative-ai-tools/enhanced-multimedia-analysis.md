---
title: Enhanced Multimedia Analysis
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
**Enhanced Multimedia Analysis** is an optional feature in **Media Settings** > **Video AI** > **Generative AI Tools** that may be enabled if you have the [Rev IQ credits](doc:rev-license-types-and-add-ons#rev-iq-credits) available. The default option is set to disabled.

<Image align="center" border={false} src="https://files.readme.io/f0ebd6c7d148d2110b6948f397121f0c576b27fbdcfc94e543cff8e02c0ad523-enhancedAnalysisEnabled.png" />

When this option is enabled, the [Video Metadata Generation](doc:video-metadata-generation) and [Vbrick Assistant](doc:vbrick-assistant) Generative AI Tools are enhanced by allowing analysis of images, thumbnails, and supplemental documents associated with the video in addition to its transcript.

## Enhanced Vbrick Assistant

When you use the Vbrick Assistant with **Enhanced Multimedia Analysis** enabled, chapter images, the video thumbnail, and some supplemental files attached to the video are analyzed and included in the context when the assistant answers your questions, in addition to evaluating the video's transcript.

For example, the video below has a Supplemental File (PDF) attached.

<Image align="center" alt="Supplemental Files are also evaluated by the Video Assistant when Enhanced Multimedia Analysis is enabled" border={false} caption="Supplemental Files are also evaluated by the Video Assistant when Enhanced Multimedia Analysis is enabled" src="https://files.readme.io/7f808db4ee71237dc71b77e71acdfb44cbb893a26392bc2ef909b35728bb616f-supplementalFileAttached.png" />

In this case, the attached PDF contains additional references with more information about the subject matter in the video.

<Image align="center" border={false} src="https://files.readme.io/3d691ace43b32d8f6cd463e1f025348ea4e79da394d77214fdd0dd485346e44f-additionalReferencesforAssistant.png" />

The Video Assistant now evaluates this file in addition to the video's transcript when answering questions.

<Image align="center" alt="The Video Assistant uses your Supplemental Documents to answer questions as well (if applicable)" border={false} caption="The Video Assistant uses your Supplemental Documents to answer questions as well (if applicable)" src="https://files.readme.io/fee7ef38d77050bed1b6ebb31866ecc1543c54ac17ea88f7e89f2bb000568654-videoAssistantSupplementalDoc.png" />

## Enhanced Video Metadata Generation

When you use Video Metadata Generation with **Enhanced Multimedia Analysis** enabled, chapter images and video thumbnails attached to the video are considered along with its transcript when generating titles, tags, and descriptions.

<Image align="center" alt="When enhanced, Video Metadata Generation also uses chapter images and thumbnails when generating a video's title, description, and tags" border={false} caption="When enhanced, Video Metadata Generation also uses chapter images and thumbnails when generating a video's title, description, and tags" src="https://files.readme.io/3e4b22984cfa66233e726593204d7b7ad449ad998141effae269463ef545e687-enhancedMetadataGen.png" />

## Limitations

There are limitations to using the **Enhanced Multimedia Analysis** feature.

It is advised that you resize or reformat your images and/or documents first _before_ uploading if they exceed size recommendations or aren't an acceptable file type. This includes chapter images, thumbnail images, images and documents that you upload to Supplemental files.

* Up to 15 images can be analyzed. Each image’s size, height, and width must be no more than 3.75 MB, 8000 px, and 8000 px, respectively, and must be in PNG, JPEG, or GIF format.
* Up to 5 documents can be analyzed. Each document’s size must be no more than 4.5 MB and must be in PDF format.
* Reminder: webp is not a supported type in Rev.
