---
title: 準備識別碼清單在 Office 365 中的內容搜尋的 CSV 檔案
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: 使用 Results.csv 或未編製索引的 Items.csv 檔案從現有的內容搜尋來建立識別碼清單搜尋會傳回特定的電子郵件。 識別碼清單搜尋通常用來傳回已局部編製索引的信箱項目。
ms.openlocfilehash: 4b28032761961dcac03a15de216e29253f4ab430
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37076446"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a>準備識別碼清單在 Office 365 中的內容搜尋的 CSV 檔案

您可以搜尋特定的信箱電子郵件訊息和使用 Exchange 識別碼清單的其他信箱項目。 若要建立 （正式稱為的目標式的搜尋） 的識別碼清單搜尋，您提交識別特定信箱的項目若要搜尋的逗號分隔的值 (CSV) 檔案。 此 CSV 檔案中使用**Results.csv**檔案或都包含在內，當您匯出內容搜尋結果，或從內容搜尋報表] 和 [現有的內容搜尋匯出**未編製索引的 Items.csv**檔案。 然後您編輯下列其中一個這些檔案，以指出搜尋，然後建立新的識別碼清單中搜尋並提交 CSV 檔案的特定項目。 
  
以下是建立識別碼清單中搜尋的程序的簡要概觀。
  
1. 建立並執行新的或引導式的內容搜尋中安全性 & 合規性中心。
    
2. 匯出內容搜尋結果，或匯出內容搜尋報告。 如需詳細資訊，請參閱：
    
    - [匯出內容搜尋結果](export-search-results.md)
    
    - [匯出內容搜尋報告](export-a-content-search-report.md)
    
3. 編輯**Results.csv**檔案或**未編製索引的 Items.csv**並找出您想要併入識別碼清單中搜尋特定的信箱項目。 請參閱準備識別碼清單中搜尋的 CSV 檔案的[指示](#prepare-the-csv-file-for-an-id-list-search)。 
    
4. 建立新的識別碼清單搜尋 （請參閱[指示](#create-an-id-list-search)），並提交您備妥的 CSV 檔案。 選取 CSV 檔案中的項目只會搜尋建立搜尋查詢。
    
> [!NOTE]
> 識別碼清單搜尋只支援的信箱項目。 您無法搜尋的 SharePoint 和 OneDrive 文件識別碼在列出搜尋。 
  
 **為什麼要建立識別碼清單搜尋？** 如果您無法判斷**Results.csv**或**未編製索引的 Items.csv**檔案中的中繼資料為基礎的 eDiscovery 要求回應項目時，您可以使用識別碼清單搜尋來尋找，預覽，，然後將匯出至判斷它是否表示項目回應正在調查的案例。 識別碼清單搜尋通常用來搜尋並傳回一組特定的未編製索引的項目。 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a>準備識別碼清單中搜尋的 CSV 檔案

匯出的搜尋結果或報表的內容搜尋之後，您可以執行下列步驟來準備識別碼清單中搜尋的 CSV 檔案。 此 CSV 檔案會識別每個項目識別碼清單搜尋中。
  
請注意，您可以使用 CSV 檔案從搜尋中包含 SharePoint 網站與 OneDrive 帳戶，但您可以選取*只*識別碼清單中搜尋的信箱項目。 如果您在 SharePoint 或 OneDrive 中選取文件，CSV 檔案將會失敗驗證，當您建立的識別碼清單搜尋。 
  
1. 在 Excel 中開啟 [ **Results.csv** ] 或 [**未編製索引的 Items.csv**檔案。 
    
2. 插入新欄並將其命名為 [**已選取**。 您可以在該處插入欄沒關係。 為了方便，請考慮插入左邊的第一欄。
    
3. 在 [**選取**] 欄中，輸入 **[是]** 中的儲存格，會對應至您想要搜尋的項目。 針對每個您想要搜尋的項目重複此步驟。 
    
    > [!IMPORTANT]
    > 當您在 Excel 中開啟 CSV 檔案時，**文件識別碼**] 欄中的資料格式會變更為**一般**。 這會導致科學記號中顯示項目的文件識別碼。 例如，「 481037338205 」 的 ID 會顯示為 「 4.81037E + 11"的文件必須執行接下來的步驟來變更**文件識別碼**] 欄中的資料格式**號碼**若要還原的正確格式的文件識別碼。 如果您不這樣做，使用 CSV 檔案的識別碼清單搜尋將會失敗。 
  
4. 以滑鼠右鍵按一下 [整個**文件識別碼**] 欄，然後選取 [**儲存格格式**。
    
5. 在 [**類別**] 方塊中，按一下 [**數字**。
    
6. 變更的小數位數設為**0**，，，然後按一下 **[確定]** 以儲存變更。 請注意 [文件識別碼] 欄中的值會變更為數字。 
    
    以下是範例已準備好要送出識別碼清單內容搜尋的 CSV 檔案。
    
    ![已設定目標內容搜尋的 CSV 檔案的範例](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. 儲存該 CSV 檔案，或使用**另存新檔**儲存具有不同的檔案名稱的檔案。 在這兩種情況下，務必將檔案儲存與 CSV 格式。 
  
## <a name="create-an-id-list-search"></a>建立識別碼清單搜尋

下一步是建立新的識別碼清單內容搜尋並提交您在先前步驟中備妥的 CSV 檔案。
  
> [!IMPORTANT]
> 您應該建立識別碼清單搜尋不超過 2 天後匯出內容搜尋的結果或報表。 如果搜尋結果，或報表其中匯出 2 天以上，您應該重新匯出搜尋結果或報告，以產生更新的 CSV 檔案。 然後您可以準備下列其中一個更新的 CSV 檔案，並使用它來建立識別碼清單搜尋。 
  
1. 在 [安全性 & 合規性中心，移至**搜尋** \> **內容搜尋**。
    
2. 在 [**搜尋**] 頁面上，按一下箭號下一步]![加入圖示](media/8ee52980-254b-440b-99a2-18d068de62d3.gif)**新搜尋**]，然後按一下 [**搜尋依識別碼清單**。
    
    ![按一下 [搜尋]，依識別碼清單，從新的 [搜尋] 下拉式清單](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. **識別碼清單來搜尋**彈出式視窗中，在名稱搜尋 （及選擇性描述），然後按一下 [**瀏覽]** 並在先前步驟中選取您備妥的 CSV 檔案。 
    
    Office 365 會嘗試驗證 CSV 檔案。 如果驗證失敗，會顯示錯誤訊息，可能會協助您進行疑難排解的驗證錯誤。 CSV 檔案已成功驗證，以建立識別碼清單搜尋。
    
4. 之後將 CSV 檔案驗證成功時，請按一下 [**搜尋**] 以建立識別碼清單搜尋。 
    
    以下是預估的搜尋結果並產生識別碼清單搜尋查詢的範例。
    
    ![在詳細資料窗格中的目標內容搜尋的搜尋查詢](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    請注意，[識別碼] 搜尋統計資料中顯示的估計項的目數應該符合您在 CSV 檔案中選取的項目數。
    
5. 預覽或匯出識別碼清單搜尋所傳回的項目。
    
> [!NOTE]
> 如果您將信箱移動後建立識別碼清單搜尋時，搜尋查詢將不會傳回指定的項目。 這是因為移動信箱時，會變更**DocumentId**屬性的信箱項目。 在極罕見的執行個體中移動信箱時建立的識別碼清單搜尋之後，您應該建立新的內容搜尋 （或更新現有的內容搜尋的搜尋結果），然後匯出搜尋結果或報告產生更新可用的 CSV 檔案 若要建立新的識別碼清單搜尋。 