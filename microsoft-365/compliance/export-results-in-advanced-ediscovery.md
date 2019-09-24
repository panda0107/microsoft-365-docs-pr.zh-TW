---
title: 在 Office 365 進階電子文件探索中匯出結果
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: '了解如何定義從 Office 365 進階電子文件探索，包括指定參數匯出批次的程序中匯出結果的選項。 '
ms.openlocfilehash: ad11ac742f3157811523164c7e4d063e1d101343
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37077031"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a>在 Office 365 進階電子文件探索中匯出結果

> [!NOTE]
> 進階電子文件探索需要具有進階合規性附加元件的 Office 365 E3，或適用於您組織的 E5 訂閱。如果您沒有該方案，且想要嘗試進階電子文件探索，您可以[註冊 Office 365 企業版 E5 試用版](https://go.microsoft.com/fwlink/p/?LinkID=698279)。 
  
本主題說明 [進階電子文件探索匯出設定] 選項。
  
 **本主題內容：**
  
- [定義匯出批次和工作階段](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [增量和其他匯出](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [設定批次匯出參數](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [匯出報告輸出檔案](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a>定義匯出批次和工作階段
<a name="BK_Define"> </a>

匯出批次允許匯出處理使用一組已定義的參數。 進階電子文件可讓您定義自訂每個匯出批次。
  
參數會定義每個匯出批次。 案例的第一個批次的預設會建立名為 「 匯出批次 01 」 批次。 您也可以編輯的批次名稱和描述。
  
匯出工作階段是進階電子文件探索匯出匯出批次內執行。
  
## <a name="incremental-and-additional-exports"></a>增量和其他匯出
<a name="BK_IncrementalReports"> </a>

您可以執行匯出批次，以確保結果一致根據相同的匯出範本和參數中的多個匯出工作階段。 為一個批次中每個工作階段，您可以匯出分析的新處理案例資料，並且處理每個 「 逐漸 」。
  
若要匯出使用一組不同的參數，必須先建立新的批次。 在新的批次中的第一個工作階段會產生檔案的情況下到目前為止，處理，不論這些檔案所匯入，並透過一或多個匯入處理的結果。 樞紐分析表、 相似性、 inclusives 等，會重新計算每個批次。工作階段使用批次所定義的參數，並不會計算樞紐分析表、 相似性、 inclusives 等針對每個工作階段執行。
  
例如，假設情況已匯入且其資料分析。 若要擷取接近重複項目和電子郵件執行緒增量資料的結果，請按一下 [先前用來將資料匯出同一個批次中的 [**建立匯出工作階段**]。 
  
## <a name="set-up-batch-export-parameters"></a>設定批次匯出參數
<a name="BK_SetUpExport"> </a>

EDiscovery 匯出工具用來從進階電子文件的搜尋結果匯出到本機電腦。 若要增加資料傳輸輸送量並提升並匯出程序，您可以用來匯出搜尋結果的電腦上設定 Windows 登錄設定。 如果您想要增加的下載速度，設定為登錄設定的設定匯出參數之前。 如需詳細資訊，請參閱[增加匯出 eDiscovery 搜尋結果從 Office 365 時的下載速度](increase-download-speeds-when-exporting-ediscovery-results.md)。
  
1. 在 [進階電子文件，select Case，按一下 [**匯出** \> **安裝程式**。
    
    - 從**匯出批次**] 清單中，選取批次名稱，或將結果匯出至匯出批次 01、 （預設批次）。 
    
    - 若要匯出結果的新檔案新增至現有的情況下，繼續執行您目前的批次。 批次中建立工作階段、 選取相同的批次數目，並按一下 [**建立匯出工作階段**中，您可以使用此選項為前一個批次，匯出相同的參數，以累加方式。 
    
    - 若要匯出至新的批次時，按一下 [**新增**![新增圖示](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)和**批次名稱**輸入新名稱 （或接受預設值） 和 [描述] 中**批次描述**。 按一下 [確定]****。
    
    - 若要編輯的批次名稱或描述，請選取中**匯出批次**的名稱，請按一下 [**編輯**![編輯圖示](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)，然後再修改欄位。
    
      > [!NOTE]
      > 您已執行匯出批次的工作階段之後，他們無法刪除。 此外，一旦執行第一個工作階段後，可以編輯只有一些參數。 
  
    - 若要建立的重複匯出批次，請選擇 [**重複匯出批次**![建立重複的匯出批次圖示](media/3f6d5f59-e842-4946-a493-473528af0119.jpg)和在 [資訊] 面板中輸入名稱和描述重複的批次。 
    
    - 若要刪除匯出批次，請選擇 [**刪除**![刪除匯出批次圖示](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)。
    
    - 若要檢視的批次歷程記錄，請選擇 [**批次歷程記錄**![檢視歷程記錄圖示](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)。
    
2. [**母體**，選取**包含上述相關性截止分數的檔案**及/或**精簡匯出批次**如果您想要微調您匯出批次的設定。 
    
3. 如果您選取**包含上述相關性截止分數的檔案**，然後會啟用**問題**。 如果檔案的相關性分數是高於所選問題的截止分數，除非它排除 '進行檢閱' 篩選器，將會匯出檔案。 
  
    如果您選取 [**精簡匯出批次**，**取消 dupe**及篩選由 '的檢閱' 欄位選項按鈕隨即啟用。 如果您選擇**取消 dupe**，然後重複的檔案會根據定義的原則篩選出 [案件層級 （預設值）： 每個一組重複檔案在整個的情況下，從所有但一個檔案將會被取消 duped。 Custodian 層級： 每個一組重複檔案的相同 custodian，從所有但一個檔案將會被取消 duped。]匯出輸出中包含重複的所有檔案的記錄。 如果您選擇**的 '進行檢閱' 的篩選器**] 欄位，選取 [**修改] 底下的中繼資料**]，輸入您 **'進行檢閱'** 的欄位設定]。 選取要包含封裝內容中的來源檔案**包含的輸入的檔**。 您可以清除此設定可加速在匯出程序。 請注意的原生檔案將會在任何情況下匯出。 
    
4. [**中繼資料**，選取 [從下列選項中**匯出範本**] 清單中 （一次每個工作階段）。 
    
    - **標準**： 基本組資料的項目、 中繼資料，以及屬性。 進階 eDiscovery 中已經處理匯入資料，並將資料匯出至已經含有檔案系統上傳時，請使用此選項。 根據預設，匯出的範本建立並填入資料行。
    
    - **全部**： 包括所有處理資料，以及分析與相關性分數的標準中繼資料的完整集合。 此範本時，需要進階電子文件會執行的處理和檔案資料上載到外部系統的第一次。
    
    - **問題**： 選取 [**所有問題**，或都選取您已建立的特定問題。 
    
5. 在 [**目的地**]:
    
    - **下載到本機電腦**
    
    - **匯出至使用者定義的 Azure blob**： 如果選取此項，您可以指定容器 URL 和 SAS 權杖。
    
      > [!NOTE]
      > 一旦匯出套件儲存至使用者定義的 Azure blob、 資料不會再由進階電子文件;它是由 Azure blob 中的管理。 這表示如果您刪除這種情況，匯出的檔案都會仍保留在 Azure blob。 
  
    - **儲存 SAS 語彙基元未來匯出工作階段**： 如果選取這個選項，會被 SAS 語彙基元加密供日後使用的進階電子文件內部資料庫中。
    
      > [!NOTE]
      > 目前 SAS 語彙基元，會在一個月後到期。 如果您嘗試下載您需要復原最後一個工作階段多個月份之後，然後再次匯出。 
  
6. 按一下 [**修改]** 若要設定的 '進行檢閱'] 欄位。 
    
    ![匯出批次的檢閱欄位設定為設定](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - 在**檢閱欄位設定**，在 [**選取案例**] 下拉式清單中，選取案例和檢閱的範圍。 根據您的選取範圍所顯示的設定。
    
      - **檢閱所有**（預設值）： 依預設已選取所有的電子郵件、 附件和文件。 
    
      - **檢閱一組中的所有唯一內容**： 電子郵件中的唯一附件 Inclusives 和唯一的內含副本，設定層級，從每個一組完全重複的代表性。
    
      - **檢閱一組-無 （含） 的副本中的所有唯一內容**： Inclusives，電子郵件中的唯一附件設定層級，從每個一組完全重複的代表性。
    
      - **檢閱所有唯一內容及相關的家長監護檔案**： Inclusives，電子郵件設定層級，代表從完全重複的項目，每組中的唯一附件展開到包含系列的檔案。
    
      - **自訂**（可讓您定義的選項] 對話方塊中）： 預設值是以保留目前的選取項目，並啟用所有的對話方塊選項，允許其選取項目。 如果您選取此選項，您可以再自訂電子郵件、 文件、 附件的設定及其他。
    
    - 在 [**電子郵件**，選取您想要匯出之電子的郵件。
    
      - **所有的電子郵件**: （預設值） 會選取所有的電子郵件。
    
      - **Inclusives**: （含） 的電子郵件是否在執行緒中，最後一個電子郵件，並且包含所有其他電子郵件從執行緒。
    
      - **Inclusives 和唯一的內含副本**: （含） 的複本，並具有相同的主旨、 內文和附件; inclusives唯一內含副本是唯一的複本這些電子郵件。
    
    - 在 [**文件**，選取您想要匯出的文件。 
    
      - **所有文件**: （預設值） 會選取所有文件。
    
      - **樞紐分析表**： 選擇作為近似重複項目組，通常用於作為基準檢閱設定的具有代表性的檔案。
    
      - **從完全重複的每一組代表性**： 唯一的近似重複檔案 （包含樞紐分析表）。
    
    - 在 [**附件**]，選取您想要匯出的附件。 
    
      - **所有附件**: （預設值） 會選取所有附件。
    
      - **附件案例層級的唯一方式**： 指定案例中的唯一的附件檔案。
    
      - **電子郵件中的唯一附件設定層級**： 中指定的電子郵件案例的唯一的附件檔案。
    
   - 下**Micellaneous**，您可以選擇**將視為附件為文件**、**將視為作為文件的電子郵件**，或**展開並包括系列的檔案**。 當您選擇**展開並包括家庭檔案**，會加上旗標供檢閱每個檔案時，也被標示所有檔案的相同的家庭。
    
7. 選擇 [**儲存**] 以儲存設定。 
    
8. 指定匯出參數之後，若要啟動匯出批次，請按一下 [**建立匯出工作階段**]。
    
    在匯出期間，狀態會顯示在 [**工作狀態**。 結果會顯示在**匯出摘要**。
    
9. 在 [**檔案下載**] 視窗中，按一下 [**複製到剪貼簿**複製的匯出金鑰]。 
    
    ![下載檔案](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. 按一下 [關閉]****。 
    
    啟動 eDiscovery 匯出工具。
    
    ![eDiscovery 匯出工具](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. 在**eDiscovery 匯出工具**中：
    
    -  中**貼上共用的存取簽章，將會用來連線至來源**，請在步驟 7 中該 youcopied 到剪貼簿貼的匯出金鑰。
    
    - 按一下 [**瀏覽]** 以選取用來儲存在本機電腦上的下載的匯出檔案的目標位置。 
    
    - 按一下 [**啟動**]。匯出的檔案下載至本機電腦。 如果您在步驟 4 中所選擇**匯出至使用者定義的 Azure blob** ，工作階段會匯出到您所選擇的 Blob 儲存體 URL 目的地。
    
在 [匯出] 報告中的欄位的完整說明，請參閱[匯出報告欄位](export-report-fields-in-advanced-ediscovery.md)。
  
## <a name="export-report-output-files"></a>匯出報告輸出檔案
<a name="BK_ExportOutputFIles"> </a>

下表列出當您執行匯出批次時所產生的輸出檔案。
  
|**檔案名稱**|**檔案類型**|**描述**|
|:-----|:-----|:-----|
|匯出摘要  <br/> |csv  <br/> |EDiscovery 匯出工具所產生記錄檔。  <br/> |
|追蹤  <br/> |txt  <br/> |EDiscovery 匯出工具所產生記錄檔。  <br/> |
|擷取的文字檔案  <br/> |檔案的資料夾  <br/> |包含匯出的檔案解壓縮的文字檔案的資料夾。  <br/> |
|輸入] 或 [原生檔案  <br/> |檔案的資料夾  <br/> |包含的原生和輸入檔案的匯出檔案的資料夾。  <br/> |
|匯出清單  <br/> |xlsx  <br/> |Xlsx 格式匯出的檔案中繼資料。 若要匯出的範本使用者選取會根據檔案中的欄位。 如有需要建立一些檔案、 每個包含 100-150 K 資料列。 如果特定值會包含非 Excel 儲存格可以包含多個字元 （目前限制為 32767 個字元），然後將修剪允許的最大長度的值。 如果調整值，此儲存格的背景色彩是紅色，這表示使用者 」。電子郵件參與者 」 是可以超過此長度限制，欄位的範例，如果電子郵件已傳送至大型通訊群組。 如需詳細資訊輸出欄位，請參閱[匯出報告欄位](export-report-fields-in-advanced-ediscovery.md)。  <br/> |
|載入檔案  <br/> |csv  <br/> |其他應用程式中載入的 csv 格式匯出的檔案中繼資料。 若要匯出的範本使用者選取會根據檔案中的欄位。  <br/> |
|成功指示器  <br/> |txt  <br/> |匯出至第 3 方 Azure blob 時，才建立。 如果完全成功匯出，將會建立檔案。 如果失敗，或部分將不會建立成功檔案。 會在根資料夾中，讓上不同匯出批次/工作階段狀態的自動化的追蹤建立檔案。 這是空的檔案。 它的名稱： TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt。  <br/> |
   
## <a name="see-also"></a>另請參閱

[Office 365 進階電子文件探索](office-365-advanced-ediscovery.md)
  
[檢視批次歷程記錄及匯出過去的結果](view-batch-history-and-export-past-results.md)
  
[快速設定 Office 365 進階電子文件探索](quick-setup-for-advanced-ediscovery.md)

[匯出報告欄位](export-report-fields-in-advanced-ediscovery.md)
  
[匯出 eDiscovery 搜尋結果從 Office 365 時，增加的下載速度](increase-download-speeds-when-exporting-ediscovery-results.md)
