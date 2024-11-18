---
title: What are Communications Credits?
ms.author: danismith
author: DaniEASmith
manager: jtremper
ms.reviewer: dachocro
ms.date: 11/18/2024
ms.topic: conceptual
ms.assetid: 524dbea7-117f-493d-8005-6461f7f10059
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
audience: Admin
appliesto: 
  - Skype for Business
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
- CSH
ms.custom: 
  - Licensing
  - admindeeplinkMAC
  - admindeeplinkTEAMS
description: Learn about Communication Credits funding, how to find rates, and which services you receive.
---

# What are Communications Credits?

Communications Credits pay for Audio Conferencing and Calling Plan minutes. They ensure your users are never caught without being able to:
  
- Add toll-free numbers to use with Audio Conferencing meetings, auto attendants, or call queues.
  - Toll-free calls are billed per minute and require a positive Communications Credits balance.
- Dial out from an Audio Conference meeting to add someone else from anywhere in the world.
- Dial out from an Audio Conference meeting to their mobile phone with the Microsoft Teams app to destinations that aren't already included in their subscription.
- Dial any international phone number when they have a **Domestic Calling Plan** subscription.
- Dial international phone numbers beyond what is included in a **Domestic and International Calling Plan** subscription.
- Dial out and pay per minute once they exhausted the monthly minute allotment.
- Dial out and pay per minute for all outgoing calls, if they have a **Pay-As-You-Go Calling Plan**.

To set up Communication Credits, see [Set up Communications Credits for your organization](set-up-communications-credits-for-your-organization.md).

## Can I use Communication Credits?

Not all customers can or should use Communication Credits. Here are a few reasons why you can't or shouldn't use Communication Credits.

### Call destinations are already included in your subscription

Outbound calls to some destinations may already be included in your Audio Conferencing or Calling Plan subscription. Check your subscription information for details before purchasing Communication Credits you don't need.
  
### Conflicting organization addresses

If your organization is located in a different region than the billing address of your Enterprise Agreement (EA), you might not be able to purchase Communications Credits.

If you're unable to purchase Communications Credits, open a support ticket from the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2166757), and we can work with you to mitigate this issue until a permanent solution is in place.

### Customers with new commerce experience (NCE) calling subscriptions

The new commerce experience (NCE) allows customers to pay for services after the services were consumed, also known as post-usage billing.

Because Communication Credits are a prepaid budget to support outgoing minutes, they're not available to purchase for customers with NCE calling subscriptions.

For more information about the new commerce experience for calling subscriptions, see [Enable pay-as-you-go for your subscription](/microsoft-365/commerce/subscriptions/manage-pay-as-you-go-services) and [New commerce overage for telco pay-as-you-go](/partner-center/new-commerce-telco-payg).

> [!WARNING]
> NCE customers need to turn of Communication Credits automatic recharge. For instructions on how to turn off Communication Credits auto recharge, see [Turn off Communication Credits auto recharge for new commerce experience (NCE) customers](turn-off-communication-credits-auto-recharge-for-nce-customers.md).

### Your Calling Plan or Audio Conferencing plan is through a Cloud Solution Provider (CSP)

If you purchased your Calling or Audio Conferencing plan through a CSP, you can't acquire Communication Credits in the Microsoft 365 admin center.

To fund your Calling or Audio Conferencing plan with Communication Credits, directly purchase your Calling and Audio Conferencing plans from Web Direct or Volume License agreement (VL) channels.

## What are the Communications Credits rates?

See the cost of calls for Teams Calling Plans at [Cloud-Based Phone System for Voice Calling](https://go.microsoft.com/fwlink/p/?LinkId=799523) and scroll to the *See rates for where you want to call* section.
  
## Determine how many Communication Credits to purchase

If you choose to fund your Communications Credits balance with a one-time amount and then the balance falls to zero, most calling scenarios will no longer work, including toll-free phone numbers. As such, we recommend that you use the **Auto-recharge** setting to avoid any disruption of service should your Communications Credits balance reach 0 (zero). View your current Communication Credits balance by going to the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339) and selecting **Billing** > **Your products** > **Communications Credits**.
  
If you're ready to set up Communication Credits, see [Set up Communications Credits for your organization](set-up-communications-credits-for-your-organization.md).

### View your usage data in the Teams admin center

Each organization has different calling volumes and rates to consider. Retrieve your usage data from your third-party service provider. For organizations using Teams as their service provider, review your data by completing the following steps:

1. Sign in to the [Teams admin center](https://go.microsoft.com/fwlink/p/?linkid=2066851).
1. In the left navigation menu, select **Analytics & reports** > **Usage reports**.
1. On the **Usage reports** page, select **PSTN and SMS (preview) usage** from the **Report** dropdown menu and a date range to review.
1. Select the **Run report** button.
  
This report lets you export the call data records to Excel and create custom reports.

For more information about Teams usage reports, see [Teams PSTN usage report](teams-analytics-and-reports/pstn-usage-report.md).

## Who receives notifications about Communication Credits statuses?

Important notifications related to the Communication Credits status of your organization are sent to the following admins:

- Application Administrator
- Authentication Administrator
- Azure AD Joined Device Local Administrator
- Billing Administrator
- Cloud Device Administrator
- Company Administrator
- Device Administrator
- Global Administrator
- Helpdesk Administrator
- License Administrator
- Lync Service Administrator
- Privileged Authentication Administrator
- Service Support Administrator
- Skype for Business Administrator
- Teams Administrator
- Teams Communications Administrator
- Teams Communications Support Engineer
- Teams Communications Support Specialist
- User Account Administrator
- User Administrator

These notifications include when transactions succeed, when recharge transactions fail (such as an expired credit card), and when the Communications Credits balance reaches 0 (zero).
  
## Want to know about plans and pricing?

You can see the plans and pricing by visiting one of the following links:
  
- [Calling Plans](https://go.microsoft.com/fwlink/?linkid=799761)
- [Audio Conferencing](https://go.microsoft.com/fwlink/?linkid=799762)
- [Phone System](https://go.microsoft.com/fwlink/?linkid=799763 )

You can also see information about pricing by [signing in to the Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339) and going to **Marketplace**.
  
To see a table with the licenses you need for each feature, see [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md).

## Related articles

- [What are Communication Credits?](what-are-communications-credits.md)
- [Turn off Communication Credits auto recharge for new commerce experience (NCE) customers](turn-off-communication-credits-auto-recharge-for-nce-customers.md).
