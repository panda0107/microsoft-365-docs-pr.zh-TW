---
title: Microsoft 365 商務版的增加威脅防護
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
description: 設定 Office 365 進階威脅防護，和保護機密資料。
ms.openlocfilehash: 53741a7726222bb32329a401953be72257df95cc
ms.sourcegitcommit: 7ac06563c6ff034358e8fd3f9298fc426187ade2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668379"
---
# <a name="set-up-compliance-features"></a>設定符合性功能

Microsoft 365 商務版隨附功能來保護您的資料和裝置，並協助您保護其他與您的客戶敏感資訊的安全。

## <a name="set-up-dlp-features"></a>設定 DLP 功能

如需有關如何設定的原則，以防止個人識別資訊 (PII) 的範例，請參閱[建立 DLP 原則範本中](https://support.office.com/article/59414438-99f5-488b-975c-5023f2254369)。 
  
DLP 隨附許多不同的地區設定的許多準備-使用原則範本。 例如，澳洲財務資料、 加拿大個人資訊法案、 美國財務資料，等等。如需完整清單，請參閱[什麼的 DLP 原則範本包含](https://support.office.com/article/c2e588d3-8f4f-4937-a286-8c399f28953a)。 所有這些範本可啟用類似 PII 範本範例。 
  
## <a name="set-up-email-retention-with-exchange-online-archiving"></a>設定搭配 Exchange Online Archiving 的電子郵件保留

 **Exchange Online Archiving**授權功能可協助維護合規性和法規的標準來保留電子郵件內容 ediscovery （英文）。 它也可協助降低發生訴訟風險，並提供方法來復原資料安全性漏洞，或當您要復原刪除的項目。 您可以使用訴訟暫止來保留的所有使用者的內容，或使用自訂您要保留的保留原則。
  
**訴訟資料暫留：** 您可以保留所有信箱內容，包括已刪除的項目依據] 將使用者的整個信箱放置於訴訟保留。 
    
若要將信箱置於訴訟暫止，在系統管理中心：
    
1. 在左側導覽中，移至 [**使用者** \> **作用中的使用者**。
    
2. 選取您想要置於 [訴訟暫止的信箱保留的使用者在使用者窗格中展開 [**郵件設定**和**其他設定**旁邊選擇 [**編輯 Exchange 屬性**。
    
3. 在使用者信箱] 頁面上，選擇 [* * 信箱功能 * * 在左側導覽中，然後選擇 [在 [**訴訟暫止**] 下的 [**啟用**] 連結。
    
4. 在**訴訟暫止狀態**對話方塊您可以指定訴訟保留期間在**訴訟暫止持續時間**] 欄位中，將欄位保留空白，如果您想要放置無限期的保留。 您也可以新增備忘稿並導向至網站，您可能必須將說明更多有關訴訟保留的郵件] 方塊中擁有者\>**儲存**。
    
**保留：** 您可以啟用自訂的保留原則，例如，若要保留經過一段時間，或在保留期間結束永久刪除內容。 若要深入了解，請參閱[保留原則的概觀](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423)。

## <a name="set-up-azure-information-protection-features"></a>設定 Azure 資訊保護功能

Azure 資訊保護 (AIP) 可協助您分類，並選擇性地套用標籤，以保護您的文件和電子郵件。 定義規則和條件的系統管理員，以手動方式的使用者，或使用組合提供使用者的建議，可自動套用標籤。

網頁型 Outlook 中您可以套用到您的電子郵件的下列內建的標籤和限制：
  
- **不要轉寄**： 收件者可以讀取郵件，但他們無法轉寄、 列印或複製內容
    
- **加密**： 加密整封郵件。 收件者存取加密的內容之前，必須先確認其身分識別，且無法移除加密。
    
- **2 私人 3 機密**： 授與您的組織中的員工完整權限的電子郵件內容和附件，但不適用於您組織外的人員。 資料擁有者可以追蹤及撤銷的任何一點的內容。
    
- **高度機密**： 此限制可套用至高度機密資料，讓員工能夠檢視、 編輯和回覆，但不是轉寄、 列印或複製資料。 資料擁有者可以追蹤及撤銷的任何一點的內容。

### <a name="make-sure-azure-information-protection-is-activated"></a>請確定已啟動 Azure 資訊保護

若要確認 AIP 會在啟動：

1. 登入[Azure 入口網站](https://portal.azure.com/)。

2. *Azure 資訊保護*在**搜尋] 方塊**中，選取 [**所有服務**和類型。

3. 一旦顯示結果，請按一下 [下一步] **Azure 資訊保護**來使其成為我的最愛且更容易尋找稍後開始。

4. 選取 [ **Azure 資訊保護** \> **保護啟用**，並確定狀態設為啟用。 

### <a name="view-the-azure-information-protection-policy-and-default-labels"></a>檢視 Azure 資訊保護原則和預設標籤 

標籤來檢視及修改，現有：

1. 在 [Azure 資訊保護儀表板中，選取 [**分類** \> **標籤**。 <br/>![標準的 Azure 資訊保護標籤。](media/AIPLabels.png)

2. 您可以選擇任何標籤來檢視的選項，您可以變更的顯示名稱、 色彩等等。
 
3. 請參閱[修改，並建立新的標籤](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step2)如果您想要建立您自己。 

### <a name="install-the-azure-information-protection-client-manually"></a>以手動方式安裝 Azure 資訊保護用戶端

若要手動安裝 AIP 用戶端：

1. 從[Microsoft 下載中心](https://www.microsoft.com/download/details.aspx?id=53018)下載**AzInfoProtection.exe** 。
 
2. 您可以確認安裝成功可以檢視 Word 文件，以確定可在 [**首頁**] 索引標籤上 [**保護**] 選項。 <br/>![保護索引標籤下拉式清單中的 Word 文件。](media/Word_Protect.png)

如需詳細資訊，請參閱[安裝用戶端](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step3)。