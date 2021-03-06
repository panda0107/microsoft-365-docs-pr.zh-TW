---
title: Microsoft 365 企業版測試環境的 Azure AD 身分識別保護
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/10/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: 設定 Azure AD 身分識別保護，並分析您的 Microsoft 365 企業版測試環境中目前的帳戶。
ms.openlocfilehash: 3f3740e42c7ec909f44a3c761dfc743359b3f030
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/13/2020
ms.locfileid: "42633641"
---
# <a name="azure-ad-identity-protection-for-your-microsoft-365-enterprise-test-environment"></a>Microsoft 365 企業版測試環境的 Azure AD 身分識別保護

*這個測試實驗室指南只能用於 Microsoft 365 企業版測試環境。*

Azure Active Directory （Azure AD）身分識別保護可讓您偵測影響組織身分識別的潛在弱點、設定自動回應，以及調查事件。 本文說明如何使用 Azure AD Identity Protection 來查看測試環境帳戶的分析。

在 Microsoft 365 企業版測試環境中設定 Azure AD 身分識別保護有兩個階段：

1. 建立 Microsoft 365 企業版測試環境。
2. 使用 Azure AD Identity Protection。

![Microsoft Cloud 的測試實驗室指南](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> 按一下[這裡](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf)(英文)，可查看 Microsoft 365 企業版測試實驗室指南堆疊中所有文章的視覺對應。
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a>階段 1：建置您的 Microsoft 365 企業版測試環境

如果您只想以具有最低需求的輕量方式測試 Azure AD 身分識別保護，請遵循[輕量基本](lightweight-base-configuration-microsoft-365-enterprise.md)設定中的指示。
  
如果您想要在模擬的企業中測試 Azure AD 身分識別保護，請依照[傳遞驗證](pass-through-auth-m365-ent-test-environment.md)中的指示進行。
  
> [!NOTE]
> 測試 Azure AD 身分識別保護不需要模擬企業測試環境，其中包括連線到網際網路的模擬內部網路和 Active Directory 網域服務（AD DS）樹系的目錄同步處理。 這裡是以選項形式提供的，可讓您測試 Azure AD 身分識別保護，並在代表一般組織的環境中進行試驗。 
  
## <a name="phase-2-use-azure-ad-identity-protection"></a>階段2：使用 Azure AD 身分識別保護

1. [https://portal.azure.com](https://portal.azure.com)使用 Microsoft 365 企業版測試環境的全域系統管理員帳戶，開啟瀏覽器的私人實例，並登入 Azure 入口網站。
2. 在 Azure 入口網站的搜尋方塊中，輸入**identity protection** ，然後按一下 [ **Azure AD identity protection**]。
3. 在 [身分**識別保護-一覽表**] 中，按一下每個報告以查看報告的內容。
4. 在 [**通知**] 底下，按一下 [**使用者時檢查警示**]。
5. 在 [偵測**到風險的使用者警示**] 窗格中，選取 [**中**]。
6. 針對**電子郵件傳送給下列使用者**，請按一下 [**包含**]，並確認您的全域系統管理員帳戶位於選取的成員清單中。
7. 按一下 **[儲存]**。

按一下 [**保護**] 底下的不同原則，以查看如何進行設定。 如果您建立及啟動原則，請確定它不會封鎖太寬的條件範圍，否則您可能無法登入，即使是全域管理員也是一樣。

如需進一步的測試及實驗，請參閱[模擬風險事件](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook)。

若要瞭解如何在實際執行 Azure AD 身分識別保護的資訊和連結，請參閱身分識別階段中的防範[認證安全](identity-secure-user-sign-ins.md#identity-ident-prot)步驟。

## <a name="next-step"></a>下一步

瀏覽測試環境中的其他[身分識別](m365-enterprise-test-lab-guides.md#identity)功能。

## <a name="see-also"></a>另請參閱

[階段 2：身分識別](identity-infrastructure.md)

[Microsoft 365 企業版測試實驗室指南](m365-enterprise-test-lab-guides.md)

[Microsoft 365 企業版部署](deploy-microsoft-365-enterprise.md)

[Microsoft 365 企業版文件](https://docs.microsoft.com/microsoft-365-enterprise/)
