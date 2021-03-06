---
title: 還原 Office 365 使用者
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 2c261e42-5dd1-48b0-845f-2a016d29cfc1
description: 了解如何還原已刪除的 Office 365 使用者帳戶及其所有相關聯的資料。
ms.openlocfilehash: 385f7938f5e0ce1f3a580d40830124f77454f64d
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239346"
---
# <a name="restore-a-user-in-office-365"></a>還原 Office 365 使用者
   
只要在刪除使用者帳戶後的 30 天內還原，該帳戶及其所有相關資料都會全部還原。使用者可以透過相同的公司或學校帳戶登入。信箱的內容會完全還原。若您要查詢某個使用者帳戶還剩多少時間可以還原，[請連絡我們](../contact-support-for-business-products.md)。
  
以下是幾個祕訣︰
  
- 請確定有可用的 Office 365 授權可指派給帳戶。
    
- 如果貴公司使用 Active Directory，請參閱[如何對 Office 365 中已刪除之使用者帳戶的問題進行疑難排解](https://support.microsoft.com/kb/2619308)，以取得更多關於還原使用者帳戶的說明。 
    
## <a name="restore-one-or-more-user-accounts"></a>若要還原一或多個使用者帳戶

您必須是全域系統管理員或使用者管理系統管理員，才能執行這些步驟的 Office 365 中。 
  
 
::: moniker range="o365-worldwide"

1. 在系統管理中心，移至 [**使用者** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">已刪除使用者</a>] 頁面。

::: moniker-end

::: moniker range="o365-germany"

1. 移至[管理中心](https://go.microsoft.com/fwlink/p/?linkid=848041)]，然後選取 [**使用者** \> **已刪除使用者**。

::: moniker-end

::: moniker range="o365-21vianet"

1. 移至[管理中心](https://go.microsoft.com/fwlink/p/?linkid=850627)]，然後選取 [**使用者** \> **已刪除使用者**。

::: moniker-end

2. 在 [**已刪除使用者**] 頁面上，選取您想要還原的使用者名稱，然後選取 [**還原**。
    
 
3. 遵循提示，設定其密碼，然後選取 [**還原**。
    
4. 如果使用者成功還原，請選取 [**傳送電子郵件，並關閉**]。 如果您遇到名稱衝突或 Proxy 位址衝突，請參閱下方說明，了解如何還原這類帳戶。
    
您已還原使用者後，請確定您會告知使用者他們的密碼變更，且您與其待。
  
## <a name="restore-a-user-that-has-a-user-name-conflict"></a>還原有使用者名稱衝突的使用者
<a name="RestoreUserNameConflict"> </a>

當您刪除使用者帳戶，以相同的使用者名稱建立新的使用者帳戶 (不論是同一名使用者，還是另一名具有類似名稱的使用者)，稍後又試圖還原已刪除的帳戶時，即會發生名稱衝突的情形。
  
若要修正此問題，您可以將您要還原的使用者帳戶取代作用中的使用者帳戶，或是為您要還原的帳戶指派不同的使用者名稱，以避免產生兩個具相同使用者名稱的帳戶。步驟如下：
  

::: moniker range="o365-worldwide"

1. 在系統管理中心，移至 [**使用者** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">已刪除使用者</a>] 頁面。

::: moniker-end

::: moniker range="o365-germany"

1. 移至[管理中心](https://go.microsoft.com/fwlink/p/?linkid=848041)]，然後選取 [**使用者** \> **已刪除使用者**。

::: moniker-end

::: moniker range="o365-21vianet"

1. 移至[管理中心](https://go.microsoft.com/fwlink/p/?linkid=850627)]，然後選取 [**使用者** \> **已刪除使用者**。

::: moniker-end

  
2. 在 [**已刪除使用者**] 頁面上，選取您想要還原的使用者名稱，然後選取 [**還原**。
    
    > [!NOTE]
    > 若無法還原兩名或多名使用者，一則錯誤訊息會通知您某些使用者的還原作業失敗。請檢視記錄，了解哪些使用者無法順利還原，接著逐一對這些帳戶進行還原作業。 
  
3. 遵循提示，設定密碼，然後選取 [**還原**。
    
4. 隨即會跳出一則訊息，提示您還原帳戶時發生問題。請執行下列其中一項操作：
    
  - 取消還原並重新命名目前作用中的使用者，然後再次嘗試還原。
    
  - 或者，輸入新使用者的主要電子郵件地址，然後選取 [**還原**。
    
5. 檢閱結果，然後再選取 [**關閉**。
    
## <a name="restore-a-user-that-has-a-proxy-address-conflict"></a>還原 Proxy 位址衝突的使用者

當您刪除包含 Proxy 位址的使用者帳戶、將相同的 Proxy 位址指派給另一個帳戶，然後試圖還原已刪除的帳戶時，會發生 Proxy 位址衝突的情形。請依照下列步驟操作以修正此問題。
  
您必須具備 Office 365 的[系統管理員權限](about-admin-roles.md)，才能執行此動作。 
  

::: moniker range="o365-worldwide"

1. 在系統管理中心，移至 [**使用者** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">已刪除使用者</a>] 頁面。

::: moniker-end

::: moniker range="o365-germany"

移至[管理中心](https://go.microsoft.com/fwlink/p/?linkid=848041)]，然後選取 [**使用者** \> **已刪除使用者**。

::: moniker-end

::: moniker range="o365-21vianet"

1. 移至[管理中心](https://go.microsoft.com/fwlink/p/?linkid=850627)]，然後選取 [**使用者** \> **已刪除使用者**。

::: moniker-end

2. 在 [**已刪除使用者**] 頁面上，選取您想要還原的使用者，然後選取 [**還原**。 
    
3. 在 [**還原**] 頁面上，依照指示設定密碼，並選取 [**還原**。 所有衝突的 Proxy 位址都會自動從您要還原的使用者移除。
    
4. 檢閱結果，然後再選取 [**關閉**。

## <a name="related-articles"></a>相關文章

[刪除使用者](delete-a-user.md)
  

