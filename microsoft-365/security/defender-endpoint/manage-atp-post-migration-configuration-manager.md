---
title: Manage Microsoft Defender for Endpoint using Configuration Manager
description: Learn how to manage Microsoft Defender for Endpoint with Configuration Manager
keywords: post-migration, manage, operations, maintenance, utilization, Configuration Manager, windows defender advanced threat protection, atp, edr
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.technology: mde
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: deniseb
author: denisebmsft
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: 
  - M365-security-compliance
  - m365solution-scenario
ms.topic: article
ms.date: 09/22/2020
ms.reviewer: chventou
---

# Manage Microsoft Defender for Endpoint with Configuration Manager

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**Applies to:**
- [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Want to experience Microsoft Defender for Endpoint? [Sign up for a free trial.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


We recommend using We recommend using [Microsoft Endpoint Manager](https://docs.microsoft.com/mem), which includes [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) (Intune) and [Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/mem/configmgr/core/understand/introduction) (Configuration Manager) to manage your organization's threat protection features for devices (also referred to as endpoints). 
- [Learn more about Endpoint Manager](https://docs.microsoft.com/mem/endpoint-manager-overview)
- [Co-manage Microsoft Defender for Endpoint on Windows 10 devices with Configuration Manager and Intune](manage-atp-post-migration-intune.md)

## Configure Microsoft Defender for Endpoint with Configuration Manager

|Task  |Resources to learn more  |
|---------|---------|
|**Install the Configuration Manager console** if you don't already have it<br/><br/>*If you don't already have the Configuration Manger console, use these resources to get the bits and install it.* |[Get the installation media](https://docs.microsoft.com/mem/configmgr/core/servers/deploy/install/get-install-media)<br/><br/>[Install the Configuration Manager console](https://docs.microsoft.com/mem/configmgr/core/servers/deploy/install/install-consoles)  |
|**Use Configuration Manager to onboard devices** to Microsoft Defender for Endpoint <br/><br/> *If you have devices (or endpoints) not already onboarded to Microsoft Defender for Endpoint, you can do that with Configuration Manager.*   |[Onboard to Microsoft Defender for Endpoint with Configuration Manager](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/defender-advanced-threat-protection#about-onboarding-to-atp-with-configuration-manager)      |
|**Manage antimalware policies and Windows Firewall security** for client computers (endpoints)<br/><br/>*Configure endpoint protection features, including Microsoft Defender for Endpoint, exploit protection, application control, antimalware, firewall settings, and more.*  |[Configuration Manager: Endpoint Protection](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/endpoint-protection)       |
|**Choose methods for updating antimalware updates** on your organization's devices <br/><br/>*With Endpoint Protection in Configuration Manager, you can choose from several methods to keep antimalware definitions up to date on your organization's devices.* |[Configure definition updates for Endpoint Protection](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/endpoint-definition-updates) <br/><br/>[Use Configuration Manager to deliver definition updates](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/endpoint-definitions-configmgr) |
|**Enable Network Protection** to help prevent employees from using apps that malicious content on the Internet <br/><br/>*We recommend using [audit mode](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/evaluate-network-protection) at first for network protection in a test environment to see which apps would be blocked before rolling out.* |[Turn on network protection with Configuration Manager](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/enable-network-protection#microsoft-endpoint-configuration-manager)  |
|**Configure controlled folder access** to protect against ransomware <br/><br/>*Controlled folder access is also referred to as antiransomware protection.*   |[Endpoint protection: Controlled folder access](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#controlled-folder-access) <br/><br/>[Enable controlled folder access in Microsoft Endpoint Configuration Manage](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/enable-controlled-folders#microsoft-endpoint-configuration-manager) |

## Configure your Microsoft Defender Security Center

If you haven't already done so, **configure your Microsoft Defender Security Center** ([https://securitycenter.windows.com](https://securitycenter.windows.com)) to view alerts, configure threat protection features, and view detailed information about your organization's overall security posture. 

You can also configure whether and what features end users can see in the Microsoft Defender Security Center.

- [Overview of the Microsoft Defender Security Center](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/use)

- [Endpoint protection: Microsoft Defender Security Center](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#microsoft-defender-security-center)

## Next steps

- [Get an overview of threat and vulnerability management](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)

- [Visit the Microsoft Defender Security Center security operations dashboard](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/security-operations-dashboard)

- [Manage Microsoft Defender for Endpoint with Intune](manage-atp-post-migration-intune.md)
