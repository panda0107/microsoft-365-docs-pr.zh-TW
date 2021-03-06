---
title: 當訂閱結束時，我的資料與存取權會發生什麼情況？
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
- commerce
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 4436582f-211a-45ec-b72e-33647f97d8a3
description: 瞭解當您的商務用 Office 365 訂閱到期、停用或取消時，您的資料會發生什麼事。
ms.openlocfilehash: 2529d5027305a9ceaf71033b4de52a867b9fa9fb
ms.sourcegitcommit: 58c1b4208a5e231463091573e40696d08fc39b8e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/25/2020
ms.locfileid: "42955670"
---
# <a name="what-happens-to-my-data-and-access-when-my-office-365-for-business-subscription-ends"></a>當商務用 Office 365 訂閱結束時，我的資料和存取會發生什麼情況？

如果您的訂閱結束時（因為它已到期，或您決定取消），您的 Office 365 服務、應用程式及客戶資料的存取會在訂閱完全關閉之前，先進行多種狀態，否則請*deprovisioned*。 如果您知道這項進展，您將會更好地將您的訂閱傳回使用中狀態過遲之前的狀態，或者，如果您離開 Office 365，請先備份您的資料，再將其最後刪除。
  
## <a name="office-365-for-business-subscription-lifecycle"></a>商務用 Office 365：訂閱生命週期
- 如果您的訂閱已到期，它會經歷下列階段：已到期/已停用/Deprovisioned。 在訂閱到達其結束日期之後，到期的階段會立即開始。
- 如果您關閉年度訂閱上的週期性帳單，它會與到期訂閱相同。 第一個階段的開始是年度訂閱的周年紀念，而不是在您關閉訂閱的週期性帳單設定的日期開始。
- 如果您取消每月的訂閱，它會立即停用（在取消的日期）。 這表示您的使用者將不會立即存取 Office 365 資產，而且只有系統管理員才能存取未來90天的資料。

下表說明商務用 Office 365 訂閱到期時可預期的結果。

| **Active**                                                             | **已<br/>到期（30\*天）**                                                | **停<br/>用（90\*天）**                                               | **取消佈建**                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| *所有可存取的資料*                                               | *所有可存取的資料*                                                     | *僅限系統管理員可存取的資料*                                             | **資料刪除<br/>的 Azure Active Directory 已移除，如果其他服務未使用該 Active Directory** |
| 使用者可以正常存取 Office 365、資料和 Office 應用程式  | 使用者具備 Office 365、檔案及應用程式的一般存取權              | 使用者無法存取 Office 365、檔或應用程式                        | 使用者無法存取 Office 365、檔或應用程式                                     |
| 系統管理員可以正常存取 Office 365、資料和 Office 應用程式 | 系統管理員可以存取系統管理中心，但無法將授權指派給使用者   | 系統管理員可以存取系統管理中心，但無法將授權指派給使用者       | 系統管理員可以存取系統管理中心，以購買及管理其他訂閱             |
|                                                                        | 全域或計費系統管理員可以在系統管理中心重新啟用訂閱 | 全域或計費系統管理員可以在系統管理中心重新啟用訂閱 |                                                                                           |

* 大部分的國家和地區中的產品。
  
