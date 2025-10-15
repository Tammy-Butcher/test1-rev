---
title: Use Vbrick Universal eCDN with Microsoft Teams
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
  "html": "<div class=\"feature\">\n  <h3>Who can use this feature?</h3>\n <li>⏩ <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Rev</a></li>\n  <li>💻 <a href=\"/docs/rev-license-types-and-add-ons\">Vbrick Universal eCDN</a></li>\n</div>\n\n<style>\n  \n .feature {\nlist-style-type: none;\n   text-indent:10px;\n   width: 60%;\n   margin: 10px 10px;\n   padding-top: 5px;\n   padding-bottom: 15px;\n   padding-left:10px;\ndisplay: block;\n   background-color:#F6F3F3;\n   border-radius: 10px;\n   box-shadow: rgba(0, 0, 0, 0.14) 0px 1px 5px 0px;\n   \n}\n  \n</style>"
}
[/block]


There are two sets of configurations that need to be accomplished to enable Microsoft Teams to utilize the Vbrick eCDN.  

- First, it must be configured within **Vbrick**.  
- Second, it must be configured within **Microsoft Teams**.  As always, the third step is testing.

Both configurations must be set for the feature to work across the systems.

***

## Vbrick Configuration

Microsoft Teams supports 3rd-party eCDN distribution with **MS Teams Townhall Premium** which means you can configure [Vbrick Universal eCDN](doc:what-is-the-vbrick-universal-ecdn) for distribution.

### Requirements

- Rev Cloud or Vbrick Universal eCDN Account
- Microsoft Teams Admin access (for configuration only)

### Configuration

Microsoft supports 3rd-party eCDN distribution which means you can use Vbrick Rev and Vbrick Universal eCDN for distribution in Teams. The **Use the Vbrick Universal eCDN with Teams integration** section defines a Microsoft Teams JSON that is used within Microsoft Teams as a configuration. Complete the following steps to configure this integration:

1. Navigate to **Media Settings > Integrations** and scroll down to the **Microsoft** - **Use Vbrick Universal eCDN with Teams** section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1c7a78-msTeamsECDN.png",
        "",
        "Enable the Vbrick Universal eCDN with Teams integration to use Rev or Vbrick Universal eCDN for distribution"
      ],
      "align": "center",
      "caption": "Enable the Vbrick Universal eCDN with Teams integration to use Rev and Vbrick Universal eCDN for distribution"
    }
  ]
}
[/block]


2. In the Select **JWT Certificate** dropdown, select the certificate you want to use. Make sure you either create a new certificate or select an already generated certificate.
3. By default, a Certificate named **RevConnectDefault** should have already been created. You can use that certificate or provide your own.
4. Copy the **Microsoft Teams JSON** and provide it to your IT staff that controls and configures your Microsoft Teams environment. This JSON provides the location and authentication for Microsoft Teams to utilize the **Vbrick Universal eCDN** distribution.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06db85f-teamsIntegration.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


5. Note that the **apiKey** and **apiSecret** within the **Microsoft Teams JSON** use the **UNIVERSAL_ECDN API** key defined within the Vbrick Management Interface.
   1. This **UNIVERSAL_ECDN** key _must_ exist and remain in place.
   2. If the API key is changed (at a later time), the JSON will need to be regenerated and reapplied into Microsoft Teams.
   3. If the apiKey and apiSecret fields are **blank** within the JSON, that is an indication that the API Key **UNIVERSAL_ECDN** does not exist. Please recreate the API key.

You are now ready to use the [Vbrick Universal eCDN](doc:what-is-the-vbrick-universal-ecdn) for distribution with Microsoft Teams.  Next step is to tie this eCDN into Microsoft Teams (see below).

***

## Microsoft Teams Configuration

Before you begin, you will need the Vbrick generated JSON (from the help above), and you will also need to coordinate your efforts with your IT Team (who have access to Microsoft policy settings and Teams configuration).   Additionally, please review and understand all the following steps before starting.

