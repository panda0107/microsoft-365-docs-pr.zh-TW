---
title: 在安全性 & 合規性中心的內容搜尋的限制
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 78fe3147-1979-4c41-83bb-aeccf244368d
description: '了解作用中的 Office 365，例如同時搜尋的最大數目安全性 & 規範中心中的內容搜尋功能的限制。 '
ms.openlocfilehash: 6933fcb2a7b54c3617b2c01d54fa50fa4955ead2
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37076216"
---
# <a name="limits-for-content-search-in-the-security--compliance-center"></a>在安全性 & 合規性中心的內容搜尋的限制

> [!NOTE]
> 本主題中的限制會與 Exchange Online 中的就地 ediscovery 和 SharePoint Online 中的 eDiscovery 中心的目前限制不同。 
  
各種限制會套用至安全 & 與規範中心中的內容搜尋功能。 這包含搜尋執行**內容搜尋**頁面，並與 eDiscovery 案例相關聯的搜尋。 這些限制有助於維持的健康狀況和 Office 365 組織所提供的服務品質。 也有一些與編製索引的電子郵件訊息在 Exchange Online 的搜尋相關的限制。 您無法修改的內容搜尋或電子郵件編製索引限制，但您應該要知道它們，讓您可以考慮這些限制時規劃、 執行和疑難排解內容搜尋。 
  
## <a name="content-search-limits"></a>內容搜尋限制

下表列出安全性 & 合規性中心中的搜尋限制。
  
