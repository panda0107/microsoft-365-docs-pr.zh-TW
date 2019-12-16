---
title: Office 365 安全性藍圖 - 前 30 天、90 天和之後的首要工作
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: 'Microsoft 網路安全性小組對於實作安全性功能以保護您 Office 365 環境的主要建議。 '
ms.openlocfilehash: f07363585917a7088a590e11e89794b924cfb992
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "39971631"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a><span data-ttu-id="11c6b-103">Office 365 安全性藍圖 - 前 30 天、90 天和之後的首要工作</span><span class="sxs-lookup"><span data-stu-id="11c6b-103">Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond. This roadmap includes recommendations for implementing capabilities.</span></span>

<span data-ttu-id="11c6b-104">本文包含 Microsoft 網路安全性小組對於實作安全性功能以保護您 Office 365 環境的主要建議。</span><span class="sxs-lookup"><span data-stu-id="11c6b-104">This article includes top recommendations from Microsoft's cybersecurity team for implementing security capabilities to protect your Office 365 environment.</span></span> <span data-ttu-id="11c6b-105">本文改編自 Microsoft Ignite 工作階段 - [像網路安全性專業人員一般保護 Office 365：前 30 天、90 天和之後的首要工作](https://www.youtube.com/watch?v=luignzNyR-o)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-105">This article is adapted from a Microsoft Ignite session — [Secure Office 365 like a cybersecurity pro: Top priorities for the first 30 days, 90 days, and beyond](https://www.youtube.com/watch?v=luignzNyR-o).</span></span> <span data-ttu-id="11c6b-106">這個工作階段是由企業網路安全性架構師 Mark Simos 和 Matt Kemelhar 開發及展示。</span><span class="sxs-lookup"><span data-stu-id="11c6b-106">This session was developed and presented by Mark Simos and Matt Kemelhar, Enterprise Cybersecurity Architects.</span></span>

<span data-ttu-id="11c6b-107">本文內容：</span><span class="sxs-lookup"><span data-stu-id="11c6b-107">In this article:</span></span>

