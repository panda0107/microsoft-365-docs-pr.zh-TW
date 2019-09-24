---
title: 套用或移除網站的文件刪除原則
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3e92668-f9b2-46ee-8e5e-c623870588b6
description: 組織通常會受限於合規性、 法律或其他法規，需要一段時間保留文件。 但是，將文件保留超過要求時間，可能會讓組織暴露在法律風險下。 基於這個理由，您的組織可能已建立您網站的文件刪除原則 — 例如，一般商業文件可能需要刪除五年之後建立它們。
ms.openlocfilehash: c826d6c9e163e79c4e72510e3362328ae902c80c
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37076739"
---
# <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a>套用或移除網站的文件刪除原則

組織通常會受限於合規性、 法律或其他法規，需要一段時間保留文件。 但是，將文件保留超過要求時間，可能會讓組織暴露在法律風險下。 基於這個理由，您的組織可能已建立您網站的文件刪除原則 — 例如，一般商業文件可能需要刪除五年之後建立它們。
  
有些組織可能使用文件刪除原則：
  
- **強制**網站擁有人無法選擇不採用強制原則，自動套用至網站。 
    
- **預設值**預設原則會自動套用至網站，但網站擁有者可以： 
    
  - 如果有的話，請選擇其他原則。
    
  - 退出原則，完全如果它不是相關網站中的內容。
    
- **既非強制，也不預設**在此情況下，沒有原則會自動套用至網站和網站擁有者必須自行套用原則。 
    
文件刪除原則可能包含多個規則 — 例如，一個規則可能會說刪除文件之後，他們所建立，但另一個規則可能會說刪除文件之後他們上次修改的一年的一年。 如果原則包含多個規則，您可以選取最佳適用於您網站的規則。 刪除規則會套用至站台內的所有文件庫。 只能將一個原則和一個規則可以為作用中的網站一次。 一個原則，例如規則可以設定為預設值，使其在套用原則時就會自動套用。
  
最後，會繼承文件刪除原則。 當您選取的原則或規則您的網站，選取範圍繼承而來的所有子網站，雖然子網站的擁有者，可以選取不同的原則或規則來中斷繼承。 當您選取的原則或規則時，請考慮您網站下任何子網站的內容。
  
## <a name="view-the-document-deletion-policies-available-in-a-site-collection"></a>檢視網站集合中可用的文件刪除原則

您的組織可能會將不同的原則指派給不同的網站集合。 在網站集合層級，網站集合擁有者可以檢視所有可用來該網站集合的文件刪除原則。 原則可能已可使用的網站集合範本 （並因此所有網站集合建立此範本中） 或此特定網站集合。
  
1. 最上層網站中的網站集合，在右上角，選擇 [**設定**[齒輪圖示] \> **網站設定]**。
    
2. 在 [**網站集合管理**] 下\>**文件刪除原則**。
    
    > [!NOTE]
    > 除非已指派原則至網站集合，不會出現 [**文件刪除原則**] 連結。 此外，連結不會出現原則已指派至網站之後，立即 — 可能需要 24 小時的時間從時原則指派給時顯示**文件刪除原則**的連結。 
  
3. 在此頁面上，您可以檢視：
    
  - 目前指派的原則和相關聯的規則。 選取要檢視的規則在右窗格中的原則。
    
  - 預設原則，如果有的話，會顯示 **[是]** [**預設**] 欄中。 
    
  - 如果原則已被指派為 [**強制**] 清單下方會顯示訊息。
    
這份清單可僅，檢視網站集合擁有者若要查看所有可用的原則和規則。 若要套用原則，請參閱下一節。
  
![指派給網站集合的文件刪除原則檢視](media/f2c0433b-2bb5-407d-a364-ae07c9627176.png)
  
## <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a>套用或移除網站的文件刪除原則

為網站擁有人或網站集合擁有者，您的組織可能已建立的原則，您可以套用至您的網站，或選擇退出完全。
  
