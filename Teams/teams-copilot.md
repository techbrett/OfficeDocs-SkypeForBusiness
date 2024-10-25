---
title: Copilot in Microsoft Teams
author: MicrosoftHeidi
ms.author: heidip
manager: jtremper
ms.reviewer: andrewklutz
ms.date: 11/15/2024
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
ms.collection: 
  - M365-collaboration
f1.keywords:
- NOCSH
appliesto: 
  - Microsoft Teams
ms.localizationpriority: high
search.appverid: MET150
description: Learn about Copilot in Microsoft Teams
---

# Copilot in Microsoft Teams

XXX COPILOT FOR TEAMS, OR TEAMS COPILOT? TARGET THE NAME

Teams Copilot is a collaborative meeting agent available to you and your team to use in meeting scenarios. It combines the power of large language models (LLMs) with Teams data to provide summaries and answer questions in real-time to help you stay productive in the work place.  

- Chat
- Meetings

XXX DISTILLED FROM THE SPEC:

Microsoft Teams is introducing Copilot to provide a shared summary, or a synthesis, of a of the most important information in a single mode (one chat, channel post, or meeting). Information from that mode is synthesized into a shared canvas, which keeps everyone in the mode on the same page as the conversation happens. Users focus on communicating naturally and Team Copilot synthesizes that communication into output. Team Copilot is an active synthesis of ongoing work.

Most importantly, Copilot for Teams provides users with key insights from the chat without the user having to ask Copilot for it. Currently, in order to get insights from Copilot, users need to either use a pre-built prompt or know what to ask. By having a pre-built synthesis, we make key information readily available for all users in the moment, without further action on their part.

Teams Copilot also continuously works as the chat progresses. Copilot is a shared view of the current state of the discussion, it ensures alignment across a group of collaborators. It shows options being considered and then replaces those with a single choice once the decision has been made.

> [!IMPORTANT]
> While this information is communally shared to appropriate participants, when individual users query Copilot in regard to this information, those queries and responses from Copilot remain private to that user.

## Defining synthesis

A synthesis of information refers to the process of combining multiple sources or pieces of data into a coherent and integrated whole. This can involve analyzing, summarizing, and organizing information in a way that highlights important insights and connections between different elements of communication.

The goal of information synthesis is to create a more complete and nuanced understanding of a topic or subject by pulling together diverse strands of evidence or perspectives.

## Prerequisites

Copilot for Teams requires a copilot license for all users (XXX is it a per-org license or a per-user license?). It also requires admins opt-in to turn on group copilot skills for copilot license users.

### Opt-in steps

XXX WHAT ARE OPT-IN STEPS

## Turn on Copilot for Teams for chats and meetings

- [Manage App](manage-apps.md).
  - Under **Teams Apps**, select **Manage Apps**.
  - Enter **Copilot** or **Teams Copilot**.
  - AI Notes is enabled when GCP is enabled. XXX WE NEED TO DEFINE GCP
- [App polices](teams-app-permission-policies.md) (for the whole tenant or select group of users).
  - Add to the specific set of users.
- Refer to video recording for more details. XXX WHAT VIDEO RECORDING?

## Security, Purview, and Privacy

XXX MORE NEEDED HERE.

GCP can use the same terms and conditions as PCP.

[End-user link.](https://support.microsoft.com/office/frequently-asked-questions-about-copilot-in-microsoft-teams-e8737767-4087-4ae6-b1d8-10264152b05a)
