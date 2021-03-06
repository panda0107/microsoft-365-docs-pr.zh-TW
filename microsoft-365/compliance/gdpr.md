---
title: 一般資料保護規定
description: 一般資料保護規定 (GDPR) 的 Microsoft 技術指導
keywords: Microsoft 365, Microsoft 365 教育版, Microsoft 365 文件, GDPR
localization_priority: Priority
ms.prod: Microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 960a09c89c855861e3db0402f40dd558b27527ac
ms.sourcegitcommit: 6c7f6ef98c321c80a9254c10bbbb917895b5c156
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/27/2020
ms.locfileid: "42322552"
---
# <a name="general-data-protection-regulation-summary"></a>一般資料保護摘要

針對為歐盟 (EU) 中的人們提供產品及服務或為歐盟居民收集和分析資料的組織，一般資料保護規定 (GDPR) 推出了新的規則，而無論您或您的企業位於何處都必須遵守。 這份文件將引導您在使用 Microsoft 產品和服務時，幫助取得 GDPR 規定下執行權限和完成義務的資訊。 [GDPR 的建議動作方案](gdpr-action-plan.md)與[責任整備檢查清單](gdpr-arc.md)提供評估及實作GDPR 合規性的其他資源。

## <a name="terminology"></a>術語

本文件中使用的 GDPR 術語的實用定義：

- 資料控制者 (控制者)****：法律人員、公開授權單位、公司或其他實體，不論單獨或聯合其他單位，會決定個人資料處理方式的用途及方式。  
- **個人資料和資料主體**：與已識別或可識別的自然人 (資料主體) 相關的任何資訊；可識別的自然人為可直接或間接識別的個人。  
- 處理者：**** 自然人或法人、公家機關、公司，或代表控制者處理個人資料的其他主體。  
- **客戶資料**：在公司運作的日常作業中產生並儲存的資料。

## <a name="what-is-the-gdpr"></a>GDPR 是什麼？

GDPR 提供人員管理組織中收集之個人資料的權限。 透過資料主體要求 (DSR) 使用這些權限。 組織必須提供關於 DSR 和資料外洩，以及執行資料保護影響評估 (DPIA) 的即時資訊。

實作或評估 GDPR 需求時，應考慮幾點：

- 開發或評估您 GDPR 合規性資料的隱私權原則。
- 評估貴組織的資料安全性。
- 誰是您的資料控制者？
- 可能有哪些必須執行的資料安全性處理程序？

[GDPR 的建議動作方案](gdpr-action-plan.md)與[責任整備檢查清單](gdpr-arc.md)可能會提示其他思考重點。

以下任務與達成 GDPR 標準相關。 請跟隨清單中的連結來取得有關實作的詳細資料。  

- **[資料主體要求 (DSR)](gdpr-data-subject-requests.md)**。 由資料主體向控制者提出以對其個人資料採取行動 (變更、限制、存取) 的正式要求。
- **[外洩通知](gdpr-breach-notification.md)**。 在 GDPR 規範下，個人資料外洩是「導致意外或非法損毀、遺失、變更、未經授權洩漏或存取所傳輸、儲存或處理的個人資料之安全性缺口。」
- **[資料保護影響評估](gdpr-data-protection-impact-assessments.md)**。 GDPR 規定資料控制者為「可能導致自然人之權利和自由高風險」的資料作業準備資料保護影響評估 (DPIA)。

如上所述，GDPR 的建議動作方案和責任整備檢查清單提供使用 Microsoft 產品和服務時，實作或評估 GDPR 合規性的指南。

## <a name="data-subject-request-dsr"></a>資料主體要求 (DSR)

GDPR 會授予使用者 (或資料主體) 關於處理其個人資料的特定權限，包括修正錯誤資料、清除資料或限制其處理、接收其資料及滿足將其資料傳送至另一個控制者的要求等權限。 控制者會負責提供即時且 GDPR 合規性的回覆。 如需技術詳細資訊，請參閱[資料主體要求](gdpr-data-subject-requests.md)。  

### <a name="dsr-faqs"></a>DSR 常見問題集

**完成 DSR 需要採取哪些動作？**

DSR 涉及六種動作：探索、存取、改正、限制、匯出和刪除。

**資料來源為何？**

