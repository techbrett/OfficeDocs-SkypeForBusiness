---
title: Set up and manage speed dial keys on Teams phones
author: mstonysmith
ms.author: tonysmit
manager: pamgreen
ms.reviewer: prashibadkur
ms.date: 11/04/2024
ms.topic: article
audience: Admin
appliesto:
- Microsoft Teams
ms.service: msteams
ms.subservice: itpro-devices
ms.collection:
  - teams-rooms-devices
  - Teams_ITAdmin_Devices
  - Tier1
f1.keywords:
  - NOCSH
search.appverid: MET150
ms.localizationpriority: medium
description: Learn how to set up and manage line or speed dial keys on Microsoft Teams certified phones for quick access to custom contacts and speed dial.
---

# Line or speed dial keys on Microsoft Teams certified phones

This article provides you with guidance on setting up and managing line keys ( or speed dial keys) on Microsoft Teams certified phones. This feature allows your users to set up use a phone line key to set up speed dial for your contacts and phone numbers for quick access using buttons on nontouch devices and sidecars.

> [!IMPORTANT]
> This feature is only available on non touch Teams phones and not on touch-enabled Teams phones.

A phone line key is one of the keys used to designate individual lines on a phone. Depending on the model and manufacturer, phones typically have between two and 12 phone line keys.

## Line keys

## Steps to use line keys to set up speed dial

> [!IMPORTANT]
> With this update, you can use line keys to set up speed dial for contacts and phone numbers only.

To set up a line key for speed dial, follow these steps:

1. **Update the Teams phone to version 1449/1.0.94.2024101709** After updating the phone, you'll notice a new home screen experience on your device with a dedicated place for your line keys. To update your Teams phones, see [Update your phones remotely](remote-update-teams-phones.md).  Verify that you are running Android version 1449/1.0.94.2024101709 by going to 

:::image type="content" source="./media/nontouch-linekeys-empty.jpg" alt-text="Screenshot of a non touch phone with line keys." lightbox="./media/nontouch-linekeys-empty.jpg":::

2. **Assign a contact for speed dial:** Select on **Assign line key** and search for an existing contact including a PSTN contact, or add a new one.

:::image type="content" source="./media/nontouch-linekeys-assigned.jpg" alt-text="Screenshot of assigned line keys on a Teams phone." lightbox="./media/nontouch-linekeys-assigned.jpg":::

3. **Modify or manage an assigned line key:** Long press an existing line key to see a detailed menu with the following options:
    - **Unassign line key:** To remove an assigned line key.
    - **Reassign line key:** To modify the contact assigned to this line key.
    - **Manage line key:** Access more management options.
1. **Place a call:** Press or select on the key to place a call to the user or number assigned to that line key.

## Frequently Asked Questions

**Question:** When will line keys be supported on touch phone devices?  
**Answer:** Support for touch phone devices is coming soon. Check the public roadmap for timelines. With this application update, line keys are available for nontouch devices and devices with sidecars.

**Question:** Can line keys be configured on the Teams Admin Center with this update?  
**Answer:** No, currently configuration support is only through the device.

**Question:** What other functions can I perform using line keys?  
**Answer:** With this update, you can use line keys for quick access to speed dial only. In the future, we'll support line keys for call controls and offer enhancements for shared line configuration.

**Question:** Does this change the existing functionality of sidecars?  
**Answer:** Before the Teams application update to 1449/1.0.94.2024101709, users were able to add contacts to sidecars if the account was marked as a Favorite, speed dial, or assigned as a Boss. Additionally, users had the option to pin groups to sidecars. With this update, contacts on sidecars can only be added by configuring them as line keys on the sidecar. Saved configurations continue to appear on the sidecar with this app. Any further edits will only happen through line key management as described above. We'll make changes to streamline this experience on sidecars in the future.

### Related Links

- [Microsoft Certified Teams phones](../devices/teams-phones-certified-hardware.md)
- [Phones for Microsoft Teams](phones-for-teams.md)
- [Microsoft Teams Phone Settings](/microsoftteams/phones-settings)