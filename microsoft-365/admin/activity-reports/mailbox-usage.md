---
title: Microsoft 365 報告在系統管理中心的 [信箱使用量
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: beffbe01-ce2d-4614-9ae5-7898868e2729
description: 了解如何取得信箱使用量報表來了解與使用者信箱的使用者活動。
ms.openlocfilehash: d7d36359801fe72ac1c3ffc210c7795030f0b2e2
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239167"
---
# <a name="microsoft-365-reports-in-the-admin-center---mailbox-usage"></a>Microsoft 365 報告在系統管理中心的 [信箱使用量

**信箱使用量報表**會提供使用者與使用者信箱的相關資訊和活動的個別電子郵件傳送、 讀取、 為基礎的層級建立約會、 傳送會議邀請、 接受會議、 拒絕會議取消會議活動。 它也提供各個使用者信箱已耗用多少儲存空間，以及其中有多少即將接近儲存空間配額等相關資訊。 
  
> [!NOTE]
> 您必須是全域系統管理員、 全域讀者或報告讀取者，在 Microsoft 365 或 Exchange、 SharePoint 或 Skype 商務系統管理員，才能查看報告。 
 
## <a name="how-to-get-to-the-mailbox-usage-report"></a>如何查看信箱使用量報表

1. 在系統管理中心中，移至 **[報告]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">[使用量]</a> 頁面。

    
2. 從 [**選取 [報告]** 下拉式清單，選取 [ **Exchange** \> **信箱使用量]**。
  
## <a name="interpret-the-mailbox-usage-report"></a>解讀信箱使用量報表

您可以透過檢視您的組織**信箱使用量**查看**信箱**、**儲存**及**配額**] 圖表。 
  
|||
|:-----|:-----|
|1.  <br/> |[**信箱使用量**] 報告可檢視的趨勢，過去 7 天、 30 天、 前 90 天或 180 天。 不過，如果您在報表中選取的特定一天，表格會顯示資料 28 天，從目前的日期 （不是該報告產生的日期）。  <br/> |
|2.  <br/> |每個報告中的資料通常涵蓋的最後一個 24 到 48 小時。  <br/> |
|3.  <br/> |[信箱] 圖表顯示貴組織中的使用者信箱總數量，以及在任何指定的報表天數期間內為使用中狀態的總數量。 使用者信箱會被視為作用中，如果它有電子郵件傳送、 讀取、 建立約會、 傳送會議邀請、 接受會議、 拒絕會議和取消會議活動。  <br/> |
|4.  <br/> |**儲存空間**] 圖表顯示貴組織中使用您的儲存空間量。 儲存空間] 圖表不包括封存信箱。 如需自動展開封存，請參閱[Microsoft 365 中的無限制封存概觀](https://docs.microsoft.com/office365/securitycompliance/unlimited-archiving)。<br/> |
|5.  <br/> | [**配額**] 圖表會顯示使用者的信箱數目中每個配額類別。 有以下四種配額類別：  <br/>  良好 - 已使用的儲存空間低於發出警告配額的使用者人數。  <br/>  警告 - 已使用的儲存空間等於或高於發出警告，但低於禁止傳送配額的使用者人數。  <br/>  無法傳送 - 已使用的儲存空間等於或高於禁止傳送配額，但低於禁止傳送/接收配額的的使用者人數。  <br/>  無法傳送/接收 - 已使用的儲存空間等於或高於禁止傳送/接收資料的使用者人數。  <br/> |
|6.  <br/> | 在 [**信箱**] 圖表中，Y 軸是使用者信箱的計數。  <br/>  **儲存**在圖表上，Y 軸是您組織中的使用者信箱所使用的儲存空間量。  <br/>  在 [**配額**] 圖表中，Y 軸是在每個儲存空間配額的使用者信箱數目。  <br/>  [信箱] 和 [儲存空間] 圖表的 X 軸代表該特定報表的已選取日期範圍。  <br/>  [配額] 圖表的 X 軸代表配額類別。  <br/> |
|7.  <br/> |您可以篩選您會看到所選取項目在圖例中的圖表。  <br/> |
|8.  <br/> | 表格顯示每個使用者層級的信箱使用量明細。 您可以新增其他欄到表格中。  <br/> **使用者名稱**是使用者的電子郵件地址。  <br/> **顯示名稱**為的完整名稱，如果使用者。  <br/> **已刪除**指的是其目前狀態已刪除，但在報表的報表期間的某些部分期間是作用中的信箱。  <br/> **已刪除日期**是信箱已刪除的日期。  <br/> **建立日期**是信箱的建立的日期。  <br/> **[上次活動日期**指的是信箱有電子郵件傳送或讀取活動的日期。  <br/> **項目計數**] 代表信箱中的項目總數。  <br/> **使用的儲存空間 (MB)** 是指使用的總儲存空間。  <br/> **刪除項目計數**是指在信箱中刪除的項目總數。 <br/> **刪除項目大小 (MB)** 是指在信箱中所有已刪除的項目總大小。 <br/> 是指**發出警告] 配額 (MB)** 的儲存空間限制，但信箱擁有者會收到警告，它是即將到達儲存空間配額。  <br/> **禁止傳送配額 (MB)** 是指的儲存空間限制，當信箱就無法再傳送電子郵件。  <br/> **禁止傳送接收配額 (MB)** 是指的儲存空間限制，當信箱可以無法再傳送或接收電子郵件。  <br/>  如果貴組織的原則防止您檢視可識別之使用者資訊的報告，您可以變更所有這類報告的隱私權設定。 查看 [**隱藏報告中的使用者詳細資料**] 區段中[的 Microsoft 365 系統管理中心的活動報告](activity-reports.md)中。  <br/> |
|9.  <br/> |您可以也報告資料匯出到 Excel.csv 檔案，藉由選取 [**匯出**] 連結。  <br/> |
|||
   
