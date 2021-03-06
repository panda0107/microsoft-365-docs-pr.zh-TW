---
title: 讓使用者在 Office 365 中自行重設密碼
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
- Adm_TOC
ms.custom:
- MSStore_Link
- TRN_M365B
- OKR_SMB_Videos
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 5bc3f460-13cc-48c0-abd6-b80bae72d04a
description: 瞭解如何使用自助密碼重設工具來重設密碼。
ms.openlocfilehash: 666d3843f7917cf9bd5718c0ce29f87f93d6effe
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211892"
---
# <a name="let-users-reset-their-own-passwords"></a>讓使用者重設自己的密碼

您是否對大量的重設密碼要求感到不勝其擾？ 做為 Microsoft 365 系統管理員，您可以讓使用者使用[自助密碼重設工具](https://go.microsoft.com/fwlink/p/?LinkId=522677)，這樣您就不需要重設密碼。 這可為您分擔一些工作！ 
  
以下是一些您需要知道的事項：
  
- 您可以使用任何 Office 365 商務、教育或非盈利性收費方案 **，為雲端**使用者取得自助密碼重設。 此工具無法搭配 Office 365 試用版。 
    
- 該工具會使用 Azure。 當您執行這些步驟時，您將會在 Azure 中自動**免費**取得此項功能。 如果您不使用其他的 Azure 功能，開啟自助密碼重設不會花費您任何費用。 
    
- **如果您使用的是內部部署 Active Directory**，則不會套用上述兩個點。 相反地，您可以設定此設定，但**需要使用 AZURE AD Premium 付費訂閱**。 

觀賞有關讓使用者重設其自己密碼的簡短影片。 <br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3AY8S] 

如果您覺得這段影片很有幫助，請查看[適用於小型企業和 Microsoft 365 新手的完整訓練系列](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)。

## <a name="let-people-reset-their-own-passwords"></a>讓使用者重設自己的密碼 

下列步驟會針對公司中的所有人員開啟自助密碼重設。
  
::: moniker range="o365-worldwide"
1.  在系統管理中心中，移至 [**設定** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">安全性 & 隱私權</a>] 頁面。

::: moniker-end

::: moniker range="o365-germany"

1. 在系統<a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">管理中心</a>中，移至 [**設定** \> **安全性&amp;隱私權**] 頁面。

::: moniker-end

::: moniker range="o365-21vianet"

1. 在系統<a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">管理中心</a>中，移至 [**設定** \> **安全性&amp;隱私權**] 頁面。

::: moniker-end

   
2. 在 [**讓您的使用者重設自己的密碼**] 底下，選取**Azure AD 系統管理中心**的連結。 您將能免費取得 Azure！
  
3. 在左側導覽中選取 [**使用者**]，然後選取 [**密碼重設**]。
  
4. 在 [屬性] 頁面上，選取 [**全部**] 以針對您公司內的每個人啟用它，然後選取 [**儲存**]。
  
5. 當使用者登入 Office 365 時，系統將提示使用者輸入額外的連絡資訊以協助日後重設使用者的密碼。

## <a name="related-articles"></a>相關文章

[設定組織的密碼到期原則](../manage/set-password-expiration-policy.md)
  
[設定個別使用者的密碼永不過期](set-password-to-never-expire.md)

[Microsoft 365 商務版訓練影片](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)
