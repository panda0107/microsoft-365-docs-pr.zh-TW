---
title: 使用 Office 365 ATP 安全連結來設定自訂「不要重寫」URL 清單
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: article
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
ms.collection:
- M365-security-compliance
description: 當您設定您的 ATP 安全連結原則時，可以包括不要重寫的 URL 清單，讓組織中的某些人員造訪您清單中包含的網站。
ms.openlocfilehash: 1983e0ff2ea85092af483d4f7a563681a6441152
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2020
ms.locfileid: "42082205"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>使用 Office 365 ATP 安全連結來設定自訂「不要重寫」URL 清單

> [!IMPORTANT]
> 本文適用於擁有 [Office 365 進階威脅防護](office-365-atp.md)的企業客戶。 如果您是家用版使用者且正在尋找 Outlook 中安全連結的相關資訊，請參閱[進階 Outlook.com 安全性](https://support.office.com/article/882d2243-eab9-4545-a58a-b36fee4a46e2)。

有了 [Office 365 進階威脅防護](office-365-atp.md) (ATP)，貴組織可以擁有[自訂封鎖 URL](set-up-a-custom-blocked-urls-list-wtih-atp.md)，這樣一來，當使用者按一下電子郵件訊息中的網址 (URL) 或特定 Office 文件時，系統就不會阻止他們前往這些 URL。 貴組織還可以針對貴組織中的特定群組，擁有自訂「不要重寫」清單。 「不要重寫」清單可讓某些人員造訪 [Office 365 中的 ATP 安全連結](atp-safe-links.md)封鎖的 URL。

本文說明如何指定排除在 ATP 安全連結掃描以外的 URL 清單，以及要注意的一些重點。

## <a name="set-up-a-do-not-rewrite-list"></a>設定「不要重寫」清單

ATP 安全連結保護使用數個清單，包括貴組織的封鎖 URL 清單和例外的「不要重寫」清單。 如果您具有必要權限，則可以設定您的自訂「不要重寫」清單。 當您新增或編輯適用於貴組織中特定收件者的安全連結原則時，您可以這麼做。

若要編輯 (或定義) ATP 原則，您必須獲派適當的角色。 下表包括一些範例。 若要深入了解，請參閱 [Office 365 安全性與合規性中心中的權限](permissions-in-the-security-and-compliance-center.md)。

|角色  |指派位置/條件  |
|---------|---------|
|Office 365 全域系統管理員 |註冊購買 Office 365 的人會預設為為全域系統管理員。 (請參閱[關於 Office 365 系統管理員角色](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) (部分機器翻譯) 以深入了解。)         |
|安全性系統管理員 |Azure Active Directory 系統管理中心 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 組織管理 |Exchange 系統管理中心 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>或 <br>  PowerShell Cmdlet (請參閱 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell)) |

> [!TIP]
> 若要深入了解角色和權限，請參閱[Office 365 安全性 & 合規性中心的權限](permissions-in-the-security-and-compliance-center.md)。

### <a name="to-view-or-edit-a-custom-do-not-rewrite-urls-list"></a>若要檢視或編輯自訂「不要重寫」URL 清單

1. 移至 [https://protection.office.com](https://protection.office.com) 然後以您的公司或學校帳戶當入。

2. 在左側導覽中，選擇 [威脅管理]**** \> [原則]**** \> [安全連結]****。

3. 在 [適用於特定收件者的原則]**** 區段中，選擇 [新增]**** ([新增] 按鈕類似加號 (**+**) 以建立新原則。 (或者，您也可以編輯現有的原則。)<br/>![選擇 [新增] 以新增特定電子郵件收件者的安全連結原則](../../media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)

4. 為您的原則指定名稱和描述。

5. 在 [不要重寫下列 URL]**** 區段中，選取 [輸入有效的 URL]**** 方塊，輸入 URL，然後選擇加號 (+)。

6. 在 [套用至]**** 區段中，選擇 [收件者是以下的成員]****，然後選擇您想要包含在原則中的群組。 選擇 [新增]****，然後選擇 [確認]****。

7. 完成新增 URL 之後，在螢幕畫面右下角選擇 [儲存]****。

> [!NOTE]
> 請務必檢閱貴組織的自訂已封鎖 URL 清單。 請參閱[使用 ATP 安全連結來設定自訂的封鎖 URL 清單](set-up-a-custom-blocked-urls-list-wtih-atp.md)。

## <a name="important-points-to-keep-in-mind"></a>請注意重要要點

- 您在「不要重寫」清單中指定的任何 URL，都會針對您指定的收件者，從 ATP 安全連結掃描中排除。

- 如果您在「不要重寫」清單中已經有 URL 清單，請務必檢閱該清單，並視需要新增萬用字元。 例如，如果您的現有清單包含像是 `https://contoso.com/a` 的項目，而您想要在原則中包含類似 `https://contoso.com/a/b` 的子路徑，請在您的項目中新增萬用字元，使它看起來像是 `https://contoso.com/a/*`。

- 當您為 ATP 安全連結原則指定「不要重寫」清單時，最多可以包含三個萬用字元星號 (\*)。 使用萬用字元 (\*) 用來明確包含前置詞或子網域。 項目`contoso.com`不是相同`*.contoso.com/*`，因為`*.contoso.com/*`允許以瀏覽個子網域和路徑指定的網域中的人員。

下表列出您可以輸入的內容範例，以及這些項目的影響。

|**範例項目**|**功能**|
|:-----|:-----|
|`contoso.com`|讓收件者可以造訪 `https://contoso.com`，而不是子網域或路徑。|
|`*.contoso.com/*`|可讓收件者，請造訪網域、 子網域，以及路徑，例如： `https://www.contoso.com`、 `https://www.contoso.com`、 `https://maps.contoso.com`，或`https://www.contoso.com/a`。 <br/><br/> 這個項目是原本就是優於`*contoso.com*`，因為它不會像包含可能詐騙網站，`https://www.falsecontoso.com`或`https://www.false.contoso.completelyfalse.com`|
|`https://contoso.com/a`|讓收件者可以造訪像是 `https://contoso.com/a` 的網站，而不是像是 `https://contoso.com/a/b` 的子路徑。|
|`https://contoso.com/a/*`|讓收件者可以造訪像是 `https://contoso.com/a` 的網站，以及像是 `https://contoso.com/a/b` 的子路徑。|
