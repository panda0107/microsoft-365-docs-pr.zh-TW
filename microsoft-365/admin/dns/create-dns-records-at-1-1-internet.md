---
title: 在 1&1 IONOS for Office 365 建立 DNS 記錄
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
ms.assetid: 5762c3ca-1de2-4999-bfe5-4c5e25a8957e
description: 瞭解如何驗證您的網域，並設定電子郵件、商務用 Skype Online 及其他服務的 DNS 記錄，以供 Office 365 1&1 IONOS。
ms.openlocfilehash: e31c9d9d08e29156ff6197c030de6b0f4169b5f4
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211868"
---
# <a name="create-dns-records-at-11-ionos-for-office-365"></a>在 1&1 IONOS for Office 365 建立 DNS 記錄

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
> [!CAUTION]
> 請注意，1&1 IONOS 不允許網域同時具有 MX 記錄和最上層自動探索 CNAME 記錄。 這會限制您可設定 Exchange Online for Office 365 的方式。 有一種解決方法，但只有在您已具備在 1&1 IONOS 建立子域的經驗時，**才**建議使用此方法。 > 如果這項[服務限制](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx)您選擇在 1&1 IONOS 管理您自己的 OFFICE 365 DNS 記錄，請遵循本文中的步驟來驗證您的網域，並設定電子郵件、商務用 Skype Online 等的 DNS 記錄。 
  
在 1&1 IONOS 新增這些記錄之後，您的網域就會設定為搭配 Office 365 服務使用。
  
