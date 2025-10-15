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

The **viewport** displays the content outlined in the rectangular area of your browser seen in the image below. It does \_not \_include things like the address bar, Favorites toolbar, or the status bar.

BCR 2.0 provides Vbrick complete control of Rev’s content display using HTML5 technology including the HTML5 video player. It allows Vbrick to serve multi-bit rate HLS video directly on the receiver or thin client.

<Image title="citrixViewPort.png" alt={768} align="center" src="https://files.readme.io/ae8b55b-citrixViewPort.png">
  The viewport does not include the browser address bar, Favorites toolbar, or the status bar
</Image>

## Vbrick Multicast

**Browser Content Redirection** is also supported for **Vbrick Multicast** and provides support for multicast using the HTML5 player. This requires the Vbrick Multicast agent to be installed on the Citrix receiver or thin client.

## Vbrick Rev Zoning

With **Browser Content Redirection** enabled, Rev receives the IP of the receiver and applies the **Zone** using the IP of the receiver. If the **User Location IP Service (ULS)** is enabled, Rev uses the DME ULS URL to get the client IP of the receiver and uses the IP returned by DME ULS for zoning.

## Software Requirements

### Citrix BCR

<Table align={["left","left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Citrix Version
      </th>

      <th>
        Rev Version
      </th>

      <th>
        Citrix VDA/VDI OS Version
      </th>

      <th>
        Citrix Receiver (Thin client) OS Version
      </th>

      <th>
        Browser
      </th>

      <th>
        Stream Playback Type
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Citrix XenApp/XenDesktop 7.15 LTSR CU3  

        Citrix XenApp/XenDesktop 7.16+  

        **More Info:**
        [Citrix Blogs - Maximize Multimedia w/BCR 2.0](https://www.citrix.com/blogs/2018/12/12/browser-content-redirection-2-0-will-help-you-maximize-your-multimedia/)
      </td>

      <td>
        Rev 7.25+
      </td>

      <td>
        Windows 10
      </td>

      <td>
        Windows 10\
        Windows 8\
        Dell ThinOS
      </td>

      <td>
        Chrome
      </td>

      <td>
        HTML5 HLS-based multicast and unicast  

        Multicast requires Vbrick Multicast (VBM) agent installation on the Citrix receiver
      </td>
    </tr>
  </tbody>
</Table>

## Configuration

1. Install the **Browser Content Redirection Chrome Extension** on the **VDA** for each user that will login to the receiver. This can be pushed as a policy by the Citrix Admin.
   * Find it here: [https://chrome.google.com/webstore/detail/browser-content-redirecti/hdppkjifljbdpckfajcmlblbchhledln?utm\_source=chrome-ntp-icon](https://chrome.google.com/webstore/detail/browser-content-redirecti/hdppkjifljbdpckfajcmlblbchhledln?utm_source=chrome-ntp-icon)

2. You (or your Citrix Admin) should also configure a studio policy on the controller by selecting the **Policies** menu option then the **Settings** tab.

<Image title="configureStudioPolicy.png" alt={272} align="center" width="smart" src="https://files.readme.io/1eb6a96-configureStudioPolicy.png">
  Select the Policies option then the Settings tab to configure a Studio policy
</Image>

3. This includes allow listing the **Rev URL** under **Browser Content Redirection ACL Configuration**.

<Image title="allowListRevUrl.png" alt={902} align="center" src="https://files.readme.io/68112c9-allowListRevUrl.png">
  Add the Rev URL to your Allow List as part of the Policy
</Image>

4. If you are using **SAML SSO in Rev** then under **Browser Content Redirection Authentication Sites** the **SAML Identity Provider (IDP) URL** is allow listed (example below).
   * Refer to [https://support.citrix.com/article/CTX238236](https://support.citrix.com/article/CTX238236) for additional details if needed.

<Image title="bcrAuthenticationSiteforSamlSso.png" alt={902} align="center" src="https://files.readme.io/ea3aeed-bcrAuthenticationSiteforSamlSso.png">
  Allow list the SAML IDP URL if using SAML SSO in Rev
</Image>

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

<Image title="aboutHDXBcrMenu.png" alt={760} align="center" src="https://files.readme.io/8f5095a-aboutHDXBcrMenu.png">
  The About HDX Browser Redirection menu displays when BCR is configured correctly
</Image>

You can also verify it by confirming three processes on the receiver called **HDX Overlay Browser** on Windows 10 or called **HdxBrowserCef.exe** on Windows 7.

<Image title="BCRTaskManager.png" alt={505} align="center" src="https://files.readme.io/8811d06-BCRTaskManager.png">
  Confirm BCR configuration through processes in the Task Manager
</Image>
