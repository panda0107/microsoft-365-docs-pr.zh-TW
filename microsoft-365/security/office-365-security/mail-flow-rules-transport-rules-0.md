---
title: Exchange Online Protection 中的郵件流程規則 (傳輸規則)
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9c2cf227-eff7-48ef-87fb-487186e47363
description: 您可以使用郵件流程規則 (傳輸規則)，找出經過 Office 365 組織的郵件並採取相應動作。
ms.openlocfilehash: 604e2c7cb0b2cc34021e6708ae9f08769e8e6e91
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "39970339"
---
# <a name="mail-flow-rules-transport-rules-in-exchange-online-protection"></a><span data-ttu-id="7c444-103">Exchange Online Protection 中的郵件流程規則 (傳輸規則)</span><span class="sxs-lookup"><span data-stu-id="7c444-103">Mail flow rules (transport rules) in Exchange Online Protection</span></span>

<span data-ttu-id="7c444-p101">您可以使用郵件流程規則 (也稱為傳輸規則)，找出經過 Office 365 組織的郵件並採取相應動作。郵件流程規則類似於 Outlook 和 網頁型 Outlook 中可用的收件匣規則。主要差異是郵件流程規則會在郵件傳輸期間採取動作，而不是在郵件傳遞至信箱之後。郵件流程規則包含一組更豐富的條件、例外狀況和行動，可讓您靈活地實作許多種郵件原則。</span><span class="sxs-lookup"><span data-stu-id="7c444-p101">You can use mail flow rules (also known as transport rules) to identify and take action on messages that flow through your Office 365 organization. Mail flow rules are similar to the Inbox rules that are available in Outlook and Outlook on the web. The main difference is mail flow rules take action on messages while they're in transit, and not after the message is delivered to the mailbox. Mail flow rules contain a richer set of conditions, exceptions, and actions, which provides you with the flexibility to implement many types of messaging policies.</span></span>

<span data-ttu-id="7c444-108">本文說明郵件流程規則的元件和它們的運作方式。</span><span class="sxs-lookup"><span data-stu-id="7c444-108">This article explains the components of mail flow rules, and how they work.</span></span>

