---
title: 適用於 Microsoft 365 測試環境的傳遞驗證
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: ''
description: 摘要：設定適用於 Microsoft 365 測試環境的傳遞驗證。
ms.openlocfilehash: 26222f04617999104a1ad010eb189a0c01370a6d
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866313"
---
# <a name="pass-through-authentication-for-your-microsoft-365-test-environment"></a>適用於 Microsoft 365 測試環境的傳遞驗證

想要直接使用內部部署 Windows Server Active Directory (AD) 基礎結構，對 Microsoft 雲端式服務和應用程式進行驗證的組織，可以使用傳遞驗證。本文說明可以如何針對傳遞驗證設定 Microsoft 365 測試環境，造成下列組態：
  
![使用傳遞驗證測試環境的模擬企業](media/pass-through-auth-m365-ent-test-environment/Phase2.png)
  
設定此測試環境有兩個主要階段︰

1.  使用密碼雜湊同步處理建立 Microsoft 365 模擬企業測試環境。
2.  在 APP1 上針對傳遞驗證設定 Azure AD Connect。
    
![Microsoft Cloud 的測試實驗室指南](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> 按一下[這裡](https://aka.ms/m365etlgstack)(英文)，可查看 Microsoft 365 企業版測試實驗室指南堆疊中所有文章的視覺對應。
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a>階段 1：設定適用於 Microsoft 365 測試環境的密碼雜湊同步處理

請遵循[適用於 Microsoft 365 的密碼雜湊同步處理](password-hash-sync-m365-ent-test-environment.md)中的指示。以下是您產生的組態。
  
![使用密碼雜湊同步處理測試環境的模擬企業](media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
此組態包含： 
  
- Office 365 E5 和 EMS E5 試用版或永久訂閱。
- 簡化的組織內部網路與網際網路連線，由 Azure 虛擬網路的子網路上的 DC1、APP1 及 CLIENT1 虛擬機器組成。在 APP1 上執行的 Azure AD Connect 會定期將 TESTLAB Windows Server AD 網域同步處理至 Office 365 和 EMS E5 訂閱的 Azure AD 租用戶。

## <a name="phase-2-configure-azure-ad-connect-on-app1-for-pass-through-authentication"></a>階段 2：在 APP1 上針對傳遞驗證設定 Azure AD Connect

在這個階段中，您會在 APP1 上設定 Azure AD Connect 以使用傳遞驗證，然後驗證它是否運作正常。

### <a name="configure-azure-ad-connect-on-app1"></a>在 APP1 上設定 Azure AD Connect

1.  從 [Azure 入口網站](https://portal.azure.com)，以您的全域管理員帳戶登入，然後以 TESTLAB\User1 帳戶連線到 APP1。

2.  從 APP1 的桌面執行 Azure AD Connect。

3.  在 [歡迎]**** 頁面上，按一下 [設定]****。

4.  在 [其他工作] 頁面上，按一下 [變更使用者登入]****，然後按 [下一步]****。

5.  在 [連線到 Azure AD]**** 頁面上，輸入您的全域管理員帳戶認證，然後按 [下一步]****。

6.  在 [使用者登入]**** 頁面上，按一下 [傳遞驗證]****，然後按 [下一步]****。

7.  在 [準備設定]**** 頁面上，按一下 [設定]****。

8.  在 [組態完成]**** 頁面上，按一下 [結束]****。

9.  從 Azure 入口網站的左窗格，按一下 [Azure Active Directory > Azure AD Connect]****。確認 [傳遞驗證]**** 功能顯示為 [已啟用]****。

10. 按一下 [傳遞驗證]****。[傳遞驗證]**** 窗格會列出您的驗證代理程式安裝所在的伺服器。您應該會在清單中看到 APP1。關閉 [傳遞驗證]**** 窗格。

接下來，以 User1 帳戶的 user1@testlab.\<您的公用網域> 使用者名稱測試登入 Office 365 訂閱的能力。

1. 從 APP1 登出 Office 365，然後再次登入，這次指定不同的帳戶。

2. 當系統提示輸入使用者名稱和密碼時，指定 user1@testlab.\<您的公用網域> 和 User1 密碼。您應該可以用 User1 的身分成功登入。

請注意，User1 雖具有 TESTLAB Windows Server AD 網域的網域管理員權限，但並不是 Office 365 全域管理員。因此，您不會看到 [管理員]**** 圖示選項。

以下是您產生的組態：

![使用傳遞驗證測試環境的模擬企業](media/pass-through-auth-m365-ent-test-environment/Phase2.png)
 
此組態包含：

- 已註冊 DNS 網域 TESTLAB.\<您的網域名稱> 的 Office 365 E5 和 EMS E5 試用版或永久訂閱。
- 簡化的組織內部網路與網際網路連線，由 Azure 虛擬網路子網路上的 DC1、APP1 及 CLIENT1 虛擬機器組成。驗證代理程式會在 APP1 上執行，以處理來自 Office 365 和 EMS E5 訂閱 Azure AD 租用戶的傳遞驗證要求。

## <a name="next-step"></a>下一步

瀏覽測試環境中的其他[身分識別](m365-enterprise-test-lab-guides.md#identity)功能。

## <a name="see-also"></a>另請參閱

[Microsoft 365 企業版測試實驗室指南](m365-enterprise-test-lab-guides.md)

[部署 Microsoft 365 企業版](deploy-microsoft-365-enterprise.md)

[Microsoft 365 企業版文件](https://docs.microsoft.com/microsoft-365-enterprise/)

