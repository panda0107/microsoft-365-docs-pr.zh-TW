---
title: 企業用 Microsoft 365 底層基礎結構
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 09/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: 了解貴組織中部署企業用 Microsoft 365 底層基礎結構的主要階段，也稱為核心部署。
ms.openlocfilehash: 6c2784d22e236880b87ece9e04e11fb0502667dd
ms.sourcegitcommit: e525bcf073a61e1350484719a0c3ceb6ff0d8db1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/06/2020
ms.locfileid: "43153841"
---
# <a name="microsoft-365-for-enterprise-foundation-infrastructure"></a>企業用 Microsoft 365 底層基礎結構

如果您要自行進行企業用 Microsoft 365 的端對端部署，請先建置穩固的基礎，以便應用程式與服務能夠在安全的環境中發揮創意和實現團隊合作能力。 此基礎有時也稱為*核心部署*。

如需明確的端對端部署路徑，您可以使用下列階段來規劃和部署企業用 Microsoft 365 的底層基礎結構：

| | 階段 | 結果 |
|:-------|:-----|:-----|
|![階段 1：網路](../media/deploy-foundation-infrastructure/networking_icon-small.png)|[階段 1：網路](networking-infrastructure.md)| 網路會針對 Microsoft 365 雲端式服務的存取進行最佳化。 |
|![階段 2：身分識別](../media/deploy-foundation-infrastructure/identity_icon-small.png)|[階段 2：身分識別](identity-infrastructure.md)| 系統管理員帳戶會受到保護、使用者和群組會進行同步處理，並提供增強式的使用者驗證機制。 |
|![階段 3：Windows 10 企業版](../media/deploy-foundation-infrastructure/win10enterprise_icon-small.png)|[階段 3：Windows 10 企業版](windows10-infrastructure.md)| 現有的 Windows 架構電腦可升級為 Windows 10 企業版，且新裝置會使用 Windows 10 企業版來進行安裝。 |
|![階段 4：Office 365 專業增強版](../media/deploy-foundation-infrastructure/O365proplus_icon-small.png)|[階段 4：Office 365 專業增強版](office365proplus-infrastructure.md)| 現有的 Microsoft Office 使用者可升級為 Office 365 專業增強版。 |
|![階段 5：行動裝置管理](../media/deploy-foundation-infrastructure/mobiledevicemgmt_icon-small.png)|[階段 5：行動裝置管理](mobility-infrastructure.md)| 裝置可以進行註冊並受到管理。 |
|![階段 6：資訊保護](../media/deploy-foundation-infrastructure/infoprotection_icon-small.png)|[階段 6：資訊保護](infoprotect-infrastructure.md)| 已啟用 Office 365 安全功能，您的標籤和原則已就緒，可保護文件和電子郵件。 |

這些階段會從最基本的項目 (網路和身分識別) 開始，然後會建立基礎結構的各個設定和群組層級，以便：

- 在裝置上安裝最新且最安全的 Windows 版本。
- 在裝置上安裝最新的 Microsoft Office 版本，並讓它保持最新。
- 管理您組織的裝置和其對應用程式的存取。
- 保護這些裝置上和雲端中的資訊。

不過，您可以彈性地設定和推出這些階段或階段內的步驟，以符合 IT 資源和企業的需求。

- **如果您是規模較小或創立不久的組織**，請視需要地遵循這些階段以便有系統地建置基礎結構。 若為非企業的簡化部署，請按一下[這裡](deploy-foundation-infrastructure-non-enterprises.md)。

-  **如果您是企業組織**，請將這些階段視為 IT 基礎結構層級而非明確的路徑，並判斷最終要如何做才能符合組織內每一層級的需求。

在每個階段的結尾，您都應該檢查其允出準則** (內含必須符合的必要條件以及要考慮的選擇性條件)。 每個階段的允出準則可確保您的內部部署和雲端基礎結構與產生的端對端設定符合企業用 Microsoft 365 部署需求。

若要了解內容的建構方式，請觀看這段短片。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE23VRG]

以下是整個企業用 Microsoft 365 部署指南中的底層基礎結構：

![整個企業用 Microsoft 365 部署指南中的底層基礎結構](../media/deploy-foundation-infrastructure/m365-deploy-content-arch-foundation.png)

## <a name="at-a-glance"></a>概覽

[企業用 Microsoft 365 底層基礎結構海報](../media/deploy-foundation-infrastructure/Microsoft365EnterpriseFoundInfra.pdf)是可讓您檢視每個階段的中央位置：

