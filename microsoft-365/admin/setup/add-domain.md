---
title: 新增網域至 Office 365
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
- Adm_O365_Setup
- Adm_O365
- Adm_TOC
ms.custom:
- TopSMBIssues
- SaRA
- MSStore_Link
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 6383f56d-3d09-4dcb-9b41-b5f5a5efd611
description: 在您的 DNS 主機上新增 DNS 記錄，將您的網域新增至 Microsoft 365 系統管理中心中的 Office 365。 安裝精靈會引導您完成此程式。
ms.openlocfilehash: 746163b83190a73326ad589b8e3bc9377ddaa9b4
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43209637"
---
# <a name="add-a-domain-to-office-365"></a>新增網域至 Office 365

 若您找不到所需功能，請**[檢查網域常見問題集](domains-faq.md)**。 
  
 *若要新增、修改或移除網域，您**必須**是[企業或企業方案](https://products.office.com/business/office)的**全域系統管理員**。這些變更會影響整個承租人、*自訂*的系統管理員或*一般使用者*無法進行這些變更。*  

 請遵循下列步驟來新增、設定或繼續設定網域。 

::: moniker range="o365-worldwide"
  
::: moniker-end

::: moniker range="o365-germany"

> [!VIDEO https://www.microsoft.com/videoplayer/embed/dda6df6d-37b0-41ff-905b-089448355a31?autoplay=false]
  
::: moniker-end

::: moniker range="o365-worldwide"

1. 移至位於 <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> 的系統管理中心。

::: moniker-end
::: moniker range="o365-germany"

1. 移至位於 <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a> 的系統管理中心。

::: moniker-end

::: moniker range="o365-21vianet"

1. 移至位於 <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a> 的系統管理中心。

::: moniker-end
    
2. 移至 [**安裝** > **網域**] 頁面。 

3. 選取 [**新增網域**]。
    
4. 輸入您要新增的功能變數名稱，然後選取 **[下一步]**。
    
5. 選擇您要如何驗證您擁有該網域。
    
    1. 如果您的網域註冊于 GoDaddy 或 1&amp;1，請選取 [登**入** > **] [下一步]** ，Office 365[將會自動設定記錄](../get-help-with-domains/domain-connect.md)。
    
    2. 您可以傳送一封含有驗證碼的電子郵件給網域的已登記連絡人。 如果您無法辨識或存取記錄中的電子郵件，您可以使用第三個選項。
    
    3. 您可以使用 TXT 記錄來驗證您的網域。 選取 **[下一步]，然後選取 [下一步]** ，查看如何將此 DNS 記錄新增至您註冊機構網站的指示。 在您新增記錄後，可能需要長達30分鐘的時間來進行驗證。 
    
6. 選擇您想要如何進行 DNS 變更，Office 才能使用您的網域。
    
    1. 如果您想要讓 Office 自動設定 DNS，請選擇 [**為我新增 dns 記錄**]。 
    
  
    2. 如果您只想要將特定的 Office 365 服務附加至您的網域，請選擇 [**我要自行新增 DNS 記錄**]，否則請稍後再進行此操作。 **如果您確切知道您在做什麼，請選擇此選項。**
    
7. 如果您選擇*自行新增 DNS 記錄*，請選取 **[下一步]** ，您將會看到一個頁面，其中包含您需要新增至註冊機構網站以設定網域的所有記錄。 
    
  
  
    如果入口網站無法辨認您的註冊機構，您可以[遵循這些一般指示](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md) (機器翻譯)。
    
    查看我們的[特定主機指示](https://support.office.com/article/ae950c9e-e8d9-4108-b0cb-449156998580) 來尋找您的主機，並遵循步驟來新增您需要的所有記錄。 
    
    如果您不知道您網域的 DNS 主機提供者或網域註冊機構，請參閱[尋找您的網域註冊機構或 DNS 主機服務提供者](../get-help-with-domains/find-your-domain-registrar.md)。
    
    如果您想稍後等候，請滾動至底部，然後選取 [**略過此步驟**]。
    
8. 選取 **[完成]** -您已經完成！ 

## <a name="related-articles"></a>相關文章

[網域常見問題集](domains-faq.md)

[什麼是網域？](../get-help-with-domains/what-is-a-domain.md)

[在 Office 365 中購買網域名稱](../get-help-with-domains/buy-a-domain-name.md)

[設定您的網域 (主機專用指示)](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md)

[取得 Office 365 網域的說明](../get-help-with-domains/get-help-with-domains.md)
