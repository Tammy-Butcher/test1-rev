---
title: Search and Filter Functions
excerpt: Best practices to find content in Rev
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
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>&#9193; <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


## AI-Powered Smart Search

Rev uses an **AI-powered smart search** by default.  What does this mean?  In the past, simple keyword queries and matches were used to drive the most relevant search results.  This is still largely prevalent today. However, with emerging AI technologies, queries can now begin to consider _intent_ and _context_.  

Consider the example below.  If you enter the keyword search "Spanish", the video "Spanish Language" is returned as expected since the keyword is in the metadata (title) and enrichment data (transcripts).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d1d6a58-keywordSearch.png",
        "",
        "A simple keyword search returns a video with the keyword in the metadata (title) and enrichment data as expected"
      ],
      "align": "center",
      "caption": "A simple keyword search returns a video with the keyword in the metadata (title) and enrichment data as expected"
    }
  ]
}
[/block]


AI-powered search engines understand "conversational" language and intent.  This means that instead of a simple keyword search you might enter more of an actual phrase such as "How can I learn Spanish?". Notice that this query also returns the top metadata keyword and enrichment results but also understands your _intent_ and returns a suggestion on watching a popular sitcom with a Spanish translation as its second recommendation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9c36049-aiSearch.png",
        "",
        "AI-powered searches use conversational language to recognize the intent behind your query"
      ],
      "align": "center",
      "caption": "AI-powered searches use conversational language to recognize the intent behind your query"
    }
  ]
}
[/block]


In addition to understanding natural language, AI search results are personalized and tailored exactly to you and your viewing history.  AI search engines learn your search behavior which means your results become even more relevant over time.  The goal is that Rev's AI search, paired with keywords, will provide you with more personalized and helpful results.

## Keyword Search

The keyword search index in Rev ranks content based on the following factors:

- Video metadata, such as title, description, category, tags and custom fields
- Enrichment data from transcription, uploaded SRT files, and user’s tagged in a video
- Popularity based on all video views in the last 7 days
- Freshness (recency) based on the video’s upload date 

> 📘 Note
> 
> Search text is _not_ case‑sensitive and you can enter any combination of words and numbers (special characters, however, are not permitted). 
> 
> You are not limited by Video queries. Try categories, video owner, subtitles, and so forth to find the content you need. To further narrow results, combine your search results with filters.
> 
> Use the **Back** button on your browser to keep your previously set search filters.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/56f7dba-gridViewResults.png",
        "gridViewResults.png",
        1856
      ],
      "align": "center",
      "caption": "Search results sorted by relevance.  Hover over a video in tile view to preview it."
    }
  ]
}
[/block]


By default, results appear in **List** view.  Switch to **Grid** view to use the **Sort **dropdown to view results by the following attributes:

- Relevance
- Uploaded Date
- Title
- Views 

You can also preview videos in **Grid** view by hovering over them with your mouse.

When viewing search results in **List **view, sort all columns by ascending or descending view by your preference.

Note that when viewing results in **List **view that, if your query is included in subtitles attached to a video, it will be highlighted in search results as seen in the image below as well as your title.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/93e4bae-searchResultsListViewSubtitles.png",
        "searchResultsListViewSubtitles.png",
        1832
      ],
      "align": "center",
      "caption": "Search results in List view with subtitle results included"
    }
  ]
}
[/block]


> 👍 Tip
> 
> Hover over a video in tile view to preview it.  Right-clicking on a video allows you to open it in a new tab or window.

## Transcript Speech Search Results

Most often, video titles are what are entered in the **Search Media** field and, as a result, search results are weighted toward those title searches. However, keep in mind, you may also search the _transcript speech_ of all videos so that you can find specific videos that include those phrases in the audio transcript of the video (and who is speaking) and not just use the video metadata for your video searches.

> 📘 Note
> 
> [Subtitles](doc:update-advanced-video-settings#subtitles-translations-and-closed-captions) must be added to a video _before_ a speech search may be performed on it.

Keyword matches within a video’s subtitles are included in search results. Subtitle matches will include the time and text with the matching search string highlighted.

Further, if a video contains more than one audio search result, they are contained in a list sorted by start time. This is displayed in the image below (**List **view).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7480a92-searchResultsSubtitlesTimestamps.png",
        "searchResultsSubtitlesTimestamps.png",
        1835
      ],
      "align": "center",
      "caption": "Search results with highlighted speech search and timestamps included along with the speaker"
    }
  ]
}
[/block]


Keep in mind:

- Each audio result is an active link to the video player page. The video will start playing from the start time link that is clicked.
- Rev will only search subtitles for the user’s language. For example, if the user’s Rev interface is in English, search results will only include matches associated to English subtitles.
- As noted, the video must have a subtitle file associated with it before it will be included in an audio search.
- You may also search individual video files for specific metadata content by using the [Video Pulse flyout](doc:rev-video-player-features#video-pulse) panel on the video player.

## Filter Search Results

User the **Filter** icon in the right sidebar to apply various filters to narrow your search results if needed.  The image below details what filters can be applied. Use the **Clear All** button to reset your applied filters and start over.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98da013-filters.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]