- [<span data-ttu-id="11c6b-108">藍圖結果</span><span class="sxs-lookup"><span data-stu-id="11c6b-108">Roadmap outcomes</span></span>](security-roadmap.md#Roadmap)

- [<span data-ttu-id="11c6b-109">30 天 - 強力快速致勝</span><span class="sxs-lookup"><span data-stu-id="11c6b-109">30 days — Powerful Quick Wins</span></span>](security-roadmap.md#Thirdaydays)

- [<span data-ttu-id="11c6b-110">90 天 - 加強的保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-110">90 days — Enhanced Protections</span></span>](security-roadmap.md#Ninetydays)

- [<span data-ttu-id="11c6b-111">以後</span><span class="sxs-lookup"><span data-stu-id="11c6b-111">Beyond</span></span>](security-roadmap.md#Beyond)

## <a name="roadmap-outcomes"></a><span data-ttu-id="11c6b-112">藍圖結果</span><span class="sxs-lookup"><span data-stu-id="11c6b-112">Roadmap outcomes</span></span>
<span data-ttu-id="11c6b-113"><a name="Roadmap"> </a></span><span class="sxs-lookup"><span data-stu-id="11c6b-113"></span></span>

<span data-ttu-id="11c6b-114">這些藍圖建議橫跨有邏輯順序的三個階段，具有下列目標。</span><span class="sxs-lookup"><span data-stu-id="11c6b-114">These recommendations are provided across three phases in a logical order with the following outcomes:</span></span>

|||
|:-----|:-----|
| |<span data-ttu-id="11c6b-115">結果</span><span class="sxs-lookup"><span data-stu-id="11c6b-115">Outcomes</span></span>
|<span data-ttu-id="11c6b-116">30 天</span><span class="sxs-lookup"><span data-stu-id="11c6b-116">30 days</span></span>|<span data-ttu-id="11c6b-117">快速設定：</span><span class="sxs-lookup"><span data-stu-id="11c6b-117">Rapid configuration:</span></span>  <br/> <span data-ttu-id="11c6b-118">• 基本系統管理保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-118">• Basic admin protections</span></span>  <br/> <span data-ttu-id="11c6b-119">• 記錄和分析</span><span class="sxs-lookup"><span data-stu-id="11c6b-119">• Logging and analytics</span></span>  <br/> <span data-ttu-id="11c6b-120">• 基本身分識別保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-120">• Basic identity protections</span></span>  <br/> <span data-ttu-id="11c6b-121">租用戶設定</span><span class="sxs-lookup"><span data-stu-id="11c6b-121">Tenant configuration</span></span>  <br/>  <span data-ttu-id="11c6b-122">準備專案關係人</span><span class="sxs-lookup"><span data-stu-id="11c6b-122">Prepare stakeholders</span></span>|
|<span data-ttu-id="11c6b-123">90 天</span><span class="sxs-lookup"><span data-stu-id="11c6b-123">90 days</span></span>|<span data-ttu-id="11c6b-124">進階保護：</span><span class="sxs-lookup"><span data-stu-id="11c6b-124">Advanced protections:</span></span>  <br/> <span data-ttu-id="11c6b-125">• 系統管理員帳戶</span><span class="sxs-lookup"><span data-stu-id="11c6b-125">• Admin accounts</span></span>  <br/>  <span data-ttu-id="11c6b-126">• 資料與使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="11c6b-126">• Data &amp; user accounts</span></span>  <br/>  <span data-ttu-id="11c6b-127">合規性、威脅及使用者需求的可見度</span><span class="sxs-lookup"><span data-stu-id="11c6b-127">Visibility into compliance, threat, and user needs</span></span>  <br/>  <span data-ttu-id="11c6b-128">改編和實作預設原則和保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-128">Adapt and implement default policies and protections</span></span>|
|<span data-ttu-id="11c6b-129">以後</span><span class="sxs-lookup"><span data-stu-id="11c6b-129">Beyond T+120</span></span>|<span data-ttu-id="11c6b-130">調整及微調重要原則和控制項</span><span class="sxs-lookup"><span data-stu-id="11c6b-130">Adjust and refine key policies and controls</span></span>  <br/> <span data-ttu-id="11c6b-131">將保護延伸到內部部署相依性</span><span class="sxs-lookup"><span data-stu-id="11c6b-131">Extend protections to on-premises dependencies</span></span>  <br/> <span data-ttu-id="11c6b-132">整合企業與安全性流程 (法律、測試人員威脅等等)</span><span class="sxs-lookup"><span data-stu-id="11c6b-132">Integrate with business and security processes (legal, insider threat, etc.)</span></span>|



## <a name="30-days--powerful-quick-wins"></a><span data-ttu-id="11c6b-133">30 天 - 強力快速致勝</span><span class="sxs-lookup"><span data-stu-id="11c6b-133">30 days — Powerful Quick Wins</span></span>
<span data-ttu-id="11c6b-134"><a name="Thirdaydays"> </a></span><span class="sxs-lookup"><span data-stu-id="11c6b-134"></span></span>

<span data-ttu-id="11c6b-135">這些工作可以快速地完成，並且對使用者的影響小。</span><span class="sxs-lookup"><span data-stu-id="11c6b-135">These tasks can be accomplished quickly and have low impact to users.</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11c6b-136">適用範圍</span><span class="sxs-lookup"><span data-stu-id="11c6b-136">Area</span></span>|<span data-ttu-id="11c6b-137">工作</span><span class="sxs-lookup"><span data-stu-id="11c6b-137">Tasks</span></span>|
|<span data-ttu-id="11c6b-138">安全性管理</span><span class="sxs-lookup"><span data-stu-id="11c6b-138">Security management</span></span>|<span data-ttu-id="11c6b-139">• 檢查安全分數並記下您目前的分數 ([https://securescore.office.com](https://securescore.office.com))。</span><span class="sxs-lookup"><span data-stu-id="11c6b-139">• Check Secure Score and take note of your current score ([https://securescore.office.com](https://securescore.office.com)).</span></span>  <br/>  <span data-ttu-id="11c6b-140">• 開啟 Office 365 的稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="11c6b-140">• Turn on audit logging for Office 365.</span></span> <span data-ttu-id="11c6b-141">請參閱[搜尋稽核記錄](../../compliance/search-the-audit-log-in-security-and-compliance.md)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-141">[Search the audit log](../../compliance/search-the-audit-log-in-security-and-compliance.md)</span></span>  <br/> <span data-ttu-id="11c6b-142">• [設定 Office 365 租用戶以提高安全性](tenant-wide-setup-for-increased-security.md)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-142">[Configure your Office 365 tenant for increased security](tenant-wide-setup-for-increased-security.md)</span></span>  <br/>  <span data-ttu-id="11c6b-143">• 定期檢閱 Microsoft 365 安全性中心和 Cloud App Security 中的儀表板和報告。</span><span class="sxs-lookup"><span data-stu-id="11c6b-143">• Regularly review dashboards and reports in the Microsoft 365 security center and Cloud App Security.</span></span>|
|<span data-ttu-id="11c6b-144">威脅防護</span><span class="sxs-lookup"><span data-stu-id="11c6b-144">Threat protection</span></span>|<span data-ttu-id="11c6b-145">[將 Office 365 連線至 Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) (部分機器翻譯)，開始使用預設的威脅偵測原則監視異常行為。</span><span class="sxs-lookup"><span data-stu-id="11c6b-145">[Connect Office 365 to Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) to start monitoring using the default threat detection policies for anomalous behaviors.</span></span> <span data-ttu-id="11c6b-146">建立異常偵測的基準需要 7 天。</span><span class="sxs-lookup"><span data-stu-id="11c6b-146">It takes seven days to build a baseline for anomaly detection.</span></span>  <br><br/>  <span data-ttu-id="11c6b-147">針對系統管理員帳戶實作保護：</span><span class="sxs-lookup"><span data-stu-id="11c6b-147">Implement protection for admin accounts:</span></span>  <br/> <span data-ttu-id="11c6b-148">• 使用專用的系統管理員帳戶來執行系統管理活動。</span><span class="sxs-lookup"><span data-stu-id="11c6b-148">•  Use dedicated admin accounts for admin activity.</span></span>  <br/>  <span data-ttu-id="11c6b-149">• 針對系統管理員帳戶強制執行多重要素驗證 (MFA)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-149">• Enforce multi-factor authentication (MFA) for admin accounts.</span></span>  <br/>  <span data-ttu-id="11c6b-150">• 使用[高度安全的 Windows 10 裝置](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) (部分機器翻譯) 進行系統管理活動。</span><span class="sxs-lookup"><span data-stu-id="11c6b-150">• Use a [highly secure Windows 10 device](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) for admin activity.</span></span>|
|<span data-ttu-id="11c6b-151">身分識別和存取管理</span><span class="sxs-lookup"><span data-stu-id="11c6b-151">Identity and access management</span></span>|<span data-ttu-id="11c6b-152">• [啟用 Azure Active Directory Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-152">Azure Active Directory Identity Protection.</span></span>  <br/> <span data-ttu-id="11c6b-153">• 針對同盟身分識別環境，強制執行帳戶安全性 (密碼長度、年限、複雜性等等)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-153">• For federated identity environments, enforce account security (password length, age, complexity, etc.).</span></span>|
|<span data-ttu-id="11c6b-154">資訊保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-154">Information protection</span></span>| <span data-ttu-id="11c6b-155">檢閱範例資訊保護建議。</span><span class="sxs-lookup"><span data-stu-id="11c6b-155">Review example information protection recommendations.</span></span> <span data-ttu-id="11c6b-156">資訊保護需要跨組織進行協調。</span><span class="sxs-lookup"><span data-stu-id="11c6b-156">Information protection requires coordination across your organization.</span></span> <span data-ttu-id="11c6b-157">使用下列資訊開始使用：</span><span class="sxs-lookup"><span data-stu-id="11c6b-157">Get started with these resources:</span></span>  <br/> <span data-ttu-id="11c6b-158">• [GDPR 的 Office 365 資訊保護](https://aka.ms/o365gdpr)</span><span class="sxs-lookup"><span data-stu-id="11c6b-158">[Office 365 Information Protection for GDPR](https://aka.ms/o365gdpr)</span></span> <br/> <span data-ttu-id="11c6b-159">• [保護 SharePoint Online 網站與檔案](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (包括共用、分類、資料外洩防護和 Azure 資訊保護)</span><span class="sxs-lookup"><span data-stu-id="11c6b-159">• [Secure SharePoint Online sites and files](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (includes sharing, classification, data loss prevention, and Azure Information Protection)</span></span>|

## <a name="90-days--enhanced-protections"></a><span data-ttu-id="11c6b-160">90 天 - 加強的保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-160">90 days — Enhanced Protections</span></span>
<span data-ttu-id="11c6b-161"><a name="Ninetydays"> </a></span><span class="sxs-lookup"><span data-stu-id="11c6b-161"></span></span>

<span data-ttu-id="11c6b-162">這個工作需要多一些時間來計劃及實作，但是可以大幅增加您的安全性狀態。</span><span class="sxs-lookup"><span data-stu-id="11c6b-162">These tasks take a bit more time to plan and implement but greatly increase your security posture.</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11c6b-163">適用範圍</span><span class="sxs-lookup"><span data-stu-id="11c6b-163">Area</span></span>|<span data-ttu-id="11c6b-164">工作</span><span class="sxs-lookup"><span data-stu-id="11c6b-164">Task</span></span>|
|<span data-ttu-id="11c6b-165">安全性管理</span><span class="sxs-lookup"><span data-stu-id="11c6b-165">Security management</span></span>|<span data-ttu-id="11c6b-166">• 檢查針對您環境建議動作的安全分數 ([https://securescore.office.com](https://securescore.office.com))。</span><span class="sxs-lookup"><span data-stu-id="11c6b-166">• Check Secure Score for recommended actions for your environment ([https://securescore.office.com](https://securescore.office.com)).</span></span>  <br/>  <span data-ttu-id="11c6b-167">• 持續定期檢閱 Microsoft 365 安全性中心、Cloud App Security 和 SIEM 工具中的儀表板和報告。</span><span class="sxs-lookup"><span data-stu-id="11c6b-167">• Continue to regularly review dashboards and reports in the Microsoft 365 security center, Cloud App Security, and SIEM tools.</span></span> <br/> <span data-ttu-id="11c6b-168">• 尋找及實作軟體更新。</span><span class="sxs-lookup"><span data-stu-id="11c6b-168">• Look for and implement software updates.</span></span> <br/> <span data-ttu-id="11c6b-169">•使用 [攻擊模擬器](attack-simulator.md) (隨附於 [Office 365 威脅情報](office-365-ti.md)) 來進行魚叉式網路釣魚、密碼噴灑和暴力密碼破解攻擊的攻擊模擬。</span><span class="sxs-lookup"><span data-stu-id="11c6b-169">• Conduct attack simulations for spear-phishing, password-spray, and brute-force password attacks using [Attack Simulator](attack-simulator.md) (included with [Office 365 Threat Intelligence](office-365-ti.md)).</span></span>  <br/> <span data-ttu-id="11c6b-170">• 藉由檢閱 Cloud App Security 中的內建報告 (在 [調查] 索引標籤上)，以尋找共用風險。</span><span class="sxs-lookup"><span data-stu-id="11c6b-170">• Look for sharing risk by reviewing the built-in reports in Cloud App Security (on the Investigate tab).</span></span> <br/> <span data-ttu-id="11c6b-171">• 檢查 [合規性管理員](../../compliance/meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md)，檢閱適用於貴組織的法規狀態 (例如 GDPR，NIST 800-171)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-171">• Check [Compliance Manager](../../compliance/meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) to review status for regulations that apply to your organization (such as GDPR, NIST 800-171).</span></span>|
|<span data-ttu-id="11c6b-172">威脅防護</span><span class="sxs-lookup"><span data-stu-id="11c6b-172">Threat protection</span></span>| <span data-ttu-id="11c6b-173">針對系統管理員帳戶實作增強型防護：</span><span class="sxs-lookup"><span data-stu-id="11c6b-173">Implement enhanced protections for admin accounts:</span></span> <br/> <span data-ttu-id="11c6b-174">• 為系統管理活動設定[特殊權限存取工作站](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) (PAW)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-174">• Configure [Privileged Access Workstations](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) (PAWs) for admin activity.</span></span> <br/> <span data-ttu-id="11c6b-175">• 設定 [Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-175">Azure AD Privileged Identity Management</span></span> <br/> <span data-ttu-id="11c6b-176">• 設定安全性資訊和事件管理 (SIEM) 工具，以收集 Office 365、Cloud App Security 及其他服務 (包括 AD FS) 的記錄資料。</span><span class="sxs-lookup"><span data-stu-id="11c6b-176">• Configure a security information and event management (SIEM) tool to collect logging data from Office 365, Cloud App Security, and other services, including AD FS.</span></span> <span data-ttu-id="11c6b-177">Office 365 稽核記錄只會儲存 90 天的資料。</span><span class="sxs-lookup"><span data-stu-id="11c6b-177">The Office 365 Audit Log stores data for only 90 days.</span></span> <span data-ttu-id="11c6b-178">在 SIEM 工具中擷取這項資料，可讓您將資料儲存更長的時間。</span><span class="sxs-lookup"><span data-stu-id="11c6b-178">Capturing this data in SIEM tool allows you to store data for a longer period.</span></span>|
|<span data-ttu-id="11c6b-179">身分識別和存取管理</span><span class="sxs-lookup"><span data-stu-id="11c6b-179">Identity and access management</span></span>|<span data-ttu-id="11c6b-180">• 為所有使用者啟用和強制執行 MFA。</span><span class="sxs-lookup"><span data-stu-id="11c6b-180">• Enable and enforce MFA for all users.</span></span> <br/> <span data-ttu-id="11c6b-181">• 實作一組[條件式存取及相關原則](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-policies-configurations) (部分機器翻譯)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-181">• Implement a set of [conditional access and related policies](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-policies-configurations).</span></span> |
|<span data-ttu-id="11c6b-182">資訊保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-182">Information protection</span></span>| <span data-ttu-id="11c6b-183">改編和實作資訊保護原則。</span><span class="sxs-lookup"><span data-stu-id="11c6b-183">Adapt and implement information protection policies.</span></span> <span data-ttu-id="11c6b-184">這些資源包括範例：</span><span class="sxs-lookup"><span data-stu-id="11c6b-184">These resources include examples:</span></span> <br/> <span data-ttu-id="11c6b-185">• [GDPR 的 Office 365 資訊保護](https://aka.ms/o365gdpr)</span><span class="sxs-lookup"><span data-stu-id="11c6b-185">[Office 365 Information Protection for GDPR](https://aka.ms/o365gdpr)</span></span> <br/> <span data-ttu-id="11c6b-186">• [保護 SharePoint Online 網站與檔案](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files)</span><span class="sxs-lookup"><span data-stu-id="11c6b-186">[Secure SharePoint Online sites and files](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files)</span></span> <br/> <br> <span data-ttu-id="11c6b-187">針對儲存在 Office 365 (而不是 Cloud App Security) 的資料，使用 Office 365 中的資料外洩防護原則及監視工具。</span><span class="sxs-lookup"><span data-stu-id="11c6b-187">Use data loss prevention policies and monitoring tools in Office 365 for data stored in Office 365 (instead of Cloud App Security).</span></span> <br><br><span data-ttu-id="11c6b-188">針對進階警示功能 (資料外洩防護以外的功能) 搭配使用 Cloud App Security 和 Office 365。</span><span class="sxs-lookup"><span data-stu-id="11c6b-188">Use Cloud App Security with Office 365 for advanced alerting features (other than data loss prevention).</span></span>|

## <a name="beyond"></a><span data-ttu-id="11c6b-189">以後</span><span class="sxs-lookup"><span data-stu-id="11c6b-189">Beyond T+120</span></span>
<span data-ttu-id="11c6b-190"><a name="Beyond"> </a></span><span class="sxs-lookup"><span data-stu-id="11c6b-190"></span></span>

<span data-ttu-id="11c6b-191">這些是以上述工作為基礎建置的安全性措施。</span><span class="sxs-lookup"><span data-stu-id="11c6b-191">These configurations are important security measures that build on previous work.</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11c6b-192">適用範圍</span><span class="sxs-lookup"><span data-stu-id="11c6b-192">Area</span></span>|<span data-ttu-id="11c6b-193">工作</span><span class="sxs-lookup"><span data-stu-id="11c6b-193">Task</span></span>|
|<span data-ttu-id="11c6b-194">安全性管理</span><span class="sxs-lookup"><span data-stu-id="11c6b-194">Security management</span></span>|<span data-ttu-id="11c6b-195">• 使用安全分數 ([https://securescore.office.com](https://securescore.office.com)) 繼續規劃下一個動作。</span><span class="sxs-lookup"><span data-stu-id="11c6b-195">• Continue planning next actions by using Secure Score ( [https://securescore.office.com](https://securescore.office.com)).</span></span> <br/> <span data-ttu-id="11c6b-196">• 持續定期檢閱 Microsoft 365 安全性中心、Cloud App Security 和 SIEM 工具中的儀表板和報告。</span><span class="sxs-lookup"><span data-stu-id="11c6b-196">• Continue to regularly review dashboards and reports in the Microsoft 365 security center, Cloud App Security, and SIEM tools.</span></span> <br/> <span data-ttu-id="11c6b-197">• 持續尋找及實作軟體更新。</span><span class="sxs-lookup"><span data-stu-id="11c6b-197">• Continue to look for and implement software updates.</span></span> <br/> <span data-ttu-id="11c6b-198">• 將電子文件探索整合到您的法律和威脅回應程序中。</span><span class="sxs-lookup"><span data-stu-id="11c6b-198">• Integrate eDiscovery into your legal and threat response processes.</span></span>|
|<span data-ttu-id="11c6b-199">威脅防護</span><span class="sxs-lookup"><span data-stu-id="11c6b-199">Threat protection</span></span>|<span data-ttu-id="11c6b-200">• 針對內部部署身分識別元件 (AD、AD FS) 實作[保護特殊權限存取](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (SPA)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-200">• Implement [Secure Privileged Access](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (SPA) for identity components on premises (AD, AD FS).</span></span> <br/> <span data-ttu-id="11c6b-201">• 使用 Cloud App Security 來監視測試人員威脅。</span><span class="sxs-lookup"><span data-stu-id="11c6b-201">• Use Cloud App Security to monitor for insider threats.</span></span> <br/> <span data-ttu-id="11c6b-202">• 使用 Cloud App Security 探索陰影 IT SaaS 使用。</span><span class="sxs-lookup"><span data-stu-id="11c6b-202">• Discover shadow IT SaaS usage by using Cloud App Security.</span></span>|
|<span data-ttu-id="11c6b-203">身分識別和存取管理</span><span class="sxs-lookup"><span data-stu-id="11c6b-203">Identity and access management</span></span>|<span data-ttu-id="11c6b-204">• 精簡​​原則和操作程序。</span><span class="sxs-lookup"><span data-stu-id="11c6b-204">• Refine policies and operational processes.</span></span> <br/> <span data-ttu-id="11c6b-205">• 使用 Azure AD Identity Protection 來識別測試人員威脅。</span><span class="sxs-lookup"><span data-stu-id="11c6b-205">• Use Azure AD Identity Protection to identify insider threats.</span></span>|
|<span data-ttu-id="11c6b-206">資訊保護</span><span class="sxs-lookup"><span data-stu-id="11c6b-206">Information protection</span></span>| <span data-ttu-id="11c6b-207">精簡資訊保護原則：</span><span class="sxs-lookup"><span data-stu-id="11c6b-207">Refine information protection policies:</span></span> <br/> <span data-ttu-id="11c6b-208">• Microsoft 365 和 Office 365 敏感度標籤和資料外洩防護 (DLP) 或 Azure 資訊保護。</span><span class="sxs-lookup"><span data-stu-id="11c6b-208">• Microsoft 365 and Office 365 sensitivity labels and data loss prevention (DLP), or Azure Information Protection.</span></span> <br/> <span data-ttu-id="11c6b-209">• Cloud App Security 原則和警示。</span><span class="sxs-lookup"><span data-stu-id="11c6b-209">• Cloud App Security policies and alerts.</span></span>|

<span data-ttu-id="11c6b-210">另請參閱：[如何減輕例如 Petya 和 WannaCrypt 的快速網路攻擊](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/) (英文)。</span><span class="sxs-lookup"><span data-stu-id="11c6b-210">Also see: [How to mitigate rapid cyberattacks such as Petya and WannaCrypt](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/).</span></span>