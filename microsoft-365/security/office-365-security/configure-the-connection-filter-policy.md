---
title: 設定連線篩選原則、允許清單、封鎖清單
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/27/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
ms.collection:
- M365-security-compliance
description: 若要確定您信任的人所傳送的電子郵件並未遭到封鎖，可以使用連線篩選原則，對於您信任的 IP 位址建立允許清單 (也稱為安全寄件者清單)。 您也可以建立封鎖寄件者清單。
ms.openlocfilehash: d3151ab436c5d904897d518fa119d52a11db4850
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "39971831"
---
# <a name="configure-the-connection-filter-policy"></a><span data-ttu-id="9c03c-104">設定連線篩選原則</span><span class="sxs-lookup"><span data-stu-id="9c03c-104">Configure the connection filter policy</span></span>

<span data-ttu-id="9c03c-105">大多數的人都有信任的朋友和企業夥伴。</span><span class="sxs-lookup"><span data-stu-id="9c03c-105">Most of us have friends and business partners we trust.</span></span> <span data-ttu-id="9c03c-106">發現這些人寄送的電子郵件出現在垃圾郵件資料夾或甚至遭到垃圾郵件篩選器整個封鎖，會令人感覺不便。</span><span class="sxs-lookup"><span data-stu-id="9c03c-106">It can be frustrating to find email from them in your junk email folder, or even blocked entirely by a spam filter.</span></span> <span data-ttu-id="9c03c-107">如果您想要確定您信任的人所傳送的電子郵件並未遭到封鎖，可以使用連線篩選原則，對於您信任的 IP 位址建立允許清單 (也稱為安全寄件者清單)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-107">If you want to make sure that email sent from people you trust isn't blocked, you can use the connection filter policy to create an Allow list (or "safe sender list") of IP addresses that you trust.</span></span> <span data-ttu-id="9c03c-108">您也可以建立不想收到電子郵件的封鎖寄件者清單，其中列出一般來自已知濫發垃圾郵件者的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9c03c-108">You can also create a blocked senders list, which is a list of IP addresses, typically from known spammers, that you don't ever want to receive email messages from.</span></span>

- <span data-ttu-id="9c03c-109">當考慮[允許清單](create-safe-sender-lists-in-office-365.md)\*\* 時，請牢記連線篩選原則本身與篩選「允許的信任帳戶」\*\* 有關。</span><span class="sxs-lookup"><span data-stu-id="9c03c-109">When thinking about *[Allow lists](create-safe-sender-lists-in-office-365.md)*, keep in mind connection filter policies concern themselves with the *trusted accounts allowed* by the filter.</span></span> <span data-ttu-id="9c03c-110">這項功能可讓您更準確地篩選較不信任或不信任的郵件程式，並同時保留您所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="9c03c-110">This is done in the interest of more accurately filtering out less trusted or untrusted mailers while keeping what you need.</span></span> <span data-ttu-id="9c03c-111">連線篩選原則允許清單是關於從更大的帳戶和 IP 集區，篩選到少數信任的 IP，並確保您信任的郵件程式能更輕鬆地存取。</span><span class="sxs-lookup"><span data-stu-id="9c03c-111">A connection filter policy Allow list is about filtering to the few trusted IPs from a much larger pool of accounts and IPs, and assuring your trusted mailers easier access.</span></span>

