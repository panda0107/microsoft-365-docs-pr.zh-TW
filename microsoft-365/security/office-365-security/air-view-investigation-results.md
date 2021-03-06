---
title: 在 Office 365 中查看自動調查的結果
keywords: AIR, autoIR, ATP, 自動化, 調查, 回應, 修正, 威脅, 進階, 威脅, 保護
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: 在 Office 365 的自動調查期間和之後，您可以查看結果和重要結果。
ms.openlocfilehash: 6db1c6a999a7791e8fb7bf728a9ee0a33733eeaf
ms.sourcegitcommit: d1909d34ac0cddeb776ff5eb8414bfc9707d5ac1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/07/2020
ms.locfileid: "43163907"
---
# <a name="details-and-results-of-an-automated-investigation-in-office-365"></a>Office 365 中自動調查的詳細資料和結果

當[Office 365 的「高級威脅防護](office-365-atp.md)」會進行[自動調查](office-365-air.md)時，系統會在自動化調查程式期間和之後使用該調查的詳細資料。 如果您擁有必要權限，您可以在調查詳細資料檢視中查看這些詳細資料。 調查詳細資料檢視可提供您最新的狀態，以及核准任何待核准動作的能力。 

## <a name="view-details-of-an-investigation"></a>檢視調查的詳細資料

