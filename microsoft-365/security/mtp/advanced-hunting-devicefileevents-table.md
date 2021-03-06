---
title: DeviceFileEvents 資料表中的進階的狩獵結構描述
description: 了解進階的狩獵結構描述的 DeviceFileEvents 資料表中的檔案相關的事件
keywords: 進階狩獵、 威脅狩獵、 網路威脅狩獵、 microsoft 威脅防護、 microsoft 365、 mtp、 m365、 搜尋、 查詢、 遙測、 結構描述參考、 kusto、 表格、 欄、 資料類型、 描述、 filecreationevents、 DeviceFileEvents、 檔案、 路徑雜湊、 sha1、 sha256、 md5
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
ms.openlocfilehash: 07569b93244bd420fe5961e20e6951ea84ae47d7
ms.sourcegitcommit: 74bf600424d0cb7b9d16b4f391aeda7875058be1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42235032"
---
# <a name="devicefileevents"></a>DeviceFileEvents

適用於：****
- Microsoft 威脅防護



`DeviceFileEvents` [進階的狩獵](advanced-hunting-overview.md)結構描述中的表格包含的檔案建立、 修改和其他檔案系統事件的相關資訊。 使用這個參考來建立從此表格取回之資訊的查詢。

如需進階搜捕結構描述中其他表格的資訊，[請參閱進階搜捕參考](advanced-hunting-schema-tables.md) (部分內容為機器翻譯)。

| 欄名稱 | 資料類型 | 描述 |
|-------------|-----------|-------------|
| `Timestamp` | datetime | 事件記錄的日期和時間 |
| `DeviceId` | string | 服務中電腦的唯一識別碼 |
| `DeviceName` | string | 電腦的完整網域名稱 (FQDN) |
| `ActionType` | string | 觸發事件的活動類型 |
| `FileName` | string | 記錄動作已套用的檔案名稱 |
| `FolderPath` | string | 包含已錄製的巨集指令所套用之檔案的資料夾 |
| `SHA1` | string | 記錄動作已套用的檔案 SHA-1 |
| `SHA256` | 字串 | 記錄動作已套用的檔案 SHA-256。 通常沒有填入此欄位 — 使用時可用的 SHA1 欄 |
| `MD5` | string | 錄製巨集指令所套用之檔案的 MD5 雜湊 |
| `FileOriginUrl` | string | 從何處下載檔案的 URL |
| `FileOriginReferrerUrl` | string | 下載的檔案所連結之 web 頁面的 URL |
| `FileOriginIP` | string | 從何處下載檔案的 IP 位址 |
| `InitiatingProcessAccountDomain` | string | 執行負責事件程序的帳戶網域 |
| `InitiatingProcessAccountName` | string | 執行負責事件程序的帳戶使用者名稱 |
| `InitiatingProcessAccountSid` | string | 安全性識別碼 (SID) 執行負責事件程序的帳戶 |
| `InitiatingProcessMD5` | string | 初始化事件程序 （影像檔案） 的 MD5 雜湊 |
| `InitiatingProcessSHA1` | string | SHA-1 起始之事件程序 （影像檔案） |
| `InitiatingProcessFolderPath` | string | 包含起始事件程序 （影像檔案） 的資料夾 |
| `InitiatingProcessFileName` | string | 初始化事件的處理序名稱 |
| `InitiatingProcessId` | int | 處理程序識別碼 (PID) 的起始事件程序 |
| `InitiatingProcessCommandLine` | string | 用來執行初始化事件程序的命令列 |
| `InitiatingProcessCreationTime` | datetime | 初始化事件程序時已開始日期和時間 |
| `InitiatingProcessIntegrityLevel` | string | 初始化事件程序的完整性層級。 Windows 會指派完整性層級根據若干特質程序，例如如果他們已啟動從網際網路下載。 這些完整性層級影響資源的權限 |
| `InitiatingProcessTokenElevation` | string | 指出使用者存取控制 (UAC) 提高權限套用至初始化事件程序存在的 token 型別 |
| `InitiatingProcessParentId` | int | 處理程序識別碼 (PID) 的產生處理程序負責事件父處理序 |
| `InitiatingProcessParentFileName` | string | 產生負責事件程序的父處理序名稱 |
| `InitiatingProcessParentCreationTime` | datetime | 日期和時間的父代負責事件程序已啟動時 |
| `ReportId` | long | 以重複計數器為基礎的事件識別碼。 若要識別唯一的事件，必須使用此資料行搭配 DeviceName 和時間戳記欄 |
| `AppGuardContainerId` | string | 虛擬化的容器應用程式防護用於隔離瀏覽器活動識別碼 |
| `SensitivityLabel` | string | 套用至電子郵件、 檔案或其他內容來分類資訊保護標籤 |
| `SensitivitySubLabel` | string | 子標籤套用至電子郵件、 檔案或其他內容來分類資訊保護;敏感度子標籤進行分組敏感度標籤，但分開處理 |
| `IsAzureInfoProtectionApplied` | 布林值 | 會指出是否要將檔案加密的 Azure 資訊保護 |

## <a name="related-topics"></a>相關主題
- [主動威脅搜捕](advanced-hunting-overview.md)
- [了解查詢語言](advanced-hunting-query-language.md)
- [使用共用查詢](advanced-hunting-shared-queries.md)
- [搜捕所有裝置和電子郵件的威脅](advanced-hunting-query-emails-devices.md)
- [了解結構描述](advanced-hunting-schema-tables.md)
- [套用查詢最佳做法](advanced-hunting-best-practices.md)
