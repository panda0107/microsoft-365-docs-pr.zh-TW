---
title: 使用 Windows 型 DNS 建立 Office 365 的 DNS 記錄
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
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9eec911d-5773-422c-9593-40e1147ffbde
description: 瞭解如何驗證您的網域，並設定電子郵件、商務用 Skype Online 和其他服務的 DNS 記錄，以 Windows a 為基礎的 Windows DNS for Office 365。
ms.openlocfilehash: d33a2f79111f8951c3ec31ca5680877ad2e7d570
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43210561"
---
# <a name="create-dns-records-for-office-365-using-windows-based-dns"></a>使用 Windows 型 DNS 建立 Office 365 的 DNS 記錄

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
   
如果您使用 Windows 型 DNS 託管自己的 DNS 記錄，請按照本文的步驟設定您電子郵件的記錄、商務用 Skype Online 等。
  
若要開始，您必須[在 Windows 型 dns 中尋找您的 dns 記錄](#find-your-dns-records-in-windows-based-dns)，以便您進行更新。 此外，如果您計畫要同步處理內部部署 Active Directory 與 Office 365，請參閱[在部署 Active directory 中做為 UPN 的非路由電子郵件地址](#non-routable-email-address-used-as-a-upn-in-your-on-prem-active-directory)。
  
新增 DNS 記錄後，出現郵件流程或其他問題的相關問題，請參閱[疑難排解變更功能變數名稱或 DNS 記錄後的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="find-your-dns-records-in-windows-based-dns"></a>在 Windows 架構的 DNS 中尋您的 DNS 記錄
<a name="BKMK_find_your_dns_1"> </a>移至具有您網域之 DNS 記錄的頁面。 如果您是在 Windows Server 2008 中工作，請移至**開始** > **執行**。 如果您是在 Windows Server 2012 中工作，請按 Windows 鍵和**r**。 輸入**dnsmgmnt**，然後選取 **[確定]**。 在 [dns 管理員] 中，展開** \<[dns 伺服器名稱\> \>正向對應區域  **]。 選取您的網域。 您現在可以建立 DNS 記錄了！
   
## <a name="add-mx-record"></a>新增 MX 記錄
<a name="BKMK_add_MX"> </a>

新增 MX 記錄，以便將您網域的電子郵件送至 Office 365。
- 您要新增的 MX 記錄包含一個類似 \<MX token\>.mail.protection.outlook.com 的值 (**[指向位址]** 值)，其中 \<MX token\> 值類似 MSxxxxxxx。 
- 從 Office 365 的 [新增 DNS 記錄] 頁面的 [Exchange Online] 區段中的 [MX] 列中，複製 [點數為下列值] 底下所列的值。 您將會在您要建立的記錄中使用此值。 
- 在網域的 [DNS 管理員] 頁面上，移至 [**動作** > **郵件交換器（MX）**]。 若要尋找網域的此頁面，請參閱[在 Windows 型 dns 中尋找您的 DNS 記錄](#find-your-dns-records-in-windows-based-dns)。  
- 在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值： 
    - 主機名稱： 
    - @Address：在這裡，貼上您剛才從 Office 365 複製的點到位址值。  
    - Pref: 
- 選取 [**儲存變更**]。
- 移除任何過時的 MX 記錄。 如果您有此網域的任何舊版 MX 記錄，可將電子郵件路由傳送至其他地方，請選取每個舊記錄旁邊的核取方塊，然後選取 [**刪除** > **確定]**。 
   
## <a name="add-cname-records"></a>新增 CNAME 記錄
<a name="BKMK_add_CNAME"> </a>

新增 Office 365 所需的 CNAME 記錄。 如果 Office 365 中列出其他 CNAME 記錄，也請同樣按照這裡顯示的一般步驟來新增這些記錄。
  
> [!IMPORTANT]
> 如果您有 Office 365 行動裝置管理 (MDM)，則您必須建立兩筆其他的 CNAME 記錄。 請按照您針對其他四筆 CNAME 記錄所進行的程序執行，但提供下表的值。 （如果您沒有 MDM，您可以略過此步驟。） 

- 在網域的 [DNS 管理員] 頁面上，移至 [**動作** > **CNAME （cname）**]。
- 在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值：  
    - 主機名稱：自動探索
    - 類型： 
    - Cname 位址： autodiscover.outlook.com
- 選取 [ **O**K]。

新增 SIP CNAME 記錄。 
- 在網域的 [DNS 管理員] 頁面上，移至 [**動作** \> **CNAME （cname）**]。 
- 在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值：  
    - 主機名稱： sip
    - 類型： CNAME
    - 位址： sipdir.online.lync.com
- 選取 [確定]****。

新增商務用 Skype Online 自動探索 CNAME 記錄。  
- 在網域的 [DNS 管理員] 頁面上，移至 [**動作** \> **CNAME （cname）**]。 在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值：  
    - 主機名稱： lyncdiscover
    - 類型： CNAME
    - 位址： webdir.online.lync.com
- 選取 [確定]****。
   
### <a name="add-two-cname-records-for-mobile-device-management-mdm-for-office-365"></a>為 Office 365 行動裝置管理 (MDM) 新增兩筆 CNAME 記錄

> [!IMPORTANT]
> 如果您有 Office 365 行動裝置管理 (MDM)，則您必須建立兩筆其他的 CNAME 記錄。 請按照您針對其他四筆 CNAME 記錄所進行的程序執行，但提供下表的值。 > （如果您沒有 MDM，您可以略過此步驟）。 
  

新增 MDM Enterpriseregistration CNAME 記錄。  
- 在網域的 [DNS 管理員] 頁面上，移至 [**動作** \> **CNAME （cname）**]。 
- 在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值：  
- 主機名稱： enterpriseregistration
- 類型： CNAME
- 位址： enterpriseregistration.windows.net
- 選取 [確定]****。 

新增 MDM Enterpriseenrollment CNAME 記錄。 
-  在網域的 [DNS 管理員] 頁面上，移至 [**動作** \> **CNAME （cname）**]。 
-  在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值：  
    - 主機名稱： enterpriseenrollment
    - 類型： CNAME
    - 位址： enterpriseenrollment-s.manage.microsoft.com
- 選取 [確定]****。
   
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>新增 SPF 的 TXT 記錄以協助防範垃圾郵件
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> 網域的 SPF 不得擁有一個以上的 TXT 記錄。 如果您的網域具有多筆 SPF 記錄，您將收到電子郵件錯誤，以及傳送及垃圾郵件分類問題。 如果網域已經有 SPF 記錄，請勿為 Office 365 建立一個新的記錄。 而是，請將必要的 Office 365 值新增到目前的記錄，以便擁有包含這兩組值的*單一* SPF 記錄。 
  
新增網域的 SPF TXT 記錄，以協助防堵垃圾郵件。
  
- 萬一這筆記錄的 [TXT] 值已有其他字串 (例如行銷電子郵件的字串)，沒關係，請保留那些字串，然後再加上這個字串，並分別用雙引號括住字串加以區分。 
- 在您網域的 [DNS 管理員] 頁面上，移至 [**動作** \> **文字（TXT）**]。 
-  在 [**新增資源記錄**] 對話方塊中，確定欄位已設定為嚴格下列的值。 
 > [!IMPORTANT]
> 在某些 Windows DNS 管理員版本中，可能已設定網域，因此當您建立 txt 記錄時，首頁名稱會預設為上層網域。 在此情況中，當您新增 TXT 記錄時，請將主機名稱設定為空白 (無值)，而不是將它設定為 @ 或網域名稱。 

-  主機類型：@
-  記錄類型： TXT
-  Address： v = spf1 包含: spf.protection.outlook.com。 .com-all 
         
-  選取 [確定]****。
   
## <a name="add-srv-records"></a>新增 SRV 記錄
<a name="BKMK_add_SRV"> </a>

新增兩筆 Office 365.所需的 SRV 記錄。

為商務用 Skype Online Web 會議新增 SIP SRV 記錄。  <br/> 
-  在您網域的 [DNS 管理員] 頁面上，移至 [**動作** \> ] [**其他新記錄**]。 
-   在 [**資源記錄類型**] 視窗中，選取 [**服務位置（SRV）**]，然後選取 [**建立記錄**]。 
-   在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值：  
    -  服務： _sip
    -  通訊協定： _tls
    -  優先順序：100
    -  加權：1
    -  連接埠：443
    -  目標（主機名稱）： sipdir.online.lync.com
-  選取 [確定]****。 


為商務用 Skype Online 同盟新增 SIP SRV 記錄。  
-  在您網域的 [DNS 管理員] 頁面上，移至 [**動作** \> ] [**其他新記錄**]。  
-  在 [**資源記錄類型**] 視窗中，選取 [**服務位置（SRV）**]，然後選取 [**建立記錄**]。 
-   在 [**新增資源記錄**] 對話方塊中，確定已將欄位設定為嚴格下列值：  
    -  服務： _sipfederationtls
    -  通訊協定： _tcp
    -  優先順序：100
    -  加權：1
    -  連接埠：5061
    -  目標（主機名稱）： sipfed.online.lync.com
-  選取 [確定]****。 
   
## <a name="add-a-record-to-verify-that-you-own-the-domain-if-you-havent-already"></a>新增記錄以驗證您擁有網域 (若您尚未這麼做)
<a name="BKMK_verify"> </a>

在新增 DNS 記錄以設定 Office 365 服務之前，Office 365 必須先確認您擁有所要新增的網域。若要這麼做，請新增一筆記錄，然後依照下列步驟進行。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。 
  

1. 從 Office 365 收集資訊。  <br/> 
2. 在系統管理中心中，移至 **[設定]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">[網域]</a> 頁面。 
3. 在 [**網域**] 頁面上，于您所驗證之網域的 [**動作**] 欄中，選取 [**開始設定**]。 
4. 在 [**新增網域至 Office 365** ] 頁面上，選取 [**開始步驟 1**]。 
5. 在 [**確認您擁有您的網域**] 頁面上，于 [**請參閱執行此步驟的指示**] 下拉式清單中，選擇 **[一般指示**]。 
6. 從表格複製 [目的地或指向位址] 值。 您在下一步會需要這項資訊。 我們建議您複製並貼上此值，如此一來，所有的間距皆會保持正確。

新增 TXT 記錄。 
-  在您網域的 [DNS 管理員] 頁面上，移至 [**動作** \> **文字（TXT）**]。 
-   在 [**新增資源記錄**] 對話方塊中，選取 [**編輯**]。  
-  在 [**新增資源記錄**] 對話方塊的 [**自訂主機名稱**] 區域中，確定欄位已設定為嚴格下列的值。 

> [!IMPORTANT] 
> 在某些 Windows DNS 管理員版本中，可能已設定網域，因此當您建立 txt 記錄時，首頁名稱會預設為上層網域。 在此情況中，當您新增 TXT 記錄時，請將主機名稱設定為空白 (無值)，而不是將它設定為 @ 或網域名稱。 

- 主機名稱：@
- 類型： TXT
- Address：貼上您剛從 Office 365 複製的目的地或指向位址值。  
- 選取 **[確定** > **完成**]。

在 Office 365 驗證您的網域。  
> [!IMPORTANT]
> 請等候大約15分鐘，再執行這項作業，這樣您剛才建立的記錄便可在網際網路上更新。       

- 回到 Office 365，然後按照下列步驟要求驗證檢查。 這項檢查會尋找您在上述步驟中新增的 TXT 記錄。 找到正確的 TXT 記錄之後，網域即驗證完畢。  
1. 在系統管理中心中，移至 [**安裝** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">網域</a>] 頁面。
2. 在 [**網域**] 頁面上，于您所驗證之網域的 [**動作**] 欄中，選取 [**開始設定**]。 
3. 在 [**確認您擁有您的網域**] 頁面上，選取 [**完成，立即驗證**]，然後在確認對話方塊中，選取 **[完成]**。 
   
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="non-routable-email-address-used-as-a-upn-in-your-on-prem-active-directory"></a>在內部部署 Active Directory 中用來做為 UPN 的非可路由電子郵件地址
<a name="BKMK_ADNote"> </a>

如果您計劃同步處理內部部署 Active Directory 與 Office 365，您會想要確認 Active Directory 使用者主體名稱 (UPN) 尾碼是有效的網域尾碼，而非不受支援的網域尾碼，例如 @contoso.local。 如果您需要變更 UPN 尾碼，請參閱 how [to prepare a 不可路由的網域以進行目錄同步](https://support.office.com/article/e7968303-c234-46c4-b8b0-b5c93c6d57a7)處理。
  
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
