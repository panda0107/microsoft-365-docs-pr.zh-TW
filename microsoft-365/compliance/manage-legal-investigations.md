---
title: 管理 Microsoft 365 的法律調查
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e
description: 使用 Microsoft 365 規範中心的 eDiscovery 案例來管理組織的法律調查。 如果您有 E5 訂閱，您可以使用「高級 eDiscovery」的文字分析、機器學習和預測編碼功能，進一步分析案例資料。
ms.openlocfilehash: 0db2187259c0c828c492f56698963bf9f61c9c18
ms.sourcegitcommit: 825037f166eea3ba70f8980cedc5492f90c1cc56
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/01/2020
ms.locfileid: "43097191"
---
# <a name="manage-legal-investigations-in-microsoft-365"></a>管理 Microsoft 365 的法律調查

組織會有許多理由，以回應與組織中特定主管或其他員工相關的法律案例。 這可能會讓您快速尋找及保留電子郵件、檔、立即訊息交談，以及人員在日常工作工作中所使用之其他內容位置中的進一步調查特定資訊。 您可以使用安全性與合規性中心的 eDiscovery 案例工具來執行這些及許多其他類似的活動。
  
**想知道 Microsoft 如何管理其 eDiscovery 調查？** 以下是您可以下載的[技術白皮書](https://go.microsoft.com/fwlink/?linkid=852161)，說明如何使用相同的 Office 365 搜尋和調查工具來管理我們的內部 eDiscovery 工作流程。
   
## <a name="manage-legal-investigations-with-ediscovery-cases"></a>管理 eDiscovery 案例的法律調查

eDiscovery 案例可讓您控制哪些人員可以在組織中建立、存取及管理 eDiscovery 案例。 使用案例新增成員並控制其可執行檔動作類型，保留與法律案例相關的內容位置，並使用內容搜尋工具，針對可能會回應您案例的內容，搜尋保留的位置。 然後，您也可以匯出及下載這些結果，以供外部檢閱者進一步調查。
  
- 針對您的組織必須執行的每個法律調查建立及使用 eDiscovery 案例，以[管理您的 eDiscovery 工作流程](ediscovery-cases.md) 
    
- [指派 ediscovery 許可權](assign-ediscovery-permissions.md)，以控制誰可以在組織中建立及管理 eDiscovery 案例 
    
- [設定規范界限](tagging-and-assessment-in-advanced-ediscovery.md)，以控制 eDiscovery 管理員可搜尋的使用者內容位置 
    
- [搜尋組織中的內容](search-for-content.md) 
    
### <a name="use-scripts-for-advanced-scenarios"></a>使用腳本進行高級案例

就像前一節所列的內容搜尋案例一樣，我們也建立了一些安全性 & 合規性中心 PowerShell 腳本，協助您管理 eDiscovery 案例。
  
- [建立「ediscovery 保留」報告](create-a-report-on-holds-in-ediscovery-cases.md)，其中包含與您組織中的 eDiscovery 案例相關聯之所有保留的相關資訊。 
    
- 將使用者清單的[信箱和 OneDrive 位置新增](use-a-script-to-add-users-to-a-hold-in-ediscovery.md)至 eDiscovery 暫止 
  
## <a name="manage-legal-investigations-with-the-advanced-ediscovery-solution-in-microsoft-365"></a>使用 Microsoft 365 中的高級 eDiscovery 解決方案管理法律調查

Microsoft 365 中的「高級 eDiscovery 解決方案」是以 Office 365 中現有的 eDiscovery 和分析功能為基礎。 這個新的解決方案稱為「*高級 eDiscovery*」，提供了端對端工作流程，可保留、收集、審閱、分析及匯出回應組織內部和外部調查的內容。 它也可讓法律團隊管理整個法律封存通知工作流程，以與案例中的保管人進行通訊。

「高級 eDiscovery」需要您的 Microsoft 365 或 Office 365 組織的 E5 訂閱。 如需授權的詳細資訊，請參閱[Advanced eDiscovery 入門](get-started-with-advanced-ediscovery.md#step-1-verify-and-assign-appropriate-licenses)。

以下是 Advanced eDiscovery 中內建工作流程的快速綜述。 如需詳細資訊，請參閱[探索高級 eDiscovery 工作流程](get-started-with-advanced-ediscovery.md#explore-the-advanced-ediscovery-workflow)。

- [建立案例](create-new-ediscovery-case.md)以開始使用

- [管理保管人](managing-custodians.md)的方式是將其新增至案例，並對其信箱中的內容進行合法保留，OneDrive 帳戶，以及他們是其成員的 Microsoft 團隊。

- 自動化法律封存通知程式，以管理與保管人的[通訊](managing-custodian-communications.md)

- [索引管理員資料](processing-data-for-case.md)並修正索引錯誤，讓您能有效地收集調查的資料

- [收集](collecting-data-for-ediscovery.md)案例的資料，並將[其新增至複查集](collecting-data-for-ediscovery.md#adding-search-results-to-a-review-set)以進行進一步調查

- [查看](view-documents-in-review-set.md)審閱集中的檔、[查詢](review-set-search.md)資料及[標記](tagging-documents.md)專案

- 使用高級分析工具[分析案例資料](analyzing-data-in-review-set.md)

- [匯出案例資料](exporting-data-ediscover20.md)以供外部顧問審閱

- 在高級 eDiscovery 中[管理長期執行的工作](managing-jobs-ediscovery20.md)
