---
title: 切換 Office 365 for business 方案之前備份資料
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- commerce
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
ms.assetid: a1da52c9-2167-4973-9e6d-492314a79b87
description: 在切換 Office 365 訂閱或使用者離開組織之前，請先備份 Outlook、OneDrive、Yammer 及 SharePoint 內容。
ms.openlocfilehash: 3d8196bcbd0296e1b6e681b1077d165e168d2f2f
ms.sourcegitcommit: e695bcfc69203da5d3d96f3d6a891664a0e27ae2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2020
ms.locfileid: "43105744"
---
# <a name="back-up-data-before-switching-office-365-for-business-plans"></a>切換 Office 365 for business 方案之前備份資料

如果使用者要切換至另一個訂閱，該訂閱的資料相關服務較少或使用者離開組織，則可以在將其儲存在 Office 365 中的資料複本，在切換至新的訂閱之前加以下載。
  
## <a name="save-a-copy-of-outlook-information"></a>儲存 Outlook 資訊複本

如果使用者有 Outlook，他們可以在切換其計畫之前，[將電子郵件、連絡人及行事曆匯出或備份至 outlook .pst](https://support.office.com/article/14252b52-3075-4e9b-be4e-ff9ef1068f91)檔案。
  
當切換到新的計畫完成之後，使用者可以[從 Outlook .pst 檔案匯入電子郵件、連絡人及行事曆](https://support.office.com/article/431a8e9a-f99f-4d5f-ae48-ded54b3440ac)。
  
## <a name="save-files-stored-in-onedrive-for-business"></a>儲存在商務 OneDrive 中儲存的檔案

在切換至不同的訂閱之前，使用者可以[從 OneDrive 或 SharePoint 中將檔案和資料夾下載](https://support.office.com/article/5c7397b7-19c7-4893-84fe-d02e8fa5df05)至不同的位置，例如電腦硬碟上的資料夾，或組織網路上的檔案共用。
  
## <a name="save-yammer-information"></a>儲存 Yammer 資訊

系統管理員可以將所有郵件、記事、檔案、主題、使用者和群組匯出為 .zip 檔案。 如需詳細資訊，請參閱[從 Yammer Enterprise 匯出資料](https://docs.microsoft.com/yammer/manage-security-and-compliance/export-yammer-enterprise-data)。 開發人員也可以使用[YAMMER API](https://go.microsoft.com/fwlink/p/?linkid=842495)來執行這項作業。
  
## <a name="how-to-save-sharepoint-information"></a>如何儲存 SharePoint 資訊

如果使用者從已 SharePoint 線上的訂閱切換為沒有該使用者的訂閱，則**SharePoint**磚將不再出現在其 Office 365 功能表中。
  
不過，只要新的訂閱與其所切換的所在組織位於相同組織內，使用者仍可以存取 SharePoint 小組網站。 他們可以使用小組網站的直接 URL 來查看和更新筆記本、檔、工作及行事曆。
  
> [!TIP]
> 建議使用者在其訂閱切換之前先前往小組網站，然後在其瀏覽器中將 URL 儲存為我的最愛或書簽。
  
依預設，小組網站的 URL 為此格式：
  
```html
https://<orgDomain>/_layouts/15/start.aspx#/SitePages/Home.aspx
```

其中_ \<orgDomain\> _是組織的 URL。
  
例如，如果組織的網域為 contoso.onmicrosoft.com，小組網站的直接 URL 就會是https://contoso.onmicrosoft.com/_layouts/15/start.aspx#/SitePages/Home.aspx。
  
當然，使用者也可以將 SharePoint 線上檔從 SharePoint 小組網站下載至他們的本機電腦，也可以在任何時間從其他位置下載。