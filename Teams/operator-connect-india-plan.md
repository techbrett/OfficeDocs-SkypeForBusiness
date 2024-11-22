---
title: Plan for Operator Connect for India
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.date: 09/01/2023
ms.topic: article
ms.service: msteams
audience: admin
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
ms.reviewer: roykuntz
search.appverid: MET150
f1.keywords:
- NOCSH
description: Learn more about Operator Connect for India, such as requirements and planning for deployment.
ms.custom: 
 - seo-marvel-apr2020
 - seo-marvel-jun2020
appliesto: 
  - Microsoft Teams
---

# Plan Operator Connect for India

Operator Connect for India is a country-specific method for providing Public Switched Telephone Network (PSTN) connectivity to your tenant and PSTN access to Teams Phone users in India. Operator Connect for India is designed to support India’s telephony regulatory requirements and provide customers an alternative to Direct Routing. This article is intended to help IT pros and enterprise telecom admins.

## Prerequisite knowledge

- [PSTN connectivity options](pstn-connectivity.md)
- [Operator Connect as a PSTN connectivity option](operator-connect-plan.md)

## Overview

There are some helpful points to consider about telecommunications in India when planning your PSTN integration.

- India operators are approved to provide services in regional zones within India that loosely follow state boundaries. Regional zones are also known as geo-circles and calls within a region are considered intra-circle and calls from one India region to another India region are considered inter-circle.

- India operators can provide numbers that are categorized as either wireline numbers or wireless numbers. Each number type is designed to adhere to regulated policies that govern acceptable use of PSTN access. For example:

|**Number type**|**Access permissions**|
|:--- |:---: |
|Wireline numbers | Permitted to access PSTN only from their assigned region or geo-circle, collocated at a Network Communication Server (NCS) site that the operator associates with the number. |
|Wireless numbers | Permitted to roam and access PSTN from any region or geo-circle within India. |

>
> [!NOTE]
> Operator Connect for India wireless numbers aren't integrating with the user’s mobile phone SIM. Teams Phone Mobile is currently not supported in India.

It isn't possible to convert wireline numbers to wireless numbers.

Wireline and wireless numbers are for in-India-use only.

- Teams Phone users with an Operator Connect for India number who roam outside of India aren't allowed access to the PSTN.

Toll bypass isn't allowed for India wireline or wireless numbers.

- When a Teams user with a wireless or wireline number originates a call from within India to somebody outside of India, you must not reroute their call (for example, through your Teams VoIP network) to bypass the toll of the India telecom operator.

Given these considerations, Microsoft supports compliance for acceptable use of India wireline numbers in two ways:

|**Number type**|**Access control**|
|:--- |:---: |
|Wireline numbers | [Teams Location Based Routing](location-based-routing-india-plan.md) |
|Wireless numbers | [Location services](https://support.microsoft.com/windows/windows-location-service-and-privacy-3a8eee0a-5b0b-dc07-eede-2a5ca1c49088) in the operating system of the user’s device  |

The PSTN Access controls are automatically recognized in Teams Phone according to the number type provided by the India operator.

## Licensing, requirements, and considerations

You can integrate India wireless and wireline numbers into your tenant through a unique Operator Connect for India arrangement that delegates the PSTN integration and Teams Phone licensing to the India operator.

With Operator Connect for India:

- You need to acquire the India-specific Microsoft Teams Phone license from a licensed telecom operator in India. This requirement must be met even if you have an existing Teams Phone entitlement. For example, if you have a Teams Phone entitlement included with an E5 license, you still need to purchase an India-specific Microsoft Teams Phone license from your India operator.

  - The India Teams Phone license available from the India Operator Connect partners supports both India wireline and wireless numbers.
  - The India Teams Phone license supports the entitlement model for [Teams Phone Resource Account licenses](teams-add-on-licensing\virtual-user.md).

    - Resource accounts for Auto attendants and Call Queues can be assigned with Operator Connect for India numbers. The resource accounts are provisioned as described in [Plan for Teams Auto attendants and Call queues](plan-auto-attendant-call-queue.md), and don't require the India Teams Phone license.

- Wireless numbers require the user to consent to sharing their location at the time of establishing connectivity to the PSTN to determine if the user should be connected or blocked.

  - Teams clients will prompt the user for consent and use location services in the operating system of the user's device to share with the operator.

  - Teams clients don't show the dial button for users whom are assigned an India wireless number but haven’t consented to share their location to Teams.  

>
> [!NOTE]
> The user location data may be shared with the Operator Connect for India partners to fully enable PSTN calling scenarios. Microsoft does not store and retain this user location data.  

- Network sites / subnets which are used to determine the location of a user who is assigned a wireline number aren't used with wireless numbers.

- Teams Phone devices and Microsoft Teams Room systems don't support Operator Connect for India wireless numbers. 

- When India wireline numbers are used, Location Based Routing must be implemented and a Location Based Routing policy applied to the respective users.  

- The users in scope must be in **TeamsOnly** mode. It isn't required for the entire organization to be in TeamsOnly mode, but the users getting provisioned with Operator Connect in India must be in TeamsOnly mode. To learn more, see Understand Microsoft Teams and Skype for Business coexistence and interoperability. 

For technical support, contact the customer support of your operator first.  If the partner determines the issue is with Microsoft, they might ask you to raise a case with Microsoft, providing context of the investigation completed by the partner. If needed, the partner can bring the issue to Microsoft through their Microsoft support channel. Microsoft might reject support cases if investigation shows that the issue is one that the partner can address. 

>
> [!NOTE]
> India has a regulated classification of user, known as “other service provider (OSP)”, that allows calls for this type of user to egress out of India through your private network, bypassing India PSTN toll. OSP deployments are typically used for call centers and entitlement is arranged by the customer through India’s Department of Telecommunications. For purposes of this article, all users are considered non-OSP  and adhere to toll regulations. Microsoft support for Other Service Provider (OSP) calls with international telephone numbers is pending.

For next steps, see [Configure Operator Connect for India](operator-connect-india-configure.md).

## Related articles

- [Configure Operator Connect for India](operator-connect-india-configure.md)
- [Plan and configure Location-Based Routing for Operator Connect for India](location-based-routing-india-plan.md)
- [Configure network settings for Location-Based Routing](location-based-routing-configure-network-settings.md)