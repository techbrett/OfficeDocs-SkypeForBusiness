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

This experience is supported in the Planner app on Teams web, desktop, and mobile. You can update any Teams app to create these app-powered tasks and provide tailored task experiences.  

## Requirements

App-powered tasks is an extensibility feature that relies on programmatic creation and management of task. Here are the requirements to use this feature in your organization.

- Each app-powered task must have a reference link that points to an experience in a destination Teams app. It's recommended to point this reference link to the specific item or screen the user should be working on. This reference link must be added to the task in a specific way.
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

## Add the destination link

## Related articles
  
- [Manage the Planner app for your organization in Microsoft Teams](manage-planner-app.md)
