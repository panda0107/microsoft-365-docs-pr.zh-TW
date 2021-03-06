---
title: 從 Microsoft 365 商務版移轉至 Microsoft 365 E3
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
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
search.appverid:
- BCS160
- MET150
ms.assetid: 5b4ba843-24b8-4526-8e1f-f9b9eab89d06
description: 瞭解如何將您的企業從 Microsoft 365 商務版移至 Microsoft 365 E3。
ms.openlocfilehash: 0d636c0572850a53612bf756508c4b57f1b3e4eb
ms.sourcegitcommit: e525bcf073a61e1350484719a0c3ceb6ff0d8db1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/06/2020
ms.locfileid: "43153517"
---
# <a name="migrate-from-microsoft-365-business-to-microsoft-365-e3"></a>從 Microsoft 365 商務版移轉至 Microsoft 365 E3

Microsoft 365 公司具有您的小型企業所需的一切，結合了最佳的雲端架構應用程式與簡單的裝置管理和安全性，可讓您的員工採取最佳的工作。 不過，在某些情況下，您可能需要將 Microsoft 365 商務版訂閱遷移至 Microsoft 365 E3。 

例如，您的公司成長並需要超過300的授權（順便說一來）。

或者，您的業務需要企業版功能，例如 Office 365 ProPlus、Windows 10 企業版 E3 或企業用戶端存取授權（Cal）。

升級非常簡單：您可以[從系統管理中心](../commerce/subscriptions/upgrade-to-different-plan.md)開始升級。 您目前訂閱中的所有資料和設定均會維護。 您不需要做為遷移準備，也不需要執行任何動作，只會利用新功能。

>[!Note]
>您也可以使用 Microsoft 365 商務版訂閱來獲得最多300的席位，並取得 Microsoft 365 E3 訂閱，以供超過300的席位使用。 不過，Office 365 ATP 並未包含在 Microsoft 365 E3 中。 針對持續威脅防護，您應該新增額外的 Office 365 ATP 授權，以便授權您的 Office 365 ATP 原則範圍內的所有使用者。
>

## <a name="differences-between-microsoft-365-business-and-microsoft-365-enterprise"></a>Microsoft 365 商務和 Microsoft 365 企業版之間的差異

下表顯示 Microsoft 365 商務和 Microsoft 365 E3 之間的差異。

