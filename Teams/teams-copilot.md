---
title: AI Notes in Microsoft Teams
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
description: Learn about AI Notes powered by Copilot in Microsoft Teams.
---

# AI Notes in Microsoft Teams

> [!IMPORTANT]
> This feature is currently in Teams Public preview.
>
> Features in preview might not be complete and could undergo changes before becoming available in the public release. They're provided for evaluation and exploration purposes only.

AI Notes is a collaborative communication agent available to your users in Teams conversations. It combines the power of large language models (LLMs) and Teams data to record notes and help users be productive during collaboration. Stay in the flow of conversation and receive powerful, AI-generated notes within a single workspace. No need for users to switch from reference to reference or app to app.

Use AI Notes in peer-to-peer:

- Chats
- Meetings

Unlike an individual user's queries to Copilot in Teams, AI Notes displays Copilot's notes within the group's conversation. Users can focus on the conversation and let Copilot take care of the note-taking for everyone.

AI Notes also continuously updates as the conversation progresses. For example, AI Notes displays the options being considered by the team and then replaces those options with a single choice once the group decides. Now, that's intelligent collaboration right in Teams.

> [!IMPORTANT]
> AI Notes's notes are communally shared between collaborators.
>
> However, when an individual user queries Copilot in Teams using the Copilot in Teams pane, their queries and responses from Copilot remain private to that user.
>
> Users are shown a notice when their queries are private or shared with others.

For more information about how users can integrate AI Notes into their Teams chats, see [getting from Yasmine]().

For more information about how users can integrate AI Notes into their Teams meetings, see [getting from Yasmine]().

## Security, Purview, and Privacy

XXX LINK TO CAROL'S DOC TOO XXX

Copilot and Microsoft 365 are built on Microsoft's comprehensive approach to security, compliance, and privacy. For more information about security and privacy in Microsoft 365 Copilot, see the following articles:

- [Data, Privacy, and Security for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-privacy) for Microsoft 365 Copilot in your organization (work or school).
- [Microsoft Purview data security and compliance protections for generative AI apps](/purview/ai-microsoft-purview).
- [Copilot Pro: Microsoft 365 apps and your privacy](https://support.microsoft.com/office/copilot-pro-microsoft-365-apps-and-your-privacy-6f0d8d80-f4bb-4c9f-989e-64a4adfd62e5) for Microsoft 365 Copilot apps at home.

## Prerequisites and licensing

The following list contains the prerequisites for users to be able to access AI Notes in Teams chats and meetings:

- An eligible *Microsoft 365* base license.
  - For the list of eligible base licenses, see [Understand licensing requirements for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-licensing).
- A *Microsoft 365 Copilot* license.
  - For information on how to acquire *Microsoft 365 Copilot* licenses, see [Where can I get Microsoft Copilot?](https://support.microsoft.com/topic/where-can-i-get-microsoft-copilot-40a622db-6d25-4266-b008-4bbcb55cf52f).
- Be a Microsoft Teams Public preview participant.
  - For information on how to access Teams Public preview features, see [Microsoft Teams Public preview](/microsoftteams/public-preview-doc-updates).

> [!NOTE]
> The AI Notes agent is license-checked at the user level; however, if one user in the conversation has a *Microsoft 365 Copilot* license, all members of the conversation can view and benefit from AI Notes's note-taking capabilities.

## Turn on AI Notes for chats and meetings

As an admin, you control whether AI Notes is available to your entire organization or to a certain group of users.

AI Notes is blocked to users by default. To turn on AI Notes for users, complete the following steps:

### 1. Turn on AI Notes

XXX WHAT WILL BE THE STRING IN THE TEAMS ADMIN CENTER? XXX

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard) with your Teams admin credentials.
1. In the left rail navigation, select **Teams apps** > **Manage apps**.
1. In the apps list's search box, search for **AI Notes???**.
1. Select **AI Notes???** from the app list.
1. In the actions menu, select **Allow**.
1. In the **Allow app?** pop-up, select the **Allow** button.
    1. AI note-taking is turned on when **AI Notes???** is turned on.

For more information about managing apps in Teams, see [Manage apps](manage-apps.md).

### 2. Allow AI Notes for a group of users

To allow AI Notes for users, a new app policy needs to be created and then assigned to users.

Follow the instructions at [Use app permission policies to control user access to apps](teams-app-permission-policies.md) to create a new app policy for AI Notes.

You can then assign the policy to your entire tenant or to a select group of users. Follow the instructions at [Add or modify app availability for users](/microsoftteams/app-centric-management#add-or-modify-app-availability-for-users) to assign the policy to users.

### 3. Turn on Loop experiences in Teams for meeting AI notes

Loop experiences in Teams need to be turned on in order for Copilot to generate notes in Teams meetings.

To turn on Loop experiences in Teams, follow the instructions at [Settings management for Loop functionality in Teams](/microsoft-365/loop/loop-components-configuration#settings-management-for-loop-functionality-in-teams).

## Related articles

- [What is responsible AI?](https://support.microsoft.com/topic/what-is-responsible-ai-33fc14be-15ea-4c2c-903b-aa493f5b8d92)
- [Frequently asked questions: AI, Microsoft Copilot, and Microsoft Designer](https://support.microsoft.com/topic/frequently-asked-questions-ai-microsoft-copilot-and-microsoft-designer-987b275d-f6f2-4d5d-94c5-e927cffae705)
- [Providing feedback about Microsoft Copilot with Microsoft 365 apps](https://support.microsoft.com/topic/providing-feedback-about-microsoft-copilot-with-microsoft-365-apps-c481c26a-e01a-4be3-bdd0-aee0b0b2a423?ocid=CopilotLab_SMC_Privacy_Feedback)
