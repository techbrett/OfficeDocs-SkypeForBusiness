---
title: Admins- Manage sensitive Microsoft Teams town halls and webinars
ms.author: wlibebe
author: wlibebe
manager: pamgreen
ms.topic: article
ms.service: msteams
ms.reviewer: vivek.mohan
ms.date: 11/12/2024
audience: admin
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.collection: 
  - m365solution-compliantmeetings
  - m365initiative-meetings
  - highpri
  - Tier1
appliesto: 
  - Microsoft Teams
description: Learn how to configure sensitivity labels for sensitive webinars and town halls.
---

# Admins- Manage sensitive Microsoft Teams town halls and webinars

[!INCLUDE[Teams Premium ECM](includes/teams-premium-ecm.md)]

As an admin, you might have compliance requirements for Microsoft Teams town halls and webinars in your organization. You can customize settings in your per-organizer sensitivity labels to manage these requirements.

> [!IMPORTANT]
> Sensitivity labels only applies to new events. If you change the sensitivity label after an organizer creates an event, the label doesn’t apply to that existing event. The label only applies to events created after you set the new label.

## How do I create and manage sensitivity labels?

For detailed instructions on how to create and manage sensitivity labels, see [Use sensitivity labels to protect calendar items, Teams meetings, and chat[(/purview/sensitivity-labels-meetings).  

To learn how your users use sensitivity labels, see [Sensitivity labels for Teams meetings](https://support.microsoft.com/office/sensitivity-labels-for-teams-meetings-2b244d1d-72d0-471e-8e58-c41079e190fb).  

## Manage recording

You can use sensitivity labels to control whether events are recorded automatically. To learn more about managing recordings, see [Manage Microsoft Teams meeting recording options for sensitive meetings](manage-meeting-recording-options.md).

## Manage chat

You can use sensitivity labels to manage chat and prevent copying and forwarding. For town halls, only organizers, co-organizers, and presenters use chat. For details on how to set sensitivity labels for chat in events, see [Manage chat for sensitive Teams meetings](manage-chat-sensitive-meetings.md).

## Manage the lobby and event access

You can use sensitivity labels to manage event access and the lobby for town halls. For webinars, you can manage the lobby, but not event access. You can also control whether people dialing in can bypass the lobby for both webinars and town halls. To learn more about managing lobby options with sensitivity labels, see [Control who can bypass the meeting lobby in Microsoft Teams](who-can-bypass-meeting-lobby.md).

### Town halls

The options you set for the Who can bypass the lobby setting control event access for town halls. The following table shows how this setting affects event access for town halls based on whether you lock the setting:

|Sensitivity label: Who can bypass the lobby |Is the sensitivity label for the lobby locked? |Event access for town halls |
|:------|:----------:|:---------------:|
|Everyone|No|Organizers can create public, in org, or town halls that require an invitation to join.|
|Everyone|Yes|Organizers can only create public town halls.|
|People in my org, and guests |No|Organizers can create in org, or town halls that require an invitation to join.|
|People in my org, and guests |Yes|Organizers can only create in org town halls. |

### Webinars

Your organizers control event access for webinars through the Who can bypass the lobby setting, not sensitivity labels. However, you can use the Who can bypass the lobby setting to control the lobby for webinars in your org.  The following table shows how this setting affects lobby access for webinars based on whether you lock the setting:

|Sensitivity label: Who can bypass the lobby |Is the sensitivity label for the lobby locked? |Lobby access for webinars |
|:------|:----------:|:---------------:|
|Everyone|No|Organizers can allow anyone to bypass the lobby.|
|Everyone|Yes|All attendees always bypass the lobby. |
|People in my org, and guests |No|Organizers can allow attendees in your organization and guests defined in external access to bypass the lobby.|
|People in my org, and guests |Yes|Attendees in your organization and guests defined in external access always bypass the lobby.|
|People who were invited |No|Organizers can allow co-organizers and presenters to bypass the lobby.|
|People who were invited  |Yes|Organizers and presenters always bypass the lobby. |

## Examples

For examples on managing sensitivity labels with different levels of protection, see these articles:

- [Configure Teams meetings with protection for highly sensitive data](configure-meetings-highly-sensitive-protection.md#sensitivity-labels)

- [Configure Teams meetings with protection for highly sensitive data](configure-meetings-highly-sensitive-protection.md#sensitivity-labels)

- [Configure Teams meetings with baseline protection - Microsoft Teams](configure-meetings-baseline-protection.md#sensitivity-labels)

## Unsupported features and settings

Webinars and town halls don’t support the following features and settings:

- End-to-end encryption
- Watermarks for town halls
- The **Who can record** setting

## Related topics

- [Configure Teams meetings with three tiers of protection](configure-meetings-three-tiers-protection.md)
- [Overview of custom meeting templates in Microsoft Teams](custom-meeting-templates-overview.md)
- [Use Teams meeting templates, sensitivity labels, and admin policies together for sensitive meetings](meeting-templates-sensitivity-labels-policies.md)
- [Use sensitivity labels to protect calendar items, Teams meetings and chat](/microsoft-365/compliance/sensitivity-labels-meetings)