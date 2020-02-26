---
title: 在 eNomCentral 建立 Office 365 的 DNS 記錄
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
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
ms.assetid: a6626053-a9c8-445b-81ee-eeb6672fae77
description: 了解如何驗證您的網域和設定 Office 365 的電子郵件、 商務用 Skype 線上商務和 enomcentral 其他服務的 DNS 記錄。
ms.openlocfilehash: c4cd12667ebf945aa2f354ccfa0bad1688dc9863
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239046"
---
# <a name="create-dns-records-at-enomcentral-for-office-365"></a>在 eNomCentral 建立 Office 365 的 DNS 記錄

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
如果 eNomCentral 是您的 DNS 主機服務提供者，請按照本文所述的步驟驗證網域，並為電子郵件與商務用 Skype Online 等項目設定 DNS 記錄。
  
在 eNomCentral 新增這些記錄之後，您的網域就會設定為搭配 Office 365 服務使用。
  
若要了解使用 Office 365 網站的虛擬主機和 DNS，請參閱[搭配 Office 365 使用公用網站](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)。
  
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-a-txt-record-for-verification"></a>新增 TXT 記錄以供驗證
<a name="BKMK_verify"> </a>

在您將自己的網域用於 Office 365 之前，我們必須先確認您擁有該網域。如果您能在自己的網域註冊機構登入自己的帳戶並能建立 DNS 記錄，Office 365 就能確信您擁有該網域。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。您可以選擇稍後再刪除記錄。 
  
請依照下列步驟操作或[觀看影片 (0:46 從開始)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
1. 首先請用[這個連結](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered)移至 eNom Central 上您的網域頁面。系統會提示您先登入。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. [**我的網域**] 中，選取您想要編輯的網域名稱。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-DYN-BP-CONFIGURE-1-確認-1-1](../media/6e4184a1-9525-47a6-8a8a-9600126c0db4.png)
  
4. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Choose the **Record Type** value from the drop-down list.) 
    
    ||||
    |:-----|:-----|:-----|
    |**Host Name** <br/> |**Record Type** <br/> |**Address** <br/> |
    |@  <br/> |TXT  <br/> |MS=ms *XXXXXXXX*  <br/> **附註：** 這是範例。 Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![eNom-DYN-BP-CONFIGURE-1-確認-1-2](../media/e1f95529-46a6-40f9-9709-9fe66f373bcf.png)
  
5. 選取 [**儲存**]。
    
    ![eNom-DYN-BP-CONFIGURE-1-確認-1-3](../media/d6277ab0-5d03-44e0-968f-fd5de1905423.png)
  
6. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 在系統管理中心，移至 [**設定** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">網域</a>] 頁面。

    
2. 在 [**網域**] 頁面上，選取您要驗證的網域。 
    
    
  
3. 在 [**安裝**] 頁面上，選取 [**啟動安裝程式**。
    
    
  
4. 在 [**驗證網域**] 頁面上，選取 [**驗證**]。
    
    
  
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>新增 MX 記錄，以將寄往您網域的電子郵件轉至 Office 365
<a name="BKMK_add_MX"> </a>

請依照下列步驟操作或[觀看影片 (從 3:40 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
1. 首先請用[這個連結](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered)移至 eNom Central 上您的網域頁面。系統會提示您先登入。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. [**我的網域**] 中，選取您想要編輯的網域名稱。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. 在 [**管理網域**] 下拉式清單中，選擇 [**電子郵件設定**]。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-3](../media/4b438629-afdf-4a47-ab11-56644cdb6158.png)
  
4. 在 [**選取服務**] 下拉式清單中，選擇 [**使用者 (MX)**。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-4](../media/7680ab48-b8d1-4573-b20f-4745a5d7c079.png)
  
5. In the boxes for the new record, type or copy and paste the values from the following table.
    
    |**Host Name**|**Address**|**Pref**|
    |:-----|:-----|:-----|
    |@  <br/> | *\<網域金鑰\>*  .mail.protection.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> **附註：** 取得您*\<網域金鑰\>* 從您的 Office 365 帳戶。           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |10   <br/> 如需關於優先順序的詳細資訊，請參閱[什麼是 MX 優先順序？](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |
       
   ![eNom-DYN-BP-CONFIGURE-1-設定-2-1](../media/c32e8954-8209-4f77-a3a8-4b7aeea325d5.png)
  
6. 選取 [**儲存**]。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-2-2](../media/cf3058ea-9d30-4747-8cf0-2bc13d5ec6be.png)
  
7. 如果有任何其他現有的 MX 記錄，請選取其核取方塊來進行選取。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-2-3](../media/5017ed03-ca76-4c5c-93a7-84ffe24125dc.png)
  
8. 選取 [**刪除檢查**]。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-2-4](../media/072dc039-bddb-4c1f-bb44-5660e77f14b0.png)
  
## <a name="add-the-cname-records-that-are-required-for-office-365"></a>新增 Office 365 所需的 CNAME 記錄
<a name="BKMK_add_CNAME"> </a>

請依照下列步驟操作或[觀看影片 (從 4:24 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
1. 首先請用[這個連結](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered)移至 eNom Central 上您的網域頁面。系統會提示您先登入。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. [**我的網域**] 中，選取您想要編輯的網域名稱。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-5](../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. 選取**新的資料列**。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-3-1](../media/a30f0a88-7b09-411e-9133-e7965bcf1de0.png)
  
5. 在六筆新記錄的方塊中，輸入或複製並貼上下列的值。
    
        (Choose the **Record Type** value from the drop-down list.) 
        
    |**Host Name**|**Record Type**|**Address**|
    |:-----|:-----|:-----|
    |autodiscover (自動探索)  <br/> |CNAME (Alias)  <br/> |autodiscover.outlook.com。  <br/> **This value MUST end with a period (.)** <br/> |
    |sip  <br/> |CNAME (Alias)  <br/> |sipdir.online.lync.com>。  <br/> **This value MUST end with a period (.)** <br/> |
    |lyncdiscover  <br/> |CNAME (Alias)  <br/> |webdir.online.lync.com>。  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseregistration  <br/> |CNAME (Alias) (CNAME (別名))  <br/> |enterpriseregistration.windows.net>。  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseenrollment  <br/> |CNAME (Alias) (CNAME (別名))  <br/> |enterpriseenrollment-s.manage.microsoft.com。  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![eNom-DYN-BP-CONFIGURE-1-設定-3-2](../media/672371c0-51af-44ba-bb18-80286b7676c1.png)
  
6. 選取 [**儲存**]。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-3-3](../media/027b57ce-5699-408b-993b-e46a9ac31090.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>新增 SPF 的 TXT 記錄以協助防範垃圾郵件
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.
  
請依照下列步驟操作或[觀看影片 (從 5:12 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
1. 首先請用[這個連結](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered)移至 eNom Central 上您的網域頁面。系統會提示您先登入。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. [**我的網域**] 中，選取您想要編輯的網域名稱。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-5](../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. 在每一筆新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    (Choose the **Record Type** value from the drop-down list.) 
    
    |**Host Name**|**Record Type**|**Address**|
    |:-----|:-----|:-----|
    |@  <br/> |TXT  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/>**附註：** 建議您複製並貼上這個項目，好讓所有的間距保持正確。           |
   
   ![eNom-DYN-BP-CONFIGURE-1-設定-4-1](../media/64c68697-258d-4044-84b1-c28f4a402e3b.png)
  
5. 選取 [**儲存**]。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-4-2](../media/89f4effa-349e-4734-96a5-cd80b0cecd60.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>新增兩筆 Office 365 所需的 SRV 記錄
<a name="BKMK_add_SRV"> </a>

請依照下列步驟操作或[觀看影片 (從 5:50 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
1. 首先請用[這個連結](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered)移至 eNom Central 上您的網域頁面。系統會提示您先登入。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. [**我的網域**] 中，選取您想要編輯的網域名稱。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-1-5](../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. 若要**新的資料列**的右邊，選取 [**新增 SRV 或 SPF 記錄**。
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-5-1](../media/c73c154d-5aa0-41ef-be25-f43129eb178c.png)
  
5. 在這兩筆新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    |**服務**|**通訊協定**|**優先順序**|**Weight**|**Port**|**目標          (主機名稱)**|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |_sip  <br/> |_tls  <br/> |100  <br/> |1  <br/> |443  <br/> |sipdir.online.lync.com>。  <br/> **This value MUST end with a period (.)** <br/> |
    |_sipfederationtls  <br/> |_tcp  <br/> |100  <br/> |1  <br/> |5061  <br/> |sipfed.online.lync.com。  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![eNom-DYN-BP-CONFIGURE-1-設定-5-2](../media/4d478f40-780f-43b9-940b-712b09da8c63.png)
  
6. 選取 [**儲存**]
    
    ![eNom-DYN-BP-CONFIGURE-1-設定-5-3](../media/d03b6f75-49f2-471d-978d-d32c47cd6aa7.png)
  
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
