---
title: Support for Windows 11
titleSuffix: Configuration Manager
description: Learn about the Windows 11 versions that are supported as clients with Configuration Manager.
ms.date: 10/08/2021
ms.prod: configuration-manager
ms.technology: configmgr-core
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Support for Windows 11 in Configuration Manager  

*Applies to: Configuration Manager (current branch)*

Learn about the Windows 11 versions that Configuration Manager supports as a client.

For more information about support for the Windows Assessment and Deployment Kit (ADK) for Windows 11, see [Support for the Windows ADK](support-for-windows-adk.md).

> [!NOTE]
> You can continue to use Microsoft Endpoint Manager to manage devices running Windows 11 the same as with Windows 10. If another article doesn't explicitly reference Windows 11, assume that feature support for Windows 10 also includes Windows 11. This article lists some [known issues](#known-issues).

<!--
> [!TIP]
> Windows Server builds as a client are supported the same as the associated Windows 11 version. For example, Windows Server 2022 is the same build version as Windows 11 ..., and Windows Server version ... is the same build version as Windows 11, version .... 
>
> For more information on Windows Server as a site system, see [Supported operating systems for Configuration Manager site system servers](supported-operating-systems-for-site-system-servers.md).
-->

## Windows 11 versions

Configuration Manager attempts to provide support as a client for each new Windows 11 version soon after it becomes available. Because the products have separate development and release schedules, the support that Configuration Manager provides depends on when each becomes available.

A Configuration Manager version drops from the matrix after [support for that version](../../servers/manage/current-branch-versions-supported.md) ends. Similarly, Configuration Manager doesn't support Windows 11 versions when their support lifecycle ends.

- The latest version of Configuration Manager current branch receives both security and critical updates, which can include fixes for Windows 11-specific features. When Microsoft releases a new version of Configuration Manager current branch, prior versions only receive security updates. For more information, see [Support for Configuration Manager current branch versions](../../servers/manage/current-branch-versions-supported.md).

    > [!NOTE]
    > The best way to stay current with Windows 11 is to stay current with Configuration Manager. For more information, see [Configuration Manager and Windows as a Service](../../understand/configuration-manager-and-windows-as-service.md).

- This information supplements [Supported operating systems for clients and devices](supported-operating-systems-for-clients-and-devices.md).

The following table lists the versions of Windows 11 that you can use as a client with different versions of Configuration Manager.

| Windows 11 version                         | ConfigMgr 2006 | ConfigMgr 2010 | ConfigMgr 2103 | ConfigMgr 2107 |
|--------------------------------------------|----------------|----------------|----------------|----------------|
| **21H2**<br>(10.0.22000) <!--2024-10-08--> | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Supported](media/green-check.png) |

<!--
All currently supported versions of Configuration Manager current branch support the following Windows 11 LTSC editions:

- **Enterprise LTSC xxxx** <!--mm/dd/yyyy
-->

For more information on Windows lifecycle, see the [Windows lifecycle fact sheet](/lifecycle/faq/windows) and [Windows release information](/windows/release-health/windows11-release-information).

| Key |
|--|
| ![Supported](media/green-check.png) = **Supported** |
| ![Not supported](media/red-x.png) = **Not supported** |

## Support notes

- Support for Windows 11 versions includes the following editions: Enterprise, Pro, Education, Pro Education, and Pro for Workstation.

- Windows 11 reports the **Operating System** property as `Microsoft Windows NT Workstation 10.0`, which is identical to Windows 10. To distinguish devices running Windows 11, use the **Operating System Build** device property for build number `10.0.22000` or later.<!-- 11059508 -->

- OS deployment images and upgrade packages for Windows 11 show the image name as Windows 10. For more information, see [Using deployment tools with Windows 11 images](/windows-hardware/manufacture/desktop/using-deployment-tools-with-windows-11).<!--11128713-->

## Support for Windows Insider

You can [update and service Windows Insider](../../../sum/get-started/configure-classifications-and-products.md#bkmk_WIfB) builds. This ability is provided as a convenience to our customers. While this functionality should work, its support is best effort. Configuration Manager might not issue a hotfix for this functionality if it doesn't work.

To provide feedback on Windows Insider, use the Windows [Feedback Hub](/windows-insider/business/feedback).

## Known issues

### Desktop Analytics

<!-- 10797955 -->

[Desktop Analytics](../../../desktop-analytics/overview.md) doesn't support Windows 11. For information about Windows 11 hardware readiness, Microsoft recommends that you enable tenant attach and [Endpoint analytics](../../../../analytics/overview.md).

### Windows servicing dashboard

<!-- 10732387 -->

The **Windows Servicing** dashboard currently includes Windows 11 devices with the latest version of Windows 10. It doesn't yet distinguish a version for Windows 11. For more information on this dashboard, see [Manage Windows as a service using Configuration Manager](../../../osd/deploy-use/manage-windows-as-a-service.md).

### Software Center notifications don't display during quiet period

<!-- 11059565 -->

By default, Windows 11 enables **focus assist** for the first hour after a user signs on for the first time. For more information, see [Reaching the Desktop and the Quiet Period](/windows-hardware/customize/desktop/customize-oobe-in-windows-11#reaching-the-desktop-and-the-quiet-period).

Software Center notifications are currently suppressed during this time. For more information, see [Turn Focus assist on or off in Windows](https://support.microsoft.com/windows/turn-focus-assist-on-or-off-in-windows-5492a638-b5a3-1ee0-0c4f-5ae044450e09#ID0EBD=Windows_11).


<!-- 11307733 -->
[!INCLUDE [windows-adk-11-preprovision-bitlocker](includes/windows-adk-11-preprovision-bitlocker.md)]

## Next steps

[Support for the Windows ADK](support-for-windows-adk.md)
