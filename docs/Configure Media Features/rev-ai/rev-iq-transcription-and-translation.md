---
title: Rev IQ Transcription and Translation
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
<HTMLBlock>{`
<div class="feature">
  <h3>Who can use this feature?</h3>
 <li>&#9193; <a href="/docs/rev-license-types-and-add-ons">Vbrick Rev</a></li>
  <li>&#128187; <a href="/docs/vbrick-distribution">Vbrick Distribution</a></li>
  <li>&#128736; <a href="/docs/rev-ai">Rev IQ Module</a></li>
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

The **Rev IQ Transcription and Translation** services have several features present for you to use with your VOD uploads and Live Event recordings.  Using these features, you can:

* Choose the transcription actions that you want to occur when you record or upload video to Rev
* Choose an automatic transcription language and audio track
* Choose one or more automatic translation language(s) to transcribe that will use your automatic transcription language as its source for translations
* Generate alternative audio tracks for a VOD file for supported languages
* Allow AI generated voice tracks from your transcription files in supported languages
* Create a custom dictionary to handle Proper nouns in your subtitles

## Requirements

* You must have a **Rev AI license** and [Rev IQ credits available](doc:rev-license-types-and-add-ons#rev-iq-credits) to use transcription and translation feature(s), including **Rev IQ-enabled** [Presentation Profiles](doc:add-a-presentation-profile#rev-iq-enabled-presentation-profiles) that are used to generate live subtitles for encoder-sourced webcasts.
* A [primary language](doc:supported-languages) must be set in Rev account settings before you may use **Automatic** transcription and translation settings.

## Configuration

To enable Rev IQ Transcription and Translation:

1. Navigate to **Admin** > **Media Settings** > **Video AI**.

2. Select the **Rev IQ Transcription and Translation** checkbox in the **AI & Machine Learning** section. If this checkbox is not visible, **Rev AI Hours licensing** must be purchased and applied first.

<Image align="center" src="https://files.readme.io/4cd1f8fbd152260ca0ba875372b81932dfe564de8c551ee9595fb8e3fe030cd4-enableTranscripTranslation.png" />

3. Note that **Automatic Transcription** and **Automatic Translation** options become visible for configuration along with the ability to configure a **Rev IQ custom dictionary**.  Each of these configuration options is described in the sections below.
4. Click **Save Changes**.

> 🚧 Important!
>
> Rev IQ supports transcribing videos up to 4 hours maximum duration length currently.

### Allow AI Generated Voices for Audio Tracks

If you enable **Audio Track Generation**, Rev will generate the voice for you in the [VOD Voice Generation Supported Language](doc:vod-voice-generation-language-support) you choose on the [Languages](doc:manage-audio-tracks-for-a-video) tab of the video.  You must have this enabled by selecting the **Audio Track Generation** checkbox indicated below and have Rev IQ credits.

<Image align="center" src="https://files.readme.io/f0186f560ead73b8f828f97de44816f05503f16caf52520dc2e645b17871002e-enableAudioTrackGeneration.png" />

### Automatic Transcription Settings

**Transcription** is the process of converting *spoken* language into written *text*. This can be done manually, by a human transcriber, or automatically using speech recognition software.

When you enable transcription services, your first step is to decide what *type* of transcription actions occur *automatically* for *new* video uploads as well as the *automatic* transcription language you want to use for those actions.  

For example, you should choose if you want new Live event recordings to be transcribed into text *automatically* (versus all other uploads or both) and what text language they should be transcribed into *automatically* when that occurs, such as English language text.

> 👍 Tip
>
> It is important to note that most of Rev's generative AI features *require* an English transcript before they can be used. For this reason, we *highly* recommend that you select **English** as the automatic transcription language if you plan to use these features.

To enable Automatic Transcription settings:

1. Begin by making sure the **Rev IQ Transcription and Translation** checkbox is enabled.
2. **Automatic Transcription** checkboxes are visible once the service is enabled. This means that *new* video uploads are *automatically* transcribed in the *automatic transcription language* you choose if the following options are subsequently enabled:
   * **New Live Event Recordings** (including video conference based events)
   * **All Other Uploads** (including video conference based imports and uploads)

<Image title="automaticAndDefaultTranscription.png" alt={949} align="center" src="https://files.readme.io/f48a963c5299e998931116c708154ef9075c3445c35432bfbde74a2bfc3938f6-automaticTranscriptionOptions.png">
  When enabled, the selected Automatic Transcription options are transcribed into the Automatic Transcription Language
</Image>

3. Choose your **Automatic Transcription Language**. When *any* **Automatic Transcription** option is enabled, this field is required.

### Automatic Translation Settings

You can also choose automatic translation to occur and select the **automatic languages** to use. This means that your videos will be automatically translated into the languages you set and will be translated from the automatic transcription language you have set.

To enable Automatic Translation Language(s):

1. Make sure that **Rev IQ Transcription and Translation** services are enabled.

2. Configure the [Automatic Transcription](doc:rev-iq-transcription-and-translation#automatic-transcription-settings) settings you want.

> 🚧 Caution
>
> If you do *not* enable **Automatic Transcription** settings, you are still able to translate individual videos as needed but *new* video uploads are *not* translated automatically.

<Image title="defaultTranslationLanguages.png" alt={986} align="center" src="https://files.readme.io/2c1337b84016804746561f15ba1d2ee5cd0dd6647001ce0da0ad1748fbc55f84-automaticTranslationOptions.png">
  Automatically translate your videos into the languages you set in the Automatic Translation Languages box from language set in the Automatic Transcription Language
</Image>

3. Select the **Automatic Translation Language(s)** from the supported languages. These are the additional languages the transcription file is translated and generated into automatically for new uploads *if* **Automatic Transcription** checkboxes are enabled.

### Create a Custom Dictionary

You can create an advanced custom dictionary to make sure that certain terms are recognized when it comes to proper nouns.  This means things like brand names, company names, speakers, and so forth are transcribed correctly.

To create a custom dictionary:

1. Click the **Enabled** checkbox next to **Rev IQ Custom Dictionary**.

2. Choose a **Custom Dictionary Language**.

3. Click the **Add New** button to begin defining your new dictionary entries. 

![](https://files.readme.io/ea2f21f-addCustomDictionary.png "addCustomDictionary.png")

4. For each Dictionary Entry, enter the attributes described in the table below.

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Phrase
      </th>

      <th>
        Sounds Like Pronunciation
      </th>

      <th>
        Sounds Like IPA
      </th>

      <th>
        Display As
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        This field is **required** and may not contain any spaces.  

        If multiple words are used, you may use hyphens.  

        Use periods for acronyms.  For example: <code>F.Y.I.</code>  

        If both a word and an acronym are used, separate them by a hyphen.  

        Avoid using any other special characters or punctuation
      </td>

      <td>
        This is an optional field.  

        Do not use spaces.  

        Use hyphen-separated syllables that mimic how the word sounds.  It is preferable to use common words over phonetic syllables.  

        For example:  For example, for 'Los Angeles', 'loss-ann-gel-es' is preferable to 'lahs-ahn-jul-ees'.  

        You may not use both Sounds Like and IPA.
      </td>

      <td>
        This is an optional field.  

        This field is used for phonetic spellings using only characters in the [International Phonetic Alphabet (IPA)](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet).  

        There must be a single space between between every IPA character (single-byte) or valid IPA character pair (double-byte).  

        You may not use both Sounds Like and IPA.
      </td>

      <td>
        This field describes how you want your Dictionary Entry to appear when transcribed.  

        This field is optional.  

        Spaces may be used in this field.  

        If this field is left empty, the Phrase field is used to determine how it is displayed.
      </td>
    </tr>
  </tbody>
</Table>

<Image title="addDictionaryEntry.png" alt={594} align="center" src="https://files.readme.io/6ab7e51-addDictionaryEntry.png">
  A custom dictionary facilitates transcriptions that are often difficult to understand normally
</Image>

5. Click the **Add** button to add your dictionary term to your custom dictionary.  Each term or phrase you add is displayed in a table below the **Add New** button.  

> 👍 Tip
>
> Currently, only one custom dictionary per portal is supported. There is currently a 50kb limit on entries.

<Image title="dictionaryTable.png" alt={1364} align="center" src="https://files.readme.io/5d8107e-dictionaryTable.png">
  Dictionary updates are Unsaved Changes until you click the Save Changes button on the Integration form.  At that point, status changes to Pending.
</Image>

6. Notice that your dictionary entries display a status of **Unsaved Changes** after you add them.  You must click the **Save Changes** button at the bottom of the Rev IQ integration form to complete your dictionary and save your entries.

7. Once you click the **Save Changes** button, the table status switches to **Pending**.  If you have made any errors when you define your entries, it is then displayed above the table.

<Image title="dictionaryError.png" alt={323} align="center" src="https://files.readme.io/11e68be-dictionaryError.png">
  If you receive an error when you try to save your dictionary, click the Action menu to the right of the entry to edit it
</Image>

8. Click the **Actions** dropdown menu to the right of the entry to edit and correct it before saving the dictionary again.  It will display a status of **Ready**when table entries are correct.

## Usage

When a video is uploaded, you can view languages, audio tracks, and transcription options you have selected on the [Languages](doc:video-languages) tab.

1. Navigate to [Video Settings](doc:update-basic-video-settings) and click the **Details** > [Languages](doc:video-languages) tab option.

2. Use this tab to view the **Automatic Transcription Language** on the top row and to view the translation languages you selected. 

<Image title="revIQTranscription.png" alt={370} align="center" src="https://files.readme.io/e0b75bd-languagesTab.png">
  The Languages tab displays default transcription and translation languages
</Image>

3. Use this tab to [edit, delete, and download video subtitles](doc:video-languages) as needed.
4. You can also choose to generate additional [audio tracks](doc:supported-languages#vod-audio-and-voice-language-support-for-rev-iq) for supported languages (up to ten).
