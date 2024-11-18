---
title: Walkie Talkie troubleshooting guide
author: lana-chin
ms.author: v-chinlana
manager: jtremper
ms.topic: conceptual
ms.service: msteams
audience: admin
ms.reviewer: yinchang
description: Use this guidance to help you troubleshoot common issues for the Walkie Talkie app in Microsoft Teams.
ms.localizationpriority: medium
search.appverid: MET150
f1.keywords: NOCSH
ms.collection: 
- M365-collaboration
- m365-frontline
- teams-1p-app-admin
- highpri
appliesto: 
  - Microsoft Teams
  - Microsoft 365 for frontline workers
ms.date: 
---

# Walkie Talkie troubleshooting guide

This article provides guidance for how to troubleshoot common issues that users might encounter when using the Walkie Talkie app in Microsoft Teams. Use this information to help identify the source of the issues for more effective troubleshooting.

## Common issues

### Incoming transmissions not received

If a user hears an audio tone or a notification that a transmission is incoming but they don't receive the transmission, have the user try the following steps:

1. Make sure the network is healthy.
1. Leave and reconnect to the channel.

If the issue persists, send logs to Microsoft for investigation.

### Missing transmissions

1. Verify that both the sender and receiver are connected to the same Walkie Talkie channel.
1. Make sure that Walkie Talkie is connected to the network.
1. Restart Walkie Talkie to refresh the connection.
1. Check whether the user's status is set to **Do not disturb**, in focus time, or in quiet time in Teams on the device. These modes might block transmissions.

    If the user is in any of these modes, have the user switch out of that mode. Make sure that notifications are turned on, and then restart Walkie Talkie to ensure that any changes to notification settings take effect.

### Participants list in a channel is inaccurate

The participants list is the list of users who are actively connected to a Walkie Talkie channel and can potentially hear transmissions. Sometimes this list can become inaccurate. For example, a user is missing from the list even though they're connected to the channel. This issue can occur because of network issues or if a user's status is set to **Do not disturb**.

If the participants list in a channel doesn't accurately reflect the users who are actively connected to the channel, have the users try the following steps:

1. Leave and reconnect to the channel.
1. Switch channels.
1. Close, and then reopen Walkie Talkie (if on an iOS device).
1. Send at least two transmissions.

### Network connectivity issues

To check the quality of the network connection, in Teams, tap your profile picture, and then tap **Settings** > **Walkie Talkie** > **Test Network Quality**

What good looks like:

- Jitter < 30 ms, RTT less than 150, Avg RountTripTime <100 ms
- Max Avg RounTripTime <500 ms = Medium, >500 ms Is poor
- PacketLossRate Avg <1% MaxAvgPacketLossRate <10%
- Latency greater than 500 ms is poor; Jitter should be less than 30 ms.
  - If jitter is high, you hear crackling sounds or audio breaking
  - If latency is high, connecting to Walkie Talkie will take longer, and jitter will be higher as well.

- Move to an area with better network coverage.
- Switch between WiFi and cellular data to determine which provides a more stable connection.
- Close any other apps that might be using network bandwidth.
- Restart the device to reset the network connection.

### Device issues

- Make sure the device has the latest possible firmware update installed.
- Check that the device has adequate battery life and isn't overheating.
- Update the device’s operating system to the latest version.
- Reset the device’s settings to use the default settings, if persistent issues occur.
- Check for and install any available Walkie Talkie updates.

### Headset issues

Check the headset:

- Check the headset for any physical damage or connectivity issues.
- Check whether the headset has noise cancellation and voice isolation capabilities.
- Make sure the headset is properly connected to the device.
- Test the headset with another app to see if the issue persists.
- Make sure wireless headsets are fully charged.

<!--
- Replace the headset if it is found to be defective or incompatible.
- SCO channel connection settings-->

Additionally, check the following things:

- Make sure the device’s microphone and speaker are clean and unobstructed.
- Adjust the audio settings in Walkie Talkie to improve sound quality.

### Permissions issues

Make sure Teams has permissions to access the microphone, network, and notifications on the device.

1. Go to Settings on the device and check whether Teams has access to the microphone, network, and notifications.
1. Grant access to Teams to the items in step 1 for which Teams doesn't already have access.
1. Restart Teams.
1. If permissions issues continue to occur, reinstall Teams on the device.

