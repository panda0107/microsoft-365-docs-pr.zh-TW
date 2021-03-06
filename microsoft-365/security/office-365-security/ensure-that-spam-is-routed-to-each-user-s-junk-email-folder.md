---
title: 將 EOP 設定為混合式環境中的垃圾郵件
f1.keywords:
- NOCSH
ms.author: chrisda
author: MSFTTracyP
manager: chrisda
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: 系統管理員可以瞭解如何設定其內部部署 Exchange 環境，以將垃圾郵件路由傳送至內部部署使用者的垃圾郵件資料夾，如果他們在混合式環境中使用獨立 Exchange Online Protection （EOP）。
ms.openlocfilehash: 8a3887d1cc7390e75b7708d2167372e976923e01
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/21/2020
ms.locfileid: "42893715"
---
# <a name="configure-standalone-eop-to-deliver-spam-to-the-junk-email-folder-in-hybrid-environments"></a>設定獨立 EOP，將垃圾郵件傳遞至混合式環境中的 [垃圾郵件] 資料夾

> [!IMPORTANT]
> 本主題僅適用于混合式環境中的獨立 EOP 客戶。 本主題不適用於含 Exchange Online 信箱的 Office 365 客戶。

如果您是混合式環境中的獨立 Exchange Online Protection （EOP）客戶，您必須設定內部部署 Exchange 組織，以辨識及翻譯 EOP 的垃圾郵件篩選 verdicts，使內部部署信箱中的垃圾郵件規則可以將郵件移至 [垃圾郵件] 資料夾。

具體而言，您必須在內部部署 Exchange 組織中建立郵件流程規則（也稱為傳輸規則），條件是使用下列任何 EOP 反垃圾郵件標頭和值，以及設定垃圾郵件信賴等級的動作來尋找郵件。SCL）的郵件至6：

- `X-Forefront-Antispam-Report: SFV:SPM`（透過垃圾郵件篩選標示為垃圾郵件）

- `X-Forefront-Antispam-Report: SFV:SKS`（透過垃圾郵件篩選之前 EOP 中郵件流程規則標示為垃圾郵件的郵件）

- `X-Forefront-Antispam-Report: SFV:SKB`（由於寄件者的電子郵件地址或電子郵件網域位於 EOP 中，封鎖的寄件者清單或封鎖的網域清單中，以垃圾郵件篩選標示為垃圾郵件的郵件）

如需這些標頭值的詳細資訊，請參閱[反垃圾郵件郵件頭](anti-spam-message-headers.md)。

本主題說明如何建立郵件流程規則 Exchange 系統管理中心（EAC），以及內部部署 Exchange 組織中的 Exchange 管理命令介面（Exchange PowerShell）。

> [!TIP]
> 您可以在 EOP 中設定反垃圾郵件原則，以隔離 EOP 中的垃圾郵件，而不是將郵件傳遞至內部部署使用者的 [垃圾郵件] 資料夾。 如需詳細資訊，請參閱[在 Office 365 中設定反垃圾郵件原則](configure-your-spam-filter-policies.md)。

## <a name="what-do-you-need-to-know-before-you-begin"></a>開始之前有哪些須知？