- 系統管理員和使用者的階段整體目標
- 服務、功能及工具
- 規劃的重要決策
- 組態結果
- 新使用者的上線程序
- 如何監控及更新

[![企業用 Microsoft 365 底層基礎結構海報的影像](../media/deploy-foundation-infrastructure/Microsoft365EnterpriseFoundInfra.png)](../media/deploy-foundation-infrastructure/Microsoft365EnterpriseFoundInfra.pdf)

若要下載此海報的副本，請按一下[這裡](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/deploy-foundation-infrastructure/Microsoft365EnterpriseFoundInfra.pdf)。


## <a name="infrastructure-configuration-vs-user-rollout"></a>基礎結構設定與使用者推出

底層基礎結構是一組設定好的軟體和服務，結合在一起時可讓使用者利用企業用 Microsoft 365 所提供的完整功能和保護機制。 端對端部署旅程的終點是要讓這個基礎結構套用至所有使用者和其持有的 Windows 架構裝置。 

不過請務必注意，對使用者推出軟體與服務的行為與企業用 Microsoft 365 底層基礎結構無關。 ***您可以設定底層基礎結構的層級，而不需要對所有使用者推出這些層級。***

您可以事先設定、測試和試驗底層基礎結構的元素，然後再對辦公室、地區或組織部門內的眾多使用者推出這些元素。

例如，您可以針對下列項目建立設定：

| 階段 | 結果 |
|:-------|:-----|
| 身分識別 | 帳戶同步處理和身分識別型條件式存取原則的群組。 |
| Windows 10 企業版 | 可自動將執行 Windows 7 或 Windows 8.1 的電腦就地升級為 Windows 10 企業版的群組。 |
| Office 365 專業增強版 | 可自動為使用 Office 2010、Office 2013 或 Office 2016 的使用者部署 Office 365 專業增強版的群組。 |
| 行動裝置管理 | 用於裝置註冊和裝置型條件式存取原則的群組。 |
| 資訊保護 | Office 365 敏感度標籤的群組。 |

當您準備好對使用者推出這個基礎結構的元素時：

| 階段 | 推出動作 |
|:-------|:-----|
| 身分識別 | 將使用者帳戶新增至身分識別型條件式存取原則的群組。 |
| Windows 10 企業版 | 將帳戶新增至可自動為使用 Windows 7 或 Windows 8.1 的使用者就地部署 Windows 10 企業版的群組。 |
| Office 365 專業增強版 | 將使用者帳戶新增至可自動為使用 Office 2010、Office 2013 或 Office 2016 的使用者部署 Office 365 專業增強版的群組。 |
| 行動裝置管理 | 將帳戶新增至用於裝置註冊和裝置型條件式存取原則的群組。 |
| 資訊保護 | 將使用者帳戶新增至敏感度標籤群組。 |

在底層基礎結構的階段或元素完成、經過測試及試驗後，您便可以對使用者以最符合業務目標和 IT 資源的方式推出已安裝好的軟體 (例如，Windows 10 企業版和 Office 365 專業增強版) 以及雲端式服務和保護 (例如，裝置註冊和條件式存取原則)。

## <a name="deployment-and-project-management-strategies"></a>部署和專案管理策略

若要了解如何讓試驗使用者和組織內的其他人知道如何對底層基礎結構的不同階段進行專案管理，請參閱[部署策略](deployment-strategies-microsoft-365-enterprise.md)。

## <a name="deployment-for-non-enterprises"></a>非企業部署

如果您是小型組織，而 Microsoft 365 商務版不適合您，請參閱[非企業部署](deploy-foundation-infrastructure-non-enterprises.md)，以了解簡化的部署方式。


## <a name="next-step"></a>下一步

| 我的所在位置 | 我要前往何處 |
|:-------|:-----|
| 我有現有的 Office 365、Enterprise Mobility + Security (EMS) 或 Windows 10 企業版基礎結構 | 從[使用現有基礎結構部署](deploy-with-existing-infrastructure.md)開始，這將逐步引導您進行每個階段的允出準則。 |
| 我是從頭開始的企業 | 使用[階段 1：網路](networking-infrastructure.md)開始端對端部署旅程。 |
| 我從頭開始，但不是企業 | 使用[非企業部署](deploy-foundation-infrastructure-non-enterprises.md)開始端對端部署旅程。 |
