---  
title: "Whiteboard on Teams Rooms" 
description:  
author: tonysmit
ms.author: mstonysmith
manager: pamgreen
ms.date: 12/13/2024  
ms.topic:  
ms.service: msteams  
ms.subservice: itpro-devices + itpro-rooms  
ms.localizationpriority:  
ms.collection:  
ms.custom: QuickDraft  
ms.reviewer:  yoojinjung 
search.appverid: MET150  
f1.keywords:  
audience:  
ai-usage:  
- ai-assisted  
description: Learn how to use Microsoft Whiteboard on Microsoft Teams Rooms (MTR) to enhance collaboration during and outside meetings.
---  

# Using Microsoft Whiteboard on Microsoft Teams Rooms

Microsoft Whiteboard on Microsoft Teams Rooms (MTR) is a tool for enhancing collaboration by allowing participants to visually share ideas and work together in real-time, no matter where they are. This article provides information on how to use Whiteboard in both meeting and non-meeting scenarios.

## Outside of a Meeting

Brainstorm effortlessly in the office by tapping the **Whiteboard** button on the home screen. With a single touch, Microsoft Whiteboard launches, enabling collaboration outside of a Teams meeting.

- **Temporary Whiteboards:** Since resource accounts do not have OneDrive, starting a whiteboard from Teams Rooms creates a temporary session. To save your work, select the **Save** button and invite your Teams work account. This ensures the whiteboard is saved in your OneDrive for Business.
- **Warning:** Users will get a Save error if they invite a participant who does not have OneDrive or invite an external user.
- **Switch to online collaboration:** Transition seamlessly from local to online collaboration by selecting **Start meeting** on the whiteboarding screen. This initiates an ad-hoc meeting and presents a temporary whiteboard. Add participants to the meeting and collaborate in real-time. The temporary whiteboard will be saved to the OneDrive of the first participant, in the same tenant, who does not join through a Teams Rooms device. Participants will get an email from the whiteboard owner with a link to the whiteboard. Additionally, participants can access the whiteboard in the meeting chat's **Meeting Whiteboard** tab menu.
- **Note:** Upon selecting **Start meeting**, Teams Rooms users can invite others to the meeting. A participant not joining through a Teams Rooms device must join for the Whiteboard to become collaborative. Whiteboard collaboration between two Teams Rooms only is not supported.

Temporary whiteboard example: (Image 1)  
Once it's saved to a participant's OneDrive for Business: (Image 2)

## In a Meeting

When a remote participant shares a whiteboard in a meeting, Teams Rooms displays it in the shared content area.

- **Interactive whiteboarding:** If your Teams Rooms device is a Touch board or configured with a touch-enabled Front of Room display, you can interact with the shared whiteboard.
- **Start a whiteboard:** To start a whiteboard during a meeting from Teams Rooms devices, tap **Share** button and select **Microsoft Whiteboard**. If the meeting is scheduled by a non-MTR user in the same tenant, the whiteboard will be saved in the organizer's OneDrive if they are present when the whiteboard is initiated. If the organizer is not present when the whiteboard is initiated, the whiteboard will instead be saved in the OneDrive of a non-MTR participant present in the meeting.
- **Note:** Please check your tenant settings meet the requirements outlined in [Manage sharing for Microsoft Whiteboard](https://learn.microsoft.com/microsoft-whiteboard/manage-sharing) to have the **Start Whiteboard** feature.

## Whiteboard on Teams Rooms on Windows

The **Start whiteboard** feature is enabled by default for Touch board devices like Surface Hub 3. This means:

- **Home screen:** The **Whiteboard** button appears outside of meetings next to **Calendar**.
- **In-meeting Share Tray:** The **Microsoft Whiteboard** option is available.

Even if the **Start Whiteboard** feature is disabled and/or your Teams Rooms device is not a Touch board device like Surface Hub 3, you can view and follow whiteboards shared by remote participants in a meeting. It mirrors a remote participant's view when the remote participant uses the [Follow me](https://learn.microsoft.com/whiteboard-follow-me-feature) feature on the whiteboard.

**Note:** If you want to disable the **Start Whiteboard** feature, please apply this XML: `false`

## Whiteboard on Teams Rooms on Android

The **Start Whiteboard** feature is enabled by default for any Teams Rooms on Android devices. This means:

- **Home screen:** The **Whiteboard** button appears outside of meetings next to **Calendar**.
- **In-meeting Share Tray:** The **Microsoft Whiteboard** option is available.

Even if the **Start Whiteboard** feature is disabled on your Teams Rooms on Android device, you can view and follow whiteboards shared by remote participants in a meeting. It mirrors a remote participant's view when the remote participant uses the [Follow me](https://learn.microsoft.com/whiteboard-follow-me-feature) feature on the whiteboard.

**Note:** If needed, you can disable the **Start Whiteboard** feature via the admin setting on your device or by applying a configuration profile in Teams Admin Center under **Allow room to use Microsoft Whiteboard** setting in the **Meeting settings** section.

## Related articles

- [Microsoft Teams Rooms](https://learn.microsoft.com/microsoft-teams/rooms)
- [Microsoft Whiteboard](https://learn.microsoft.com/microsoft-whiteboard)