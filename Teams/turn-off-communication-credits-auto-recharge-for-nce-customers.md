---
title: Turn off Communication Credits auto recharge for New Commerce Experience Customers
ms.author: danismith
author: DaniEASmith
manager: jtremper
ms.reviewer: dachocro
ms.date: 11/12/2024
ms.topic: article
ms.assetid: 691c9301-1f66-41fe-9b2c-ca24ae987463
ms.tgt.pltfrm: cloud
audience: admin
ms.service: msteams
search.appverid: MET150
ms.collection:
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
appliesto: 
  - Skype for Business
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
 - CSH
ms.custom:
  - Licensing
  - admindeeplinkMAC
description: Learn how to turn off Communication Credits automatic recharge if you're a new commerce experience (NCE) customer.
---

# Turn off Communication Credits auto recharge for new commerce experience (NCE) customers

The new commerce experience (NCE) allows customers to pay for services after the services have been consumed, also known as post-usage billing.

Because Communication Credits are a pre-paid budget to support outgoing minutes, they're not available to purchase for customers with NCE calling subscriptions.

Instead, NCE customers pay for outgoing minutes after they've used them. There's no need for a pool of Communication Credits.

- For more information about the new commerce experience, see [Enable pay-as-you-go for your subscription](/microsoft-365/commerce/subscriptions/manage-pay-as-you-go-services).
- To learn how to check if your tenant is on the NCE, see [New commerce overage for telco pay-as-you-go](/partner-center/new-commerce-telco-payg).

Most customers not using the NCE have the *Automatic Top Up* (ATU) flag enabled within their account. The ATU flag automatically refills your Communications Credit balance to the threshold you selected.

When switching to NCE, you need to disable this ATU option. Otherwise, the Communications Credit balance indefinitely refills itself, and the commerce system doesn't switch to the post-usage mechanism under NCE.

If you're moving to NCE, turn off automatic recharge by completing the following steps:

1. Sign into the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339) with your admin credentials.
1. In the left navigation menu, navigate to and select **Your products**.
1. Select **Communication Credits** in your listed products.
1. On the **Communication Credits** page, find the section titled **Billing settings** and select **Edit auto recharge settings**.
1. On the **Auto-recharge settings** page, uncheck the box next to **Auto recharge**.
1. Select the **Save** button.

When this process is complete, you can transition to NCE before your Communications Credit balance is empty. Even as an NCE customer, the commerce system consumes your Communications Credit balance prior to changing to post-usage billing. There's no extra action needed by you to ensure this switch happens.

## Related articles

- [What are Communication Credits?](what-are-communications-credits.md)
- [Set up Communication Credits for your organization](set-up-communications-credits-for-your-organization.md)
