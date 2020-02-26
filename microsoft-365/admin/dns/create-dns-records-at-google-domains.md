---
title: 在 Google Domains 建立 Office 365 的 DNS 記錄
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
ms.assetid: 0db29490-2612-48bc-9b77-1862e7a41a8c
description: 了解以驗證您的網域及設定在 Google Domains for Office 365 的電子郵件、 Lync 與其他服務的 DNS 記錄。
ms.openlocfilehash: c59a3d63797f20b0d3a42647eb68d7699ed63450
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42240826"
---
# <a name="create-dns-records-at-google-domains-for-office-365"></a>在 Google Domains 建立 Office 365 的 DNS 記錄

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
如果 Google Domains 是您的 DNS 主機服務提供者，請按照本文所述的步驟驗證網域，並設定電子郵件與 Lync 等項目的 DNS 記錄。
  
在 Google Domains 新增這些記錄之後，您的網域就會設定為搭配 Office 365 服務使用。
  
若要了解使用 Office 365 網站的虛擬主機和 DNS，請參閱[搭配 Office 365 使用公用網站](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)。
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. 如果您遇到與郵件流程或其他問題新增 DNS 記錄之後，請參閱[尋找並修正新增網域或 Office 365 中的 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-a-txt-record-for-verification"></a>新增 TXT 記錄以供驗證
<a name="BKMK_verify"> </a>

在您將自己的網域用於 Office 365 之前，我們必須先確認您擁有該網域。如果您能在自己的網域註冊機構登入自己的帳戶並能建立 DNS 記錄，Office 365 就能確信您擁有該網域。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。您可以選擇稍後再刪除記錄。 
  
1. 首先請用[這個連結](https://domains.google.com/registrar)移至 Google Domains 上您的網域頁面。系統會提示您登入。若要執行此作業，請執行下列動作：
    
1. 選取 [**登入**]。
    
2. 輸入您的登入認證，然後再選取 [**登入**。
    
2. 在 [**我的網域**] 頁面上，尋找您想要使用與 Office 365 的網域並選取其旁邊的 [**管理**] 連結。 在左側導覽中，選取 [ **DNS**]。
    
3. 在 [* * 自訂資源記錄 * *] 區段的方塊新的記錄，輸入或複製並貼上下表中的值。 
    
    (You may have to scroll down.)
    
    (Choose the **Type** value from the drop-down list.) 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |**Name** <br/> |**Type** <br/> |**TTL** <br/> |**資料** <br/> |
    |@  <br/> |TXT  <br/> |1H]  <br/> |MS=ms *XXXXXXXX*  <br/> **附註：** 這是範例。 Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
4. 選取 **[新增]**。
    
5. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 在系統管理中心，移至 [**設定** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">網域</a>] 頁面。

    
2. 在 [**網域**] 頁面上，選取您要驗證的網域。 
    
3. 在 [**安裝**] 頁面上，選取 [**啟動安裝程式**。
    
4. 在 [**驗證網域**] 頁面上，選取 [**驗證**]。
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. 如果您遇到與郵件流程或其他問題新增 DNS 記錄之後，請參閱[尋找並修正新增網域或 Office 365 中的 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 

  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>新增 MX 記錄，以將寄往您網域的電子郵件轉至 Office 365
<a name="BKMK_add_MX"> </a>

1. 首先請用[這個連結](https://domains.google.com/registrar)移至 Google Domains 上您的網域頁面。系統會提示您登入。若要執行此作業，請執行下列動作：
    
2. 選取 [**登入**]。
    
3. 輸入您的登入認證，然後再選取 [**登入**。
4. 在 [**網域**] 頁面上，在 [**網域**] 區段中，選取**設定 DNS**針對您想要編輯的網域。
    
    > [!IMPORTANT]
    > 如果您擁有 G Suite 電子郵件帳戶，則必須先刪除與該帳戶相關聯的 MX 記錄。G Suite 的 MX 記錄會使您無法新增其他 MX 記錄，包括 Office 365 所需的記錄。請注意，刪除 G Suite 記錄並不會刪除您的 G Suite 帳戶。若要刪除您的 G Suite MX 記錄，請依照下列步驟操作。 
  
5. 在 [**綜合記錄**] 區段的 [ **G Suite** ] 區域中，選取 [**刪除**]。
    
    (You may have to scroll down.)
    
    ![在 [綜合記錄] 區段中選取 [刪除]](../media/bd276b5d-5667-4bb1-a233-2dc5194e7ace.png)
  
6. 選取 [**刪除**]。
    
    ![選取 [刪除]](../media/4413a45a-5b82-4ec6-82c6-0091f5be9696.png)
  
7. In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (You may have to scroll down.)
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**Name**|**Type**|**TTL**|**資料**|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |MX  <br/> |1H]  <br/> |0  *\<網域金鑰\>*  .mail.protection.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> **0**是指 MX 優先順序值。 請將它新增到 MX 值的開頭，並以空格分隔該值的其餘部分。  <br/> **附註：** 取得您\<*網域金鑰*\>從您的 Office 365 帳戶。  [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |
   
    ![輸入或貼上自訂資源記錄] 區段中的值](../media/b660ca9e-984d-449f-ae59-a65fe4e2c6bd.png)
  
5. 選取 **[新增]**。
    
    ![選取 [新增]](../media/32f8f23c-0b80-48da-b08e-4e04052971af.png)
  
6. 如果有任何其他的自訂 MX 記錄，請移除它們。
    
1. MX 記錄資料列中，選取 [**編輯**]。 
    
    ![MX 記錄列中選取 [編輯]](../media/acc53ae9-3b8a-421d-8d11-d4a4108b2353.png)
  
2. 針對每一筆自訂 MX 記錄，在 [**資料**] 方塊中選取的項目，然後按**Delete**鍵以刪除該筆記錄鍵盤上。 
    
    繼續，直到您已刪除的**資料**項目為每個其他的 MX 記錄。 
    
    ![Delete entries in the Data box](../media/28192089-7b38-4d2e-9d52-9b83422c27d5.png)
  
7. 當您刪除**資料**輸入的每個其他的 MX 記錄時，選取 [**儲存**] 以儲存變更。 
    
    ![選取 [儲存]](../media/bf496d01-ccbe-4800-95f4-7b2283f2e5f6.png)
  
## <a name="add-the-five-cname-records-that-are-required-for-office-365"></a>新增 Office 365 所需的五筆 CNAME 記錄

1. 若要開始，移至您的 [Google Domains 頁面] (https://domains.google.com/registrar)並登入。
    
2. 在 [**網域**] 頁面上，在 [**網域**] 區段中，選取**設定 DNS**針對您想要編輯的網域。 
    
3. 新增第一筆 CNAME 記錄。
    
    在 [**自訂資源記錄**] 區段，於新記錄的方塊中輸入或複製並貼上下表第一列的值。 
    
    (You may have to scroll down.)
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**Name**|**Type**|**TTL**|**資料**|
    |:-----|:-----|:-----|:-----|
    |autodiscover  <br/> |CNAME  <br/> |1H]  <br/> |autodiscover.outlook.com。  <br/> **This value MUST end with a period (.)** <br/> |
    |sip  <br/> |CNAME  <br/> |1H]  <br/> |sipdir.online.lync.com>。  <br/> **This value MUST end with a period (.)** <br/> |
    |lyncdiscover  <br/> |CNAME  <br/> |1H]  <br/> |webdir.online.lync.com>。  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseregistration  <br/> |CNAME  <br/> |1H]  <br/> |enterpriseregistration.windows.net>。  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseenrollment  <br/> |CNAME  <br/> |1H]  <br/> |enterpriseenrollment-s.manage.microsoft.com。  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![輸入或貼上自訂資源記錄] 區段中的值](../media/cff9832a-6d57-421f-a183-55320974ed87.png)
  
4. 選取 **[新增]**。
    
    ![選取 [新增]](../media/4a78080a-e0b2-4582-9696-3fe4fea41e91.png)
  
5. 新增其他四筆 CNAME 記錄。
    
    在**自訂資源記錄**] 區段中，在表格中，使用下一列的值來建立記錄，然後再次選擇 [**新增**] 以完成該筆記錄。 
    
    重複此程序，直到您已建立的所有必要的 CNAME 記錄。
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>新增 SPF 的 TXT 記錄以協助防範垃圾郵件

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. 而是，請將必要的 Office 365 值新增至目前的記錄，以便擁有包含這兩組值的單一 SPF 記錄。 需要範例？ 請查看這些[Office 365 的外部網域名稱系統記錄](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords)。 To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md). 
  
