---
title: 適用於 Microsoft 365 測試環境的密碼回寫
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/22/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom:
- TLGS
- Ent_TLGs
ms.assetid: ''
description: 摘要：設定適用於 Microsoft 365 測試環境的密碼回寫。
ms.openlocfilehash: 8ff6c8c7d2eae735a2572bae1c437502602cfd0b
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/13/2020
ms.locfileid: "42633081"
---
# <a name="password-writeback-for-your-microsoft-365-test-environment"></a>適用於 Microsoft 365 測試環境的密碼回寫

*這個測試實驗室指南只能用於 Microsoft 365 企業版測試環境。*

密碼回寫可讓使用者透過 Azure Active Directory (Azure AD) 更新密碼，然後將密碼複製到本機 Active Directory 網域服務 (AD DS)。使用密碼回寫，使用者不需要透過內部部署 AD DS 更新密碼，這是其原始使用者帳戶的儲存位置。這對沒有內部部署網路的遠端存取連線的漫遊或遠端使用者來說，很有幫助。

本文說明如何設定您的 Microsoft 365 測試環境以進行密碼回寫。

此測試環境的設定分為兩個階段︰

1.  使用密碼雜湊同步處理建立 Microsoft 365 模擬企業測試環境。
2.  啟用適用於 TESTLAB AD DS 網域的密碼回寫。
    
![Microsoft Cloud 的測試實驗室指南](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> 按一下[這裡](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf)(英文)，可查看 Microsoft 365 企業版測試實驗室指南堆疊中所有文章的視覺對應。
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a>階段 1：設定適用於 Microsoft 365 測試環境的密碼雜湊同步處理

首先，請遵循[密碼雜湊同步處理](password-hash-sync-m365-ent-test-environment.md)中的指示。以下是您產生的組態。
  
![使用密碼雜湊同步處理測試環境的模擬企業](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
此組態包含： 
  
- Microsoft 365 E5 或 Office 365 E5 試用版或付費訂閱。
- 簡化的組織內部網域與網際網路的連線，由 Azure 虛擬網路的子網路上的 DC1、APP1 及 CLIENT1 虛擬機器組成 
- Azure AD Connect 在 APP1 上執行，以將 TESTLAB AD DS 網域同步至 Microsoft 365 或 Office 365 訂閱的 Azure AD 租用戶。

## <a name="phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain"></a>階段 2：啟用適用於 TESTLAB AD DS 網域的密碼回寫

首先，使用全域系統管理員角色設定使用者 1 帳戶。

1. 從 [Microsoft 365 系統管理中心](https://portal.microsoft.com)，使用您的全域系統管理員帳戶登入。

2. 按一下 [作用中使用者]****。
 
3. 在 [作用中使用者]**** 頁面上，按一下 [user1]**** 帳戶。

4. 在 [user1]**** 窗格中，按一下 [角色]**** 旁的 [編輯]****。

5. 在 user1 的 [編輯使用者角色]**** 窗格中，按一下 [全域系統管理員]****。按一下 [儲存]****，然後按一下 [關閉]****。

接下來，使用安全性設定來配置使用者 1 帳戶，該安全性設定允許其代表 TESTLAB AD DS 網域中的其他使用者變更密碼。。

1. 從 [Azure 入口網站](https://portal.azure.com)，以您的全域管理員帳戶登入，然後以 TESTLAB\User1 帳戶連線到 APP1。

2.  從 APP1 的桌面，按一下 [開始]****，輸入 [Active]****，然後按一下 [Active Directory 使用者及電腦]****。

3. 按一下功能表列中的 [檢視]****。如果**進階功能**未啟用，請按一下以啟用。

4. 在樹狀窗格中，以滑鼠右鍵按一下您的網域，按一下 [內容]****，然後按一下 [安全性]**** 索引標籤。

5. 按一下 [進階]****。

6. 在 [使用權限]**** 索引標籤上，按一下 [新增]****。

7. 按一下 [選取主體]****，輸入 [User1]****，然後按一下 [確定]****。

8. 在 [適用於]**** 中，選取 [子系使用者物件]****。

9. 在 [使用權限]**** 下，選取下列動作：

    - 變更密碼
    - 重設密碼

10. 在 [內容]**** 下，選取下列動作：
    - 撰寫 lockoutTime
    - 撰寫 pwdLastSet

11. 按三次 [確定]**** 以儲存變更。

12. 關閉 [Active Directory 使用者及電腦]****。

接著，在 APP1 上設定 Azure AD Connect 以進行密碼回寫。

1. 如有需要，請以 TESTLAB\User1 帳戶連線至 APP1。

2. 從 APP1 的桌面，按兩下 [Azure AD Connect]****。

3. 在 [歡迎]**** 頁面上，按一下 [設定]****。

4. 在 [其他工作] **** 頁面，按一下 [自訂同步處理選項]****，然後按 [下一步]****。

5. 在 [連線到 Azure AD]**** 頁面上，輸入您的全域管理員帳戶認證，然後按 [下一步]****。

6. 在 [連線目錄]**** 和 [網域/OU]** 篩選**頁面上，按一下 [下一步]****。

7. 在 [選擇性功能]**** 頁面上，選取 [密碼回寫]****，並按 [下一步]****。 

8. 在 [已可設定]**** 頁面上，按一下 [設定]**** 並等待程序完成。

9. 當您看到設定完成時，請按一下 [結束]****。

您現在可以為電腦 (未連線至模擬內部網路的虛擬網路) 上的使用者測試密碼回寫。

以下是您產生的組態：

![使用傳遞驗證測試環境的模擬企業](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)

此組態包含：

- 已註冊 DNS 網域 TESTLAB.\<您的網域名稱> 的 Microsoft 365 E5 或 Office 365 E5 試用版或付費訂閱。
- 簡化的組織內部網域與網際網路的連線，由 Azure 虛擬網路的子網路上的 DC1、APP1 及 CLIENT1 虛擬機器組成 
- Azure AD Connect 在 APP1 上執行，以將來自 Microsoft 365 或 Office 365 訂閱之 Azure AD 租用戶的帳戶和群組清單同步至 TESTLAB AD DS 網域。 
- 密碼回寫已啟用，因此使用者可以透過 Azure AD 變更其密碼，而不需要連線到簡化的內部網路。

如需在生產中進行密碼回寫的相關資訊和連結，請參閱身分識別階段中的「[簡化密碼更新](identity-add-user-accounts.md#identity-pw-writeback)」步驟。

## <a name="next-step"></a>下一步

瀏覽測試環境中的其他[身分識別](m365-enterprise-test-lab-guides.md#identity)功能。

## <a name="see-also"></a>另請參閱

[Microsoft 365 企業版測試實驗室指南](m365-enterprise-test-lab-guides.md)

[部署 Microsoft 365 企業版](deploy-microsoft-365-enterprise.md)

[Microsoft 365 企業版文件](https://docs.microsoft.com/microsoft-365-enterprise/)