1. 移至 [https://protection.office.com](https://protection.office.com) 並登入。 這樣會帶您前往安全性與合規性中心。

2. 執行下列其中一項動作：

    - 移至 [威脅管理]****  >  [儀表板]**** 這樣會帶您前往[安全性儀表板](security-dashboard.md)。 您的 AIR 小工具會顯示在[安全性儀表板](security-dashboard.md)上方。 選取小工具，例如**調查摘要**。

    - 移至 [威脅管理]****  >  [調查]****。 

    這兩種方法都會帶您前往調查清單。

    ![AIR 的主要調查頁面](../../media/air-maininvestigationpage.png) 

3. 在調查清單中，選取 [識別碼]**** 欄中的項目。 這樣會開啟調查詳細資料頁面，從檢視中的調查圖形開始。

    ![AIR 調查圖形頁面](../../media/air-investigationgraphpage.png)

   使用各個索引標籤深入了解調查。

## <a name="view-details-about-an-alert-related-to-an-investigation"></a>檢視與調查相關警示的詳細資料

某些類型的警示會在 Office 365 中觸發自動化調查。 若要深入了解，請參閱[警示](automated-investigation-response-office.md#alerts)。 使用下列程序來檢視與自動化調查相關聯警示的詳細資料。

1. 移至 [https://protection.office.com](https://protection.office.com) 並登入。 這樣會帶您前往安全性與合規性中心。

2. 移至 [威脅管理]****  >  [調查]****。

3. 在調查清單中，選取 [識別碼]**** 欄中的項目。 

4. 開啟調查詳細資料時，選取 [警示]**** 索引標籤。觸發調查的任何警示都會列在此處。

5. 選取清單中的項目。 隨即開啟一個飛出視窗，其中包含警示的詳細資料以及其他資訊和動作的連結。

6. 檢閱飛出視窗中的資訊，並視特定警示採取動作，例如**解決**、**隱藏**，或**通知使用者**。 

    - **解決**等同於關閉警示
    
    - **隱藏**會導致原則在指定時段不觸發警示
    
    - **通知使用者**會啟動電子郵件，並且已輸入使用者的電子郵件地址，讓您的安全性操作小組輸入要給這些使用者的訊息。 (這類似於使用[威脅總管](threat-explorer.md)將訊息傳送給收件者。)  

## <a name="how-to-use-the-various-tabs"></a>如何使用各種選項卡

下列各節會逐步引導您完成「自動化調查」頁面上的各項索引標籤，以及如何使用此資訊。

### <a name="automated-investigations-page"></a>自動調查頁面

「自動調查」頁面會顯示您組織的調查及其目前狀態。

![AIR 的主要調查頁面](../../media/air-maininvestigationpage.png) 
  
您可以：
- 直接流覽至調查（選取**調查識別碼**）。
- 套用篩選器。 您可以選擇**調查類型**、**時間範圍**、**狀態**或兩者的組合。
- 將資料匯出至 .csv 檔案。

調查狀態會指出分析和動作的進度。 調查執行時，會變更狀態，以指出是否發現威脅，以及是否已核准動作。 

|狀態  |含義  |
|---------|---------|
|啟動中 | 調查已觸發並等候開始執行。 這是第一個步驟。 |
|正在執行 | 調查過程已開始且正在進行中。 當[待定的動作](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-review-approve-pending-completed-actions#approve-or-reject-pending-actions)獲得批准時，也會發生此狀態。 |
|找不到威脅 | 調查已完成且沒有發現任何威脅（使用者帳戶、電子郵件訊息、URL 或檔案）。 <br/><br/>**提示**：如果您懷疑某項未錯過（例如，為 false），您可以使用[威脅 Explorer](https://docs.microsoft.com/microsoft-365/security/office-365-security/threat-explorer)採取動作。 |
|由系統終止 | 調查已停止。 這可能是由於多種原因所造成。 以下是兩個最常見的原因：<br/>-調查的擱置中動作已過期。 等候一周的核准，待處理的動作超時。 <br/>-動作太多。 例如，如果有太多使用者點擊惡意的 URLs，它可能會超出調查的執行所有分析器的能力，所以調查會暫停。 <br/><br/>**提示**：如果調查在採取動作之前暫停，請嘗試使用[威脅瀏覽器](https://docs.microsoft.com/microsoft-365/security/office-365-security/threat-explorer)來尋找並處理威脅。  |
|擱置的動作 | 調查發現威脅，例如惡意電子郵件、惡意 URL 或風險信箱設定，以及修正威脅等候[核准](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-review-approve-pending-completed-actions)的動作。<br/><br/>當找到對應動作的任何威脅時，就會觸發擱置動作狀態;不過，請注意，調查可能尚未完全完成。  檢查[調查記錄](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-view-investigation-results#playbook-log)檔，查看是否有其他專案仍待完成。 |
|修復 | 調查已完成且所有動作均已核准（已完全修正）。<br/><br/>**附注**：核准的修復動作可能會有錯誤，導致無法採取動作。 這不會變更調查狀態。 檢查[調查記錄](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-view-investigation-results)檔中的詳細結果。 |
|部分修正 | 調查產生修正動作，有些已經過核准和完成。 其他動作仍[有待處理](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-review-approve-pending-completed-actions)。 |
|失敗 | 至少有一個調查分析器遇到問題，導致無法正確完成。 <br/><br/>**附注**：如果在已核准修正動作後，調查失敗，修正動作可能仍然會成功。 檢查[調查記錄](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-view-investigation-results)檔中的詳細結果。 |
|依節流佇列 | 在佇列中保存調查。 當其他調查完成時，佇列調查便會開始。 這有助於避免服務效能不良。 <br/><br/>**提示**：擱置的動作可能會限制可執行檔新調查數目。 請務必[核准（或拒絕）暫](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-review-approve-pending-completed-actions#approve-or-reject-pending-actions)止的動作。 |
|由節流終止 | 如果佇列中的調查保留太長，它會停止。 <br/><br/>**提示**：您可以[從威脅瀏覽器開始調查](https://docs.microsoft.com/microsoft-365/security/office-365-security/automated-investigation-response-office#example-a-security-administrator-triggers-an-investigation-from-threat-explorer)。 |

### <a name="investigation-graph"></a>調查圖表

當您開啟特定調查時，您會看到 [調查圖形] 頁面。 此頁面會顯示所有不同的實體：電子郵件訊息、使用者（及其活動），以及在觸發之警示中自動調查的裝置。

![AIR 調查圖形頁面](../../media/air-investigationgraphpage.png)

您可以：
- 取得目前調查的視覺效果。
- 查看調查週期的摘要。
- 選取視覺化效果中的節點，以查看該節點的詳細資料。
- 選取頂端的索引標籤，以查看該索引標籤的詳細資料。

### <a name="alert-investigation"></a>警示調查

在調查的 [**提醒**] 索引標籤上，您可以看到與調查相關的警示。 詳細資料包括觸發調查的警示，以及與調查相關的其他相關警示（如危險登入、DLP 原則違規等等）。 在此頁面中，安全性分析員也可以查看個別警示的其他詳細資料。

![空氣提醒頁面](../../media/air-investigationalertspage.png)

您可以：
- 取得目前觸發警示及任何相關警示的視覺效果。
- 在清單中選取警示，以開啟顯示完整警示詳細資料的飛出頁面。

### <a name="email-investigation"></a>電子郵件調查

在調查的 [**電子郵件**] 索引標籤上，您可以看到原始的電子郵件，以及視為調查之一部分之類似電子郵件的聚簇。 

考慮到組織中的使用者傳送和接收的大量電子郵件，以及電子郵件通訊和攻擊的多使用者性質，您的處理常式 
- 根據來自郵件頭、內文、URL 和附件的類似屬性來聚簇電子郵件訊息; 
- 將惡意電子郵件與良好的電子郵件分開;和 
- 對惡意電子郵件採取動作 

會花很長的時間。 現在，AIR 可自動化此程式，儲存組織的安全性小組時間和精力。 

電子郵件分析步驟期間可識別兩種不同類型的電子郵件簇：相似性聚簇和指示器叢集。 
- 相似性聚簇是透過搜尋與類似寄件者和內容屬性的電子郵件所識別的電子郵件訊息。 根據原始的偵測結果，這些聚簇會針對惡意內容進行評估。 包含足夠惡意電子郵件偵測的電子郵件群集被視為惡意電子郵件。
- 指標聚簇是透過搜尋來自原始電子郵件的相同指示器實體（檔案雜湊或 URL）所識別的電子郵件訊息。 當原始檔案/URL 實體識別為惡意時，AIR 會將指示器結論套用到包含該實體的完整電子郵件。 識別為惡意程式碼的檔案，表示包含該檔案的電子郵件叢集會被視為惡意程式碼電子郵件訊息。

聚簇的目標是尋找及尋找其他相關的電子郵件訊息，這些郵件是由同一個寄件者在攻擊或活動中所傳送。  在某些情況下，合法的電子郵件可能會觸發調查（例如，使用者報告行銷電子郵件）。  在這些案例中，電子郵件叢集應識別電子郵件群集是否不是惡意的-當有適當的情況時，它不會指出威脅，也**不**會建議刪除電子郵件。

[**電子郵件**] 索引標籤也會顯示與調查相關的電子郵件專案，例如使用者報告的電子郵件詳細資料、報告的原始電子郵件、zapped 由於惡意程式碼/網路釣魚等的電子郵件。

[電子郵件] 索引標籤上所識別的電子郵件計數目前代表 [**電子**郵件] 索引標籤上所顯示之所有電子郵件的總數。由於電子郵件訊息存在於多個聚簇中，因此所識別的實際電子郵件總數（並受修正動作影響）是在所有的聚簇和原始收件者的電子郵件中顯示的唯一電子郵件計數。 

根據每個收件者，Explorer 和 AIR 的電子郵件都會以每個收件者為基礎，因為每個收件者的安全性 verdicts、動作和傳遞位置各不相同。 因此，傳送給三位使用者的原始電子郵件會算作三個電子郵件的總數，而不是一封電子郵件。 附注可能是電子郵件會被計算兩次以上的情況，因為電子郵件可能會有多個動作，而且在所有動作都會發生時，可能會有多個電子郵件副本。 例如，在傳遞時偵測到惡意程式碼的電子郵件，可能會導致封鎖（隔離）電子郵件和取代的電子郵件（威脅檔案會以警告檔取代，然後傳遞至使用者的信箱）。 由於系統中的電子郵件有逐字的兩個複本，所以兩者都可能會計入簇計數。 

電子郵件計數會在調查時進行計算，當您開啟調查 flyouts 時，會重新計算某些計數（根據基礎查詢）。 [電子郵件] 索引標籤上的電子郵件聚簇及 [叢集] 浮出控制項上顯示的電子郵件數量詞的電子郵件數目會在調查時進行計算，而且不會變更。 電子郵件的 [電子郵件] 索引標籤底部顯示的電子郵件計數，以及 Explorer 中所顯示之電子郵件的計數，會反映在調查的初始分析之後所收到的電子郵件。 因此，顯示原始數量10封電子郵件的電子郵件，會顯示在調查分析階段和系統管理員檢查調查時，會有5封以上的電子郵件訊息到貨的電子郵件清單總額15。  同樣的「調查」的計數可能會比 Explorer 查詢所顯示的計數大，因為 ATP P2 會在30天內的30天后到期資料，以及已收費授權的30天。  在不同的視圖中顯示計數歷史和目前的計數，都是為了指出調查時的電子郵件影響，以及目前的影響，直到執行補救的時間為止。

舉例來說，請考慮下列案例。 第三個電子郵件的第一個叢集已被視為網路釣魚。 會找到另一個具有相同 IP 和主體的類似郵件，並將其視為惡意網路，因為在初始偵測時，已將其中一部分識別為網路釣魚。 

![航空電子郵件調查頁面](../../media/air-investigationemailpage.png)

您可以：
- 取得目前的聚簇結果及發現威脅的視覺概況。
- 按一下 [叢集] 實體或威脅清單，開啟顯示完整警示詳細資料的飛出頁面。
- 按一下 [電子郵件叢集詳細資料] 索引標籤頂端的「在 Explorer 中開啟」連結進一步調查電子郵件叢集

![使用飛出詳細資料的航空調查電子郵件](../../media/air-investigationemailpageflyoutdetails.png)

> [!NOTE]
> 在電子郵件的內容中，您可能會在調查過程中看到大量的反常威脅曲面。 大量的事件會指出調查事件時間與較舊的時程表之間的類似電子郵件訊息中的波峰。 這種具有類似特性的電子郵件流量（例如，主旨和寄件者網域、內文相似性和寄件者 IP）通常是電子郵件宣傳活動或攻擊的開始。 不過，大量、垃圾郵件和合法的電子郵件活動通常會共用這些特性。 大量的情況代表潛在威脅，而且與使用防病毒引擎、引爆或惡意信譽所識別的惡意程式碼或網路釣魚威脅相比，其可能會較低的危險。

### <a name="user-investigation"></a>使用者調查

在 [**使用者**] 索引標籤上，您可以看到所有識別為調查之一部分的使用者。 當發生事件時，使用者帳戶會出現在調查中，或指出這些使用者帳戶可能受到影響或遭到破壞。

例如，在下圖中，AIR 會根據所建立的新收件匣規則，識別出損等損等現象。 調查的其他詳細資料（證據）可透過此索引標籤內的詳細資料。受損的跡象和反常也包括來自[Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)的反常偵測。

![AIR 調查使用者頁面](../../media/air-investigationuserspage.png)

您可以：
- 深入瞭解已識別的使用者結果和找到的風險。
- 選取使用者開啟彈出頁面，顯示完整的提醒詳細資料。

### <a name="machine-investigation"></a>機器調查

在 [**機器**] 索引標籤上，您可以看到識別為調查一部分的所有機器。 

![AIR 調查電腦頁面](../../media/air-investigationmachinepage.png)

在某些行動行動中，AIR 會將電子郵件威脅與裝置相關聯（例如，Zapped 惡意程式碼）。 例如，調查會將惡意檔雜湊傳遞至[Microsoft DEFENDER ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection
)以進行調查。 這可讓您針對使用者自動調查相關的機器，以協助確保雲端和您的端點都有解決威脅。 

您可以：
- 取得目前的電腦及發現威脅的視覺概況。
- 選取機器，以開啟 Microsoft Defender Security Center 中相關[Microsoft DEFENDER ATP 調查](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)中的視圖。

### <a name="entity-investigation"></a>實體調查

在 [**實體**] 索引標籤上，您可以看到在調查中識別及分析的實體。 

在這裡，您可以查看已調查的實體和實體類型的詳細資料，例如電子郵件訊息、叢集、IP 位址、使用者等等。 您也可以查看已分析的實體數量，以及與每個實體相關聯的威脅。 

![AIR 調查實體頁面](../../media/air-investigationentitiespage.png)

您可以：
- 取得所找到之調查實體和威脅的視覺效果。
- 選取實體以開啟顯示相關實體詳細資料的飛出頁面。

![空中調查實體詳細資料](../../media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>行動手冊記錄

在 [**記錄**] 索引標籤上，您可以看到在調查過程中所發生的所有操作手冊步驟。 記錄檔會捕獲 Office 365 自動調查功能所完成之所有 analyzer 和動作的完整清查，做為空氣的一部分。 它提供所有採取步驟的清晰視圖，包括動作本身、描述，以及實際從開始到完成的持續時間。 

![航空調查記錄頁面](../../media/air-investigationlogpage.png)

您可以：
- 請參閱行動手冊步驟的視覺概況。
- 將結果匯出至 CSV 檔案。
- 篩選視圖。

|分析儀 | 說明 |
|-----|-----|
|DLP 違規調查 |調查[Office 365 資料遺失防護](../../compliance/data-loss-prevention-policies.md)（DLP）偵測到的任何衝突 |
|電子郵件指示器解壓縮 |從電子郵件的標頭、本文和內容提取指示器，以進行調查 |
|檔案雜湊信譽 |根據組織中使用者和機器的檔案雜湊，偵測不好的異常 |
|郵件叢集識別 |以標頭、內文、內容及 URLs 為基礎的電子郵件聚簇分析 |
|郵件聚簇磁片區分析 |根據輸出郵件流程大量模式進行的電子郵件叢集分析 |
|郵件委派調查 |調查與此次調查相關之使用者信箱的郵件委派存取權 |
|郵件轉發規則調查 |調查與此次調查相關之使用者信箱的任何郵件轉送規則 |
|偵測到未接惡意程式碼 |偵測未接的惡意程式碼已傳遞至組織中的使用者信箱 |
|隨選引爆 |觸發電子郵件訊息、附件及 URLs 的隨選引爆 |
|輸出郵件反常狀況調查 |根據歷史郵件流程針對組織中的使用者傳送模式來偵測異常 |
|輸出惡意程式碼和垃圾郵件反常情況調查 |偵測來自組織中使用者的組織內和輸出惡意程式碼、網路釣魚詐騙或垃圾郵件 |
|寄件者網域調查 |從[Microsoft 智慧型 Security Graph](https://www.microsoft.com/security/operations/intelligence)和外部威脅情報來源對網域信譽的要求檢查 |
|寄件者 IP 調查 | 從[Microsoft 智慧型 Security Graph](https://www.microsoft.com/security/operations/intelligence)和外部威脅情報來源對 IP 信譽的要求檢查 |
|URL 按一下調查 | 調查組織中的[Office 365 ATP 安全連結](atp-safe-links.md)所保護的使用者按一下 |
|URL 信譽調查 |對來自[Microsoft 智慧型 Security Graph](https://www.microsoft.com/security/operations/intelligence)和外部威脅情報來源之 URL 信譽的要求檢查 |
|使用者活動調查 |分析[Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)中的使用者活動異常 |
|使用者報告的電子郵件指示器解壓縮 |從[使用者報告的郵件](enable-the-report-message-add-in.md)頭、內文和內容提取指示器，以進行調查 |

### <a name="recommended-actions"></a>建議的動作

在 [**動作**] 索引標籤上，您可以看到在調查完成之後，修正建議的所有行動手冊動作。 

動作會捕獲 Microsoft 建議您在調查結束時採取的步驟。 您可以選取一或多個動作來採取補救措施。 按一下 [**核准**]，即可開始修復。 （需要適當的許可權-需要「搜尋和清除」角色才能從 Explorer 和 AIR 執行動作）。 例如，安全性讀者可以查看動作但不能核准。 附注：您不需要核准每個動作。 如果您不同意建議的動作，或您的組織未選擇某些類型的動作，您可以選擇**拒絕**動作或完全忽略動作，不採取任何動作。 核准和/或拒絕所有動作可讓調查完全關閉（狀態會變成「已修正」），而保留某些動作會導致調查狀態變更為部分修正狀態。

![AIR 調查動作頁面](../../media/air-investigationactionspage.png)

您可以：
- 取得行動手冊-建議動作的視覺效果。
- 選取一個或多個動作。
- 使用批註核准或拒絕建議的動作。
- 將結果匯出至 CSV 檔案。
- 篩選視圖。

## <a name="next-steps"></a>後續步驟

- [審閱及核准擱置的動作](https://review.docs.microsoft.com/microsoft-365/security/office-365-security/air-review-approve-pending-completed-actions)

- [深入瞭解 Microsoft 威脅防護中的自動化調查和回應](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir)
