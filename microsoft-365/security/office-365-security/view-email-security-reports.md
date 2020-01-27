---
title: 檢視安全性中的電子郵件安全性報告&amp;合規性中心 Compromised 使用者，加密、 威脅保護狀態，惡意程式碼偵測、 上方惡意程式碼、 垃圾郵件偵測傳送和接收電子郵件、 使用者所報告的郵件、 讀取的報告、 偵測、 安全性資料、 安全性資訊
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 01/16/2020
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection:
- M365-security-compliance
description: 了解如何尋找並使用您的組織電子郵件安全性報告。 安全性中的電子郵件安全性報告可用&amp;合規性中心。
ms.openlocfilehash: c44944c8f392b2df8cfe4b9e1741ba4b7ea13382
ms.sourcegitcommit: 5b8e9935fe7bfcb96b8f8356119ce23152bd16a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/16/2020
ms.locfileid: "41209948"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="e8365-104">檢視安全性與合規性中心內的電子郵件安全性報告</span><span class="sxs-lookup"><span data-stu-id="e8365-104">View email security reports in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="e8365-105">提供各種報告所[安全性&amp;合規性中心](https://protection.office.com)可協助您查看如何電子郵件安全性功能，例如 Office 365 中的反垃圾郵件、 反惡意程式碼及加密功能保護您的組織。</span><span class="sxs-lookup"><span data-stu-id="e8365-105">A variety of reports are available in the [Security &amp; Compliance Center](https://protection.office.com) to help you see how email security features, such as anti-spam, anti-malware, and encryption features in Office 365 are protecting your organization.</span></span> <span data-ttu-id="e8365-106">如果您有[必要權限](#what-permissions-are-needed-to-view-these-reports)，您可以檢視這些報告中的安全性&amp;合規性中心，移至**報表** \> **儀表板**。</span><span class="sxs-lookup"><span data-stu-id="e8365-106">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security &amp; Compliance Center by going to **Reports** \> **Dashboard**.</span></span>
  
![儀表板您瞭解進階威脅防護的運作方式](../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="e8365-108">您的電子郵件安全性報告包括下列：</span><span class="sxs-lookup"><span data-stu-id="e8365-108">Your email security reports include the following:</span></span>
- [<span data-ttu-id="e8365-109">危害使用者報告 (**新增 ！**)</span><span class="sxs-lookup"><span data-stu-id="e8365-109">Compromised Users report (**NEW!**)</span></span>](#compromised-users-report-new)
- [<span data-ttu-id="e8365-110">加密報表</span><span class="sxs-lookup"><span data-stu-id="e8365-110">Encryption report</span></span>](#encryption-report)
- [<span data-ttu-id="e8365-111">威脅防護狀態報告</span><span class="sxs-lookup"><span data-stu-id="e8365-111">Threat Protection Status report</span></span>](#threat-protection-status-report) 
- [<span data-ttu-id="e8365-112">惡意程式碼偵測報告</span><span class="sxs-lookup"><span data-stu-id="e8365-112">Malware Detections report</span></span>](#malware-detections-report) 
- [<span data-ttu-id="e8365-113">上方的惡意程式碼報告</span><span class="sxs-lookup"><span data-stu-id="e8365-113">Top Malware report</span></span>](#top-malware-report)
- [<span data-ttu-id="e8365-114">上方的寄件者和收件者的報告</span><span class="sxs-lookup"><span data-stu-id="e8365-114">Top Senders and Recipients report</span></span>](#top-senders-and-recipients-report)
- [<span data-ttu-id="e8365-115">詐騙偵測報告</span><span class="sxs-lookup"><span data-stu-id="e8365-115">Spoof Detections report</span></span>](#spoof-detections-report)
- [<span data-ttu-id="e8365-116">垃圾郵件偵測報告</span><span class="sxs-lookup"><span data-stu-id="e8365-116">Spam Detections report</span></span>](#spam-detections-report)
- [<span data-ttu-id="e8365-117">傳送和接收電子郵件報告</span><span class="sxs-lookup"><span data-stu-id="e8365-117">Sent and received email report</span></span>](#sent-and-received-email-report)
- [<span data-ttu-id="e8365-118">使用者回報郵件報告</span><span class="sxs-lookup"><span data-stu-id="e8365-118">User-reported messages report</span></span>](#user-reported-messages-report)


## <a name="compromised-users-report-new"></a><span data-ttu-id="e8365-119">危害使用者報告 (**新增 ！**)</span><span class="sxs-lookup"><span data-stu-id="e8365-119">Compromised Users report (**NEW!**)</span></span> 

<span data-ttu-id="e8365-120">這份報告，可與 Exchange Online Protection 中，任何人都顯示標示為 Suspicious 或受限的使用者，當帳戶輸入狀態指出的使用者帳戶的其中一個特別有用的資料可能有問題，或偶數的使用者帳戶的數目洩漏。</span><span class="sxs-lookup"><span data-stu-id="e8365-120">This report, available to anyone with Exchange Online Protection, shows the number of user accounts marked as Suspicious or Restricted users, data particularly useful as accounts enter either of the states that indicate the user account may be problematic, or even compromised.</span></span> <span data-ttu-id="e8365-121">經常使用與危害使用者報告可以找出突發性，以及偶數的趨勢，標示可疑或有限狀態，讓的證據可能會有此問題： 安全性與您的租用戶同等重要的帳戶中。</span><span class="sxs-lookup"><span data-stu-id="e8365-121">With frequent use, the Compromised User report can spot spikes, and even trends, in accounts marked in suspicious or restricted states, giving evidence there could be an issue with security and the wellness of your tenant.</span></span>

![遭入侵的使用者報告為它會出現在 Office 365。](../media/tp-threatProtectStatRpt-CompromisedUserRpt.png)

## <a name="encryption-report"></a><span data-ttu-id="e8365-123">加密報表</span><span class="sxs-lookup"><span data-stu-id="e8365-123">Encryption report</span></span>

<span data-ttu-id="e8365-124">**加密報表**顯示已加密，透過您的組織原則，或透過使用者控制項的電子郵件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e8365-124">The **Encryption report** shows information about email messages that were encrypted, either through your organization's policies, or through end-user controls.</span></span> <span data-ttu-id="e8365-125">貴組織的安全性小組可以找出模式並主動或套用調整機密電子郵件的原則，以使用此報告中資訊。</span><span class="sxs-lookup"><span data-stu-id="e8365-125">Your organization's security team can use information in this report to identify patterns and proactively apply or adjust policies for sensitive email messages.</span></span>

<span data-ttu-id="e8365-126">若要檢視此報告中，安全性 & 合規性中心，移至**報表** \> **儀表板** \> **加密報表**。</span><span class="sxs-lookup"><span data-stu-id="e8365-126">To view this report, in the Security & Compliance Center, go to **Reports** \> **Dashboard** \> **Encryption report**.</span></span>

![加密報表](../media/encryptionreport-defaultview.png) 

<span data-ttu-id="e8365-128">報告第一次開啟時，您會看到在過去七 （7） 天適用於電子郵件訊息的加密方法的相關資料。</span><span class="sxs-lookup"><span data-stu-id="e8365-128">When the report first opens, you'll see data about encryption methods used on email messages for the past seven (7) days.</span></span> <span data-ttu-id="e8365-129">您可以變更的日期範圍，會顯示在報告中的 [**篩選器**的畫面右上角的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e8365-129">You can change the date range and the details that are displayed in the report by clicking **Filters** in the upper right corner of the screen.</span></span>

![加密報告篩選器](../media/encryptionreport-filters.png)   

<span data-ttu-id="e8365-131">您也可以使用 [**依細分**] 功能表來檢視資料的加密範本 （或方法）。</span><span class="sxs-lookup"><span data-stu-id="e8365-131">You can also use the **Break down by** menu to view data by encryption template (or method).</span></span>

![加密方法或範本](../media/encryptionreport-breakdownby.png)

<span data-ttu-id="e8365-133">然後您可以使用 [**檢視資料**] 功能表變更檢視，以查看已加密郵件的頂端的五個收件者網域的計數。</span><span class="sxs-lookup"><span data-stu-id="e8365-133">And, you can use the **View data by** menu to change the view to see counts of encrypted messages to the top five recipient domains.</span></span>

![依據] 功能表的加密報表檢視資料](../media/encryptionreport-viewdataby.png)

<span data-ttu-id="e8365-135">在新的加密報告的彈性，您可以檢視趨勢，並採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="e8365-135">With the flexibility of the new Encryption report, you can view trends and take appropriate actions.</span></span> <span data-ttu-id="e8365-136">例如，如果您看到大量的使用者所加密的電子郵件，您可能要新增某些使用情況下，自動化加密加密原則。</span><span class="sxs-lookup"><span data-stu-id="e8365-136">For example, if you see a high number of email messages encrypted by users, you might want to add an encryption policy to automate encryption for certain use cases.</span></span> <span data-ttu-id="e8365-137">（若要取得的說明，請參閱[定義郵件流規則以加密 Office 365 中的電子郵件](../../compliance/define-mail-flow-rules-to-encrypt-email.md)）。另一個範例是，如果您有可用的加密範本的數字，但沒有人正在使用這些，您可能會瀏覽是否使用者需要訓練該功能。</span><span class="sxs-lookup"><span data-stu-id="e8365-137">(To get help with that, see [Define mail flow rules to encrypt email messages in Office 365](../../compliance/define-mail-flow-rules-to-encrypt-email.md).) As another example, if you have a number of encryption templates available but no one is using them, you might explore whether users need training for that feature.</span></span> 

<span data-ttu-id="e8365-138">使用此報告可讓您組織的安全性與合規性小組，以監視使用郵件加密的方式，以及是否進一步動作所需。</span><span class="sxs-lookup"><span data-stu-id="e8365-138">Use this report enables your organization's security and compliance team to monitor how message encryption is being used, and whether further actions are needed.</span></span> <span data-ttu-id="e8365-139">若要深入了解加密，請參閱[Office 365 中的電子郵件加密](../../compliance/email-encryption.md)。</span><span class="sxs-lookup"><span data-stu-id="e8365-139">To learn more about encryption, see [Email encryption in Office 365](../../compliance/email-encryption.md).</span></span>

## <a name="threat-protection-status-report"></a><span data-ttu-id="e8365-140">威脅防護狀態報告</span><span class="sxs-lookup"><span data-stu-id="e8365-140">Threat Protection Status report</span></span>

<span data-ttu-id="e8365-141">**威脅保護狀態**報表的智慧顯示的報告，已偵測並封鎖 Exchange Online protection 的惡意電子郵件。</span><span class="sxs-lookup"><span data-stu-id="e8365-141">The **Threat Protection Status** report is a smart report that shows malicious email that was detected and blocked by Exchange Online Protection.</span></span> <span data-ttu-id="e8365-142">這份報告可以用來檢視被識別為惡意程式碼的電子郵件或網路釣魚嘗試透過時間 （最多為 90 天），以及它可讓安全性系統管理員識別趨勢或判斷原則是否需要調整。</span><span class="sxs-lookup"><span data-stu-id="e8365-142">This report is useful for viewing email identified as malware or a phishing attempt over time (up to 90 days), and it enables security administrators to identify trends or determine whether policies need adjustments.</span></span>

> [!NOTE]
> <span data-ttu-id="e8365-143">威脅保護狀態報表是適用於擁有[Office 365 ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)或[Exchange Online Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/what-is-eop) (EOP); 客戶然而，ATP 客戶威脅保護狀態報表中顯示的資訊可能會包含不同資料比 EOP 客戶可能會看到的內容。</span><span class="sxs-lookup"><span data-stu-id="e8365-143">A Threat Protection Status report is available to customers who have either [Office 365 ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp) or [Exchange Online Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/what-is-eop) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see.</span></span> <span data-ttu-id="e8365-144">例如，EOP 客戶可以檢視電子郵件，但不是[在 SharePoint Online、 OneDrive 或 Microsoft Teams 中偵測到惡意檔案](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-for-spo-odb-and-teams)的相關資訊，ATP 特有功能中偵測到的惡意程式碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e8365-144">For example, EOP customers can view information about malware detected in email, but not information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-for-spo-odb-and-teams), an ATP-specific capability.</span></span> <span data-ttu-id="e8365-145">（[深入了解更多關於 ATP 報告](https://docs.microsoft.com/microsoft-365/security/office-365-security/view-reports-for-atp)）。</span><span class="sxs-lookup"><span data-stu-id="e8365-145">([Learn more about ATP reports](https://docs.microsoft.com/microsoft-365/security/office-365-security/view-reports-for-atp).)</span></span>
  
<span data-ttu-id="e8365-146">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，請移至**報表** \> **儀表板** \> **威脅保護狀態**。</span><span class="sxs-lookup"><span data-stu-id="e8365-146">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![威脅防護狀態報告](../media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
<span data-ttu-id="e8365-148">當您首次開啟威脅保護狀態報表時，報告顯示資料的過去 7 天的預設值;不過，您可以按一下 [**篩選**]，並 90 天的詳細資料變更日期範圍。</span><span class="sxs-lookup"><span data-stu-id="e8365-148">When you first open the Threat Protection Status report, the report shows data for the past seven days by default; however, you can click **Filters** and change the date range for up to 90 days of detail.</span></span> <span data-ttu-id="e8365-149">（如果您使用試用訂閱，您可能會受限於的 30 天的資料。）</span><span class="sxs-lookup"><span data-stu-id="e8365-149">(If you are using a trial subscription, you might be limited to 30 days' of data.)</span></span>

<span data-ttu-id="e8365-150">這份報告是適用於檢視的效率和影響貴組織的[Exchange Online Protection 功能](https://docs.microsoft.com/microsoft-365/security/office-365-security/eop-features)，以及更長期的趨勢。</span><span class="sxs-lookup"><span data-stu-id="e8365-150">This report is useful for viewing the effectiveness and impact of your organization's [Exchange Online Protection features](https://docs.microsoft.com/microsoft-365/security/office-365-security/eop-features), and for longer-term trending.</span></span> 
  
![威脅保護狀態報告的篩選器](../media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
<span data-ttu-id="e8365-152">您也可以選擇是否要檢視的電子郵件被識別為惡意的資料，識別為網路釣魚嘗試，電子郵件或電子郵件被識別為包含惡意程式碼。</span><span class="sxs-lookup"><span data-stu-id="e8365-152">You can also choose whether to view data for email identified as malicious, email identified as a phishing attempts, or email identified as containing malware.</span></span>
  
![威脅保護狀態報表檢視選項](../media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a><span data-ttu-id="e8365-154">惡意程式碼偵測報告</span><span class="sxs-lookup"><span data-stu-id="e8365-154">Malware Detections report</span></span>

<span data-ttu-id="e8365-155">**惡意程式碼偵測**報告 」 顯示為包含組織的惡意程式碼偵測到多少的內送和外寄郵件。</span><span class="sxs-lookup"><span data-stu-id="e8365-155">The **Malware Detections** report shows how many incoming and outgoing messages were detected as containing malware for your organization.</span></span> 
  
<span data-ttu-id="e8365-156">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，請移至**報表** \> **儀表板** \> **惡意程式碼偵測**。</span><span class="sxs-lookup"><span data-stu-id="e8365-156">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Malware Detections**.</span></span>
  
![惡意程式碼偵測] 報告範例](../media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
<span data-ttu-id="e8365-158">類似其他報表，例如[威脅保護狀態報表](#threat-protection-status-report)，報告預設會顯示資料的過去 7 天。</span><span class="sxs-lookup"><span data-stu-id="e8365-158">Similar to other reports, like the [Threat Protection Status report](#threat-protection-status-report), the report displays data for the past seven days by default.</span></span> <span data-ttu-id="e8365-159">不過，您可以選擇要變更的日期範圍**篩選器**。</span><span class="sxs-lookup"><span data-stu-id="e8365-159">However, you can choose **Filters** to change the date range.</span></span> 
  
## <a name="top-malware-report"></a><span data-ttu-id="e8365-160">上方的惡意程式碼報告</span><span class="sxs-lookup"><span data-stu-id="e8365-160">Top Malware report</span></span>

<span data-ttu-id="e8365-161">**Top 惡意程式碼**報告 」 顯示各種不同的[Exchange Online](https://docs.microsoft.com/microsoft-365/security/office-365-security/eop-features)所偵測到的惡意程式碼。</span><span class="sxs-lookup"><span data-stu-id="e8365-161">The **Top Malware** report shows the various kinds of malware that was detected by [Exchange Online](https://docs.microsoft.com/microsoft-365/security/office-365-security/eop-features).</span></span> 
  
<span data-ttu-id="e8365-162">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，請移至**報表** \> **儀表板** \> **頂端惡意程式碼**。</span><span class="sxs-lookup"><span data-stu-id="e8365-162">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Top Malware**.</span></span>
  
![SCC-EOP 上方惡意程式碼](../media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
<span data-ttu-id="e8365-164">當您將滑鼠停留在圓形圖扇形擴展時，您可以看到的惡意程式碼和為具有該惡意程式碼偵測到多少郵件類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8365-164">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>
  
<span data-ttu-id="e8365-165">按一下 （或點選），在新的瀏覽器視窗，您可以在哪裡取得報告的詳細的檢視中開啟報表。</span><span class="sxs-lookup"><span data-stu-id="e8365-165">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![這份報告顯示上方的惡意程式碼偵測到您的組織](../media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
<span data-ttu-id="e8365-167">下方圖表中，您會看到偵測到惡意程式碼和為具有該惡意程式碼偵測到多少郵件的清單。</span><span class="sxs-lookup"><span data-stu-id="e8365-167">Below the chart, you'll see a list of detected malware and how many messages were detected as having that malware.</span></span>
  
## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="e8365-168">上方的寄件者和收件者的報告</span><span class="sxs-lookup"><span data-stu-id="e8365-168">Top Senders and Recipients report</span></span>

<span data-ttu-id="e8365-169">**Top 寄件者和收件者**的報告是顯示您上方的電子郵件寄件者圓形圖帶有子橫條圖。</span><span class="sxs-lookup"><span data-stu-id="e8365-169">The **Top Senders and Recipients** report is a pie chart showing your top email senders.</span></span> 
  
<span data-ttu-id="e8365-170">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，請移至**報表** \> **儀表板** \> **頂端寄件者和收件者**。</span><span class="sxs-lookup"><span data-stu-id="e8365-170">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Top Senders and Recipients**.</span></span>
  
![若要檢視此報告中，安全性&amp;合規性中心，移至報表\>儀表板\>頂端寄件者和收件者](../media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
<span data-ttu-id="e8365-172">當您將滑鼠停留在圓形圖扇形擴展時，您可以看到傳送或接收郵件計數。</span><span class="sxs-lookup"><span data-stu-id="e8365-172">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>
  
<span data-ttu-id="e8365-173">按一下 （或點選），在新的瀏覽器視窗，您可以在哪裡取得報告的詳細的檢視中開啟報表。</span><span class="sxs-lookup"><span data-stu-id="e8365-173">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="e8365-174">用於**顯示資料**] 清單中選擇要檢視的主要寄件者，接收器、 垃圾郵件收件者、 惡意程式碼收件者的資料。</span><span class="sxs-lookup"><span data-stu-id="e8365-174">Use the **Show data for** list to choose whether to view data for top senders, receivers, spam recipients, and malware recipients.</span></span> <span data-ttu-id="e8365-175">您也可以查看誰收到偵測到[Exchange Online](https://docs.microsoft.com/microsoft-365/security/office-365-security/what-is-eop)protection 的惡意程式碼。</span><span class="sxs-lookup"><span data-stu-id="e8365-175">You can also see who received malware that was detected by [Exchange Online Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/what-is-eop).</span></span> 
  
![使用 [顯示資料的清單以檢視特定的資訊](../media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
<span data-ttu-id="e8365-177">下方圖表中，您會看到誰上方的電子郵件寄件者或收件者，以及傳送或接收的指定的時間期間內郵件計數。</span><span class="sxs-lookup"><span data-stu-id="e8365-177">Below the chart, you'll see who the top email senders or recipients were, along with a count of messages sent or received for the given time period.</span></span>
  
## <a name="spoof-detections-report"></a><span data-ttu-id="e8365-178">詐騙偵測報告</span><span class="sxs-lookup"><span data-stu-id="e8365-178">Spoof Detections report</span></span>

<span data-ttu-id="e8365-179">**詐騙偵測**報告 」 可顯示已偵測到多少詐騙郵件，以及那些標籤哪些項目已被視為 「 良好 」 （詐騙郵件為合法的商業原因而完成）。</span><span class="sxs-lookup"><span data-stu-id="e8365-179">The **Spoof Detections** report shows how many spoof mail messages were detected, and of those, which ones were considered "good" (spoof mail done for legitimate business reasons).</span></span> 
  
<span data-ttu-id="e8365-180">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，請移至**報表** \> **儀表板** \> **詐騙郵件**。</span><span class="sxs-lookup"><span data-stu-id="e8365-180">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Spoof Mail**.</span></span>
  
![安全性&amp;合規性中心，移至報表\>儀表板\>詐騙郵件](../media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
<span data-ttu-id="e8365-182">當您將滑鼠停留一天圖表中時，您可以看到多少詐騙郵件是透過。</span><span class="sxs-lookup"><span data-stu-id="e8365-182">When you hover over a day in the chart, you can see how many spoof mail messages came through.</span></span>
  
<span data-ttu-id="e8365-183">按一下 （或點選），在新的瀏覽器視窗，您可以在哪裡取得報告的詳細的檢視中開啟報表。</span><span class="sxs-lookup"><span data-stu-id="e8365-183">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span> <span data-ttu-id="e8365-184">若要深入了解反詐騙保護，請參閱[在 Office 365 中的反詐騙保護](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spoofing-protection)。</span><span class="sxs-lookup"><span data-stu-id="e8365-184">To learn more about anti-spoof protection, see [Anti-spoofing protection in Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spoofing-protection).</span></span>
  
## <a name="spam-detections-report"></a><span data-ttu-id="e8365-185">垃圾郵件偵測報告</span><span class="sxs-lookup"><span data-stu-id="e8365-185">Spam Detections report</span></span>

<span data-ttu-id="e8365-186">[**垃圾郵件偵測**] 報告顯示封鎖的 Exchange Online 中的垃圾郵件內容。</span><span class="sxs-lookup"><span data-stu-id="e8365-186">The **Spam Detections** report shows all the spam content blocked by Exchange Online.</span></span> <span data-ttu-id="e8365-187">郵件會計算每封郵件，而不是個別寄件者。</span><span class="sxs-lookup"><span data-stu-id="e8365-187">Messages are counted per message, and not per recipient.</span></span> <span data-ttu-id="e8365-188">例如，如果電子郵件已傳送給組織中的 100 收件者，它就會計算成一封郵件。</span><span class="sxs-lookup"><span data-stu-id="e8365-188">For example, if an email message was sent to 100 recipients in your organization, it is counted as one message.</span></span>
  
<span data-ttu-id="e8365-189">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，請移至**報表** \> **儀表板** \> **垃圾郵件偵測**。</span><span class="sxs-lookup"><span data-stu-id="e8365-189">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Spam Detections**.</span></span>
  
![若要檢視此報告中，安全性&amp;合規性中心，移至報表\>儀表板\>EOP 垃圾郵件偵測](../media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
<span data-ttu-id="e8365-191">當您將滑鼠停留一天圖表中時，您可以看到多少個項目遭到封鎖該日，以及如何分類項目。</span><span class="sxs-lookup"><span data-stu-id="e8365-191">When you hover over a day in the chart, you can see how many items were blocked that day, as well as how those items are categorized.</span></span> <span data-ttu-id="e8365-192">例如，您可以看到多少垃圾郵件進行篩選，以及多少個項目是來自封鎖的網際網路通訊協定 (IP) 位址。</span><span class="sxs-lookup"><span data-stu-id="e8365-192">For example, you can see how many spam messages were filtered, and how many items came from a blocked Internet Protocol (IP) address.</span></span>
  
<span data-ttu-id="e8365-193">按一下 （或點選），在新的瀏覽器視窗，您可以在哪裡取得報告的詳細的檢視中開啟報表。</span><span class="sxs-lookup"><span data-stu-id="e8365-193">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![[垃圾郵件偵測] 報告會告訴您如何許多垃圾郵件被封鎖或篩選出](../media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
<span data-ttu-id="e8365-195">下方圖表中，您會看到所偵測到的垃圾郵件項目清單。</span><span class="sxs-lookup"><span data-stu-id="e8365-195">Below the chart, you'll see a list of spam items that were detected.</span></span> <span data-ttu-id="e8365-196">選取要檢視其他資訊，例如垃圾郵件項目已輸入或輸出、 其郵件識別碼，以及其收件者的項目。</span><span class="sxs-lookup"><span data-stu-id="e8365-196">Select an item to view additional information, such as whether the spam item was inbound or outbound, its message ID, and its recipient.</span></span> <span data-ttu-id="e8365-197">若要深入了解反垃圾郵件保護，請參閱[Office 365 電子郵件反垃圾郵件保護](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-and-anti-malware-protection)。</span><span class="sxs-lookup"><span data-stu-id="e8365-197">To learn more about anti-spam protection, see [Office 365 email anti-spam protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-and-anti-malware-protection).</span></span>
  
## <a name="sent-and-received-email-report"></a><span data-ttu-id="e8365-198">傳送和接收電子郵件報告</span><span class="sxs-lookup"><span data-stu-id="e8365-198">Sent and received email report</span></span>

<span data-ttu-id="e8365-199">**已傳送和接收的電子郵件**報告是智慧報表顯示資訊內送和外寄電子郵件，包括垃圾郵件偵測、 惡意程式碼，以及電子郵件被識別為 「 良好 」。</span><span class="sxs-lookup"><span data-stu-id="e8365-199">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> 
  
<span data-ttu-id="e8365-200">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，請移至**報表** \> **儀表板** \> **已傳送和接收的電子郵件**。</span><span class="sxs-lookup"><span data-stu-id="e8365-200">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Sent and received email**.</span></span>
  
![若要檢視此報告中，安全性&amp;合規性中心，移至報表\>儀表板\>已傳送和接收的電子郵件](../media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
<span data-ttu-id="e8365-202">當您將滑鼠停留一天圖表中時，您可以看到多少郵件的來源，以及這些郵件分類的方式。</span><span class="sxs-lookup"><span data-stu-id="e8365-202">When you hover over a day in the chart, you can see how many messages came in, and how those messages are categorized.</span></span> <span data-ttu-id="e8365-203">例如，您可以看到為包含惡意程式碼，偵測到多少郵件和多少被判定為垃圾郵件。</span><span class="sxs-lookup"><span data-stu-id="e8365-203">For example, you can see how many messages were detected as containing malware, and how many were identified as spam.</span></span>
  
<span data-ttu-id="e8365-204">按一下 （或點選），在新的瀏覽器視窗，您可以在哪裡取得報告的詳細的檢視中開啟報表。</span><span class="sxs-lookup"><span data-stu-id="e8365-204">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="e8365-205">您可以使用**細分的**清單檢視類型，或方向 （內送和外寄） 的資訊。</span><span class="sxs-lookup"><span data-stu-id="e8365-205">You can use the **Break down by** list to view information by type or by direction (incoming and outgoing).</span></span> 
  
![使用 [自動換行向下依據] 清單來檢視資訊類型或方向](../media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
<span data-ttu-id="e8365-207">下方圖表中，您會看到一份電子郵件類別，例如**GoodMail**、 **SpamContentFiltered**，等等。</span><span class="sxs-lookup"><span data-stu-id="e8365-207">Below the chart, you'll see a list of email categories, such as **GoodMail**, **SpamContentFiltered**, and so on.</span></span> <span data-ttu-id="e8365-208">選取要檢視其他資訊，例如惡意程式碼，所採取的動作和是否電子郵件類別是傳入或傳出。</span><span class="sxs-lookup"><span data-stu-id="e8365-208">Select a category to view additional information, such as actions that were taken for malware, and whether email was incoming or outgoing.</span></span>
  
![此報表會告訴您有關反惡意程式碼、 反垃圾郵件和其他郵件偵測](../media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)

<span data-ttu-id="e8365-210">若要深入了解電子郵件智慧，請參閱[在 Office 365 中的郵件流程情報](https://docs.microsoft.com/microsoft-365/security/office-365-security/mail-flow-intelligence-in-office-365)。</span><span class="sxs-lookup"><span data-stu-id="e8365-210">To learn more about email intelligence, see [Mail flow intelligence in Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/mail-flow-intelligence-in-office-365).</span></span>
  
## <a name="user-reported-messages-report"></a><span data-ttu-id="e8365-211">使用者回報郵件報告</span><span class="sxs-lookup"><span data-stu-id="e8365-211">User-reported messages report</span></span>

<span data-ttu-id="e8365-212">**使用者回報郵件**報告會顯示使用者會回報為垃圾郵件、 網路釣魚企圖或良好郵件[報告訊息增益集](https://docs.microsoft.com/microsoft-365/security/office-365-security/enable-the-report-message-add-in)使用的電子郵件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e8365-212">The **User-reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](https://docs.microsoft.com/microsoft-365/security/office-365-security/enable-the-report-message-add-in).</span></span>
  
<span data-ttu-id="e8365-213">詳細資料可供每則訊息，包括傳遞的原因，這類垃圾郵件原則的例外狀況或組織設定的郵件流程規則。</span><span class="sxs-lookup"><span data-stu-id="e8365-213">Details are available for each message, including the delivery reason, such a spam policy exception or mail flow rule configured for your organization.</span></span> <span data-ttu-id="e8365-214">若要檢視的詳細資訊，請在使用者報告] 清單中，選取項目，然後檢視資訊**摘要**和**詳細資料**] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="e8365-214">To view details, select an item in the user-reports list, and then view the information on the **Summary** and **Details** tabs.</span></span> 
  
![User-Reported 郵件報告顯示標示為垃圾郵件、 非垃圾郵件或網路釣魚嘗試的郵件使用者。](../media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
<span data-ttu-id="e8365-216">若要檢視此報告中，在[安全性&amp;合規性中心](https://protection.office.com)，執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="e8365-216">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), do one of the following:</span></span>
  
- <span data-ttu-id="e8365-217">移至**威脅管理，** \> **儀表板** \> **使用者報告的郵件**。</span><span class="sxs-lookup"><span data-stu-id="e8365-217">Go to **Threat management** \> **Dashboard** \> **User-reported messages**.</span></span>
    
- <span data-ttu-id="e8365-218">移至**威脅管理，** \> **檢閱** \> **使用者報告的郵件**。</span><span class="sxs-lookup"><span data-stu-id="e8365-218">Go to **Threat management** \> **Review** \> **User-reported messages**.</span></span>
    
![安全性&amp;合規性中心，選擇 [威脅管理\>檢閱\>使用者所報告的郵件](../media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> <span data-ttu-id="e8365-220">在順序，如使用者回報郵件報告能夠正常運作，**必須先開啟稽核記錄功能**適用於 Office 365 環境。</span><span class="sxs-lookup"><span data-stu-id="e8365-220">In order for the User-reported messages report to work correctly, **audit logging must be turned on** for your Office 365 environment.</span></span> <span data-ttu-id="e8365-221">這項工作通常是由在 Exchange Online 中獲派稽核記錄角色的人員完成。</span><span class="sxs-lookup"><span data-stu-id="e8365-221">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="e8365-222">如需詳細資訊，請參閱[開啟或關閉 Office 365 稽核記錄搜尋](https://docs.microsoft.com/microsoft-365/compliance/turn-audit-log-search-on-or-off)。</span><span class="sxs-lookup"><span data-stu-id="e8365-222">For more information, see [Turn Office 365 audit log search on or off](https://docs.microsoft.com/microsoft-365/compliance/turn-audit-log-search-on-or-off).</span></span> 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="e8365-223">若要檢視這些報告需要哪些權限？</span><span class="sxs-lookup"><span data-stu-id="e8365-223">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="e8365-224">若要檢視及使用本文中所述的報告**您必須具有適當的角色指派給這兩種安全性&amp;規範中心和 Exchange 系統管理中心**。</span><span class="sxs-lookup"><span data-stu-id="e8365-224">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange admin center**.</span></span>

- <span data-ttu-id="e8365-225">針對「安全性與合規性中心」，您必須受指派下列其中一個角色：</span><span class="sxs-lookup"><span data-stu-id="e8365-225">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="e8365-226">組織管理</span><span class="sxs-lookup"><span data-stu-id="e8365-226">Organization Management</span></span>
    - <span data-ttu-id="e8365-227">安全性系統管理員 (這可以在 Azure Active Directory 系統管理中心中指派 ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="e8365-227">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>
    - <span data-ttu-id="e8365-228">安全性讀取者</span><span class="sxs-lookup"><span data-stu-id="e8365-228">Security Reader</span></span>

- <span data-ttu-id="e8365-229">針對 Exchange Online，您必須在 Exchange 系統管理中心 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 或 PowerShell Cmdlet (請參閱 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) 受指派下列其中一個角色：</span><span class="sxs-lookup"><span data-stu-id="e8365-229">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="e8365-230">組織管理</span><span class="sxs-lookup"><span data-stu-id="e8365-230">Organization Management</span></span>
    - <span data-ttu-id="e8365-231">僅檢視組織管理</span><span class="sxs-lookup"><span data-stu-id="e8365-231">View-only Organization Management</span></span>
    - <span data-ttu-id="e8365-232">僅檢視收件者角色</span><span class="sxs-lookup"><span data-stu-id="e8365-232">View-Only Recipients role</span></span>
    - <span data-ttu-id="e8365-233">合規性管理</span><span class="sxs-lookup"><span data-stu-id="e8365-233">Compliance Management</span></span>

<span data-ttu-id="e8365-234">若要深入了解，請參閱下列資源：</span><span class="sxs-lookup"><span data-stu-id="e8365-234">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="e8365-235">Office 365 安全性與合規性中心權限</span><span class="sxs-lookup"><span data-stu-id="e8365-235">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center)

- [<span data-ttu-id="e8365-236">Exchange Online 中的功能權限</span><span class="sxs-lookup"><span data-stu-id="e8365-236">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="e8365-237">如果報表不顯示資料？</span><span class="sxs-lookup"><span data-stu-id="e8365-237">What if the reports aren't showing data?</span></span>

<span data-ttu-id="e8365-238">如果您不在報表中看到的資料，請仔細檢查您的原則已正確設定。</span><span class="sxs-lookup"><span data-stu-id="e8365-238">If you are not seeing data in your reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="e8365-239">若要深入了解，請參閱[防範 Office 365 中的威脅](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats)。</span><span class="sxs-lookup"><span data-stu-id="e8365-239">To learn more, see [Protect against threats in Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="e8365-240">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8365-240">Related topics</span></span>

[<span data-ttu-id="e8365-241">Office 365 電子郵件的反垃圾郵件保護</span><span class="sxs-lookup"><span data-stu-id="e8365-241">Office 365 Email Anti-Spam Protection</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-and-anti-malware-protection)
  
[<span data-ttu-id="e8365-242">報告和 Office 365 安全性的深入解析&amp;合規性中心</span><span class="sxs-lookup"><span data-stu-id="e8365-242">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/reports-and-insights-in-security-and-compliance)
  
[<span data-ttu-id="e8365-243">建立報表排程安全性&amp;合規性中心</span><span class="sxs-lookup"><span data-stu-id="e8365-243">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/create-a-schedule-for-a-report)
  
[<span data-ttu-id="e8365-244">設定及下載自訂報告中的安全性&amp;合規性中心</span><span class="sxs-lookup"><span data-stu-id="e8365-244">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/set-up-and-download-a-custom-report)
  