|**限制說明**|**限制**|
|:-----|:-----|
|信箱或可搜尋的單一內容搜尋中的網站數目上限  <br/> |無限制  <br/> |
|在您組織中的同一時間可執行內容搜尋數目上限。  <br/> |無限制  <br/> |
|單一使用者可以在同一時間開始的內容搜尋數目上限。 請注意，此限制最有可能叫用時當使用者嘗試使用啟動多個搜尋**Get-compliancesearch \| Start-compliancesearch**安全性 & 合規性中心 PowerShell 中的命令。  <br/> |10   <br/> |
|每個使用者信箱時預覽內容搜尋結果的預覽頁面顯示的項目數目上限。  <br/> |100  <br/> |
|在預覽內容搜尋結果時，會顯示在預覽頁面的所有使用者信箱中找到的項目數目上限。 顯示最新的項目。  <br/> |1,000  <br/> |
|可以預覽搜尋結果中的使用者信箱數目上限。 如果有超過 1000 個信箱包含符合搜尋查詢的內容，在大部分的搜尋結果只上方 1000 個信箱將會為可供預覽。  <br/> |1,000  <br/> |
|SharePoint 和 OneDrive for Business 網站預覽內容搜尋結果時顯示在 [預覽] 頁面上找到的項目數目上限。 顯示最新的項目。  <br/> |200  <br/> |
|（在 SharePoint 和商務用 OneDrive） 可以預覽搜尋結果的網站數目上限。 如果有 200 個以上的總網站包含符合搜尋查詢的內容，只有前 200 網站在大部分的搜尋結果將可供預覽。  <br/> |200  <br/> |
|每個公用資料夾信箱時預覽內容搜尋結果的預覽頁面顯示的項目數目上限。  <br/> |100  <br/> |
|在預覽內容搜尋結果時，會顯示在預覽頁面的所有公用資料夾信箱中找到的項目數目上限。  <br/> |200  <br/> |
|公用可以預覽搜尋結果中的信箱數目上限。 如果有超過 500 個公用資料夾信箱包含符合搜尋查詢的內容，只上方 500 個公用資料夾信箱在大部分的搜尋結果將會為可供預覽。  <br/> |500  <br/> |
|內容搜尋的搜尋查詢 （包括運算子和條件） 的字元數目上限。  <br/><br/> **附註：** 此限制查詢擴充時，這表示查詢將會取得展開針對每個關鍵字之後，才會生效。 例如，如果在搜尋查詢有 15 關鍵字和額外的參數和條件，查詢取得展開 15 次，每個都有的其他參數和在查詢條件。 因此即使下方限制可能會在搜尋查詢中的字元數，它會是超過此限制可能會導致擴充的查詢。  <br/> |**信箱：** 10000  <br/> **網站：** 4000 搜尋最多 20 個網站<sup>1</sup>時，搜尋所有的網站] 或 [2000 <br/> |
|變化時所要搜尋的搜尋查詢中或精準字詞使用前置詞萬用字元和**NEAR**或**ONEAR**布林運算子使用前置詞萬用字元時，傳回的最大數目。  <br/> |10000 <sup>2</sup> <br/> |
|前置詞萬用字元; alpha 字元數下限例如， `time*`、 `one*`，或`set*`。  <br/> |3  <br/> |
|您可以刪除內容搜尋中的信箱數目上限中的項目執行動作的 「 搜尋及清除 」 動作 (使用**New-compliancesearchaction-清除**命令)。 如果您正在執行清除巨集指令的 [內容搜尋具有多個來源信箱超過此限制，清除動作將會失敗。 如需搜尋及清除的詳細資訊，請參閱[搜尋並刪除 Office 365 組織中的電子郵件訊息](search-for-and-delete-messages-in-your-organization.md)。  <br/> |各 50000 個  <br/> |
   
> [!NOTE]
> <sup>1</sup>搜尋 SharePoint 和 OneDrive for Business 位置時, 要搜尋的網站 Url 中的字元都會列入計算對此限制。 <br/> <sup>2</sup>非片語查詢 （不會使用雙引號關鍵字值） 我們會使用特殊的前置字元索引。 這會告知我們，word 就會發生在文件，但不是其中它就會發生在文件。 若要執行的片語查詢 （雙引號的關鍵字值），我們需要比較內文件中的字片語中的位置。 這表示，我們不能使用的前置字元索引片語查詢。 在此情況下，我們在內部依序展開 [與所有可能的字前置詞會展開成; 查詢例如，`"time*"`可以展開至`"time OR timer OR times OR timex OR timeboxed OR …"`。 10000 是變體 word 可以展開至不符合查詢的文件數目的最大數目。 非片語字詞沒有上限。 
  
## <a name="indexing-limits-for-email-messages"></a>編製索引的電子郵件的限制

下表說明的索引限制，可能會導致電子郵件訊息所傳回做為未編製索引的項目或內容的搜尋結果中的已局部編製索引項目。
  
|**索引限制**|**最大值**|**描述**|
|:-----|:-----|:-----|
|附件大小上限 （不含 Excel 檔案）  <br/> |150 MB  <br/> |會將剖析為編製索引的電子郵件附件的大小上限。 任何大於此限制的附件不會被剖析為編製索引，並包含附件的郵件會被標示為已局部編製索引。  <br/> <br/>**附註：** 剖析是其中的索引服務從附件擷取文字移除不必要的字元，像是標點符號和空格，，然後將文字插入文字 （以處理程序呼叫 token 化），然後儲存在索引中的程序。           |
|Excel 檔案的大小上限  <br/> |4 MB  <br/> |Excel 檔案的大小上限位在網站上，或附加至將會被剖析為編製索引的電子郵件訊息。 任何過大，而不會剖析此限制，並將檔案或電子郵件檔案附件的郵件會被標示為未建立索引的 Excel 檔案。  <br/> |
|附件數目上限  <br/> |250  <br/> |附加到電子郵件，將會被剖析為編製索引的檔案數目上限。 如果郵件超過 250 個附件前, 250 附件會剖析編製索引，並將郵件標示為已局部編製索引，因為它已有未剖析的額外附件。  <br/> |
|最大的附件深度  <br/> |30  <br/> |會剖析的巢狀附件數目上限。 例如，如果電子郵件具有附加到其另一則訊息，而且該附加的郵件未附加的 Word 文件，Word 文件與附加的郵件會被編製索引。 此行為會繼續最多 30 個巢狀的附件。  <br/> |
|附加的影像的最大數目  <br/> |0  <br/> |影像，附加到電子郵件會略過剖析器及未編製索引。  <br/> |
|剖析項目所花費的時間上限  <br/> |30 秒  <br/> |最大值為 30 秒花費剖析為編製索引項目。 如果剖析的時間超過 30 秒，項目會標示為已局部編製索引。  <br/> |
|最大剖析器輸出  <br/> |200 萬個字元  <br/> |剖析器已編製索引的文字輸出數量上限。 例如，如果剖析器從文件 8 萬個字元，只有第一次 2 百萬個字元編製索引。  <br/> |
|最大的註解權杖  <br/> |2 百萬  <br/> |當電子郵件會編製索引時，每個字會指定如何該 word 應該要編製索引的不同的處理指示加註解。 每一組的處理指示會呼叫的註解權杖。 若要維護 Office 365 中的服務品質，沒有 2 百萬個註解語彙基元的電子郵件的限制。  <br/> |
|在索引中的最大的主體大小  <br/> |67 萬個字元  <br/> |電子郵件訊息及所有其附件的內文中的字元總數。 當電子郵件會編製索引時，郵件內文中與所有附件中的所有文字會都串接成單一字串。 此字串已編製索引的大小上限為 67 萬個字元。  <br/> |
|在本文中的最大唯一 token  <br/> |1 百萬  <br/> |如同先前的說明，語彙基元會從內容擷取文字、 移除標點符號和空格，並再將其分成 （稱為語彙基元） 儲存在索引中的單字的結果。 例如，片語`"cat, mouse, bird, dog, dog"`含有 5 語彙基元。 但是只有 4 種是唯一的語彙基元。 沒有電子郵件訊息，可協助防止索引變得太大隨機權杖與每 1 百萬個唯一的語彙基元的限制。  <br/> |
  
## <a name="more-information"></a>詳細資訊

仍有一些其他限制相關不同層面內容搜尋，例如匯出搜尋結果及內容編製索引。 這些限制的說明，請參閱下列主題：
  
- [匯出內容搜尋結果](export-search-results.md#export-limits)
    
- [位於 Office 365 中內容搜尋的已局部編製索引項目](partially-indexed-items-in-content-search.md)
    
- [調查 Office 365 電子文件探索中已局部編製索引的項目](investigating-partially-indexed-items-in-ediscovery.md)
    
- [適用於 SharePoint Online 的搜尋限制](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f)
    
內容搜尋的相關資訊，請參閱：
  
- [Office 365 中的內容搜尋](content-search.md)
    
- [內容搜尋的關鍵字查詢與搜尋條件](keyword-queries-and-search-conditions.md)