大部分的組織資料在 [Office 應用程式](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#using-the-content-search-ediscovery-tool-to-respond-to-dsrs)中產生，例如 Excel 和 Outlook。 您還可以在 Microsoft 產品和服務產生的[深入解析](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365)和[系統產生的記錄](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#part-3-responding-to-dsrs-for-system-generated-logs)中找到 DSR 相關資料。

**需要搜尋何種資料？**

個人資料可能會出現在客戶資料，Microsoft 產品和服務產生的深入解析，以及系統產生的記錄中。

**如何搜尋個人資料？**

搜尋的個人資料可能會因 Microsoft 產品和服務而有所不同。 搜尋工具包含[內容搜尋](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#using-the-content-search-ediscovery-tool-to-respond-to-dsrs)，或[應用程式內搜尋](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#using-in-app-functionality-to-respond-to-dsrs)容量。 系統管理員可以存取使用者活動相關聯之[系統產生的記錄](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#part-3-responding-to-dsrs-for-system-generated-logs)。  

**個人資料該以何種格式呈現？**

GDPR「資料可攜帶權」允許資料主體以「經過結構化、常用的、機器可讀取的格式」，要求其個人資料的複本，以及要求貴組織將這些檔案傳輸給另一個資料控制者。

**GDPR 的要求內容，以及我身為控制者的責任？**

身為控制者，GDPR 會要求您能夠：

- 為資料主體提供一份其個人資料，以及說明正在處理的資料類型、要對其揭露資料的第三方類型。
- 協助每位使用者執行其權限以修正錯誤的個人資料、清除資料或限制其處理、以可讀取的格式接收其資料，且如果適用的話，完成將其資料傳送到另一個控制者的要求。

**GDPR 的要求內容，以及 Microsoft 身為處理者的責任？**

我們必須實作適當的技術與組織措施，以協助您回應上述執行其權限的資料主題所發出的要求。

**哪裡可以找到內部部署伺服器的 GDPR 相關資訊？**

您可以在這裡找到一系列 GDPR 相關文章。 這些文章都是由 Microsoft 提供，其針對 SharePoint Server、Exchange Server、Project Server、Office Web Apps Server、Office Online Server 和內部部署檔案共用的內部部署工作負載提供建議方法。

**Microsoft 如何讓您回應資料主體要求？**

線上服務以控制者身分提供許多功能，可讓您回應資料主體的要求。 Microsoft 企業線上服務與管理控制項可協助您對於回應資料主體權限要求的個人資料採取動作，讓您能探索、存取、修正、限制、刪除及匯出位於儲存在 Microsoft 雲端中控制者所管理資料內的個人資料。 若您需要，線上服務也會以電腦可讀取的格式提供資料。

## <a name="data-protection-impact-assessment"></a>資料保護影響評估

GDPR 規範下，資料控制者需要為「可能導致自然人之權利和自由高風險」的處理作業準備[資料保護影響評估](gdpr-data-protection-impact-assessments.md) (DPIA)。 Microsoft 產品和服務中沒有需要 DPIA 建立的項目。 而是取決於您 Microsoft 設定的詳細資料。 [DPIA 內容](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dpia-office365#part-2--contents-of-a-dpia)中可找到 Office 中必須考量的詳細資訊清單

### <a name="dpia-faqs"></a>DPIA 常見問題集

**何時必須進行 DPIA？**

控制者需要執行 DPIA 來解決個人資料安全風險，或因資料外洩而造成的風險。 Office 中特定風險因素的範例可在[判斷是否需要 DPIA](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dpia-office365#part-1--determining-whether-a-dpia-is-needed)中得到解決。  

**完成 DPIA 的必要項目？**

GDPR 強制需要 DPIA 的包含項目：

- 評估與 DPIA 目的相關之資料處理的必要性和相稱性。
- 評估資料主體的權利和自由風險。
- 意圖解決風險的措施、防護措施、安全性措施，和確保個人資料保護並證明遵守 GDPR 的機制。

**我身為控制者的責任？**

在 GDPR 下，您必須在可能會對使用者權限和自由造成高風險的資料處理之前以控制者身分進行 DPIA，尤其是使用新的技術處理。 GDPR 提供下列必須在其中執行 DPIA 的非完整清單：

- 就分析和具有法律效力或同樣會大幅影響資料主題的類似活動的目的自動處理；  
- 處理大規模的特殊類別個人資料 – 顯示種族或種族來源、政治意見等的資料 — 或與刑事定罪和犯罪相關的資料；  
- 系統化監視大規模的公開區域。  

如果您無法找出足夠的程序將資料主題的高度風險降到最低，GDPR 也會要求您在開始任何處理之前，必須洽詢資料保護授權單位 (DPA)。

**Microsoft 負責的項目為何？**

Microsoft 根據預設會在其工程與商業功能依設計和隱私權實施隱私權。 在這些工作中，Microsoft 會執行關於資料處理作業的完整隱私權檢閱，可能會對資料主題的權限和自由造成影響。 服務群組中內嵌的隱私權小組會檢閱服務的設計和實作，以確保個人資料是以適切的方式進行處理，並遵循國際法律、使用者期望和我們的快速承諾。

這些隱私權檢閱通常很細微 — 特定服務可能會收到數十或數百個檢閱。 Microsoft 會將這些細微的隱私權檢閱累積為資料保護影響評估 (DPIA)，涵蓋主要的處理群組，而 Microsoft 歐盟資料保護長 (DPO) 會再加以檢閱。 DPO 會評估與資料處理相關的風險，以確保有足夠的防護功能。 如果 DPO 發現未防護的風險，建議變更回工程群組。 在資料保護風險變更時，將對 DPIA 進行檢閱及更新。


Microsoft 身為處理者，有責任協助控制者確保 GDPR 配置中展示 DPIA 需求之合規性。 為了要支援我們的客戶，我們提供 Microsoft DPIA 相關章節的摘要，並在未來的更新中透過這個區段提供，目的是讓控制者仰賴 Microsoft 服務來運用摘要，以建立自己的 DPIA。

## <a name="breach-notification"></a>外洩通知

若發生個人資料外洩，GDPR 會要求資料控制者與處理者的通知要求。 身為資料處理者，Microsoft 確保客戶能夠符合 GDPR 外洩通知需求。 資料控制者負責評估資料隱私權的風險，並且決定外洩時是否需要客戶 DPA 的通知。 Microsoft 提供進行該評估所需的資訊。 如需 Microsoft 如何偵測及回應個人資料外洩的詳細資訊，請參閱 [GDPR 規定的資料外泄通知](gdpr-breach-notification.md)。

### <a name="breach-notification-faqs"></a>外洩通知常見問題集

**GDPR 規定的個人資料是由什麼所構成？**

個人資料表示與個人相關的任何資訊，可用來直接或間接識別他們。 個人資料外洩是「導致意外或非法損毀、遺失、變更、未經授權洩漏或存取所傳輸、儲存或處理的個人資料之安全性缺口。」

**您身為控制者的責任？**

如果發生可能導致對權限和個人自由造成高風險 (例如辨識、身分遭竊、詐騙、財務損失或對其聲譽造成損毀) 的個人資料外洩，GDPR 會要求您：

- 在察覺後 72 小時內通知適當的資料保護授權單位 (DPA)，例如，在 Microsoft 通知您之後。 如果您未在這個期間內通知 DPA，則必須向 DPA 說明原因。 您必須通知 DPA，即使是對於個人的風險不太可能導致高風險。
- 通知外洩的資料主題而不過度延遲。
- 記錄資料外洩包括說明外洩的本質，例如受影響的人數、受影響的資料記錄數目、資料外洩的結果，以及貴組織所建議或採取的任何修正動作。

**Microsoft 身為處理者的責任？**

我們在發現個人資料外洩之後，GDPR 會要求我們向您發出通知而不過度延遲。 在 Microsoft 身為處理者的情況下，我們的義務反映 GDPR 需求和我們的標準、全球合約條款。 我們建議所有確認的個人資料外洩都是在範圍內；不會有傷害臨界值的風險。 我們會向客戶通知資料外洩是否是 Microsoft 直接承受，還是由我們任何的子處理者承受。 我們提供適當程序，能快速找出並連絡您在貴組織中識別的安全性事件人員。 此外，所有的子處理者都有義務依合約向 Microsoft 報告自己的資料外洩，並提供適當保證。

**Microsoft 如何偵測資料外洩？**

我們所有的服務及人員都遵循內部事件管理程序，以確保我們採取適當的預防措施，以在第一時間避免資料外洩。 不過，此外，線上服務在我們所有的平台上都有特定的適當安全性控制，可偵測在極罕見的事件中發生的資料外洩。

**Microsoft 如何回應資料外洩？**

為了支援您因應個人資料外洩，Microsoft 提供：
    - 根據要遵循的特定程序受訓的安全性人員。
    - 適當原則、程序及控制，以確保 Microsoft 維護詳細的記錄。 此回應包括擷取事件論據、其效果和補救措施，以及在我們的事件管理系統中追蹤和儲存資訊的文件。

**發生資料外洩時，Microsoft 如何通知我？**

Microsoft 具備適當原則和程序可立即通知您。 為滿足您對 DPA 的通知需求，我們會提供用來判斷是否已發生個人資料外洩的程序描述、資料外洩本質的描述，以及我們所採取要減輕資料外洩的方法描述。

## <a name="accountability-readiness-checklists-for-the-gdpr"></a>符合 GDPR 的責任整備檢查清單

這些[檢查清單](gdpr-arc.md) 提供使用 Microsoft 產品時，便於存取支援 GDPR 所需資訊的方式。 您可以使用 [Microsoft 合規性管分數](compliance-score.md)管理檢查清單項目，方法是參考 GDPR 動態磚中 [客戶管理控制措施] 底下的控制措施識別碼和控制措施標題。

## <a name="gdpr-faqs"></a>GDPR 常見問題集

**Microsoft 是否就 GDPR 向其客戶作出承諾？**

是。 GDPR 要求控管者 (例如使用 Microsoft 企業線上服務的組織) 僅使用提供足夠保證的處理者 (例如 Microsoft)，以符合 GDPR 的主要要求。 Microsoft 已主動跨出一大步，在所有大量授權客戶的合約中向他們提供這些承諾。

**Microsoft 如何協助我遵守？**

Microsoft 提供若干工具和文件來支援您的 GDPR 責任。 其中包括支援資料主體權限、執行您自己的資料保護影響評估，以及共同合作解決個人資料外洩問題。

**GDPR 條款中有哪些承諾？**

Microsoft GDPR 條款反映第 28 條規定處理者應履行的承諾。 第 28 條規定處理者承諾：

- 僅在控制者同意的情況下使用輔助處理者，並為輔助處理者負責。
- 在控制者的指示下處理個人資料，包括涉及資料傳輸之情形。
- 確保處理個人資料的人員承諾保密。
- 實行適當的技術與組織措施，確保個人資料安全層級對該風險是恰當的。
- 協助控制者履行義務，回應資料主體行使 GDPR 權利的要求。
- 符合 GDPR 的違反通知及協助規範。
- 協助控制者執行資料保護影響評估及諮詢監理機關。
- 於提供服務結束時移除或傳回個人資料。
- 支援控制者時具備符合 GDPR 之證明。

**Microsoft 在什麼基礎下協助在歐盟以外傳輸個人資料？**

Microsoft 長期以來一直使用標準合同條款 (也稱為示範條款) 作為其企業線上服務資料傳輸的基礎。 標準合約條款是歐洲委員會所提供的標準條款，可用來以合規方式在歐洲經濟區以外傳輸資料。 Microsoft 已透過[線上服務條款](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)，將標準合約條款納入我們的所有大量授權合約中。 第 29 條工作方認為 Microsoft 遵守了標準合約條款。 當歐盟-美國隱私護盾推出時，微軟是第一家獲得認證的公司。 請參閱 [Microsoft 的隱私護盾認證](https://www.privacyshield.gov/participant?id=a2zt0000000KzNaAAK&status=Active)，並閱讀[線上服務條款](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)。 歐盟-美國隱私護盾可協助想要將其資料慱輸至美國的客戶，採用與將其資料保護責任一致的方式。

**有哪些其他 Microsoft 合規性方案？**

身為客戶幾乎遍及全世界每個國家/地區的全球公司，Microsoft 具備強固的合規性產品組合來協助我們的客戶。 若要檢視合規性方案的完整清單，包括 FedRamp、HIPAA/HITECH、ISO 27001、ISO 27002、ISO 27018、NIST 800-171、UK G-Cloud， 以及其他等等，請參閱[合規性方案主題](offering-home.md)。

**GDPR 對我的公司有何影響？**

GDPR 會對收集或處理個人資料的組織施加多種要求，包括遵守六個關鍵原則的要求：

- 處理和使用個人資料時*透明*、*公平*和*合法*。 您需要清楚了解使用個人資料的方式，而且也需要「依法」處理該資料。
- 將個人資料的處理限制為*指定*、*明確*且*合法的目的*。 您將無法重複使用或揭露個人資料，因為這與當初收集資料的目的「抵觸」。
- *儘量只收集和儲存夠用且與預期目的相關的個人資料*。
- 確保*個人資料正確無誤* ，並讓其可以進行*清除或修正*。 您必須採取步驟，以確保您保留的個人資料正確無誤，並在錯誤發生時加以更正。
- *限制個人資料的儲存*。 您必須確保只保留實現資料收集目的所需的個人資料。
- 確保個人資料的*安全性*、*完整性*和*機密性*。 貴組織必須採取步驟，透過技術和組織安全措施保護個人資料的安全。

雖然 Microsoft 會隨時在您邁向 GDPR 旅程的過程中提供協助，但您需要了解貴組織對於 GDPR 有哪些具體義務，以及如何符合這些義務。

**公司必須依據 GDPR 支援哪些權利？**

GDPR 提供歐盟派駐人員，透過一組「資料主體權限」控制個人資料。 其中包括下列權限：

- 存取如何使用個人資料的相關資訊。
- 存取組織持有的個人資料。
- 刪除或更正不正確的個人資料。
- 在某些情況下，修正和清除個人資料 (有時候稱為「忘記的權限」)。
- 限制或約束個人資料的自動處理。
- 接收個人資料的複本。

**什麼是處理者和控管者？**

控管者是獨自或與其他人共同判斷處理個人資料之用途和方法的自然人或法人、公務機關、局處或其他機構。 處理者是自然人或法人、公家機關、公司，或代表控制者處理個人資料的其他主體。

**GDPR 是否適用於處理者和控制者？**

是，GDPR 同於適用於控制者和處理者。 控制者只能使用採取措施以符合 GDPR 需求的處理者。 相較於資料保護指導方針，根據 GDPR，處理者將面臨由於不合規或不按控制者所提供指示行事的額外職責和責任。 處理者的職責包括 (但不僅限於)：

- 僅依控制者的指示處理資料。
- 使用適當的技術和組織措施來保護個人資料。
- 協助控制者處理資料主體要求。
- 確保參與的輔助處理者符合這些需求。

**如果不符合合規性，公司會被處以多少罰鍰？**

公司若無法符合特定 GDPR 需求，最高可罰 2 千萬歐元或全球年度營業額的 4% (以較大者為准)。 如果您無法遵守 GDPR 需求，額外的個別救濟可能會增加您的風險。

**我的公司需要指派資料保護長 (DPO) 嗎？**

這取決於法規內識別的幾個因素。 GDPR 第 37 條規定，在以下任何情況下，控制者和處理者均應指定一名資料保護長：(a) 處理是由公家機關或機構實施，但以司法身分行事的法院除外；(b) 控制者或處理者的核心活動由處理作業組成，這些處理作業由於其天性、範圍和 (或) 目的，需要對資料主體進行大規模的定期和系統性監視；(c) 控制者或處理者的核心活動包括根據第 9 條處理大規模特殊類別的資料，以及處理與第 10 條所指的刑事定罪和罪行有關的個人資料。

**符合 GDPR 合規性需要多少成本？**

對於大多數組織而言，要符合 GDPR 的合規性將花費時間和金錢，儘管對於那些在結構良好的雲端服務模型中操作並有適當且有效資料治理計劃的公司而言，這個轉換可能更為順暢。

**如何知道 GDPR 是否涵蓋組織處理的資料？**

GDPR 會規範個人資料的收集、儲存、使用和共用。 依據 GDPR，個人資料的定義很廣泛，舉凡與已識別或可識別自然人相關的任何資料皆屬之。

個人資料可以包括 (但不限於) 線上識別碼 (例如 IP 位址)、員工資訊、銷售資料庫、客戶服務資料、客戶意見反應表、位置資料、生物特徵辨識資料、CCTV 片段、忠誠計劃記錄、健康情況，以及財務資訊等等。 其甚至可以包含似乎不是個人的資訊，例如一張沒有人的風景照，其中該資訊是以帳戶號碼或唯一代碼連結至可辨識的個人。 甚至，如果筆名可以連結至特定個人，則具有筆名的個人資料可以是個人資料。 

處理某些「特殊」類別的個人資料 (例如，顯示某人種族或血統或與其健康或性向有關的個人資料) 要比處理「普通」個人資料受到更嚴格的規範。 評估個人資料是高度以事實為依歸，因此建議讓專家參與來評估您的特定狀況。

**我的組織只代表他人處理資料。是否仍需要遵守 GDPR？**

是。 雖然這些規則稍有不同，但 GDPR 適用於基於自己目的收集及處理資料的組織 (「控制者」)，以及代表他人處理資料的組織 ('「處理者」)。 這項需求是從現有的資料保護指導方針轉變而來，適用於控制者。

**具體來說，會將什麼內容認定為個人資料？**

個人資料是任何與已識別或可識別個人相關的資訊。 個人的私人、公開或公司角色之間沒有區別。 個人資料可能包括：

- 姓名
- 住家地址
- 公司地址
- 電話號碼
- 手機號碼
- 電子郵件地址
- 護照號碼
- 國民身分證
- 社會安全號碼 (或等同)
- 駕駛執照
- 物理、生理或遺傳資訊
- 醫療資訊
- 文化身分識別
- 銀行詳細資料/帳號
- 稅號
- 公司地址
- 信用卡/轉帳卡號碼
- 社交媒體貼文
- 社交媒體貼文
- IP 地址 (歐盟地區)
- 位置/GPS 資料
- Cookie

**允許我在歐盟外傳輸資料嗎？**

允許，不過 GDPR 嚴格控管將歐洲居民的個人資料傳輸到歐洲經濟區以外的目的地。 您可能需要設定特定的法律機制 (例如合同)，或遵循認證機制，才能啟用這些傳輸。 Microsoft 會在線上服務條款中詳述我們使用的機制。

**我有透過合規性保留資料的需求。這些需求會否決清除權限嗎？**

若有合法的理由繼續處理和保留資料，例如「為了遵守法律義務，要求控制者遵守的聯邦或成員國法律進行處理」(第 17 條第 3 款 (b) 項)，GDPR 認可組織可能需要保留資料。 不過，請務必聘請法律顧問，以確定在權衡下列情況的利弊得失時考慮保留原因：資料主體的權限和自由、收集資料時其對資料的期望。

**GDPR 會處理加密嗎？**

在 GDPR 中，會將加密識別為保護措施，以在受到資料外洩影響時，使個人資料呈現無法辨識的狀態。 因此，無論是否使用加密，都會影響個人資料外洩的通知需求。 在某些情況下，GDPR 還會指出加密是一種適當的技術或組織措施，取決於風險。 支付卡行業資料安全標準和部分金融服務行業特定的嚴格合規性指導方針，也需要加密。 Microsoft 產品和服務 (例如 Azure、Dynamics 365、Enterprise Mobility + Security、Office Microsoft 365、SQL Server/Azure SQL Database 和 Windows 10) 為傳輸中資料和靜態資料提供強大的加密功能。

**GDPR 如何變更組織對個人資料外洩的回應？**

GDPR 會變更資料保護需求，並就個人資料外洩的通知，對處理者和控制者提出更嚴格的義務。 在新的管理法規底下，處理者一旦注意到個人資料外洩，必須立即將此情況通知控制者，而不致造成不當的延遲。 一旦注意到個人資料外洩，控制者必須在 72 小時內通知相關資料保護授權單位。 如果外洩可能對個人的權限和自由造成高度風險，控制者也需要通知受影響的個人，而不致造成不當的延遲。 本主題的其他指引是由歐盟第 29 條工作方所開發的。

Microsoft 產品和服務 (例如 Azure、Dynamics 365、Enterprise Mobility + Security、Microsoft Office 365 和 Windows 10) 都有立即可用的解決方案，以協助您偵測及評估安全性威脅和外洩，並履行 GDPR 的外洩通知義務。

## <a name="additional-resources"></a>其他資源

- [使用我們全球合作夥伴提供的其中一個 Microsoft 解決方案，滿足您對 GDPR 的需求](https://aka.ms/findgdprpartner)
- [了解 Microsoft 如何管理您的資料、其位在何處、誰可以存取，以及條款等等。](https://www.microsoft.com/trust-center/privacy)
- [了解 Microsoft 如何遵守歐盟 -美國隱私護盾的原則](https://blogs.microsoft.com/eupolicy/2016/07/11/eu-u-s-privacy-shield-progress-for-privacy-rights/)
- [Microsoft 如何偵測及回應個人資料外洩，並在 GDPR 下通知您](https://www.microsoft.com/trust-center/privacy/gdpr-data-breach)
- [立即評估您的 GDPR 整備狀況](https://discover.microsoft.com/gdpr-readiness-assessment/)
