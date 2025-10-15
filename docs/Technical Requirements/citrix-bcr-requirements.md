---
title: Citrix BCR Requirements
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
**Citrix Browser Content Redirection (BCR) 2.0** is a new feature introduced in Citrix XenApp/XenDesktop v7.16. It allows seamless redirection of the entire browser content area (a.k.a. viewport) to the Citrix client (known as the receiver) for selected webpages or domains. Previous versions of Citrix allowed only the video element of the page redirected to the client.

The **viewport **displays the content outlined in the rectangular area of your browser seen in the image below. It does \_not \_include things like the address bar, Favorites toolbar, or the status bar.

BCR 2.0 provides Vbrick complete control of Rev’s content display using HTML5 technology including the HTML5 video player. It allows Vbrick to serve multi-bit rate HLS video directly on the receiver or thin client.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae8b55b-citrixViewPort.png",
        "citrixViewPort.png",
        768
      ],
      "align": "center",
      "caption": "The viewport does not include the browser address bar, Favorites toolbar, or the status bar"
    }
  ]
}
[/block]

## Vbrick Multicast

**Browser Content Redirection** is also supported for **Vbrick Multicast** and provides support for multicast using the HTML5 player. This requires the Vbrick Multicast agent to be installed on the Citrix receiver or thin client.

## Vbrick Rev Zoning

With **Browser Content Redirection** enabled, Rev receives the IP of the receiver and applies the **Zone **using the IP of the receiver. If the **User Location IP Service (ULS)** is enabled, Rev uses the DME ULS URL to get the client IP of the receiver and uses the IP returned by DME ULS for zoning.

## Software Requirements

### Citrix BCR

[block:parameters]
{
  "data": {
    "h-0": "Citrix Version",
    "h-1": "Rev Version",
    "h-2": "Citrix VDA/VDI OS Version",
    "h-3": "Citrix Receiver (Thin client) OS Version",
    "h-4": "Browser",
    "h-5": "Stream Playback Type",
    "0-0": "Citrix XenApp/XenDesktop 7.15 LTSR CU3  \n  \nCitrix XenApp/XenDesktop 7.16+  \n  \n**More Info:**  \n[Citrix Blogs - Maximize Multimedia w/BCR 2.0](https://www.citrix.com/blogs/2018/12/12/browser-content-redirection-2-0-will-help-you-maximize-your-multimedia/)",
    "0-1": "Rev 7.25+",
    "0-2": "Windows 10",
    "0-3": "Windows 10  \nWindows 8  \nDell ThinOS",
    "0-4": "Chrome",
    "0-5": "HTML5 HLS-based multicast and unicast  \n  \nMulticast requires Vbrick Multicast (VBM) agent installation on the Citrix receiver"
  },
  "cols": 6,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]

## Configuration

1. Install the **Browser Content Redirection Chrome Extension** on the **VDA **for each user that will login to the receiver. This can be pushed as a policy by the Citrix Admin.
   - Find it here: <https://chrome.google.com/webstore/detail/browser-content-redirecti/hdppkjifljbdpckfajcmlblbchhledln?utm_source=chrome-ntp-icon>

2. You (or your Citrix Admin) should also configure a studio policy on the controller by selecting the **Policies **menu option then the **Settings **tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1eb6a96-configureStudioPolicy.png",
        "configureStudioPolicy.png",
        272
      ],
      "align": "center",
      "sizing": "smart",
      "caption": "Select the Policies option then the Settings tab to configure a Studio policy"
    }
  ]
}
[/block]

3. This includes allow listing the **Rev URL **under **Browser Content Redirection ACL Configuration**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/68112c9-allowListRevUrl.png",
        "allowListRevUrl.png",
        902
      ],
      "align": "center",
      "caption": "Add the Rev URL to your Allow List as part of the Policy"
    }
  ]
}
[/block]

4. If you are using **SAML SSO in Rev** then under **Browser Content Redirection Authentication Sites** the **SAML Identity Provider (IDP) URL** is allow listed (example below).
   - Refer to <https://support.citrix.com/article/CTX238236> for additional details if needed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea3aeed-bcrAuthenticationSiteforSamlSso.png",
        "bcrAuthenticationSiteforSamlSso.png",
        902
      ],
      "align": "center",
      "caption": "Allow list the SAML IDP URL if using SAML SSO in Rev"
    }
  ]
}
[/block]

> 👍 Tip
> 
> There is no need to allow list DME or CDN URLs because any URL that Rev accesses on a Rev page is automatically redirected to the Citrix client.

<h3>How the Citrix Receiver Fetches Content</h3>

Understanding how the **Citrix Receiver** fetches content is an important configuration consideration.

**Client Fetch – Client Rendering**: Receiver contacts Rev directly, therefore it requires Internet access. This offloads all network usage, CPU, GPU and RAM from VDA to Receiver. All the heavy lifting is done by the Receiver. **This configuration is tested and recommended by Vbrick for Rev.**

**Server Fetch – Client Render**: Receiver contacts and fetches content from Rev through the VDA using a virtual channel. This is useful when the client does not have Internet access. Low CPU, GPU and RAM consumption are expected on the VDA but bandwidth is consumed on the ICA virtual channel.

**Server Side Rendering (SSR)**: No redirection happening, either because the Rev URL is not allow listed, or the redirection failed and Citrix fallbacks to rendering the webpage on the VDA.

> ❗️ Warning!
> 
> Note that when **Browser Content Redirection** is configured, the server fetch is prohibited by default.

## Verify BCR Configuration

To verify that you have successfully configured BCR 2.0, right-click on the webpage to display an **About HDX Browser Redirection** pop-up menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8f5095a-aboutHDXBcrMenu.png",
        "aboutHDXBcrMenu.png",
        760
      ],
      "align": "center",
      "caption": "The About HDX Browser Redirection menu displays when BCR is configured correctly"
    }
  ]
}
[/block]

You can also verify it by confirming three processes on the receiver called **HDX Overlay Browser** on Windows 10 or called **HdxBrowserCef.exe** on Windows 7.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8811d06-BCRTaskManager.png",
        "BCRTaskManager.png",
        505
      ],
      "align": "center",
      "caption": "Confirm BCR configuration through processes in the Task Manager"
    }
  ]
}
[/block]