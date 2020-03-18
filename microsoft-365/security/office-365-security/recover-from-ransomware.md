---
title: 從勒索軟體的攻擊中復原
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Office 365 系統管理員可以瞭解如何從勒索軟體的攻擊復原。
ms.openlocfilehash: aa606ea3bf3f549645fe26a4aa95066568132243
ms.sourcegitcommit: 72983702a42552a29228d387bb279e8ff2ab59b4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/14/2020
ms.locfileid: "42640015"
---
# <a name="recover-from-a-ransomware-attack-in-office-365"></a><span data-ttu-id="40cad-103">從 Office 365 復原勒索軟體攻擊</span><span class="sxs-lookup"><span data-stu-id="40cad-103">Recover from a ransomware attack in Office 365</span></span>

<span data-ttu-id="40cad-104">即使您採取每一種預防措施來保護 Office 365 組織，仍然可以遭到您的[勒索軟體](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)攻擊。</span><span class="sxs-lookup"><span data-stu-id="40cad-104">Even if you take every precaution to protect your Office 365 organization, you can still fall victim to a [ransomware](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware) attack.</span></span> <span data-ttu-id="40cad-105">勒索軟體是很大的商務用，攻擊是以複雜的驗證。</span><span class="sxs-lookup"><span data-stu-id="40cad-105">Ransomware is big business, and the attacks are verify sophisticated.</span></span>

<span data-ttu-id="40cad-106">本主題中的步驟可讓您最有可能復原由勒索軟體加密的資料，並將協助停止在 Office 365 組織中的感染傳播。</span><span class="sxs-lookup"><span data-stu-id="40cad-106">The steps in this topic will give you the best chance to recover data that was encrypted by the ransomware, and will help stop the spread of the infection in your Office 365 organization.</span></span> <span data-ttu-id="40cad-107">在您開始之前，請考慮下列項目：</span><span class="sxs-lookup"><span data-stu-id="40cad-107">Before you get started, consider the following items:</span></span>

- <span data-ttu-id="40cad-108">不保證支付 ransom 將會傳回檔案的存取權。</span><span class="sxs-lookup"><span data-stu-id="40cad-108">There's no guarantee that paying the ransom will return access to your files.</span></span> <span data-ttu-id="40cad-109">實際上，支付 ransom 可讓您成為更多勒索軟體的目標。</span><span class="sxs-lookup"><span data-stu-id="40cad-109">In fact, paying the ransom can make you a target for more ransomware.</span></span> <span data-ttu-id="40cad-110">如果您已付費，但您已能夠順利復原檔案，而不需要使用攻擊者的解決方式，則應該撥打您的銀行以查看是否可以封鎖交易。</span><span class="sxs-lookup"><span data-stu-id="40cad-110">If you've already paid, but you were able to successfully recover your files without having to use the attacker's resolution, you should call your bank to see if they can block the transaction.</span></span> <span data-ttu-id="40cad-111">此外，我們也建議您向法律強制執行（如本主題稍後所述），向法律執行、詐騙報告網站和 Microsoft 報告勒索軟體攻擊。</span><span class="sxs-lookup"><span data-stu-id="40cad-111">We also recommend that you report the ransomware attack to law enforcement, scam reporting websites and Microsoft as described later in this topic.</span></span>

- <span data-ttu-id="40cad-112">您必須快速回應攻擊及其結果，這一點很重要。</span><span class="sxs-lookup"><span data-stu-id="40cad-112">It's very important that you respond quickly to the attack and its consequences.</span></span> <span data-ttu-id="40cad-113">您等候的時間越長，您可以復原受影響資料的可能性也就越低。</span><span class="sxs-lookup"><span data-stu-id="40cad-113">The longer you wait, the less likely it is that you can recover the affected data.</span></span>

## <a name="step-1-verify-your-backups"></a><span data-ttu-id="40cad-114">步驟1：驗證備份</span><span class="sxs-lookup"><span data-stu-id="40cad-114">Step 1: Verify your backups</span></span>

<span data-ttu-id="40cad-115">如果您有離線備份，您可能會在從環境中移除勒索軟體的負載（惡意程式碼）**之後**，還原加密的資料。</span><span class="sxs-lookup"><span data-stu-id="40cad-115">If you have offline backups, you can probably restore the encrypted data **after** you've removed the ransomware payload (malware) from your environment.</span></span>

