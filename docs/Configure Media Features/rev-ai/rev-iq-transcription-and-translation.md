---
title: Rev IQ Transcription and Translation
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
[block:html]
{
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>&#128187; <a href=\"/docs/vbrick-distribution\">Vbrick Distribution</a></li>\n  <li>&#128736; <a href=\"/docs/rev-ai\">Rev IQ Module</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


The **Rev IQ Transcription and Translation** services have several features present for you to use with your VOD uploads and Live Event recordings.  Using these features, you can:

- Choose a transcription service to handle automatic transcription actions that you want to occur
- Choose a default transcription language
- Choose one or more default translation language(s) that will use your default transcription language as its source for translations
- Create a custom dictionary to handle Proper nouns in your subtitles

## Requirements

- You must have a **Rev AI license** and [Rev IQ credits available](doc:rev-license-types-and-add-ons#rev-iq-credits) to use transcription and translation feature(s), including **Rev IQ-enabled** [Presentation Profiles](doc:add-a-presentation-profile#rev-iq-enabled-presentation-profiles) that are used to generate live subtitles for encoder-sourced webcasts.
- A [primary language](doc:supported-languages) must be set in Rev account settings before you may use **Automatic** and **Default** settings.
- To use the [VoiceBase integration](doc:voicebase), you must have a [VoiceBase account](https://www.voicebase.com/) created first.  Note that if you have both Rev IQ and VoiceBase enabled, RevIQ is always used first and takes precedence over VoiceBase settings.

### Using Rev IQ Versus VoiceBase

It is important to note that if you have either [Rev IQ Transcription and Translation](doc:rev-iq-transcription-and-translation) services or the [VoiceBase](doc:voicebase) integration option(s) enabled, it allows the ability to auto-generate SubRip (SRT) files directly in Rev rather than only allowing manual uploading of a subtitle file.  

Additionally, **Rev IQ Transcription and Translation** services allow you to translate your file into additional supported languages at the same time and define a [custom dictionary](doc:rev-iq-transcription-and-translation#create-a-custom-dictionary) to assist with company brands and speakers.  

You can have both transcription options enabled, however, only Rev IQ is used if _both_ are enabled and VoiceBase options are not visible.  Further, VoiceBase has some additional restrictions.  The differences are described below.

| Service                                | Feature                 | Included?         |
| :------------------------------------- | :---------------------- | :---------------- |
| **Rev IQ Transcription & Translation** | Automatic Transcription | Yes               |
|                                        | Automatic Translation   | Yes               |
|                                        | Custom Dictionary       | Yes               |
|                                        |                         |                   |
| **VoiceBase**                          | Automatic Transcription | Yes, English Only |
|                                        | Automatic Translation   | No                |
|                                        | Custom Dictionary       | No                |

## Configuration

To enable Rev IQ Transcription and Translation:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Select the **Rev IQ Transcription and Translation** checkbox in the **AI & Machine Learning** section. If this checkbox is not visible, **Rev AI Hours licensing** must be purchased and applied first.

3. Note that **Automatic Transcription **and **Default Transcription ** and **Default Translation** setting options become visible for configuration.  Configure those as desired or needed below. 

4. Click **Save Changes**.

> 🚧 Important!
> 
> Rev IQ supports transcribing videos up to 4 hours maximum duration length currently.

### Automatic and Default Transcription Settings

Transcription is the process of converting spoken language into written text. This can be done manually by a human transcriber, or automatically using speech recognition software.

When you enable transcription services, one of your first steps is to decide what type of transcription actions occur _automatically_ for _new_ video uploads as well as the _default_ transcription service and language you want to use for those actions.  

For this setting, you may use _either_ **Rev IQ** or **VoiceBase **transcription services to transcribe the audio in the video into the selected default language as a subtitle file to be used for it.  At least _one_ must be activated for **Automatic Transcription** options to become visible.  

> 👍 Tip
> 
> It is important to note that most of Rev's generative AI features require an English transcript before they can be used.

To enable Automatic and Default Transcription settings:

1. Begin by selecting at least one transcription service: Choose either the **Rev IQ Transcription and Translation** checkbox or the **VoiceBase Integration** checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5e2b6d4-enableTranscriptionOptions.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


2. **Automatic Transcription** checkboxes become visible once you select a service. This means that _new_ video uploads are _automatically_ transcribed in the _default transcription language_ you choose if the following options are enabled:
   - **New Live Event Recordings** (including video conference based events)
   - **All Other Uploads** (including video conference based imports and uploads)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd5cdda-automaticAndDefaultTranscription.png",
        "automaticAndDefaultTranscription.png",
        949
      ],
      "align": "center",
      "caption": "The selected Automatic Transcription options are transcribed into the default language automatically if enabled"
    }
  ]
}
[/block]


3. Select a **Default Transcription Service** by choosing **Rev IQ** or **VoiceBase Integration**.

> 📘 Note
> 
> The **Default Transcription Service** is automatically selected for you if you only have _one_ transcription service enabled and may not be changed.
> 
> If you have _both_ services enabled, you may select which one is the default service. However, if you plan to configure** Default Translation Language(s)**, you _must_ choose **Rev IQ** here.

4. Choose your **Default Transcription Language**. Only **English **is available for **VoiceBase** at this time. When _any_ **Automatic Transcription** option is enabled, this field is required.

