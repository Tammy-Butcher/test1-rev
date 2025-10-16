---
title: Vbrick Model Context Protocol (MCP) Server
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
<BetaTopic />

**Model Context Protocol** ([MCP](https://modelcontextprotocol.io/docs/getting-started/intro)) is an open protocol that standardizes how applications like Vbrick Rev provide context to **Large Language Model (LLM)** AI systems. **Vbrick MCP Server** allows third-party AI systems like Anthropic’s Claude, OpenAI’s ChatGPT, Microsoft Copilot, etc., to search and access Vbrick video content seamlessly. It allows the AI systems to perform actions related to Vbrick video content.

At this time, Vbrick provides a self-hosted MCP server option that you can clone and host on your local machine.

This topic will cover the following:

* Requirements
* Installing the Vbrick MCP server to work with LLMs (such as Claude AI)
* How to use the Vbrick MCP Server
* Troubleshooting tips

## Requirements

To use the Vbrick MCP server, you will need:

* API key from Vbrick Rev for use with an LLM system
* Linux server or your computer (Linux or Windows). A Linux server is recommended for production use.
* Node.js v22.22.0 or above
* Code from the Vbrick MCP Server repository

## Installation

To create a local self-hosted Vbrick MCP Server, complete the following installation steps:

1. On your Vbrick Rev tenant, [create an API key](doc:create-an-api-key) with the following settings:
   1. The key should be named **vbrick-mcp-server** with a random, unique key. Make note of the unique key.
   2. The **authorized redirect URI** should be: `http://localhost:8008/oauth/callback`.  Some LLM servers like Claude make multiple connections. We recommend adding a second redirect URI,  `http://localhost:8009/oauth/callback`, as a result.
2. On your server/computer, install **NodeJS** from [Node.js - Download Node.js](https://nodejs.org/en/download).
3. Download the [Vbrick MC Server repository](https://github.com/vbrick/vbrick-mcp-server) from GitHub.
4. Extract the **vbrick-mcp-server** content to a folder (e.g., vbrick-mcp-server) on your server or computer.
5. In the vbrick-mcp-server folder, edit the **.env** file and configure the **Vbrick Rev tenant URL** and the **API key** you created in Rev as seen in the code block below.

```node .env
VBRICK_REV_TENANT_URL=https://your-vbrick-tenant.com
OAUTH_CLIENT_ID=your-vbrick-mcp-server-api-key
```

6. Open a command prompt terminal and cd to the directory **vbrick-mcp-server**.
7. Run the following commands:

```node
npm install
npm run build
```

8. Download and install the AI app you will use with your MCP Server.  For this documentation, we will use **Claude desktop** as an example. Download Claude desktop from [Download Claude](https://claude.ai/download).
9. Edit the **claude_desktop_config.json** file using Notepad from the **Settings > Developer > Edit Config** button.

<Image align="center" border={false} src="https://files.readme.io/c0fffb877b044a44ecbda06c8e06cab764dd8df136d496894a3f6004feb85660-editClaudeConfig.png" />

> 📘 Note
>
> If you do not see a Developer option, make sure you are using Claude desktop and not Claude on the web.

10. Edit the config file of Claude (or the AI app you choose to use), similar to the code below:

```json claude_desktop_config.json
{
  "mcpServers": {
    "vbrick-mcp-server": {
      "command": "node",
      "args": [
        "C:\\vbrick-mcp-server\\dist\\index.js"
      ],
      "env": {
        "VBRICK_REV_TENANT_URL": "<<https://your-vbrick-tenant.com>>",
        "OAUTH_CLIENT_ID": "<<your-vbrick-mcp-server-api-key>>"
      }
    }
  }
}
```

> ❗️ Caution!
>
> You will need to reboot Claude after modifying the config file.  Do so by either choosing **File > Exit** or closing it in the **System Tray** to make sure it closes completely.

11. If you use Claude, you can verify that your Vbrick MCP Server has been installed correctly and is running by clicking **Settings > Developer > Advanced** options.

<Image align="center" border={false} src="https://files.readme.io/1c88abe651d6196e4dccd3d509242291de15630e6f6b17414cf08127a127740e-serverInstalled.png" />

12. You are now ready to use the Vbrick MCP Server tools.

<Image align="center" border={false} src="https://files.readme.io/57431389ebe88b40636c9d67c58f29dc6f7c5e1ebe8e3f77651c5ecba74591a8-claudeMCPInstalled.png" />

<br />

> 🚧 Important!
>
> If you re-install or update your Vbrick MCP Server, you always need to run the `npm install` and `npm run build`commands referenced above.  You also need to make sure you **reboot** Claude.

## Vbrick MCP Server Tools Usage

Once you have successfully installed the Vbrick MCP Server to work with Claude or your AI app of choice, you are ready to begin using the tools we have developed to work with the MCP.  They are:

* Who Am I Tool
* Video Search Tool
* Video Details Tool
* Video Transcript Tool

Each of these is discussed in detail in the sections below.

### Who Am I Tool

The Vbrick MCP server has a tool called **Who Am I** that calls Rev API authentication and authorization endpoints to determine the logged-in user each time you use Claude. Every time you use the MCP server with Claude, you are asked to authenticate. The first time, you are also asked to allow permissions.

<Image align="center" border={false} src="https://files.readme.io/94cc7845cd1ac532ca5ef40dee9c385b977f675d7fbbd2b47bd891ba74a57b0e-claudeRevAuthenticate.png" />

Claude automatically spawns the Rev tenant window you configured during installation for you to log-in. Once you have authenticated, you can then close this window.

<Image border={false} src="https://files.readme.io/25e89a229b5285178d7671431843b000482e14d212cd019b6a93daf57334c9c1-image.png" />

Claude will call **Who Am I** again to verify that you are logged in. If not, you can ask it to continue.  The results of your request are then returned, and you can continue using Claude with the configured MCP server.

<Image align="center" border={false} src="https://files.readme.io/b323516dc5ad5af0b8dea4503df0d371c1cdc7149fe930c8fcfc35b0e30ba526-authenticationComplete.png" />

### Video Search Tool

The Vbrick MCP server has a **Video Search Tool** that calls our Video Search API and returns the top 10 results. Results are based on relevance and upload date.

For example, “Search for some videos on language”, might yield:

<Image align="center" border={false} src="https://files.readme.io/acb1a612961a26245a2e4235fc6be2ba2c89cdde4c28432d6376b01b2bf5b090-searchResults.png" />

1. A drop-down that displays the API request and response in detail
2. Video title and length
3. Video description
4. A link to the video to view in Rev

### Video Details Tool

The Vbrick MCP server has a **Video Details Tool** that returns video metadata for a video using the Get Video Metadata/Details API. Also included are the video’s chapters (if applicable) through the Get Video Chapters endpoint.

For example, “Can you give me more details about the video?” might yield:

<Image align="center" border={false} src="https://files.readme.io/ac86053d7cc9166a20f8c93b2e88a1c7d51036407034444537cd6a52ee908f8d-videoDetailsResult.png" />

Included in the result:

* Video details, including title, duration, owner, status, and views.
* Detailed descriptions
* Assigned categories
* Assigned tags
* Access controls and items that have been enabled, such as comments, ratings, and downloads
* Link to the video

### Video Transcript Tool

The Vbrick MCP server has a **Video Transcript Tool** that uses the Get Video Transcription File API to provide context and the video’s transcript.

For example, a request to include a video’s transcript might return:

<Image align="center" border={false} src="https://files.readme.io/ab4d7900e932bddbbbf3d53a0623b8f9d0a8a473b2f735e45ee2bda4779e8f31-getVideoTranscripts.png" />

Included in the result:

* Video title and length
* Uploader
* Views
* Status
* Link to the video
* Transcript summary

## Troubleshooting

* If you see errors from Claude (or the AI app that you are using it with), look in its log file at `c:\users\<your user id>\AppData\Roaming\Claude\logs\mcp-server-vbrick-mcp-server.log`
* If you are having trouble getting your MCP server to run, make sure you have extracted it to the root level of your hard drive.

## Use Case Examples

Using the Vbrick MCP Server with an AI app such as Claude desktop allows you to gather powerful analytics and contextual data from your Rev videos in one place. You can also use that combination to create new datasets and combinations to work for you to create anything you need.

You can ask the AI to create a **detailed spreadsheet** for you based on the videos you want that contains only the data you want to see. In this example, Claude is being asked only for a specific category of videos based on language, with the most popular video in the language series being highlighted.

<Image align="center" alt="Ask to create a spreadsheet and include only the data and specific information you want to view" border={false} caption="Ask to create a spreadsheet and include only the data and specific information you want to view" src="https://files.readme.io/7ee035b39bc04307b67b51dde1790af438edb996f07aff151909f28285f04c96-spreadsheet1.png" />

Once the videos are gathered, the AI is asked to create a spreadsheet of them that can be downloaded and/or published.

<Image align="center" border={false} src="https://files.readme.io/9bf1f5cb56d594a81e60a5b31fefc77ea95cf37ffea54266075ec866c2100e34-spreadsheet2.png" />

What if you want to develop a **language curriculum** based on this data that links back to your videos?  You can do that too. Speaking German was the most popular video in this case, so we can ask the AI to build a beginner German language video course. It once again checks if you are authenticated with Rev before it begins pulling relevant data from specific video(s) needed.

<Image align="center" border={false} src="https://files.readme.io/a4c37638d70791ad05560db18116c6fda801d191341f875fe87bec704edd5d28-germanCourse1.png" />

Once it has concluded, notice that Claude has built an entire German language course based on the Vbrick MCP Server’s search of the video it originally found.  It includes the entire course structure outline for you and several recommendations.

<Image align="center" border={false} src="https://files.readme.io/4c674f8b27ee82e8b1eb72f4e3bfb0c6e18b5885ade5cf46ce20023d70438677-germanCourse2.png" />

What’s more, because you are using the Vbrick MCP Server, it also pulls in more context from your Rev tenant and makes further recommendations of additional Rev videos to add to your language learning.

<Image align="center" border={false} src="https://files.readme.io/7c949706df4f6199ac209e5d00d287a0ad6d75311348b53736b724ab921672c7-germanCourse3.png" />

You are only limited by your imagination once you begin using the Vbrick MCP server.
