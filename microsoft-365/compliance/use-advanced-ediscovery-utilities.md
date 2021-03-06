---
title: 使用 Office 365 進階電子文件探索公用程式
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: '了解 Office 365 進階電子文件探索，包括大小寫的記錄檔中的公用程式、 清除資料、 處理錯誤，修改相關性和透明度分析。  '
ms.openlocfilehash: ce8eb00382bd6ff0514dfef99d18a8e4b2679cec
ms.sourcegitcommit: e741930c41abcde61add22d4b773dbf171ed72ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/07/2020
ms.locfileid: "42557653"
---
# <a name="use-advanced-ediscovery-classic-utilities"></a>使用進階電子文件 （傳統） 公用程式

> [!NOTE]
> 進階電子文件探索需要具有進階合規性附加元件的 Office 365 E3，或適用於您組織的 E5 訂閱。如果您沒有該方案，且想要嘗試進階電子文件探索，您可以[註冊 Office 365 企業版 E5 試用版](https://go.microsoft.com/fwlink/p/?LinkID=698279)。 
  
顯示且可使用進階電子文件中的公用取決於內容和使用者角色。
  
## <a name="case-log"></a>案例的記錄檔

案例的記錄檔提供應用程式的處理活動，可用於疑難排解的追蹤，以及解決錯誤和警告的詳細的清單。 記錄檔可以產生並儲存在本機上的主應用程式或伺服器，或直接傳送到電子郵件地址。
  
記錄檔也可以下載至用戶端電腦。 用戶端下載選項可能會啟用或停用根據組態及使用者角色。
  
1. 在功能表列中，按一下 [ **Cogwheel**圖示。 
    
2. 在**設定和公用程式\>公用程式**索引標籤上，選取 [**案例記錄\>安裝**。
    
3. 選取**記錄層級**如下所示： 
    
  - **標準**： 包含的基本記錄資料。 此選項通常需要針對監視，且應該使用，除非否則建議。
    
  - **最少**： 用於非常大型的情況下，並只傳回的最新資料。
    
4. 按一下 [**執行案例記錄檔**。 產生記錄檔，並顯示路徑。 在 [工作狀態] 窗格中會顯示目前和最後一個任務的任務進度資訊。
    
## <a name="clear-data"></a>清除資料

必要時刪除或重新初始化案例資料，必須被初始化的資料庫執行個體。 清除資料公用程式會刪除所有指定的項目從案例資料庫、 文字檔、 案例] 資料夾和累積的結果。 函式只能由系統管理員執行。
  
> [!IMPORTANT]
> 此巨集指令可還原並不會清除所有的相關性標記和專家使用者所執行的分析。 如有必要，請儲存資料的備份。 極端小心使用此選項。 刪除標記及排名檔案可能會影響相關性結果。 
  
1. 在功能表列中，按一下 [ **Cogwheel**圖示。 
    
2. 在**設定和公用程式\>公用程式**索引標籤上，選取 [**清除資料\>安裝**。
    
3. 選取的選項。 若要初始化的資訊：
    
  - **相關性**： 刪除完成相關性，包括定義負載及要載入的檔案關聯中的所有工作。 它會刪除所有範例和標記。
    
  - **近似重複項目和電子郵件執行緒**： 刪除所有分析資訊的近似重複項目和電子郵件執行緒。
    
  - **佈景主題**： 刪除佈景主題相關的資料。
    
  - **匯出歷程記錄**： 刪除的匯出批次歷程記錄資訊。
    
4. 按一下 [**清除資料**。 案例資料被清除。 在 [**工作狀態**] 窗格中會顯示目前和最後一個任務的任務進度資訊。 
    
## <a name="modify-relevance"></a>修改相關性

本節說明如何將略過或回復相關性樣本。
  
1. 在功能表列中，按一下 [ **Cogwheel**圖示。 
    
2. 在**設定和公用程式\>公用程式**索引標籤上，選取 [**修改相關性**。
    
3. 從選項進行選取： 
    
  - **略過目前範例-目前的使用者**： 這會標記，以**略過**，執行此公用程式的使用者開啟案例範例中的所有無標記的檔案。 相關性處理將不會標示為**略過**的檔案上執行。
    
  - **略過目前範例對所有開啟的範例**： 這會加上標籤，以**略過**，所有無標記的檔案所有開啟的範例中的所有使用者。 如果使用者目前已標記範例，是不建議使用此選項。
    
  - **回復最後一個範例**： 上次完成的相關性訓練範例將會回復，不論其是否之前或之後的 「 計算 」 程序。 不允許執行更新性樣本的復原。
    
4. 按一下 [**執行**]，以執行。 
    
## <a name="transparency-analysis"></a>透明度分析

透明度分析公用程式可讓詳細的檢視的檔案和其指派的相關性分數。 報表可用是例行性檢查或比較人性化與相關性指派進階電子文件檢閱者所定義的檔案的相關性。 
  
除了相關性分數，進階電子文件會計算，並指派考慮關鍵字內容的關鍵字加權。 檔案的相同字可被指派不同的權數，根據內容及位置。 使用色彩濃度範圍從黃色深橙色和 varying 灰網底的增加刻度標記每個關鍵字。 色彩編碼用來以視覺方式表示 [word 的相對的相關性分數的正數或負比重。 
  
在多個問題案例案例中，就會產生透明度分析報告每個問題。
  
1. 在功能表列中，按一下 [ **Cogwheel**圖示。 
    
2. 在**設定和公用程式\>公用程式**索引標籤上，選取 [**透明度分析\>安裝**。
    
3. 在 [* * 檔案識別碼 * *，輸入檔案的檔案識別碼，處理程序。
    
4. 在 [**問題**] 清單中，選取相關的問題。 
    
5. 按一下 [**透明度分析**。 完成時，會顯示檔案的透明度分析報告，它會顯示特別標示的關鍵字色彩與整體的相關性分數的相互關聯。
    
## <a name="see-also"></a>請參閱

[進階電子文件 （傳統）](office-365-advanced-ediscovery.md)
  
[定義案例與租用戶設定](define-case-and-tenant-settings-in-advanced-ediscovery.md)

