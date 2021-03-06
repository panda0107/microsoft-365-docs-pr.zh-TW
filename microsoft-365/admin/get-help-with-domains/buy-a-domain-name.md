---
title: 在 Office 365 中購買網域名稱
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
ms.assetid: 1561140a-16a9-4a02-822d-a989250e479d
description: 瞭解如何在 Office 365 中購買功能變數名稱。
ms.custom: okr_smb
ms.openlocfilehash: 89bc24683cd98d2c9f420d1470a864eef857c9b4
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211143"
---
# <a name="buy-a-domain-name-in-office-365"></a>在 Office 365 中購買網域名稱

 *若要新增、修改或移除網域，您**必須**是[企業或企業方案](https://products.office.com/business/office)的**全域系統管理員**。這些變更會影響整個承租人、*自訂*的系統管理員或*一般使用者*無法進行這些變更。*  

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
### <a name="sign-in-and-go-to-settings--domains--buy-a-domain"></a>登入並前往設定\>網域\>購買網域

1. 在系統管理中心中，移至 **[設定]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">[網域]</a> 頁面。
    
3. 在 [**網域**] 頁面上，選取 [**購買網域**]。
    
您可以從下列頂層網域選擇您要的網域。
  
- 。 .biz
    
- .com
    
- 。資訊
    
- 。 me
    
- .mobi
    
- .net
    
- org
    
- 。電視
    
- 。 co.uk
    
- org.uk
    

> [!NOTE]
> 當您選取 [**購買網域**] 時，當租使用者透過 Microsoft 合作夥伴購買/管理時，可能會重新導向至您的 Microsoft 合作夥伴網站。

### <a name="domain-privacy"></a>網域隱私權
在購買網域時，我們會提供免費的網域隱私權訂閱。 這可讓您的連絡人資訊以 ICANN 私人的方式註冊您的網域。 [瞭解更多資訊。](https://whois.icann.org/en/privacy-and-proxy-services)
  
### <a name="buy-a-domain-from-another-domain-registrar"></a>向其他網域註冊機構購買網域
如果您想要從[GoDaddy](https://www.godaddy.com)以外的網域註冊機構購買網域，我們建議您在下列其中一個支援自動安裝的產品（網域連接）。 
  
- [1&amp;1 IONOS](https://www.1and1.com/)
- [Wordpress](https://www.wordpress.com) 

   
### <a name="transfer-your-domain-to-a-different-domain-registrar"></a>將網域移轉到其他網域註冊機構

如果負責管理您網域的提供者，並不支援所有需要的 DNS 記錄，您可以將網域移轉到其他註冊機構。移轉網域後，您需變更收款對象，以續約並保留您的網域名稱。
  
Request the transfer at the registrar that you want to move your domain to. Look on their website for an option such as **Transfer DNS**. Be aware that after they make the changes, it can take a few days update across the Internet.
 



::: moniker range="o365-21vianet"
## <a name="how-to-buy-a-domain-for-office-365-operated-by-21vianet"></a>如何購買網域以用於由 21Vianet 所提供的 Office 365



如果您還沒有自己的網域，您可以輕鬆地在線上向網域名稱註冊機構、網域轉售商，甚至是目前的網際網路提供者購買網域。您註冊 由 21Vianet 提供的 Office 365 時即會獲得網域名稱，例如 contoso.partner.onmschina.cn，但您可能會想要使用自訂網域名稱，例如 fourthcoffee.com。
  
如要在 Office 365 中設定網域名稱，您必須擁有網域，而且必須變更網域的幾個 DNS 記錄。
  
> [!CAUTION]
> 部分網域註冊機構或 DNS 主機服務提供者不允許建立 Office 365 所需的所有 DNS 記錄。下列主機服務提供者則支援所有必要的記錄。如果您想使用其他的主機服務提供者，請[Service limitations when your hosting provider does not support SRV, CNAME, TXT, or redirection](https://support.office.com/article/dfbb03e3-08c1-4c4e-b2f0-891665b29b77)。 
  
(在網域註冊機構) 註冊好您的網域後，請以系統管理員身分登入 Office 365 並設定網域，以將它用於電子郵件地址及其他服務。
  
> [!NOTE]
> The SharePoint Online Public Website information in this article only applies if your organization purchased Office 365 prior to March 9, 2015. 

## <a name="domain-registrars-that-support-all-dns-records-required-for-office-365"></a>支援 Office 365 所需之所有 DNS 記錄的網域註冊機構

- [Oray](https://oray.com/)
    
- [HiChina](https://www.hichina.com/)
    
- [east.net](http://www.east.net/)
    
- [BIZCN](https://www.bizcn.com/)
    
::: moniker-end

## <a name="related-articles"></a>相關文章

[新增網域至 Office 365](../setup/add-domain.md)

[網域常見問題集](../setup/domains-faq.md)

[取得 Office 365 網域的說明](get-help-with-domains.md)

[更新 DNS 記錄以保留您的網站與目前的主機服務提供者](https://docs.microsoft.com/microsoft-365/admin/dns/update-dns-records-to-retain-current-hosting-provider) 