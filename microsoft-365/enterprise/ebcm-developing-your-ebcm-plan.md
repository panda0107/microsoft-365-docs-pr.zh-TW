---
title: 您的企業商務持續性管理計劃的考量
author: chrfox
ms.author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: 開發雲端感知商務持續性計劃時需考慮的事項。
ms.openlocfilehash: 4a133c65f6a5a2de44e871995886a01c2ce8e9a9
ms.sourcegitcommit: 7690c8bfdea6e6d245cfa7c5b09b913b092cde0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/23/2019
ms.locfileid: "37122333"
---
# <a name="developing-your-continuity-plan"></a><span data-ttu-id="c12ab-103">開發您的持續性計劃</span><span class="sxs-lookup"><span data-stu-id="c12ab-103">Developing your continuity plan</span></span>

<span data-ttu-id="c12ab-104">本主題提供開發商務持續性計劃的指導方針，將 Microsoft 365 相依性納入考量。</span><span class="sxs-lookup"><span data-stu-id="c12ab-104">This topic provides guidance on developing a business continuity plan which takes Microsoft 365 dependencies into account.</span></span> <span data-ttu-id="c12ab-105">我們在這裡建議您分析商務功能及識別有哪些項目依賴 Microsoft 365 服務的方法。</span><span class="sxs-lookup"><span data-stu-id="c12ab-105">Here we recommend methods for analyzing your business functions and identifying the ones which depend on Microsoft 365 services.</span></span> <span data-ttu-id="c12ab-106">您會在預期有服務失敗且您必須為這些可能性進行準備的情況下，執行這個分析。</span><span class="sxs-lookup"><span data-stu-id="c12ab-106">You'll perform this analysis with the anticipation that there will be service failures and that you have to prepare for those possibilities.</span></span>

<span data-ttu-id="c12ab-107">一般來說，企業持續性規劃涉及四個層面：評定、規劃、功能驗證以及溝通與協調。</span><span class="sxs-lookup"><span data-stu-id="c12ab-107">Broadly speaking, business continuity planning involves four aspects, assessment, planning, capability validation,and communication and coordination.</span></span>

## <a name="assesment"></a><span data-ttu-id="c12ab-108">評定</span><span class="sxs-lookup"><span data-stu-id="c12ab-108">Assesment</span></span>
<span data-ttu-id="c12ab-109">首先，您必須識別貴組織中的商務功能，以及支援它們的服務和程序。</span><span class="sxs-lookup"><span data-stu-id="c12ab-109">First you must identify the business functions in your org and the services and processes that support them.</span></span> <span data-ttu-id="c12ab-110">包括完成商務影響分析，其中每個商務功能會根據關鍵程度排名，並您要識別每個商務功能相依的程序和服務。</span><span class="sxs-lookup"><span data-stu-id="c12ab-110">This includes completing a business impact analysis, where each business function is ranked according to how critical it is and you identify the processes and services that each one depends on.</span></span> <span data-ttu-id="c12ab-111">以下是範例表格，可協助您開始使用自己的評定。</span><span class="sxs-lookup"><span data-stu-id="c12ab-111">Here's a sample table you can refer to help you get started with your own assessment.</span></span>

<span data-ttu-id="c12ab-112">**範例商務影響評定 (BIA)**</span><span class="sxs-lookup"><span data-stu-id="c12ab-112">**Sample Business Impact Assessment (BIA)**</span></span>

<span data-ttu-id="c12ab-113">這是 `name of the service, system, process, or function` 的 BIA 文件</span><span class="sxs-lookup"><span data-stu-id="c12ab-113">This is a BIA document for `name of the service, system, process, or function`</span></span>

