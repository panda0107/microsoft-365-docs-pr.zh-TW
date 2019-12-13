---
title: 調查 Microsoft 威脅防護中的事件
description: 分析與裝置、使用者和信箱相關的事件。
keywords: 事件,電腦,裝置,使用者,身分識別,郵件,電子郵件,信箱,調查,圖形,證據
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 716feb3317989ebcc89593c89d05a6717b4ca0ee
ms.sourcegitcommit: 0c9c28a87201c7470716216d99175356fb3d1a47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/09/2019
ms.locfileid: "39910980"
---
# <a name="investigate-incidents-in-microsoft-threat-protection"></a><span data-ttu-id="039d1-104">調查 Microsoft 威脅防護中的事件</span><span class="sxs-lookup"><span data-stu-id="039d1-104">Investigate incidents in Microsoft Threat Protection</span></span>

<span data-ttu-id="039d1-105">**適用於：**</span><span class="sxs-lookup"><span data-stu-id="039d1-105">**Applies to:**</span></span>
- <span data-ttu-id="039d1-106">Microsoft 威脅防護</span><span class="sxs-lookup"><span data-stu-id="039d1-106">Microsoft Threat Protection</span></span>

[!include[Prerelease information](prerelease.md)]


<span data-ttu-id="039d1-107">Microsoft 威脅防護可彙總各種裝置、使用者和信箱的所有相關警示、資產、調查和證據，讓您全面了解整個攻擊範圍。</span><span class="sxs-lookup"><span data-stu-id="039d1-107">Microsoft Threat Protection aggregates all related alerts, assets, investigations and evidence from across your devices, users, and mailboxes to give you a comprehensive look into the entire breadth of an attack.</span></span> 

<span data-ttu-id="039d1-108">調查影響您網路的警示、了解其含義，並彙整與該事件相關聯的證據，以便設計有效的修復方案。</span><span class="sxs-lookup"><span data-stu-id="039d1-108">Investigate the alerts that affect your network, understand what they mean, and collate evidence associated with the incidents so that you can devise an effective remediation plan.</span></span> 

## <a name="investigate-an-incident"></a><span data-ttu-id="039d1-109">調查事件</span><span class="sxs-lookup"><span data-stu-id="039d1-109">Investigate an incident</span></span>

1. <span data-ttu-id="039d1-110">從事件佇列中選取事件。</span><span class="sxs-lookup"><span data-stu-id="039d1-110">Select an incident from the incident queue.</span></span> <BR> <span data-ttu-id="039d1-111">這會開啟側邊面板，並預覽重要資訊，例如狀態、嚴重性、類別和受影響的實體。</span><span class="sxs-lookup"><span data-stu-id="039d1-111">This opens a side panel and gives a preview of important information such as status, severity, categories, and the impacted entities.</span></span>

    ![事件側邊面板影像](../images/incident-side-panel.png)

2. <span data-ttu-id="039d1-113">選取**開啟事件頁面**。</span><span class="sxs-lookup"><span data-stu-id="039d1-113">Select **Open incident page**.</span></span> <BR> <span data-ttu-id="039d1-114">這會開啟事件頁面，您可以在此找到更多資訊事件詳細資料、註解和動作、索引標籤 (概觀、警示、裝置、使用者、調查、證據)。</span><span class="sxs-lookup"><span data-stu-id="039d1-114">This opens the incident page where you'll find more information incident details, comments and actions, tabs (overview, alerts, devices, users, investigations, evidence).</span></span>

3. <span data-ttu-id="039d1-115">檢閱涉及事件的警示、裝置、使用者和其他實體。</span><span class="sxs-lookup"><span data-stu-id="039d1-115">Review the alerts, devices, users, other entities involved in the incident.</span></span>

## <a name="incident-overview"></a><span data-ttu-id="039d1-116">事件概觀</span><span class="sxs-lookup"><span data-stu-id="039d1-116">Incident overview</span></span> 
<span data-ttu-id="039d1-117">概觀頁面可讓您一覽無遺地了解事件的主要內容。</span><span class="sxs-lookup"><span data-stu-id="039d1-117">The overview page gives you a snapshot glance into the top things to notice about the incident.</span></span>


![事件概觀頁面影像](../images/incidents-overview.png)


