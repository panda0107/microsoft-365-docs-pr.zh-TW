---
title: Office 365 內送出的垃圾郵件保護
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
ms.collection:
- M365-security-compliance
description: 系統管理員可以深入瞭解 Office 365 和 Exchange Online Protection （EOP）如何防止客戶輸出垃圾郵件，以及在您需要傳送大宗郵件時要採取的動作。
ms.openlocfilehash: 99e764944335be923ee1918851d4072ea98d3a32
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895320"
---
# <a name="outbound-spam-protection-in-office-365"></a>Office 365 內送出的垃圾郵件保護

我們會認真管理輸出垃圾郵件，因為 Office 365 （Exchange Online 或獨立 Exchange Online Protection （EOP）不含 Exchange Online 信箱）是一項線上服務，許多客戶都使用共用資源集區。 一個 Office 365 客戶有意或無意地從其組織傳送垃圾郵件，可能會降低整個服務的信譽，並可能影響其他客戶的電子郵件傳遞。

本主題說明設計用來協助防止輸出垃圾郵件的控制項和通知，以及您在需要傳送大宗郵件時可以採取的動作。

## <a name="what-admins-can-do-to-control-outbound-spam"></a>管理員可控制輸出垃圾郵件的工作

- **使用內建通知**：當使用者超過傳送限制的[服務](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options)或[輸出垃圾郵件原則](configure-the-outbound-spam-policy.md)，而且限制傳送電子郵件時，會將名為「**使用者限制傳送電子郵件**的預設警示原則」傳送電子郵件通知給**TenantAdmins** （**全域管理員**）群組的成員。 若要設定接收這些通知的人員，請參閱[驗證受限使用者的警示設定](removing-user-from-restricted-users-portal-after-spam.md#verify-the-alert-settings-for-restricted-users)。 此外，已**超過名稱電子郵件傳送限制**的預設警示原則，以及**可疑的電子郵件傳送模式**，偵測到**TenantAdmins** （**全域系統管理員**）群組的成員傳送電子郵件通知。 如需有關警示原則的詳細資訊，請參閱[安全性與合規性中心中的警示原則](../../compliance/alert-policies.md)。

- **複習來自協力廠商電子郵件提供者的垃圾**郵件：許多電子郵件服務（如 Outlook.com、YAHOO 和 AOL）都會提供回應迴圈，在此情況下，如果服務中的任何使用者將 Office 365 中的電子郵件標記為垃圾郵件，則會將郵件打包並送回我們進行審閱。 若要深入瞭解 Outlook.com 的寄件者支援， <https://sendersupport.olc.protection.outlook.com/pm/services.aspx>請移至。

## <a name="how-eop-controls-outbound-spam"></a>EOP 如何控制輸出垃圾郵件

- **輸出電子郵件流量的隔離**：掃描透過服務傳送的每個輸出郵件是否有垃圾郵件。 如果將郵件決定為垃圾郵件，則會從名為「_高風險傳遞集_區」的次要、較著名的 IP 位址集區傳遞。 如需詳細資訊，請參閱[Office 365 中輸出郵件的高風險傳遞集](high-risk-delivery-pool-for-outbound-messages.md)區。

- **監控來源 IP 位址信譽**： Office 365 查詢各種協力廠商 ip 封鎖清單。 如果此清單上出現用於輸出電子郵件的任何 IP 位址，就會產生警示。 這樣一來，當垃圾郵件導致信譽降級時，我們就能快速地作出反應。 警示產生時，我們會提供內部檔，說明如何從封鎖清單中取得 IP 位址的移除（delisted）。

- **停用傳送太多垃圾郵件**<sup>\*</sup>的帳戶：即使我們將輸出的垃圾郵件分為高風險傳遞集區，我們也無法允許帳戶（通常為已遭破壞的帳戶）無限期傳送垃圾郵件。 我們會監控傳送垃圾郵件的帳戶，當郵件超過 undisclosed 限制時，系統會封鎖該帳戶傳送電子郵件。 個別使用者和整個承租人各有不同的臨界值。

- **停用傳送太高電子郵件的帳戶太快**<sup>\*</sup>：除了對標示為垃圾郵件的郵件限制以外，當郵件達到整體輸出郵件限制時，也有限制會封鎖帳戶，而不論輸出郵件中的垃圾郵件篩選是否正確。 已遭破壞的帳戶可能會傳送垃圾郵件篩選器錯過的零天（先前無法辨識的）垃圾郵件。 由於很難識別合法大宗郵件活動與垃圾郵件活動，因此這些限制可協助您降低任何可能的損毀。

<sup>\*</sup>我們不會通告確切的限制，因此垃圾郵件製造者無法在系統上玩遊戲，因此我們可以視需要增加或減少限制。 這類限制可讓平均的企業使用者超過平均的使用程度，而且可提供足夠低的程度，以協助包含垃圾郵件製造者造成的損毀。

## <a name="recommendations-for-customers-who-want-to-send-mass-mailings-through-eop"></a>希望透過 EOP 傳送大宗郵件之客戶的建議

在想要傳送大量電子郵件的客戶之間，您很難進行平衡，而不是使用不良的收件者購買做法，保護服務免受遭到攻破的帳戶和大量電子郵件寄件者。 在協力廠商 IP 封鎖清單上，Office 365 電子郵件來源登陸的成本，大於封鎖傳送太多電子郵件的使用者。

如[Exchange Online 服務描述](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)所述，使用 EOP 傳送大量電子郵件並不是支援使用服務，而且只允許以「最大努力」為基礎。 若客戶想要傳送大量電子郵件，建議您執行下列解決方案：

- **透過內部部署電子郵件伺服器傳送大量電子郵件**：這表示客戶將需要維護自己的電子郵件基礎結構以進行大宗郵件。

- **使用協力廠商大量電子郵件提供者**：您可以使用多個協力廠商大量電子郵件解決方案提供者來傳送大宗郵件。 這些公司的利益與客戶合作，以確保電子郵件傳送慣例良好的 vested。

郵件、行動裝置、惡意程式碼反濫用工作群組（MAAWG）會將其成員資格<https://www.maawg.org/about/roster>的名單發行于。 有幾個大量的電子郵件提供者在清單中，而且也稱為「負責的網際網路公民」。
