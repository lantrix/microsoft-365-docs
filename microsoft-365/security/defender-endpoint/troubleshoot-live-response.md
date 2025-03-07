---
title: Troubleshoot Microsoft Defender ATP live response issues
description: Troubleshoot issues that might arise when using live response in Microsoft Defender ATP
keywords: troubleshoot live response, live, response, locked, file
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: troubleshooting
ms.technology: mde
---

# Troubleshoot Microsoft Defender for Endpoint live response issues

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**Applies to:**
- [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Want to experience Defender for Endpoint? [Sign up for a free trial.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 

This page provides detailed steps to troubleshoot live response issues.

## File cannot be accessed during live response sessions
If while trying to take an action during a live response session, you encounter an error message stating that the file can't be accessed, you'll need to use the steps below to address the issue.

1. Copy the following script code snippet and save it as a PS1 file:

    ```
    $copied_file_path=$args[0] 
    $action=Copy-Item $copied_file_path -Destination $env:TEMP -PassThru -ErrorAction silentlyContinue
        
    if ($action){
         Write-Host "You copied the file specified in $copied_file_path to $env:TEMP Succesfully"
    }
    
    else{
        Write-Output "Error occoured while trying to copy a file, details:"
        Write-Output  $error[0].exception.message
 
    }
    ```


2. Add the script to the live response library.
3. Run the script with one parameter: the file path of the file to be copied.
4. Navigate to your TEMP folder.
5. Run the action you wanted to take on the copied file.

## Slow live response sessions or delays during initial connections
Live response leverages Defender for Endpoint sensor registration with WNS service in Windows. 
If you are having connectivity issues with live response, confirm the following details:
1. `notify.windows.com` is not blocked in your environment. For more information, see, [Configure device proxy and Internet connectivity settings](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).
2. WpnService (Windows Push Notifications System Service) is not disabled.

Refer to the articles below to fully understand the WpnService service behavior and requirements:
- [Windows Push Notification Services (WNS) overview](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/windows-push-notification-services--wns--overview)
- [Enterprise Firewall and Proxy Configurations to Support WNS Traffic](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)
- [Microsoft Push Notifications Service (MPNS) Public IP ranges](https://www.microsoft.com/en-us/download/details.aspx?id=44535)

