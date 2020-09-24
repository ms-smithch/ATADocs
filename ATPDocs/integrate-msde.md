---
# required metadata

title: Azure Advanced Threat Protection integration with Microsoft Defender ATP
description: How to integrate Azure Advanced Threat Protection with Microsoft Defender ATP for full threat detection coverage
keywords:
author: shsagir
ms.author: shsagir
manager: shsagir
ms.date: 02/19/2020
ms.topic: how-to
ms.collection: M365-security-compliance
ms.service: azure-advanced-threat-protection
ms.assetid: f6f3ed75-d6bb-4966-a9a7-5339c4f3ebac

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: itargoet
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Integrate Azure ATP with Microsoft Defender ATP

[!INCLUDE [Rebranding notice](includes/rebranding.md)]

Azure Advanced Threat Protection enables you to integrate Azure ATP with Microsoft Defender ATP, for an even more complete threat protection solution. While Azure ATP monitors the traffic on your domain controllers, Microsoft Defender ATP monitors your endpoints, together providing a single interface from which you can protect your environment.

By integrating Microsoft Defender ATP into Azure ATP, you can leverage the full power of both services and secure your environment, including:

- Endpoint behavioral sensors: Embedded in Windows 10, these sensors collect and process behavioral signals from the operating system (for example, process, registry, file, and network communications) and send this sensor data to your private, isolated, cloud instance of Microsoft Defender ATP.

- Cloud security analytics: Leveraging big-data, machine-learning, and unique Microsoft view across the Windows ecosystem (such as the [Microsoft Malicious Software Removal Tool](https://www.microsoft.com/download/malicious-software-removal-tool-details.aspx)), enterprise cloud products (such as Microsoft 365), and online assets (such as Bing and SmartScreen URL reputation), behavioral signals are translated into insights, detections, and recommended responses to advanced threats.

- Threat intelligence: Generated by Microsoft hunters, security teams, and augmented by threat intelligence provided by partners, threat intelligence enables Microsoft Defender ATP to identify attacker tools, techniques, procedures, and generate alerts when these activities are observed in collected sensor data.

Azure ATP technology detects multiple suspicious activities, focusing on several phases of the cyber-attack kill chain including:

- Reconnaissance, during which attackers gather information on how the environment is built, what the different assets are, and which entities exist. They generally build their plan for the next phases of the attack here.

- Lateral movement cycle, during which an attacker invests time and effort in spreading their attack surface inside your network.

- Domain dominance (persistence), during which an attacker captures the information allowing them to resume their campaign using various sets of entry points, credentials, and techniques.

At the same time, Microsoft Defender ATP leverages Microsoft technology and expertise to detect sophisticated cyber-attacks, providing:

- Behavior-based, cloud-powered, advanced attack detection  
Finds the attacks that made it past all other defenses (post breach detection), provides actionable, correlated alerts for known and unknown adversaries trying to hide their activities on endpoints.

- Rich timeline for forensic investigation and mitigation  
Easily investigate the scope of breach or suspected behaviors on any machine through a rich machine timeline. File, URLs, and network connection inventory across the network. Gain additional insight using deep collection and analysis ("detonation") for any file or URLs.

- Built in unique threat intelligence knowledge base  
Unparalleled threat optics provides actor details and intent context for every threat intelligence based detection – combining first and third-party intelligence sources.

## Prerequisites

To enable this feature, you need a license for both Azure ATP and Microsoft Defender ATP.

## How to integrate Azure ATP with Microsoft Defender ATP

1. In the Azure ATP portal, open **Configuration**.

    ![Azure ATP Configuration menu](media/atp-configuration-wd.png)
1. In the Configurations list, select **Microsoft Defender ATP** and set the integration toggle to **On**.

    ![Enable Windows Defender integration](media/enable-integration.png)

1. In the [Microsoft Defender ATP portal](https://securitycenter.windows.com/preferences/advanced), go to **Settings**, **Advanced features** and set **Azure ATP integration** to **ON**.

    ![Microsoft Defender ATP enable integration](media/wd-atp-enable.png)

1. To check the status of the integration, in the Azure ATP portal, go to **Settings** > **Microsoft Defender ATP integration**. You can see the status of the integration and if something is wrong, you'll see an error.

## How it works

After Azure ATP and Microsoft Defender ATP are fully integrated, in the Azure ATP portal, in the mini-profile pop-up and in the entity profile page, each entity that exists in Microsoft Defender ATP includes a badge to show that it is integrated with Microsoft Defender ATP.

 ![Microsoft Defender ATP alerts profile](media/profile-alerts-wd.png)

If the entity contains alerts in Microsoft Defender ATP, there is a number next to the badge to let you know how many alerts were raised.

 ![Azure ATP alerts](media/atp-integrated-wd-icon-alerts.png)

If you click on the badge, you are brought to the Microsoft Defender ATP portal where you can view and mitigate the alerts. If the entity is not recognized by Microsoft Defender ATP, the badge is grayed out.

 ![Microsoft Defender ATP gray](media/wd-grey.png)

From the Microsoft Defender ATP portal, click on an endpoint to view Azure ATP alerts. If you click on the alerts for this entity in Microsoft Defender ATP, the entity's profile page opens in Azure ATP.

 > [!NOTE]
 > Currently, Azure ATP integration with Microsoft Defender ATP supports only users and machines from the on-premises AD. Users from Azure AD and virtual machines that are managed in Azure will not be displayed as part of the integration

![Microsoft Defender ATP alerts](media/wd-atp-alerts.png)

## See Also

- [Investigating lateral movement paths with Azure ATP](use-case-lateral-movement-path.md)
- [Azure ATP sizing tool](https://aka.ms/aatpsizingtool)
- [Azure ATP architecture](architecture.md)
- [Install ATP](install-step1.md)
- [Check out the Azure ATP forum!](https://aka.ms/azureatpcommunity)