1. 首先請用[這個連結](https://domains.google.com/registrar)移至 Google Domains 上您的網域頁面。系統會提示您登入。若要執行此作業，請執行下列動作：
    
1. 選取 [**登入**]。
    
2. 輸入您的登入認證，然後再選取 [**登入**。
    
3. 在 [**網域**] 頁面上，在 [**網域**] 區段中，選取**設定 DNS**針對您想要編輯的網域。 
    
4. [**自訂資源記錄**] 區段，於 [TXT 記錄] 列中，選取 [**編輯**]。 
    
    > [!IMPORTANT]
    > Google Domains 會將 TXT 記錄儲存為一組可包含多個記錄的集合。 當您有至少一個其他的 TXT 記錄時 (例如用於驗證網域的 TXT 記錄)，您必須新增 TXT 新記錄到該記錄集。 任何嘗試輸入額外 TXT 記錄，如個別項目會導致 「**重複記錄**」 錯誤訊息。 
  
    ![在 [TXT 記錄列中選取 [編輯]](../media/eae14850-8d0c-4f29-8587-df8b36129d5f.png)
  
5. 選取 [ **（+）** 控制項。 
    
    ![選取加上的控制項](../media/628604cc-d2b2-42a5-bb5b-13c327b85d9f.png)
  
6. 在每一筆新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    (您可能需要向下捲動。)
    
    |**資料**|
    |:-----|
    |v=spf1 include:spf.protection.outlook.com -all  <br/> 

    > [!NOTE]
    > We recommend copying and pasting this entry, so that all of the spacing stays correct.           
   
   ![輸入或貼上自訂資源記錄] 區段中的值](../media/4645cc4f-9fcc-4626-9674-072ed6fa34c2.png)
  
7. 選取 **[儲存]**。
    
    ![選取 [儲存]](../media/20c4c926-f062-4048-9265-bf752be54e0c.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>新增兩筆 Office 365 所需的 SRV 記錄
<a name="BKMK_add_SRV"> </a>

1. 首先請用[這個連結](https://domains.google.com/registrar)移至 Google Domains 上您的網域頁面。系統會提示您登入。若要執行此作業，請執行下列動作：
    
2. 選取 [**登入**]。
    
3. 輸入您的登入認證，然後再選取 [**登入**。
    
4. 在 [**網域**] 頁面上，在 [**網域**] 區段中，選取**設定 DNS**針對您想要編輯的網域。 
    
5. 新增第一筆 SRV 記錄。
    
    In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (You may have to scroll down.)
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**Name**|**Type**|**TTL**|**資料**|
    |:-----|:-----|:-----|:-----|
    |_sip._tls|SRV|1H]|100 1 443 sipdir.online.lync.com>。 **此值必須以英文句點 （.） 結尾。****附註：** 建議您複製並貼上這個項目，好讓所有的間距保持正確。           |
    |_sipfederationtls._tcp|SRV|1H]|100 1 5061 sipfed.online.lync.com>。 **This value MUST end with a period (.)**

    We recommend copying and pasting this entry, so that all of the spacing stays correct.       
   
    ![輸入或貼上自訂資源記錄] 區段中的值](../media/429d06a9-c0af-4961-b7d2-7a8dea6db37e.png)
  
6. 選取 **[新增]**。
    
    ![選取 [新增]](../media/89df6efd-e641-4441-baa2-d9a890424569.png)
  
7. 新增另一筆 SRV 記錄。
    
    在**自訂資源記錄**] 區段中，在表格中，使用第二列的值來建立記錄，然後再次選擇 [**新增**] 以完成該筆記錄。 
    
    > [!NOTE]
    > Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. 如果您遇到與郵件流程或其他問題新增 DNS 記錄之後，請參閱[尋找並修正新增網域或 Office 365 中的 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  