- <span data-ttu-id="9c03c-112">可將建立封鎖清單的連線篩選原則視為在篩選器中捕捉較少或不信任的帳戶。</span><span class="sxs-lookup"><span data-stu-id="9c03c-112">A connection filter policy creating a Block list can be thought of as catching less, or untrustworthy accounts in the filter instead.</span></span>

 <span data-ttu-id="9c03c-113">如需適用於整個組織的垃圾郵件設定，請參閱[如何在 Office 365 中防止好的電子郵件被標示為垃圾郵件](https://docs.microsoft.com/microsoft-365/compliance/prevent-email-from-being-marked-as-spam)或[如何減少 Office 365 中的垃圾郵件](reduce-spam-email.md)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-113">For more spam settings that apply to the whole organization, take a look at [How to prevent good email from being marked as spam in Office 365](https://docs.microsoft.com/microsoft-365/compliance/prevent-email-from-being-marked-as-spam) or [How to reduce spam email in Office 365](reduce-spam-email.md).</span></span> <span data-ttu-id="9c03c-114">如果您有系統管理員層級的控制權，且您想要避免誤判或漏報，這些內容很有幫助。</span><span class="sxs-lookup"><span data-stu-id="9c03c-114">These are helpful if you have administrator-level control and you want to prevent false positives or false negatives.</span></span>

> [!TIP]
> <span data-ttu-id="9c03c-115">您可能想要暫停並了解如何建立[允許 (或安全寄件者) 清單](create-safe-sender-lists-in-office-365.md)和[封鎖清單](create-block-sender-lists-in-office-365.md)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-115">You may want to pause and read up on how to create [Allow (or safe sender) lists](create-safe-sender-lists-in-office-365.md) and [Block lists](create-block-sender-lists-in-office-365.md).</span></span>

<span data-ttu-id="9c03c-116">下列影片顯示連線篩選原則的組態步驟：</span><span class="sxs-lookup"><span data-stu-id="9c03c-116">The following video shows the configuration steps for the connection filter policy:</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9c03c-117">開始之前有哪些須知？</span><span class="sxs-lookup"><span data-stu-id="9c03c-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9c03c-118">預估完成時間：15 分鐘</span><span class="sxs-lookup"><span data-stu-id="9c03c-118">Estimated time to complete: 15 minutes</span></span>

- <span data-ttu-id="9c03c-119">您必須已獲指派權限，才能執行此程序或這些程序。</span><span class="sxs-lookup"><span data-stu-id="9c03c-119">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="9c03c-120">若要查看您需要的權限，請參閱 [Exchange Online 中的功能權限](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions) (部分機器翻譯) 主題中的「反垃圾郵件」項目。</span><span class="sxs-lookup"><span data-stu-id="9c03c-120">To see what permissions you need, see the Anti-spam entry in the [Feature Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions) topic.</span></span>

- <span data-ttu-id="9c03c-121">若要取得寄件者的 IP 位址以允許或封鎖其郵件，您可以檢查郵件的 Internet 標頭。</span><span class="sxs-lookup"><span data-stu-id="9c03c-121">To obtain the IP address of the sender whose messages you want to allow or block, you can check the Internet header of the message.</span></span> <span data-ttu-id="9c03c-122">如＜[反垃圾郵件訊息標頭](anti-spam-message-headers.md)＞所述尋找 CIP 標頭。</span><span class="sxs-lookup"><span data-stu-id="9c03c-122">Look for the CIP header as described in [Anti-spam message headers](anti-spam-message-headers.md).</span></span> <span data-ttu-id="9c03c-123">如需如何在各種電子郵件用戶端中檢視郵件標頭的詳細資訊，請參閱[在 Outlook 中查看網際網路郵件標題](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-123">For information about how to view a message header in various email clients, see [View internet message headers in Outlook](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c).</span></span>

- <span data-ttu-id="9c03c-124">從 IP 封鎖清單上的 IP 位址傳送的電子郵件訊息會遭到拒絕，不會標示為垃圾郵件，也不會發生額外的篩選。</span><span class="sxs-lookup"><span data-stu-id="9c03c-124">Email messages sent from an IP address on the IP Block list are rejected, not marked as spam, and no additional filtering occurs.</span></span>

- <span data-ttu-id="9c03c-125">下列連線篩選程序也可以透過遠端 PowerShell 執行。</span><span class="sxs-lookup"><span data-stu-id="9c03c-125">The following connection filter procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="9c03c-126">使用 [Get-HostedConnectionFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-hostedconnectionfilterpolicy) Cmdlet 來檢閱您的設定，以及使用 [Set-HostedConnectionFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedconnectionfilterpolicy) 來編輯您的連線篩選原則設定。</span><span class="sxs-lookup"><span data-stu-id="9c03c-126">Use the [Get-HostedConnectionFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-hostedconnectionfilterpolicy) cmdlet to review your settings, and the [Set-HostedConnectionFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedconnectionfilterpolicy) to edit your connection filter policy settings.</span></span> <span data-ttu-id="9c03c-127">若要了解如何使用 Windows PowerShell 來連接至 Exchange Online Protection，請參閱[連線到 Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell) (部分機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-127">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span> <span data-ttu-id="9c03c-128">若要了解如何使用 Windows PowerShell 連線到 Exchange Online，請參閱[連線到 Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-128">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a><span data-ttu-id="9c03c-129">使用 EAC 編輯預設連線篩選原則</span><span class="sxs-lookup"><span data-stu-id="9c03c-129">Use the EAC to edit the default connection filter policy</span></span>

<span data-ttu-id="9c03c-p108">您可以在 Exchange 系統管理中心 (EAC) 編輯連線篩選原則，以建立 IP 允許清單或 IP 封鎖清單。連線篩選原則設定僅適用於輸入郵件。</span><span class="sxs-lookup"><span data-stu-id="9c03c-p108">You create an IP Allow list or IP Block list by editing the connection filter policy in the Exchange admin center (EAC). The connection filter policy settings are applied to inbound messages only.</span></span>

1. <span data-ttu-id="9c03c-132">在 Exchange 系統管理中心 (EAC)，瀏覽至 **[保護]** \> **[連線篩選器]**，然後連按兩下預設原則。</span><span class="sxs-lookup"><span data-stu-id="9c03c-132">In the Exchange admin center (EAC), navigate to **Protection** \> **Connection filter**, and then double-click the default policy.</span></span>

2. <span data-ttu-id="9c03c-133">Click the **Connection filtering** menu item and then create the lists you want: an IP Allow list, an IP Block list, or both.</span><span class="sxs-lookup"><span data-stu-id="9c03c-133">Click the **Connection filtering** menu item and then create the lists you want: an IP Allow list, an IP Block list, or both.</span></span>

   <span data-ttu-id="9c03c-p109">若要建立這些清單，請按一下![加入圖示](../media/ITPro-EAC-AddIcon.gif)。在後續對話方塊中，指定 IP 位址或位址範圍，然後按一下 **[確定]**。重複此程序來新增其他位址。(新增 IP 位址後，您也可以編輯或移除 IP 位址。)</span><span class="sxs-lookup"><span data-stu-id="9c03c-p109">To create these lists, click ![Add Icon](../media/ITPro-EAC-AddIcon.gif). In the subsequent dialog box, specify the IP address or address range, and then click **ok**. Repeat this process to add additional addresses. (You can also edit or remove IP addresses after they have been added.)</span></span>

   <span data-ttu-id="9c03c-138">以 nnn.nnn.nnn.nnn 格式 (其中 nnn 是從 0 到 255 的數字) 來指定 IPV4 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9c03c-138">IPV4 IP addresses must be specified in the format nnn.nnn.nnn.nnn where nnn is a number from 0 to 255.</span></span> <span data-ttu-id="9c03c-139">您也可以用 nnn.nnn.nnn.nnn/rr 格式來指定無類別網域間路由選擇 (CIDR) 範圍，其中 rr 是 24 到 32 的數字。</span><span class="sxs-lookup"><span data-stu-id="9c03c-139">You can also specify Classless Inter-Domain Routing (CIDR) ranges in the format nnn.nnn.nnn.nnn/rr where rr is a number from 24 to 32.</span></span> <span data-ttu-id="9c03c-140">若要指定 24 到 32 以外的範圍，請參閱下一節：[設定 IP 允許清單時的其他考量](#additional-considerations-when-configuring-ip-allow-lists)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-140">To specify ranges outside of the 24 to 32 range, see  [Additional considerations when configuring IP Allow lists](#additional-considerations-when-configuring-ip-allow-lists).</span></span>

   > [!NOTE]
   > <span data-ttu-id="9c03c-141">如果將 IP 位址新增到兩個清單中，則允許從該 IP 位址傳送的電子郵件。</span><span class="sxs-lookup"><span data-stu-id="9c03c-141">If you add an IP address to both lists, email sent from it is allowed.</span></span> <br/><br/> <span data-ttu-id="9c03c-p112">您最多可以指定 1273 個項目，一個項目就是單一 IP 位址，或 IP 位址從 /24 至 /32 的 CIDR 範圍。 </span><span class="sxs-lookup"><span data-stu-id="9c03c-p112">You can specify a maximum of 1273 entries, where an entry is either a single IP address or a CIDR range of IP addresses from /24 to /32. </span></span><br/><br/> <span data-ttu-id="9c03c-143">如果您正在傳送 TLS 加密訊息，則 IPv6 位址與位址範圍不受支援。</span><span class="sxs-lookup"><span data-stu-id="9c03c-143">>  If you're sending TLS-encrypted messages, IPv6 addresses and address ranges are supported.</span></span>

3. <span data-ttu-id="9c03c-144">或者，選取 **[啟用安全清單]** 核取方塊避免某些已知寄件者的電子郵件遺失。</span><span class="sxs-lookup"><span data-stu-id="9c03c-144">Optionally, select the **Enable safe list** check box to prevent missing email from certain well-known senders.</span></span> <span data-ttu-id="9c03c-145">怎麼做？</span><span class="sxs-lookup"><span data-stu-id="9c03c-145">How?</span></span> <span data-ttu-id="9c03c-146">Microsoft 會訂閱協力廠商來源的信任寄件者。</span><span class="sxs-lookup"><span data-stu-id="9c03c-146">Microsoft subscribes to third-party sources of trusted senders.</span></span> <span data-ttu-id="9c03c-147">使用這份安全清單表示不會將信任的寄件者錯誤標記為垃圾郵件。</span><span class="sxs-lookup"><span data-stu-id="9c03c-147">Using this safe list means that these trusted senders aren't mistakenly marked as spam.</span></span> <span data-ttu-id="9c03c-148">我們建議您選取這個選項，因為它應該會減少您收到的誤判 (好的郵件被分類為垃圾郵件)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-148">We recommend selecting this option because it should reduce the number of false positives (good mail that's classified as spam) that you receive.</span></span>

4. <span data-ttu-id="9c03c-p114">按一下 **[儲存]**。預設原則設定的摘要隨即出現在右側窗格中。</span><span class="sxs-lookup"><span data-stu-id="9c03c-p114">Click **save**. A summary of your default policy settings appears in the right pane.</span></span>

## <a name="additional-considerations-when-configuring-ip-allow-lists"></a><span data-ttu-id="9c03c-151">設定 IP 允許清單時的其他考量</span><span class="sxs-lookup"><span data-stu-id="9c03c-151">Additional considerations when configuring IP Allow lists</span></span>

<span data-ttu-id="9c03c-152">以下是設定 IP 允許清單時需要考慮或應該注意的其他事項。</span><span class="sxs-lookup"><span data-stu-id="9c03c-152">The following are additional considerations you may want to consider or that you should be aware of when configuring an IP Allow list.</span></span>

### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a><span data-ttu-id="9c03c-153">指定超出建議範圍的 CIDR 範圍</span><span class="sxs-lookup"><span data-stu-id="9c03c-153">Specifying a CIDR range that falls outside of the recommended range</span></span>

<span data-ttu-id="9c03c-154">若要指定 /1 到 /23 的 CIDR IP 位址範圍，您必須建立在該 IP 位置範圍上運作的傳輸規則，並使該規則將垃圾郵件信賴等級 (SCL) 設為 [略過垃圾郵件篩選]\*\*\*\* (表示將接收自此 IP 位址範圍的所有郵件都設為「不是垃圾郵件」，且服務不會執行其他篩選)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-154">To specify a CIDR IP address range from /1 to /23, you must create a Transport rule that operates on the IP address range that sets the spam confidence level (SCL) to **Bypass spam filtering** (meaning that all messages received from within this IP address range are set to "not spam" and no additional filtering is performed by the service).</span></span> <span data-ttu-id="9c03c-155">However, if any of these IP addresses appear on any of Microsoft's proprietary block lists or on any of our third-party block lists, these messages will still be blocked.</span><span class="sxs-lookup"><span data-stu-id="9c03c-155">However, if any of these IP addresses appear on any of Microsoft's proprietary block lists or on any of our third-party block lists, these messages will still be blocked.</span></span> <span data-ttu-id="9c03c-156">因此，強烈建議您使用 /24 到 /32 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="9c03c-156">It is therefore strongly recommended that you use the /32 to /24 IP address range.</span></span>

<span data-ttu-id="9c03c-157">若要建立此郵件流程規則，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="9c03c-157">To create this Transport rule, perform the following steps.</span></span>

1. <span data-ttu-id="9c03c-158">在 EAC 中，瀏覽至 **[郵件流程]** \> **[規則]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-158">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="9c03c-159">按一下 ![加入圖示](../media/ITPro-EAC-AddIcon.gif)，然後選取 **[建立新的規則]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-159">Click ![Add Icon](../media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="9c03c-160">命名規則，然後按一下 **[更多選項]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-160">Give the rule a name and then click **More options**.</span></span>

4. <span data-ttu-id="9c03c-161">在 **[套用此規則情況]** 下，選取 **[寄件者]**，然後選擇 **[IP 位址在任何這些範圍中或完全符合]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-161">Under **Apply this rule if**, select **The sender** and then choose **IP address is in any of these ranges or exactly matches**.</span></span>

5. <span data-ttu-id="9c03c-162">在 [指定 IP 位址]\*\*\*\* 方塊中，指定 IP 位址範圍，按一下 [新增]\*\*\*\* ![新增圖示](../media/ITPro-EAC-AddIcon.gif)，然後按一下 [確定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="9c03c-162">In the **specify IP addresses**, specify the IP address range, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif), and then click **ok**.</span></span>

6. <span data-ttu-id="9c03c-p116">在 **[執行下列動作]** 方塊下，選擇 **[修改訊息屬性]**，再選擇 **[設定垃圾郵件信賴等級 (SCL)]** 來設定動作。在 **[指定 SCL]** 方塊中，選取 **[略過垃圾郵件篩選]**，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-p116">Under **Do the following** box, set the action by choosing **Modify the message properties** and then **set the spam confidence level (SCL)**. In the **specify SCL** box, select **Bypass spam filtering**, and click **ok**.</span></span>

7. <span data-ttu-id="9c03c-165">您也可以視需要選取稽核規則、測試規則、在特定期間啟動規則等等選項。</span><span class="sxs-lookup"><span data-stu-id="9c03c-165">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections.</span></span> <span data-ttu-id="9c03c-166">施行規則之前，建議先測試規則一段時間。</span><span class="sxs-lookup"><span data-stu-id="9c03c-166">We recommend testing the rule for a period before you enforce it.</span></span> <span data-ttu-id="9c03c-167">[Exchange Server 中的郵件流程規則](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) (部分機器翻譯) 包含這些選項的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9c03c-167">[Procedures for mail flow rules in Exchange Server](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contains more information about these selections.</span></span>

8. <span data-ttu-id="9c03c-168">按一下 [儲存]\*\*\*\* 儲存規則。</span><span class="sxs-lookup"><span data-stu-id="9c03c-168">Click the **save** button to save the rule.</span></span> <span data-ttu-id="9c03c-169">規則會顯示在您的規則清單中。</span><span class="sxs-lookup"><span data-stu-id="9c03c-169">It appears in your list of rules.</span></span>

<span data-ttu-id="9c03c-170">當您建立並強制執行規則之後，服務會針對您指定的 IP 位址範圍略過垃圾郵件篩選。</span><span class="sxs-lookup"><span data-stu-id="9c03c-170">After you create and enforce the rule, spam filtering is bypassed for the IP address range you specified.</span></span>

### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a><span data-ttu-id="9c03c-171">針對特定網域設定 IP 允許清單例外狀況</span><span class="sxs-lookup"><span data-stu-id="9c03c-171">Scoping an IP Allow list exception for a specific domain</span></span>

<span data-ttu-id="9c03c-172">一般而言，建議將您認為安全的所有網域的 IP 位址 (或 IP 位址範圍) 新增至 IP 允許清單。</span><span class="sxs-lookup"><span data-stu-id="9c03c-172">In general, we recommend that you add the IP addresses (or IP address ranges) for all your domains that you consider safe to the IP Allow list.</span></span> <span data-ttu-id="9c03c-173">不過，如果不要將 IP 允許清單項目套用至所有網域，您可以建立排除特定網域的郵件流程規則 (也稱為傳輸規則)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-173">However, if you don't want your IP Allow List entry to apply to all your domains, you can create a Transport rule that excepts specific domains.</span></span>

<span data-ttu-id="9c03c-174">例如，假設您有三個網域：ContosoA.com、ContosoB.com 和 ContosoC.com，而您想要新增 IP 位址 (為了簡單起見，我們用 1.2.3.4)，並僅針對網域 ContosoB.com 來略過篩選。</span><span class="sxs-lookup"><span data-stu-id="9c03c-174">For example, let's say you have three domains: ContosoA.com, ContosoB.com, and ContosoC.com, and you want to add the IP address (for simplicity's sake, let's use 1.2.3.4) and skip filtering only for domain ContosoB.com.</span></span> <span data-ttu-id="9c03c-175">您可以建立 1.2.3.4 的 IP 允許清單，以針對所有網域將垃圾郵件信賴等級 (SCL) 設定為 -1 (表示歸類為非垃圾郵件)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-175">You would create an IP Allow list for 1.2.3.4, which sets the spam confidence level (SCL) to -1 (meaning it is classified as non-spam) for all domains.</span></span> <span data-ttu-id="9c03c-176">接著，您可以建立一個郵件流程規則，以針對 ContosoB.com 以外的所有網域將 SCL 設定為 0。</span><span class="sxs-lookup"><span data-stu-id="9c03c-176">You can then create a Transport rule that sets the SCL for all domains except ContosoB.com to 0.</span></span> <span data-ttu-id="9c03c-177">這會導致針對與此 IP 位址相關聯的所有網域 (在規則中列為例外的 ContosoB.com 除外) 來重新掃描郵件。</span><span class="sxs-lookup"><span data-stu-id="9c03c-177">This results in the message being rescanned for all domains associated with the IP address except for ContosoB.com which is the domain listed as the exception in the rule.</span></span> <span data-ttu-id="9c03c-178">ContosoB.com 的 SCL 仍為 -1 (表示略過篩選)，然而 ContosoA.com 和 ContosoC.com 的 SCL 為 0 (表示將由內容篩選器進行重複掃描)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-178">ContosoB.com still has an SCL of -1 which means skip filtering, whereas ContosoA.com and ContosoC.com have SCLs of 0, meaning they will be rescanned by the content filter.</span></span>

<span data-ttu-id="9c03c-179">若要執行此動作，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9c03c-179">To do this, perform the following steps:</span></span>

1. <span data-ttu-id="9c03c-180">在 EAC 中，瀏覽至 **[郵件流程]** \> **[規則]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-180">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>

2. <span data-ttu-id="9c03c-181">按一下 ![加入圖示](../media/ITPro-EAC-AddIcon.gif)，然後選取 **[建立新的規則]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-181">Click ![Add Icon](../media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>

3. <span data-ttu-id="9c03c-182">命名規則，然後按一下 **[更多選項]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-182">Give the rule a name and then click **More options**.</span></span>

4. <span data-ttu-id="9c03c-183">在 **[套用此規則情況]** 下，選取 **[寄件者]**，然後選擇 **[IP 位址在任何這些範圍中或完全符合]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-183">Under **Apply this rule if**, select **The sender** and then choose **IP address is in any of these ranges or exactly matches**.</span></span>

5. <span data-ttu-id="9c03c-184">在 [指定 IP 位址]\*\*\*\* 方塊中，指定您在 IP 允許清單中輸入的 IP 位址或 IP 位址範圍，按一下 [新增]\*\*\*\* ![新增圖示](../media/ITPro-EAC-AddIcon.gif)，然後按一下 [確定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="9c03c-184">In the **specify IP addresses** box, specify the IP address or IP address range you entered in the IP Allow list, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif), and then click **ok**.</span></span>

6. <span data-ttu-id="9c03c-185">在 [執行下列動作]\*\*\*\* 下，選擇 [修改訊息屬性]\*\*\*\*，再選擇 [設定垃圾郵件信賴等級 (SCL)]\*\*\*\* 來設定動作。</span><span class="sxs-lookup"><span data-stu-id="9c03c-185">Under **Do the following**, set the action by choosing **Modify the message properties** and then **set the spam confidence level (SCL)**.</span></span> <span data-ttu-id="9c03c-186">在 [指定 SCL]\*\*\*\* 方塊中，選取 [0]\*\*\*\*，然後按一下 [確定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="9c03c-186">In the **specify SCL** box, select **0**, and click **ok**.</span></span>

7. <span data-ttu-id="9c03c-187">按一下 [新增例外狀況]\*\*\*\*，在 [除非]\*\*\*\* 下，選取 [寄件者]\*\*\*\*，然後選擇 [網域是]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="9c03c-187">Click **add exception**, and under **Except if**, select **The sender** and choose **domain is**.</span></span>

8. <span data-ttu-id="9c03c-188">在 [指定網域]\*\*\*\* 方塊中，輸入您要略過垃圾郵件篩選的網域，例如 **contosob.com**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-188">In the **specify domain** box, enter the domain for which you want to bypass spam filtering, such as **contosob.com**.</span></span> <span data-ttu-id="9c03c-189">按一下 [新增]\*\*\*\* ![新增圖示](../media/ITPro-EAC-AddIcon.gif)，將它移至片語清單。</span><span class="sxs-lookup"><span data-stu-id="9c03c-189">Click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif) to move it to the list of phrases.</span></span> <span data-ttu-id="9c03c-190">如果要新增其他網域當作例外狀況，請重複此步驟，完成時按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-190">Repeat this step if you want to add additional domains as exceptions, and click **ok** when you are finished.</span></span>

9. <span data-ttu-id="9c03c-191">您也可以視需要選取稽核規則、測試規則、在特定期間啟動規則等等選項。</span><span class="sxs-lookup"><span data-stu-id="9c03c-191">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections.</span></span> <span data-ttu-id="9c03c-192">施行規則之前，建議先測試規則一段時間。</span><span class="sxs-lookup"><span data-stu-id="9c03c-192">We recommend testing the rule for a period before you enforce it.</span></span> <span data-ttu-id="9c03c-193">[Exchange Server 中的郵件流程規則](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) (部分機器翻譯) 包含這些選項的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9c03c-193">[Procedures for mail flow rules in Exchange Server](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contains more information about these selections.</span></span>

10. <span data-ttu-id="9c03c-194">按一下 [儲存]\*\*\*\* 儲存規則。</span><span class="sxs-lookup"><span data-stu-id="9c03c-194">Click **Save** to save the policy.</span></span> <span data-ttu-id="9c03c-195">規則會顯示在您的規則清單中。</span><span class="sxs-lookup"><span data-stu-id="9c03c-195">It appears in your list of rules.</span></span>

<span data-ttu-id="9c03c-196">建立並強制執行規則後，系統就只會針對您輸入的例外網域，對您指定的 IP 位址或 IP 位址範圍略過垃圾郵件篩選。</span><span class="sxs-lookup"><span data-stu-id="9c03c-196">After you create and enforce the rule, spam filtering for the IP address or IP address range you specified is bypassed only for the domain exception you entered.</span></span>

### <a name="scenarios-where-allowed-ip-addresses-are-still-filtered"></a><span data-ttu-id="9c03c-197">仍然篩選允許 IP 位址的案例</span><span class="sxs-lookup"><span data-stu-id="9c03c-197">Scenarios where allowed IP addresses are still filtered</span></span>

<span data-ttu-id="9c03c-198">在下列案例中，來自您在連線篩選原則中所設定允許 IP 位址的郵件，仍然受限於垃圾郵件篩選：</span><span class="sxs-lookup"><span data-stu-id="9c03c-198">Messages from allowed IP addresses that you've configured in connection filter policies are still subject to spam filtering in the following scenarios:</span></span>

- <span data-ttu-id="9c03c-199">連線篩選原則中的來源 IP 位址也是在內部部署、以 IP 為主的輸入連接器、「任何」\*\* 租用戶 (讓我們將其稱為租用戶 A) 中設定，**而且**租用戶 A 和第一次在 Office 365 中遇到郵件的 Exchange Online Protection 伺服器都是在 Microsoft 資料中心的相同 Active Directory 樹系。</span><span class="sxs-lookup"><span data-stu-id="9c03c-199">The source IP address in your connection filter policy is also configured in an on-premises, IP-based inbound connector in *any* tenant (let's call this Tenant A), **and** Tenant A and the Exchange Online Protection server that first encounters the message in Office 365 both happen to be in the same Active Directory forest in the Microsoft datacenters.</span></span> <span data-ttu-id="9c03c-200">在這種情況下，**IPV:CAL** 會新增至郵件的[反垃圾郵件標頭](anti-spam-message-headers.md) (表示郵件略過垃圾郵件篩選)，但是郵件仍受限於垃圾郵件篩選。</span><span class="sxs-lookup"><span data-stu-id="9c03c-200">In this scenario, **IPV:CAL** is added to the message's [anti-spam message headers](anti-spam-message-headers.md) (indicating the message bypassed spam filtering), but the message is still subject to spam filtering.</span></span>

- <span data-ttu-id="9c03c-201">您的租用戶 (您已設定連線篩選原則) 和 Exchange Online Protection 伺服器 (在 Office 365 中第一次遇到郵件)，出現在 Microsoft 資料中心的不同 Active Directory 樹系中。</span><span class="sxs-lookup"><span data-stu-id="9c03c-201">Your tenant (where you've configured the connection filter policy) and the Exchange Online Protection server that first encounters the message in Office 365 both happen to be in different Active Directory forests in the Microsoft datacenters.</span></span> <span data-ttu-id="9c03c-202">在這個案例中，**IPV:CAL** 不會新增至郵件標頭，因此郵件仍受限於垃圾郵件篩選。</span><span class="sxs-lookup"><span data-stu-id="9c03c-202">In this scenario, **IPV:CAL** is not added to the message headers, so the message is still subject to spam filtering.</span></span>

<span data-ttu-id="9c03c-203">如果您遇到下列其中一種情況，您可以在 EAC 中建立郵件流程規則，並 (至少) 使用下列設定，以確保來自 IP 位址的郵件略過垃圾郵件篩選：</span><span class="sxs-lookup"><span data-stu-id="9c03c-203">If you encounter either of these scenarios, you can create a mail flow rule in the EAC with (at a minimum) the following settings to ensure messages from the IP address or addresses bypass spam filtering:</span></span>

- <span data-ttu-id="9c03c-204">規則條件：**若為以下情況，套用這個規則** \> **寄件者** \> **IP 位址在任何這些範圍中或完全符合** \> (您的 IP 位址)。</span><span class="sxs-lookup"><span data-stu-id="9c03c-204">Rule condition: **Apply this rule if** \> **The sender** \> **IP address is in any of these ranges or exactly matches** \> (your IP address or addresses).</span></span>

- <span data-ttu-id="9c03c-205">規則動作：**修改郵件屬性** \> **設定垃圾郵件信賴等級 (SCL)** \> **略過垃圾郵件篩選**。</span><span class="sxs-lookup"><span data-stu-id="9c03c-205">Rule action: **Modify the message properties** \> **Set the spam confidence level (SCL)** \> **Bypass spam filtering**.</span></span>

<span data-ttu-id="9c03c-206">基本上是與上一個[針對特定網域設定 IP 允許清單例外狀況](#scoping-an-ip-allow-list-exception-for-a-specific-domain)區段的規則建立程序相同。</span><span class="sxs-lookup"><span data-stu-id="9c03c-206">This is basically the same rule creation procedure from the previous [Scoping an IP Allow list exception for a specific domain](#scoping-an-ip-allow-list-exception-for-a-specific-domain) section.</span></span>

## <a name="new-to-office-365"></a><span data-ttu-id="9c03c-207">初次使用 Office 365 嗎？</span><span class="sxs-lookup"><span data-stu-id="9c03c-207">New to Office 365?</span></span>

||
|:-----|
|<span data-ttu-id="9c03c-208">![LinkedIn Learning 的短圖示](../media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **初次使用 Office 365？**</span><span class="sxs-lookup"><span data-stu-id="9c03c-208">![The short icon for LinkedIn Learning](../media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**</span></span> <span data-ttu-id="9c03c-209">探索 LinkedIn Learning 提供的 **Office 365 admins and IT pros** 免費影片課程。</span><span class="sxs-lookup"><span data-stu-id="9c03c-209">Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span>|

## <a name="for-more-information"></a><span data-ttu-id="9c03c-210">如需詳細資訊</span><span class="sxs-lookup"><span data-stu-id="9c03c-210">For more information</span></span>

[<span data-ttu-id="9c03c-211">Exchange Online 中的安全寄件者和封鎖寄件者清單</span><span class="sxs-lookup"><span data-stu-id="9c03c-211">Safe sender and blocked sender lists in Exchange Online</span></span>](safe-sender-and-blocked-sender-lists-faq.md)

[<span data-ttu-id="9c03c-212">設定您的垃圾郵件篩選原則</span><span class="sxs-lookup"><span data-stu-id="9c03c-212">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="9c03c-213">設定輸出垃圾郵件原則</span><span class="sxs-lookup"><span data-stu-id="9c03c-213">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)

[<span data-ttu-id="9c03c-214">如何在 Office 365 中防止好的電子郵件被標示為垃圾郵件</span><span class="sxs-lookup"><span data-stu-id="9c03c-214">How to prevent real email from being marked as spam in Office 365</span></span>](https://docs.microsoft.com/microsoft-365/compliance/prevent-email-from-being-marked-as-spam)

[<span data-ttu-id="9c03c-215">如何減少 Office 365 中的垃圾郵件</span><span class="sxs-lookup"><span data-stu-id="9c03c-215">How to reduce spam email in Office 365</span></span>](reduce-spam-email.md)