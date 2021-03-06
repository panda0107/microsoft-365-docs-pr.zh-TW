---
title: 在 Microsoft Edge 中使用 Office 365 eDiscovery 匯出工具
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 您必須啟用 ClickOnce 支援，才能使用最新版的 Microsoft Edge 從內容搜尋和 eDiscovery 的安全性與合規性中心下載搜尋結果。
ms.openlocfilehash: 80924b124521b24ffabf1e0273802265cd715500
ms.sourcegitcommit: 01ead889086ecc7dcf5d10244bcf67c5a33c8114
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/17/2020
ms.locfileid: "42710342"
---
# <a name="use-the-office-365-ediscovery-export-tool-in-microsoft-edge"></a>在 Microsoft Edge 中使用 Office 365 eDiscovery 匯出工具

由於最近的 Microsoft Edge 版本變更，因此預設不再啟用 ClickOnce 支援。 若要繼續使用 Microsoft Office 365 eDiscovery 匯出工具下載內容搜尋或 eDiscovery 搜尋結果，您需要使用[Microsoft Internet Explorer](https://support.microsoft.com/help/17621/internet-explorer-downloads)或在最新版的 microsoft Edge 中啟用 ClickOnce 支援。

## <a name="enable-clickonce-support-in-microsoft-edge"></a>在 Microsoft Edge 中啟用 ClickOnce 支援

1. 在 Microsoft Edge 中，移至**edge://flags/#edge-按一下一次**。

2. 在下拉式清單中，如果現有的值設為**Default**或**Disabled** ，請將其變更為**Enabled**。

   ![](../media/ClickOnceimage1.png)

3. 向下滾動至瀏覽器視窗底部，然後按一下 [**重新開機**] 重新開機 Edge。

   ![](../media/ClickOnceimage2.png)

**附注：** 組織可以使用「群組原則」來停用 ClickOnce 支援。 若要檢查是否有 ClickOnce 支援的組織原則，請移至**edge://policy**。 下列螢幕擷取畫面顯示整個組織內啟用 ClickOnce。 如果此原則值設定為**false**，您將需要與組織中的系統管理員聯繫。

![](../media/ClickOnceimage3.png)

## <a name="install-and-run-the-ediscovery-export-tool"></a>安裝並執行 eDiscovery 匯出工具

1. 在 [內容搜尋] 或 [eDiscovery 案例] 中，按一下 [匯出] 之飛入頁面上的 [**下載結果**]。

   ![按一下彈出頁面上的 [下載結果] 以下載搜尋結果](../media/ClickOnceExport1.png)

2. 系統會提示您確認啟動工具，請按一下 [**開啟**]。

   ![按一下 [開啟] 以啟動 eDiscovery 匯出工具](../media/ClickOnceimage4.png)

   如果未安裝 Microsoft Office 365 eDiscovery 匯出工具，系統會提示您顯示安全性警告。 

   ![按一下 [安裝] 以安裝 eDiscovery 匯出工具](../media/ClickOnceimage5.png)

3. 按一下 [安裝]****。 安裝完畢後，會自動啟動 [匯出工具]。

如需詳細資訊，請參閱下列主題：

- [匯出內容搜尋結果](export-search-results.md)

- [如何在 Microsoft Edge 中啟用實驗旗標](https://microsoftedgesupport.microsoft.com/hc/articles/360034075294-How-to-enable-experiment-flags-in-Microsoft-Edge-Insider-channels)
