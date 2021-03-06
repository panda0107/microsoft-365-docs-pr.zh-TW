---
title: 通訊合規性
description: 深入瞭解 Microsoft 365 中的通訊法規遵從性
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.openlocfilehash: 13b19079e52a390e8be3372939619541aa3b7294
ms.sourcegitcommit: 13f28aa762e467bab8ab1e95e1917b3ac28931da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "43193469"
---
# <a name="communication-compliance-in-microsoft-365"></a>Microsoft 365 中的通訊法規遵從性

通訊相容性是 Microsoft 365 中新的有問必答風險方案方案的一部分，可協助您偵測、捕獲和採取補救措施，對組織中不適當的郵件進行偵測，以協助降低通訊風險。 預先定義和自訂原則可讓您掃描內部及外部通訊的原則符合，以供指定的檢閱者檢查。 檢閱者可以調查組織中已掃描的電子郵件、Microsoft 小組或協力廠商通訊，並採取適當的修正動作，以確保它們符合您組織的郵件標準。

Microsoft 365 中的通訊相容性原則可協助您克服與相容性和內部及外部通訊相關的眾多現代化挑戰，包括：

- 掃描不斷增加的通訊通道類型
- 不斷增加的郵件資料量
- 法規實施和罰款風險

在某些組織中，IT 支援和規範管理群組之間可能會有不同的職責。 Microsoft 365 支援通訊相容性設定與掃描通訊的原則設定之間的分隔。 例如，組織的 IT 群組可能負責設定角色許可權和群組，以支援由組織的合規性小組設定及管理的通訊規範原則。