### Walkie Talkie not appearing

<!--1. Walkie Talkie will show up in Teams mobile as a pre-installed app for all users in ring0, ring1, ring1.5, ring2, ring3, ring3.6, and ring3.9, irrespective of their license and TAC setup policy. Example: E SKU user A in ring3.9 will see Walkie Talkie in Teams with no policy setup required, while E SKU user in ring4 will not see it until the app is pinned via policy.

2. Walkie Talkie will show up for all users with an F license, regardless of their TAC setup policy and user ring. Example: All F-SKU users should see Walkie Talkie app in Teams without needing to do anything in TAC

3. For E SKUs, needs to be top 10 app for pinned app policy

If a tenant wants the Walkie Talkie App to show up for E SKU users for all rings (e.g. ring4), they must pin the Walkie Talkie app via app setup policy and assign the policy to each user. Alternatively, they may also purchase F licenses and assign them to users who they want to have the Walkie Talkie app. Use app setup policies to pin and auto-install apps for users

If a customer provides a specific E-SKU user who does not have the Walkie Talkie app appearing, verify their setup policy with the following steps:

1. In Teams Admin Center, go to "Users" -> "Manage Users" -> search for the affected user -> Click on the user -> Click the "Policies" tab.

2. Click on the policy to the right of "App setup policy" and verify that Walkie Talkie appears in the "Pinned apps" section.-->

### Proxy servers

Using a proxy server with Walkie Talkie and Teams isn't recommended.

Performance-related issues can be introduced to the environment through latency and packet loss by attempting to route Teams traffic through a proxy server. These issues can occur if the proxy is unable to handle the amount of traffic passing through it, or incorrectly routes traffic to a Microsoft network service front door location that's further away from users. Issues such as these can result in a negative experience within Walkie Talkie and Teams.

However, if you need to use a proxy server, make sure it's set up correctly. To learn more, see:

