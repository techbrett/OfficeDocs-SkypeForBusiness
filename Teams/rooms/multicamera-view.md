---  
title: "Multiple camera view in Teams Rooms"  
author: mstonysmith
ms.author: tonysmit  
manager: pamgreen
ms.reviewer: sammili 
ms.date: 01/09/2025  
ms.topic: article
ms.service: msteams
ms.subservice: itpro-rooms
audience: Admin
appliesto: 
  - Microsoft Teams
ms.collection: 
  - teams-rooms-devices
  - Tier1
f1.keywords: 
  - NOCSH
search.appverid: MET150
ms.localizationpriority: medium
ms.custom: QuickDraft  
ai-usage: ai-assisted  
description:  Learn how to set up and manage multiple cameras in Microsoft Teams Rooms on Windows to provide various angles and perspectives during meetings.
---  

# Configuring Multiple Camera View in Microsoft Teams Rooms on Windows

## Prerequisites

- Teams Rooms resource account with an assigned Microsoft Teams Rooms Pro license. For more information, see [Microsoft Teams Rooms Licensing](/microsoftteams/rooms/rooms-licensing).
- Teams Rooms on Windows version 5.3 or later installed.
- Connect a maximum of four Teams certified single stream USB camera peripherals.

> [!IMPORTANT]
> Multi-stream intelligent cameras aren't supported.

## Recommendations

- USB has limited bandwidth. Each camera should be connected to the Microsoft Teams Rooms device USB port directly. If there are insufficient Microsoft Teams Rooms USB ports for all peripheral devices, a USB hub can be used to but should have only one camera connected to it.
- Older MTR models may not have sufficient capacity to process multiple simultaneous videos. Video freeze or missing video streams might occur. Therefore, the following is our minimum compute recommendation:
  - Intel Core i5 processor or above
  - For 2-3 camera setup, minimum Intel ninth Generation CPU
  - For four camera setup, minimum Intel 12th Generation CPU
  - Cameras should support MJPEG video format.

## Set up Multiple Camera View

Teams Rooms on Windows can send up to four single stream cameras feeds to render on the receiver-side for remote meeting participants to view simultaneously. This is an opt-in feature that requires admins to enable the Multiple camera view toggle and map cameras to the desired order that are displayed on the receiver side.

There are two ways to set up multiple camera views:

### Using the admin settings on the device

1. In admin settings on-device, go to **Settings \> Peripherals**, and ensure **Default Video Camera** has been selected.
2. Enable **Multiple camera view** toggle.
3. When **Multiple camera view** is enabled, **IntelliFrame** toggle is disabled.
4. When **Multiple camera view** is enabled, **Video Camera 2** dropdown selection appears. Select a camera.
5. Check **Preview** to see and verify the camera view.
6. Continue to select **Add Camera** until you complete the configuration as desired.

### Using Remote Access in the Teams Rooms Pro Management portal

1. In Pro Management Portal, under **Teams Rooms on Windows**, go to **Settings \> Remote Access**. Ensure that Remote Access is enabled by going to the **Remote Access** section and set **Enable Remote Access** to **Enabled**.
2. Choose **Rooms** and select the room device to remotely administer. Under the **Rooms** tab, select **Remote Access**, then **Start Session**.
3. Follow the on-device admin settings until you complete the configuration as desired.

## How remote participants experience Multiple Camera View

Remote participants can view up to four camera feeds simultaneously in Gallery view. Each camera view is displayed in a 16:9 aspect ratio in equal size within the optimized room video tile. Using the carousel navigation, remote participants can switch camera views for their view only. When content is shared, the default camera view is shown with the ability to navigate to one camera view at a time.

**Camera 1**
:::image type="content" source="/microsoftteams/rooms/media/multicamera/camera1.png" alt-text="Screenshot of what a Teams Rooms display from camera 1 looks like when multiple cameras aren't used." lightbox="/microsoftteams/rooms/media/multicamera/camera1-hi-res.png":::

**Camera 2**
:::image type="content" source="/microsoftteams/rooms/media/multicamera/camera2.png" alt-text="Screenshot of what a Teams Rooms display from camera 2 looks like when multiple cameras aren't used." lightbox="/microsoftteams/rooms/media/multicamera/camera2-hi-res.png":::

**Example of a 2-camera view**
:::image type="content" source="/microsoftteams/rooms/media/multicamera/default-camera.png" alt-text="Screenshot of what a Teams Rooms display looks like when multiple cameras are used." lightbox="/microsoftteams/rooms/media/multicamera/default-camera-hi-res.png":::

## Related Articles

- [Microsoft Teams Rooms Licensing](rooms-licensing.md)
- [Content cameras](content-camera.md?tabs=Windows)
- [Microsoft Teams Rooms planning and guidance](/microsoftteams/rooms/room-planning-guidance)