Microsoft Teams supports both a command-line and and the normal Teams Admin user interface for setting Live Event delivery options. These settings allow the Microsoft Teams tenant administrator to select the eCDN provider and specify configuration parameters to customize the the eCDN operation for the given provider.

### PowerShell Cmdlet

To enable the **Vbrick Universal eCDN** option for Teams delivery, we provide **PowerShell** commands.  These PowerShell commands are run as an authenticated Microsoft Teams administrator session connected to the Teams Admin interface. 

For information on establishing an authenticated administrator PowerShell session for Teams, see Microsoft documentation.  (These are provided only as starting points)

- [Install Microsoft Teams PowerShell - Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/teams-powershell-install)
- [Configure live event settings in Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/teams-live-events/set-teams-live-events-policies-using-powershell)
- [Install Microsoft Teams PowerShell - Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/teams-live-events/configure-teams-live-events)

For all the following command steps, log in as an authenticated Teams administrator and open PowerShell as an administrator; authenticate, and then connect to Teams administration.

#### Install-Module MicrosoftTeams

First, using PowerShell, install the Microsoft Teams module with the following command:

```Text Install Microsoft Teams module
Install-Module MicrosoftTeams
```

The response should be similar to:

```Text Possible Response
Untrusted repository
You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet. Are you sure you want to
install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Type **Y** or **A** to install it.

If you have already installed it, you will get a warning.  If you want to update it, please use:

```Text Update existing MicrosoftTeams module
Update-Module MicrosoftTeams
```

#### Connect-Microsoft Teams | Format-Table -wrap

Next, connect to the Microsoft Teams module with:

```Text Connect to MicrosoftTeams module
Connect-MicrosoftTeams
```

This opens a browser tab that allows you to authenticate.  

To verify your Account settings, use:

```Text Verify Account Settings
Connect-MicrosoftTeams | Format-Table -wrap
```

#### Configure the eCDN within Microsoft Teams

First, you will need to **Set the eCDN policy.**  There are several steps to this.

1. Create the necessary JSON to populate into Microsoft Teams to use Vbrick Universal eCDN.  The JSON includes some options and a **rev** section.    

- The **verbose** option will populate the players control panel with information helpful to forensics.  
- The **overlay** option, if true, will add a video title to your top of your player which is useful in testing.

The **rev** section includes the JSON provided by the Rev / Vbrick Universal eCDN interface.  Here is an example of that JSON:

```Text JSON from Rev / Vbrick Universal eCDN
{
  "hostName": "acme.rev.vbrick.com",
  "jwtKeyName": "RevConnectDefault",
  "apiKey": "gKPEYHHD",
  "apiSecret": "Jqq55TF6bI6wvlWJkTFW2Hr6wKJrzjEUpVDgo+8+oguOh0Pjy4IycqJIzY+UFwgaZvnwsYRXIMorKMjdRPpOtbmgoV3YRSoPByC5xPGLWwFZ/2EDdpcRVqJ0jcYmvIarWenxotdoPaz1d+WrXRC6cFK4iFk4PMDBlRu0uAeI="
}
```

Here is an example of the complete JSON that is composed of both options and **rev** section.   Edited together you would get:

```Text Edited JSON for Microsoft
{
    "verbose": true,
    "overlay": false,
    "params": {
        "rev": {
                  "hostName": "acme.rev.vbrick.com",
                  "jwtKeyName": "RevConnectDefault",
                  "apiKey": "gKPEYHHD",
                  "apiSecret": "Jqq55TF6bI6wvlWJkTFW2Hr6wKJrzjEUpVDgo+8+oguOh0Pjy4IycqJIzY+UFwgaZvnwsYRXIMorKMjdRPpOtbmgoV3YRSoPByC5xPGLWwFZ/2EDdpcRVqJ0jcYmvIarWenxotdoPaz1d+WrXRC6cFK4iFk4PMDBlRu0uAeI="
               }
    }
}
```

That JSON is what must be set within Microsoft in order for Teams to utilize Vbrick distribution.  It would be included in the following `Set-CsTeamsMeetingBroadcastConfiguration` command:

```Text Set eCDN Policy
Get-CsTeamsMeetingBroadcastPolicy -identity Global
Set-CsTeamsMeetingBroadcastConfiguration -AllowSdnProviderForBroadcastMeeting $True -SdnProviderName ramp -SdnRuntimeConfiguration '{"verbose":true,"overlay":false,"params":{"rev":{"hostName":"acme.rev.vbrick.com","jwtKeyName":"RevConnectDefault","apiKey":"gKPEYHHD","apiSecret":"Jqq55TF6bI6wvlWJkTFW2Hr6wKJrzjEUpVDgo+8+oguOh0Pjy4IycqJIzY+UFwgaZvnwsYRXIMorKMjdRPpOtbmgoV3YRSoPByC5xPGLWwFZ/2EDdpcRVqJ0jcYmvIarWenxotdoPaz1d+WrXRC6cFK4iFk4PMDBlRu0uAeI="}}}'
```

> 📘 Note
> 
> You can utilize a Vbrick tool at <https://livetools.rampecdn.com/portal/dev/psescape.html> to check the format of your JSON and generate the `Set-CsTeamsMeetingBroadcastConfiguration` command above.

2. Next **Verify the eCDN **setting with:

```Text Verify the eCDN
Get-CsTeamsMeetingBroadcastConfiguration -ExposeSDNConfigurationJsonBlob
```

or

```Text Verify the eCDN
Get-CsTeamsMeetingBroadcastConfiguration -ExposeSDNConfigurationJsonBlob | Format-Table SdnRuntimeConfiguration -wrap
```

Lastly, if you ever need to Disable Vbrick eCDN within Microsoft Teams, use:

```
Set-CsTeamsMeetingBroadcastConfiguration -AllowSdnProviderForBroadcastMeeting $False
```

> 📘 Note
> 
> While on average the change takes effect within 60 minutes, it may also take up to 24 hours to propagate.

At this point, you can begin testing Microsoft Teams with Vbrick distribution.

### Recommendation: Alternative approach to Configuration (configUrl parameter)

When initially testing and setting up your environment, it is often better to set up a redirect  to a configuration URL.  In that way, you can then change the configuration at will, thus changing the Microsoft Teams settings without the necessity to revisit Microsoft to reapply and wait for any changes you make.  You would utilize this approach for testing, and once you have perfected your configuration you would use the JSON (from above) with Microsoft to communicate the settings directly.

Follow the steps outlined below to utilize this alternative approach for a config URL file is accomplished

- Generate the JSON on Vbrick Universal eCDN as you normally would and copy it to a file
- Host the file that contains the generated JSON.
  - Note: You determine the name of the file but it should be meaningful.  
    - Format: https\://hostFQDN/path/file 
  - Make sure the host machine is reachable by your testing machines
- When providing Microsoft the JSON (via the commands above), use the following JSON:

```
{"configUrl":"https\://hostFQDN/path/file"}   
   
```

> 🚧 Important!
> 
> Microsoft offers Teams licensing options (Teams Premium, for example) that automatically enable a Microsoft eCDN.  If your Teams license includes a Microsoft eCDN, you will have an option to enable/disable it in the Teams admin center Events Settings or via PowerShell and you must disable it to use the Vbrick Universal eCDN.  
> 
> Accessing that option in the Teams admin web interface varies depending on if you are using the unified settings experience Microsoft is rolling out in 2024-2025.  
> 
> More details on this are available at the following links: 
> 
> - [Enterprise Content Delivery and the Microsoft eCDN](https://learn.microsoft.com/en-us/microsoftteams/streaming-ecdn-enterprise-content-delivery-network#microsoft-ecdn)
> - [Unified Policy Settings Admin Center](https://learn.microsoft.com/en-us/microsoftteams/unified-policies-settings-management-teams-admin-center)