- [Proxy servers for Teams](proxy-servers-for-skype-for-business-online.md)
- [Office 365 URLs and IP address ranges](/microsoft-365/enterprise/urls-and-ip-address-ranges#skype-for-business-online-and-microsoft-teams)

## Send logs to Microsoft for investigation

If users are still experiencing issues, you can send logs to us for further investigation.

Reproduce the issue, clearly describe it and mention Walkie Talkie in your report.

You can send in logs in the following two ways:

- Shake and send. You need to enable this feature at the tenant level for Teams.
- Send feedback. This is the default feedback option. In Teams, tap your profile picture, tap **Settings**, tap **Help & feedback**, and then tap **Send feedback**.

To learn more, see:

- [Give feedback in Teams](https://support.microsoft.com/office/give-feedback-in-microsoft-teams-c0fb6297-22af-4db5-b19b-69e0a6720927#ID0EBBD=Android)
- [Manage feedback policies in Teams](manage-feedback-policies-in-teams.md)

## Frequently asked questions

Why is the Walkie Talkie app showing up for some users and not others?

For users with an E license, the Walkie Talkie app shows up automatically without any policy needed if they're part of an early ring (eg. an admin part of the Private Preview Ring will get the Walkie Talkie app automatically). However, E-SKU users in general ring must have an app setup policy assigned to them with the Walkie Talkie app pinned or else they won't see the app. Needs to be pinned in top 10 apps for E SKUs.

I have my permission policy setup so that all Microsoft apps are "Allowed", shouldn't Walkie Talkie appear?

A permission policy isn't sufficient. E-SKU users in general ring must have an app setup policy assigned to them with the Walkie Talkie app pinned or else they will not see the app.

Why can't I add the app as an "Installed app" instead of "Pinned app" in my app setup policy?

Currently Walkie Talkie can only be pinned, it doesn't support being added as an "Installed app" and won't show up if you try searching for it in this section.

Is the app available for desktop users?

The Walkie Talkie app is only available for Teams on Android and iOS.


By following these troubleshooting steps, users can address common problems encountered while using the Microsoft Teams Walkie Talkie app and ensure a smoother communication experience.

## Known limitations

We don't support channel navigation from the lock screen. You'll be able to hear transmissions across multiple channels that you're connected to with “Listen to Multiple Channels” mode turned on. You can only transmit to your primary selected channel while the phone is locked.

· you can If you need to change channels you can do so by going to Walkie Talkie App in Teams,

Audio static

- iOS devices: Walkie Talkie doesn't support noise cancellation or voice isolation. Users may hear some background noise during communications.
- Android devices: If the user's device supports noise cancellation, they can turn it on in Walkie Talkie settings.  can turn this on in Teams settings > Walkie Talkie.

<!--
## Prepare your network

Walkie Talkie requires connectivity to the internet. Use the following guidance to set up your organization's network for Walkie Talkie:

- Make sure that all endpoints listed for Teams in [Office 365 URLs and IP address ranges](/microsoft-365/enterprise/urls-and-ip-address-ranges#skype-for-business-online-and-microsoft-teams) are reachable by Teams users on your network.

- Prepare your network:

  - [Prepare your organization's network for Teams](prepare-network.md)
  - [Proxy servers for Teams](proxy-servers-for-skype-for-business-online.md)

- Download and run the [Microsoft Teams Network Assessment Tool](https://www.microsoft.com/download/details.aspx?id=103017) to test your network performance and connectivity to determine how well your network will perform with Walkie Talkie.

## Deploy Walkie Talkie

You deploy and manage Walkie Talkie from the Teams admin center. Walkie Talkie is supported on Android devices with Google Mobile Services (GMS) and iOS devices.

> [!IMPORTANT]
> Deployment is a three-step process. You'll need to complete all three steps for your users to have access to Walkie Talkie.

### Step 1: Make sure Walkie Talkie is enabled in your organization

You control whether the app is available at the organization level on the [Manage apps](manage-apps.md) page in the Microsoft Teams admin center. To confirm that the app is enabled in your organization:

1. In the left navigation of the Teams admin center, go to **Teams apps** > **Manage apps**.
2. In the list of apps, search for the Walkie Talkie app, select it, and then make sure the **Status** toggle is set to **Allowed**.

### Step 2: Create and assign an app permission policy

Control which users in your organization can use Walkie Talkie by assigning app permission policies in the Teams admin center. To learn more, see [Use app permission policies to control user access to apps](teams-app-permission-policies.md).

Make sure Walkie Talkie is an allowed app in the app permission policy, and you assign the policy to all users who need Walkie Talkie.

### Step 3: Pin Walkie Talkie for your users

Pin Walkie Talkie to Teams for easy access. This step depends on which license your users have.

- [If your users have E licenses](#e-license-use-an-app-setup-policy-to-pin-walkie-talkie-to-teams)
- [If your users have F licenses](#f-license-use-the-tailored-frontline-app-experience-to-pin-walkie-talkie-and-other-apps-to-teams)

#### E license: Use an app setup policy to pin Walkie Talkie to Teams

> [!NOTE]
> If your users have an E licence and [Public preview is enabled in Teams](public-preview-doc-updates.md), Walkie Talkie is pre-pinned to the app bar.

App setup policies let you customize Teams to pin apps that are most important for your users in your users.

To pin the Walkie Talkie app for your users, you can edit the global (Org-wide default) policy or create and assign a custom policy in app setup policy. To learn more, see [Use app setup policies to pin and auto-install apps for users](teams-app-setup-policies.md).

:::image type="content" source="media/deploy-walkie-talkie-2.png" alt-text="Screenshot showing adding Walkie Talkie to the pinned apps list in the Add pinned apps pane." lightbox="media/deploy-walkie-talkie-2.png":::

> [!NOTE]
> If you're pinning more than 10 apps, Walkie Talkie must be added to one of the first 10 slots in the list.

#### F license: Use the Tailored frontline app experience to pin Walkie Talkie and other apps to Teams

The tailored frontline app experience in Teams pins the most relevant apps in Teams for users who have an [F license](https://www.microsoft.com/microsoft-365/enterprise/frontline#office-SKUChooser-0dbn8nt). Pinned apps include Walkie Talkie, Shifts, Tasks, and Approvals. By default, this feature is on, giving your frontline workers an out-of-the-box experience tailored to their needs.

The apps are pinned to the app bar at the bottom of Teams mobile clients where users can quickly and easily access them.

To learn more, including how the experience works with app policies that you set, see [Tailor Teams apps for your frontline workers](/microsoft-365/frontline/pin-teams-apps-based-on-license?bc=%2fmicrosoftteams%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoftteams%2ftoc.json).-->
