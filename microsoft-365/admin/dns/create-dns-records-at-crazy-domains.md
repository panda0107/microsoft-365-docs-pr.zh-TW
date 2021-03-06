---
title: 在 Crazy Domains 建立 Office 365 的 DNS 記錄
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
ms.assetid: 6386d63e-b78f-4736-90e7-b99a2c116a9f
description: 瞭解如何驗證您的網域，以及如何設定電子郵件、商務用 Skype Online 和其他服務的 DNS 記錄，以便在 Office 365 的古怪網域上進行。
ms.openlocfilehash: 74c9a940f8d6f52c31712357557ea8cfda76e6bb
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211820"
---
# <a name="create-dns-records-at-crazy-domains-for-office-365"></a>在 Crazy Domains 建立 Office 365 的 DNS 記錄

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
如果 Crazy Domains 是您的 DNS 主機服務提供者，請按照本文所述的步驟驗證網域，並設定電子郵件與商務用 Skype Online 等項目的 DNS 記錄。
  
在 Crazy Domains 新增這些記錄之後，您的網域就會設定為搭配 Office 365 服務使用。
  
若要了解使用 Office 365 網站的虛擬主機和 DNS，請參閱[搭配 Office 365 使用公用網站](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)。
  
> [!NOTE]
> DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-a-txt-record-for-verification"></a>新增 TXT 記錄以供驗證
<a name="BKMK_verify"> </a>

在您將自己的網域用於 Office 365 之前，我們必須先確認您擁有該網域。如果您能在自己的網域註冊機構登入自己的帳戶並能建立 DNS 記錄，Office 365 就能確信您擁有該網域。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。您可以選擇稍後再刪除記錄。 
  
