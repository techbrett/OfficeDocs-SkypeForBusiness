---
title: Manage Cloud Voicemail settings
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: jenstr
ms.date: 05/21/2021
ms.topic: article
ms.assetid: 9c590873-b014-4df3-9e27-1bb97322a79d
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - Tier1
audience: Admin
appliesto: 
  - Skype for Business
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords: 
  - CSH
ms.custom: 
  - Phone System
description: Manage Voicemail settings for your users.
---

# Manage Cloud Voicemail settings for users

Voicemail settings allow you to configure voicemail settings for individual users.

Before configuring voicemail settings for your users, you should read [Set up Cloud Voicemail](set-up-phone-system-voicemail.md). For information about setting policies for groups of users, see [Manage Voicemail policies](manage-voicemail-policies.md).

The default settings for Cloud Voicemail are:

- Voicemail is enabled.
- The prompt language is set to the user’s preferred language.
- The out-of-office greeting is disabled.
- The out-of-office greeting, when automatic replies are set in Outlook, is disabled.
- The out-of-office greeting, when the calendar in Outlook shows out-of-office, is disabled.
- Sharing of voicemail and transcription data with the service for training and improving accuracy purposes is disabled.
- The call answering rule is set to Regular Voicemail.
- The default greeting prompt overwrite isn't set.
- The default out-of-office greeting prompt overwrite isn't set.
- The transfer target isn't set.
- Play out-of-office greetings is disabled.

To manage Cloud Voicemail features for your users, you can use the Teams admin center or PowerShell. Your end users can also configure these settings in the Teams client by going to **Settings -> Calls -> Configure Voicemail.**

## Use Teams admin center

In the Teams admin center:

1. In the left navigation, go to **Users > Manage users** and select the user.

2. On the user details page, go to the **Voicemail** tab.

3. Change the settings.

4. Select **Save**.

## Use PowerShell

You can also use PowerShell to manage voicemail settings as follows:

- To manage Cloud Voicemail settings for individual users, use the  [Set-CsOnlineVoicemailUserSettings](/powershell/module/teams/set-csonlinevoicemailusersettings) cmdlet.

- To view settings, use the [Get-CsOnlineVoicemailUserSettings](/powershell/module/teams/get-csonlinevoicemailusersettings) cmdlet.

- You can disable Cloud Voicemail for a user by using the [Set-CsOnlineVoicemailUserSettings](/powershell/module/teams/set-csonlinevoicemailusersettings) cmdlet and setting the VoicemailEnabled parameter to $false.

## Voicemail settings

- **Voicemail  ** - This setting controls whether Cloud Voicemail is enabled for the user. If the setting is false, Cloud Voicemail service isn't available for the user, and a voicemail isn't recorded for the user.
- **Prompt language** - This setting specifies the language used for the prompts in the Cloud Voicemail. For more information, see [Change the default language for greetings and emails](change-the-default-language-for-greetings-and-emails.md).
- **Call answering mode** - This setting specifies the call answering rule. The rule can be:
  - Caller can leave a voicemail
    - The relevant greeting (normal or out-of-office) is played and the caller can leave a voicemail.
  - Play an outgoing message to the caller
    - Only the relevant greeting (normal or out-of-office) is played. The caller can't leave a voicemail.
  - Service declines the call with no message
    - The system disconnects the caller.
- **Call transfer** - Specifies the user or phone number that the caller is transferred to.
- **Default greeting prompt** -  specifies the text-to-speech greeting that is played in case the user hasn't recorded a greeting.
- **Default out-of-office prompt** - specifies the text-to-speech greeting that is played in case the user is out-of-office and hasn't recorded an out-of-office  g
- **Play out-of-office greetings** - specifies whether to play out-of-office greeting in voicemail deposit scenario when user set automatic replies in Outlook.
- **Share data for service improvements** (PowerShell only) - Specifies whether voicemail and transcription data is shared with the service for training and improving accuracy. If set to false, voicemail data isn't shared, regardless of user choice.
