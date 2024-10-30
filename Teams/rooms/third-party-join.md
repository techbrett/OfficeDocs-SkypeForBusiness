---
title: Third-party meetings on Teams Rooms
author: mstonysmith
ms.author: tonysmit
manager: pamgreen
ms.reviewer: naforer
ms.date: 08/22/2024
ms.topic: article
audience: Admin
ms.service: msteams
ms.subservice: itpro-rooms
appliesto: 
  - Microsoft Teams
ms.collection: 
  - M365-collaboration
  - teams-rooms-devices
  - Tier1
f1.keywords: 
  - NOCSH
ms.localizationpriority: medium
description: This article discusses how to configure your organization and Teams Rooms devices to support third-party meeting joining to Cisco Webex and Zoom.
---

# Third-party meetings on Teams Rooms

Microsoft Teams Rooms devices support a one-touch and join by ID experiences for connecting to third-party online meetings. This capability comes in two forms: Direct Guest Join (DGJ) or Cross-Platform meetings via SIP (Session Initiation Protocol) join. When 3rd party join is enabled, you can use Teams Rooms to join meetings hosted on other meeting platforms just as easily as you can join meetings hosted on Microsoft Teams. Keep in mind that when using these features, the experience is largely driven by the third-party online meeting provider with the Teams Room device simply connecting to that platform.
Supported devices and services:

Before you can join third-party meetings from Teams Rooms, you need to do the following:
1.	Understand which third-party meeting join solution is right for your organization.
2.	Configure the Teams Rooms' resource accounts Exchange mailbox to process invites for 3rd party and externally scheduled meetings. 
3.	Ensure no tenant policies are blocking devices from connecting to third-party meeting services.
4.	Configure Teams Rooms devices to allow third-party meetings.

## Step 1: Which Third-Party Meeting Join solution is right for your Teams Rooms?

Teams Rooms offer two ways for connecting to third-party meetings: a SIP video based solution known as cross-platform meeting via SIP join and a WebRTC based solution known as Direct Guest Join. These solutions have different requirements and capabilities which are noted in the table, please review and determine which is right for your organization.

| Supported Functionality | Cross-Platform via SIP | Direct Guest Join
|--------|----------|---------|---------|
| Join Button &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Amazon Chime &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; <br>Cisco Webex <br>Google Meet <br>GoToMeeting <br>RingCentral <br>Zoom <br>Other SIP services | Cisco Webex &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; <br>Zoom |
| Join by ID | Amazon Chime <br>Cisco Webex <br>Google Meet <br>GoToMeeting <br>RingCentral <br>Zoom <br>Other SIP via URL | Zoom |
| Events & Webinars | Cisco Webex <br>Zoom | Not available |
| Receive video quality | Up to 1080p / 30 fps | Up to 720p / 30fps |
| Send video quality | Up to 1080p / 30 fps | Up to 720p / 30fps |
| Receive content | Available | Available |
| Send content | Available | Not available |
| Maximum supported number of Front of Room Displays | 2 displays | 1 display |
| Layout controls | Available* | Available* |
| List participant | Available* | Available* |
| View chat | Available* | Available* |
| Breakout rooms | Available* | Available* |
| View reactions | Available* | Available* |
| Send reactions | Not available | Not available |
| View content annotations | Not available | Not available |
| View transcript | Not available | Not available |
| Recording notification | Available | Available |
| Whiteboard consume | Available* | Available* |
| Whiteboard interact | Not available | Not available |
| Lobby control | Available* | Not available |
| Lobby authentication / bypass | Not available | Not available |
| Teams Rooms coordinated join | Not available | Not available |
| Microphone mute sync | Not available | Not available |
| SIP calling plan required | Yes | No |
| Direct internet access required | No | Yes |
| Teams Rooms license | Teams Rooms Pro | Teams Rooms Basic <br>Teams Rooms Pro |
| Teams Rooms platform availbability | Teams Rooms on Windows | Teams Rooms on Windows <br>Teams Rooms on Android |

> [!NOTE]
> *These features vary by 3rd party meeting platform.
> Third party platform features mentioned above were available at the time this article was last updated and may vary from platform to platform. Microsoft periodically reviews these features to keep this document current but other platforms may make changes which can impact these features.

> [!NOTE]
> To join a Cisco Webex meeting from a Teams Rooms device using Direct Guest Join, the Cisco meeting needs to be hosted in Webex Meetings Pro using Cisco Webex web application version WBS 40.7 or later.

## Step 2: Allow Exchange to process third-party meetings and externally created invites

When a Teams Room joins a Teams Meeting it utilizes hidden properties in the Outlook meeting invite to know the meeting link to join. But when joining third-party meetings, Teams Rooms read the calendar invite message body so you need to retain the meeting invite body to ensure a “join” button can be generated for third-party meeting platforms. Similarly, a typical use case for third-party meeting join is for meetings created outside of your organization, in which case, you want users to be able to forward the externally scheduled meeting invite to their preferred meeting space and have the room accept the invite. 

To enable these scenarios, you need to modify the Exchange calendar processing rules on the room resource account. To set these room mailbox options using the [Set-CalendarProcessing](/powershell/module/exchange/set-calendarprocessing) cmdlet, do the following:

1. Connect to Exchange Online PowerShell. For more information, [Connect to Exchange Online PowerShell](/powershell/exchange/mfa-connect-to-exchange-online-powershell).

2. Using the resource account mailbox's UPN, run the following command. Replace `<UserPrincipalName>` with the room mailbox's UPN:

    ```powershell
    Set-CalendarProcessing <UserPrincipalName> -ProcessExternalMeetingMessages $True -DeleteComments $False
    ```

