---
title: 從 [受限使用者] 入口網站中移除封鎖的使用者
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 系統管理員可以從 Office 365 中的 [受限使用者] 入口網站瞭解如何移除使用者。 傳送輸出垃圾郵件 (通常是因為「帳戶洩露」) 的使用者會被新增至 [受限使用者] 入口網站。
ms.openlocfilehash: f1f869a81ef5b01733bf9060117cf3706094b961
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895200"
---
# <a name="remove-blocked-users-from-the-restricted-users-portal-in-office-365"></a>從 Office 365 中的 [受限使用者] 入口網站移除封鎖的使用者

如果使用者超過[服務限制](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options)或[輸出垃圾郵件](configure-the-outbound-spam-policy.md)原則中所指定的輸出傳送限制之一，系統就會限制使用者傳送電子郵件，但他們仍可接收電子郵件。

使用者會被新增至 Office 365 安全性 與合規性中心的 [受限使用者] 入口網站。 當他們嘗試傳送電子郵件時，系統會以未傳遞回報 (又稱為 NDR 或退回的郵件) 傳回郵件，並包含錯誤碼 [5.1.8](https://docs.microsoft.com/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-1-8-in-exchange-online) 和下列文字：

> 「因為您不是認可的有效寄件者，所以無法傳遞您的郵件。 最有可能發生此狀況的原因是您的電子郵件地址有傳送垃圾郵件的嫌疑，因此系統已不允許此電子郵件地址傳送電子郵件。  請連絡您的電子郵件系統管理員以取得協助。 遠端伺服器傳回 ‘550 5.1.8 存取被拒，錯誤的外寄寄件者。’」

系統管理員可以從安全性與合規性中心移除使用者，或用 Exchange Online PowerShell 移除使用者。

## <a name="what-do-you-need-to-know-before-you-begin"></a>開始之前有哪些須知？

- 您要在 <https://protection.office.com/> 開啟安全性與合規性中心。 若要直接移至 [受限使用者]**** 頁面，請使用 <https://protection.office.com/restrictedusers>。

- 若要連線至 Exchange Online PowerShell，請參閱[連線至 Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)。

- 您必須已獲指派權限，才能執行這些程序。 若要移除 [受限使用者] 入口網站中的使用者，您必須是**組織管理**或**安全性系統管理員**角色群組的成員。 若要以唯讀方式存取 [受限使用者] 入口網站，您必須是**安全性讀取者**角色群組的成員。 如需有關安全性與合規性中心中角色群組的詳細資訊，請參閱 [Office 365 安全性與合規性中心裡的權限](permissions-in-the-security-and-compliance-center.md)。

- 超過輸出郵件限制的寄件者是帳戶洩露的指標。 從 [受限使用者] 入口網站移除使用者之前，請務必遵循所需的步驟重新取得該帳戶的控制權。 如需詳細資訊，請參閱[針對 Office 365 電子郵件帳戶洩露的對策](responding-to-a-compromised-email-account.md)。

## <a name="use-the-security--compliance-center-to-remove-a-user-from-the-restricted-users-list"></a>使用安全性與合規性中心移除 [受限使用者] 清單中的使用者。

1. 在安全性與合規性中心，移至 [威脅管理]**** \> [檢閱]**** \> [受限使用者]****。

2. 尋找並選取您要解除封鎖的使用者。 在 [動作]**** 資料行中，按一下 [解除封鎖]****。

3. 隨即會出現飛出視窗，內含帳戶的傳送受到限制的詳細資料。 您必須逐一查看建議，以確保帳戶實際上遭到入侵時，您會採取適當的動作。 完成時，按 [下一步]****。

4. 下一個畫面提供建議來協助避免未來的入侵。 啟用多重要素驗證 (MFA)，並變更密碼，是很好的防禦方式。 完成時按一下 [解除封鎖使用者]****。

5. 按一下 [是]**** 以確認變更。

   > [!NOTE]
   > 可能需要 30 分鐘以上的時間，才能移除限制。

## <a name="verify-the-alert-settings-for-restricted-users"></a>確認受限使用者的提醒設定

當系統封鎖使用者傳送電子郵件時，預設的警示原則**無法傳送電子郵件的受限使用者**會自動通知系統管理員。 您可以確認這些設定，並新增其他要通知的使用者。 如需有關警示原則的詳細資訊，請參閱[安全性與合規性中心中的警示原則](../../compliance/alert-policies.md)。

> [!IMPORTANT]
> 若要讓警示運作，必須開啟稽核記錄搜尋。 如需詳細資訊，請參閱[開啟或關閉 Office 365 稽核記錄搜尋](../../compliance/turn-audit-log-search-on-or-off.md)。

1. 在安全性與合規性中心，移至 [警示]**** \> [警示原則]****。

2. 尋找並選取 [無法傳送電子郵件的受限使用者]**** 警示。

3. 在隨即出現的飛出視窗中，確認或設定如下設定：

   - **狀態**：確認已開啟警示 ![打開](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)。

   - **電子郵件收件者**：按一下 [編輯]****，在 [編輯收件者]**** 飛出視窗中確認或設定如下列設定：

     - **傳送電子郵件通知**：確認已選取核取方塊 ([開啟]****)。

     - **電子郵件收件者**：預設值是 **TenantAdmins** (表示 **全域系統管理員**成員)。 若要新增其他收件者，按一下方塊中的空白處。 收件者清單隨即顯示，您可以輸入名稱開始篩選，然後選取收件者。 若要移除方塊中的現有收件者，只要按一下其名稱旁的移除圖示![](../../media/scc-remove-icon.png)即可。

     - **每日通知限制**：預設值是 [無限制]****，但您可以選取每天的通知數量上限。

     完成後，按一下 [儲存]****。

4. 返回 [限制使用者傳送電子郵件]**** 飛出視窗中，按一下 [關閉]****。

## <a name="use-exchange-online-powershell-to-view-and-remove-users-from-the-restricted-users-list"></a>使用 Exchange Online PowerShell 杦檢視和移除受限使用者清單中的使用者

若要檢視限制傳送電子郵件的使用者清單，請執行下列命令：

```powershell
Get-BlockedSenderAddress
```

若要檢視特定使用者的詳細資料，請執行下列命令並以其電子郵件地址取代 \<emailaddress\>：

```powershell
Get-BlockedSenderAddress -SenderAddress <emailaddress>
```

如需詳細的語法及參數資訊，請參閱 [Get-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-blockedsenderaddress)。

若要從 [受限使用者] 清單中移除使用者，請執行下列命令並以其電子郵件地址取代 \<emailaddress\>：

```powershell
Remove-BlockedSenderAddress -SenderAddress <emailaddress>
```

如需詳細的語法及參數資訊，請參閱 [Remove-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/remove-blockedsenderaddress)。