- 您必須在內部部署 Exchange 環境中指派許可權，才能執行這些程式。 具體而言，您必須被指派**傳輸規則**角色，預設會指派給**組織管理**、**規範管理**及**記錄管理**角色。 如需詳細資訊，請參閱 [將成員新增至角色群組](https://docs.microsoft.com/Exchange/permissions/role-group-members?view=exchserver-2019#add-members-to-a-role-group)。

- 當郵件傳遞至內部部署 Exchange 組織中的 [垃圾郵件] 資料夾時，由下列設定的組合來控制：

  - Exchange 管理命令介面中[Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/organization/set-organizationconfig) Cmdlet 上的_SCLJunkThreshold_參數值。 預設值為4，表示 SCL 上限為5或以上，則應該會將郵件傳遞至使用者的 [垃圾郵件] 資料夾。

  - Exchange 管理命令介面中[Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) Cmdlet 上的_SCLJunkThreshold_參數值。 預設值為空白（$null），這表示使用組織設定。

  如需詳細資訊，請參閱[Exchange 垃圾郵件信賴等級（SCL）閾值](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/scl)。

  - 信箱上是否啟用垃圾郵件規則（ _enabled_參數值是在 Exchange 管理命令介面的[Set-MailboxJunkEmailConfiguration](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-mailboxjunkemailconfiguration)指令程式中 $true）。 這是垃圾郵件規則，它會在傳送後實際將郵件移至 [垃圾郵件] 資料夾。 依預設，會在信箱上啟用垃圾郵件規則。 如需詳細資訊，請參閱[設定信箱上的 Exchange 反垃圾郵件設定](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/configure-antispam-settings)。
  
- 若要在 Exchange 伺服器上開啟 EAC，請參閱 exchange [server 中的 exchange 系統管理中心](https://docs.microsoft.com/Exchange/architecture/client-access/exchange-admin-center)。 若要開啟 Exchange 管理命令介面， [https://docs.microsoft.com/powershell/exchange/exchange-server/open-the-exchange-management-shell](https://docs.microsoft.com/powershell/exchange/exchange-server/open-the-exchange-management-shell)請參閱。

- 如需內部部署 Exchange 中郵件流程規則的相關資訊，請參閱下列主題：

  - [Exchange Server 中的郵件流程規則](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rules)

  - [Exchange Server 中的郵件流程規則條件和例外狀況 (述詞)](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/conditions-and-exceptions)

  - [Exchange Server 中的郵件流程規則動作](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/actions)

## <a name="use-the-eac-to-create-mail-flow-rules-that-set-the-scl-of-eop-spam-messages"></a>使用 EAC 來建立郵件流程規則，以設定 EOP 垃圾郵件訊息的 SCL

1. 在 EAC 中，移至 [郵件流程]**** \> [規則]****。

2. 按一下 [**新增** ![新增](../../media/ITPro-EAC-AddIcon.png)圖示]，然後在出現的下拉式清單中選取 [**建立新的規則**]。

3. 在開啟的 [**新增規則**] 頁面中，設定下列設定：

   - **名稱**：輸入規則的唯一描述性名稱。 例如：

     - EOP SFV： SPM 至 SCL 6

     - EOP SFV： SKS 至 SCL 6

     - EOP SFV:SKB 至 SCL 6

   - 按一下 [**更多選項**]。

   - **在下列情況中套用此規則**： Select **message 標頭** \> **包含任何這些字**。

     在 [**輸入文字標頭包含**會出現的輸入文字句子] 中，執行下列步驟：

     - 按一下 [**輸入文字**]。 在出現的 [**指定標頭名稱**] 對話方塊中，輸入**X-Forefront-Antispam-Report** ，然後按一下 **[確定**]。

     - 按一下 [**輸入文字**]。 在出現的 [**指定字詞或片語**] 對話方塊中，輸入下列其中一個 EOP 的垃圾郵件頭值（**SFV： SPM**、 **SFV： SKS**或**SFV:SKB**），按一下](../../media/ITPro-EAC-AddIcon.png)[**新增** ![] [新增] 圖示，然後按一下 **[確定]**。

   - **請執行下列**動作：選取 [**修改郵件屬性** \> ]**設定垃圾郵件信賴等級（SCL）**。

     在 [**指定 SCL** ] 對話方塊中，選取 [ **6** （預設值為**5**）]。

   完成後，請按一下 [儲存]****。

針對餘下的 EOP 垃圾郵件判定值（**SFV： SPM**、 **SFV： SKS**或**SFV:SKB**）重複這些步驟。

## <a name="use-the-exchange-management-shell-to-create-mail-flow-rules-that-set-the-scl-of-eop-spam-messages"></a>使用 Exchange 管理命令介面來建立郵件流程規則，以設定 EOP 垃圾郵件訊息的 SCL

使用下列語法來建立三個郵件流程規則：

```Powershell
New-TransportRule -Name "<RuleName>" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "<EOPSpamFilteringVerdict>" -SetSCL 6
```

例如：

```Powershell
New-TransportRule -Name "EOP SFV:SPM to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
```

```Powershell
New-TransportRule -Name "EOP SFV:SKS to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
```

```Powershell
New-TransportRule -Name "EOP SFV:SKB to SCL 6" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
```

如需詳細的語法和參數資訊，請參閱 [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-transportrule)。

## <a name="how-do-you-know-this-worked"></a>如何知道這是否正常運作？

若要確認您是否已成功將獨立 EOP 設定為將垃圾郵件傳遞至混合式環境中的 [垃圾郵件] 資料夾，請執行下列任一步驟：

- 在 EAC 中，移至 [**郵件流程** \> **規則**]，選取規則，然後按一下 [**編輯** ![編輯](../../media/ITPro-EAC-EditIcon.png)圖示] 以驗證設定。

- 在 Exchange 管理命令介面中， \<將\> RuleName 取代為郵件流程規則的名稱，然後 rul 下列命令，以確認設定：

  ```powershell
  Get-TransportRule -Identity "<RuleName>" | Format-List
  ```

- 在**沒有掃描輸出郵件的**外部電子郵件系統中，請將未經授權的大量電子郵件（GTUBE）郵件的一般測試傳送至受影響的收件者，並確認郵件已傳遞至其 [垃圾郵件] 資料夾。 GTUBE 訊息類似用來測試惡意程式碼設定的《電腦防病毒調查（EICAR.TXT）」文字檔的歐洲研究院。

  若要傳送 GTUBE 訊息，請在電子郵件的本文中包含下列文字，但不含任何空格或分行符號：

  ```text
  XJS*C4JDBQADN1.NSBN3*2IDNEN*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL*C.34X
  ```
