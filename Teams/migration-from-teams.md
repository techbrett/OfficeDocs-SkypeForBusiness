---
title:  Migration from Microsoft Teams
ms.author: heidip
author: MicrosoftHeidi
manager: jtremper
ms.topic: article
ms.date: 12/05/2024
ms.service: msteams
audience: admin
ms.collection: 
- M365-collaboration
- m365initiative-deployteams
ms.reviewer: 
search.appverid: MET150
f1.keywords:
- NOCSH
description: Guidance on data export when migrating from Microsoft Teams to a third-party application.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Export options for migration from Teams

Microsoft supports customer choice, including the choice to migrate your data away from Teams. Teams now offer a 90-day free exit for customers who are leaving Teams and taking their data out to switch to a third-party. This allows for unlimited exports within that period. For small and medium-sized customers (up to 500 employees), see the [Prerequisites to access the Teams data export tool](#prerequisites-to-access-the-teams-data-export-tool) section. For large enterprise customers, refer to [Prerequisites to access the Teams export APIs](#prerequisites-to-access-the-teams-export-apis).

## Essential requirements and access guidelines for the Teams data export tool

Use the following steps to submit your request for a one-time free exit from Microsoft Teams:

### Prerequisites to access the Teams data export tool 

1. To migrate out of Microsoft Teams and access the tool, select [this link](https://aka.ms/AccessTeamsDataExportTool) to contact support.
1. Choose your preferred method of contact: email or phone. Make sure to have the following information ready.
    1. Title: Use a predefined title.
    1. Description: Provide an estimate of the size of your tenant and why you want to move your data.
1. Wnen we receive your request we begin the evaluation process and notify you when you can access the tool.

### Access the Teams data export tool

Migrating data involves sensitive content. Note the following:

- **Access role**: As it contains sensitive data, you will need to login to the Teams Admin Center as the global administrator to access it
- **Duration**: You can use the tool for up to 90 days.
- **Download window**: After the data is prepared, you’ll download a ZIP file with a series of JSON files. When the download link becomes available, you have 24 hours to download it.

> [!NOTE]
> When you start exporting data or when an export is in progress, any new data created after that isn't included. To capture the content that isn't included, you can do another export within 90 days.

### What the Teams data export tool supports

Teams data export tool allows you to export the following from Microsoft Teams:

- 1:1 chats
- Group chats
- Meeting chats
- Channel messages

To learn more about what's supported, see [Export content with the Microsoft Teams Export APIs](export-teams-content.md) for more information.

The Teams data export tool also supports the following data:

- **Team and Channel structure**: The Teams data export tool supports the Team and Channels structure. Channels are specific collaboration spaces within a Team where members can focus on topics, projects, or departments.
- **User/Roster**: The Teams data export tool supports exporting the list of users who are part of a specific team or channel, including details about each user’s roles.
- **Apps**: The Teams data export tool supports exporting the list of installed apps for a channel.

### What the Teams data export tool doesn't support

- **Teams Copilot Interactions and Microsoft 365 Chat**: The Teams data export tool doesn't support user-to-Copilot interaction messages and Microsoft 365 chat messages sent by the bot.

### What the ZIP file includes

|File name |Note |Public documentation |
|----------|-----|---------------------|
|/users/usersList.json |List of all users with user details |[List users](/graph/api/user-list) |
|/users/{userId}/messages_{userId}.json |List of messages for a user |[chats: getAllMessages](/graph/api/chats-getallmessages) |
|/users/{userId}/retainedMessages_{userId}.json |List of edit message history of a user |[chat: getAllRetainedMessages](/graph/api/chat-getallretainedmessages) |
|/users/{userId}/meetings_{userId}.json |List of meetings user is part of |[List events](/graph/api/calendar-list-events) |
|/users/{userId}/meetingRecordings_{userId}.json |List of meeting recordings links organized by a user |[onlineMeeting: getAllRecordings](/graph/api/onlinemeeting-getallrecordings) |
|/users/{userId}/meetingTranscripts_{userId}.json |List of meeting transcript links organized by a user |[onlineMeeting: getAllTranscripts](/graph/api/onlinemeeting-getalltranscripts) |
|/teams/teamsList |List of teams |[List groups](/graph/api/group-list) |
|/teams/teamsSettings |Team settings of all teams |[Get team](/graph/api/team-get) |
|/teams/{teamId}/teamMembers_{teamId}.json |List of members of a team |[List members of team](/graph/api/team-list-members) |
|/teams/{teamId}/messages_{teamId}.json |List of messages for a team  |[channel: getAllMessages](/graph/api/channel-getallmessages) |
|/teams/{teamId}/retainedMessages_{teamId}.json |Message edit history of a team |[channel: getAllRetainedMessages](/graph/api/channel-getallretainedmessages) |
|/teams/{teamId}/teamInstalledApps_{teamId}.json |List of installed apps of a team |[List apps in team](/graph/api/team-list-installedapps) |
|/teams/{teamId}/groupEvents_{teamdId}.json |List of meetings for a team |[List calendarView](/graph/api/calendar-list-calendarview) |
|/teams/{teamId}/channels_{teamId}.json |List of channels for a team |[List allChannels](/graph/api/team-list-allchannels) |
|/teams/{teamId}/channels/{channelId}/channelMembers.json |List of members of a channel (this will be only available for shared and private channels, standard channel members are same as team’s member) |[List members of a channel](/graph/api/channel-list-members) |

## Prerequisites to access the Teams export APIs

1. To migrate out of Microsoft Teams and get access to the APIs free of charge, select [this link](https://aka.ms/AccessTeamsDataExportTool) to contact support.
1. Choose your preferred method of contact: email or phone. Make sure to have the following information ready.
    1. Title: Use a predefined title.
    1. Description: Provide information on why you want to move your data.
1. Wnen we receive your request we begin the evaluation process and notify you when you can access the APIs with no cost.

### Access the Teams Export APIs

Please refer to this article: Export content with the Microsoft Teams Export APIs.