<span data-ttu-id="40cad-116">如果您沒有備份，或是您的備份也受到勒索軟體的影響，您可以略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="40cad-116">If you don't have backups, or if your backups were also affected by the ransomware, you can skip this step.</span></span>

## <a name="step-2-disable-activesync-and-onedrive-sync"></a><span data-ttu-id="40cad-117">步驟2：停用 ActiveSync 和 OneDrive 同步處理</span><span class="sxs-lookup"><span data-stu-id="40cad-117">Step 2: Disable ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="40cad-118">這裡的關鍵點是停止勒索軟體加密的資料加密。</span><span class="sxs-lookup"><span data-stu-id="40cad-118">The key point here is to stop the spread of data encryption by the ransomware.</span></span>

<span data-ttu-id="40cad-119">如果您懷疑電子郵件是目標，您應該暫時停用使用者對信箱的存取權。</span><span class="sxs-lookup"><span data-stu-id="40cad-119">If you suspect that email is a target, you should temporarily disable user access to mailboxes.</span></span> <span data-ttu-id="40cad-120">Exchange ActiveSync 是由行動裝置用於同步裝置與 Exchange Online 信箱之間的資料。</span><span class="sxs-lookup"><span data-stu-id="40cad-120">Exchange ActiveSync is used by mobile devices to synchronize data between the device and the Exchange Online mailbox.</span></span>