1. 首先請用[這個連結](https://manage.crazydomains.com/members/domains/)移至 Crazy Domains 上您的網域頁面。系統會提示您先登入。
    
    ![CrazyDomains-BP-Configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. 在 [**我的帳戶**] 區段中，選取 [**網域**]。
    
    ![CrazyDomains-BP-Configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. 在 [**網功能變數名稱稱**] 頁面上的 [**網域**] 區段中，選取您要更新的網功能變數名稱稱。 
    
    ![CrazyDomains-BP-Configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. 在 [ **DNS 設定**] 區段中，選取下拉式清單圖示。 
    
    ![CrazyDomains-BP-Configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. 選取 [**新增記錄**]。
    
    ![CrazyDomains-BP-Configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. Choose **TXT Record** from the **Add Record** drop-down list. 
    
    ![CrazyDomains-BP-Verify-1-1](../../media/f0ffdefb-d7a5-47df-bb5e-bf8a3bcc9b01.png)
  
7. 選取 **[新增]**。
    
    ![CrazyDomains-BP-Verify-1-2](../../media/b0cd623a-67f7-4bae-a5b5-507f5a106123.png)
  
8. 在每一筆新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    |**Sub Domain**|**Text Record**|
    |:-----|:-----|
    |(Leave this field empty.)  <br/> |MS=ms *XXXXXXXX*  <br/> **附註：** 這是範例。 在這裡請使用您自己的 [目的地或指向位址] 值，請參閱 Office 365 表格。           [如何找到呢？](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![CrazyDomains-BP-Verify-1-3](../../media/3867de97-6a98-4475-9bda-470bac75d483.png)
  
9. 選取 [**更新**]。
    
    ![CrazyDomains-BP-Verify-1-4](../../media/0e416df6-b7a2-4dd7-971c-f1cc31df30da.png)
  
10. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
現在您已在網域註冊機構網站新增記錄，請返回 Office 365 並要求 Office 365 尋找該記錄。
  
在 Office 365 找到正確的 TXT 記錄後，您的網域就完成驗證了。
  
1. 在系統管理中心中，移至 **[設定]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">[網域]</a> 頁面。

    
2. 在 **[網域]** 頁面上，選取您要驗證的網域。 
    
    
  
3. 在 **[設定]** 頁面上，選取 **[開始設定]**。
    
    
  
4. 在 **[驗證網域]** 頁面上，選取 **[驗證]**。
    
    
  
> [!NOTE]
>  DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>新增 MX 記錄，以將寄往您網域的電子郵件轉至 Office 365
<a name="BKMK_add_MX"> </a>

1. 首先請用[這個連結](https://manage.crazydomains.com/members/domains/)移至 Crazy Domains 上您的網域頁面。系統會提示您先登入。
    
    ![CrazyDomains-BP-Configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. 在 [**我的帳戶**] 區段中，選取 [**網域**]。
    
    ![CrazyDomains-BP-Configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. 在 [**網功能變數名稱稱**] 頁面上的 [**網域**] 區段中，選取您要更新的網功能變數名稱稱。 
    
    ![CrazyDomains-BP-Configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. 在 [ **DNS 設定**] 區段中，選取下拉式清單圖示。 
    
    ![CrazyDomains-BP-Configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. 選取 [**新增記錄**]。
    
    ![CrazyDomains-BP-Configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. 從 [**新增記錄：** ] 下拉式清單中，選擇 [ **MX 記錄**]。 
    
    ![CrazyDomains-BP-Configure-2-1](../../media/63f7ab77-e686-4e7b-a3a2-1ac28a02d5f3.png)
  
7. 選取 **[新增]**。
    
    ![CrazyDomains-BP-Configure-2-2](../../media/a60680a1-2513-498c-b42f-8ffa575ee48e.png)
  
8. 在新記錄的方塊中，輸入或複製並貼上下表中的值。
    
    （從下拉式清單中選擇 [**優先順序**] 值。） 
    
    |**Mail For Zone (區域郵件)**|**優先順序**|**Assigned To Server (指派給伺服器)**|
    |:-----|:-----|:-----|
    |(將此欄位保留空白。)  <br/> |1   <br/> 如需關於優先順序的詳細資訊，請參閱[什麼是 MX 優先順序？](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> | *\<網域金鑰\>*  .mail.protection.outlook.com  <br/> **附注：** 從您的 Office 365 帳戶取得您* \<的網域金鑰\> * 。           [如何找到呢？](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![CrazyDomains-BP-Configure-2-3](../../media/e27df6a6-19a6-4e58-9716-a74be1c3f8da.png)
  
9. 選取 [**更新**]。
    
    ![CrazyDomains-BP-Configure-2-4](../../media/ba25cdef-a436-48bf-b0e9-5dffd03234a4.png)
  
10. 如果 [ **Mx 記錄**] 區段中列出任何其他 MX 記錄，請針對其中一個記錄選取 [**修改**]。 
    
    ![CrazyDomains-BP-Configure-2-5](../../media/9acdda39-33ec-4b24-ad83-91c26f9c599b.png)
  
11. 選取 [刪除]****。
    
    ![CrazyDomains-BP-Configure-2-6](../../media/50b0e263-6f21-41b3-8fa0-7dd55dbe6c2e.png)
  
12. 選取 [**更新**] 以確認刪除。 
    
    ![CrazyDomains-BP-Configure-2-7](../../media/db751bfe-31c2-4632-a491-6893eda38a51.png)
  
13. 使用相同方法移除清單中其他所有 MX 記錄，直到只剩下您先前在本程序中新增的記錄為止。
    
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a>新增 Office 365 所需的六筆 CNAME 記錄
<a name="BKMK_add_CNAME"> </a>

1. 首先請用[這個連結](https://manage.crazydomains.com/members/domains/)移至 Crazy Domains 上您的網域頁面。系統會提示您先登入。
    
    ![CrazyDomains-BP-Configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. 在 [**我的帳戶**] 區段中，選取 [**網域**]。
    
    ![CrazyDomains-BP-Configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. 在 [**網功能變數名稱稱**] 頁面上的 [**網域**] 區段中，選取您要更新的網功能變數名稱稱。 
    
    ![CrazyDomains-BP-Configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. 在 [ **DNS 設定**] 區段中，選取下拉式清單圖示。 
    
    ![CrazyDomains-BP-Configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. 選取 [**新增記錄**]。
    
    ![CrazyDomains-BP-Configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. 從 [**新增記錄：** ] 下拉式清單中，選擇 [ **CNAME 記錄**]。 
    
    ![CrazyDomains-BP-Configure-3-1](../../media/2f02538b-fc79-46d2-a2b7-1022eaf0fb08.png)
  
7. 選取 **[新增]**。
    
    ![CrazyDomains-BP-Configure-3-2](../../media/4c5929cf-1c21-4af9-899b-e36091f0f14d.png)
  
8. 新增六筆 CNAME 記錄的第一筆。
    
    在每一筆新記錄的方塊中，輸入或複製並貼上下表第一列中的值。
    
    |**Sub Domain**|**Alias for (別名)**|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |
    |enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![CrazyDomains-BP-Configure-3-3](../../media/81a7b837-3f4d-4565-89a9-380e4d318acf.png)
  
9. 選取 [**新增 CNAME 記錄**]。
    
    ![CrazyDomains-BP-Configure-3-4](../../media/9bcba729-7085-4ebc-8183-ecde82f5c364.png)
  
10. 新增第二筆 CNAME 記錄。
    
    在新記錄的方塊中，使用表格中下一列的值，然後再選取 [**新增 CNAME 記錄**]。
    
    重複這個程序，直到六筆 CNAME 記錄全部建立完畢。
    
11. 選取 [**更新**] 以儲存變更。 
    
    ![CrazyDomains-BP-Configure-3-5](../../media/dbe578f6-359c-428c-b296-ca624cecfc3c.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>新增 SPF 的 TXT 記錄以協助防範垃圾郵件
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> 網域的 SPF 不得擁有一個以上的 TXT 記錄。 如果您的網域具有多筆 SPF 記錄，您將收到電子郵件錯誤，以及傳送及垃圾郵件分類問題。 如果網域已經有 SPF 記錄，請勿為 Office 365 建立一個新的記錄。 而是，請將必要的 Office 365 值新增到目前的記錄，以便擁有包含這兩組值的*單一* SPF 記錄。 
  
1. 首先請用[這個連結](https://manage.crazydomains.com/members/domains/)移至 Crazy Domains 上您的網域頁面。系統會提示您先登入。
    
    ![CrazyDomains-BP-Configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. 在 [**我的帳戶**] 區段中，選取 [**網域**]。
    
    ![CrazyDomains-BP-Configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. 在 [**網功能變數名稱稱**] 頁面上的 [**網域**] 區段中，選取您要更新的網功能變數名稱稱。 
    
    ![CrazyDomains-BP-Configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. 在 [ **DNS 設定**] 區段中，選取下拉式清單圖示。 
    
    ![CrazyDomains-BP-Configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. 選取 [**新增記錄**]。
    
    ![CrazyDomains-BP-Configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. 從 [**新增記錄：** ] 下拉式清單中選擇 [ **TXT 記錄**]。 
    
    ![CrazyDomains-BP-Configure-4-1](../../media/7f2461e2-0468-49bd-9eb0-981e9b2f72d6.png)
  
7. 選取 **[新增]**。
    
    ![CrazyDomains-BP-Configure-4-2](../../media/64ef9e1f-676d-46e2-9253-a83d9bcd1c4e.png)
  
8. 在新記錄的方塊中，輸入或貼上下表中的值。
    
    |**Sub Domain**|**Text Record**|
    |:-----|:-----|
    |(將此欄位保留空白。)  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **注意：** 建議您複製並貼上這個項目，好讓所有的間距保持正確。           |
   
    ![CrazyDomains-BP-Configure-4-3](../../media/e7fd524a-c94b-4cdd-b264-67abb532a71b.png)
  
9. 選取 [**更新**]。
    
    ![CrazyDomains-BP-Configure-4-4](../../media/d4f378ee-0f14-46ae-ba32-1596660ecf91.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>新增兩筆 Office 365 所需的 SRV 記錄
<a name="BKMK_add_SRV"> </a>

1. 首先請用[這個連結](https://manage.crazydomains.com/members/domains/)移至 Crazy Domains 上您的網域頁面。系統會提示您先登入。
    
    ![CrazyDomains-BP-Configure-1-1](../../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. 在 [**我的帳戶**] 區段中，選取 [**網域**]。
    
    ![CrazyDomains-BP-Configure-1-2](../../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. 在 [**網功能變數名稱稱**] 頁面上的 [**網域**] 區段中，選取您要更新的網功能變數名稱稱。 
    
    ![CrazyDomains-BP-Configure-1-3](../../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. 在 [ **DNS 設定**] 區段中，選取下拉式清單圖示。 
    
    ![CrazyDomains-BP-Configure-1-4-1](../../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. 選取 [**新增記錄**]。
    
    ![CrazyDomains-BP-Configure-1-4-2](../../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. 從 [**新增記錄：** ] 下拉式清單中選擇 [ **SRV 記錄**]。 
    
    ![CrazyDomains-BP-Configure-5-1](../../media/156acebc-7f6d-4b5e-8493-6bc62ca0ee27.png)
  
7. 選取 **[新增]**。
    
    ![CrazyDomains-BP-Configure-5-2](../../media/6a711df7-4215-49b2-b58f-1cf1a242b383.png)
  
8. 新增兩筆 SRV 記錄中的第一筆。
    
    在每一筆新記錄的方塊中，輸入或複製並貼上下表第一列中的值。
    
    |**Record Type** (記錄類型)|**Sub Domain**|**Priority** (優先順序)|**Weight** (權數)|**Port** (連接埠)|**Target** (目標)|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |SRV Record (SRV 記錄)  <br/> |_sip。 _tls  <br/> |100  <br/> |1   <br/> |443  <br/> |sipdir.online.lync.com  <br/> |
    |SRV Record (SRV 記錄)  <br/> |_sipfederationtls。 _tcp  <br/> |100  <br/> |1   <br/> |5061  <br/> |sipfed.online.lync.com  <br/> |
   
    ![CrazyDomains-BP-Configure-5-3](../../media/cc0ea6eb-7358-434e-bd1a-2737725c6d41.png)
  
9. 選取 [**新增 SRV 記錄**]。
    
    ![CrazyDomains-BP-Configure-5-4](../../media/de4ec312-6833-469a-b23a-f376140a35ca.png)
  
10. 新增另一筆 SRV 記錄。
    
    在新記錄的方塊中，使用下表第二列中的值。
    
11. 選取 [**更新**] 以儲存變更。 
    
    ![CrazyDomains-BP-Configure-5-5](../../media/f0bb1dd6-3772-4293-bf74-710f635e0658.png)
  
> [!NOTE]
> DNS 變更生效通常約需 15 分鐘的時間。而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[變更網域名稱或 DNS 記錄之後所發生問題的疑難排解](../get-help-with-domains/find-and-fix-issues.md)。 
  
