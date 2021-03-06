---
title: 適用於 Microsoft 365 測試環境的密碼重設
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/13/2019
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
description: 摘要：設定並測試適用於 Microsoft 365 測試環境的密碼重設。
ms.openlocfilehash: c8d5ed0c7feac98afd3230a305f4ab1f850ca7f8
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/13/2020
ms.locfileid: "42633171"
---
# <a name="password-reset-for-your-microsoft-365-test-environment"></a>適用於 Microsoft 365 測試環境的密碼重設

*這個測試實驗室指南只能用於 Microsoft 365 企業版測試環境。*

Azure Active Directory (Azure AD) 自助密碼重設 (SSPR) 允許使用者重設或解除鎖定其密碼或帳戶。 

本文將以三階段說明如何針對 Microsoft 365 測試環境，設定及測試密碼重設：

1.  建立 Microsoft 365 企業版測試環境。
2.  啟用密碼回寫。
3.  設定及測試「使用者 3」帳戶的密碼重設。
    
![Microsoft Cloud 的測試實驗室指南](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> 按一下[這裡](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf)(英文)，可查看 Microsoft 365 企業版測試實驗室指南堆疊中所有文章的視覺對應。

## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a>階段 1：設定適用於 Microsoft 365 測試環境的密碼雜湊同步處理

首先，請遵循[密碼雜湊同步處理](password-hash-sync-m365-ent-test-environment.md)中的指示。以下是您產生的組態。
  
![使用密碼雜湊同步處理測試環境的模擬企業](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
此組態包含： 
  
- Microsoft 365 E5 或 Office 365 E5 試用版或付費訂閱。
- 簡化的組織內部網域與網際網路的連線，由 Azure 虛擬網路的子網路上的 DC1、APP1 及 CLIENT1 虛擬機器組成 
- Azure AD Connect 會在 APP1 上執行，以將 TESTLAB Active Directory Domain Services (AD DS) 網域同步至 Microsoft 365 或 Office 365 訂閱的 Azure AD 租用戶。

## <a name="phase-2-enable-password-writeback"></a>階段 2：啟用密碼回寫

遵循[測試實驗室指南密碼回寫階段 2](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain) 中的指示。

您必須啟用密碼回寫才能使用密碼重設。
  
## <a name="phase-3-configure-and-test-password-reset"></a>階段 3：設定及測試密碼重設

在這個階段中，您會在透過群組成員資格在 Azure AD 租用戶中設定密碼重設，然後驗證是否運作正常。

首先，在特定 Azure AD 群組中啟用該帳戶的密碼重設。

1. 從您瀏覽器的私用執行個體開啟 [https://portal.azure.com](https://portal.azure.com)，然後使用全域系統管理員帳戶的認證登入。
2. 在 Azure 入口網站中，按一下 [Azure Active Directory] > [群組] > [新增群組]****。
3. 將 [群組類型]**** 設為 [安全性]****、[群組名稱]**** 設為 [PWReset]****，以及將 [成員類型]**** 設為 [指派]****。 
4. 按一下 [成員]****，尋找並選取 [使用者 3]****，然後按一下 [選取]****，接著按一下 [建立]****。
5. 關閉 [群組]**** 窗格。
6. 在 [Azure Active Directory] 窗格中，按一下左側導覽的 [密碼重設]****。
7. 在 [密碼重設屬性]**** 窗格中，選擇 [已啟用自助式密碼重設]**** 選項底下的 [已選取]****。
8. 按一下 [選取群組]****，選取 [PWReset]**** 群組，然後按一下 [選取] > [儲存]****。
9. 關閉私用瀏覽器執行個體。

下一階段，您將測試「使用者 3」帳戶的密碼重設。

1. 開啟新的私用瀏覽器執行個體，並瀏覽至 [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup)。
2. 以「使用者 3」的認證登入。
3. 在 [需要更多資訊]**** 中按一下 [下一步]****。 
5. 在 [避免您失去帳戶的存取權]**** 中，將認證電話設為您的手機號碼，並將認證電子郵件設為您的公司或個人電子郵件帳戶。
7. 兩者皆經過驗證之後，按一下 [狀況良好]****，並關閉瀏覽器的私用執行個體。
8. 開啟新的私用瀏覽器執行個體並前往 [https://aka.ms/sspr](https://aka.ms/sspr)。
9. 輸入「使用者 3」的帳戶名稱，輸入 CAPTCHA 顯示的字元，然後再按一下 [下一步]****。
10. 對於 [驗證步驟 1]****，請按一下 [寄電子郵件到我的備用電子郵件地址]****，然後再按一下 [寄電子郵件]****。當您收到電子郵件後，請輸入驗證碼，然後再按一下 [下一步]****。
11. 在 [取回您的帳戶]**** 中，輸入「使用者 3」帳戶的新密碼，然後按一下 [完成]****。 請記下「使用者 3」帳戶變更的密碼，並儲存到安全的位置。
12. 在相同瀏覽器的新分頁中，前往 [https://portal.office.com](https://portal.office.com)，並以「使用者 3」帳戶名稱及新密碼登入。 您應該會看到 [Microsoft Office 首頁]**** 頁面。

如需在生產中進行密碼重設的相關資訊和連結，請參閱身分識別階段中的「[簡化密碼重設](identity-secure-your-passwords.md#identity-pw-reset)」步驟。

## <a name="next-step"></a>下一步

瀏覽測試環境中的其他[身分識別](m365-enterprise-test-lab-guides.md#identity)功能。

## <a name="see-also"></a>另請參閱

[Microsoft 365 企業版測試實驗室指南](m365-enterprise-test-lab-guides.md)

[部署 Microsoft 365 企業版](deploy-microsoft-365-enterprise.md)

[Microsoft 365 企業版文件](https://docs.microsoft.com/microsoft-365-enterprise/)
