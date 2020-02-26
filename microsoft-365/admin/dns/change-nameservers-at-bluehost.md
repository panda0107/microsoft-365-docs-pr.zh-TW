---
title: 使用 Bluehost 變更名稱伺服器以設定 Office 365
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
ms.assetid: 7712b6af-329c-43a0-af7b-c4e4c1befb0e
description: '了解如何設定 Office 365 來管理您的 DNS 記錄，在 Bluehost。 '
ms.openlocfilehash: 27d73071a08477b0adc372d8a88db2c805fecacf
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239051"
---
# <a name="change-nameservers-to-set-up-office-365-with-bluehost"></a>使用 Bluehost 變更名稱伺服器以設定 Office 365

 若您找不到所需功能，請**[檢查網域常見問題集](../setup/domains-faq.md)**。 
  
如果您希望 Office 365 為您管理 Office 365 DNS 記錄，請按照下列指示進行。(您可視需要[在 Bluehost 管理所有 Office 365 DNS 記錄](create-dns-records-at-bluehost.md)。)
  
## <a name="add-a-txt-record-for-verification"></a>新增 TXT 記錄以供驗證

在您將自己的網域用於 Office 365 之前，我們必須先確認您擁有該網域。如果您能在自己的網域註冊機構登入自己的帳戶並能建立 DNS 記錄，Office 365 就能確信您擁有該網域。
  
> [!NOTE]
> 這筆記錄只會用於驗證您擁有自己的網域，不會影響其他項目。您可以選擇稍後再刪除記錄。 
  
1. 首先請用[這個連結](https://my.bluehost.com/cgi/dm)移至 Bluehost 上您的網域頁面。 You'll be prompted to log in first.
    
2. 在 [**網域**] 頁面上，在 [**網域**] 區域中，尋找您要變更，網域列，然後選取該網域的核取方塊。 
    
    (You may have to scroll down.) 
    
3. 在**domain_name**區域中，在 [ **DNS 區域編輯器**] 列中，選取 [**管理 DNS 記錄**]。
    
4. On the **DNS Zone Editor** page, in the Add DNS Record area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
|||||
|:-----|:-----|:-----|:-----|
|**Host Record** <br/> |**TTL** <br/> |**類型** <br/> |**TXT Value** <br/> |
|@  <br/> |14400  <br/> |TXT  <br/> |MS=ms *XXXXXXXX* <br/> **附註：** 這是範例。 Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md) <br/> |

   
5. 選取 [**新增記錄**]。
    
