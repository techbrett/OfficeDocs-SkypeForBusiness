---
title: Create app-powered tasks in Planner for tailored task experiences
author: lana-chin
ms.author: v-chinlana
manager: jtremper
ms.topic: conceptual
ms.service: msteams
ms.reviewer: andfried
ms.date: 
search.appverid: MET150
searchScope: 
  - Microsoft Teams
audience: admin
description: 
ms.localizationpriority: medium
appliesto: 
  - Microsoft Teams
ms.collection: 
- M365-collaboration
- m365-frontline
- teams-1p-app-admin
- highpri
---

# Create app-powered tasks in Planner for tailored task experiences

## Overview

The app-powered tasks feature offers your organization more control over what users see when they open their tasks in the Planner app within Microsoft Teams. Instead of showing only the standard set of task fields, you can provide users with an experience tailored to the task at hand. That experience might be a workflow-specific set of fields or step-by-step guidance to walk the user through a workflow from beginning to end. To achieve this, you integrate a Teams app with the task and create these tasks programmatically.

Here's an example scenario.

Users in your organization use a Teams app to track and complete inspections. You choose to integrate this inspections app with tasks so that a Planner task is created for each inspection tracked in the system.

 -  When a user opens one of these tasks from the Planner app in Teams, they see a simplified screen with a button to jump directly to the inspection experience powered by your inspections app. 
- When they complete the task and exit the inspections experience, they’re right back in Planner where they started. 

Users get the tailored experience that a Teams app provides right from within their assigned tasks. They don’t have to navigate to a different app to get work done.

In addition to these benefits when users complete tasks, the app-powered tasks feature allows organizations to reflect required line-of-business (LOB) processes and workflows as tasks, so employees can see all tasks assigned to them from a single place.

This experience is supported in the Planner app on Teams web, desktop, and mobile. You can update any Teams app to create these app-powered tasks and provide tailored task experiences.  

## Requirements

App-powered tasks is an extensibility feature that relies on programmatic creation and management of task. Here are the requirements to use this feature in your organization.

- Each app-powered task must have a reference link that points to an experience in a destination Teams app. It's recommended to point this reference link to the specific item or screen the user should be working on. This reference link must be added to the task in a specific way. To learn more, see [Add the destination link](#add-the-destination-link).
- Tasks must be created and updated using the [business scenarios](/graph/api/resources/businessscenario-planner-overview?view=graph-rest-beta) API in Microsoft Graph.
  - Users who need to work with the task must have access to the destination app in Teams, as governed by the app policies you set in the Teams admin center. To learn more, see [Overview of app management and governance in Teams admin center](manage-apps.md).
- The destination Teams app is responsible for managing the task lifecycle, which includes the following actions:

  - Create the task. See [Create businessScenarioTask](/graph/api/businessscenarioplanner-post-tasks?view=graph-rest-beta).
  - Assign the task. See [Update businessScenarioTask](/graph/api/businessscenariotask-update?view=graph-rest-beta).
  - Update the task, if properties change. See [Update businessScenarioTask](/graph/api/businessscenariotask-update?view=graph-rest-beta).
  - Mark the task as Completed when all steps are done. See [Update businessScenarioTask](/graph/api/businessscenariotask-update?view=graph-rest-beta).
  - Delete the task. See [Delete businessScenarioTask](/graph/api/businessscenarioplanner-delete-tasks?view=graph-rest-beta).

### Why does the app need to manage the task lifecycle?

Some workflows might not have deterministic flows. For example, a finding during an inspection might result in the inclusion of several more steps in the inspection. The Planner app can’t determine whether all required steps are completed, so we designed this feature to allow your app to govern the lifecycle of the task. Similarly, we prevent users from updating task fields or marking the task complete, which might otherwise result in users making changes that conflict with what’s reflected in your Teams app.

## Create an app-powered task

<!--the main thing that differentiates is the prescense of a specific attachment.-->

### Add the destination link

The Planner app depends on the presence of a link to the destination app as a specific type of attachment, which allows Planner to recognize the task as an app-powered task. Note that the API refers to task attachments as [references](/graph/api/resources/plannerexternalreferences?view=graph-rest-beta).

When you specify the attachment, define the following fields:

- URL that uses the Teams modal stage view link syntax.

- **alias**: The name of your app. When a user opens the task, they see a message that says, “Complete this task in <**alias**> and a **Start here** button to jump to the destination experience.

- **previewPriority**: Leave as **!**.

- **type**: Set to **TeamsHostedApp**.

### How to format the reference link to the destination experience - here what this looks like in more detail. 

The reference URL to the destination experience must follow the [stage view syntax](/microsoftteams/platform/tabs/open-content-in-stageview) using the following format:

`https://teams.microsoft.com/l/stage/{Teams-app-Id}/0?context={"contentUrl":"URL-to-destination-experience","name":"{desired-page-title}","openMode":"modal"}`

