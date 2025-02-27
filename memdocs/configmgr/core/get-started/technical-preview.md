---
title: Technical preview releases
titleSuffix: Configuration Manager
description: Learn about the technical preview branch to test-drive new functionality and capabilities in Configuration Manager.
ms.date: 10/12/2021
ms.prod: configuration-manager
ms.technology: configmgr-core
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.localizationpriority: medium
---

# Technical preview for Configuration Manager

*Applies to: Configuration Manager (technical preview branch)*

This article provides details about the monthly technical preview branch of Configuration Manager. The technical preview introduces new functionality that Microsoft is working on. It introduces new features that aren't yet included in the current branch of Configuration Manager. These features might eventually be included in an update to the current branch. Before we finalize the features, we want you to try them out and give us feedback.

Because this release is a technical preview, details and functionality are subject to change.

This information applies to all versions of the Configuration Manager technical preview branch. This article lists each new feature along with the technical preview version in which it first appears. For example, version **2101** for January (`01`) of 2021 (`21`). Separate articles dedicated to each preview version detail the individual features.

For information about what's new in the *current branch* of Configuration Manager, see [What's new in Configuration Manager incremental versions](../plan-design/changes/whats-new-incremental-versions.md).

> [!TIP]
> To get notified when this page is updated, copy and paste the following URL into your RSS feed reader:
> `https://docs.microsoft.com/api/search/rss?search=%22technical+preview+releases+-+Configuration+Manager%22&locale=en-us`

## <a name="bkmk_reqs"></a> Requirements and limitations

> [!IMPORTANT]
> The technical preview is licensed for use only in a lab environment. Microsoft may not provide support services and certain features may not be available in technical previews. Additionally, technical preview software may have reduced or different security, privacy, accessibility, availability, and reliability standards relative to commercially provided software.

For most product prerequisites, use the information in the [Supported configurations](../plan-design/configs/supported-configurations.md). The following exceptions apply to the technical preview branch:

- Each install is active for 90 days before it becomes inactive.

- English is the only language supported.

- It only supports the following setup command-line parameters:

  - `/silent`
  - `/testdbupgrade`

- The service connection point installs to online mode. It doesn't support offline mode.

    > [!NOTE]
    > You may need to allow specific internet URLs, some of which are specific to the technical preview branch. For more information, see [Internet access requirements](../plan-design/network/internet-endpoints.md).

- The separate articles for each specific version of the technical preview include additional limitations or requirements, as applicable.

- The following features aren't supported with the technical preview branch:

  - [Migration](../migration/migrate-data-between-hierarchies.md) to or from this preview branch.

  - [Upgrade](../servers/deploy/install/upgrade-to-configuration-manager.md) to this preview branch.

  - [Site recovery](../servers/manage/recover-sites.md) from the cd.latest folder.<!--507106-->

