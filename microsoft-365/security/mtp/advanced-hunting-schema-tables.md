---
title: Microsoft 威脅防護進階搜捕結構描述的資料表格
description: 了解進階搜捕結構描述中的表格，以明白您可以執行威脅搜捕查詢的資料
keywords: 高級搜尋，威脅搜尋，網路威脅搜尋，microsoft 威脅防護，microsoft 365，mtp，m365，search，query，遙測，schema reference，kusto，table，data
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 0b28cf2ce96e4c040fac0999d669623cef066fe4
ms.sourcegitcommit: 3b2fdf159d7dd962493a3838e3cf0cf429ee2bf2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "42929489"
---
# <a name="understand-the-advanced-hunting-schema"></a>了解進階搜捕結構描述

**適用於：**
- Microsoft 威脅防護



[進階搜捕](advanced-hunting-overview.md)結構描述是由多個提供事件資訊或與電腦或實體相關資訊的表格所組成。 若要有效組建跨越多個表格的查詢，您需要了解進階搜捕結構描述中的表格和欄。

## <a name="schema-tables"></a>結構描述表格

以下參考列出結構描述中的所有表格。 每個表格名稱都會連結到描述該表格之欄名稱的頁面。 表格和欄名稱也同樣列於安全性中心，成為進階搜捕畫面上結構描述代表中的一部分。

| 表格名稱 | 描述 |
|------------|-------------|
| **[AlertInfo](advanced-hunting-alertinfo-table.md)** | 來自 Microsoft Defender ATP、Office 365 ATP、Microsoft Cloud App Security 和 Azure ATP 的警示，包括嚴重性資訊和威脅分類  |
| **[AlertEvidence](advanced-hunting-alertevidence-table.md)** | 與警示相關聯的檔案、IP 位址、URLs、使用者或裝置 |
| **[AccountInfo](advanced-hunting-accountinfo-table.md)** | 各來源的帳戶資訊，包括 Azure Active Directory |
| **[EmailEvents](advanced-hunting-emailevents-table.md)** | Office 365 電子郵件事件，包括電子郵件傳送和封鎖事件 |
| **[EmailAttachmentInfo](advanced-hunting-emailattachmentinfo-table.md)** | 有關已附加到 Office 365 電子郵件的檔案相關資訊 |
| **[EmailUrlInfo](advanced-hunting-emailurlinfo-table.md)** | Office 365 電子郵件上 URL 的相關資訊 |
| **[DeviceInfo](advanced-hunting-deviceinfo-table.md)** | 電腦資訊，包括作業系統資訊 |
| **[DeviceNetworkInfo](advanced-hunting-devicenetworkinfo-table.md)** | 電腦的網路摘要資訊，包括介面卡、IP 和 MAC 位址，以及已連結的網路和網域 |
| **[DeviceProcessEvents](advanced-hunting-deviceprocessevents-table.md)** | 程序建立與相關事件 |
| **[DeviceNetworkEvents](advanced-hunting-devicenetworkevents-table.md)** | 網路連結與相關事件 |
| **[DeviceFileEvents](advanced-hunting-devicefileevents-table.md)** | 檔案建立、修改及其他檔案系統事件 |
| **[DeviceRegistryEvents](advanced-hunting-deviceregistryevents-table.md)** | 登錄項目的建立及修改 |
| **[DeviceLogonEvents](advanced-hunting-devicelogonevents-table.md)** | 登入和其他驗證事件 |
| **[DeviceImageLoadEvents](advanced-hunting-deviceimageloadevents-table.md)** | DLL 載入事件 |
| **[DeviceEvents](advanced-hunting-deviceevents-table.md)** | 多種事件種類，包括由安全性控制項觸發的事件，例如 Windows Defender 防毒軟體和惡意探索保護 |
| **[DeviceFileCertificateInfoBeta](advanced-hunting-devicefilecertificateinfobeta-table.md)** | 從端點上的憑證驗證事件取得的簽署檔憑證資訊 |
| **[DeviceTvmSoftwareInventoryVulnerabilities](advanced-hunting-tvm-softwareinventory-table.md)** | 裝置上的軟體庫存，以及這些軟體產品中的任何已知弱點 |
| **[DeviceTvmSoftwareVulnerabilitiesKB](advanced-hunting-tvm-softwarevulnerability-table.md)** | 公開披露弱點的知識庫，包括是否公開提供惡意探索代碼 |
| **[DeviceTvmSecureConfigurationAssessment](advanced-hunting-tvm-configassessment-table.md)** | 威脅與弱點管理評定事件，可表示裝置上的各種安全性設定狀態 |
| **[DeviceTvmSecureConfigurationAssessmentKB](advanced-hunting-tvm-secureconfigkb-table.md)** | 由威脅與弱點管理所使用之各種安全性設定的知識庫來評定裝置，包含各種標準和效能評定的對應  |
| **[AppFileEvents](advanced-hunting-appfileevents-table.md)** | 雲端應用程式和服務中的檔相關活動 |
| **[IdentityLogonEvents](advanced-hunting-identitylogonevents-table.md)** | 由 Active Directory 及其他 Microsoft online 服務記錄的驗證事件 |
| **[IdentityQueryEvents](advanced-hunting-identityqueryevents-table.md)** | 對 Active Directory 物件（例如使用者、群組、裝置和網域）執行的查詢活動 |


## <a name="related-topics"></a>相關主題
- [進階搜捕概觀](advanced-hunting-overview.md)
- [了解查詢語言](advanced-hunting-query-language.md)
- [使用查詢結果工作](advanced-hunting-query-results.md)
- [使用共用查詢](advanced-hunting-shared-queries.md)
- [搜捕所有裝置和電子郵件的威脅](advanced-hunting-query-emails-devices.md)
- [套用查詢最佳做法](advanced-hunting-best-practices.md)
