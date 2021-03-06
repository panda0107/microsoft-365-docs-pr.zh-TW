---
title: 從 Office 365 E3 遷移至 Microsoft 365 商務版
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
description: 瞭解如何將您的商務用 Office 365 E3 移至 Microsoft 365 商務版。
ms.openlocfilehash: cff6166529df2e56ba948a9bd3ea4594fb295b08
ms.sourcegitcommit: e525bcf073a61e1350484719a0c3ceb6ff0d8db1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/06/2020
ms.locfileid: "43153529"
---
# <a name="migrating-from-office-365-e3-to-microsoft-365-business"></a>從 Office 365 E3 遷移至 Microsoft 365 Business 

Microsoft 365 公司具有您的小型企業所需的一切，結合了最佳的雲端式生產力應用程式與簡單的裝置管理和安全性。 如果您目前已有 Office 365 E3 訂閱，但沒有超過300名員工，請考慮切換至 Microsoft 365 商務以加入安全性功能。

遷移非常簡單：先切換授權，您的目前訂閱中的所有資料和使用者資訊仍會維護。 遷移後，您必須設定在 Microsoft 365 商務版中新增的功能。

## <a name="differences-between-office-365-e3-and-microsoft-365-business"></a>Office 365 E3 與 Microsoft 365 業務之間的差異

下表顯示 Microsoft 365 商務版與 Office 365 E3 之間的差異。

| 功能    | Microsoft 365 商務版中的支援    | Office 365 E3 中的支援 | 
|:-------|:-----|:-----|
| **內部部署**        | | | 
| Office app<sup>1</sup>    | Office 365 商務版    | Office 365 專業增強版 | 
| **雲端生產力應用程式**        | | | 
| Exchange Online 和 Outlook    | 每個信箱 50 GB 儲存空間限制和 Exchange Online 封存數目不受限制    | 每個信箱 100 GB 儲存空間限制和 Exchange Online 封存數目不受限制 | 
| Teams    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Office 365 E3](../media/check-mark.png) | 
| 商務用 OneDrive    | 每個使用者 1 TB 的儲存空間限制    | 無限制 | 
| Yammer、SharePoint 線上、Planner、Stream    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Office 365 E3](../media/check-mark.png) | 
| StaffHub    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Office 365 E3](../media/check-mark.png) | 
| Outlook 客戶經理，MileIQ    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | | 
| **威脅防護**        | | | 
| Office 365 高級威脅防護（ATP）方案1 | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | 不包含，但可以新增于 | 
| **身分識別管理**        | | | 
| 混合式 Azure Active Directory （Azure AD）帳戶的自助密碼重設，Azure Multi-Factor 驗證，條件式存取，針對內部部署身分識別的密碼回寫功能|     ![隨附于 Microsoft 365 商務](../media/check-mark.png)    |  | 
| **裝置和應用程式管理**        | | |
| Microsoft Intune、Windows AutoPilot|     ![隨附于 Microsoft 365 商務](../media/check-mark.png)    |  |
| 共用電腦啟用|     ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Office 365 E3](../media/check-mark.png)| 
| 從 Win 7/8.1 Pro 授權到 Windows 10 專業版的升級許可權|     ![隨附于 Microsoft 365 商務](../media/check-mark.png)    || 
| **資訊保護**        | | |
|Office 365 資料外洩防護|    ![隨附于 Microsoft 365 商務](../media/check-mark.png)|![隨附于 Office 365 E3](../media/check-mark.png)|
|Azure 資訊保護方案1，Bitlocker 強制執行|![隨附于 Microsoft 365 商務](../media/check-mark.png)||
|Azure 資訊保護方案1，敏感度標籤|![隨附于 Microsoft 365 商務](../media/check-mark.png)||
|**用戶端存取許可證（CAL 許可權）**|||
|Enterprise CAL 套件（Exchange、SharePoint、Skype）||![隨附于 Office 365 E3](../media/check-mark.png)|

<sup>1</sup> Microsoft 365 商務版的 Office 應用程式不包括透過群組原則、應用程式遙測、更新控制項、試算表比較和查詢或商務智慧的大量啟用。

## <a name="migration"></a>移轉

