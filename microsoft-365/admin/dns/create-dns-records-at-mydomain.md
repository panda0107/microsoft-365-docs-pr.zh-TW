---
title: 在 MyDomain 建立 Office 365 的 DNS 記錄
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9982191d-ed79-46a9-b2e7-317d1a3a9867
description: 了解如何在 Office 365 的 [我的網域] 中驗證網域，並為電子郵件、商務用 Skype Online和其他服務設定 DNS 記錄。
ms.openlocfilehash: 1a75c2ab0077cac07781e5102c43e53ed965b1df
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211688"
---
# <a name="create-dns-records-at-mydomain-for-office-365"></a>在 MyDomain 建立 Office 365 的 DNS 記錄


  
 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
> [!CAUTION]
> MyDomain 網站不支援 SRV 記錄，這表示有幾項商務用 Skype Online 和 Outlook Web App 功能將無法使用。 無論您使用哪一種 Office 365 方案，只要在 MyDomain 管理 DNS 記錄，都會受到[重大的服務限制](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx)，建議您改換不同的 DNS 主機服務提供者。 
  
儘管有這些服務限制，如果您仍選擇在 MyDomain 管理您的 Office 365 DNS 記錄，請按照本文中的步驟設定電子郵件與商務用 Skype Online 等項目的 DNS 記錄。
    
在 MyDomain 新增這些記錄之後，您的網域就會設定為搭配 Office 365 服務使用。
  