|<span data-ttu-id="c12ab-114">BIA 欄位</span><span class="sxs-lookup"><span data-stu-id="c12ab-114">BIA fields</span></span>|<span data-ttu-id="c12ab-115">描述</span><span class="sxs-lookup"><span data-stu-id="c12ab-115">Description</span></span>|
|---------|---------|
|<span data-ttu-id="c12ab-116">BIA 類型</span><span class="sxs-lookup"><span data-stu-id="c12ab-116">BIA type</span></span>|`is it a business process or technology, service or system?`|
|<span data-ttu-id="c12ab-117">BIA 名稱</span><span class="sxs-lookup"><span data-stu-id="c12ab-117">BIA name</span></span>|`name of the service/system/function/process`|
|<span data-ttu-id="c12ab-118">服務描述</span><span class="sxs-lookup"><span data-stu-id="c12ab-118">Service description</span></span>|`give a full description of the service, process, or function`|
|<span data-ttu-id="c12ab-119">企業功能</span><span class="sxs-lookup"><span data-stu-id="c12ab-119">enterprise function</span></span>|`some examples: customer services; legal; marketing; risk management, security, sales, information technology, production, manufacturing`|
|<span data-ttu-id="c12ab-120">會計年度</span><span class="sxs-lookup"><span data-stu-id="c12ab-120">fiscal year</span></span>|`the current fiscal year, re-evaluate these on a regular basis`|
|<span data-ttu-id="c12ab-121">重要性</span><span class="sxs-lookup"><span data-stu-id="c12ab-121">criticality</span></span>|`develop your own classifications, but here are some examples: mission critical, important, deferrable`|
|<span data-ttu-id="c12ab-122">營業單位</span><span class="sxs-lookup"><span data-stu-id="c12ab-122">business unit</span></span>|`name of the business unit that owns this business function`|
|<span data-ttu-id="c12ab-123">程序 (服務、功能)</span><span class="sxs-lookup"><span data-stu-id="c12ab-123">process (service, feature)</span></span>|`the name of the process, service, or feature`|
|<span data-ttu-id="c12ab-124">商務群組高層領導</span><span class="sxs-lookup"><span data-stu-id="c12ab-124">business group senior leader</span></span>|`the name and contact information of the senior leader of the business group that owns this business process`|
|<span data-ttu-id="c12ab-125">技術是否已建立**內部** SLA 或 OLA？</span><span class="sxs-lookup"><span data-stu-id="c12ab-125">Does the technology have an established **internal** SLA or OLA?</span></span>|`please explain in as much detail as possible`|
|<span data-ttu-id="c12ab-126">技術是否已建立**外部** SLA 或 OLA？</span><span class="sxs-lookup"><span data-stu-id="c12ab-126">Does the technology have an established **external** SLA or OLA?</span></span>|`please explain in as much detail as possible`|
|<span data-ttu-id="c12ab-127">技術是否有驅動特定程序 SLA 的已知執行規定？</span><span class="sxs-lookup"><span data-stu-id="c12ab-127">Does the technology have a known executive mandate driving a specific process SLA?</span></span> <span data-ttu-id="c12ab-128">如果是的話，請詳細說明。</span><span class="sxs-lookup"><span data-stu-id="c12ab-128">If yes, explain in detail.</span></span>|`details here`|
|<span data-ttu-id="c12ab-129">與此服務相關聯的資料遺失或洩露時，是否會觸發重大事件？</span><span class="sxs-lookup"><span data-stu-id="c12ab-129">Will the loss or compromise of the data associated with this services trigger a major event?</span></span> <span data-ttu-id="c12ab-130">如果是的話，請詳細說明。</span><span class="sxs-lookup"><span data-stu-id="c12ab-130">If yes, explain in detail.</span></span>|`details here`|
|<span data-ttu-id="c12ab-131">服務是否有針對部分或所有關鍵功能的因應措施或替代方案？</span><span class="sxs-lookup"><span data-stu-id="c12ab-131">Does the service have a workaround or alternative in place for some or all of its key functions and features?</span></span> <span data-ttu-id="c12ab-132">如果是的話，請詳細說明。</span><span class="sxs-lookup"><span data-stu-id="c12ab-132">If yes, explain in detail.</span></span>|`details here`|
|<span data-ttu-id="c12ab-133">服務是否會處理、儲存或傳輸客戶資料 (PII)？</span><span class="sxs-lookup"><span data-stu-id="c12ab-133">Does the service process, store, or transmit customer data (PII)?</span></span> <span data-ttu-id="c12ab-134">如果是的話，請詳細說明。</span><span class="sxs-lookup"><span data-stu-id="c12ab-134">If yes, explain in detail.</span></span>|`details here`|
|<span data-ttu-id="c12ab-135">BIA 狀態</span><span class="sxs-lookup"><span data-stu-id="c12ab-135">BIA status</span></span>|`develop your own status classification, here are some examples: planned, started, in-progress, complete, on-hold, expired`|
|<span data-ttu-id="c12ab-136">完成日期</span><span class="sxs-lookup"><span data-stu-id="c12ab-136">Task: The completion date.</span></span>|`the date this BIA was completed`|
|<span data-ttu-id="c12ab-137">BIA 講授者</span><span class="sxs-lookup"><span data-stu-id="c12ab-137">BIA facilitator</span></span>|`name of the person or group who is responsible for developing and maintaining this BIA`|
|<span data-ttu-id="c12ab-138">BIA 核准</span><span class="sxs-lookup"><span data-stu-id="c12ab-138">BIA approval</span></span>|`name of the person or group who is the executive sponsor of this BIA and who has responsibility for approving it.`|
|<span data-ttu-id="c12ab-139">投稿人</span><span class="sxs-lookup"><span data-stu-id="c12ab-139">contributors</span></span>|`optional list of the people who helped develop this BIA and their contact information`|
|<span data-ttu-id="c12ab-140">BIA 核准位置</span><span class="sxs-lookup"><span data-stu-id="c12ab-140">BIA approval location</span></span>|`indicate where the executive approval is located, or attach proof to this document`|