1. 在右上角，選擇 [**設定**[齒輪圖示] \> **網站設定]**。
    
2. 在 [**網站管理**] 下\>**文件刪除原則**。
    
    > [!NOTE]
    > 除非已指派原則至網站集合，不會出現 [**文件刪除原則**] 連結。 此外，連結不會出現原則已指派至網站之後，立即 — 可能需要 24 小時的時間從時原則指派給時顯示**文件刪除原則**的連結。 
  
3. 執行下列其中一項動作：
    
  - **若要套用原則**選取原則\>選取該原則中的規則\>**儲存**。
    
    只能將一個原則和一個規則可以為作用中的網站一次。 您的組織可能會提供數個原則和規則，以從中選擇或只能將一個原則或規則。
    
    ![選取原則選項](media/f7c7c055-fca7-4a4f-bb97-63e35a65beac.png)
  
  - **若要選擇退出原則**選擇 [**退出： 不要注意刪除** \> **儲存**。
    
    網站擁有人，您可以選擇退出文件刪除原則如果您決定的原則不適用於您的網站中的內容。 不過，您無法選擇退出已標示為 [**強制**原則。
    
    ![選擇加入出選項](media/efac709c-bef7-4a02-a09d-5bc7d2b4ec63.png)
  
## <a name="document-deletion-policies-override-other-policies"></a>文件刪除原則會覆寫其他原則

網站可能使用其他原則來保留及刪除內容：
  
- 網站集合的內容類型原則。
    
- 清單或文件庫的資訊管理原則。
    
如果您將文件刪除原則套用至已對清單或文件庫使用內容類型原則或資訊管理原則的站台，這些原則將會被忽略，而文件刪除原則會有效用。 如果會略過的其他原則，您會看到訊息 「 此網站上的內容使用文件刪除原則 」。
  
這表示您應該規劃站台能夠使用僅供結構化的內容 （的資訊管理原則與內容類型原則） 或非結構化的內容 （文件刪除原則） 的原則不能兩者同時。 如果您選擇退出文件刪除原則，將不會顯示警告，而其他類型的原則會繼續運作。
  
網站原則不會受到文件刪除原則。
  
### <a name="determine-if-content-type-policies-are-being-ignored"></a>決定是否要忽略內容類型原則

如果正在使用您的網站內容類型原則，您現在會看到這個訊息，這些原則不再有效。 若要還原的內容類型原則，您可以從您的網站，移除文件刪除原則，如前所述，如果沒有可用的退出選項。 若要選擇退出任何選項時，文件刪除原則強制性，且您需要連絡法務人員在組織中。
  
1. 在右上角，選擇 [**設定**[齒輪圖示] \> **網站設定]**。
    
2. 在 [**網站管理**] 下\>**內容類型原則範本**。
    
    ![文件刪除原則，正在使用的網站上的警告](media/4cc3d703-9aff-4695-9670-f78c291c0010.png)
  
### <a name="determine-if-information-management-policies-are-being-ignored"></a>決定是否要忽略資訊管理原則

如果您的網站所使用的資訊管理原則，您現在會看到這個訊息，這些原則不再有效。 若要還原的資訊管理原則，您可以從您的網站，移除文件刪除原則，如前所述，如果沒有可用的退出選項。 若要選擇退出任何選項時，文件刪除原則強制性，且您需要連絡法務人員在組織中。
  
- 清單或文件庫，在功能區上的\>**文件庫**] 索引標籤\>**文件庫設定** \> **權限與管理**] 下\>**資訊管理原則設定**。
    
    ![文件刪除原則，正在使用的網站上的警告](media/3f043057-a741-4cd8-a165-6d139b986064.png)
  
## <a name="see-also"></a>請參閱

[文件刪除原則概觀](document-deletion-policies.md)
  
[建立文件刪除原則](create-a-document-deletion-policy.md)
