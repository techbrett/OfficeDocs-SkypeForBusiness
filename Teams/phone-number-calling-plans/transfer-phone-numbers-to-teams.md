---
title: Transfer phone numbers to Microsoft Teams
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: leiaglezer
ms.date: 11/22/2024
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
f1.keywords:
- NOCSH
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
search.appverid: MET150
description: Learn how to use the porting wizard to transfer your phone number from your current service provider to Microsoft Teams.
ms.custom: seo-marvel-mar2020
---

# Transfer phone numbers to Microsoft Teams

This article is for administrators and IT professionals and applies to Microsoft Teams Calling Plans and services. The article describes how to transfer phone numbers from your current service provider to Microsoft Teams.

To transfer your phone numbers, you can use the porting step-by-step guide in the Microsoft Teams admin center. After you port your phone numbers to Teams, Microsoft becomes your service provider.

Before you start, review prerequisite knowledge referenced in the following articles:

- [What's a port order](port-order-overview.md)
- [How many phone numbers can you get?](../how-many-phone-numbers-can-you-get.md)
- [Country or region specific articles](../manage-phone-numbers.md).

> [!NOTE]
> If you have more than 999 phone numbers that you need to transfer to Teams in one port request, do not use the port wizard. Navigate to the [Phone Number Service Center portal](https://pstnsd.powerappsportals.com/create-ticket/) and create/submit a new "Port in" case with the [Telephone Number Services (TNS) - Service Desk](https://learn.microsoft.com/microsoftteams/phone-reference/manage-numbers/contact-tns-service-desk).

Microsoft's Telephone Number Service Center completes ports orders only on United States business days and not on public holidays or weekends.

## Create a port order and transfer your phone numbers to Teams

1. In Teams admin center, launch the port wizard
    - In the left navigation rail, go to **Voice** > **Phone numbers**. Select the section tab for **Numbers**, and then from the table's header-menu select the word **Port**.

### Get started

On the **Get started** page, populate the fields per your request.

**Country or region**: Country or region where you're porting numbers.

**List your phone number** Add your phone numbers manually or by uploading a list.

- To add phone numbers manually, enter numbers in 10-digit or E.164 format, separated by a comma or semi-colon. Ranges aren't supported. Optional dashes or hyphens are supported.
- To upload a list of phone numbers, the list must be in CSV format and must have only one column with a header designated as PhoneNumber. Each phone number must be in a separate row and can be in 10-digit or E.164 format.

### Manage numbers

The Manage numbers page provides an initial check to make sure the number format is recognized by the wizard, matches the country or region you specified, and is a valid number.

If the number validation summary isn't successful, view the details to understand the reason.

- Click on **View details** in the Number validation summary, or click on the red text in the summary below **Validation status** to check the reasons for phone number failure.

- If failure is not understood, you may create a case with the TNS-Service Desk team through the [Phone Number Service Center portal](https://pstnsd.powerappsportals.com/create-ticket/).

The Number validation summary must indicated all numbers are valid before the wizard can continue.
If there are no errors, continue.

### Add account information

On the **Add account information** page, complete the following, and then select **Next**.
>
> [!NOTE]
> The information displayed on this page is determined by the country or region and number type. Each country and region has different regulations on the information that's required to port numbers. What you see on this page may be different from what's described here.

1. **Order details**:

The order details are where you input required information for your port request.

The order name you specify here becomes viewable by you in the Teams Admin Center during the porting process and after order completion for your records.

1. **Port details**, enter the Billing Telephone Number (BTN) in E.164 format.

    - If you enter a BTN number that isn't in the list of numbers that you're porting, your request is automatically categorized as a **Partial port** and the BTN will remain with your current service provider after the port is complete.
    - If you enter a BTN number that matches a number in the list of numbers that you're porting, you have two options.

        - Port **all numbers in my account**. If you choose this option, the account with your current service provider will be closed after the port is complete.
        - Port **some numbers in my account, and I'm including my account's BTN**. If you choose this partial port option, you can enter a new BTN to designate for the account that is still open with your current service provider.

> [!NOTE]
> All information input for your organization and current service provider must match *exactly* with the current service provider's records.
>
> Some fields are optional, but some service providers require the optional fields.
>
> This is dependent upon the current service provider. For example, PIN is required to port mobile numbers.

1. **Organization details**, enter your organization's name.

1. **Current service provider details**, provide the current service provider's name, account number, and security PIN.

1. **Requester details**, populate this information with the contact details of the person who Microsoft can contact with port order status updates.

1. **Authorized user details**, populate this information with the contact details of the person who is the authorized user with your current service provider.

1. **How do you want to sign the Letter of Authorization?** section, you select whether you want e-signature or manual upload for the Letter of Authorization.

1. **Service address**, assign the default emergency address for the numbers.

1. **Default number usage** section, you select the intended typed of usage for the numbers. If you would like to change it, select *Yes, change usages* to go to **Add number features** page. If you select *No*, the wizard skips you to the **Complete your order** page.

### Add number features

The add number features page is where you update the number usage. Usage is a category of service for the phone numbers.

- For numbers assigned to users, the default number type is geographic phone numbers and is listed as **User**.

- For numbers assigned to voice applications, such as Auto-Attendants and Call Queues, the number usage type should be set as **Voice app**.

- For numbers assigned to audio conferencing, the number usage type should be set to **Conference**.

Toll-free numbers default to **Voice app**, but you can make changes to the default number usages in this section of the wizard.

To update the number usage, check the desired number and select **Update number usage**. Then, from the right-hand side rail, use the drop-down and select your desired number usage to assign to the numbers.

### Complete your order

- If you selected **Paper signature** in the **Add account information** page, you can download a Letter of Authorization template.

    - The template is prepopulated with the information you input in the wizard.
    - Once signed, you upload a copy of the signed Letter of Authorization and then you can select **Submit** and the port request proceeds.

- If you selected **E-signature** in the **Add account information** page, the authorized user receives an email to sign the Letter of Authorization once you select **Complete and send e-signature request**.

    - Once they electronically sign, the port request proceeds.

## What happens next

When we receive your port order, you'll receive an automated email that confirms your request. All port order status changes will generate automated email notifications to you about the order. If your port request is rejected by the carrier, if you need help with your port request, or if you have any questions about your port request, contact the [TNS Service Desk](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md) for assistance.

> [!NOTE]
> If you already have a case open with the TNS-Service Desk for your port request, update that existing ticket instead of creating a new case.

To view the status of your port order, in the left navigation of the Microsoft Teams admin center, go to  **Voice** > **Port orders**, and then select **Order history**. Each port order status is listed in the **Status** column. To learn more, see [What's the status of your port orders?](port-order-status.md)

## Report phone number issues

If you notice any issues with the ported numbers within the first 24-48 hours after the port is completed, contact the [TNS Service Desk](https://learn.microsoft.com/microsoftteams/phone-reference/manage-numbers/contact-tns-service-desk). For any issues beyond 48 hours, contact the Microsoft Support Team.

## Related articles

- [What's a port order?](port-order-overview.md)
- [Different kinds of phone numbers used for Calling Plans](../different-kinds-of-phone-numbers-used-for-calling-plans.md)
- [Manage phone numbers for your organization](../manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md)
- [Emergency calling terms and conditions](../emergency-calling-terms-and-conditions.md)
- [Emergency Calling disclaimer label](https://download.microsoft.com/download/9/9/0/990e24c1-eb49-4b52-9306-dbd4c864ed91/emergency-calling-label-(en-us)-(v.1.0).zip)