如需溝通相容性的快速綜述，請參閱偵測工作地點騷擾，並以 microsoft Communication[通道](https://www.youtube.com/user/OfficeGarageSeries)的[microsoft 365 影片中的通訊相容性回應](https://youtu.be/z33ji7a7Zho)。

## <a name="scenarios-for-communication-compliance"></a>通訊相容性案例

通訊相容性原則可協助您在一些重要的合規性區域中查看組織中的郵件：

- **公司原則**

    員工必須遵循其所有與業務相關的通訊中可接受的使用、道德標準及其他公司原則。 通訊相容性原則可以偵測原則相符，並協助您採取糾正動作，協助緩解這些類型的事件。 例如，您可以在組織中掃描員工通訊，以找出潛在的人力資源問題，例如騷擾或使用不當或冒犯性的語言。

- **風險管理**

    組織負責在其基礎結構和公司網路系統之間散佈的所有通訊。 使用通訊監督原則來協助識別及管理可能的法律公開和風險，可協助您降低風險，使其不會損毀公司的運作。 例如，您可以掃描組織中的郵件，以取得有關機密專案（例如即將進行的收購、合併、收入披露、reorganizations 或領導小組變更）的未經授權通訊。

- **法規遵從性**

    大多數的組織必須遵守某些類型的規章遵循標準，成為其正常運作程式的一部分。 這些法規通常會要求組織執行某些類型的監察或監管程式，以進行適用于其行業的郵件功能。 財務行業規章機關（FINRA） Rule 3110 是一種很好的範例，其組織必須有主管程式的主管程式，才可掃描員工通訊和其所參與的企業類型。 另一個範例可能需要檢查您組織中的經紀人通訊，以防範可能的金錢 laundering、內幕交易、collusion 或 bribery 活動。 通訊相容性原則可提供掃描和報告公司通訊的程式，協助您的組織符合這些需求。 如需對金融組織支援的詳細資訊，請參閱[美國銀行和資本市場的主要法規遵從性和安全性考慮](../solutions/financial-services-secure-collaboration.md)。

## <a name="new-enhancements"></a>新的增強功能

Microsoft 365 中的通訊法規遵從性建立于[Office 365 中的監察原則](supervision-policies.md)功能，具有下列幾項新的增強功能：

- 可自訂的智慧範本
- 彈性修復工作流程
- 可操作的洞察力

![通訊合規性首頁](../media/communication-compliance-home.png)

### <a name="intelligent-customizable-templates"></a>可自訂的智慧範本

通訊相容性中可自訂的智慧範本可讓您套用機器教學，以智慧化偵測組織中的通訊違規。

- **可自訂的預先設定的範本**：新原則範本可協助解決最常見的通訊風險。 使用預先定義的反騷擾和冒犯性語言、機密資訊和法規遵從性範本，就能更快速地建立及後續更新。
- **新機器學習支援**：內建威脅、騷擾和猥褻語言[分類](classifier-getting-started-with.md)程式可協助減少已掃描郵件中的誤報，在調查和修正程式期間儲存檢閱者的時間。
- **改進的條件**建立器：設定原則條件現在已簡化為原則嚮導中的單一整合體驗，以減少原則套用條件的方式混淆。

### <a name="flexible-remediation-workflows"></a>彈性修復工作流程

內建的修復工作流程可讓您快速識別與組織中的原則相符的郵件採取的動作。 下列新功能會提升調查和修復活動的效能：

- **彈性修復工作流程**：新的修復工作流程可協助您快速採取原則的動作，包括將郵件提升至其他檢閱者的新選項，以及使用原則相符的使用者傳送電子郵件通知。
- **交談串接**：透過原始郵件和所有關聯的回復訊息，郵件現在會以視覺方式分組，讓您在調查和修正動作中取得更佳的內容。
- **關鍵字**醒目提示：字詞符合原則條件會在郵件文字視圖中反白顯示，以協助檢閱者快速找到並修正原則警示。
- **完全和接近的重複偵測**：除了掃描完全符合通訊相容性原則的字詞之外，近期的重複偵測可群組中的類似字詞和郵件，以協助您取得審閱程式的速度。
- **新的篩選**：使用多個欄位（包括寄件者、收件者、日期、網域及其他許多欄位）的郵件篩選器，調查和修正原則警示。
- **改進的郵件**功能：現在，調查和修正動作會在新的郵件來源、文字和批註視圖中加快。 現在可以查看郵件附件，以在採取修正動作時提供完整內容。
- **使用者歷程記錄**模式：所有使用者郵件修復活動的歷史視圖，例如過去的通知和上報原則相符，現在在修正工作流程過程中為檢閱者提供更多內容。 使用者的第一次或重複的原則相符專案現在已封存，而且可輕鬆查看。

### <a name="actionable-insights"></a>可操作的洞察力

新的警示儀表板、原則比對、動作和趨勢，可協助您快速查看組織中待處理及已解決之警示的狀態。

- **主動預防性的智慧警示**：符合要求立即注意的原則相符事項，包含以嚴重性的新儀表板，以及傳送給指定的檢閱者的新自動電子郵件通知。
- **互動儀表板**：新的儀表板會顯示原則符合性、擱置和解決的動作，以及使用者和原則的趨勢。
- **審核支援**：完整的原則及檢查活動記錄，可從 Microsoft 365 規範中心輕鬆匯出，以協助支援審核審閱要求。

## <a name="integration-with-microsoft-365-services"></a>與 Microsoft 365 服務整合

通訊相容性原則可跨多個通訊通道掃描及捕獲郵件，以協助您快速查看和修正法規遵從性問題：

- **Microsoft 小組**：公用和私人[Microsoft 團隊](https://docs.microsoft.com/MicrosoftTeams/Teams-overview)通道和個別聊天的聊天通訊支援為獨立通道來源或其他 Microsoft 365 服務。 原則現在會針對原則中定義的特定使用者自動掃描所有的 Microsoft 團隊通道和團隊，不需要為 Microsoft 小組的工作分派保留個別對應清單。
- **Exchange online**：在您的 Microsoft 365 組織中的[exchange Online](https://docs.microsoft.com/Exchange/exchange-online)上主控的所有信箱都符合掃描資格。 電子郵件和附件比對相容性原則的情況立即可用於監視和監察報告。 Exchange Online 現在是一種選用的來源通道，而且通訊法規遵從性原則中已不再需要。
- **商務用 Skype online**：通訊相容性原則支援在[商務用 skype Online](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online)中的掃描聊天通訊和相關聯的附件。
- **協力廠商來源**：您可以掃描來自[協力廠商來源](archiving-third-party-data.md)的郵件，以用於將資料匯入至 Microsoft 365 組織中的信箱。 通訊相容性支援多個流行平臺的連線，包括立即 Bloomberg、Facebook、Twitter 及其他。

若要深入瞭解通訊相容性原則中的訊息通道支援，請參閱[支援的通訊類型](communication-compliance-feature-reference.md#supported-communication-types)。

## <a name="workflow"></a>工作流程

通訊規範可協助您解決與遵守內部原則及法規遵從性需求相關的常見痛點。 透過焦點原則範本及靈活的工作流程，您可以使用可行動的真知灼見，快速解決偵測到的相容性問題。

使用下列工作流程，識別及解決 Microsoft 365 中的通訊法規遵從性問題：

![通訊合規性工作流程](../media/communication-compliance-workflow.png)

### <a name="configure"></a>設定

在此工作流程步驟中，您可以識別您的相容性需求，並設定適用的通訊相容性原則。 原則範本是一種極好的方式，不僅可以快速設定新的符合性原則，也可以在需求變更時快速修改和更新原則。 例如，在為組織中的所有使用者設定原則之前，您可能會想要快速測試用於冒犯性語言和反騷擾使用者通訊的原則。

>[!Important]
>根據預設，全域管理員無法存取通訊規範功能。 若要啟用通訊相容性功能的許可權，請參閱[建立組織中的通訊相容性](communication-compliance-configure.md#step-1-required-enable-permissions-for-communication-compliance)。

您可以從下列 Microsoft 365 規範中心的原則範本中選擇：

- **冒犯性語言和反騷擾**：使用此範本可快速建立使用內建威脅、猥褻和騷擾分類程式的原則，以自動偵測可能被視為濫用或攻擊性的內容。
- **機密資訊**：使用此範本可建立一個原則，用以掃描包含定義的敏感資訊類型或關鍵字的通訊，以協助確保重要的資料不會與不應該存取的人員共用。
- **規章遵循**：使用此範本可建立原則來掃描通訊，以查看與法規標準相關的標準財務術語參考。
- **自訂原則**：使用此範本，設定組織中的特定通訊通道、分類程式、個別偵測條件，以及要查看的內容數量。

### <a name="investigate"></a>調查

在這個步驟中，您會深入瞭解偵測為符合您的通訊相容性原則所偵測到的問題。 此步驟包含下列 Microsoft 365 規範中心提供的動作：

- **警示**：當郵件符合監督原則時，系統會自動產生警示。 針對每個警示，您可以查看狀態、嚴重性、偵測到的時間，以及是否已指派案例及其狀態。 新的提醒會顯示在通訊合規性首頁及**警示**頁面上，並依嚴重性順序列出。
- **問題管理**：針對每個警示，您可以採取調查動作來協助修復在郵件中偵測到的問題。
- **檔檢查**：在調查問題期間，您可以使用多個郵件視圖，以協助正確地評估偵測到的問題。 這些視圖包括交談摘要、僅限文字、批註和通訊交談的詳細資料檢視。
- **審閱使用者活動歷程記錄**：針對原則相符，查看使用者訊息活動和修正動作（如過去的通知和上報）的記錄。
- **篩選**：使用寄件者、收件者、日期及主旨等篩選器，快速縮小您要審閱的寄件提醒。

### <a name="remediate"></a>修復

下一步是使用下列選項修正您已調查的通訊相容性問題：

- **解決**方法：在複查問題之後，您可以解析警示以進行修正。 解決警示會將其從擱置的警示佇列中移除，並且此動作會保留為符合原則之已解析佇列中的專案。 將警示標示為誤報後，系統會自動解決警示問題，並將通知傳送給員工相關通知，或開啟提醒的新案例。
- **標記郵件**：作為問題解決的一部分，您可以將偵測到的郵件標記為相容性、不相容性，或因其與組織的原則及標準相關的可疑專案。 標記可協助您微篩選原則警示，以進行升級或其他內部審查程式的一部分。
- **通知使用者**：通常是使用者意外或不經意地違反通訊規範原則。 您可以使用 [通知] 功能，針對使用者提供警告通知並解決問題。
- **升級至其他檢閱者**：有時候問題的初始檢閱者需要從其他檢閱者輸入，以協助解決事件。 您可以輕鬆地將郵件問題提升至組織其他區域中的檢閱者，做為解決程式的一部分。
- **標記為誤報**：由於相容性原則的符合性，錯誤地偵測到郵件時，可能會遍歷審核程式。 您可以將這些類型的警示標示為誤報，並自動解決問題。
- **建立案例**：在最嚴重的情況下，您可能需要與組織中的其他檢閱者共用通訊相容性資訊。 通訊法規遵從性會與其他 Microsoft 365 相容性功能緊密整合，以協助您進行端對端的風險解決。 呈報案例進行調查，可讓您將案例的資料和管理移轉到 Microsoft 365 中的進階電子文件探索。 進階電子文件探索提供端對端工作流程，可讓您保留、收集、檢閱、分析及匯出您組織內部及外部調查所需的內容。 這可讓法務小組管理整個法務保存措施通知工作流程。 若要深入了解進階電子文件探索案例，請參閱[ Mcrosoft 365 中的進階電子文件探索概觀](overview-ediscovery-20.md)。

### <a name="monitor"></a>監視

追蹤和管理通訊相容性原則所識別的合規性問題，跨越整個工作流程處理常式。 當產生警示並執行調查和修正動作時，現有的原則可能需要複查和更新，而且可能需要建立新的原則。

- **監視與報告**：使用整合的 Office 365 審核記錄檔中所記錄的通訊規範儀表板、報告、匯出記錄檔和事件，以不斷評估和改善您的相容性狀況。

## <a name="ready-to-get-started"></a>準備好開始使用了嗎？

若要設定 Microsoft 365 組織的通訊相容性，請參閱[設定 microsoft 365 的通訊相容性](communication-compliance-configure.md)，[以及如何](communication-compliance-case-study.md)快速設定通訊相容性原則，以監視 Microsoft 小組和 Exchange Online 通訊中的攻擊性語言。