若要遷移您的訂閱，請參閱[手動變更計畫](../commerce/subscriptions/change-plans-manually.md)，以瞭解是否只想要將少數幾個人移至 Microsoft 365 商務。 您也可以[自動升級所有人](../commerce/subscriptions/upgrade-to-different-plan.md)，或與合作夥伴合作，將 E3 訂閱和授權移至 Microsoft 365 商務版訂閱。
下列各節說明您需要做的變更（若有的話），以及遷移後可以執行的動作。

### <a name="office-365-e3-subscription-configuration-and-data"></a>Office 365 E3 訂閱設定和資料
您不需要在遷移之前對目前的訂閱或資料做任何變更，包括：

- 訂閱設定，例如 DNS 記錄和功能變數名稱。
- 使用者和群群組帳戶及驗證設定，例如多重因素驗證或條件式存取原則。
- 生產力服務設定及其資料，例如小組、Exchange Online 信箱、SharePoint 線上網站、商務 OneDrive 商務資料夾，以及 OneNote 筆記本。

### <a name="windows-10"></a>Windows 10

如果您的 Windows 未在 Windows Pro Creator 更新，請[將其升級至 Windows pro 建立者更新](upgrade-to-windows-pro-creators-update.md)。

### <a name="set-up-policies-to-protect-user-devices-and-files"></a>設定保護使用者裝置及檔的原則

> [!NOTE]
> 如果您設定 Office 365 MDM 原則和裝置，這些裝置將會列在 Microsoft 365 系統管理中心的 [**裝置**] 頁面上。 您設定的任何原則都會顯示在[Intune 入口網站](https://portal.azure.com/#blade/Microsoft_Intune_DeviceSettings/ExtensionLandingBlade/overview)的經典原則清單中。

將授權指派給 Microsoft 365 商務後，您就可以開始保護使用者的裝置和檔案。

如果您已將組織中的所有人員升級至 Microsoft 365 商務版，您會在首頁上看到 [安裝精靈]，而且可以遵循[安裝精靈的 [設定] 中的 [Microsoft 365 業務](set-up.md)]，以保護檔案和行動裝置。

您也可以在 [裝置] 頁面上完成這些步驟：
  
1. 在系統管理中心的左側導覽中，移至 [**裝置** \> **原則**]。
    
2. 在 [**裝置原則**] 頁面上，選擇 [**新增**]。
    
3. 在 [**新增原則**] 窗格中，將原則命名為 [名稱]，然後從下拉式清單中選擇**原則類型**。 
    
     您可以設定應用程式原則來保護 Android 和 iPhone 裝置上的檔案，以及 Windows 10，而且您可以設定公司擁有的 Windows 10 裝置的裝置設定原則。 如需詳細資訊，請參閱下列連結：
    
  - [設定 Android 或 iOS 裝置的 App 保護設定](app-protection-settings-for-android-and-ios.md)
    
  - [設定 Windows 10 裝置的應用程式保護設定](protection-settings-for-windows-10-devices.md)
    
  - [設定 Windows 10 電腦的裝置保護設定](protection-settings-for-windows-10-pcs.md)
  
4. 一旦您設定原則，您和您的員工便可以設定裝置：
    
  - 如需 Windows 裝置的步驟，請參閱為[Microsoft 365 商務使用者設定 Windows 裝置](set-up-windows-devices.md)。 
    
  - 如需 Android 手機和 Iphone 的步驟，請參閱為[Microsoft 365 商務版使用者設定行動裝置](set-up-mobile-devices.md)。 

### <a name="threat-protection"></a>威脅防護

在遷移至 Microsoft 365 商務版之後，您有 Office 365 ATP。 如需概要，請參閱[Office 365 ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp) 。 若要設定，請參閱[設定 atp 安全連結](https://support.office.com/article/61492713-53c2-47da-a6e7-fa97479e97fa)、[設定 atp 安全附件](https://support.office.com/article/e7e68934-23dc-4b9c-b714-e82e27a8f8a5)，以及[設定 atp 反網路釣魚](https://support.office.com/article/86c425e1-1686-430a-9151-f7176cce4f2c)。

### <a name="sensitivity-labels"></a>敏感度標籤

若要開始使用敏感度標籤，請參閱[敏感度標籤](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels)和[建立及管理敏感度標籤](https://support.office.com/article/2fb96b54-7dd2-4f0c-ac8d-170790d4b8b9)影片。
