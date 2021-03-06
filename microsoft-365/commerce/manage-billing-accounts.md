---
title: 管理帳單帳戶
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
- commerce
ms.custom: ''
search.appverid:
- MET150
description: 深入瞭解記帳帳戶及管理方式。
ms.openlocfilehash: ce7b9d2a2cc35261c7e6e3f5547574ea9c49e658
ms.sourcegitcommit: 2859c82b30ae9cbd3a3e4bcdebd65f18444f1a9e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/18/2020
ms.locfileid: "42826264"
---
# <a name="manage-billing-accounts"></a>管理帳單帳戶

當您註冊以嘗試或購買 Microsoft 產品時，即會建立帳單帳戶。 您可以使用您的計費帳戶來管理帳戶設定、發票、支付方式及購買。 您可以存取多個帳單帳戶。 例如，您已直接註冊 Microsoft 365，或您可以存取組織的企業合約、Microsoft 產品 & 服務合約或 Microsoft 客戶合約。 針對上述每個案例，您會有個別的帳單帳戶。

Microsoft 365 admin center 目前支援下列類型的計費帳戶：

- Microsoft 線上服務方案：當您直接註冊 Microsoft 365 訂閱時，就會建立這種計費帳戶。
- Microsoft 產品 & 服務合約（MPSA）程式：當您的組織簽署 MPSA 大量授權合約以購買軟體和線上服務時，就會建立這種計費帳戶。
- Microsoft 客戶合約：當您的組織與 Microsoft 代表、授權的協力廠商或獨立購買合作時，即會建立這種計費帳戶。

「<a href="https://go.microsoft.com/fwlink/p/?linkid=2084771" target="_blank">帳單帳戶</a>」頁面可提供您的商務客戶與 Microsoft 的觀點。 根據預設，您的組織在直接購買或大量授權時，至少要有一個與合約相關聯的帳單帳戶。

## <a name="understand-billing-account-details"></a>瞭解帳單帳戶詳細資料

[**帳單帳戶**詳細資料] 頁面的頂端是您的帳戶設定檔，包含您組織的法律和稅務資訊。 您可以更新您的設定檔，以變更您的法律位址和電話號碼。 此帳戶是支付所購買產品的法律法人。

下表列出您在 [**帳單帳戶**詳細資料] 頁面中看到的重要字詞。

| 欄位名稱 | 描述 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 銷售位址 | 負責支付及識別發票上的法律法人。 除非您選擇在購買過程中提供替代的寄送位址，否則這裡提供的位址是用來判斷您的稅率。 如需詳細資訊，請參閱[稅務資訊](billing-and-payments/tax-information.md)。 |
| 段 | 可識別您組織之業務區段的唯讀欄位（商業性、教育、政府或非贏利）。 |
| 帳戶狀態 | 指定您的商務用 Microsoft 帳戶狀態的唯讀欄位。 |
| 納稅識別碼 | 如果您在美國境外，您必須提供加值稅或當地對等專案。 如需詳細資訊，請參閱[稅務資訊](billing-and-payments/tax-information.md)。 |
| 協定 | 在建立計費帳戶時（透過直接購買或大量授權安排），組織的簽署人會接受（或簽署）列出該帳戶的條款 & 條件的合約。 如果適用的話，此視圖會列出合約記錄。 如果您需要接受更新的字詞，就會顯示「**核准合約**」的連結。 |
| 計費設定檔 | 計費設定檔會定義發票的內容，例如誰接收帳單、帳單傳遞的方式、付款條款和 PO 號碼。 若要在組織中散佈帳單，您可以建立多個帳單設定檔，並在購買時識別適當的帳單設定檔。 如需計費設定檔的詳細資訊，以及如何使用它們為您的組織建立更靈活的帳單選項，請[管理帳單設定檔](billing-and-payments/manage-billing-profiles.md)。 |

> [!NOTE]
> 如果您想要變更已**售出**的名稱或位址，但沒有看到**編輯**連結，您必須[聯繫支援人員](https://docs.microsoft.com/office365/admin/contact-support-for-business-products)加以變更。 要求**銷售**變更名稱的要求會要求信用支票。 當您聯繫支援人員時，請準備好下列其中一份檔：
>
> - 外部宣告檔，指出公司名稱或公司結構中的任何變更
> - 政府簽發的檔或註冊信件
> - 列印本機公司的登錄
>
> 支援可協助您在名稱和位址變更時，只有客戶名稱變更，但實體仍保持不變。 提供的檔應明確指出實體的名稱已變更。 如果變更與客戶銷售部門或客戶關聯的分割或 "spinoff" 相關聯，請與您的 Microsoft 賣方聯繫。

## <a name="shipping-addresses"></a>送貨位址

本節會列出與您的帳單帳戶相關聯的運送位址。 當您進行購買時，您可以使用此位址來識別購買或使用購買的位置。 送貨位址是可編輯的。 您可以新增送貨位址或更新現有的位址。 此位址是用來決定購買的納稅率。

## <a name="understand-access-to-billing-accounts"></a>瞭解計費帳戶的存取權

您可以讓其他人透過角色和許可權，存取 Microsoft 365 系統管理中心內的帳單帳戶。 只有帳單帳戶擁有者可以授與帳單帳戶的存取權。 您可以將下列角色之一指派給使用者：

- **帳單帳戶擁有** &mdash;者可以指派許可權、編輯帳戶、簽署合約和 view accounts。
- **帳單帳戶參與者** &mdash;可以編輯帳戶、簽署協定和查看帳戶。
- **帳單帳戶讀者** &mdash;可以查看帳戶。

> [!Note]
> 計費帳戶角色只適用于帳單帳戶，不適用於其他 Microsoft 365 系統管理中心案例。

## <a name="related-articles"></a>相關文章

[稅務資訊](billing-and-payments/tax-information.md)

[管理帳單設定檔](billing-and-payments/manage-billing-profiles.md)