Specify the following properties in the reference URL:

- `Teams-app-Id`: The app ID of the Teams app you're integrating with the task.
- `contentUrl`: The URL that points to the specific experience in your destination Teams app that you want users to see when they open the task. The domain of the URL must be a valid domain for the app ID.
- `name`: The title that should appear at the top of the screen when the user is shown the contentURl.

```http
        "references": { 
            "reference-URL-as-constructed-above": { 
                "@odata.type": "microsoft.graph.plannerExternalReference", 
                "alias": "{destination app name}", 
                "previewPriority": " !", 
                "type": "TeamsHostedApp" 
            } 
        } 
```
Here's an example of a reference URL before encoding:

`https://teams.microsoft.com/l/stage/com.microsoft.teamspace.tab.youtube/0?context={"contentUrl":"https://tabs.teams.microsoft.com/youtubeContentStage?videoId=HBGmSy1iVmY","name":"Security%20talk","openMode":"modal"}`

In this example:

- `Teams-app-Id` is the app ID of the YouTube app in Teams (`com.microsoft.teamspace.tab.youtube`). Keep in mind that most Teams app Ids are alphanumeric and might look different.
- `contentUrl` points to the experience within the destination Teams app (`https://tabs.teams.microsoft.com/youtubeContentStage?videoId=HBGmSy1iVmY`).
- `name` is the name of the screen title when loading the URL and `open Mode` is set to `modal`.

If the YouTube app in Teams is available to you, you can send this URL to yourself and confirm it opens.

You need to encode the reference URL before using it in the attachment. URL encoding ensure the link is in a compatible format for programmatic user. Follow these steps to encode the reference URL:

1. Encode the part of the URL that comes after `0?context=`. Do not encode `https://` or `=` (the equal symbol), or any of the text in between.

    `https://teams.microsoft.com/l/stage/com.microsoft.teamspace.tab.youtube/0?context=%7B%22contentUrl%22%3A%22https%3A%2F%2Ftabs.teams.microsoft.com%2FyoutubeContentStage%3FvideoId%3DHBGmSy1iVmY%22%2C%22name%22%3A%22Security%2520talk%22%2C%22openMode%22%3A%22modal%22%7D`

    > [!TIP]
    > This is the last step where the link can be easily validated in Teams chat. After you complete this step, you can test the URL by sending it to yourself in a Teams chat. The link should open on desktop, web, or mobile for any user who has access to the destination app in Teams.

2. Replace *all* `.` characters in the reference URL with `%2E`. You must do this across all characters in the reference URL, from beginning to end. If you miss this step, the reference URL might not work. 

    The following link is ready for programmatic use.

    `https://teams%2Emicrosoft%2Ecom/l/stage/com%2Emicrosoft%2Eteamspace%2Etab%2Eyoutube/0?context=%7B%22contentUrl%22%3A%22https%3A%2F%2Ftabs%2Eteams%2Emicrosoft%2Ecom%2FyoutubeContentStage%3FvideoId%3DHBGmSy1iVmY%22%2C%22name%22%3A%22Security%2520talk%22%2C%22openMode%22%3A%22modal%22%7D`

    > [!NOTE]
    > If your URL points to a Power App, make sure your URL includes the `&source=teamstab` parameter to make single sign-on (SSO) work for Power Apps and the `&skipMobileRedirect=1` parameter to skip the screen that prompts users to open the standalone Power App Player.

## Create an app-powered task

Here's an example of how to create an app-powered task using the [business scenarios](/graph/api/resources/businessscenario-planner-overview?view=graph-rest-beta) API.

```http
POST https://graph.microsoft.com/beta/solutions/businessScenarios/{your-business-scenario-ID}/planner/tasks 

{ 
    "title": "{Task title}", 
    "target": { 
        "@odata.type": "#microsoft.graph.businessScenarioGroupTarget", 
        "taskTargetKind": "group", 
        "groupId": "{Team ID / Group ID}" 
    }, 
    "businessScenarioProperties": { 
        "externalObjectId": "{any unique ID, e.g. ID of the object in your destination app}", 
        "externalBucketId": "{any bucketID from planConfiguration of your business scenario}" 
    }, 
    "assignments": { 
        "{user ID of user you want to assign the task to}": { 
            "@odata.type": "#microsoft.graph.plannerAssignment", 
            "orderHint": " !" 
        } 
    }, 
    "details": { 
        "references": { 
            "reference-URL-as-constructed-above": { 
                "@odata.type": "microsoft.graph.plannerExternalReference", 
                "alias": "{destination app name}", 
                "previewPriority": " !", 
                "type": "TeamsHostedApp" 
            } 
        } 
    } 
} 
```

## Related articles
  
- [Manage the Planner app for your organization in Microsoft Teams](manage-planner-app.md)
