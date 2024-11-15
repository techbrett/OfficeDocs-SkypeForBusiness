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

This article provides guidance for how to troubleshoot common issues for the Walkie Talkie app in Microsoft Teams. Use this information to help identify the source of the issues for more effective troubleshooting.

## Common issues

### Incoming transmissions drop

If users hear an audio tone or a notification that a transmission is incoming but they don't receive the transmission, try the following steps:

1. Make sure the network is healthy.
1. Leave and reconnect to the channel.
1. If the issue persists, send logs to Microsoft for investigation.

### Missing transmissions

1. Verify that both the sender and receive are connected to the same Walkie Talkie channel.
1. Make sure that Walkie Talkie is connected to the network.
1. Restart Walkie Talkie to refresh the connection.
1. Check whether the user's status is set to **Do not disturb**, in focus time, or in quiet time in Teams on the device. These modes might block transmissions.

    If the user is in any of these modes, switch out of that mode, check that notifications are turned on, and then restart Walkie Talkie to ensure that changes in notification settings take effect.

### Participants list refresh

The participants list contains a list of users who are actively connected to a Walkie Talkie channel and can potentially hear transmissions. Sometimes this list can become inaccurate because of network issues or if a user's status is set to **Do not disturb**.

If the participants list in a Walkie Talkie channel doesn't accurately reflect the users who are actively connected to the channel, have the users try the following steps:

1. Leave and reconnect to the channel.
1. Switch channels.
1. If a user is using an iOs device, close, and then reopen Walkie Talkie.
1. Send at least two transmissions.

### Network connectivity

### Device issues

- Make sure devices have the latest possible firmware update.

- Ensure the device has adequate battery life and isn't overheating.

- Update the device’s operating system to the latest version.

- Reset the device’s settings to use default settings, if persistent issues occur.

- Check for and install any available Walkie Talkie updates.

### Headset issues

### Permissions issues

### Walkie Talkie not appearing

### Proxy servers

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
