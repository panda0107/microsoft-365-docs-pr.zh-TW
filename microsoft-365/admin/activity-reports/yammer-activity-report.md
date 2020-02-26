---
title: 管理中心-Yammer 活動報告中的 office 365 報告
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
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a
description: 取得 Yammer 活動報告，並深入了解張貼、 like，或閱讀的郵件使用 Yammer 的使用者數目。
ms.openlocfilehash: 0b6e7feb1d80ddc56c9ea172fa3c7e91ea0903b3
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239463"
---
# <a name="office-365-reports-in-the-admin-center---yammer-activity-report"></a>管理中心-Yammer 活動報告中的 office 365 報告

Microsoft 365 系統管理員，在**報告**儀表板會顯示您資料的組織內的產品使用情況。 請參閱[在系統管理中心的活動報告](activity-reports.md)。 **Yammer 活動報告**中，您都可以查看使用 Yammer 張貼、 like 或讀取的郵件，並產生整個組織內的活動量的唯一使用者數目來了解 Yammer 貴組織的參與程度。 
  
> [!NOTE]
> 您必須是全域系統管理員、 全域讀者或報告讀取者，在 Microsoft 365 或 Exchange、 SharePoint 或 Skype 商務系統管理員，才能查看報告。 
 
## <a name="how-to-get-to-the-yammer-activity-report"></a>如何取得 Yammer 活動報告

1. 在系統管理中心中，移至 **[報告]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">[使用量]</a> 頁面。

    
2. 從 [**選取 [報告]** 下拉式清單，選取 [ **Yammer** \> **活動**。
  
## <a name="interpret-the-yammer-activity-report"></a>解讀 Yammer 活動報告

您可以查看 [活動] 和 [使用者] 圖表以了解使用者的 Yammer 活動。
  
![Yammer 活動報告](../media/92e8b2c6-166a-4154-9824-3fb6bbedf0db.JPG)
  
活動報告中包含下列資訊。
  
- 若要檢視過去 7 天、 30 天、 前 90 天或 180 天的**Yammer 活動**] 趨勢報告使用天數索引標籤。 不過，如果您在報表中選取的特定一天，表格會顯示資料 28 天，從目前的日期 （不是該報告產生的日期）。 
    
- 每份報告都具有報告產生時的日期。 報告反映出的資料通常會有 24 至 48 小時的延遲 (自活動時間起算)。
    
- 您可以檢視 [**活動**] 圖表以了解您的組織中的 Yammer 活動數量的趨勢。 您可以了解張貼訊息、閱讀訊息及對訊息按讚的個別數據。 
    
    ![Yammer 活動報告中的 [活動] 檢視](../media/76983516-2c5f-43a1-a5e3-c414e9f17638.JPG)
  
  - 在 [**活動**] 圖表中，Y 軸是活動的訊息張貼]、 [讀取] 或按讚的計數。 
    
- 您可以檢視 [**使用者**] 圖表以了解正在產生 Yammer 活動的唯一使用者數量的趨勢。 您可以查看使用者張貼、閱讀或對 Yammer 訊息按讚的趨勢。 
    
    ![Yammer 活動報告中的 [使用者] 檢視](../media/b1098162-7b79-430f-bfe4-9d3957d56885.JPG)
  
  - 在 [**使用者**] 活動圖表中，Y 軸是使用者張貼、 閱讀或獲得聲望 Yammer 訊息。 
    
  - 這兩份圖表的 X 軸都代表該特定報告的已選取日期範圍。
    
- 您可以篩選看圖表所選取項目在圖例中的數列。 例如，在 [**活動**] 圖表中，選取 [**已張貼**、**讀取**、 或**Liked**以查看只與其個別相關的資訊。 
    
    ![已張貼、 讀取、 和按讚] 選項](../media/8b832afc-415c-409b-816f-cb02b7a71e69.png)
  
    變更此選取項目並不會變更格線表格中的資訊。
    
- 圖表底下的表格顯示每個使用者層級的 Yammer 活動明細。
    
    您可以使用功能表來篩選和排序資料。
    
    ![對於 Yammer 報表的功能表選項](../media/9d32240c-f1ff-400b-9c4e-a21b48651530.JPG)
  
    您也可以新增和移除欄位。 可用的欄位如下︰
    
  - **Username**是使用者的電子郵件地址。 您可以顯示實際的電子郵件地址，也可以讓此欄位匿名。 
    
    此格線會顯示使用 Office 365 帳戶登入 Yammer 的使用者，或使用單一登入功能登入網路的使用者。
    
  - **顯示名稱**是使用者的完整名稱。 您可以顯示實際的名稱，也可以讓此欄位匿名。 
    
  - **使用者狀態**是三個值之一： 啟動，刪除的郵件，或暫停。 
    
    這些報告顯示作用中、已停權及已刪除的使用者。報告不會反映出擱置中使用者，因為擱置中的使用者不能張貼訊息、閱讀訊息或對訊息按讚。
    
  - **狀態變更日期 (UTC)** 是在其的使用者狀態已變更 Yammer 中的日期。 
    
  - **[上次活動日期 (UTC)** 是指的最後一個日期使用者張貼、 閱讀，或按讚的訊息。 
    
  - **「 已張貼**是使用者在您指定時間期間內張貼的訊息數目。 
    
  - **讀取**是使用者在您指定的期間讀取的交談數目。 
    
  - **Liked**是您指定使用者在時間期間內按讚的訊息數目。 
    
  - **產品指派**是指派給此位使用者的產品。 
    
    如果貴組織的原則防止您檢視可識別之使用者資訊的報告，您可以變更所有這類報告的隱私權設定。 請參閱**如何隱藏使用者層級的詳細資訊？** [在 Microsoft 365 系統管理中心的活動報告](activity-reports.md)中的一節。
    
- 您可以也報告資料匯出到 Excel.csv 檔案，藉由選取 [**匯出**] 連結。 這會匯出所有使用者的資料，並可讓您進行簡單的排序和篩選，以便進一步分析。 如果您的使用者少於 2000 個，您可以直接在報告中的表格內進行排序和篩選。 如果您的使用者多於 2000 個，則需要匯出資料才能進行排序和篩選。 
    
## <a name="what-data-is-in-these-reports"></a>這些報告中有哪些資料？

- **所有用戶端**這些報告彙總所有用戶端，包括在瀏覽器中或在 iOS 或 Android 應用程式上使用 Yammer 總資料。 
    
- **無外部網路資料**這些報告中未包含外部網路資料。 
    
- **已啟用的網路**這些報告顯示是 Office 365 訂閱的一部分的 Yammer 網路的資料。 圖表會彙總所有登入 Yammer 網路的使用者使用情況，不論他們使用 Office 365 還是 Yammer 登入。 
    
