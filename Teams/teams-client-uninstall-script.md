---
title:  Uninstallation script for the classic Teams client
ms.author: heidip
author: MicrosoftHeidi
manager: jtremper
ms.topic: article
ms.date: 11/07/2024
ms.service: msteams
audience: admin
ms.collection: 
- M365-collaboration
- m365initiative-deployteams
ms.reviewer: asgupta
search.appverid: MET150
f1.keywords:
- NOCSH
description: Documenting a downloadable uninstall script for the classic Teams client which allows you to manually shut off and remove the classic Teams client after moving to the new Teams client on non-VDI devices.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Uninstall the classic Teams client using a script

Microsoft has an [uninstallation script](https://download.microsoft.com/download/9/2/e/92e3b1f4-4c7e-4c93-9c8e-3df82a369333/UninstallClassicTeams.ps1) designed to uninstall the classic Teams client from all user profiles found on devices in your organization. This applies to all devices apart from VDI. If the classic Teams client is running for any user on the machine at the time the script is run, this script also ends the existing classic Teams running instance.

## Using the script

### Running the script on a single device

If you want to have the uninstallation script run for a single device, run it on that device. After you run the script, the classic Teams client is uninstalled from all user profiles of the specified device.

## Running the script with device management software

If you need to have this uninstallation script run across all devices in your organization, run this script using device management software, like Intune. We have [sample instructions](https://github.com/microsoft/MDE-PowerBI-Templates/blob/master/ASR_scripts/AddShortcuts_with_Intune.md) for running the script in Intune.

If the script is run in Intune or other device management software:

- Admins get results in the form of .JSON that indicates different parameters, like how many instances of classic Teams there are, how many have been uninstalled from devices, and so on.
- Admins can download these results as a .CSV file.

> [!NOTE]
> After the uninstallation of classic Teams, new Teams and Teams meeting add-in (TMA) might not work together. See [this article](/microsoftteams/troubleshoot/meetings/teams-meeting-add-in-missing#cause) for more information.

### Teams meeting add-in issue resolution

Microsoft has [an additional script](http://download.microsoft.com/download/9/2/e/92e3b1f4-4c7e-4c93-9c8e-3df82a369333/DetectAndUninstallTMA.ps1) to deal with issues such as the TMA problem mentioned previously. This script needs to be deployed in a user context through Intune or some manageability software, and run periodically to address any issues as they occur.

> [!NOTE]
> If the new Teams client is running and the TMA issue is detected by this script, it can't uninstall TMA at that time, as the process is running. Periodically running the script increases the chances of it running at a time when the new Teams client is not active.
