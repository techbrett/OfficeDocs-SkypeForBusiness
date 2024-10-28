---
title: AI Notetaker in Microsoft Teams
author: MicrosoftHeidi
ms.author: heidip
manager: jtremper
ms.reviewer: andrewklutz
ms.date: 11/18/2024
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
ms.collection: 
  - M365-collaboration
ms.custom:
  - admindeeplinkTEAMS
f1.keywords:
- NOCSH
appliesto: 
  - Microsoft Teams
ms.localizationpriority: high
search.appverid: MET150
description: Learn about AI Notetaker powered by Copilot in Microsoft Teams.
---

# AI Notetaker in Microsoft Teams

AI Notetaker is a collaborative communication agent available to your users in Teams conversations. It combines the power of large language models (LLMs) and Teams data to record notes in real time to help users be productive during collaboration. Stay in the flow of conversation and receive powerful, AI-generated notes within a single workspace. No need for users to switch from reference to reference or app to app.

Use AI Notetaker in peer-to-peer:

- Chats
- Meetings

Unlike an individual user's queries to Copilot in Teams, AI Notetaker displays Copilot's notes within the group's conversation. Users can focus on the conversation and let Copilot take care of the note-taking for everyone.

AI Notetaker also continuously updates as the conversation progresses. For example, AI Notetaker displays the options being considered by the team and then replaces those options with a single choice once the group decides. Now, that's intelligent collaboration right in Teams.

> [!IMPORTANT]
> AI Notetaker's notes are communally shared between collaborators.
>
> However, when an individual user queries Copilot in Teams using the Copilot in Teams pane, their queries and responses from Copilot remain private to that user.
>
> Users are shown a notice in Copilot in Teams when their queries are private or shared with others.

For more information about how users can integrate AI Notetaker into their Teams chats, see [getting from Yasmine]().

For more information about how users can integrate AI Notetaker into their Teams meetings, see [getting from Yasmine]().

## Security, Purview, and Privacy

XXX LINK TO CAROL'S DOC TOO XXX

Copilot and Microsoft 365 are built on Microsoft's comprehensive approach to security, compliance, and privacy. For more information about security and privacy in Microsoft 365 Copilot, see the following articles:

- [Data, Privacy, and Security for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-privacy) for Microsoft 365 Copilot in your organization (work or school).
- [Microsoft Purview data security and compliance protections for generative AI apps](/purview/ai-microsoft-purview).
- [Copilot Pro: Microsoft 365 apps and your privacy](https://support.microsoft.com/office/copilot-pro-microsoft-365-apps-and-your-privacy-6f0d8d80-f4bb-4c9f-989e-64a4adfd62e5) for Microsoft 365 Copilot apps at home.

For answers to frequently asked questions about security and privacy in Copilot in Teams, see [Frequently asked questions about Copilot in Microsoft Teams](https://support.microsoft.com/office/frequently-asked-questions-about-copilot-in-microsoft-teams-e8737767-4087-4ae6-b1d8-10264152b05a).

## Prerequisites and licensing

In general, all Copilot in Teams features require a *Microsoft 365 Copilot* license and an eligible base license for all users because **Microsoft 365 Copilot** is licensed on a per-user subscription model. For a list of the eligible base licenses, see [Understand licensing requirements for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-licensing).

AI Notetaker features are license-checked at the user level; however, if one user in the conversation has a *Microsoft 365 Copilot* license, all members of the conversation can view and benefit from AI Notetaker's note-taking capabilities.

We recommend purchasing *Microsoft 365 Copilot* licenses for all users who could benefit from Copilot in Teams features to ensure maximum coverage.

## Turn on AI Notetaker for chats, posts, and meetings

As an admin, you control whether AI Notetaker is available in your organization or to a certain group of users.

AI Notetaker is blocked to users by default. To turn on AI Notetaker for users, complete the following steps:

### 1. Turn on AI Notetaker

XXX WHAT WILL BE THE STRING IN THE TEAMS ADMIN CENTER? XXX

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard) with your Teams admin credentials.
1. In the left rail navigation, select **Teams apps** > **Manage apps**.
1. In the apps list's search box, search for **AI Notetaker???**.
1. Select **AI Notetaker???** from the app list.
1. In the actions menu, select **Allow**.
1. In the **Allow app?** pop-up, select the **Allow** button.
    1. AI note-taking is turned on when **AI Notetaker???** is turned on.

For more information about managing apps in Teams, see [Manage apps](manage-apps.md).

### 2. Allow AI Notetaker for a group of users

To allow AI Notetaker for users, a new app policy needs to be created and then assigned to users.

Follow the instructions at [Use app permission policies to control user access to apps](teams-app-permission-policies.md) to create a new app policy for AI Notetaker.

You can then assign the policy to your entire tenant or to a select group of users. Follow the instructions at [Add or modify app availability for users](/microsoftteams/app-centric-management#add-or-modify-app-availability-for-users) to assign the policy to users.

### 3. Turn on Loop experiences in Teams for meeting AI notes

Loop experiences in Teams need to be turned on in order for Copilot to generate notes in Teams meetings.

To turn on Loop experiences in Teams, follow the instructions at [Settings management for Loop functionality in Teams](/microsoft-365/loop/loop-components-configuration#settings-management-for-loop-functionality-in-teams).

## Related articles

- [What is responsible AI?](https://support.microsoft.com/topic/what-is-responsible-ai-33fc14be-15ea-4c2c-903b-aa493f5b8d92)
- [Frequently asked questions: AI, Microsoft Copilot, and Microsoft Designer](https://support.microsoft.com/topic/frequently-asked-questions-ai-microsoft-copilot-and-microsoft-designer-987b275d-f6f2-4d5d-94c5-e927cffae705)
- [Where can I get Microsoft Copilot?](https://support.microsoft.com/topic/where-can-i-get-microsoft-copilot-40a622db-6d25-4266-b008-4bbcb55cf52f)
- [Providing feedback about Microsoft Copilot with Microsoft 365 apps](https://support.microsoft.com/topic/providing-feedback-about-microsoft-copilot-with-microsoft-365-apps-c481c26a-e01a-4be3-bdd0-aee0b0b2a423?ocid=CopilotLab_SMC_Privacy_Feedback)