若要了解使用 Office 365 網站的虛擬主機和 DNS，請參閱[搭配 Office 365 使用公用網站](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)。
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. 而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。 在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[尋找並修正在 Office 365 中新增網域或 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="add-a-txt-record-for-verification"></a>新增 TXT 記錄以供驗證

在您將自己的網域用於 Office 365 之前，我們必須先確認您擁有該網域。如果您能在自己的網域註冊機構登入自己的帳戶並能建立 DNS 記錄，Office 365 就能確信您擁有該網域。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。您可以選擇稍後再刪除記錄。 
  
請依照下列步驟操作或[觀看影片 (從 0:42 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-1-1-Internet-for-Office-365-543fb112-ecf5-47ae-b096-07f3f942a089?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
1. 若要開始使用，請移至您的網域頁面，1&1 IONOS，方法是使用[此連結](https://my.1and1.com/)。 You'll be prompted to log in.
    
2. 選取 [**管理網域**]。
    
3. 在 [**網域中心**] 頁面上，找到您要更新的網域，然後選取該網域的 [**面板**] （ **v**）控制。
    
4. 在 [**網域設定**] 區域中，選取 [**編輯 DNS 設定**]。
    
5. 在 [ **TXT 和 SRV 記錄**] 區段中，選取 [**新增記錄**]。
    
6. In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    ||||
    |:-----|:-----|:-----|
    |**類型** <br/> |**Prefix** <br/> |**Name Value** <br/> |
    |TXT  <br/> |（將此欄位保留空白）  <br/> |MS=ms *XXXXXXXX*  <br/> 請注意：這是一個範例。 在這裡請使用您自己的 [目的地或指向位址] 值，請參閱 Office 365 表格。 [如何找到呢？](../get-help-with-domains/information-for-dns-records.md)          |
   
7. 選取 **[儲存]**。
    
8. 再次選取 [**儲存**]。 
    
9. 在 [**編輯 DNS 設定**] 對話方塊中，選取 **[是]**。
    
10. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
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

請依照下列步驟操作或[觀看影片 (從 3:22 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-1-1-Internet-for-Office-365-543fb112-ecf5-47ae-b096-07f3f942a089?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
> [!NOTE]
> 如果您已登錄1und1.de，請[在這裡登入](https://go.microsoft.com/fwlink/?linkid=859152)。 
  
1. 若要開始使用，請移至您的網域頁面，1&1 IONOS，方法是使用[此連結](https://my.1and1.com/)。 You'll be prompted to log in.
    
2. 選取 [**管理網域**]。
    
3. 在 [**網域中心**] 頁面上，找到您要更新的網域，然後選取該網域的 [**面板**] （ **v**）控制。
    
4. 在 [**網域設定**] 區域中，選取 [**編輯 DNS 設定**]。
    
5. 在 [ **MX** Record] （mx 記錄）區段的 [郵件交換器（MX 記錄）] 區域中，選取 [**其他郵件伺服器**]。<br/>(You may have to scroll down.)<br/>![1&amp;1-BP-Configure-2-1](../../media/b0db72ae-9431-460f-ba7a-3268590b892e.png) <br/>
  
6. 如果已列出任何 MX 記錄，請選取該記錄，然後按下鍵盤上的**delete**鍵，以刪除每一筆記錄。<br/>(如果未列出 MX 記錄，請繼續下一個步驟)。<br/>![1&amp;1-BP-Configure-2-2](../../media/4a39bac7-7310-481d-bda4-1dd5c220c60f.png)<br/>
  
7. 在 [ **MX 1** ] 記錄的方塊中，輸入或複製並貼上下表中的值。 
    
    |**MX 1**|**優先順序**|
    |:-----|:-----|
    | *\<網域金鑰\>*  .mail.protection.outlook.com  <br/>  附注：從您\<的 Office 365\>帳戶取得您的網域金鑰。 [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |10   <br/> 如需關於優先順序的詳細資訊，請參閱[什麼是 MX 優先順序？](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> | 
    
    ![1和 1-設定2和3](../../media/3afb04d1-7bbf-4147-89ae-561e14ded26d.png)<br/>
  
8. 選取 **[儲存]**。<br/>(You may have to scroll down.)<br/>![1&amp;1-BP-Configure-2-4](../../media/355b3ba7-4d2b-45ed-aa17-ac4affb54fe3.png)
  
9. 在 [**編輯 DNS 設定**] 對話方塊中，選取 **[是]**。<br/>![在 [編輯 DNS 設定] 對話方塊中選取 [是]](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a>新增 Office 365 所需的六筆 CNAME 記錄
<a name="BKMK_add_CNAME"> </a>

1&1 IONOS 需要一種方法，讓您可以搭配使用 MX 記錄和 Office 365 電子郵件服務所需的 CNAME 記錄。 此項變通方法需要您在 1&1 IONOS，建立一組子域，並將它們指派給 CNAME 記錄。
  
> [!IMPORTANT]
> 請確認您至少有兩個可用的子網域，才能開始進行此程序。 只有在您已有在 1&1 IONOS 建立子域的經驗時，才建議使用此解決方案。 
  
### <a name="basic-cname-records"></a>基本 CNAME 記錄

請按照下列步驟操作或[觀看影片 (從 3:57 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-1-1-Internet-for-Office-365-543fb112-ecf5-47ae-b096-07f3f942a089?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
> [!NOTE]
> 如果您已登錄1und1.de，請[在這裡登入](https://go.microsoft.com/fwlink/?linkid=859152)。 
  
1. 若要開始使用，請移至您的網域頁面，1&1 IONOS，方法是使用[此連結](https://my.1and1.com/)。 You'll be prompted to log in.
    
2. 選取 [**管理網域**]。
    
3. 在 [**網域中心**] 頁面上，尋找您要更新的網域，然後選取 [**管理子域**]。<br/>![1&amp;1-BP-Configure-3-0](../../media/d570d03f-5c38-463d-809e-5bb9e4fb2777.png) <br/>現在您會建立兩個子域，並為每個子域設定一個**別名**值。<br/>（這是必要的，因為 1&1 IONOS 只支援一個最上層 CNAME 記錄，但 Office 365 需要數個 CNAME 記錄。）<br/>首先，建立自動探索子網域。
    
4. 在 [**子域一覽**] 區段中，選取 [**建立子域**]。
    
    ![1&amp;1-BP-設定-3-1](../../media/95c63639-eb80-443d-8951-98e8b6cdcc4f.png)
  
5. 在 [**建立**新子域的子域] 方塊中，輸入或複製並貼上下清單格中的 [**建立子域**] 值。 （您將在稍後的步驟中新增**別名**值。）

    |**建立子網域**|**Alias**|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com   | 

    ![1&amp;1-BP-Configure-3-2](../../media/9be45113-ebaf-48e6-983c-a7e6ff9eea45.png)
  
6. 選取 [**建立子域**]。<br/>![1&amp;1-BP-Configure-3-3](../../media/1e7bc874-f174-4597-8c08-df611d16a74d.png)
  
7. 在 [**子域一覽**] 區段中，找出您剛剛建立的**自動**探索子域，然後選取該子域的 [**面板] （v）** 控制。 <br/>![1&amp;1-BP-Configure-3-4](../../media/10e2e446-3e54-4fb2-8a29-8c442536cc31.png)
  
8. 在 [**子域設定**] 區域中，選取 [**編輯 DNS 設定**]。 <br/>![1&amp;1-BP-Configure-3-5](../../media/5c602118-b89b-4897-9faf-0736be8a6a0d.png)
  
9. 在 [ **A/AAAA 記錄（IP 位址）** ] 區段的 [ **IP 位址（A 記錄）** ] 區域中，選取 [ **CNAME**]。<br/>![1&amp;1-BP-Configure-3-6](../../media/7f57f468-fbee-4440-a53d-3e334d8e5b71.png)
  
10. 在 [**別名：** ] 方塊中，只輸入或複製並貼上下清單格中的**別名**值。<br/> 
    
    |**建立子網域**|**Alias**|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com   |

    ![1&amp;1-BP-Configure-3-7](../../media/afac3118-3337-4f99-98dd-a7ca930230ce.png)
  
11. 選取 [**我的感知**免責聲明] 的核取方塊。<br/>![1&amp;1-BP-Configure-3-8-1](../../media/6c4cac1a-23f2-4ff3-b2d1-3dca908638d2.png)
  
12. 選取 **[儲存]**。<br/>![1&amp;1-BP-Configure-3-8-2](../../media/ea1dfc06-c175-4146-ab40-da4d162097e1.png)
  
  
### <a name="additional-cname-records"></a>額外 CNAME 記錄

下列程序中產生的額外 CNAME 記錄會啟用商務用 Skype Online 服務。您會採用與您已經建立兩筆 CNAME 記錄時所採用的相同步驟。
  
1. 建立第三個子網域 (Lyncdiscover)。<br/>在 [**子域一覽**] 區段中，選取 [**建立子域**]。
    
2. 在 [**建立**新子域的子域] 方塊中，輸入或複製並貼上下清單格中的 [**建立子域**] 值。 （您將在稍後的步驟中新增**別名**值。）<br/> 
    
    |**建立子網域**|**Alias**|
    |:-----|:-----|
    |lyncdiscover   |webdir.online.lync.com  |
   
3. 選取 [**建立子域**]。
    
4. 在 [**網域中心**] 頁面上，選取 [**管理子域**]。
    
5. 在 [**子域一覽**] 區段中，尋找您剛才建立的**lyncdiscover**子域，然後選取該子域的 [**面板] （v）** 控制。 <br/>在 [**子域設定**] 區域中，選取 [**編輯 DNS 設定**]。
    
6. 在 [ **A/AAAA 記錄（IP 位址）** ] 區段的 [* * IP 位址（A 記錄）]] 區域中，選取 [ **CNAME**]。
    
7. 在 [**別名：** ] 方塊中，只輸入或複製並貼上下清單格中的**別名**值。 <br/>
    
    |**建立子網域**|**Alias**|
    |:-----|:-----|
    |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |
   
8. 選取 [**我的感知**免責聲明] 的核取方塊，然後選取 [**儲存**]。
    
9. 在 [**編輯 DNS 設定**] 對話方塊中，選取 **[是]**。
    
10. 建立第四個子網域 (SIP)： <br/>在 [**子域一覽**] 區段中，選取 [**建立子域**]。
    
11. 在 [**建立**新子域的子域] 方塊中，輸入或複製並貼上下清單格中的 [**建立子域**] 值。 （您將在稍後的步驟中新增**別名**值。） <br/>
    
    |**建立子網域**|**Alias**|
    |:-----|:-----|
    |sip  <br/> |sipdir.online.lync.com  <br/> |
   
12. 選取 [**建立子域**]。
    
13. 在 [**網域中心**] 頁面上，選取 [**管理子域**]。
    
14. 在 [**子域一覽**] 區段中，尋找您剛才建立的**sip**子域，然後為該子域選取**面板（v）** 控制。 <br/>在 [**子域設定**] 區域中，選取 [**編輯 DNS 設定**]。
    
15. 在 [ **A/AAAA 記錄（IP 位址）** ] 區段的 [* * IP 位址（A 記錄）]] 區域中，選取 [ **CNAME**]。
    
16. 在 [**別名：** ] 方塊中，只輸入或複製並貼上下清單格中的**別名**值。 
    
    |**建立子網域**|**Alias**|
    |:-----|:-----|
    |sip  <br/> |sipdir.online.lync.com  <br/> |
   
17. 選取 [**我的感知**免責聲明] 的核取方塊，然後選取 [**儲存**]。
    
18. 在 [**編輯 DNS 設定**] 對話方塊中，選取 **[是]**。
    
### <a name="cname-records-needed-for-mdm"></a>MDM 所需的 CNAME 記錄

> [!IMPORTANT]
> 請按照您針對其他四筆 CNAME 記錄所進行的程序執行，但提供下表的值。 
  
|**建立子網域**|**Alias**|
|:-----|:-----|
|enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |
|enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>新增 SPF 的 TXT 記錄以協助防範垃圾郵件

> [!IMPORTANT]
> 網域的 SPF 不得擁有一個以上的 TXT 記錄。 如果您的網域具有多筆 SPF 記錄，您將收到電子郵件錯誤，以及傳送及垃圾郵件分類問題。 如果網域已經有 SPF 記錄，請勿為 Office 365 建立一個新的記錄。 而是，請將必要的 Office 365 值新增到目前的記錄，以便擁有包含這兩組值的*單一* SPF 記錄。 需要範例？ 請參閱這些 [Office 365 的外部網域名稱系統記錄](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0)。 若要驗證您的 SPF 記錄，您可以使用其中一種[spf 驗證工具](../setup/domains-faq.md)。 
  
請依照下列步驟操作或[觀看影片 (從 5:09 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-1-1-Internet-for-Office-365-543fb112-ecf5-47ae-b096-07f3f942a089?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
> [!NOTE]
> 如果您已登錄1und1.de，請[在這裡登入](https://go.microsoft.com/fwlink/?linkid=859152)。 
  
1. 若要開始使用，請移至您的網域頁面，1&1 IONOS，方法是使用[此連結](https://my.1and1.com/)。 You'll be prompted to log in.
    
2. 選取 [**管理網域**]。
    
3. 在 [**網域中心**] 頁面上，找到您要更新的網域，然後選取該網域的 [**面板**] （**v**）控制。
    
4. 在 [**網域設定**] 區域中，選取 [**編輯 DNS 設定**]。
    
5. 在 [ **TXT 和 SRV 記錄**] 區段中，選取 [**新增記錄**]。 <br/>(You may have to scroll down.)
    
6. In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table. <br/>(Choose the **Type** value from the drop-down list.) <br/>
    
    |**類型**|**Prefix**|**Name Value**|
    |:-----|:-----|:-----|
    |TXT  <br/> |(Leave this field empty.)  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **注意：** 建議您複製並貼上這個項目，好讓所有的間距保持正確。           | 
    
    ![TXT 記錄](../../media/0b3ba3b4-64b9-4d68-9ee1-04eb3a17d4c5.png)
  
7. 選取 **[儲存]**。<br/>![新增記錄](../../media/0f222eb9-3bfd-4908-9a99-516cc6fb1d0e.png)
  
8. 選取 **[儲存]**。<br/>![儲存記錄](../../media/86ed1b59-31b2-4094-9cd4-32b94eb09e35.png)
  
9. 在 [**編輯 DNS 設定**] 對話方塊中，選取 **[是]**。<br/>![在 [編輯 DNS 設定] 對話方塊中選取 [是]](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>新增兩筆 Office 365 所需的 SRV 記錄

請依照下列步驟操作或[觀看影片 (從 5:51 處開始)](https://support.office.com/article/Video-Create-DNS-records-at-1-1-Internet-for-Office-365-543fb112-ecf5-47ae-b096-07f3f942a089?ui=en-US&amp;rs=en-US&amp;ad=US)。
  
> [!NOTE]
> 如果您已登錄1und1.de，請[在這裡登入](https://go.microsoft.com/fwlink/?linkid=859152)。 
  
1. 若要開始使用，請移至您的網域頁面，1&1 IONOS，方法是使用[此連結](https://my.1and1.com/)。 You'll be prompted to log in.
    
2. 選取 [**管理網域**]。
    
3. 在 [**網域中心**] 頁面上，找到您要更新的網域，然後選取該網域的 [**面板**] （ **v**）控制。
    
4. 在 [**網域設定**] 區域中，選取 [**編輯 DNS 設定**]。
    
5. 在 [ **TXT 和 SRV 記錄**] 區段中，選取 [**新增記錄**]。
    
6. 新增兩筆 SRV 記錄中的第一筆。<br/>在 [ **Add Record** ] （新增記錄）區域的新記錄方塊中，輸入或複製並貼上下表中第一列的值。 <br/>（從下拉式清單中選擇 [**類型**] 和 [ **TTL** ] 值。） 
    
    |**類型**|**服務**|**Protocol** (通訊協定)|**名稱**|**Host**|**Priority** (優先順序)|**Weight** (權數)|**Port** (連接埠)|**TTL**|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |SRV  <br/> |sip  <br/> |tls  <br/> |(Leave this field empty.)  <br/> |sipdir.online.lync.com  <br/> |100  <br/> |1   <br/> |443  <br/> |3600 (1 小時)  <br/> |
    |SRV  <br/> |sipfederationtls  <br/> |tcp  <br/> |(將此欄位保留空白。)  <br/> |sipfed.online.lync.com  <br/> |100  <br/> |1   <br/> |5061  <br/> |3600 (1 小時)  <br/> |  
    
    ![1&amp;1-BP-Configure-5-1](../../media/087e337d-926b-42ff-b11d-b449cfaed76c.png)
  
7. 選取 **[儲存]**。 <br/>![1&amp;1-BP-Configure-5-2](../../media/aa5f803d-fb24-48e0-976a-6759c5fd252c.png)
  
8. 選取 **[儲存]**。 <br/>![1&amp;1-BP-Configure-5-3](../../media/097e7e95-4899-4878-b6e7-c3abd8193c52.png)
  
9. 在 [**編輯 DNS 設定**] 對話方塊中，選取 **[是]**。 <br/>![在 [編輯 DNS 設定] 對話方塊中選取 [是]](../../media/920cc95f-fedf-4da2-94a4-9cb41ed49bcf.png)
  
10. 新增另一筆 SRV 記錄。 <br/>在 [ **TXT 和 SRV 記錄**] 區段中，選取 [**新增記錄**]。 <br/>在 [**新增記錄**] 區域中，使用表格中另一列的值建立記錄，然後再選取 [**新增**]、[**儲存** **] 及 [是]** 以完成記錄。 
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. 而如果您所做的變更要在整個網際網路 DNS 系統中生效，有時可能需要更久的時間。 在您新增 DNS 記錄後，如有郵件流程或其他方面的問題，請參閱[尋找並修正在 Office 365 中新增網域或 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