<span data-ttu-id="039d1-119">攻擊類別為您提供視覺和數字檢視，以了解這項攻擊對終止鏈的進展狀況。</span><span class="sxs-lookup"><span data-stu-id="039d1-119">The attack categories give you visual and numeric view of how advanced the attack has progressed against the kill chain.</span></span> <span data-ttu-id="039d1-120">如同其他 Microsoft 安全性產品，Microsoft 威脅防護保護與 [MITRE ATT&CK&trade;](https://attack.mitre.org/) 架構一致。</span><span class="sxs-lookup"><span data-stu-id="039d1-120">As with other Microsoft security products, Microsoft Threat Protection is aligned to the [MITRE ATT&CK&trade;](https://attack.mitre.org/) framework.</span></span> 

<span data-ttu-id="039d1-121">範圍區段會顯示屬於此事件中影響最大的資產清單。</span><span class="sxs-lookup"><span data-stu-id="039d1-121">The scope section gives you a list of top impacted assets that are part of this incident.</span></span> <span data-ttu-id="039d1-122">如果關於此資產的特定資訊，例如風險層級、調查優先順序以及資產上的任何標記，本區段也將會顯示這項資訊。</span><span class="sxs-lookup"><span data-stu-id="039d1-122">If there is specific information regarding this asset, such as risk level, investigation priority as well as any tagging on the assets this will also surface in this section.</span></span>

<span data-ttu-id="039d1-123">警示時間表可讓您先預覽警示發生的時間順序，以及這些警示與此事件相關聯的原因。</span><span class="sxs-lookup"><span data-stu-id="039d1-123">The alerts timeline provides a sneak peek into the chronological order in which the alerts occurred, as well as the reasons that these alerts linked to this incident.</span></span>

<span data-ttu-id="039d1-124">最後，證據區段提供事件中包含多少不同成品以及其修復狀態摘要，因此您可以立即識別是否需要採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="039d1-124">And last - the evidence section provides a summary of how many different artifacts were included in the incident and their remediation status, so you can immediately identify if any action is needed on your end.</span></span> 

<span data-ttu-id="039d1-125">此概觀藉由提供您應該注意的事件主要特性深入解析，可協助對事件進行初步分級。</span><span class="sxs-lookup"><span data-stu-id="039d1-125">This overview can assist in the initial triage of the incident by providing insight to the top characteristics of the incident that you should be aware of.</span></span> 


## <a name="alerts"></a><span data-ttu-id="039d1-126">警示</span><span class="sxs-lookup"><span data-stu-id="039d1-126">Alerts</span></span> 
<span data-ttu-id="039d1-127">您可以檢視與該事件相關的所有警示，以及與該事件相關的其他資訊，例如嚴重性、涉及警示的實體、警示來源 (Azure ATP、Microsoft Defender ATP、Office 365 ATP)，以及連結在一起的原因。</span><span class="sxs-lookup"><span data-stu-id="039d1-127">You can view all the alerts related to the incident and other information about them such as severity, entities that were involved in the alert, the source of the alerts (Azure ATP, Microsoft Defender ATP , Office  365 ATP) and the reason they were linked together.</span></span> 

![事件警示頁面影像](../images/incident-alerts.png)

<span data-ttu-id="039d1-129">根據預設，警示會依時間順序排列，讓您首先檢視攻擊如何隨時間推移而進行。</span><span class="sxs-lookup"><span data-stu-id="039d1-129">By default, the alerts are ordered chronologically, to allow you to first view how the attack played out over time.</span></span> <span data-ttu-id="039d1-130">按一下每個警示，就會引導您至相關警示頁面，您可以在該頁面中深入調查警示。</span><span class="sxs-lookup"><span data-stu-id="039d1-130">Clicking on each alert will lead you to the relevant alert page where you can conduct an in depth investigation of that alert.</span></span> 

## <a name="devices"></a><span data-ttu-id="039d1-131">裝置</span><span class="sxs-lookup"><span data-stu-id="039d1-131">Devices</span></span> 
<span data-ttu-id="039d1-132">裝置索引標籤會列出所有顯示事件相關警示的裝置。</span><span class="sxs-lookup"><span data-stu-id="039d1-132">The devices tab lists all the devices where alerts related to the incident are seen.</span></span> 

<span data-ttu-id="039d1-133">按一下執行攻擊的電腦名稱，引導您至其 [電腦] 頁面，您可以其中查看觸發的警示，以及提供的相關事件，以便輕鬆調查。</span><span class="sxs-lookup"><span data-stu-id="039d1-133">Clicking the name of the machine where the attack was conducted navigates you to its Machine page where you can see alerts that were triggered on it and related events provided to ease investigation.</span></span> 

![事件機器索引標籤影像](../images/incident-machines.png)

<span data-ttu-id="039d1-135">選取 [時間表] 索引標籤可讓您捲動電腦時程表，並以時間順序檢視電腦上觀測到的所有活動和行為，以及散布其中的警示。</span><span class="sxs-lookup"><span data-stu-id="039d1-135">Selecting the Timeline tab enables you to scroll through the machine timeline and view all events and behaviors observed on the machine in chronological order, interspersed with the alerts raised.</span></span> 


## <a name="users"></a><span data-ttu-id="039d1-136">使用者</span><span class="sxs-lookup"><span data-stu-id="039d1-136">Users</span></span> 
<span data-ttu-id="039d1-137">查看已識別為指定事件一部分或與相關的使用者。</span><span class="sxs-lookup"><span data-stu-id="039d1-137">See users that have been identified to be part of, or related to a given incident.</span></span> 

<span data-ttu-id="039d1-138">按一下使用者名稱以引導您至使用者的雲端 App 安全性頁面，可在頁面中執行進一步的調查。</span><span class="sxs-lookup"><span data-stu-id="039d1-138">Clicking the username navigates you to the user's Cloud App Security page where further investigation can be conducted.</span></span>


![事件使用者索引標籤影像](../images/incident-users.png)

## <a name="mailboxes"></a><span data-ttu-id="039d1-140">信箱</span><span class="sxs-lookup"><span data-stu-id="039d1-140">Mailboxes</span></span>
<span data-ttu-id="039d1-141">調查已識別為指定事件一部分或與相關的信箱。</span><span class="sxs-lookup"><span data-stu-id="039d1-141">Investigate mailboxes that's been identified to be part of, or related to an incident.</span></span> <span data-ttu-id="039d1-142">若要執行進一步調查工作，選取與郵件相關的警示，將會開啟 Office 365 進階威脅防護，便可進行修復。</span><span class="sxs-lookup"><span data-stu-id="039d1-142">To do further investigative work, selecting the mail related alert will open Office 365 Advanced Threat Protection where you can take remediation actions.</span></span>


![事件信箱索引標籤影像](../images/incident-mailboxes.png)

## <a name="investigations"></a><span data-ttu-id="039d1-144">調查</span><span class="sxs-lookup"><span data-stu-id="039d1-144">Investigations</span></span>
<span data-ttu-id="039d1-145">選取 [調查] \*\*\*\* 即可在此事件中透過警示查看所有觸發的自動化調查內容。</span><span class="sxs-lookup"><span data-stu-id="039d1-145">Select **Investigations** to see all the automated investigation striggered by alerts in this incident.</span></span> <span data-ttu-id="039d1-146">調查將執行修復動作或等待分析人員核准動作，具體取決於您如何設定自動化調查以在 Microsoft Defender ATP 和 Office 365 進階威脅防護中執行。</span><span class="sxs-lookup"><span data-stu-id="039d1-146">The investigations will perform remediation actions or wait for analyst approval of actions, depending on how you configured your automated investigations to run in Microsoft Defender ATP and Office 365 Advanced Threat Protection.</span></span>

![事件調查索引標籤影像](../images/incident-investigations.png)


<span data-ttu-id="039d1-148">選取調查以瀏覽至 [調查詳細資料] 頁面，取得調查和修復狀態的完整資訊。</span><span class="sxs-lookup"><span data-stu-id="039d1-148">Select an investigation to navigate to the Investigation details page to get full information on the investigation and remediation status.</span></span> <span data-ttu-id="039d1-149">如果有任何待核准的動作為調查的一部分，將顯示在 [擱置中的動作] 索引標籤中。採取動作，作為事件修復的一部分。</span><span class="sxs-lookup"><span data-stu-id="039d1-149">If there are any actions pending for approval as part of the investigation they will appear in the Pending actions tab. Take action as part of incident remediation.</span></span>


## <a name="evidence"></a><span data-ttu-id="039d1-150">證據</span><span class="sxs-lookup"><span data-stu-id="039d1-150">Evidence</span></span>
<span data-ttu-id="039d1-151">Microsoft 威脅防護會自動調查警示中所有事件支援活動和可疑實體，為您提供重要檔案、程序、服務、電子郵件等相關自動回應與資訊。</span><span class="sxs-lookup"><span data-stu-id="039d1-151">Microsoft Threat Protection automatically investigates all the incidents' supported events and suspicious entities in the alerts, providing you with auto-response and information about the important files, processes, services, emails, and more.</span></span> <span data-ttu-id="039d1-152">可協助您快速偵測並封鎖事件中的潛在威脅。</span><span class="sxs-lookup"><span data-stu-id="039d1-152">This helps quickly detect and block potential threats in the incident.</span></span> 

![事件證據索引標籤影像](../images/incident-evidence.png)

<span data-ttu-id="039d1-154">系統會將每個經分析的實體標示為判定結果 (惡意、可疑、清除) 以及修復狀態。</span><span class="sxs-lookup"><span data-stu-id="039d1-154">Each of the analyzed entities will be marked with a verdict (Malicious, Suspicious, Clean) as well as a remediation status.</span></span> <span data-ttu-id="039d1-155">可協助您了解整個事件的修復狀態，以及進一步修復可採取的步驟。</span><span class="sxs-lookup"><span data-stu-id="039d1-155">This assists you in understanding the remediation status of the entire incident and what are the next steps that can be taken to further remediate.</span></span>


## <a name="related-topics"></a><span data-ttu-id="039d1-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="039d1-156">Related topics</span></span>
- [<span data-ttu-id="039d1-157">事件概觀</span><span class="sxs-lookup"><span data-stu-id="039d1-157">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="039d1-158">設定事件優先順序</span><span class="sxs-lookup"><span data-stu-id="039d1-158">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="039d1-159">管理事件</span><span class="sxs-lookup"><span data-stu-id="039d1-159">Manage incidents</span></span>](manage-incidents.md)