## Step 3A: Configure URL rewrite policies to not modify third party meeting links

To enable the one-touch join experience, meeting join link information from the third-party meeting needs to be present and readable in the meeting invite by the Teams Room device. If your organization uses the [Microsoft Defender for Office 365](/microsoft-365/security/office-365-security/safe-links) safe links feature, or if you use a third-party solution that scans all URLs for threats, it may change the meeting join URLs and make the meeting unrecognizable by the Teams Rooms device. To ensure this doesn't happen, you need to add the third-party meeting service's URLs to the [Defender for Office 365 Safe Links **Do not rewrite** list](/microsoft-365/security/office-365-security/safe-links) or the third-party URL rewrite exception list. If you use a third-party solution, refer to the instructions for that solution to add URLs to its URL rewrite exception list.

Here are some example entries that you may need to add to your Defender for Office 365 Safe Links *Do not rewrite* list or third-party URL rewrite exception list:

- **Cisco Webex** `*.webex.com/*`
- **Zoom** `*.zoom.us/*`, `*.zoom.com/*`, `*.zoomgov.com/*`

> [!CAUTION]
> Only add URLs that you trust to your *do not rewrite* exception list.

## Step 3B: If you are utilizing Direct Guest Join, ensure your network connections are optimized to connect to your desired platform

When using Direct Guest Join, Teams Rooms devices connect directly to the website for that third-party platform. Because of this direct connection, your Teams Rooms devices will need to be able to connect to that third party website, ensure your organization’s firewalls and web filters allow the traffic without authentication and that the web traffic is in an appropriate QoS class (if applicable). Please refer to the third-party meeting platforms documentation for the correct URLs and IPs to allow.

## Step 4: Enable third-party meetings on your Teams Rooms devices 

The last step you need to take is to allow Teams Rooms to join third-party meetings. Most third-party meeting platforms require a username and email address to join them, if the username and email address that you wish to use is different than the device's resource account, you can configure that while enabling third-party meeting join.

## [Teams Rooms on Windows](#tab/MTRW)

If you wish to utilize the cross-platform SIP join capability, you need to enable SIP video calling on your Teams Rooms devices following these instructions: SIP and H.323 Calling Once SIP calling is enabled, the Teams Room will automatically use SIP instead of WebRTC to join the enabled third-party meetings. If SIP calling is enabled but a third party meeting invite sent to the Teams Room does not contain a SIP dial string, the Teams Room device will automatically fall back to using Direct Guest Join over WebRTC for that single meeting instance to ensure you are able to join the meeting. Lastly, if SIP calling is not enabled, Teams Rooms on Windows devices will only utilize Direct Guest Join over WebRTC for third party meetings.

### Using the Pro Management Portal

1. Login to the [Pro Management Portal](enrolling-mtrp-managed-service.md)
2. Select **Rooms**
3. Select your desired room
4. Select **Settings**
5. Select **Meetings**
6. Toggle your desired meeting platforms
7. Select **Apply**

### Using the local device settings

To configure Teams Rooms on Windows using the touchscreen console, do the following:

1. On the Microsoft Teams Rooms console, select **More**.
2. Select **Settings**, and then enter the device administrator username and password.
3. Go to the **Meetings** tab and select a third-party meeting provider you wish to enable (e.g., **Webex**, **Zoom**, etc.).

:::image type="content" source="../media/use-device-settings.png" alt-text="Turning on and off third party providers.":::

1. If you want to join meetings with the username and email address associated with the room mailbox, select **Join with room info**.
1. If you want to join meetings with an alternate username and email address, select **Join with custom info** and enter username and email address you'd like to use.
1. Select **Save and exit**. Your device will restart.

     ![Meetings](https://github.com/MicrosoftDocs/OfficeDocs-SkypeForBusiness/assets/63427703/6503b72c-4482-4ec4-9492-610503d02c36)

### Use the SkypeSettings.xml configuration file

For more information about the `SkypeSettings.xml` file, see [Manage Microsoft Teams Rooms settings with an XML configuration file](xml-config-file.md).

To enable the various platforms, set the XML element to **True**, as follows.

```xml
<ZoomMeetingsEnabled>True</ZoomMeetingsEnabled>
<WebexMeetingsEnabled>True</WebexMeetingsEnabled>

```

You can optionally specify a custom username and email address to join third-party meetings using the following XML elements. If the values you provide aren't valid, the Teams Rooms device will default to use room mailbox username and email address.

```xml
<UseCustomInfoForThirdPartyMeetings>true</UseCustomInfoForThirdPartyMeetings>

<CustomDisplayNameForThirdPartyMeetings>guestname</CustomDisplayNameForThirdPartyMeetings>

<CustomDisplayEmailForThirdPartyMeetings>guest@contoso.com</CustomDisplayEmailForThirdPartyMeetings>
```

## [Teams Rooms on Android](#tab/MTRA)

To configure Teams Rooms on Android locally on the device, do the following:

1. On the Microsoft Teams Rooms device, select **More**.
2. Select **Settings**.
3. Locate **Teams admin settings**, enter the device adminsitrative credentials
4. Select **Meetings**.

    ![Meetings settings for MTR on Android](..\media\step-3b-enable-third-party-meetings-on-teams-rooms-on-android.png)

5. Select the toggle next to the third-party meeting provider(s) you want to enable.
6. If you want to join meetings with a custom username and email address, select **Join with custom name and email**. To update custom personal info, press **Edit custom info** and input your preferred name and email address.
