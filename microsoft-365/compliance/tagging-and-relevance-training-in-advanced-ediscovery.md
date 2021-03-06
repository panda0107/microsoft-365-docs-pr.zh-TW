---
title: 標記與相關性訓練中 Office 365 進階電子文件探索
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 09/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 8576cc86-d51b-4285-b54b-67184714cc62
description: '了解標記的步驟，然後會使用 Office 365 進階電子文件探索的相關性訓練階段期間的訓練樣本的 40 個檔案。  '
ms.openlocfilehash: 6362aef6f4e0e17b39429dfeebca796d58d2d13e
ms.sourcegitcommit: e741930c41abcde61add22d4b773dbf171ed72ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/07/2020
ms.locfileid: "42557713"
---
# <a name="tagging-and-relevance-training-in-advanced-ediscovery-classic"></a>標記與相關性訓練中進階電子文件 （傳統）

> [!NOTE]
> 進階電子文件探索需要具有進階合規性附加元件的 Office 365 E3，或適用於您組織的 E5 訂閱。如果您沒有該方案，且想要嘗試進階電子文件探索，您可以[註冊 Office 365 企業版 E5 試用版](https://go.microsoft.com/fwlink/p/?LinkID=698279)。 
  
本主題說明使用進階電子文件相關性訓練模組的程序。 
  
進階電子文件，來完成評估，並輸入相關性訓練階段後，會將 40 個檔案的訓練範例帶入用於標示 [標記] 索引標籤。 
  
## <a name="performing-relevance-training"></a>執行相關性訓練

1. 在**相關性\>標籤**] 索引標籤，[標記] 窗格中顯示的左的窗格及顯示檔案的範例中的預設值，用於標示一次一個。 
    
    ![相關性標籤面板](../media/0cf19ab4-b427-4a7f-8749-0f4ed9afaf58.png)
  
    在 [**標籤**] 索引標籤會顯示檔案的顯示名稱。 這可能是路徑、 電子郵件主旨、 標題、 或使用者定義的名稱。 ID、 檔案路徑或文字路徑可以被複製檔案的路徑上按一下滑鼠右鍵。 
    
    標記統計資料顯示 [**標籤**] 索引標籤 （在左邊窗格的頂端） 檔案範例編號、 超出檔案總數 （右窗格的底部），本範例在目前顯示的檔案數目及目前在範例中 （底部的左窗格），它變更為您的標記檔案總數標記檔案。 這適用於任何相關性標記中評估、 訓練、 Catch-up 或測試是否完成。 
    
    表示註解、 標記和家庭檔案存在的圖示會顯示在 [檔案] 檢視中的列上方檔案。
    
2. 決定檔案的相關性案例問題和標記，如下表所示，使用 [標記] 選項圖示按鈕或 [鍵盤快速鍵等，該檔案：

|**標記] 選項**|**描述**|**鍵盤快速鍵**|**多個問題-大量標記鍵盤快速鍵**|
|-----|-----|-----|-----|
|R  <br/> |相關  <br/> |Z  <br/> |Shift + Z  <br/> |
|編號  <br/> |不相關  <br/> |X  <br/> |Shift + X  <br/> |
|略過  <br/> |略過  <br/> |C  <br/> |Shift + A  <br/> |
   
  - 當之後標記一個問題，多個問題存在於檔案中，選取範圍移至下一個問題 （如果有的話）。 
    
  - 反白顯示關鍵字時，由系統管理員或案例管理員所定義的關鍵字 (相關性設定\>以反白顯示關鍵字)，將顯示 （在指定的色彩），以協助識別相關的檔案時標記。 如果關鍵字都有雙底線，它可以按下顯示的關鍵字描述的工具提示。 
    
    （選用) 在 [**標籤**] 索引標籤中，按一下 [**標記設定**來設定下列選項： 
    
    ![相關性標籤設定](../media/533e89fa-7eb4-409e-ab07-f5aab9296dd8.png)
  
  - **大量標記**： 使用此選項可透過選取**所有**設定的所有問題 （覆寫已標記問題） 選取的檔案的標籤或選取**其餘**的其餘的無標記問題套用標籤指派多個問題的檔案。 所選取的選項保持作用中的所有使用者的情況下變更該使用者，才能 （設定為每位使用者的所有使用者的情況下）。 
    
  - **自動標記**： 選取此核取方塊，可為 [未設定其他問題的檔案相關之後單一相關標記。
    
  - **自動換頁**： 選取此核取方塊可將顯示的檔案選取範圍移動至下一個檔案，標記的最後一筆或僅無標記的問題時。 
    
    略過的檔案不會被視為相關性訓練和相關性分數用途。
    
3. 任意文字註解相關聯的檔案，可以檢視及編輯透過在左的窗格中的下拉式清單] 清單中的 [**註解**] 選項。 （選用） 
    
4. 在左的窗格中的下拉式清單] 清單中選取 [**標記準則**] 選項可檢視標記的指導方針。 
    
5. 完成 [標記] 清單中的所有檔案後，當您準備好要計算結果時，按一下 [**計算**]。 會顯示 [**追蹤**] 索引標籤。 
    
## <a name="working-with-the-sample-files-list"></a>使用範例檔案清單

範例檔案清單可讓您檢視訓練範例中的檔案清單，並在一或多個檔案上執行各種動作。 在 [**相關性** \> **標籤**] 索引標籤，**範例檔案**左邊的窗格會顯示範例檔案，如評估、 與訓練、 Catch-up，不一致的處理程序的清單。 
  
1. 在**相關性\>標籤**索引標籤上，選取左的窗格下拉式清單中的範例檔案。 在左窗格中列出的範例檔案。 
    
    ![相關性標籤範例檔案清單](../media/fd058bdd-645a-4af1-a1eb-bff08581cb18.png)
  
2. 藉由輸入或選取其數字**範例**或**檔案**] 方塊中選取一個特定的範例或檔案數目。 
    
  -   - 檔案序列數字會列在左邊欄位的 [**標籤**] 索引標籤上的顯示的檔案清單。藉由按一下標頭，檔案的原始顯示的順序傳回至其原始的順序。 
    
  - 在 [檔案] 列上按一下右窗格中顯示其內容。
    
  - 瀏覽之間檔案範例中，目前使用較低的功能表列選項。 此外，瀏覽的鍵盤快速鍵可用：
    
    瀏覽至第一個檔案中的範例： Shift + Ctrl +\<
    
    瀏覽至範例中的前一個檔案： Shift +\<
    
    瀏覽至範例中的下一個檔案： Shift +\>
    
    瀏覽至最後一個範例中的檔案： Shift + Ctrl +\>
    
## <a name="see-also"></a>請參閱

[進階電子文件 （傳統）](office-365-advanced-ediscovery.md)
  
[了解相關性評估](assessment-in-relevance-in-advanced-ediscovery.md)
  
[標記與評估](tagging-and-assessment-in-advanced-ediscovery.md)
  
[追蹤相關性分析](track-relevance-analysis-in-advanced-ediscovery.md)
  
[決定根據結果](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[測試相關性分析](test-relevance-analysis-in-advanced-ediscovery.md)