<span data-ttu-id="7c444-109">如需建立、複製和管理郵件流程規則的步驟，請參閱 [管理 Exchange Online 中的郵件流程規則](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) (部分內容為機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="7c444-109">For steps to create, copy, and manage mail flow rules, see [Manage mail flow rules in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules).</span></span> <span data-ttu-id="7c444-110">針對每個規則，您可以選擇強制執行規則、測試規則，或測試規則並通知寄件者。</span><span class="sxs-lookup"><span data-stu-id="7c444-110">For each rule, you have the option of enforcing it, testing it, or testing it and notifying the sender.</span></span> <span data-ttu-id="7c444-111">若要深入了解測試選項，請參閱[測試郵件流程規則](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/test-mail-flow-rules)和 [Exchange Online 中的原則提示](https://docs.microsoft.com/exchange/security-and-compliance/data-loss-prevention/policy-tips) (部分內容為機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="7c444-111">To learn more about the testing options, see [Test mail flow rules](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/test-mail-flow-rules) and [Policy Tips in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/data-loss-prevention/policy-tips).</span></span>

<span data-ttu-id="7c444-112">如需符合郵件流程規則之訊息的摘要和詳細報告，請參閱 [使用 Office 365 的郵件保護報告以檢視有關惡意程式碼、垃圾郵件和規則偵測的資訊](https://docs.microsoft.com/exchange/monitoring/use-mail-protection-reports)。</span><span class="sxs-lookup"><span data-stu-id="7c444-112">For summary and detail reports about messages that matched mail flow rules, see [Use mail protection reports in Office 365 to view data about malware, spam, and rule detections](https://docs.microsoft.com/exchange/monitoring/use-mail-protection-reports).</span></span>

<span data-ttu-id="7c444-113">若要使用郵件流程規則實作特定的訊息原則，請參閱下列主題︰</span><span class="sxs-lookup"><span data-stu-id="7c444-113">To implement specific messaging policies by using mail flow rules, see these topics:</span></span>

- [<span data-ttu-id="7c444-114">使用郵件流程規則來檢查 Exchange Online 中的郵件附件</span><span class="sxs-lookup"><span data-stu-id="7c444-114">Use mail flow rules to inspect message attachments in Exchange Online</span></span>](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments)

- [<span data-ttu-id="7c444-115">設定 Office 365 企業版中的加密</span><span class="sxs-lookup"><span data-stu-id="7c444-115">Set up encryption in Office 365 Enterprise</span></span>](../../compliance/set-up-encryption.md)

- <span data-ttu-id="7c444-116">[Exchange Online 中的全組織郵件免責聲明、簽名、頁尾或頁首](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/disclaimers-signatures-footers-or-headers) (部分內容為機器翻譯)</span><span class="sxs-lookup"><span data-stu-id="7c444-116">[](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/disclaimers-signatures-footers-or-headers)Organization-wide disclaimers, signatures, footers, or headers in Exchange 2016</span></span>

- [<span data-ttu-id="7c444-117">使用郵件流程規則在郵件中設定垃圾郵件信賴等級 (SCL)</span><span class="sxs-lookup"><span data-stu-id="7c444-117">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)

- [<span data-ttu-id="7c444-118">在 Office 365 中建立封鎖寄件者清單</span><span class="sxs-lookup"><span data-stu-id="7c444-118">Create organization-wide safe sender or blocked sender lists in Office 365</span></span>](create-block-sender-lists-in-office-365.md)

- [<span data-ttu-id="7c444-119">透過 Exchange Online Protection 中的檔案附件封鎖功能來降低惡意軟體威脅</span><span class="sxs-lookup"><span data-stu-id="7c444-119">Reducing malware threats through file attachment blocking in Exchange Online Protection</span></span>](reducing-malware-threats-through-file-attachment-blocking-in-exchange-online-pro.md)

- [<span data-ttu-id="7c444-120">定義 Office 365 中加密或解密電子郵件訊息的規則</span><span class="sxs-lookup"><span data-stu-id="7c444-120">Define mail flow rules to encrypt email messages in Office 365</span></span>](https://docs.microsoft.com/microsoft-365/compliance/define-mail-flow-rules-to-encrypt-email)

<span data-ttu-id="7c444-121">下列視訊提供在 Exchange Online Protection 中設定郵件流程規則的示範。</span><span class="sxs-lookup"><span data-stu-id="7c444-121">The following video provides a demonstration of setting up mail flow rules in Exchange Online Protection.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/7cdcd2cb-9382-4065-98e1-81257b32a189?autoplay=false]

## <a name="mail-flow-rule-components"></a><span data-ttu-id="7c444-122">郵件流程規則元件</span><span class="sxs-lookup"><span data-stu-id="7c444-122">Mail flow rule components</span></span>

<span data-ttu-id="7c444-123">郵件流程規則是由條件、例外狀況、動作和屬性所組成︰</span><span class="sxs-lookup"><span data-stu-id="7c444-123">A mail flow rule is made of conditions, exceptions, actions, and properties:</span></span>

- <span data-ttu-id="7c444-124">**條件**：識別您要套用動作的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-124">**Conditions** Identify the messages that you want to apply the actions to.</span></span> <span data-ttu-id="7c444-125">有些條件會檢查郵件標頭欄位 (例如 [收件者]、[寄件者] 或 [副本] 欄位)。</span><span class="sxs-lookup"><span data-stu-id="7c444-125">Some conditions examine message header fields (for example, the To, From, or Cc fields).</span></span> <span data-ttu-id="7c444-126">有些條件則會檢查郵件屬性 (例如郵件主旨、內文、附件、郵件大小或郵件分類)。</span><span class="sxs-lookup"><span data-stu-id="7c444-126">Other conditions examine message properties (for example, the message subject, body, attachments, message size, or message classification).</span></span> <span data-ttu-id="7c444-127">在使用大部分的條件時，您都必須指定比較運算子 (例如等於、不等於或包含) 以及要比對的值。</span><span class="sxs-lookup"><span data-stu-id="7c444-127">Most conditions require you to specify a comparison operator (for example, equals, doesn't equal, or contains) and a value to match.</span></span> <span data-ttu-id="7c444-128">如果沒有條件或例外狀況，則規則會套用至所有郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-128">If there are no conditions or exceptions, the rule is applied to all messages.</span></span>

<span data-ttu-id="7c444-129">如需 Exchange Online Protection 中郵件流程規則條件的相關資訊，請參閱 [Exchange Online 中的郵件流程規則條件和例外狀況 (述詞)](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions) (部分內容為機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="7c444-129">For more information about mail flow rule conditions in exExchangeOnline, see Mail flow rule conditions and exceptions (predicates) in Exchange Online.</span></span>

- <span data-ttu-id="7c444-130">**例外狀況**：選擇性地識別不應該套用動作的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-130">**Exceptions** Optionally identify the messages that the actions shouldn't apply to.</span></span> <span data-ttu-id="7c444-131">可在條件中使用的訊息識別碼也可用於例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7c444-131">The same message identifiers that are available in conditions are also available in exceptions.</span></span> <span data-ttu-id="7c444-132">例外狀況可覆寫條件並防止規則動作套用到郵件，即使郵件符合所有設定的條件也是如此。</span><span class="sxs-lookup"><span data-stu-id="7c444-132">Exceptions override conditions and prevent the rule actions from being applied to a message, even if the message matches all of the configured conditions.</span></span>

- <span data-ttu-id="7c444-133">**動作**：指定對於符合規則中的條件，但不符合任何例外狀況的郵件，所應採取的動作。</span><span class="sxs-lookup"><span data-stu-id="7c444-133">**Actions** Specify what to do to messages that match the conditions in the rule, and don't match any of the exceptions.</span></span> <span data-ttu-id="7c444-134">有許多動作可用，例如，拒絕、刪除或重新導向郵件、新增其他收件者、在郵件主旨中新增前置詞，或是將免責聲明插入郵件內文。</span><span class="sxs-lookup"><span data-stu-id="7c444-134">There are many actions available, such as rejecting, deleting, or redirecting messages, adding additional recipients, adding prefixes in the message subject, or inserting disclaimers in the message body.</span></span>

<span data-ttu-id="7c444-135">如需 Exchange Online Protection 中所提供郵件流程規則動作的相關資訊，請參閱 [Exchange Online 中的郵件流程規則動作](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions) (部分內容為機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="7c444-135">For more information about mail flow rule actions that are available in exExchangeOnline, see Mail flow rule actions in Exchange Online.</span></span>

- <span data-ttu-id="7c444-136">**屬性**：指定其他不是條件、例外狀況或動作的規則設定。</span><span class="sxs-lookup"><span data-stu-id="7c444-136">**Properties** Specify other rules settings that aren't conditions, exceptions or actions.</span></span> <span data-ttu-id="7c444-137">例如，何時應套用規則、是否強制執行或測試規則，以及規則作用中的時間週期。</span><span class="sxs-lookup"><span data-stu-id="7c444-137">For example, when the rule should be applied, whether to enforce or test the rule, and the time period when the rule is active.</span></span>

  <span data-ttu-id="7c444-138">如需詳細資訊，請參閱本主題中的[郵件流程規則屬性](#mail-flow-rule-properties)一節。</span><span class="sxs-lookup"><span data-stu-id="7c444-138">For more information, see the [Mail flow rule properties](#mail-flow-rule-properties) section in this topic.</span></span>

### <a name="multiple-conditions-exceptions-and-actions"></a><span data-ttu-id="7c444-139">多個條件、例外狀況和動作</span><span class="sxs-lookup"><span data-stu-id="7c444-139">Multiple conditions, exceptions, and actions</span></span>

<span data-ttu-id="7c444-140">下表顯示規則中如何處理多個條件、條件值、例外狀況和動作。</span><span class="sxs-lookup"><span data-stu-id="7c444-140">The following table shows how multiple conditions, condition values, exceptions, and actions are handled in a rule.</span></span>

|<span data-ttu-id="7c444-141">**元件**</span><span class="sxs-lookup"><span data-stu-id="7c444-141">**Component**</span></span>|<span data-ttu-id="7c444-142">**邏輯**</span><span class="sxs-lookup"><span data-stu-id="7c444-142">**Logic**</span></span>|<span data-ttu-id="7c444-143">**Comments**</span><span class="sxs-lookup"><span data-stu-id="7c444-143">**Comments**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7c444-144">多個條件</span><span class="sxs-lookup"><span data-stu-id="7c444-144">Multiple conditions</span></span>|<span data-ttu-id="7c444-145">AND</span><span class="sxs-lookup"><span data-stu-id="7c444-145">AND</span></span>|<span data-ttu-id="7c444-p107">郵件必須符合規則中的所有條件。如果您需要符合一個條件或另一個條件，請對每一個條件使用不同的規則。例如，若要將相同的免責聲明新增至附件和內容包含特定文字的郵件，請為每一個條件建立一個規則。在 EAC 中，您可以輕易地複製規則。</span><span class="sxs-lookup"><span data-stu-id="7c444-p107">A message must match all the conditions in the rule. If you need to match one condition or another, use separate rules for each condition. For example, if you want to add the same disclaimer to messages with attachments and messages that contain specific text, create one rule for each condition. In the EAC, you can easily copy a rule.</span></span>|
|<span data-ttu-id="7c444-150">具有多個值的一個條件</span><span class="sxs-lookup"><span data-stu-id="7c444-150">One condition with multiple values</span></span>|<span data-ttu-id="7c444-151">或</span><span class="sxs-lookup"><span data-stu-id="7c444-151">OR</span></span>|<span data-ttu-id="7c444-p108">有些條件允許您指定多個值。郵件必須符合任何一個 (而非全部) 指定的值。例如，如果電子郵件的主旨為股票價格資訊，而 **[主旨包含任何這些字詞]** 條件設定為符合 Contoso 或 股票這些字，則此電子郵件滿足該條件，因為主旨至少包含其中一個指定的值。  </span><span class="sxs-lookup"><span data-stu-id="7c444-p108">Some conditions allow you to specify more than one value. The message must match any one (not all) of the specified values. For example, if an email message has the subject Stock price information, and the **The subject includes any of these words** condition is configured to match the words Contoso or stock, the condition is satisfied because the subject contains at least one of the specified values.</span></span>|
|<span data-ttu-id="7c444-155">多個例外狀況</span><span class="sxs-lookup"><span data-stu-id="7c444-155">Multiple exceptions</span></span>|<span data-ttu-id="7c444-156">OR</span><span class="sxs-lookup"><span data-stu-id="7c444-156">OR</span></span>|<span data-ttu-id="7c444-p109">如果郵件符合任何例外狀況，則動作不會套用到郵件。郵件不必符合所有例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7c444-p109">If a message matches any one of the exceptions, the actions are not applied to the message. The message doesn't have to match all the exceptions.</span></span>|
|<span data-ttu-id="7c444-159">多個動作</span><span class="sxs-lookup"><span data-stu-id="7c444-159">Multiple actions</span></span>|<span data-ttu-id="7c444-160">AND</span><span class="sxs-lookup"><span data-stu-id="7c444-160">AND</span></span>|<span data-ttu-id="7c444-p110">符合規則條件的郵件可取得規則中指定的所有動作。例如，如果選取 [在郵件主旨前面加上]\*\*\*\* 和 [新增收件者到 [密件副本] 方塊]\*\*\*\* 動作，則兩個動作都會套用至郵件。 </span><span class="sxs-lookup"><span data-stu-id="7c444-p110">Messages that match a rule's conditions get all the actions that are specified in the rule. For example, if the actions **Prepend the subject of the message with** and **Add recipients to the Bcc box** are selected, both actions are applied to the message. </span></span><br/><br/> <span data-ttu-id="7c444-p111">請記住，某些動作 (例如，**[刪除郵件而不通知任何人]** 動作) 會阻止後續規則套用至郵件。其他動作 (例如 **[轉寄郵件]**) 則不允許額外的動作。</span><span class="sxs-lookup"><span data-stu-id="7c444-p111">Keep in mind that some actions, such as the **Delete the message without notifying anyone** action, prevent subsequent rules from being applied to a message. Other actions such as **Forward the message** do not allow additional actions. </span></span><br/><br/> <span data-ttu-id="7c444-165">您也可以在規則上設定動作，以便在套用該規則時，不要將後續的規則套件到郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-165">You can also set an action on a rule so that when that rule is applied, subsequent rules are not applied to the message.</span></span>|

### <a name="mail-flow-rule-properties"></a><span data-ttu-id="7c444-166">郵件流程規則屬性</span><span class="sxs-lookup"><span data-stu-id="7c444-166">Mail flow rule properties</span></span>

<span data-ttu-id="7c444-167">下表說明郵件流程規則中可用的規則屬性。</span><span class="sxs-lookup"><span data-stu-id="7c444-167">The following table describes the rule properties that are available in mail flow rules.</span></span>

|<span data-ttu-id="7c444-168">**EAC 中的屬性名稱**</span><span class="sxs-lookup"><span data-stu-id="7c444-168">**Property name in the EAC**</span></span>|<span data-ttu-id="7c444-169">**PowerShell 中的參數名稱**</span><span class="sxs-lookup"><span data-stu-id="7c444-169">**Parameter name in PowerShell**</span></span>|<span data-ttu-id="7c444-170">**描述**</span><span class="sxs-lookup"><span data-stu-id="7c444-170">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7c444-171">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="7c444-171">**Priority**</span></span>|<span data-ttu-id="7c444-172">_優先順序_</span><span class="sxs-lookup"><span data-stu-id="7c444-172">_Priority_</span></span>|<span data-ttu-id="7c444-p112">表示規則套用到郵件的順序。預設優先順序是以規則的建立時間為基礎 (較舊規則的優先順序高於較新的規則，而較高優先順序的規則會在較低優先順序的規則之前處理)。  </span><span class="sxs-lookup"><span data-stu-id="7c444-p112">Indicates the order that the rules are applied to messages. The default priority is based on when the rule is created (older rules have a higher priority than newer rules, and higher priority rules are processed before lower priority rules).</span></span> <br/><br/> <span data-ttu-id="7c444-p113">您可以在規則清單中向上或向下移動規則，以變更 EAC 中的規則優先順序。在 PowerShell 中，您可設定優先順序號碼 (0 為最高優先順序)。  </span><span class="sxs-lookup"><span data-stu-id="7c444-p113">You change the rule priority in the EAC by moving the rule up or down in the list of rules. In the PowerShell, you set the priority number (0 is the highest priority).</span></span> <br/><br/> <span data-ttu-id="7c444-177">例如，如果有一個規則是拒絕含有信用卡號碼的郵件，而另一個規則是需要核准，則您一定希望先執行拒絕規則，並停止套用其他規則。</span><span class="sxs-lookup"><span data-stu-id="7c444-177">For example, if you have one rule to reject messages that include a credit card number, and another one requiring approval, you'll want the reject rule to happen first, and stop applying other rules.</span></span>  |
|<span data-ttu-id="7c444-178">**Mode**</span><span class="sxs-lookup"><span data-stu-id="7c444-178">**Mode**</span></span>|<span data-ttu-id="7c444-179">_Mode_</span><span class="sxs-lookup"><span data-stu-id="7c444-179">_Mode_</span></span>|<span data-ttu-id="7c444-180">您可以指定是否要讓規則立即開始處理郵件，或您是否想要測試規則，而不影響郵件傳遞 (不論是否有資料遺失防護或 DLP 原則提示)。</span><span class="sxs-lookup"><span data-stu-id="7c444-180">You can specify whether you want the rule to start processing messages immediately, or whether you want to test rules without affecting the delivery of the message (with or without Data Loss Prevention or DLP Policy Tips).</span></span> <br/><br/> <span data-ttu-id="7c444-p114">原則提示可在 Outlook 或 網頁型 Outlook 中呈現簡短附註，以提供可能原則違規的相關資訊給正在建立郵件的人員。如需詳細資訊，請參閱 **Policy Tips** 。  </span><span class="sxs-lookup"><span data-stu-id="7c444-p114">Policy Tips present a brief note in Outlook or Outlook on the web that provides information about possible policy violations to the person that's creating the message. For more information, see **Policy Tips**. </span></span><br/><br/> <span data-ttu-id="7c444-183">如需模式的詳細資訊，請參閱 **測試郵件流程規則** (部分內容為機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="7c444-183">For more information about the modes, see **Test a transport rule**.</span></span>|
|<span data-ttu-id="7c444-184">**於下列日期啟用此規則**</span><span class="sxs-lookup"><span data-stu-id="7c444-184">**Activate this rule on the following date**</span></span> <br/><br/> <span data-ttu-id="7c444-185">**於下列日期停用此規則**</span><span class="sxs-lookup"><span data-stu-id="7c444-185">**Deactivate this rule on the following date**</span></span>|<span data-ttu-id="7c444-186">_ActivationDate_</span><span class="sxs-lookup"><span data-stu-id="7c444-186">_ActivationDate_</span></span> <br/> <span data-ttu-id="7c444-187">_ExpiryDate_</span><span class="sxs-lookup"><span data-stu-id="7c444-187">_ExpiryDate_</span></span>|<span data-ttu-id="7c444-188">指定規則的有效日期範圍。</span><span class="sxs-lookup"><span data-stu-id="7c444-188">Specifies the date range when the rule is active.</span></span>|
|<span data-ttu-id="7c444-189">已選取或未選取 [開啟]\*\*\*\* 核取方塊</span><span class="sxs-lookup"><span data-stu-id="7c444-189">**On** check box selected or not selected</span></span>|<span data-ttu-id="7c444-190">新規則：_New-TransportRule_ Cmdlet 上的 **Enabled** 參數。</span><span class="sxs-lookup"><span data-stu-id="7c444-190">New rules:  _Enabled_ parameter on the **New-TransportRule** cmdlet.</span></span> <br/><br/> <span data-ttu-id="7c444-191">現有規則：使用 **Enable-TransportRule** 或 **Disable-TransportRule** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c444-191">Existing rules: Use the **Enable-TransportRule** or **Disable-TransportRule** cmdlets.</span></span> <br/><br/> <span data-ttu-id="7c444-192">此值會顯示在規則的 **State** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="7c444-192">The value is displayed in the **State** property of the rule.</span></span>|<span data-ttu-id="7c444-p115">您可以建立已停用的規則，而在您準備進行測試時加以啟用。或者，您可以在不刪除規則的情況下進行停用，以保留設定。</span><span class="sxs-lookup"><span data-stu-id="7c444-p115">You can create a disabled rule, and enable it when you're ready to test it. Or, you can disable a rule without deleting it to preserve the settings.</span></span>|
|<span data-ttu-id="7c444-195">**如果無法完成規則處理時便順延郵件**</span><span class="sxs-lookup"><span data-stu-id="7c444-195">**Defer the message if rule processing doesn't complete**</span></span>|<span data-ttu-id="7c444-196">_RuleErrorAction_</span><span class="sxs-lookup"><span data-stu-id="7c444-196">_RuleErrorAction_</span></span>|<span data-ttu-id="7c444-p116">您可以指定如果無法完成規則處理時，應該如何處理郵件。預設會忽略此規則，但您可以選擇重新提交郵件進行處理。</span><span class="sxs-lookup"><span data-stu-id="7c444-p116">You can specify how the message should be handled if the rule processing can't be completed. By default, the rule will be ignored, but you can choose to resubmit the message for processing.</span></span>|
|<span data-ttu-id="7c444-199">**符合郵件中的寄件者地址**</span><span class="sxs-lookup"><span data-stu-id="7c444-199">**Match sender address in message**</span></span>|<span data-ttu-id="7c444-200">_SenderAddressLocation_</span><span class="sxs-lookup"><span data-stu-id="7c444-200">_SenderAddressLocation_</span></span>|<span data-ttu-id="7c444-201">如果此規則使用可檢查寄件者電子郵件地址的條件或例外狀況，您可以查看郵件標頭、郵件信封或這兩者的值。</span><span class="sxs-lookup"><span data-stu-id="7c444-201">If the rule uses conditions or exceptions that examine the sender's email address, you can look for the value in the message header, the message envelope, or both.</span></span>|
|<span data-ttu-id="7c444-202">**停止處理其他規則**</span><span class="sxs-lookup"><span data-stu-id="7c444-202">**Stop processing more rules**</span></span>|<span data-ttu-id="7c444-203">_SenderAddressLocation_</span><span class="sxs-lookup"><span data-stu-id="7c444-203">_SenderAddressLocation_</span></span>|<span data-ttu-id="7c444-p117">這是適用於規則的動作，但它看起來像是 EAC 中的屬性。您可以選擇在規則處理郵件之後，停止將其他規則套用至郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-p117">This is an action for the rule, but it looks like a property in the EAC. You can choose to stop applying additional rules to a message after a rule processes a message.</span></span>|
|<span data-ttu-id="7c444-206">**Comments**</span><span class="sxs-lookup"><span data-stu-id="7c444-206">**Comments**</span></span>|<span data-ttu-id="7c444-207">_Comments_</span><span class="sxs-lookup"><span data-stu-id="7c444-207">_Comments_</span></span>|<span data-ttu-id="7c444-208">您可以輸入有關規則的描述性註解。</span><span class="sxs-lookup"><span data-stu-id="7c444-208">You can enter descriptive comments about the rule.</span></span>|

## <a name="how-mail-flow-rules-are-applied-to-messages"></a><span data-ttu-id="7c444-209">郵件流程規則套用至訊息的方式</span><span class="sxs-lookup"><span data-stu-id="7c444-209">How mail flow rules are applied to messages</span></span>

<span data-ttu-id="7c444-210">通過組織中的所有郵件都會根據組織已啟用的郵件流程規則來評估。</span><span class="sxs-lookup"><span data-stu-id="7c444-210">All messages that flow through your organization are evaluated against the enabled mail flow rules in your organization.</span></span> <span data-ttu-id="7c444-211">規則會依 EAC 的 **[郵件流程]** \> **[規則]** 頁面所列出的順序來處理，或根據 PowerShell中的 _Priority_ 參數值來處理。</span><span class="sxs-lookup"><span data-stu-id="7c444-211">Rules are processed in the order listed on the **Mail flow** \> **Rules** page in EAC, or based on the corresponding  _Priority_ parameter value in the PowerShell.</span></span>

<span data-ttu-id="7c444-p119">每個規則也提供選項可於符合規則時停止處理其他規則。對於符合多個郵件流程規則中條件的郵件而言，此設定很重要 (您想要將哪個規則套用到郵件？全部？僅只一個？）。</span><span class="sxs-lookup"><span data-stu-id="7c444-p119">Each rule also offers the option of stopping processing more rules when the rule is matched. This setting is important for messages that match the conditions in multiple mail flow rules (which rule do you want applied to the message? All? Just one?).</span></span>

### <a name="differences-in-processing-based-on-message-type"></a><span data-ttu-id="7c444-216">郵件類型引發的處理差異</span><span class="sxs-lookup"><span data-stu-id="7c444-216">Differences in processing based on message type</span></span>

<span data-ttu-id="7c444-p120">通過組織的郵件有幾種類型。下表顯示郵件流程規則可處理的郵件類型。</span><span class="sxs-lookup"><span data-stu-id="7c444-p120">There are several types of messages that pass through an organization. The following table shows which messages types can be processed by mail flow rules.</span></span>

****

|<span data-ttu-id="7c444-219">**郵件類型**</span><span class="sxs-lookup"><span data-stu-id="7c444-219">**Type of message**</span></span>|<span data-ttu-id="7c444-220">**可以套用規則嗎?**</span><span class="sxs-lookup"><span data-stu-id="7c444-220">**Can a rule be applied?**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c444-221">**一般郵件**：包含單一 RTF 格式 (RTF)、HTML 或純文字郵件內文的郵件，或包含一組多部分或替代郵件內文的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-221">**Regular messages** Messages that contain a single rich text format (RTF), HTML, or plain text message body or a multipart or alternative set of message bodies.</span></span>|<span data-ttu-id="7c444-222">是</span><span class="sxs-lookup"><span data-stu-id="7c444-222">Yes</span></span>|
|<span data-ttu-id="7c444-223">**Office 365 郵件加密**：Office 365 中 Office 365 郵件加密所加密的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-223">\*\*Office 365 Message Encryption \*\* Messages encrypted by Office 365 Message Encryption in Office 365.</span></span> <span data-ttu-id="7c444-224">如需詳細資訊，請參閱 [Office 365 加密](https://docs.microsoft.com/microsoft-365/compliance/encryption) (部分內容為機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="7c444-224">For more information, see [Encryption in Office 365](https://docs.microsoft.com/microsoft-365/compliance/encryption).</span></span>|<span data-ttu-id="7c444-225">規則永遠可以存取信封標頭，並根據可檢查這些標頭的條件來處理郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-225">Rules can always access envelope headers and process messages based on conditions that inspect those headers.</span></span> <br/><br/> <span data-ttu-id="7c444-226">如需可檢查或修改加密郵件內容的規則，您必須確認已啟用傳輸解密 (強制或選擇性；預設值是選擇性)。</span><span class="sxs-lookup"><span data-stu-id="7c444-226">For a rule to inspect or modify the contents of an encrypted message, you need to verify that transport decryption is enabled (Mandatory or Optional; the default is Optional).</span></span> <span data-ttu-id="7c444-227">如需詳細資訊，請參閱[定義 Office 365 中將電子郵件加密或解密的規則](https://docs.microsoft.com/microsoft-365/compliance/define-mail-flow-rules-to-encrypt-email) (部分內容為機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="7c444-227">For more information, see [Define rules to encrypt or decrypt email messages](https://docs.microsoft.com/microsoft-365/compliance/define-mail-flow-rules-to-encrypt-email).</span></span>|
|<span data-ttu-id="7c444-228">**S/MIME 加密的郵件**</span><span class="sxs-lookup"><span data-stu-id="7c444-228">**S/MIME encrypted messages**</span></span>|<span data-ttu-id="7c444-229">規則只可以存取信封標頭，並根據可檢查這些標頭的條件來處理郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-229">Rules can only access envelope headers and process messages based on conditions that inspect those headers.</span></span> <br/><br/> <span data-ttu-id="7c444-230">無法處理具有需要檢查郵件內容之條件的規則，或具有可以修改郵件內容之動作的規則。</span><span class="sxs-lookup"><span data-stu-id="7c444-230">Rules with conditions that require inspection of the message's content, or actions that modify the message's content can't be processed.</span></span>|
|<span data-ttu-id="7c444-231">**RMS 保護的訊息**：已套件 Active Directory Rights Management Services(AD RMS) 或 Azure 版權管理 (RMS) 原則的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-231">**RMS protected messages** Messages that had an Active Directory Rights Management Services (AD RMS) or Azure Rights Management (RMS) policy applied.</span></span>|<span data-ttu-id="7c444-232">規則永遠可以存取信封標頭，並根據可檢查這些標頭的條件來處理郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-232">Rules can always access envelope headers and process messages based on conditions that inspect those headers.</span></span> <br/><br/> <span data-ttu-id="7c444-233">如需可檢查或修改 RMS 保護之郵件內容的規則，您必須確認已啟用傳輸解密 (強制或選擇性；預設值是選擇性)。</span><span class="sxs-lookup"><span data-stu-id="7c444-233">For a rule to inspect or modify the contents of an RMS protected message, you need to verify that transport decryption is enabled (Mandatory or Optional; the default is Optional).</span></span>|
|<span data-ttu-id="7c444-234">**明文簽章的郵件**：已簽署但未加密的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-234">**Clear-signed messages** Messages that have been signed but not encrypted.</span></span>|<span data-ttu-id="7c444-235">是</span><span class="sxs-lookup"><span data-stu-id="7c444-235">Yes</span></span>|
|<span data-ttu-id="7c444-236">**UM 郵件**：由整合通訊服務建立或處理的郵件 (如語音信箱、傳真、未接來電通知)，以及使用 Microsoft Outlook 語音存取 建立或轉寄的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-236">**UM messages** Messages that are created or processed by the Unified Messaging service, such as voice mail, fax, missed call notifications, and messages created or forwarded by using Microsoft Outlook Voice Access.</span></span>|<span data-ttu-id="7c444-237">是</span><span class="sxs-lookup"><span data-stu-id="7c444-237">Yes</span></span>|
|<span data-ttu-id="7c444-238">**匿名郵件**：匿名寄件者所傳送的郵件。</span><span class="sxs-lookup"><span data-stu-id="7c444-238">**Anonymous messages** Messages sent by anonymous senders.</span></span>|<span data-ttu-id="7c444-239">是</span><span class="sxs-lookup"><span data-stu-id="7c444-239">Yes</span></span>|
|<span data-ttu-id="7c444-240">**讀取報告**：為了回應寄件者的索取讀信回條而產生的報告。</span><span class="sxs-lookup"><span data-stu-id="7c444-240">**Read reports** Reports that are generated in response to read receipt requests by senders.</span></span> <span data-ttu-id="7c444-241">讀取內含 `IPM.Note*.MdnRead` 或 `IPM.Note*.MdnNotRead` 之郵件類別的報告。</span><span class="sxs-lookup"><span data-stu-id="7c444-241">Read reports have a message class of  `IPM.Note*.MdnRead` or  `IPM.Note*.MdnNotRead`.</span></span>|<span data-ttu-id="7c444-242">是</span><span class="sxs-lookup"><span data-stu-id="7c444-242">Yes</span></span>|

## <a name="what-else-should-i-know"></a><span data-ttu-id="7c444-243">其他注意事項</span><span class="sxs-lookup"><span data-stu-id="7c444-243">What else should I know?</span></span>

- <span data-ttu-id="7c444-244">在 Exchange Online Protection 中，規則的 **版本**或 **RuleVersion** 屬性值並不重要。</span><span class="sxs-lookup"><span data-stu-id="7c444-244">The **Version** or **RuleVersion** property value for a rule isn't important in Exchange Online.</span></span>

- <span data-ttu-id="7c444-245">在建立或修改郵件流程規則之後，可能需要 30 分鐘，以將新規則或更新的規則套用至訊息。</span><span class="sxs-lookup"><span data-stu-id="7c444-245">After you create or modify a mail flow rule, it can take up to 30 minutes for the new or updated rule to be applied to messages.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="7c444-246">如需詳細資訊</span><span class="sxs-lookup"><span data-stu-id="7c444-246">For more information</span></span>

[<span data-ttu-id="7c444-247">使用郵件流程規則來檢查 Exchange Online 中的郵件附件</span><span class="sxs-lookup"><span data-stu-id="7c444-247">Use mail flow rules to inspect message attachments in Exchange Online</span></span>](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments)

[<span data-ttu-id="7c444-248">Office 365 中的電子郵件加密</span><span class="sxs-lookup"><span data-stu-id="7c444-248">Email encryption in Office 365</span></span>](https://docs.microsoft.com/office365/securitycompliance/email-encryption)

[<span data-ttu-id="7c444-249">日誌、傳輸和收件匣規則限制</span><span class="sxs-lookup"><span data-stu-id="7c444-249">Journal, transport, and inbox rule limits</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#journal-transport-and-inbox-rule-limits)