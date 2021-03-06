---
title: 使用進階電子文件中的通訊
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 進階電子文件可以輕鬆管理周圍通知 custodians 法律調查中的合法持有通知工作流程。
ms.openlocfilehash: 3e9fb2bc67fc5eac181afab8ba5c78c4236fb980
ms.sourcegitcommit: 6d672eb8287526a9db90df5fa85bc4984a7047d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/26/2020
ms.locfileid: "42280121"
---
# <a name="work-with-communications-in-advanced-ediscovery"></a>使用進階電子文件中的通訊

進階電子文件可以讓法務部門，以簡化繞追蹤和散佈合法持有通知其處理程序。 Custodian 通訊工具可讓法務部門來管理及自動化的整個法律保留程序，從初始通知，提醒，以及擴大，所有在一個位置。

## <a name="what-is-a-legal-hold-notification"></a>合法持有通知是什麼？

合法持有 （也稱為*訴訟資料暫留*） 通知是寄送給從組織的法務部門的員工、 臨時員工、 或 custodians 可能是相關法律調查的資料的通知。 這些通知指示 custodians 來保留電子儲存的資訊，以及可能是相關法律專家作用中或即將發生的任何內容。 法律小組必須知道每個 custodian 已接收、 閱讀、 瞭解並同意遵守的特定指示。

## <a name="the-legal-hold-notification-process"></a>法律保留通知程序

組織有責任保留的相關資訊，當它了解即將發生訴訟資料暫留或法規的調查。 若要遵守調查的保留需求，組織應該立即通知潛在 custodians 其陪審團来保留的相關資訊。

使用進階電子文件，法務小組可以建立並自訂其合法持有通知工作流程。 Custodian 通訊工具可以讓法務小組設定下列通知及工作流程：

1. **發行注意事項：** 合法持有通知是發出 （或起始） 從法務部門通知給 custodians 人員可能會有區分大小專家的相關資訊。 此通知會指示 custodians 保留探索可能需要的任何資訊。

2. **重新發行注意事項：** 期間情況下，custodians 可能需要其他內容 （或較少的內容） 保留較先前要求。 此案例中，可以更新現有的保留通知，並重新發出到 custodians。

3. **釋出注意事項：** 一旦專家會解析及 custodian 不再受到保留需求，可從案例釋放 custodian。 此外，您可以通知 custodian 它們不再需要保留內容，並提供有關如何繼續其資料與其一般工作活動的指示。

4. **提醒和呈報：** 在某些情況下，只發出通知是不足以滿足法律需求。 與每個通知法務小組可以排程來自動追蹤與回應 custodians 提醒及呈報工作流程的一組。

   - **提醒：** 已發出或重新發行給一群 custodians 合法持有通知之後，組織可以設定提醒，提醒回應 custodians。

   - **擴大：** 在某些情況下，如果 custodian 即使之後提醒一組經過一段時間，仍然無法回應法律小組可以設定呈報流程通知回應 custodians 和其主管。

## <a name="role-groups-and-permissions"></a>角色群組和權限

法律小組可以控制及隔離他們安全性 & 合規性中心使用 eDiscovery 相關的角色群組和權限的案例活動。 

若要建立及管理合法持有通知，使用者必須執行 eDiscovery 管理員角色群組的成員。 這個角色群組的成員可以建立及管理進階電子文件探索案例。 他們可以新增和移除成員、 位置 custodians 上的內容位置保留、 管理合法持有通知、 建立和編輯在案例相關聯的搜尋、 將搜尋結果新增至檢閱設定、 分析中檢閱設定，並匯出資料並從進階下載eDiscovery 案例。 

有兩個的子群組 eDiscovery 管理員角色群組。 這些子群組之間的差異根據範圍。

- **eDiscovery 管理員：** 可以檢視及管理進階電子文件探索案例他們建立或成員。 如果其他 eDiscovery 管理員會建立案例，但不會將第二個 eDiscovery 管理員新增為該案例的成員，第二個 eDiscovery 管理員無法檢視或在安全 & 與規範中心中開啟 [進階電子文件] 頁面上的案例。

- **eDiscovery 系統管理員：** 可以執行 eDiscovery 管理員可以執行的所有案例的管理工作。 此外，eDiscovery 系統管理員可以：

  - 在 [進階電子文件] 頁面上檢視所有的情況下所列。
  
  - 在自行新增為案例的成員之後管理組織中的任何案例。

  - 在組織中任何案例的進階電子文件中的存取和匯出案例資料。

如需詳細資訊，請參閱[指派安全性 & 合規性中心的 eDiscovery 權限](assign-ediscovery-permissions.md)。
