---
title: 在 Wix 建立 Office 365 的 DNS 記錄
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
ms.assetid: 7173c635-58b3-400f-95e0-97abe915565e
description: 瞭解如何驗證您的網域，並設定電子郵件、商務用 Skype Online 及其他服務的 DNS 記錄，以供 Office 365 Wix。
ms.openlocfilehash: 8487c49e989bf2db345ae9e6d0e2970c5eb40cb6
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211059"
---
# <a name="create-dns-records-at-wix-for-office-365"></a>在 Wix 建立 Office 365 的 DNS 記錄

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
如果 Wix 是您的 DNS 主機服務提供者，請遵循本文中的步驟來驗證您的網域，並設定電子郵件、商務用 Skype Online 等的 DNS 記錄。
  
以下是要新增的主要記錄。 
  
- [新增 TXT 記錄以供驗證](#add-a-txt-record-for-verification)。
    
- [新增 MX 記錄，以便您網域的電子郵件將會傳送至 Office 365](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365)。
    
- [新增 Office 365 所需的五個 CNAME 記錄](#add-the-five-cname-records-that-are-required-for-office-365)。
    
- [新增 SPF 的 TXT 記錄，以協助防止電子郵件垃圾](#add-a-txt-record-for-spf-to-help-prevent-email-spam)郵件。
    
- [新增 Office 365 所需的兩筆 SRV 記錄](#add-the-two-srv-records-that-are-required-for-office-365)。
    
在 Wix 新增這些記錄之後，您的網域就會設定為搭配 Office 365 服務使用。
  
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-a-txt-record-for-verification"></a>新增 TXT 記錄以供驗證
<a name="BKMK_txt"> </a>

在您將自己的網域用於 Office 365 之前，我們必須先確認您擁有該網域。如果您能在自己的網域註冊機構登入自己的帳戶並能建立 DNS 記錄，Office 365 就能確信您擁有該網域。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。您可以選擇稍後再刪除記錄。 
  
1. 若要開始使用，請移至您的網域頁面 Wix，方法是使用[此連結](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account)。 系統會提示您先登入。
    
2. 在 [**我的網域**] 頁面上，選取 [**高級**] 區域中的 [**編輯 DNS** ] 按鈕。 
    
3. 在 DNS 編輯器的 [ **TXT （文字）** ] 列中，選取 [ **+ 新增其他**]。 
    
4. In the boxes for the new record, type or copy and paste the values from the following table. 
    
||||
|:-----|:-----|:-----|
|**Host Name** <br/> |**TXT Value** (TXT 值) <br/> |**TTL** <br/> |
|自動填入  <br/> |MS=ms *XXXXXXXX*  <br/> **附註：** 這是範例。 在這裡請使用您自己的 [目的地或指向位址] 值，請參閱 Office 365 表格。  [如何找到呢？](../get-help-with-domains/information-for-dns-records.md)|1 Hour <br/> |          |
   
5. 選取 [DNS 編輯器] 頂端的 [**儲存 DNS** ] 按鈕。 
    
6. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
現在您已在網域註冊機構網站新增記錄，請返回 Office 365 並要求 Office 365 尋找該記錄。
  
在 Office 365 找到正確的 TXT 記錄後，您的網域就完成驗證了。
  
1. 在系統管理中心中，移至 **[設定]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">[網域]</a> 頁面。
    
2. 在 **[網域]** 頁面上，選取您要驗證的網域。 
  
  
3. 在 **[設定]** 頁面上，選取 **[開始設定]**。
   
  
4. 在 **[驗證網域]** 頁面上，選取 **[驗證]**。
    
    
  
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>新增 MX 記錄，以將寄往您網域的電子郵件轉至 Office 365
<a name="BKMK_mx"> </a>

1. 若要開始使用，請移至您的網域頁面 Wix，方法是使用[此連結](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account)。 系統會提示您先登入。
    
2. 在 [**我的網域**] 頁面上的 [**信箱**] 區域中，選取 [**設定您的 MX 記錄**] 連結。 
    
3. 從**您的電子郵件提供者**下拉式清單中選擇 [**其他**]。 
    
4. 選取 [ **+ 另外新增**]。
    
5. 在新記錄的方塊中，輸入或複製並貼上下清單格中的值：
    
|**Host Name**|**Points to** (指向)|**Priority** (優先順序)|**TTL**|
|:-----|:-----|:-----|:-----|
|自動填入 <br/> | *\<網域金鑰\>*  .mail.protection.outlook.com  <br/> **附注：** 從您的 Office 365 帳戶取得您* \<的網域金鑰\> * 。   [How do I find this?](../get-help-with-domains/information-for-dns-records.md) |0  <br/> 如需關於優先順序的詳細資訊，請參閱[什麼是 MX 優先順序？](https://support.office.com/article/What-is-MX-priority-2784cc4d-95be-443d-b5f7-bb5dd867ba83) | 1 Hour|
   
6. 如果有列出任何其他的 MX 記錄，請將其全部刪除。 
    
7. 選取 [確定]****。
    
8. 在 [確認] 對話方塊中，選取 **[確定**]。
    
## <a name="add-the-five-cname-records-that-are-required-for-office-365"></a>新增 Office 365 所需的五個 CNAME 記錄
<a name="BKMK_cname"> </a>

1. 若要開始使用，請移至您的網域頁面 Wix，方法是使用[此連結](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account)。 You'll be prompted to login first.
    
2. 在 [**我的網域**] 頁面上，選取 [**高級**] 區域中的 [**編輯 DNS** ] 按鈕。 
    
3. 針對每個 CNAME 記錄，在 DNS 編輯器的 [ **CNAME （別名）** ] 列中，選取 [ **+ 新增其他**]。 
    
4. 在新記錄的方塊中，輸入或複製並貼上下清單格中的值：
    
|**Host Name**|**Points to** (指向)|**TTL**|
|:-----|:-----|:-----|
|autodiscover  <br/> |autodiscover.outlook.com  <br/> |1 Hour  <br/> |
|sip  <br/> |sipdir.online.lync.com  <br/> |1 Hour <br/> |
|lyncdiscover  <br/> |webdir.online.lync.com   <br/> |1 Hour  <br/> |
|enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |1 小時 <br/> |
|enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |1 Hour  <br/> |
   
5. 選取 [DNS 編輯器] 頂端的 [**儲存 DNS** ] 按鈕。 
    
6. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>新增 SPF 的 TXT 記錄以協助防範垃圾郵件
<a name="BKMK_spf"> </a>

> [!IMPORTANT]
> 網域的 SPF 不得擁有一個以上的 TXT 記錄。 如果您的網域具有多筆 SPF 記錄，您將收到電子郵件錯誤，以及傳送及垃圾郵件分類問題。 如果網域已經有 SPF 記錄，請勿為 Office 365 建立一個新的記錄。 而是，請將必要的 Office 365 值新增到目前的記錄，以便擁有包含這兩組值的*單一* SPF 記錄。  
  
1. 若要開始使用，請移至您的網域頁面 Wix，方法是使用[此連結](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account)。 系統會提示您先登入。
    
2. 在 [**我的網域**] 頁面上，選取 [**高級**] 區域中的 [**編輯 DNS** ] 按鈕。 
    
3. 在 DNS 編輯器的 [ **TXT （文字）** ] 列中，選取 [ **+ 新增其他**]。 
    
4. 在新記錄的方塊中，輸入或複製並貼上下清單格中的值：
    
|**Host Name**|**TXT Value** (TXT 值)|**TTL**|
|:-----|:-----|:-----|
|[保留此空白]  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **注意：** 建議您複製並貼上這個項目，好讓所有的間距保持正確。<br/> |TXT  <br/> | 1 Hour |
   
5. 選取 [DNS 編輯器] 頂端的 [**儲存 DNS** ] 按鈕。 
    
6. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>新增兩筆 Office 365 所需的 SRV 記錄
<a name="BKMK_srv"> </a>

1. 若要開始使用，請移至您的網域頁面 Wix，方法是使用[此連結](https://premium.wix.com/wix/api/mpContainerStaticController#/domains?referralAdditionalInfo=account)。 系統會提示您先登入。
    
2. 在 [**我的網域**] 頁面上，選取 [**高級**] 區域中的 [**編輯 DNS** ] 按鈕。 
    
3. 在 DNS 編輯器的 [ **SRV** ] 列中，選取 [ **+ 另外新增**]。 
    
4. 在新記錄的方塊中，輸入或複製並貼上下清單格中的值：
    
|**服務**|**Protocol** (通訊協定)|**名稱**|**Weight** (權數)|**Port** (連接埠)|**Target** (目標)|**Priority** (優先順序)|**TTL**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|sip  |tls  |自動填入 |1   |443   |sipdir.online.lync.com |100 |1 Hour |
|sipfed|tcp |自動填入|1  |5061 |sipfed.online.lync.com|100 | 1 Hour |
   
5. 選取 [DNS 編輯器] 頂端的 [**儲存 DNS** ] 按鈕。 
    
6. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  