若要了解使用 Office 365 網站的虛擬主機和 DNS，請參閱[搭配 Office 365 使用公用網站](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)。
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. 而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。 在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[尋找並修正在 Office 365 中新增網域或 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-a-txt-record-for-verification"></a>新增 TXT 記錄以供驗證
<a name="BKMK_verify"> </a>

在您將自己的網域用於 Office 365 之前，我們必須先確認您擁有該網域。如果您能在自己的網域註冊機構登入自己的帳戶並能建立 DNS 記錄，Office 365 就能確信您擁有該網域。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。您可以選擇稍後再刪除記錄。 
  
1. 首先，請用[此連結](https://www.mydomain.com/controlpanel)移至您在 MyDomain 的網域頁面。系統會提示您先登入。
    
2. 在 [我的最愛]**** 區段中，選取 [網域中央]****。
    
3. 在 [網域]**** 下方，選取要編輯的網域名稱。
    
4. 在 [總覽]**** 區段，選取 [DNS]****。
    
5. 從 [修改]**** 下拉式清單中，選擇 [TXT/SPF 記錄]****。
    
6. 在 [內容] 底下，於新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    ||
    |:-----|
    |**內容** <br/> |
    |MS=ms *XXXXXXXX*  <br/> **附註：** 這是範例。 在這裡請使用您自己的 [目的地或指向位址] 值，請參閱 Office 365 表格。 [如何找到呢？](../get-help-with-domains/information-for-dns-records.md)          |
   
7. 選取 [新增]****。
    
8. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
現在您已在網域註冊機構網站新增記錄，請返回 Office 365 並要求 Office 365 尋找該記錄。
  
在 Office 365 找到正確的 TXT 記錄後，您的網域就完成驗證了。
  
1. 在系統管理中心中，移至 **[設定]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">[網域]</a> 頁面。
    
2. 在 **[網域]** 頁面上，選取您要驗證的網域。 
    
3. 在 **[設定]** 頁面上，選取 **[開始設定]**。
    
4. 在 [驗證網域]**** 頁面上，選取 [驗證]****。
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. 而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。 在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[尋找並修正在 Office 365 中新增網域或 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>新增 MX 記錄，以將寄往您網域的電子郵件轉至 Office 365
<a name="BKMK_add_MX"> </a>

1. 首先，請用[此連結](https://www.mydomain.com/controlpanel)移至您在 MyDomain 的網域頁面。系統會提示您先登入。
    
2. 在 [我的最愛]**** 區段中，選取 [網域中央]****。
    
3. 在 [網域]**** 下方，選取要編輯的網域名稱。
    
4. 在 [總覽]**** 區段，選取 [DNS]****。
    
5. 在 [Modify] (修改)**** 下拉式清單中，選擇 [MX Record] (MX 記錄)****。
    
    ![MyDomain-BP-Configure-2-1](../../media/bbfba978-8c53-471b-8c9e-8ae62e559d15.png)
  
6. 在新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    |**優先順序**|**Host**|**Points to: (指向:)**|
    |:-----|:-----|:-----|
    |0  <br/> 如需關於優先順序的詳細資訊，請參閱[什麼是 MX 優先順序？](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |@  <br/> | *\<網域金鑰\>*  .mail.protection.outlook.com  <br/> **注意：** 從您的 Office 365 帳戶取得您的\<*網域金鑰*\>。 > [如何找到這項資訊？](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![MyDomain-BP-Configure-2-2](../../media/3e19cec3-7f3b-493d-81f7-cda30ba007d5.png)
  
7. 選取 [新增]****。
    
    ![MyDomain-BP-Configure-2-3](../../media/1a1951a8-11d7-405d-bef5-285bbb053ce8.png)
  
8. 如果有任何其他現有的 MX 記錄，請針對每一筆記錄，選取 [Actions] (動作)**** 欄中的 [Remove] (移除)****，將它刪除。 
    
    ![MyDomain-BP-Configure-2-4](../../media/42576149-e056-4a81-a5fd-2c5dfac44e2e.png)
  
9. 選取 [確定]****。
    
    ![MyDomain-BP-Configure-2-5](../../media/d6b70eb7-b79c-499e-82ff-ecef2e300368.png)
  
## <a name="add-the-cname-records-that-are-required-for-office-365"></a>新增 Office 365 所需的 CNAME 記錄
<a name="BKMK_add_CNAME"> </a>

1. 首先，請用[此連結](https://www.mydomain.com/controlpanel)移至您在 MyDomain 的網域頁面。系統會提示您先登入。
    
2. 在 [我的最愛]**** 區段中，選取 [網域中央]****。
    
3. 在 [網域]**** 下方，選取要編輯的網域名稱。
    
4. 在 [總覽]**** 區段，選取 [DNS]****。
    
5. 在 [Modify] (修改)**** 下拉式清單中，選取 [CNAME Alias] (CNAME 別名)****。
    
    ![MyDomain-BP-Configure-3-1](../../media/628267fc-d37b-42ef-bb92-265284e339ac.png)
  
6. 新增第一筆 CNAME 記錄。
    
    在每一筆新記錄的方塊中，輸入或複製並貼上下表第一列中的值。
    
    |**Host**|**Points to: (指向:)**|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |
    |enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![MyDomain-BP-Configure-3-2](../../media/3c8660b3-40bb-453d-8b99-4d22032bc4b3.png)
  
7. 選取 [新增]**** 以新增第一筆記錄。 
    
    ![MyDomain-BP-Configure-3-3](../../media/103a1d99-70da-4fdf-9291-7dd058ec6c4a.png)
  
8. 新增第二筆 CNAME 記錄。
    
    使用上表中第二列的值，然後選取 [新增]**** 以新增第二筆記錄。 
    
    以此類推，使用表格中第三、四、五、六列的值新增其他記錄。
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>新增 SPF 的 TXT 記錄以協助防範垃圾郵件
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> 網域的 SPF 不得擁有一個以上的 TXT 記錄。 如果您的網域具有多筆 SPF 記錄，您將收到電子郵件錯誤，以及傳送及垃圾郵件分類問題。 If you already have an SPF record for your domain, don't create a new one for Office 365. 而是，請將必要的 Office 365 值新增至目前的記錄，以便擁有包含這兩組值的單一 SPF 記錄。 需要範例？ 請參閱這些 [Office 365 的外部網域名稱系統記錄](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords)。 若要驗證您的 SPF 記錄，您可以使用其中一種 [SPF 驗證工具](../setup/domains-faq.md)。 
  
1. 首先，請用[此連結](https://www.mydomain.com/controlpanel)移至您在 MyDomain 的網域頁面。系統會提示您先登入。
    
2. 在 [我的最愛]**** 區段中，選取 [網域中央]****。
    
3. 在 [網域]**** 下方，選取要編輯的網域名稱。
    
4. 在 [總覽]**** 區段，選取 [DNS]****。
    
5. 從 [修改]**** 下拉式清單中，選擇 [TXT/SPF 記錄]****。
    
    ![MyDomain-BP-Configure-4-1](../../media/c461c762-52e6-4fde-b5bc-4dd5e5d62ed3.png)
  
6. 在 [內容] 底下，於新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    |**內容**|
    |:-----|
    |v=spf1 include:spf.protection.outlook.com -all  <br/> **注意：** 建議您複製並貼上這個項目，好讓所有的間距保持正確。           |
   
    ![MyDomain-BP-Configure-4-2](../../media/17d43106-88e6-47e5-aeba-0f18484acf3e.png)
  
7. 選取 [新增]****。
    
    ![MyDomain-BP-Configure-4-3](../../media/b3670563-b620-470c-a42b-2c77888981f8.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>新增兩筆 Office 365 所需的 SRV 記錄
<a name="BKMK_add_SRV"> </a>

> [!CAUTION]
> MyDomain 網站不支援 SRV 記錄，這表示有幾項商務用 Skype Online 和 Outlook Web App 功能將無法使用。 無論您使用哪一種 Office 365 方案，只要在 MyDomain 管理 DNS 記錄，都會受到[重大的服務限制](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx)，建議您改換不同的 DNS 主機服務提供者。 
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. 而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。 在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[尋找並修正在 Office 365 中新增網域或 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