### Default Translation Settings

You can also choose automatic translation to occur and select the **default languages** to use.  You _must _ use **Rev IQ Transcription and Translation** services to use this functionality.  **VoiceBase may not be used.**

To enable Default Translation Language(s):

1. Make sure that **Rev IQ Transcription and Translation** services are enabled.

2. Configure [Automatic and Default Transcription](doc:rev-iq-transcription-and-translation#automatic-and-default-transcription-settings) settings as required.

> 🚧 Caution
> 
> If you do _not_ enable **Automatic Transcription** settings, you are still able to translate individual videos as needed but _new_ video uploads are not translated automatically.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/57cc72d-defaultTranslationLanguages.png",
        "defaultTranslationLanguages.png",
        986
      ],
      "align": "center",
      "caption": "Enable Rev IQ and Automatic Transcription settings to automatically translate your videos into the languages you set in the Default Translation Languages control"
    }
  ]
}
[/block]


3. Select **Default Translation Language(s)** from the supported languages. These are the additional languages the transcription file is translated and generated into automatically for new uploads if **Automatic Transcription** checkboxes are enabled.

### Create a Custom Dictionary

Create an advanced custom dictionary to make sure that certain terms are recognized when it comes to proper nouns.  This means things like brand names, company names, speakers, and so forth are transcribed correctly.

To create a custom dictionary:

1. Click the **Enabled **checkbox next to **Rev IQ Custom Dictionary**.

2. Choose a **Custom Dictionary Language**.

3. Click the **Add New** button to begin defining your new dictionary entries. 

![](https://files.readme.io/ea2f21f-addCustomDictionary.png "addCustomDictionary.png")

4. For each Dictionary Entry, enter the attributes described in the table below.

[block:parameters]
{
  "data": {
    "h-0": "Phrase",
    "h-1": "Sounds Like Pronunciation",
    "h-2": "Sounds Like IPA",
    "h-3": "Display As",
    "0-0": "This field is required and may not contain any spaces.  \n  \nIf multiple words are used, you may use hyphens.  \n  \nUse periods for acronyms.  For example: <code>F.Y.I.</code>  \n  \nIf both a word and an acronym are used, separate them by a hyphen.  \n  \nAvoid using any other special characters or punctuation",
    "0-1": "This is an optional field.  \n  \nDo not use spaces.  \n  \nUse hyphen-separated syllables that mimic how the word sounds.  It is preferable to use common words over phonetic syllables.  \n  \nFor example:  For example, for 'Los Angeles', 'loss-ann-gel-es' is preferable to 'lahs-ahn-jul-ees'.  \n  \nYou may not use both Sounds Like and IPA.",
    "0-2": "This is an optional field.  \n  \nThis field is used for phonetic spellings using only characters in the [International Phonetic Alphabet (IPA)](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet).  \n  \nThere must be a single space between between every IPA character (single-byte) or valid IPA character pair (double-byte).  \n  \nYou may not use both Sounds Like and IPA.",
    "0-3": "This field describes how you want your Dictionary Entry to appear when transcribed.  \n  \nThis field is optional.  \n  \nSpaces may be used in this field.  \n  \nIf this field is left empty, the Phrase field is used to determine how it is displayed."
  },
  "cols": 4,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6ab7e51-addDictionaryEntry.png",
        "addDictionaryEntry.png",
        594
      ],
      "align": "center",
      "caption": "A custom dictionary facilitates transcriptions that are often difficult to understand normally"
    }
  ]
}
[/block]


5. Click the **Add** button to add your dictionary term to your custom dictionary.  Each term or phrase you add is displayed in a table below the **Add New** button.  

> 👍 Tip
> 
> Currently, only one custom dictionary per portal is supported. There is currently a 50kb limit on entries.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5d8107e-dictionaryTable.png",
        "dictionaryTable.png",
        1364
      ],
      "align": "center",
      "caption": "Dictionary updates are Unsaved Changes until you click the Save Changes button on the Integration form.  At that point, status changes to Pending."
    }
  ]
}
[/block]


6. Notice that your dictionary entries display a status of **Unsaved Changes** after you add them.  You must click the **Save Changes** button at the bottom of the Rev IQ integration form to complete your dictionary and save your entries.

7. Once you click the **Save Changes** button, the table status switches to **Pending**.  If you have made any errors when you define your entries, it is then displayed above the table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/11e68be-dictionaryError.png",
        "dictionaryError.png",
        323
      ],
      "align": "center",
      "caption": "If you receive an error when you try to save your dictionary, click the Action menu to the right of the entry to edit it"
    }
  ]
}
[/block]


8. Click the **Actions** dropdown menu to the right of the entry to edit and correct it before saving the dictionary again.  It will display a status of **Ready**when table entries are correct.

## Usage

When a video is uploaded, you can view languages and transcription options you have selected on the [Languages](doc:video-languages) tab.

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > [Languages](doc:video-languages) tab option.

2. Use this tab to view the **Default Transcription Language** on the top row and to view the translation languages you selected. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e0b75bd-languagesTab.png",
        "revIQTranscription.png",
        370
      ],
      "align": "center",
      "caption": "The Languages tab displays default transcription and translation languages"
    }
  ]
}
[/block]


3. Use this tab to [edit, delete, and dowload video subtitles](doc:video-languages) as needed.