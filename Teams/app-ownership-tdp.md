---
title: Ownership of apps in Developer Portal
author: ashishguptaiitb
ms.author: guptaashish
manager: prkosh
ms.topic: article
ms.service: msteams
audience: admin
ms.subservice: teams-apps
ms.date: 10/21/2024
ms.collection: 
- Teams_ITAdmin_Help
- M365-collaboration
search.appverid: 
f1keywords: 
description: 
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Manage Microsoft Teams app ownership in Developer Portal

App developers use [Developer Portal](/microsoftteams/platform/concepts/build-and-test/teams-developer-portal) to configure, distribute, and manage their Teams apps. Developers who create or import an app in Developer Portal becomes the owner of the app. An app owner can add other org users as owners as well.

An owner may leave the organization or can delete the app from the portal after the app is published. In such cases, a Global Administrator can help in the following ways:

* Take over the ownership of an app and add other developers as owners.
* Import the app if it was created outside of Developer Portal or was deleted from the portal.

This helps another developer to work on the app and manage it thereby maintaining business continuity.

## Admin takes ownership of a custom app

Your organization can use a custom app that is available just within your org and not on the Teams store. It is created for and managed within your org. Admins can take ownership of a custom app after it is removed from the portal.



## Admin takes ownership of a Store app

An org can publish its app to [Microsoft AppStore](https://appsource.microsoft.com) using Partner Center UI. The app may not be available in Developer Portal for one of the following reasons:

* The app was created using some other tools and not Developer Portal.
* The app was created using Developer Portal but was later removed from the portal.

In the above cases, you as an admin can reclaim the ownership of the app in Developer Portal by contacting Microsoft Support. To ascertain the ownership, provide a screenshot of the latest email exchange to publish the app. When they submitted the app, the submitter in your organization was contacted by Microsoft from `teamsubm@microsoft.com` email ID to let them know that their app was published on the AppStore.

## Considerations and limitations

Know the following limitations about this functionality:

* 

## Related articles

* [Know about Developer Portal](/microsoftteams/platform/concepts/build-and-test/teams-developer-portal).
* [Developer Portal Teams app](https://teams.microsoft.com/l/app/14072831-8a2a-4f76-9294-057bf0b42a68).