| 功能    | Microsoft 365 商務版中的支援    | Microsoft 365 E3 中的支援 | 
|:-------|:-----|:-----|
| **內部部署**        | | | 
| Windows 10    | Windows 10 商務版  |     Windows 10 企業版 E3| 
| Office app *    | [Office 365 商務版](#office-365-business)    | Office 365 專業增強版 | 
| **雲端生產力應用程式**        | | | 
| Exchange Online 和 Outlook    | 每個信箱 50 GB 儲存空間限制和 Exchange Online 封存數目不受限制    | 每個信箱 100 GB 儲存空間限制和 Exchange Online 封存數目不受限制 | 
| Teams    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| 商務用 OneDrive    | 每個使用者 1 TB 的儲存空間限制    | 無限制 | 
| Yammer、SharePoint 線上、Planner、Stream    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| Outlook 客戶經理，MileIQ    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | | 
| **威脅防護**        | | | 
| 攻擊面降減功能    | [請參閱此清單](#threat-protection) | Microsoft Edge 的硬體隔離的企業管理 | 
| Office 365 高級威脅防護（ATP）方案1 | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | 不包含，但可以新增于 | 
| **身分識別管理**        | | | 
| 混合式 Azure Active Directory （Azure AD）帳戶的自助密碼重設，Azure Multi-Factor 驗證，條件式存取，針對內部部署身分識別的密碼回寫功能|     ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| 雲端應用程式探索，Azure AD Connect Health    |     | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| Azure AD Office 365 應用程式單一 Sign-On （SSO）：每位使用者有10個應用程式（庫 SaaS 應用程式，例如 Salesforce） * | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| Azure AD Premium P1 SSO：沒有限制（透過 Azure AD 應用程式 Proxy 的內部部署應用程式，以及使用 Self-Service 應用程式整合範本的非畫廊應用程式）    |     | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| **裝置和應用程式管理**        | | | 
| Microsoft Intune、Windows Autopilot|     ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
|虛擬桌面存取（VDA）    |  |     ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
|Windows 虛擬機器（WVD）    | ![隨附于 Microsoft 365 商務](../media/check-mark.png) |     ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
|共用電腦啟用（SCA）    | ![隨附于 Microsoft 365 商務](../media/check-mark.png) |     ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| Microsoft 桌面優化套件    | |     ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| **資訊保護**        | | | 
| Office 365 資料遺失防護，Azure 資訊保護方案1    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| Endpoint DLP 的視窗資訊保護    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| **用戶端存取許可證（CAL 許可權）**    | | |     
| Enterprise CAL 套件（Exchange、SharePoint、Skype、Windows、Microsoft Endpoint Configuration 管理員、Windows Rights Management）| |         ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| **合規性**        | | | 
| 無限制的電子郵件封存    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| 合規性分數/合規性管理員    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| 電子文件探索    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| 就地保留和訴訟暫止    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
| 通訊記錄管理（MRM）保留標記和保留原則    | ![隨附于 Microsoft 365 商務](../media/check-mark.png)    | ![隨附于 Microsoft 365 E3](../media/check-mark.png) | 
||||

\*已獲指派 SaaS app 存取權的使用者，可對最多10個應用程式取得 SSO 存取權。 系統管理員可以設定 SSO，並變更使用者對不同 SaaS 應用程式的存取，但是每個使用者一次只能有10個應用程式使用 SSO 存取。 所有 Office 365 應用程式會計為單一應用程式。

## <a name="migration"></a>移轉

若要進行遷移，請與您的合作夥伴合作，將您的 Microsoft 365 商務版訂閱和授權，移至適當的 Microsoft 365 E3 訂閱及其授權。

下列各節說明您需要做哪些變更（若有的話），以及遷移之後可執行檔動作。

### <a name="microsoft-365-subscription-configuration-and-data"></a>Microsoft 365 訂閱設定和資料

您不需要在遷移之前對目前的訂閱或資料進行任何變更，包括：

- 訂閱設定，例如 DNS 功能變數名稱。
- 使用者和群群組帳戶及驗證設定，例如多重因素驗證或條件式存取原則。
- 生產力服務設定及其資料，例如小組、Exchange Online 信箱、SharePoint 線上網站、商務 OneDrive 商務資料夾，以及 OneNote 筆記本。

您的使用者現在可以在 Exchange Online 信箱和商務資料夾的 OneDrive 中享受無限儲存體。

您可以開始針對超過10個應用程式使用雲端應用程式探索、Azure AD Connect Health 和 SSO。

>[!Note]
>遷移至 Microsoft 365 E3 的使用者無法再使用 Outlook 客戶主管和 MileIQ。
>

<a name="threat-protection"></a>
### <a name="threat-protection"></a>威脅防護

Windows 10 商務版包含下列保護：

- 作業系統啟動處理常式的完整性強制執行
- 機密運作元件的完整性強制執行
- 「高級弱點」和「零日利用」緩解
- Microsoft Edge、Internet Explorer 和 Chrome 的信譽式網路保護
- 主機型防火牆
- 勒索軟體緩解
- Microsoft Edge 的硬體隔離
- 由智慧安全性圖形供電的應用程式控制
- 裝置控制（USB）
- 網路型威脅的網路保護
- 主機入侵防護規則

Windows 10 企業版 E3 也包含以硬體為基礎的 Microsoft Edge 隔離的企業管理。

>[!Note]
>遷移至 Microsoft 365 E3 的使用者，每個使用者都需要 Office 365 ATP 授權，以繼續威脅防護。 請務必購買其他 Office 365 ATP 授權，以便授權您的 Office 365 ATP 原則範圍內的所有使用者。 
>

### <a name="device-management-with-intune"></a>使用 Intune 的裝置管理

您不需要在遷移之前對目前的 Intune 設定進行任何變更（包括已註冊的裝置和裝置及應用程式設定）。

### <a name="windows-10"></a>Windows 10

Microsoft 365 商務版包含 Windows 10 商務版，您可以使用 Windows AutoPilot 加以安裝。 當您遷移至 Microsoft 365 E3 時，每個使用者授權都會包含 Windows 10 企業版 E3，您也可以使用 Windows Autopilot 進行安裝。

<a name="office-365-business"></a>
### <a name="office-365-business"></a>Office 365 商務版

您的裝置上安裝的 Office 365 商務用戶端將會自動開始使用 Office 365 ProPlus 的功能。 遷移後，您現在可以使用：

 - 透過群組原則啟用磁片區
 - 應用程式遙測
 - 更新控制項
 - 試算表比較及查詢
 - 商務智慧

