---
title: 在 EOP 中設定使用者垃圾郵件通知
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
ms.collection:
- M365-security-compliance
description: 您可以針對預設的全公司內容篩選原則或是網域所套用的自訂內容篩選原則，設定使用者垃圾郵件通知。
ms.openlocfilehash: 45cc75a7b090df86d0c5f9b1d47d452520693530
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078170"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a>在 EOP 中設定使用者垃圾郵件通知
  
> [!IMPORTANT]
> 本主題適用於要保護內部部署信箱的 Exchange Online Protection (EOP) 獨立版客戶。 保護雲端託管信箱的 Exchange Online 客戶應改閱讀下列主題：[設定使用者垃圾郵件通知中 Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md)。 
  
您可以針對預設的全公司內容篩選原則或是網域所套用的自訂內容篩選原則，設定使用者垃圾郵件通知。啟用使用者垃圾郵件通知訊息，可讓您的使用者自行管理其被當成垃圾郵件隔離的郵件。使用者或群組所套用的原則或具有例外狀況的原則所套用的原則，無法使用使用者垃圾郵件通知。
  
使用者垃圾郵件通知包含使用者在您設定的時間期間 (您可指定 1 到 15 天之間的值) 內收到，被當成垃圾郵件隔離的所有郵件清單。您也可以設定用來撰寫通知郵件的語言。
  
之後收到通知郵件，使用者可以選擇下列選項：

**預覽**郵件如果您想要預覽的內容或之前採取動作的標頭。

**下載**郵件如果您想要檢閱的訊息和附件 （如果有的話） 之前採取行動裝置上。

**版本**如果郵件不是垃圾郵件，而且您希望 Office 365 將郵件傳送至您的信箱。

**釋出 & 允許寄件者**如果郵件不是垃圾郵件和您想要新增至安全的寄件者和收件者清單的未來的電子郵件的寄件者的 Office 365。 請記住您的系統管理員可能會有您的安全寄件者清單會覆寫其他組織整體允許/封鎖組態。

**版本 & 報表**，如果郵件不是垃圾郵件和您想要將郵件傳送至您的信箱及該問題報告給 Microsoft 進行分析。

**封鎖寄件者**如果您希望 Office 365 將寄件者新增至封鎖的寄件者清單。
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>開始之前有哪些須知？
<a name="sectionSection0"> </a>

預估完成時間：5 分鐘
  
您必須已獲指派權限，才能執行此程序或這些程序。若要查看您需要的權限，請參閱 [EOP 中的功能權限](feature-permissions-in-eop.md)主題中的「反垃圾郵件」項目。 
  
適用於此主題中程序的鍵盤快速鍵相關資訊，請參閱[Exchange 系統管理員的鍵盤快速鍵置在 Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)。
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>使用 EAC 來設定使用者垃圾郵件通知

1. 在 Exchange 系統管理中心 (EAC)，瀏覽至 [**保護** > **垃圾郵件篩選器**。
    
2. 選取要啟用使用者垃圾郵件通知 (預設為停用) 的內容篩選原則。
    
3. In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link. 
    
4. 在後續的對話方塊中，您可以設定下列選項：
    
1. **啟用使用者垃圾郵件通知** 選取此核取方塊，以啟用此原則的使用者垃圾郵件通知。(反之，如果此原則已啟用，您可以清除此核取方塊，以停用此原則的使用者垃圾郵件通知。) 
    
2. **傳送使用者垃圾郵件通知的間隔時間 (天數)** 指定傳送使用者垃圾郵件通知的頻率。預設值為 3 天。您可以指定 1 到 15 天之間的值。例如，如果您指定 7 天，則此通知將包含在過去 7 天內對象為該使用者，卻被當成垃圾郵件隔離的所有郵件的清單。 
    
3. **通知語言** 您可以使用下拉式清單，選取用來撰寫此原則之使用者垃圾郵件通知的語言。 
    
5. 按一下 **[儲存]**。右側窗格便會出現內容篩選原則設定的摘要，包括使用者垃圾郵件通知設定。
    
> [!NOTE]
>  使用者垃圾郵件通知只會對已啟用的內容篩選原則作用。 >  每天只傳送一次使用者垃圾郵件通知。無法向任何特定客戶保證通知傳遞的時間，且無法加以設定。 
  
 **提示：** 如果您想要在完全實作使用者垃圾郵件通知之前將其傳送給有限的使用者集，藉以測試使用者垃圾郵件通知，請建立一個自訂內容篩選器原則，為使用者所在的網域啟用使用者垃圾郵件通知。 接著，在 EAC 中，[**郵件流程\>規則**，且您想要的使用者的例外狀況從 quarantine@messaging.microsoft.com （傳送通知電子郵件通訊） 建立郵件流程規則 （也稱為傳輸規則） 來封鎖郵件若要收到通知。 下圖是從網域 Contoso.com 建立兩個使用者 (SaraD 和 AlexD) 之例外狀況的範例： 
  
![測試使用者垃圾郵件通知的傳輸規則](../media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>如需詳細資訊

[設定您的垃圾郵件篩選原則](configure-your-spam-filter-policies.md)
  