<span data-ttu-id="40cad-121">若要停用信箱的 ActiveSync，請參閱[如何針對 Office 365 中的使用者停用 Exchange ActiveSync](https://support.microsoft.com/help/2795303/how-to-disable-exchange-activesync-for-users-in-office-365)。</span><span class="sxs-lookup"><span data-stu-id="40cad-121">To disable ActiveSync for a mailbox, see [How to disable Exchange ActiveSync for users in Office 365](https://support.microsoft.com/help/2795303/how-to-disable-exchange-activesync-for-users-in-office-365).</span></span>

<span data-ttu-id="40cad-122">若要停用信箱的其他類型的存取，請參閱：</span><span class="sxs-lookup"><span data-stu-id="40cad-122">To disable other types of access to a mailbox, see:</span></span>

- <span data-ttu-id="40cad-123">[啟用或停用信箱的 MAPI](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi)。</span><span class="sxs-lookup"><span data-stu-id="40cad-123">[Enable or disable MAPI for a mailbox](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi).</span></span>

- [<span data-ttu-id="40cad-124">啟用或停用使用者 POP3 或 IMAP4 存取權</span><span class="sxs-lookup"><span data-stu-id="40cad-124">Enable or Disable POP3 or IMAP4 access for a user</span></span>](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/pop3-and-imap4/enable-or-disable-pop3-or-imap4-access)

<span data-ttu-id="40cad-125">暫停 OneDrive 同步處理會協助保護您的雲端資料，使其不會受到可能受感染的裝置更新。</span><span class="sxs-lookup"><span data-stu-id="40cad-125">Pausing OneDrive sync will help protect your cloud data from being updated by potentially infected devices.</span></span> <span data-ttu-id="40cad-126">如需詳細資訊，請參閱 how [To Pause And Resume sync in OneDrive](https://support.office.com/article/2152bfa4-a2a5-4d3a-ace8-92912fb4421e)。</span><span class="sxs-lookup"><span data-stu-id="40cad-126">For more information, see [How to Pause and Resume sync in OneDrive](https://support.office.com/article/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span></span>

## <a name="step-3-remove-the-malware-from-the-affected-devices"></a><span data-ttu-id="40cad-127">步驟3：從受影響的裝置移除惡意程式碼</span><span class="sxs-lookup"><span data-stu-id="40cad-127">Step 3: Remove the malware from the affected devices</span></span>

<span data-ttu-id="40cad-128">在所有可疑電腦和裝置上執行完整的防病毒掃描，並提供最新的更新，以偵測和移除與勒索軟體相關聯的負載。</span><span class="sxs-lookup"><span data-stu-id="40cad-128">Run a full antivirus scan with the latest updates on all suspected computers and devices to detect and remove the payload that's associated with the ransomware.</span></span> <span data-ttu-id="40cad-129">請勿忘記正在同步處理資料的裝置，或對應網路磁碟機的目標（即必須掃描那些電腦和裝置）。</span><span class="sxs-lookup"><span data-stu-id="40cad-129">Don't forget devices that are synchronizing data, or the target of mapped network drives (those computers and devices need to be scanned, too).</span></span>

<span data-ttu-id="40cad-130">您可以使用[Windows Defender](https://www.microsoft.com/windows/comprehensive-security)或（適用于舊版用戶端） [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201)。</span><span class="sxs-lookup"><span data-stu-id="40cad-130">You can use [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) or (for older clients) [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span></span>

<span data-ttu-id="40cad-131">另一種方式也可協助您移除勒索軟體或惡意[軟體是惡意軟體移除工具（MSRT）](https://www.microsoft.com/download/details.aspx?id=9905)。</span><span class="sxs-lookup"><span data-stu-id="40cad-131">An alternative that will also help you remove ransomware or malware is the [Malicious Software Removal Tool (MSRT)](https://www.microsoft.com/download/details.aspx?id=9905).</span></span>

<span data-ttu-id="40cad-132">如果這些選項不起作用，您可以嘗試使用[Windows Defender 離線](https://support.microsoft.com/help/17466/windows-defender-offline-help-protect-my-pc)或[疑難排解偵測和移除惡意程式碼的問題](https://support.microsoft.com/help/4466982/windows-10-troubleshoot-problems-with-detecting-and-removing-malware)。</span><span class="sxs-lookup"><span data-stu-id="40cad-132">If these options don't work, you can try [Windows Defender Offline](https://support.microsoft.com/help/17466/windows-defender-offline-help-protect-my-pc) or [Troubleshoot problems with detecting and removing malware](https://support.microsoft.com/help/4466982/windows-10-troubleshoot-problems-with-detecting-and-removing-malware).</span></span>

## <a name="step-4-recover-files-on-a-cleaned-computer-or-device"></a><span data-ttu-id="40cad-133">步驟4：在已清除的電腦或裝置上復原檔案</span><span class="sxs-lookup"><span data-stu-id="40cad-133">Step 4: Recover files on a cleaned computer or device</span></span>

<span data-ttu-id="40cad-134">在您完成上述步驟以從環境中移除勒索軟體負載（以避免勒索軟體加密或移除檔案）之後，您可以使用 windows 10 和 Windows 8.1 中的檔案歷程[記錄](https://support.microsoft.com/help/17128/windows-8-file-history)，或 windows 7 中的系統保護，以嘗試復原您的本機檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="40cad-134">After you've completed the previous step to remove the ransomware payload from your environment (which will prevent the ransomware from encrypting or removing your files), you can use [File History](https://support.microsoft.com/help/17128/windows-8-file-history) in Windows 10 and Windows 8.1 or System Protection in Windows 7 to attempt to recover your local files and folders.</span></span>

<span data-ttu-id="40cad-135">**附註**：</span><span class="sxs-lookup"><span data-stu-id="40cad-135">**Notes**:</span></span>

- <span data-ttu-id="40cad-136">有些勒索軟體也會加密或刪除備份版本，因此您無法使用檔案記錄或系統保護來還原檔案。</span><span class="sxs-lookup"><span data-stu-id="40cad-136">Some ransomware will also encrypt or delete the backup versions, so you can't use File History or System Protection to restore files.</span></span> <span data-ttu-id="40cad-137">如果發生這種情況，您需要在外部磁片磁碟機或未受勒索軟體或 OneDrive 的裝置上使用備份，如下一節所述。</span><span class="sxs-lookup"><span data-stu-id="40cad-137">If that happens, you need use backups on external drives or devices that were not affected by the ransomware or OneDrive as described in the next section.</span></span>

- <span data-ttu-id="40cad-138">如果資料夾與 OneDrive 同步處理，而且您不是使用最新版的 Windows，則可能會有一些限制使用檔案歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="40cad-138">If a folder is synchronized to OneDrive and you aren't using the latest version of Windows, there might be some limitations using File History.</span></span>

## <a name="step-5-recover-your-files-in-your-onedrive-for-business"></a><span data-ttu-id="40cad-139">步驟5：在您的 OneDrive 商務中復原檔案</span><span class="sxs-lookup"><span data-stu-id="40cad-139">Step 5: Recover your files in your OneDrive for Business</span></span>

<span data-ttu-id="40cad-140">在 OneDrive for Business 中還原檔案，可讓您在過去的30天內，將整個 OneDrive 還原至上一個時間點。</span><span class="sxs-lookup"><span data-stu-id="40cad-140">Files Restore in OneDrive for Business allows you to restore your entire OneDrive to a previous point in time within the last 30 days.</span></span> <span data-ttu-id="40cad-141">如需詳細資訊，請參閱[還原您的 OneDrive](https://support.office.com/article/fa231298-759d-41cf-bcd0-25ac53eb8a15)。</span><span class="sxs-lookup"><span data-stu-id="40cad-141">For more information, see [Restore your OneDrive](https://support.office.com/article/fa231298-759d-41cf-bcd0-25ac53eb8a15).</span></span>

## <a name="step-6-recover-deleted-email"></a><span data-ttu-id="40cad-142">步驟6：復原已刪除的電子郵件</span><span class="sxs-lookup"><span data-stu-id="40cad-142">Step 6: Recover deleted email</span></span>

<span data-ttu-id="40cad-143">在少數情況下，勒索軟體會刪除所有的電子郵件，您可能會復原已刪除的郵件。</span><span class="sxs-lookup"><span data-stu-id="40cad-143">In the rare case that the ransomware deleted all your email, you can probably recover the deleted items.</span></span> <span data-ttu-id="40cad-144">如需詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="40cad-144">For more information, see:</span></span>

- [<span data-ttu-id="40cad-145">復原刪除的郵件使用者的信箱</span><span class="sxs-lookup"><span data-stu-id="40cad-145">Recover deleted messages in a user's mailbox</span></span>](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages)

- [<span data-ttu-id="40cad-146">在 Windows 版 Outlook 復原已刪除的項目</span><span class="sxs-lookup"><span data-stu-id="40cad-146">Recover deleted items in Outlook for Windows</span></span>](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce)

## <a name="step-7-re-enable-exchange-activesync-and-onedrive-sync"></a><span data-ttu-id="40cad-147">步驟7：重新啟用 Exchange ActiveSync 和 OneDrive 同步處理</span><span class="sxs-lookup"><span data-stu-id="40cad-147">Step 7: Re-enable Exchange ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="40cad-148">在您清潔電腦和裝置並復原資料後，您可以重新啟用 ActiveSync，並 OneDrive 您先前在[步驟 2](#step-2-disable-activesync-and-onedrive-sync)中停用的同步處理。</span><span class="sxs-lookup"><span data-stu-id="40cad-148">After you've cleaned your computers and devices and recovered your data, you can re-enable ActiveSync and OneDrive sync that you previously disabled in [Step 2](#step-2-disable-activesync-and-onedrive-sync).</span></span>

## <a name="step-8-optional-block-onedrive-sync-for-specific-file-extensions"></a><span data-ttu-id="40cad-149">步驟8（選用）：封鎖特定檔案副檔名的 OneDrive 同步處理</span><span class="sxs-lookup"><span data-stu-id="40cad-149">Step 8 (Optional): Block OneDrive sync for specific file extensions</span></span>

<span data-ttu-id="40cad-150">復原之後，您可以防止商務用戶端的 OneDrive 同步處理此勒索軟體所影響的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="40cad-150">After you've recovered, you can prevent OneDrive for Business clients from synchronizing the file types that were affected by this ransomware.</span></span> <span data-ttu-id="40cad-151">如需詳細資訊，請參閱[Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span><span class="sxs-lookup"><span data-stu-id="40cad-151">For more information, see [Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span></span>

## <a name="report-the-attack"></a><span data-ttu-id="40cad-152">報告攻擊</span><span class="sxs-lookup"><span data-stu-id="40cad-152">Report the attack</span></span>

### <a name="contact-law-enforcement"></a><span data-ttu-id="40cad-153">連絡人法律強制執行</span><span class="sxs-lookup"><span data-stu-id="40cad-153">Contact law enforcement</span></span>

<span data-ttu-id="40cad-154">您應與當地或聯邦執法機構聯繫。</span><span class="sxs-lookup"><span data-stu-id="40cad-154">You should contact your local or federal law enforcement agencies.</span></span> <span data-ttu-id="40cad-155">例如，如果您在美國，您可以聯繫[FBI 當地欄位 office](https://www.fbi.gov/contact-us/field)、 [IC3](http://www.ic3.gov/complaint/default.aspx)或[機密服務](http://www.secretservice.gov/)。</span><span class="sxs-lookup"><span data-stu-id="40cad-155">For example, if you are in the United States you can contact the [FBI local field office](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) or [Secret Service](http://www.secretservice.gov/).</span></span>

### <a name="submit-a-report-to-your-countrys-scam-reporting-website"></a><span data-ttu-id="40cad-156">將報告提交至您的國家/地區的騙局報告網站</span><span class="sxs-lookup"><span data-stu-id="40cad-156">Submit a report to your country's scam reporting website</span></span>

<span data-ttu-id="40cad-157">騙局報告網站提供如何防止和避免詐騙的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="40cad-157">Scam reporting websites provide information about how to prevent and avoid scams.</span></span> <span data-ttu-id="40cad-158">當您是騙局的受害者時，也會提供要報告的機制。</span><span class="sxs-lookup"><span data-stu-id="40cad-158">They also provide mechanisms to report if you were victim of scam.</span></span>

- <span data-ttu-id="40cad-159">澳大利亞： [SCAMwatch](http://www.scamwatch.gov.au/)</span><span class="sxs-lookup"><span data-stu-id="40cad-159">Australia: [SCAMwatch](http://www.scamwatch.gov.au/)</span></span>

- <span data-ttu-id="40cad-160">加拿大：[加拿大反欺詐中心](http://www.antifraudcentre-centreantifraude.ca/)</span><span class="sxs-lookup"><span data-stu-id="40cad-160">Canada: [Canadian Anti-Fraud Centre](http://www.antifraudcentre-centreantifraude.ca/)</span></span>

- <span data-ttu-id="40cad-161">法國： [Agence nationale de la sécurité des systèmes d'information](http://www.ssi.gouv.fr/)</span><span class="sxs-lookup"><span data-stu-id="40cad-161">France: [Agence nationale de la sécurité des systèmes d'information](http://www.ssi.gouv.fr/)</span></span>

- <span data-ttu-id="40cad-162">德國： [Bundesamt Für Sicherheit in Der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span><span class="sxs-lookup"><span data-stu-id="40cad-162">Germany: [Bundesamt für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span></span>

- <span data-ttu-id="40cad-163">愛爾蘭： a [Garda Síochána](http://www.garda.ie/)</span><span class="sxs-lookup"><span data-stu-id="40cad-163">Ireland: [An Garda Síochána](http://www.garda.ie/)</span></span>

- <span data-ttu-id="40cad-164">紐西蘭：[使用者事務詐騙](http://www.consumeraffairs.govt.nz/scams)</span><span class="sxs-lookup"><span data-stu-id="40cad-164">New Zealand: [Consumer Affairs Scams](http://www.consumeraffairs.govt.nz/scams)</span></span>

- <span data-ttu-id="40cad-165">英國：[動作欺詐](http://www.actionfraud.police.uk/)</span><span class="sxs-lookup"><span data-stu-id="40cad-165">United Kingdom: [Action Fraud](http://www.actionfraud.police.uk/)</span></span>

- <span data-ttu-id="40cad-166">美國：[線上防護](http://www.onguardonline.gov/)</span><span class="sxs-lookup"><span data-stu-id="40cad-166">United States: [On Guard Online](http://www.onguardonline.gov/)</span></span>

<span data-ttu-id="40cad-167">如果您的國家/地區未列出，請諮詢您的當地或聯邦執法機構。</span><span class="sxs-lookup"><span data-stu-id="40cad-167">If your country isn't listed, ask your local or federal law enforcement agencies.</span></span>

### <a name="submit-email-messages-to-microsoft"></a><span data-ttu-id="40cad-168">將電子郵件提交至 Microsoft</span><span class="sxs-lookup"><span data-stu-id="40cad-168">Submit email messages to Microsoft</span></span>

<span data-ttu-id="40cad-169">您可以遵循[提交垃圾郵件、非垃圾郵件和網路釣魚詐騙訊息中的指示，向 Microsoft](https://docs.microsoft.com/microsoft-365/security/office-365-security/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis)報告包含勒索軟體的網路釣魚郵件，以進行分析。</span><span class="sxs-lookup"><span data-stu-id="40cad-169">You can report phishing message that contain ransomware by following the instructions in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](https://docs.microsoft.com/microsoft-365/security/office-365-security/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis).</span></span>

## <a name="see-also"></a><span data-ttu-id="40cad-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40cad-170">See also</span></span>

- [<span data-ttu-id="40cad-171">軟體</span><span class="sxs-lookup"><span data-stu-id="40cad-171">Ransomware</span></span>](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)

- [<span data-ttu-id="40cad-172">勒索軟體回應-支付或不支付費用？</span><span class="sxs-lookup"><span data-stu-id="40cad-172">Ransomware response—to pay or not to pay?</span></span>](https://www.microsoft.com/security/blog/2019/12/16/ransomware-response-to-pay-or-not-to-pay/)

- [<span data-ttu-id="40cad-173">Norsk Hydro 會以透明度回應勒索軟體攻擊</span><span class="sxs-lookup"><span data-stu-id="40cad-173">Norsk Hydro responds to ransomware attack with transparency</span></span>](https://www.microsoft.com/security/blog/2019/12/17/norsk-hydro-ransomware-attack-transparency/)

- [<span data-ttu-id="40cad-174">勒索軟體偵測和復原 OneDrive 中的檔案</span><span class="sxs-lookup"><span data-stu-id="40cad-174">Ransomware detection and recovering your files in OneDrive</span></span>](https://support.office.com/article/0d90ec50-6bfd-40f4-acc7-b8c12c73637f)

- [<span data-ttu-id="40cad-175">Microsoft Security 情報報告</span><span class="sxs-lookup"><span data-stu-id="40cad-175">Microsoft Security Intelligence Report</span></span>](https://www.microsoft.com/securityinsights/)

- [<span data-ttu-id="40cad-176">啟用或停用 Office 檔案中的宏</span><span class="sxs-lookup"><span data-stu-id="40cad-176">Enable or disable macros in Office files</span></span>](https://support.office.com/article/12b036fd-d140-4e74-b45e-16fed1a7e5c6)

- [<span data-ttu-id="40cad-177">EOP 和 Office 365 ATP 安全性的建議設定</span><span class="sxs-lookup"><span data-stu-id="40cad-177">Recommended settings for EOP and Office 365 ATP security</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp)

- [<span data-ttu-id="40cad-178">值得升級： Windows 10 上的下一代安全性會為2017中的勒索軟體的爆發，證實其可復原</span><span class="sxs-lookup"><span data-stu-id="40cad-178">A worthy upgrade: Next-gen security on Windows 10 proves resilient against ransomware outbreaks in 2017</span></span>](https://www.microsoft.com/security/blog/2018/01/10/a-worthy-upgrade-next-gen-security-on-windows-10-proves-resilient-against-ransomware-outbreaks-in-2017/)

- [<span data-ttu-id="40cad-179">沒有 ma，Samas：在此勒索軟體的 modus operandi 中有哪些？</span><span class="sxs-lookup"><span data-stu-id="40cad-179">No mas, Samas: What's in this ransomware's modus operandi?</span></span>](https://www.microsoft.com/security/blog/2016/03/17/no-mas-samas-whats-in-this-ransomwares-modus-operandi/)

- [<span data-ttu-id="40cad-180">Locky 惡意程式碼（幸運）以避免出現</span><span class="sxs-lookup"><span data-stu-id="40cad-180">Locky malware, lucky to avoid it</span></span>](https://www.microsoft.com/security/blog/2016/02/24/locky-malware-lucky-to-avoid-it/)

- [<span data-ttu-id="40cad-181">MSRT 2016 年7月： Cerber 勒索軟體</span><span class="sxs-lookup"><span data-stu-id="40cad-181">MSRT July 2016: Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/07/12/msrt-july-2016-cerber-ransomware/)

- [<span data-ttu-id="40cad-182">Cerberus 的三個機頭（如 Cerber）勒索軟體</span><span class="sxs-lookup"><span data-stu-id="40cad-182">The three heads of the Cerberus-like Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/03/09/the-three-heads-of-the-cerberus-like-cerber-ransomware/)

- [<span data-ttu-id="40cad-183">受（） Da Vinci 程式碼影響的 Troldesh 勒索軟體</span><span class="sxs-lookup"><span data-stu-id="40cad-183">Troldesh ransomware influenced by (the) Da Vinci code</span></span>](https://www.microsoft.com/security/blog/2016/07/13/troldesh-ransomware-influenced-by-the-da-vinci-code/)