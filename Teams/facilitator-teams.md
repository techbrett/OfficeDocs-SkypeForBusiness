---
title: Set up Facilitator in Microsoft Teams for collaborative AI notes
author: DaniESmith
ms.author: danismith
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
description: Learn about how the AI-powered Facilitator agent in Microsoft Teams can take collaborative AI notes powered by Copilot.
---

# Set up Facilitator in Microsoft Teams for collaborative AI notes

> [!IMPORTANT]
> This feature is currently in Teams Public preview.
>
> Features in preview might not be complete and could undergo changes before becoming available in the public release. They're provided for evaluation and exploration purposes only.

Facilitator is a collaborative communication agent available to your users in Teams conversations. It combines the power of large language models (LLMs) and Teams data to record notes and help users be productive during collaboration. Stay in the flow of conversation and receive powerful, AI-generated notes within a single workspace. No need for users to switch from reference to reference or app to app.

Use Facilitator in peer-to-peer:

- Chats
- Meetings

Unlike an individual user's queries to Copilot in Teams, Facilitator displays Copilot's notes within the group's conversation. Users can focus on the conversation and let Copilot take care of the note-taking for everyone.

Facilitator also continuously updates as the conversation progresses. For example, the AI notes display the options being considered by the team and then replaces those options with a single choice once the group decides. Now, that's intelligent collaboration right in Teams.

> [!IMPORTANT]
> Facilitator's notes are communally shared between collaborators.
>
> However, when an individual user queries Copilot in Teams using the Copilot in Teams pane, their queries and responses from Copilot remain private to that user.
>
> Users are shown a notice when their queries are private or shared with others.

For more information about how users can integrate AI notes into their Teams chats, see [Invite Copilot as a chat participant in Microsoft Teams](https://support.microsoft.com/topic/d03e9237-ed4d-4695-8732-73a396e8b21f).

For more information about how users can integrate Notes into their Teams meetings, see [Add Team Copilot to a Microsoft Teams meeting](https://support.microsoft.com/topic/b877d958-6b62-4296-9ceb-e8c1f726f51d).

## Security, Purview, and Privacy

Facilitator, Copilot, and Microsoft 365 are built on Microsoft's comprehensive approach to security, compliance, and privacy. For more information about security and privacy in Microsoft 365 Copilot, see the following articles:

- [Data, Privacy, and Security for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-privacy) for Microsoft 365 Copilot in your organization (work or school).
- [Microsoft Purview data security and compliance protections for generative AI apps](/purview/ai-microsoft-purview).
- [Copilot Pro: Microsoft 365 apps and your privacy](https://support.microsoft.com/office/copilot-pro-microsoft-365-apps-and-your-privacy-6f0d8d80-f4bb-4c9f-989e-64a4adfd62e5) for Microsoft 365 Copilot apps at home.

### Facilitator limitations

Currently, AI notes aren't supported in external chats.

## Prerequisites and licensing

The following list contains the prerequisites for users to be able to access AI notes in Teams chats and meetings:

- An eligible *Microsoft 365* base license.
  - For the list of eligible base licenses, see [Understand licensing requirements for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-licensing).
- A *Microsoft 365 Copilot* license.
  - For information on how to acquire *Microsoft 365 Copilot* licenses, see [Where can I get Microsoft Copilot?](https://support.microsoft.com/topic/where-can-i-get-microsoft-copilot-40a622db-6d25-4266-b008-4bbcb55cf52f).
- Be a Microsoft Teams Public preview participant.
  - For information on how to access Teams Public preview features, see [Microsoft Teams Public preview](/microsoftteams/public-preview-doc-updates).

## Turn on AI notes for chats and meetings

As an admin, you control whether AI notes are available to your entire organization or to a certain group of users.

AI notes are blocked to users by default. To turn on AI notes for users, complete the following steps:

### 1. Turn on Facilitator in the Teams admin center

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard) with your Teams admin credentials.
1. In the left rail navigation, select **Teams apps** > **Manage apps**.
1. In the apps list's search box, search for **Facilitator**.
1. Select **Facilitator** from the app list.
1. In the actions menu, select **Allow**.
1. In the **Allow app?** pop-up, select the **Allow** button.
    1. AI notes are turned on when **Facilitator** is turned on.

For more information about managing apps in Teams, see [Manage apps](manage-apps.md).

### 2. Allow Facilitator for a group of users

To allow Facilitator for users, a new app policy needs to be created and then assigned to users.

Follow the instructions at [Use app permission policies to control user access to apps](teams-app-permission-policies.md) to create a new app policy for Facilitator.

You can then assign the policy to your entire tenant or to a select group of users. Follow the instructions at [Add or modify app availability for users](/microsoftteams/app-centric-management#add-or-modify-app-availability-for-users) to assign the policy to users using app-centric management.

### 3. Turn on Loop experiences in Teams for meeting AI notes

Loop experiences in Teams need to be turned on in order for Copilot to generate notes in Teams meetings.

To turn on Loop experiences in Teams, follow the instructions at [Settings management for Loop functionality in Teams](/microsoft-365/loop/loop-components-configuration#settings-management-for-loop-functionality-in-teams).

## Related articles

- [What is responsible AI?](https://support.microsoft.com/topic/what-is-responsible-ai-33fc14be-15ea-4c2c-903b-aa493f5b8d92)
- [Frequently asked questions: AI, Microsoft Copilot, and Microsoft Designer](https://support.microsoft.com/topic/frequently-asked-questions-ai-microsoft-copilot-and-microsoft-designer-987b275d-f6f2-4d5d-94c5-e927cffae705)
- [Providing feedback about Microsoft Copilot with Microsoft 365 apps](https://support.microsoft.com/topic/providing-feedback-about-microsoft-copilot-with-microsoft-365-apps-c481c26a-e01a-4be3-bdd0-aee0b0b2a423?ocid=CopilotLab_SMC_Privacy_Feedback)
