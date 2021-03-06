---
title: 從 Office 365 移除網域
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: f09696b2-8c29-4588-a08b-b333da19810c
description: 瞭解如何從 Office 365 移除舊的網域，以及將使用者和群組移至另一個網域。
ms.openlocfilehash: 621b50384b39a21bc0bf5256841c703b3ee0f74a
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43210365"
---
# <a name="remove-a-domain-from-office-365"></a>從 Office 365 移除網域

投稿人：[![Peter Baumgartner](../../media/e70dc696-c5f8-4717-a48b-9087431503e7.png)](https://go.microsoft.com/fwlink/p/?linkid=847121)
  
 **[檢查網域的常見問題集](../setup/domains-faq.md)** ：供您在找不到所需功能時參考。 
  
您移除網域是因為想要將它加入到其他 Office 365 訂閱方案嗎？還是您只想取消訂閱？您可以[變更您的方案或訂閱](../../commerce/subscriptions/switch-to-a-different-plan.md)或[取消您的訂閱](../../commerce/subscriptions/cancel-your-subscription.md)。
  
### <a name="step-1-move-users-to-another-domain"></a>步驟1：將使用者移至另一個網域

#### <a name="move-users"></a>移動使用者

::: moniker range="o365-worldwide"

> [!NOTE]
> 如果您使用的不是新的 Microsoft 365 系統管理中心，您可以選取位於首頁頂端的 **[試用新的系統管理中心] **開關將它開啟。

1. 移至系統<a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">管理中心</a>。

2. 選取 [**使用者** >作用中**使用者**]。

3. 選取您要移動之所有使用者之名稱旁的方塊。

4. 在頁面頂端選取 [**更多選項**] （**...**），然後選擇 [**變更網域**]。

5. 在 [**變更網域**] 窗格中，選取另一個網域。

如果您所處的網域也是您要移除的網域，您也必須為自己執行這個程序。為您的帳戶編輯網域時，您必須先登出，然後使用您選擇的新網域重新登入，才能繼續執行。

::: moniker-end

::: moniker range="o365-germany"

1. 移至系統<a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">管理中心</a>。  

2. 選取 [**使用者** >作用中**使用者**]。

3. 選取您要移動之所有使用者之名稱旁的方塊。

4. 在頁面頂端 **，選擇 [** > **編輯網域**]。

5. 在 [**編輯網域**] 窗格中，選取另一個網域。
  
如果您所處的網域也是您要移除的網域，您也必須為自己執行這個程序。為您的帳戶編輯網域時，您必須先登出，然後使用您選擇的新網域重新登入，才能繼續執行。

::: moniker-end

::: moniker range="o365-21vianet"

1. 移至系統<a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">管理中心</a>。  

2. 選取 [**使用者** >作用中**使用者**]。

3. 選取您要移動之所有使用者之名稱旁的方塊。

4. 在頁面頂端 **，選擇 [** > **編輯網域**]。

5. 在 [**編輯網域**] 窗格中，選取另一個網域。
  
如果您所處的網域也是您要移除的網域，您也必須為自己執行這個程序。為您的帳戶編輯網域時，您必須先登出，然後使用您選擇的新網域重新登入，才能繼續執行。

::: moniker-end

#### <a name="move-yourself"></a>自行移動

::: moniker range="o365-worldwide"

> [!NOTE]
> 如果您使用的不是新的 Microsoft 365 系統管理中心，您可以選取位於首頁頂端的 **[試用新的系統管理中心] **開關將它開啟。

1. 移至系統<a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">管理中心</a>。

2. 移至 [**使用者** \>作用中**使用者**]，然後從清單中選取您的帳戶。

3. 在 [**帳戶**] 索引標籤上，選取 [**管理使用者名稱**]，然後選擇不同的網域。
  
4. 在頂端，選取您的帳戶名稱，然後選取 **[登出]。**

5. 使用新的網域登入，並使用相同的密碼登入。

您也可以使用 PowerShell 將使用者移至另一個網域。 如需詳細資訊，請參閱 [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) (英文)。 若要設定預設網域，請使用 [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0) (英文)。

::: moniker-end

::: moniker range="o365-germany"

1. 移至 [**使用者** \>作用中**使用者**]，然後在清單中選取您的名稱。

2. 在 [使用者**名稱/電子郵件**] 區段中，選取 [**編輯**]，然後選擇不同的網域。

3. 選取 [**設為主** > **儲存** > **關閉**]。
  
4. 在頂端，選取您的帳戶名稱，然後選取 **[登出]。**

5. 使用新的網域登入，並使用相同的密碼登入。

您也可以使用 PowerShell 將使用者移至另一個網域。 如需詳細資訊，請參閱 [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) (英文)。 若要設定預設網域，請使用 [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0) (英文)。

::: moniker-end

::: moniker range="o365-21vianet"

1. 移至 [**使用者** \>作用中**使用者**]，然後在清單中選取您的名稱。

2. 在 [使用者**名稱/電子郵件**] 區段中，選取 [**編輯**]，然後選擇不同的網域。

3. 選取 [**設為主** > **儲存** > **關閉**]。
  
4. 在頂端，選取您的帳戶名稱，然後選取 **[登出]。**

5. 使用新的網域登入，並使用相同的密碼登入。

您也可以使用 PowerShell 將使用者移至另一個網域。 如需詳細資訊，請參閱 [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) (英文)。 若要設定預設網域，請使用 [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0) (英文)。

::: moniker-end

### <a name="step-2-move-groups-to-another-domain"></a>步驟2：將群組移至另一個網域

::: moniker range="o365-worldwide"

1. 在系統管理中心中，移至 [**群組** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">群組</a>] 頁面。
  
2. 選取組名，然後在 [**電子郵件地址，主要** **] 索引**標籤底下，選取 [**編輯**]。

3. 使用下拉式清單選擇另一個網域。

4. 選取 [儲存]****，再選取 [關閉]****。 針對與您要移除之網域關聯的任何群組或通訊群組清單，重複這個程序。

::: moniker-end

::: moniker range="o365-germany"

1. 在系統<a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">管理中心</a>中，移至 [**群組** > **群組**] 頁面。

2. 選取組名，然後選取 [**名稱**] 旁的 [**編輯**]。

3. 使用下拉式清單選擇另一個網域。

4. 選取 [儲存]****，再選取 [關閉]****。 針對與您要移除之網域關聯的任何群組或通訊群組清單，重複這個程序。

::: moniker-end

::: moniker range="o365-21vianet"

1. 在系統<a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">管理中心</a>中，移至 [**群組** > **群組**] 頁面。

2. 選取組名，然後選取 [**名稱**] 旁的 [**編輯**]。

3. 使用下拉式清單選擇另一個網域。

4. 選取 [儲存]****，再選取 [關閉]****。 針對與您要移除之網域關聯的任何群組或通訊群組清單，重複這個程序。

::: moniker-end

### <a name="step-3-remove-the-old-domain"></a>步驟3：移除舊的網域

::: moniker range="o365-worldwide"

1. 在系統管理中心中，移至 **[設定]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">[網域]</a> 頁面。

::: moniker-end

::: moniker range="o365-germany"

1. 在系統管理中心中，移至 [**安裝** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">網域</a>] 頁面。

::: moniker-end

::: moniker range="o365-21vianet"

1. 在系統管理中心中，移至 [**安裝** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">網域</a>] 頁面。

::: moniker-end
  
2. 在 [**網域**] 頁面上，選取您要移除的網域。

3. 在右窗格中，選取 [**移除**]。

4. 遵循任何其他提示，然後選取 [**關閉**]。

## <a name="how-long-does-it-take-for-a-domain-to-be-removed"></a>移除網域需要多久的時間？

如果不是在許多地方（如安全性群組、通訊群組清單、使用者和 Office 365 群組）上加以參考，則 Office 365 會花無5分鐘的時間來移除網域。 如果有許多參照都使用此網域，就會花費數小時 (一天) 的時間才能將網域移除。
  
如果您有數百名或數千名使用者，請使用 PowerShell 來查詢所有使用者，然後將他們移到另一個網域。否則，UI 中很可能會遺失一些使用者，當您隨後想移除此網域時，將無法執行且不知道原因為何。如需詳細資訊，請參閱 [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) (英文)。若要設定預設網域，請使用 [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0) (英文)。
  
## <a name="still-need-help"></a>仍需要協助嗎？

::: moniker range="o365-worldwide"

> [!NOTE]
> 您無法移除帳戶中的 [".onmicrosoft.com"](https://support.office.com/article/b9fc3018-8844-43f3-8db1-1b3a8e9cfd5a.aspx) 網域。
  
仍無法運作嗎？您的網域可能需要手動移除。[打電話給我們](../contact-support-for-business-products.md)，我們會協助您處理。
  
::: moniker-end

## <a name="related-articles"></a>相關文章

[網域常見問題集](../setup/domains-faq.md)

[取得 Office 365 網域的說明](get-help-with-domains.md)

[切換到其他商務用 Office 365 方案](../../commerce/subscriptions/switch-to-a-different-plan.md)

[取消訂閱](../../commerce/subscriptions/cancel-your-subscription.md)