> [!NOTE]
> **何謂「客戶資料」？** 客戶資料（如[Microsoft Online 服務條款](https://go.microsoft.com/fwlink/p/?LinkId=613649)中所定義）是指透過客戶使用 Office 365 服務時，由客戶提供給 Microsoft 的所有資料（包括所有的文字、聲音或影像檔）。 若要深入瞭解客戶資料的保護，請參閱[Microsoft 服務信任入口網站入門](https://support.office.com/article/f30e2353-0bd6-41ed-8347-eea1fb8d2662)。
  
## <a name="what-are-my-options-if-my-subscription-is-about-to-expire"></a>如果我的訂閱即將到期，我有哪些選項？

當訂閱處於使用中狀態時，您和您的使用者可以一般存取您的資料，例如電子郵件和 OneDrive 商務和 Office 應用程式等服務。 作為系統管理員，當訂閱接近其到期日時，您會透過電子郵件和系統管理中心接收一系列的通知。
  
在訂閱實際達到其到期日之前，您有幾個選項：

::: moniker range="o365-worldwide"
  
- **啟用定期計費訂閱。**

  - 如果**定期計費**已開啟，您不需要採取任何動作。 您的訂閱將會自動計費，您會根據您目前的付款頻率，向您收取額外一年或一個月的費用。 如果您因任何原因而關閉了**週期性的帳單**，您可以永遠[開啟定期計費](renew-your-subscription.md)。

  - 如果您使用預付卡購買 Office 365 商務版，您可以為訂閱[開啟定期計費](renew-your-subscription.md)。

  - 如果您是具有預付一年期的大量授權客戶，請與您的合作夥伴聯繫以購買新的產品金鑰。 您會透過電子郵件接收指示，以在[大量授權服務中心](https://go.microsoft.com/fwlink/p/?LinkID=282016)啟用金鑰。 若要瞭解如何尋找新的合作夥伴或您已在過去使用過的合作夥伴，請參閱[尋找您的合作夥伴或轉銷商](../../admin/manage/find-your-partner-or-reseller.md)。

  - 如果您有 Office 365 業務，請參閱[管理您訂閱的週期性帳單](renew-your-subscription.md)。

- **讓訂閱到期。**

  - 如果您是以信用卡或發票付款，而您不想繼續訂閱，請關閉[定期帳單](renew-your-subscription.md)。 您的訂閱會在到期日到期，而且您可以略過所有相關的電子郵件通知。

  - 如果您是已開啟的大量授權客戶與合作夥伴合作，您可以不採取任何動作，讓訂閱到期。

  - 如果您是 Office 365 Small Business Premium 客戶，且您預付 Office 365 並以產品金鑰加以啟用，您可以透過不需採取任何動作，讓訂閱到期。

- **在訂閱到期之前取消。** 如需詳細資訊，請參閱[Cancel a 訂閱](cancel-your-subscription.md)。
  
::: moniker-end

::: moniker range="o365-germany"
  
- **管理訂閱的週期性帳單。**

  - 如果**定期計費**已開啟，您不需要採取任何動作。 您的訂閱將會自動計費，您會根據您目前的付款頻率，向您收取額外一年或一個月的費用。 如果您因任何原因而關閉了**週期性的帳單**，您可以永遠[開啟定期計費](renew-your-subscription.md)。

  - 如果您使用預付卡購買 Office 365 商務版，您可以為訂閱[開啟定期計費](renew-your-subscription.md)。

  - 如果您是具有預付一年期的大量授權客戶，請與您的合作夥伴聯繫以購買新的產品金鑰。 您會透過電子郵件接收指示，以在[大量授權服務中心](https://go.microsoft.com/fwlink/p/?LinkID=282016)啟用金鑰。 若要瞭解如何尋找新的合作夥伴或您已在過去使用過的合作夥伴，請參閱[尋找您的合作夥伴或轉銷商](../../admin/manage/find-your-partner-or-reseller.md)。

  - 如果您有 Office 365 業務，請參閱[更新您的訂閱](renew-your-subscription.md)。

- **讓訂閱到期。**

  - 如果您是以信用卡或發票付款，而您不想繼續訂閱，請關閉[定期帳單](renew-your-subscription.md)。 您的訂閱會在到期日到期，而且您可以略過所有相關的電子郵件通知。

  - 如果您是已開啟的大量授權客戶與合作夥伴合作，您可以不採取任何動作，讓訂閱到期。

  - 如果您是 Office 365 Small Business Premium 客戶，且您預付 Office 365 並以產品金鑰加以啟用，您可以透過不需採取任何動作，讓訂閱到期。

- **在訂閱到期之前取消。** 如需詳細資訊，請參閱[Cancel a 訂閱](cancel-your-subscription.md)。
  
::: moniker-end

::: moniker range="o365-21vianet"
  
- **更新訂閱。** 如果**定期計費**已開啟，您不需要採取任何動作。 您的訂閱將會自動計費，您會根據您目前的付款頻率，向您收取額外一年或一個月的費用。 如果您因任何原因而關閉了**週期性的帳單**，您可以永遠[開啟定期計費](renew-your-subscription.md)。

- **讓訂閱到期。** 如果您是以信用卡或發票付款，而您不想繼續訂閱，請關閉[定期帳單](renew-your-subscription.md)。 您的訂閱會在到期日到期，而且您可以略過所有相關的電子郵件通知。

- **在訂閱到期之前取消。** 如需詳細資訊，請參閱[Cancel a 訂閱](cancel-your-subscription.md)。

::: moniker-end

## <a name="what-happens-after-my-subscription-expires"></a>訂閱到期後會發生什麼情況？
如果您要讓訂閱到期，它會經歷多個狀態，最後刪除。 這可讓您以系統管理員、重新開機時間，如果您想要繼續服務，或是在您決定不再需要訂閱時，再備份您的資料。
  
以下是訂閱處於每個狀態時您可以預期的結果。
  
### <a name="state-expired"></a>狀態：已到期
  
::: moniker range="o365-worldwide"

 **預期的專案：** 到期狀態會持續30天的大部分訂閱，包括透過[Microsoft Open](https://go.microsoft.com/fwlink/p/?LinkID=613298)購買的訂閱，在大部分的國家和地區。 針對大量授權產品，除了 Microsoft Open 之外，到期狀態會持續90天。

::: moniker-end

::: moniker range="o365-germany"

 **預期的專案：** 到期狀態會持續30天的大部分訂閱，包括透過[Microsoft Open](https://go.microsoft.com/fwlink/p/?LinkID=613298)購買的訂閱，在大部分的國家和地區。 針對大量授權產品，除了 Microsoft Open 之外，到期狀態會持續90天。

::: moniker-end

::: moniker range="o365-21vianet"

 **預期的專案：** 在大部分的國家和地區中，大部分訂閱的到期狀態為30天。

::: moniker-end

在此狀態下，使用者可以正常存取 Office 365 入口網站、Office 應用程式，以及電子郵件和 SharePoint 線上等服務。
  
做為系統管理員，您仍然可以存取系統管理中心，但無法將授權指派給使用者。 全域或計費系統管理員可以[重新開機訂閱](reactivate-your-subscription.md)，並繼續使用 Office 365。 如果您未重新啟用，請務必[備份您的資料](back-up-data-before-switching-plans.md)。
  
### <a name="state-disabled"></a>狀態：已停用
  
::: moniker range="o365-worldwide"

 **預期的專案：** 如果您未在已過期的狀態下重新啟用您的訂閱，它會進入停用狀態，在大部分的國家和地區中，會持續為大多數訂閱的90天。 若為大量授權產品，停用狀態會持續30天。

::: moniker-end

::: moniker range="o365-germany"

 **預期的專案：** 如果您未在已過期的狀態下重新啟用您的訂閱，它會進入停用狀態，在大部分的國家和地區中，會持續為大多數訂閱的90天。 若為大量授權產品，停用狀態會持續30天。

::: moniker-end

::: moniker range="o365-21vianet"

 **預期的專案：** 如果您未在已過期的狀態下重新啟用您的訂閱，它會進入停用狀態，在大部分的國家和地區中為大多數訂閱的90天。

::: moniker-end

::: moniker range="o365-worldwide"

在此狀態下，您的存取會大幅減少。 您的使用者無法登入，或存取諸如電子郵件或 SharePoint 線上的服務。 Office 應用程式最終會移到唯讀、精簡功能的模式，並顯示未[授權的產品通知](https://support.office.com/article/0d23d3c0-c19c-4b2f-9845-5344fedc4380.aspx)。 您仍可登入並進入系統管理中心，但無法將授權指派給使用者。 您的客戶資料（包括所有使用者資料、電子郵件及小組網站上的檔案）只供您和其他系統管理員使用。

::: moniker-end

以全域或計費管理員的身分，您可以[重新啟用訂閱](reactivate-your-subscription.md)，並繼續使用 Office 365，讓所有的客戶資料保持不變。 如果您選擇不重新啟用，請務必[備份您的資料](back-up-data-before-switching-plans.md)。

### <a name="state-deprovisioned"></a>狀態： Deprovisioned
  
 **預期的專案：** 如果您在寬限期或停用時未重新啟用您的訂閱，則訂閱是 deprovisioned。
  
系統管理員和使用者不再可以存取訂閱隨附的服務或 Office 應用程式。 所有客戶資料（從使用者資料到檔和電子郵件）都會永久刪除，而且無法以任何方式復原。
  
此時，您無法重新啟用訂閱。 不過，以全域或計費系統管理員的身分，您仍然可以存取系統管理中心，以管理其他訂閱，或購買新的訂閱以滿足您的業務需求。
  
> [!NOTE]
> 新增已 deprovisioned 的相同類型的訂閱，不會還原與 deprovisioned 訂閱相關聯的資料。

### <a name="what-happens-when-my-trial-ends"></a>我的試用版結束時會發生什麼情況？

當您的試用版結束時，您將無法繼續免費使用 Office 365。 您有幾個選項：

::: moniker range="o365-worldwide"
- **購買 Office 365。** 當您的試用版到期時，它會移至寬限期，為您提供另外30天（大多數國家和地區的實驗）以購買 Office 365。 若要瞭解如何將您的試用版轉換為付費訂閱，請參閱[購買您的商務用 Office 365 試用版](../buy-a-subscription-from-your-free-trial.md)。

::: moniker-end

::: moniker range="o365-germany"
- **購買 Office 365。** 當您的試用版到期時，它會移至寬限期，為您提供另外30天（大多數國家和地區的實驗）以購買 Office 365。 若要瞭解如何將您的試用版轉換為付費訂閱，請參閱[購買您的商務用 Office 365 試用版](../buy-a-subscription-from-your-free-trial.md)。

::: moniker-end

::: moniker range="o365-21vianet"
- **購買 Office 365。** 當您的試用版到期時，它會移至寬限期，為您提供另外30天（大多數國家和地區的實驗）以購買 Office 365。 若要瞭解如何將您的試用版轉換為付費訂閱，請參閱[購買或嘗試使用世紀運作之 Office 365 的訂閱](../../admin/services-in-china/buy-or-try-subscriptions.md)。

::: moniker-end

- **請擴充您的試用版。** 需要更多時間來評估 Office 365？ 在某些情況下，您可能可以[擴充試用版](../extend-your-trial.md)。

- **取消試用期或讓其到期。** 如果您決定不購買 Office 365，您可以讓您的試用版到期或[取消](cancel-your-subscription.md)。 請務必備份您要保留的任何資料。 30天的寬限期之後不久，您的試用帳戶資訊和資料就會永久清除。

## <a name="what-happens-if-i-cancel-a-subscription"></a>如果我取消訂閱，會發生什麼情況？

如果您在其期限結束日期之前取消訂閱，該訂閱就會跳過到期狀態，並且直接移到停用的狀態，在大部分的國家和地區中為大多數訂閱的90天。 建議您先[備份資料](back-up-data-before-switching-plans.md)，然後再取消，但作為系統管理員，您仍然可以存取和備份您組織的資料，當其處於停用狀態時。 您所留下的任何客戶資料在 90 天後可能會遭到刪除，並且會在取消後的 180 天內全部刪除。
  
當您取消訂閱時，以下是您和您的使用者所期望的功能。
  
- 系統**管理存取**管理員仍可登入並存取系統管理中心，並視需要購買其他訂閱。 若您是全球或計費系統管理員，您可以在90天內重新啟用所有資料都完好無損[的訂閱](reactivate-your-subscription.md)。

- **使用者存取**您的使用者將無法使用 OneDrive 商務版服務，或存取客戶資料（例如，小組網站上的電子郵件或檔）。 Word 和 Excel 等 Office 應用程式最後都會進入唯讀、精簡功能模式，並顯示[未授權產品通知](https://support.office.com/article/0d23d3c0-c19c-4b2f-9845-5344fedc4380.aspx)。

若要瞭解如何取消，請參閱[取消您的訂閱](cancel-your-subscription.md)。
  
> [!IMPORTANT]
> 如果您想要在一般停用期間刪除訂閱資料，您可以要求快速解除準備。 當您要求快速撤銷時，您的訂閱資料會在取消後的 3 天內刪除。 若要使用加速解除[支援，請致電支援](../../admin/contact-support-for-business-products.md)。

> [!NOTE]
> 此頁面上的資訊受限於[Microsoft 原則免責聲明和變更通知](https://go.microsoft.com/fwlink/p/?LinkId=613651)。 定期回到此網站以檢查任何變更。