## <a name="planning"></a><span data-ttu-id="c12ab-141">規劃</span><span class="sxs-lookup"><span data-stu-id="c12ab-141">Planning</span></span>

<span data-ttu-id="c12ab-142">接下來，您要在商務程序之間巡視，以查看是否有任何階層式相依性關聯存在。</span><span class="sxs-lookup"><span data-stu-id="c12ab-142">Next, you look across business processes to see where any cascading dependency relationships exist.</span></span> <span data-ttu-id="c12ab-143">根據結果，您優先處理並且形式復原策略，然後再進行支援您策略的標準作業程序。</span><span class="sxs-lookup"><span data-stu-id="c12ab-143">Based on the outcome, you prioritize and form resiliency strategies, and standard operating procedures supporting your strategies.</span></span>

<span data-ttu-id="c12ab-144">您可以使用 [Microsoft Service Map](https://docs.microsoft.com/zh-TW/azure/azure-monitor/insights/service-map) 協助您進行這個對應。</span><span class="sxs-lookup"><span data-stu-id="c12ab-144">You can use [Microsoft Service Map](https://docs.microsoft.com/zh-TW/azure/azure-monitor/insights/service-map) to help you in with this mapping.</span></span> <span data-ttu-id="c12ab-145">Microsoft Service Map 會自動探索 Windows 和 Linux 系統上的應用程式元件，並且對應所有 TCP 相依性、識別連線和應用程式相依的遠端第三方系統。</span><span class="sxs-lookup"><span data-stu-id="c12ab-145">Microsoft Service Map automatically discovers application components on Windows and Linux systems and maps all TCP dependencies, identifies connections,  and remote third-party systems that the app depends on.</span></span> <span data-ttu-id="c12ab-146">它也會將相依性對應至通常是陰暗的網路區域，例如 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="c12ab-146">It also maps dependencies to areas of your network that are traditionally dark, such as Active Directory.</span></span>

<span data-ttu-id="c12ab-147">以下是您可以作為起點的範例相依性分析 (DA)。</span><span class="sxs-lookup"><span data-stu-id="c12ab-147">Here's a sample dependency analysis (DA) you can start from.</span></span> <span data-ttu-id="c12ab-148">在您的相依性分析 (DA) 中，您會識別及檢查程序相依性。</span><span class="sxs-lookup"><span data-stu-id="c12ab-148">In your dependency analysis (DA), you will identify and examine the process dependencies.</span></span> <span data-ttu-id="c12ab-149">請確定您納入人員、供應商、客戶、合作關係和設施。</span><span class="sxs-lookup"><span data-stu-id="c12ab-149">Make sure you include people, suppliers, customers, partnerships and facilities.</span></span> <span data-ttu-id="c12ab-150">此分析的資料將用來識別程序的復原需求與支援相依性的復原功能之間的差距。</span><span class="sxs-lookup"><span data-stu-id="c12ab-150">The data from this analysis will be used to identify gaps between the recovery requirements of a process and the recovery capabilities of supporting dependencies.</span></span>


|<span data-ttu-id="c12ab-151">欄位</span><span class="sxs-lookup"><span data-stu-id="c12ab-151">Field</span></span>|<span data-ttu-id="c12ab-152">描述</span><span class="sxs-lookup"><span data-stu-id="c12ab-152">description</span></span>|
|---------|---------|
|<span data-ttu-id="c12ab-153">程序類型</span><span class="sxs-lookup"><span data-stu-id="c12ab-153">process type</span></span>|         |
|<span data-ttu-id="c12ab-154">講授者</span><span class="sxs-lookup"><span data-stu-id="c12ab-154">facilitator</span></span>|         |
|<span data-ttu-id="c12ab-155">完成者</span><span class="sxs-lookup"><span data-stu-id="c12ab-155">completed by</span></span>|         |
|<span data-ttu-id="c12ab-156">完成日期</span><span class="sxs-lookup"><span data-stu-id="c12ab-156">completed date</span></span>|         |
|<span data-ttu-id="c12ab-157">投稿人</span><span class="sxs-lookup"><span data-stu-id="c12ab-157">contributors</span></span>|         |
  
## <a name="capability-validation"></a><span data-ttu-id="c12ab-158">功能驗證</span><span class="sxs-lookup"><span data-stu-id="c12ab-158">Capability validation</span></span>

<span data-ttu-id="c12ab-159">當您清查商務程序，並將關係對應到其他程序和技術之後，您必須為所有程序建置驗證案例。</span><span class="sxs-lookup"><span data-stu-id="c12ab-159">Once you have inventoried your business processes and mapped out relationships to other process and technologies, you need to build validation scenarios for all the processes.</span></span> <span data-ttu-id="c12ab-160">基本上就是要了解如何驗證您的商務程序持續性計劃。</span><span class="sxs-lookup"><span data-stu-id="c12ab-160">Basically, figure out how you are going to validate your business process continuity plans.</span></span> <span data-ttu-id="c12ab-161">您可能會發現某些內容更重要，而且您想要優先處理這些問題。</span><span class="sxs-lookup"><span data-stu-id="c12ab-161">You'll probably find that some are more important that others and you'll want to prioritize those.</span></span>
<span data-ttu-id="c12ab-162">請記得在建立計劃之後，對員工進行事件回應和持續性措施的定期訓練相當重要。</span><span class="sxs-lookup"><span data-stu-id="c12ab-162">Don't forget that regularly training employees on incident response and continuity measures is important once the plan is established.</span></span> <span data-ttu-id="c12ab-163">您應該透過納入每個驗證或測試的學習，使用後續事件檢閱來增強復原策略。</span><span class="sxs-lookup"><span data-stu-id="c12ab-163">Post incident reviews should be used to enhance your resiliency strategies by incorporating learnings from each validation or test.</span></span>

## <a name="incident-coordination-and-communication"></a><span data-ttu-id="c12ab-164">事件協調與通訊</span><span class="sxs-lookup"><span data-stu-id="c12ab-164">Incident coordination and communication</span></span>

<span data-ttu-id="c12ab-165">在服務事件期間，一般通訊通道可能會受到影響或降級，因此您應該預先安排替代選項，在事件期間協助貴組織保持連線。</span><span class="sxs-lookup"><span data-stu-id="c12ab-165">During a service incident, normal communications channels may be impacted or degraded, so you should pre-arrange alternatives to help your organization stay connected during an incident.</span></span> <span data-ttu-id="c12ab-166">建立通訊通道、符合安全性和合規性，以及在中斷之前訓練使用者使用，非常重要。</span><span class="sxs-lookup"><span data-stu-id="c12ab-166">It is critical that the communication channels be established, vetted for security and compliance, and users trained on their use prior to a disruption.</span></span> <span data-ttu-id="c12ab-167">使用者比較樂見從已知狀態到另一個已知狀態的失敗，而不是在危機當中突然出現臨機操作、未知的解決方案。</span><span class="sxs-lookup"><span data-stu-id="c12ab-167">Failing from a known state to another known state is far preferable to users coming up with ad-hoc, unknown solutions in the middle of a crisis.</span></span>

<span data-ttu-id="c12ab-168">在 Microsoft 中，每個服務小組已建立內部替代通訊通道，協助我們在一般通訊通道無法使用時進行協調。</span><span class="sxs-lookup"><span data-stu-id="c12ab-168">At Microsoft, each service team has established internal alternative communication channels to help us coordinate when our normal communications channels aren’t available.</span></span> <span data-ttu-id="c12ab-169">其中包括備份電話和音訊會議解決方案、Yammer 群組、Teams 群組、內部服務健康狀態儀表板，以及內部事件管理軟體。</span><span class="sxs-lookup"><span data-stu-id="c12ab-169">These include backup telephony and audio-conferencing solutions, Yammer groups, Teams groups, internal Service Health Dashboards, and internal Incident Management software.</span></span>

<span data-ttu-id="c12ab-170">在您的業務影響分析和相依性分析期間，您會對應關鍵程序，以及它們相依的技術或服務。</span><span class="sxs-lookup"><span data-stu-id="c12ab-170">During your Business Impact Analysis and Dependency Analysis, you will be mapping critical processes and the technologies or services they depend on.</span></span> <span data-ttu-id="c12ab-171">在這個規劃階段期間特別注意通訊，並且思考替代方案。</span><span class="sxs-lookup"><span data-stu-id="c12ab-171">Pay special attention to communication during this phase of planning and think of alternatives.</span></span> <span data-ttu-id="c12ab-172">下列提供一些範例。</span><span class="sxs-lookup"><span data-stu-id="c12ab-172">Here are some examples.</span></span>

- <span data-ttu-id="c12ab-173">如果您保持使用者和專案關係人得到通知的主要方法是使用電子郵件，而您的電子郵件服務遭到降級或無法使用，您可以使用其他服務，例如 Microsoft Teams、Yammer 或其他第三方服務作為備援。</span><span class="sxs-lookup"><span data-stu-id="c12ab-173">If email is your primary method of keeping your users and stakeholders informed, and your email service is degraded or unavailable, you can use another service such as Microsoft Teams, Yammer, or another 3rd-party service as a backup.</span></span> <span data-ttu-id="c12ab-174">關鍵是事先建立這些項目，並且訓練您的使用者要到哪裡使用。</span><span class="sxs-lookup"><span data-stu-id="c12ab-174">The key is to establish these beforehand and train your users on where to go.</span></span> <span data-ttu-id="c12ab-175">如果沒有人知道 Yammer 執行緒存在，或者沒有人將它列入書籤，那麼 Yammer 執行緒就沒有什麼用處。</span><span class="sxs-lookup"><span data-stu-id="c12ab-175">A Yammer thread isn’t going to be useful if no one knows it exists or if no one has it bookmarked.</span></span>  
- <span data-ttu-id="c12ab-176">如果您的內部事件管理程序依賴語音通訊來協調您的回應，請建立替代電話語音解決方案，在危機時使用。</span><span class="sxs-lookup"><span data-stu-id="c12ab-176">If your internal Incident Management processes rely on voice communications to coordinate your responses, establish an alternative telephony solution for use during a crisis.</span></span> <span data-ttu-id="c12ab-177">這項解決方案不需要與您的主要服務有完整同位，但是應該提供最低的共同作業層級，在您的商務持續性與事件管理小組之間進行協調。</span><span class="sxs-lookup"><span data-stu-id="c12ab-177">This solution doesn’t need to have full parity with your primary service but should provide the minimum level of collaboration to coordinate your Business Continuity and Incident Management teams.</span></span> <span data-ttu-id="c12ab-178">此外，要求使用者在「全域通訊清單」中發佈他們的行動電話號碼，可以提供多一層的備援通訊，以防萬一。</span><span class="sxs-lookup"><span data-stu-id="c12ab-178">Additionally, asking users to publish their mobile phone numbers in your Global Address List can provide an additional layer of backup communication in extreme cases.</span></span>
- <span data-ttu-id="c12ab-179">您可能想要建立自訂服務健康狀態儀表板或其他此類網站，可以在事件期間提供狀態更新。</span><span class="sxs-lookup"><span data-stu-id="c12ab-179">You may want to create a custom service health dashboard, or other such site, which can provide status updates during an incident.</span></span> <span data-ttu-id="c12ab-180">事先訓練使用者要到哪裡取得資訊，可以協助減少與技術支援中心的不必要通話，並且為您的使用者加強信心，這個狀況可以快速有效率地處理。</span><span class="sxs-lookup"><span data-stu-id="c12ab-180">Training users where to go for information beforehand will help reduce unnecessary calls to help desk and instill confidence in your user base that the situation is being handled quickly and efficiently.</span></span> <span data-ttu-id="c12ab-181">使用 O365 服務通訊 API 將這個項目繫結至 M365，以提高可見度。</span><span class="sxs-lookup"><span data-stu-id="c12ab-181">Use the O365 Service Communications API to tie this into M365 for an even greater level of visibility.</span></span>  
- <span data-ttu-id="c12ab-182">讓您的商務程序性計劃和標準作業程序的位置眾所周知相當重要。</span><span class="sxs-lookup"><span data-stu-id="c12ab-182">It is critical that the location of your Business Continuity Plans and Standard Operating Procedures is well known.</span></span> <span data-ttu-id="c12ab-183">我們建議使用如 SharePoint Online 和商務用 OneDrive 的工具，並且設定自動同步到本機裝置，來維護重要文件的線上和離線複本。</span><span class="sxs-lookup"><span data-stu-id="c12ab-183">We recommend maintaining online and offline copies of critical documentation, such as with SharePoint Online or OneDrive for Business configured for automatic sync to local devices.</span></span> <span data-ttu-id="c12ab-184">針對對於復原絕對重要的服務/網路作業中心和其他較小型的小組，您可能也想要保留紙本，在緊急事件時使用。</span><span class="sxs-lookup"><span data-stu-id="c12ab-184">For Service/Network Operations Centers and other similar teams that will be absolutely critical for recovery, you may also want to keep hard copies available to be used in the event of an emergency.</span></span>

## <a name="know-your-external-points-of-integration"></a><span data-ttu-id="c12ab-185">了解您的外部整合點</span><span class="sxs-lookup"><span data-stu-id="c12ab-185">Know your external points of integration</span></span>

<span data-ttu-id="c12ab-186">無論商務模型如何，每家公司都有與客戶、合作夥伴和廠商的整合點。</span><span class="sxs-lookup"><span data-stu-id="c12ab-186">Regardless of business model, every company has points of integration with their customers, partners and vendors.</span></span> <span data-ttu-id="c12ab-187">商務價值供應鏈是建立在與外部實體的整合上。</span><span class="sxs-lookup"><span data-stu-id="c12ab-187">The business value supply chain is build on integration with external entities.</span></span> <span data-ttu-id="c12ab-188">在服務中斷事件中改善商務持續性，需要考量並保護每個整合點。</span><span class="sxs-lookup"><span data-stu-id="c12ab-188">Improving business continuity in the event of service disruption requires consideration – and protection – of each point of integration.</span></span>  
<span data-ttu-id="c12ab-189">當您分析供應鏈時，應該依照分析內部通訊的相同方式來考量外部通訊。</span><span class="sxs-lookup"><span data-stu-id="c12ab-189">As you analyze your supply chain, external communications should be considered in the same way internal communications are analyzed.</span></span> <span data-ttu-id="c12ab-190">您的客戶是否依賴您的 Exchange Online 伺服器作為與您聯繫的唯一方法？</span><span class="sxs-lookup"><span data-stu-id="c12ab-190">Do your customers rely on your Exchange Online servers as the only method of contacting you?</span></span> <span data-ttu-id="c12ab-191">您是否已建立在發生影響運作時間的事件時使用的替代通訊方法，並且讓您的供應商知悉？</span><span class="sxs-lookup"><span data-stu-id="c12ab-191">Have you established and made your suppliers aware of alternative communication methods, in the event uptime is impacted?</span></span> <span data-ttu-id="c12ab-192">以下是建議如何組織想法的範例表格。</span><span class="sxs-lookup"><span data-stu-id="c12ab-192">Here's a sample table that suggests how to organize your thinking.</span></span>

|<span data-ttu-id="c12ab-193">外部實體名稱</span><span class="sxs-lookup"><span data-stu-id="c12ab-193">external entity name</span></span>|<span data-ttu-id="c12ab-194">影響事件案例</span><span class="sxs-lookup"><span data-stu-id="c12ab-194">impacting incident scenario</span></span>|<span data-ttu-id="c12ab-195">Microsoft 365 服務整合</span><span class="sxs-lookup"><span data-stu-id="c12ab-195">Microsoft 365 services integrated</span></span>|<span data-ttu-id="c12ab-196">替代</span><span class="sxs-lookup"><span data-stu-id="c12ab-196">alternatives</span></span>|
|---------|---------|---------|---------|
|`vendor name`|<span data-ttu-id="c12ab-197">郵件流程</span><span class="sxs-lookup"><span data-stu-id="c12ab-197">Mail Flow</span></span>|<span data-ttu-id="c12ab-198">Exchange Online 是與 Contoso 通訊的唯一方式</span><span class="sxs-lookup"><span data-stu-id="c12ab-198">Exchange Online is the only means of communication with Contoso</span></span>|<span data-ttu-id="c12ab-199">設定外部 Microsoft Teams 通道或第三方共同作業軟體</span><span class="sxs-lookup"><span data-stu-id="c12ab-199">set up external Microsoft Teams channels or a third-party collaboration software</span></span>          |
|`service supplier name`|<span data-ttu-id="c12ab-200">聊天</span><span class="sxs-lookup"><span data-stu-id="c12ab-200">Chat</span></span>|<span data-ttu-id="c12ab-201">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c12ab-201">Microsoft Teams</span></span>|<span data-ttu-id="c12ab-202">第三方立即訊息</span><span class="sxs-lookup"><span data-stu-id="c12ab-202">third party instant messaging</span></span>|
|`partner name`|<span data-ttu-id="c12ab-203">語音</span><span class="sxs-lookup"><span data-stu-id="c12ab-203">Voice</span></span>|<span data-ttu-id="c12ab-204">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c12ab-204">Microsoft Teams</span></span>|<span data-ttu-id="c12ab-205">行動或公用 pstn</span><span class="sxs-lookup"><span data-stu-id="c12ab-205">mobile or public pstn</span></span>      |
|`supplier name`|<span data-ttu-id="c12ab-206">檔案共用</span><span class="sxs-lookup"><span data-stu-id="c12ab-206">file sharing</span></span>|<span data-ttu-id="c12ab-207">外部共用 SharePoint 網站和 OneDrive</span><span class="sxs-lookup"><span data-stu-id="c12ab-207">externally shared SharePoint sites and OneDrive</span></span>|<span data-ttu-id="c12ab-208">第三方檔案共用</span><span class="sxs-lookup"><span data-stu-id="c12ab-208">third party file sharing</span></span>         |