6. 繼續進行之前，請先稍候幾分鐘，好讓您剛剛建立的記錄能在網際網路上更新。
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 在系統管理中心，移至 [**設定** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">網域</a>] 頁面。

    
2. 在 [**網域**] 頁面上，選取您要驗證的網域。 
    
3. 在 [**安裝**] 頁面上，選取 [**啟動安裝程式**。
    
4. 在 [**驗證網域**] 頁面上，選取 [**驗證**]。
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. 如果您遇到與郵件流程或其他問題新增 DNS 記錄之後，請參閱[尋找並修正新增網域或 Office 365 中的 DNS 記錄之後所發生的問題](../get-help-with-domains/find-and-fix-issues.md)。 
  
## <a name="change-your-domains-nameserver-ns-records"></a>變更您網域的名稱伺服器 (NS) 記錄

如要完成網域設定以用於 Office 365，請在您的網域註冊機構更改網域的 NS 記錄，使它指向 Office 365 主要和次要名稱伺服器。這樣就會設定並讓 Office 365 為您更新網域的 DNS 記錄。我們會新增所有記錄，好讓電子郵件、商務用 Skype Online 和您的公用網站都能使用您的網域，為您做好一切準備。
  
> [!CAUTION]
> 當您變更網域的 NS 記錄以指向 Office 365 名稱伺服器時，所有目前與您網域相關聯的服務都會受到影響。例如，在您完成這項變更之後，凡是傳送到您的網域 (例如 rob@ *your_domain*  .com) 的電子郵件都將開始傳送到 Office 365。 
  
> [!IMPORTANT]
>  下列程序將告訴您如何從清單中，刪除任何其他不想要的名稱以及 how to： 新增如果他們沒有 」 列出正確的名稱伺服器。 當您完成在此區段中，應該會列出的唯一名稱伺服器的步驟 > 是這四個: > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com 
  
1. 首先請用[這個連結](https://my.bluehost.com/cgi/dm)移至 Bluehost 上您的網域頁面。 You'll be prompted to log in first.
    
2. 在 [**網域**] 頁面的**domain_name**區域中，選取您網域的核取方塊，然後選取**名稱伺服器**。
    
    ![Bluehost-BP-Redelegate-1-1](../media/8f384386-197c-4272-9675-82037922dac4.png)
  
3. 在**domain_name**區域中，選取 [**使用自訂名稱伺服器**。
    
    ![Bluehost-BP-Redelegate-1-2](../media/9fb47d21-c4ce-4eee-af90-c9569870a329.png)
  
4. 請根據現在顯示頁面上是否列出名稱伺服器，來選擇下列兩個程序其中一項繼續︰
    
  - 如果有**無**列 」 名稱伺服器，[如果有列出名稱伺服器](#if-there-are-no-nameservers-already-listed)。
    
  - 如果**是**那里 」 列出名稱伺服器，[如果有列出名稱伺服器](#if-there-are-nameservers-already-listed)。
    
### <a name="if-there-are-no-nameservers-already-listed"></a>如果列表上「沒有」名稱伺服器

1. 在 [**使用自訂名稱伺服器**] 區段中，輸入或複製並貼上下表中的值。 
    
|||
|:-----|:-----|
|**第一個空白列** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**第二個空白列** <br/> |ns2.bdm.microsoftonline.com  <br/> |
   
   ![Bluehost-BP-Redelegate-1-3-1](../media/07b13d6d-a34e-45b5-afd5-48ebd4c1344f.png)
  
2. 選取 [**新增資料列**。
    
    ![Bluehost-BP-Redelegate-1-3-2](../media/db34b632-1d10-44b7-aa1f-44bd27bf09e3.png)
  
3. 仍在**使用自訂名稱伺服器**] 區段中，輸入或複製並貼上下表第一列中的值到新的空白列。 
    
|||
|:-----|:-----|
|**第三個空白列** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**第四個空白列** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
    ![Bluehost-BP-Redelegate-1-3-3](../media/480b32bb-af27-40a5-90c5-5617ed02bb41.png)
  
4. 若要新增第四筆名稱伺服器記錄，再選取 [**新增資料列**，並使用上述表格的最後一列中的值建立記錄。 
    
5. 選取 [**儲存名稱伺服器設定**]。
    
    ![Bluehost-BP-Redelegate-1-4](../media/b24a4cfd-924b-4b6d-ad3d-2dea148fc77f.png)
  
> [!NOTE]
> 您的名稱伺服器記錄更新可能需要數小時的時間，才能更新到整個網際網路的 DNS 系統。接著，您的 Office 365 電子郵件和其他服務就能搭配您的網域順利運作。 
  
### <a name="if-there-are-nameservers-already-listed"></a>如果列表上「有」名稱伺服器

> [!CAUTION]
> Follow these steps only if you have existing nameservers other than the four correct nameservers. (也就是刪除只是任何目前的名稱*未*命名為**ns1.bdm.microsoftonline.com**、 **ns2.bdm.microsoftonline.com**、 **ns3.bdm.microsoftonline.com**或**ns4.bdm.microsoftonline.com**。) 
  
1. 如果沒有列出任何其他名稱伺服器，則選取它，然後按鍵盤上的**Delete**鍵逐一刪除。 
    
    ![Bluehost-BP-Redelegate-1-5](../media/d1051c43-f8ff-46d7-af26-3975d3f0f621.png)
  
2. 同樣在 [**使用自訂名稱伺服器**] 區段中，輸入或複製並貼上下表中的值。 
    
|||
|:-----|:-----|
|**第一個空白列** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**第二個空白列** <br/> |ns2.bdm.microsoftonline.com  <br/> |
   
   ![Bluehost-DYN-BP-CONFIGURE-1-重新委派-1-3](../media/1523debf-5eb0-4765-8e05-bcd56e375c20.png)
  
3. 選取 [**新增資料列**。
    
    ![Bluehost-BP-Redelegate-1-3-2](../media/db34b632-1d10-44b7-aa1f-44bd27bf09e3.png)
  
4. 仍在**使用自訂名稱伺服器**] 區段中，輸入或複製並貼上下表第一列中的值到新的空白列。 
    
|||
|:-----|:-----|
|**第三個空白列** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**第四個空白列** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
   ![Bluehost-BP-Redelegate-1-3-3](../media/480b32bb-af27-40a5-90c5-5617ed02bb41.png)
  
5. 若要新增第四筆名稱伺服器記錄，再選取 [**新增資料列**，並使用上述表格的最後一列中的值建立記錄。 
    
6. 選取 [**儲存名稱伺服器設定**]。
    
    ![Bluehost-BP-Redelegate-1-4](../media/b24a4cfd-924b-4b6d-ad3d-2dea148fc77f.png)
  
> [!NOTE]
> 您的名稱伺服器記錄更新可能需要數小時的時間，才能更新到整個網際網路的 DNS 系統。接著，您的 Office 365 電子郵件和其他服務就能搭配您的網域順利運作。 
  