- There's no support for updating to current branch from this preview branch.

    > [!Note]
    > When updates are available for a preview version, you still find and install them from the **Updates and Servicing** node of the Configuration Manager console. For a video of the in-console upgrade process, see [Installing Configuration Manager update packages](https://www.youtube.com/embed/KBd_EGFbUT8) on youtube.com.

- It only supports a standalone primary site. There's no support for a central administration site, multiple primary sites, or secondary sites.

The technical preview branch of Configuration Manager supports the following products and technologies:

- Unless otherwise noted, the technical preview branch supports the same versions of SQL Server as the current branch. For more information, see [Supported SQL Server versions](../plan-design/configs/support-for-sql-server-versions.md).

- The site supports up to 10 clients, which can run any [supported client OS version](../plan-design/configs/supported-operating-systems-for-clients-and-devices.md).<!-- SCCMDocs#1656 -->

> [!Note]
> The inclusion of these products in this content doesn't imply an extension of support for a version that's beyond its support lifecycle. Configuration Manager doesn't support products that are beyond their support lifecycle. For more information, see [Microsoft Lifecycle Policy](https://support.microsoft.com/lifecycle).

## <a name="bkmk_install"></a> Install and update

The Configuration Manager technical preview branch for lab use is distinct from the Configuration Manager current branch for production use.

First install a baseline version of the technical preview branch. After installing a baseline version, then use in-console updates to bring your installation up to date with the most recent preview version. Typically, new versions of the technical preview are available each month.

Microsoft supports each technical preview version up until three successive versions are available. For example, when version 1908 released, version 1904 was no longer in support. Versions 1905, 1906, and 1907 remained in support. When a baseline falls out of support, it's still supported for installing a new technical preview site, assuming you immediately update to a supported version. The older baseline is supported until a new baseline version is available. Update to the latest available version from the baseline, and then repeat the update process until you install the latest technical preview version.

> [!TIP]
> When you install an update to the technical preview, you update your preview installation to that new technical preview version. A technical preview installation never has the option to upgrade to a current branch installation. It also never receives updates from the current branch release.
>
> Several times throughout the year, there are technical preview branch and current branch versions with the same version number. For example, there is a technical preview version 2006 and a current branch version 2006.

### Active baseline versions

Install a baseline version for up to one year after its release. When you install a new technical preview site, use the latest baseline version:

- **Technical preview version 2110**

Download a baseline version from the [Evaluation Center](https://www.microsoft.com/evalcenter/evaluate-system-center-configuration-manager-and-endpoint-protection-technical-preview).

## <a name="BKMK_TPFeedback"></a> Providing feedback

We love to hear your feedback about the new features in the technical preview. For more information, see [Product feedback](../understand/product-feedback.md).

<!--10932544 If you have ideas about new features you would like to see, let us know! Submit new ideas and vote on the ideas by others: [Configuration Manager UserVoice](https://configurationmanager.uservoice.com). -->

<!--
## <a name="bdmk_tpknownissues"></a> General changes introduced in technical preview branch

<!-- (explanatory comment)
Enable this section if needed to include any broad change to the tech preview branch
-->

## <a name="bkmk_tpCaps"></a> Features in the most recent version

<!-- (explanatory comment)
This is the full list of new features in the latest TP release

bullet format:
<!-- - [title](2021/technical-preview-2101.md) <!--ID-->

The following features are available with the most recent Configuration Manager technical preview version:

### Technical preview version 2110

- [Simplified cloud attach configuration](2021/technical-preview-2110.md#bkmk_attach) <!--10964629-->
- [Improvements to client health dashboard](2021/technical-preview-2110.md#bkmk_health) <!--5728069-->
- [Enable update notifications from Microsoft 365 Apps](2021/technical-preview-2110.md#bkmk_365) <!--10628998-->
- [Branding in the Windows Update native reboot experience](2021/technical-preview-2110.md#bkmk_brand) <!--10543514-->
- [Improvements to application groups](2021/technical-preview-2110.md#bkmk_appgroups) <!--10479618-->
- [Improvements to external notifications](2021/technical-preview-2110.md#bkmk_notify) <!--10615989-->
- [Approvals for orchestration group scripts](2021/technical-preview-2110.md#bkmk_orchestration) <!--9957939-->
- [Task sequence check for TPM 2.0](2021/technical-preview-2110.md#bkmk_tpm) <!--9575077-->
- [Console improvements](2021/technical-preview-2110.md#bkmk_console) <!--9575773-->
- [Status messages for console extensions](2021/technical-preview-2110.md#bkmk_audit) <!--11048976-->

> [!NOTE]
> Features that were available in a previous version of the technical preview remain available in later versions. Similarly, features that are added to the Configuration Manager current branch remain available in the technical preview branch.

## Features in recent technical previews

<!-- (explanatory comment)
This is the full list of new features in the past TP releases since the last CB release.
Each month, add features from the list above to a new H3 section at the top of this section.
When there's a new CB, add any features not in that CB to the table in H2 "Features in previous technical previews"
-->

The following features were released with previous versions of the Configuration Manager technical preview branch since current branch version 2103:

> [!TIP]
> When a new current branch version is available, features that are available in that version are listed in the latest *What's new* article. For more information, see [What's new in incremental versions](../plan-design/changes/whats-new-incremental-versions.md#supported-versions).

### Technical preview version 2109

- [Improvements to Support Center OneTrace](2021/technical-preview-2109.md#bkmk_onetrace) <!--9348231-->
- [Options for Support Center Data Collector and Client Tools](2021/technical-preview-2109.md#bkmk_support) <!--9947307-->
- [Send product feedback from wizard and property dialogs](2021/technical-preview-2109.md#bkmk_feedback) <!--2711343-->
- [Implicit uninstall for user collections](2021/technical-preview-2109.md#bkmk_uninstall) <!--10393847-->
- [Require installation of a console extension](2021/technical-preview-2109.md#bkmk_extensions) <!--10486584-->
- [Import console extensions wizard](2021/technical-preview-2109.md#bkmk_import) <!--9741121-->
- [Improvements to ADR search criteria](2021/technical-preview-2109.md#bkmk_adr) <!--7033309-->
- [Improvements to VPN boundary types](2021/technical-preview-2109.md#bkmk_vpn) <!--7822886-->
- [.NET version 4.6.2 prerequisite check is an error](2021/technical-preview-2109.md#bkmk_dotnetprereq) <!--10644702-->
- [External dependencies require .NET 4.6.2](2021/technical-preview-2109.md#bkmk_dotnetsdk) <!--10529267-->
- [Copy GUID for ISV proxy certificate](2021/technical-preview-2109.md#bkmk_isvproxy) <!--2842082-->
- [PowerShell release notes preview](2021/technical-preview-2109.md#bkmk_powershell) <!--10654429-->

### Technical preview version 2108

- [Export to CSV](2021/technical-preview-2108.md#bkmk_csv) <!--9663857-->
- [Custom properties for devices in the console](2021/technical-preview-2108.md#bkmk_custom) <!--10642650-->
- [Improvements to Software Center notifications with logos](2021/technical-preview-2108.md#bkmk_notify) <!--4993167-->
- [PowerShell release notes preview](2021/technical-preview-2108.md#bkmk_powershell) <!--10326535-->

### Technical preview version 2107

- [Tenant attach: Software updates information](2021/technical-preview-2107.md#bkmk_sum) <!--6024419-->
- [Publish query to Community hub from CMPivot](2021/technical-preview-2107.md#bkmk_hub) <!--9965423-->

## Features in previous technical previews

<!-- (explanatory comment)
This is the list of individual features that are still in TP (not in CB). 
Copy from the lists above any individual features that are still in TP and add to the top of this list
With each CB release, review and remove from this list for anything that's now available in CB. 
-->

The following features were released with previous versions of the Configuration Manager technical preview branch. These features remain available in later versions, but aren't yet available in the current branch.

| Feature        | Technical preview version |
|----------------|---------------------------|
| Intune role-based access control for tenant attach <!--8126836--> | [Tech preview 2106](2021/technical-preview-2106.md#bkmk_rbac) |
| Windows Update native experience for software updates <!--4316341--> | [Tech preview 2105.2](2021/technical-preview-2105-2.md#bkmk_wu) |
| Support Center dark and light themes <!--8218853--> | [Tech preview 2105](2021/technical-preview-2105.md#bkmk_dark) |
| Manage aged distribution point messages <!--8561493,9388277--> | [Tech preview 2101](2021/technical-preview-2101.md#bkmk_distmsg) |
| Community hub support for application content <!--7983035--> | [Tech preview 2012](2020/technical-preview-2012.md#bkmk_hubapp) |
| Software Center notifications display with logo <!--4993167--> | [Tech preview 2011](2020/technical-preview-2011.md#bkmk_notify) |
| Improvements to multicast-enabled distribution points <!--3785535--> | [Tech preview 1908.2](2019/technical-preview-1908-2.md#bkmk_multicast) |
| Phased deployment templates <!--4961086--> | [Tech preview 1908](2019/technical-preview-1908.md#phased-deployment-templates) |
| Remote control anywhere using cloud management gateway <!--4575930--> | [Tech preview 1906](2019/technical-preview-1906.md#remote-control-anywhere-using-cloud-management-gateway) and [Tech preview 2009](2020/technical-preview-2009.md#bkmk_remctrl) |
| Client-based PXE responder service <!--3556018, fka 1357148--> | [Tech preview 1712](capabilities-in-technical-preview-1712.md#client-based-pxe-responder-service) |
| PXE network boot support for IPv6 <!--3601254, fka 1269793--> |[Tech preview 1706](capabilities-in-technical-preview-1706.md#pxe-network-boot-support-for-ipv6)|
| Use Azure Active Directory <!--3607315, fka 1322145--> | [Tech preview 1702](capabilities-in-technical-preview-1702.md#azurediscovery) |
| Improvements to Asset Intelligence <!--3601024, fka 1307390--> | [Tech preview 1608](capabilities-in-technical-preview-1608.md#improvements-to-asset-intelligence) |

## Next steps

For more information, see the following articles:

- [Evaluate Configuration Manager in a lab](evaluate-with-lab-environment.md)
- [What's new in Configuration Manager incremental versions](../plan-design/changes/whats-new-incremental-versions.md)
- [Introduction to Configuration Manager](../understand/introduction.md)

> [!TIP]
> For more information on current branch features that require consent to enable, see [pre-release features](../servers/manage/pre-release-features.md).
>
> For more information on current branch features that you must enable first, see [Enable optional features from updates](../servers/manage/optional-features.md).
