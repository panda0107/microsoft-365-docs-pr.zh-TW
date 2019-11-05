---
title: 在 Microsoft Teams 中保護檔案
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2019
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.custom:
- Ent_Architecture
ms.assetid: 1d51bd87-17bf-457c-b698-61821de3afa0
description: 摘要：在 Microsoft Teams 中保護檔案的設定建議。
ms.openlocfilehash: 1b4d5205836337b02c831341d5de65a87dba6fc5
ms.sourcegitcommit: 33242c260439de0d8db41247e9414913f24adc22
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/01/2019
ms.locfileid: "37925752"
---
# <a name="secure-files-in-microsoft-teams"></a><span data-ttu-id="3508f-103">在 Microsoft Teams 中保護檔案</span><span class="sxs-lookup"><span data-stu-id="3508f-103">Secure files in Microsoft Teams</span></span>

<span data-ttu-id="3508f-104">本文提供在 Microsoft Teams 中設定小組及其基礎 SharePoint 網站，以在兼顧安全性與共同作業順暢性的前提下進行檔案保護的建議。</span><span class="sxs-lookup"><span data-stu-id="3508f-104">This article provides recommendations for configuring teams in Microsoft Teams and their underlying SharePoint sites for file protection that balances security with ease of collaboration.</span></span> <span data-ttu-id="3508f-105">本文定義四種不同的設定，首先是組織內的公用網站，並搭配最開放的共用原則。</span><span class="sxs-lookup"><span data-stu-id="3508f-105">This article defines four different configurations, starting with a public site within your organization with the most open sharing policies.</span></span> <span data-ttu-id="3508f-106">每項額外設定均代表有意識的保護升級，但對 Teams 內儲存的檔案進行存取和共同作業的能力，則會減少為僅限相關小組成員。</span><span class="sxs-lookup"><span data-stu-id="3508f-106">Each additional configuration represents a meaningful step up in protection, but the ability to access and collaborate on resources is reduced to the relevant set of users.</span></span> <span data-ttu-id="3508f-107">您可以使用這些建議作為起點，並依據組織需求調整設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-107">Use these recommendations as a starting point and adjust the configurations to meet the needs of your organization.</span></span> 
  
<span data-ttu-id="3508f-108">本文的設定符合 Microsoft 針對資料、身分識別和裝置的下列三層保護建議：</span><span class="sxs-lookup"><span data-stu-id="3508f-108">The configurations in this article align with Microsoft's recommendations for three tiers of protection for data, identities, and devices:</span></span>
  
- <span data-ttu-id="3508f-109">基準保護</span><span class="sxs-lookup"><span data-stu-id="3508f-109">Baseline protection</span></span>
    
- <span data-ttu-id="3508f-110">敏感性保護</span><span class="sxs-lookup"><span data-stu-id="3508f-110">Sensitive protection</span></span>
    
- <span data-ttu-id="3508f-111">高度機密保護</span><span class="sxs-lookup"><span data-stu-id="3508f-111">Highly confidential protection</span></span>
    
<span data-ttu-id="3508f-112">如需這些層級和每道層級的建議功能詳細資訊，請參閱下列資源。</span><span class="sxs-lookup"><span data-stu-id="3508f-112">For more information about these tiers and capabilities recommended for each tier, see the following resources.</span></span> 
  
- [<span data-ttu-id="3508f-113">Office 365 的身分識別與裝置保護</span><span class="sxs-lookup"><span data-stu-id="3508f-113">Identity and Device Protection for Office 365</span></span>](https://docs.microsoft.com/office365/enterprise/microsoft-cloud-it-architecture-resources#BKMK_O365IDP)
    
- [<span data-ttu-id="3508f-114">Office 365 的檔案保護方案</span><span class="sxs-lookup"><span data-stu-id="3508f-114">File Protection Solutions in Office 365</span></span>](https://docs.microsoft.com/office365/enterprise/microsoft-cloud-it-architecture-resources#BKMK_O365fileprotect)
    
## <a name="capability-overview"></a><span data-ttu-id="3508f-115">功能概觀</span><span class="sxs-lookup"><span data-stu-id="3508f-115">Capability overview</span></span>

<span data-ttu-id="3508f-116">針對受保護的小組而提供的建議，依據各種不同 Microsoft 365 功能而定。</span><span class="sxs-lookup"><span data-stu-id="3508f-116">Recommendations for SharePoint Online team sites draw on a variety of Microsoft 365 capabilities.</span></span> <span data-ttu-id="3508f-117">下圖顯示建議的設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-117">The following illustration shows the recommended configurations for four SharePoint Online team sites.</span></span>

![小組的建議設定](../media/secure-team-configurations.png)

<span data-ttu-id="3508f-119">如圖例所示：</span><span class="sxs-lookup"><span data-stu-id="3508f-119">As illustrated:</span></span>
  
- <span data-ttu-id="3508f-120">基準保護包含公開小組和私人小組。</span><span class="sxs-lookup"><span data-stu-id="3508f-120">Baseline protection includes both public and private team sites.</span></span> <span data-ttu-id="3508f-121">公開小組可供組織中的任何人探索及存取。</span><span class="sxs-lookup"><span data-stu-id="3508f-121">Public sites can be discovered and accessed by anybody in the organization.</span></span> <span data-ttu-id="3508f-122">私人小組則僅供小組成員探索及存取。</span><span class="sxs-lookup"><span data-stu-id="3508f-122">Private sites can only be discovered and accessed by members of the site.</span></span> <span data-ttu-id="3508f-123">這兩種設定都允許共用將檔案儲存在小組群組以外的基礎 SharePoint 網站。</span><span class="sxs-lookup"><span data-stu-id="3508f-123">Both of these configurations allow for sharing of the underlying SharePoint site on which files are stored outside the team group.</span></span>
 
- <span data-ttu-id="3508f-124">敏感且受高度機密保護的小組是私人小組，此處會限制基礎網站的共用和存取要求。</span><span class="sxs-lookup"><span data-stu-id="3508f-124">Teams for sensitive and highly confidential protection are private teams in which sharing and the requesting of access for the underlying site is limited.</span></span>

    
- <span data-ttu-id="3508f-125">[保留標籤](../../compliance/labels.md)可用來分類基礎 SharePoint 網站內的檔案。</span><span class="sxs-lookup"><span data-stu-id="3508f-125">[Retention labels](../../compliance/labels.md) provide a way to classify files within the sites.</span></span> <span data-ttu-id="3508f-126">每個基礎 SharePoint 網站都會設為自動替文件庫中的檔案加上預設保留標籤。</span><span class="sxs-lookup"><span data-stu-id="3508f-126">Each of the SharePoint Online team sites are configured to automatically label files in document libraries with a default retention label for the site.</span></span> <span data-ttu-id="3508f-127">此範例的標籤對應到四種小組網站設定，分別是「內部公開」、「私人」、「敏感性」與「高度機密」。</span><span class="sxs-lookup"><span data-stu-id="3508f-127">Corresponding to the four site configurations, the labels in this example are Internal Public, Private, Sensitive, and Highly Confidential.</span></span> <span data-ttu-id="3508f-128">使用者可以變更個別檔案的標籤，但這種設定可確保所有檔案都收到預設標籤。</span><span class="sxs-lookup"><span data-stu-id="3508f-128">Users can change the labels, but this configuration ensures all files receive a default label.</span></span>
    
- <span data-ttu-id="3508f-129">系統會針對「敏感性」和「高度機密」的保留標籤設定[資料外洩防護](../../compliance/data-loss-prevention-policies.md) (DLP) 原則，以在使用者嘗試將這類檔案傳送到組織外部時，對他們發出警告或阻止此動作。</span><span class="sxs-lookup"><span data-stu-id="3508f-129">[Data loss prevention](../../compliance/data-loss-prevention-policies.md) (DLP) policies are configured for the Sensitive and Highly Confidential retention labels to either warn or prevent users when they attempt to send these types of files outside the organization.</span></span>
    
- <span data-ttu-id="3508f-130">如果在您的案例中有需要，您可以使用[敏感度標籤](../../compliance/sensitivity-labels.md)以使用加密與權限來保護高度機密檔案。</span><span class="sxs-lookup"><span data-stu-id="3508f-130">If needed for your scenario, you can use [sensitivity labels](../../compliance/sensitivity-labels.md) to protect highly confidential files with encryption and permissions.</span></span> <span data-ttu-id="3508f-131">針對 Azure 資訊保護客戶，您可以使用 Microsoft 365 合規性中心的 Azure 資訊保護標籤，而如果您選擇執行額外或進階組態，標籤就會與 Azure 入口網站同步處理。</span><span class="sxs-lookup"><span data-stu-id="3508f-131">For Azure Information Protection customers, you can use your Azure Information Protection labels in the Microsoft 365 compliance center, and your labels will be synced with the Azure portal in case you choose to perform additional or advanced configuration.</span></span> <span data-ttu-id="3508f-132">Azure 資訊保護標籤與 Office 365 敏感度標籤完全彼此相容。</span><span class="sxs-lookup"><span data-stu-id="3508f-132">Azure Information Protection labels and Office 365 sensitivity labels are fully compatible with each other.</span></span> <span data-ttu-id="3508f-133">這表示，比方說，如果您有使用 Azure 資訊保護加上標籤的內容，則不需將內容重新分類或重新加上標籤。</span><span class="sxs-lookup"><span data-stu-id="3508f-133">This means, for example, if you have content labeled by Azure Information Protection, you won’t need to reclassify or relabel your content.</span></span> <span data-ttu-id="3508f-134">並非所有客戶都需要此層級的保護。</span><span class="sxs-lookup"><span data-stu-id="3508f-134">Not all customers need this level of protection.</span></span> 
    
## <a name="organization-wide-settings-for-sharepoint-and-onedrive"></a><span data-ttu-id="3508f-135">SharePoint 和 OneDrive 的全組織設定</span><span class="sxs-lookup"><span data-stu-id="3508f-135">Tenant-wide settings for SharePoint Online and OneDrive for Business</span></span>

<span data-ttu-id="3508f-136">SharePoint 和 OneDrive 包含對所有網站與使用者皆有影響的全組織設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-136">SharePoint Online and OneDrive for Business include tenant-wide settings that affect all sites and users.</span></span> <span data-ttu-id="3508f-137">其中某些設定可以於網站層級進行調整，使其更加嚴格 (但不能更寬鬆)。</span><span class="sxs-lookup"><span data-stu-id="3508f-137">Some of these settings can also be adjusted at the site level to be more restrictive (but not less).</span></span> <span data-ttu-id="3508f-138">本節說明會影響安全性與共同作業的租用戶整體設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-138">This section discusses tenant-wide settings that affect security and collaboration.</span></span> 
  
### <a name="sharing"></a><span data-ttu-id="3508f-139">共用</span><span class="sxs-lookup"><span data-stu-id="3508f-139">Sharing</span></span>

<span data-ttu-id="3508f-140">針對這個解決方案，我們建議使用下列全組織設定：</span><span class="sxs-lookup"><span data-stu-id="3508f-140">For this solution, we recommend the following tenant-wide settings:</span></span>
  
- <span data-ttu-id="3508f-141">保留預設共用原則，以允許所有帳戶類型的共用作業，包括匿名共用。</span><span class="sxs-lookup"><span data-stu-id="3508f-141">Keep the default sharing policy that allows all sharing with all account types, including anonymous sharing.</span></span>
    
- <span data-ttu-id="3508f-142">您可視需要將匿名的連結設為過期。</span><span class="sxs-lookup"><span data-stu-id="3508f-142">Set anonymous links to expire, if desired.</span></span>
    
- <span data-ttu-id="3508f-p107">將共用的預設連結類型變更為「內部」。 這有助於防止資料不慎洩漏到組織外部。</span><span class="sxs-lookup"><span data-stu-id="3508f-p107">Change the default link type for sharing to Internal. This helps prevent accidental data leakage outside your organization.</span></span>
    
<span data-ttu-id="3508f-145">雖然允許外部共用似乎有悖常理，但相較於以電子郵件傳送檔案，此方法可以更充分地掌控檔案共用情況。</span><span class="sxs-lookup"><span data-stu-id="3508f-145">While it might seem counterintuitive to allow external sharing, this approach provides more control over file sharing compared to sending files in email.</span></span> <span data-ttu-id="3508f-146">SharePoint 與 Outlook 一起運作，以提供安全的檔案共同作業。</span><span class="sxs-lookup"><span data-stu-id="3508f-146">SharePoint Online and Outlook work together to provide secure collaboration on files.</span></span> 
  
- <span data-ttu-id="3508f-147">根據預設，Outlook 會共用檔案的連結，而非以電子郵件傳送檔案。</span><span class="sxs-lookup"><span data-stu-id="3508f-147">By default, Outlook shares a link to a file instead of sending the file in email.</span></span> 
    
- <span data-ttu-id="3508f-148">SharePoint 和 OneDrive 可讓您輕易地與組織內外的參與者共用檔案連結</span><span class="sxs-lookup"><span data-stu-id="3508f-148">SharePoint Online and OneDrive for Business make it easy to share links to files with contributors who are both inside and outside your organization</span></span>
    
<span data-ttu-id="3508f-p109">您也可以使用相關控制來協助控管外部共用。 例如，您可以：</span><span class="sxs-lookup"><span data-stu-id="3508f-p109">You also have controls to help govern external sharing. For example, you can:</span></span>
  
- <span data-ttu-id="3508f-151">停用匿名訪客的連結。</span><span class="sxs-lookup"><span data-stu-id="3508f-151">Disable an anonymous guest link.</span></span>
    
- <span data-ttu-id="3508f-152">撤銷使用者的網站存取權。</span><span class="sxs-lookup"><span data-stu-id="3508f-152">Revoke user access to a site.</span></span>
    
- <span data-ttu-id="3508f-153">查看誰具有特定網站或文件的存取權。</span><span class="sxs-lookup"><span data-stu-id="3508f-153">See who has access to a specific site or document.</span></span>
    
- <span data-ttu-id="3508f-154">將匿名共用連結設為過期 (租用戶設定)。</span><span class="sxs-lookup"><span data-stu-id="3508f-154">Set anonymous sharing links to expire (tenant setting).</span></span>
    
- <span data-ttu-id="3508f-155">限制可在組織外部共用的人員 (租用戶設定)。</span><span class="sxs-lookup"><span data-stu-id="3508f-155">Limit who can share outside your organization (tenant setting).</span></span>
    
### <a name="use-external-sharing-together-with-data-loss-prevention-dlp"></a><span data-ttu-id="3508f-156">搭配使用外部共用與資料外洩防護 (DLP)</span><span class="sxs-lookup"><span data-stu-id="3508f-156">Use external sharing together with data loss prevention (DLP)</span></span>

<span data-ttu-id="3508f-p110">如果您不允許外部共用，有業務需求的使用者就必須找到替代工具和方法。Microsoft 建議您結合外部共用與 DLP 原則來保護敏感性與高度機密檔案。</span><span class="sxs-lookup"><span data-stu-id="3508f-p110">If you don't allow external sharing, users with a business need will find alternate tools and methods. Microsoft recommends you combine external sharing with DLP policies to protect sensitive and highly confidential files.</span></span>
  
### <a name="device-access-settings"></a><span data-ttu-id="3508f-159">裝置存取設定</span><span class="sxs-lookup"><span data-stu-id="3508f-159">Device access settings</span></span>

<span data-ttu-id="3508f-160">SharePoint 和 OneDrive 的裝置存取設定可讓您決定要僅限瀏覽器存取 (無法下載檔案)，或是封鎖存取。</span><span class="sxs-lookup"><span data-stu-id="3508f-160">Device access settings for SharePoint Online and OneDrive for Business let you determine whether access is limited to browser only (files can't be downloaded) or if access is blocked.</span></span> <span data-ttu-id="3508f-161">如需詳細資訊，請參閱[控制未受管理裝置的存取權](https://docs.microsoft.com/sharepoint/control-access-from-unmanaged-devices)。</span><span class="sxs-lookup"><span data-stu-id="3508f-161">For more information, see [Control access from unmanaged devices](https://docs.microsoft.com/sharepoint/control-access-from-unmanaged-devices).</span></span> 

<span data-ttu-id="3508f-162">若要使用裝置存取設定搭配 Azure Active Directory 中建議的條件式存取原則，請參閱[保護 SharePoint 網站和檔案的原則建議](https://docs.microsoft.com/microsoft-365/enterprise/sharepoint-file-access-policies)。</span><span class="sxs-lookup"><span data-stu-id="3508f-162">To use device access settings with recommended conditional access policies in Azure Active Directory, see [Policy recommendations for securing SharePoint sites and files](https://docs.microsoft.com/microsoft-365/enterprise/sharepoint-file-access-policies).</span></span>
  
<span data-ttu-id="3508f-163">請瀏覽這些設定，以決定是否要變更 OneDrive 的網站預設設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-163">Visit these settings to decide if you want to change the default settings for OneDrive for Business sites.</span></span> <span data-ttu-id="3508f-164">目前，會複製 SharePoint 系統管理中心的共用和裝置存取設定，並套用到這兩個環境。</span><span class="sxs-lookup"><span data-stu-id="3508f-164">Currently, the sharing and device access settings are duplicated from the SharePoint Online admin center and apply to both environments.</span></span>
  
## <a name="team-and-sharepoint-site-configuration"></a><span data-ttu-id="3508f-165">小組和 SharePoint 網站設定</span><span class="sxs-lookup"><span data-stu-id="3508f-165">Team and SharePoint site configuration</span></span>

<span data-ttu-id="3508f-166">下表摘要說明本文先前所述的每個小組及其基礎 SharePoint 網站的設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-166">The following table summarizes the configuration for each of the team sites described earlier in this article.</span></span> <span data-ttu-id="3508f-167">您可以使用這些設定作為建議的起點，並依據組織需求調整網站類型與設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-167">Use these configurations as starting point recommendations and adjust the site types and configurations to meet the needs of your organization.</span></span> <span data-ttu-id="3508f-168">並非每個組織都需要所有類型的小組。</span><span class="sxs-lookup"><span data-stu-id="3508f-168">Not every organization needs every type of site.</span></span> <span data-ttu-id="3508f-169">只有少數組織的小組會需要高度機密的保護。</span><span class="sxs-lookup"><span data-stu-id="3508f-169">Only a small number of organizations require highly confidential protection.</span></span>
  
||||||
|:-----|:-----|:-----|:-----|:-----|
||<span data-ttu-id="3508f-170">**基準保護 #1**</span><span class="sxs-lookup"><span data-stu-id="3508f-170">**Baseline protection #1**</span></span> <br/> |<span data-ttu-id="3508f-171">**基準保護 #2**</span><span class="sxs-lookup"><span data-stu-id="3508f-171">**Baseline protection #2**</span></span> <br/> |<span data-ttu-id="3508f-172">**敏感性保護**</span><span class="sxs-lookup"><span data-stu-id="3508f-172">**Sensitive protection**</span></span> <br/> |<span data-ttu-id="3508f-173">**高度機密**</span><span class="sxs-lookup"><span data-stu-id="3508f-173">**Highly confidential**</span></span> <br/> |
|<span data-ttu-id="3508f-174">描述</span><span class="sxs-lookup"><span data-stu-id="3508f-174">Description</span></span>  <br/> |<span data-ttu-id="3508f-175">開放給組織內部探索及共同作業的公開小組。</span><span class="sxs-lookup"><span data-stu-id="3508f-175">Public team with open discovery and collaboration within the organization.</span></span>  <br/> |<span data-ttu-id="3508f-176">允許群組外部共用基礎 SharePoint 網站的私人小組。</span><span class="sxs-lookup"><span data-stu-id="3508f-176">Private team with sharing of the underlying SharePoint site allowed outside the group.</span></span>  <br/> |<span data-ttu-id="3508f-177">僅允許網站成員共用基礎 SharePoint 網站的私人小組。</span><span class="sxs-lookup"><span data-stu-id="3508f-177">Private team, but sharing of the underlying SharePoint site is only allowed to members of the site.</span></span> <span data-ttu-id="3508f-178">當使用者嘗試將檔案傳送到組織外部時，DLP 會對其發出警告。</span><span class="sxs-lookup"><span data-stu-id="3508f-178">DLP warns users when attempting to send files outside the organization.</span></span>  <br/> |<span data-ttu-id="3508f-179">檔案會隨附敏感度標籤以進行加密和權限授與的私人小組。</span><span class="sxs-lookup"><span data-stu-id="3508f-179">Private team with sensitivity labels for file encryption and permissions that travel with the file.</span></span> <span data-ttu-id="3508f-180">DLP 可防止使用者將檔案傳送到組織外部。</span><span class="sxs-lookup"><span data-stu-id="3508f-180">DLP prevents users from sending files outside the organization.</span></span>  <br/> |
|<span data-ttu-id="3508f-181">私用或公用的小組網站</span><span class="sxs-lookup"><span data-stu-id="3508f-181">Private or public team site</span></span>  <br/> |<span data-ttu-id="3508f-182">公用</span><span class="sxs-lookup"><span data-stu-id="3508f-182">Public</span></span>  <br/> |<span data-ttu-id="3508f-183">Private</span><span class="sxs-lookup"><span data-stu-id="3508f-183">Private</span></span>  <br/> |<span data-ttu-id="3508f-184">Private</span><span class="sxs-lookup"><span data-stu-id="3508f-184">Private</span></span>  <br/> |<span data-ttu-id="3508f-185">Private</span><span class="sxs-lookup"><span data-stu-id="3508f-185">Private</span></span>  <br/> |
|<span data-ttu-id="3508f-186">誰可以存取？</span><span class="sxs-lookup"><span data-stu-id="3508f-186">Who has access?</span></span>  <br/> |<span data-ttu-id="3508f-187">組織中所有人，包括 B2B 使用者。</span><span class="sxs-lookup"><span data-stu-id="3508f-187">Everybody in the organization, including B2B users and guest users.</span></span>  <br/> |<span data-ttu-id="3508f-188">僅限網站的成員。</span><span class="sxs-lookup"><span data-stu-id="3508f-188">Members of the site only.</span></span> <span data-ttu-id="3508f-189">其他人可以要求存取權。</span><span class="sxs-lookup"><span data-stu-id="3508f-189">Others can request access.</span></span>  <br/> |<span data-ttu-id="3508f-190">僅限小組的成員。</span><span class="sxs-lookup"><span data-stu-id="3508f-190">Members of the site only.</span></span> <span data-ttu-id="3508f-191">其他人可要求存取基礎網站，由小組擁有者核准。</span><span class="sxs-lookup"><span data-stu-id="3508f-191">Others can request access to the underlying site, which is approved by a team owner.</span></span>  <br/> |<span data-ttu-id="3508f-192">僅限成員。</span><span class="sxs-lookup"><span data-stu-id="3508f-192">Members only.</span></span> <span data-ttu-id="3508f-193">其他人無法要求存取基礎網站。</span><span class="sxs-lookup"><span data-stu-id="3508f-193">Others cannot request access to the underlying site.</span></span>  <br/> |
|<span data-ttu-id="3508f-194">網站層級的共用控制</span><span class="sxs-lookup"><span data-stu-id="3508f-194">Site-level sharing controls</span></span>  <br/> |<span data-ttu-id="3508f-p119">允許與任何人共用。 預設設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-p119">Sharing allowed with anybody. Default settings.</span></span>  <br/> |<span data-ttu-id="3508f-p120">允許與任何人共用。 預設設定。</span><span class="sxs-lookup"><span data-stu-id="3508f-p120">Sharing allowed with anybody. Default settings.</span></span>  <br/> |<span data-ttu-id="3508f-199">成員無法共用網站的存取權。</span><span class="sxs-lookup"><span data-stu-id="3508f-199">Members cannot share access to the site.</span></span>  <br/> <span data-ttu-id="3508f-200">非成員可要求存取網站，但這些要求需由小組的群組擁有者處理。</span><span class="sxs-lookup"><span data-stu-id="3508f-200">Non-members can request access to the site, but these requests need to be addressed by a site administrator.</span></span>  <br/> |<span data-ttu-id="3508f-201">成員無法共用網站的存取權。</span><span class="sxs-lookup"><span data-stu-id="3508f-201">Members cannot share access to the site.</span></span>  <br/> <span data-ttu-id="3508f-202">非成員無法要求存取網站或其內容。</span><span class="sxs-lookup"><span data-stu-id="3508f-202">Non-members cannot request access to the site or contents.</span></span>  <br/> |
|<span data-ttu-id="3508f-203">網站層級的裝置存取控制</span><span class="sxs-lookup"><span data-stu-id="3508f-203">Site-level device access controls</span></span>  <br/> |<span data-ttu-id="3508f-204">無額外控制。</span><span class="sxs-lookup"><span data-stu-id="3508f-204">No additional controls.</span></span>  <br/> |<span data-ttu-id="3508f-205">無額外控制。</span><span class="sxs-lookup"><span data-stu-id="3508f-205">No additional controls.</span></span>  <br/> |<span data-ttu-id="3508f-p121">防止使用者下載檔案到不相容或非加入網域的裝置。如此一來，所有其他裝置僅可進行瀏覽器存取。</span><span class="sxs-lookup"><span data-stu-id="3508f-p121">Prevents users from downloading files to non-compliant or non-domain joined devices. This allows browser-only access from all other devices.</span></span>  <br/> |<span data-ttu-id="3508f-208">封鎖將檔案下載至不相容或非加入網域的裝置。</span><span class="sxs-lookup"><span data-stu-id="3508f-208">Block downloading of files to non-compliant or non-domain joined devices.</span></span>  <br/> |
|<span data-ttu-id="3508f-209">保留標籤</span><span class="sxs-lookup"><span data-stu-id="3508f-209">Retention labels</span></span>  <br/> |<span data-ttu-id="3508f-210">內部公用</span><span class="sxs-lookup"><span data-stu-id="3508f-210">Internal Public</span></span>  <br/> |<span data-ttu-id="3508f-211">Private</span><span class="sxs-lookup"><span data-stu-id="3508f-211">Private</span></span>  <br/> |<span data-ttu-id="3508f-212">敏感性</span><span class="sxs-lookup"><span data-stu-id="3508f-212">Sensitive</span></span>  <br/> |<span data-ttu-id="3508f-213">高度機密</span><span class="sxs-lookup"><span data-stu-id="3508f-213">Highly Confidential</span></span>  <br/> |
|<span data-ttu-id="3508f-214">DLP 原則</span><span class="sxs-lookup"><span data-stu-id="3508f-214">DLP policies</span></span>  <br/> |||<span data-ttu-id="3508f-215">當使用者將標記為「敏感性」的檔案傳送到組織外部時，會對其發出警告。</span><span class="sxs-lookup"><span data-stu-id="3508f-215">Warn users when sending files that are labeled as Sensitive outside the organization.</span></span>  <br/> <span data-ttu-id="3508f-216">若要封鎖敏感性資料類型的外部共用，例如信用卡號碼或其他個人資料，您可以為這些資料類型 (包括您設定的自訂資料類型) 設定額外的 DLP 原則。</span><span class="sxs-lookup"><span data-stu-id="3508f-216">To block external sharing of sensitive data types, such as credit card numbers or other personal data, you can configure additional DLP policies for these data types (including custom data types you configure).</span></span>  <br/> |<span data-ttu-id="3508f-p122">封鎖使用者，使其無法將標示為高度機密的檔案傳送到組織外部。 允許使用者提供理由來覆寫這項預設，包括共用檔案的對象。</span><span class="sxs-lookup"><span data-stu-id="3508f-p122">Block users from sending files that are labeled as highly confidential outside organization. Allow users to override this by providing justification, including who they are sharing the file with.</span></span>  <br/> |
|<span data-ttu-id="3508f-219">敏感度標籤</span><span class="sxs-lookup"><span data-stu-id="3508f-219">Sensitivity labels</span></span>  <br/> ||||<span data-ttu-id="3508f-220">使用敏感度標籤可為檔案加密並授與其權限。</span><span class="sxs-lookup"><span data-stu-id="3508f-220">Use sensitivity labels to automatically encrypt and grant permissions to files.</span></span> <span data-ttu-id="3508f-221">這項保護會隨附於檔案，以防檔案從基礎 SharePoint 網站中外洩。</span><span class="sxs-lookup"><span data-stu-id="3508f-221">This protection travels with the files in case they are leaked.</span></span>  <br/> |
   
<span data-ttu-id="3508f-222">如需此解決方案中四種不同小組類型的部署步驟，請參閱[部署三種檔案保護層級的小組](deploy-teams-three-tiers.md)。</span><span class="sxs-lookup"><span data-stu-id="3508f-222">For the steps to deploy the four different types of SharePoint Online team sites in this solution, see [Deploy sites for three tiers of protection](deploy-teams-three-tiers.md).</span></span>
  
## <a name="office-365-retention-labels"></a><span data-ttu-id="3508f-223">Office 365 保留標籤</span><span class="sxs-lookup"><span data-stu-id="3508f-223">Office 365 retention labels</span></span>

<span data-ttu-id="3508f-224">建議您在含有敏感性資料的環境中使用保留標籤。</span><span class="sxs-lookup"><span data-stu-id="3508f-224">Using retention labels is recommended for environments with sensitive data.</span></span> <span data-ttu-id="3508f-225">設定並發佈保留標籤之後：</span><span class="sxs-lookup"><span data-stu-id="3508f-225">After you configure and publish retention labels:</span></span>
  
- <span data-ttu-id="3508f-226">您可以將預設標籤套用至某小組的基礎 SharePoint 網站中的文件庫，讓該小組的 [檔案]\*\*\*\* 區段中所有的文件都具有預設標籤。</span><span class="sxs-lookup"><span data-stu-id="3508f-226">You can apply a default label to a document library in the underlying SharePoint site for a team, so that all documents in the **Files** section of the team get the default label.</span></span> 
    
- <span data-ttu-id="3508f-227">您可以自動將標籤套用到內容 (如果內容符合特定條件的話)。</span><span class="sxs-lookup"><span data-stu-id="3508f-227">You can apply labels to content automatically if it matches specific conditions.</span></span>
    
- <span data-ttu-id="3508f-228">您可以套用以保留標籤為基礎的 DLP 原則。</span><span class="sxs-lookup"><span data-stu-id="3508f-228">You can apply DLP policies that are based on retention labels.</span></span>
    
- <span data-ttu-id="3508f-229">組織中的人員可手動將標籤套用至 Outlook 網頁版、Outlook 2010 和更新版本、OneDrive、SharePoint 和 Office 365 群組中的內容。</span><span class="sxs-lookup"><span data-stu-id="3508f-229">Enable people in your organization to apply a label manually to content in Outlook on the web, Outlook 2010 and later, OneDrive for Business, SharePoint Online, and Office 365 groups.</span></span> <span data-ttu-id="3508f-230">使用者通常最清楚自己使用的內容類型，因此可以對其分類並套用適當的 DLP 原則。</span><span class="sxs-lookup"><span data-stu-id="3508f-230">Users often know best what type of content they’re working with, so they can classify it and have the appropriate DLP policy applied.</span></span>
    
<span data-ttu-id="3508f-231">如圖例所示，此解決方案包括建立下列保留標籤：</span><span class="sxs-lookup"><span data-stu-id="3508f-231">As illustrated, this solution includes creating the following retention labels:</span></span>
  
- <span data-ttu-id="3508f-232">高度機密</span><span class="sxs-lookup"><span data-stu-id="3508f-232">Highly Confidential</span></span>
    
- <span data-ttu-id="3508f-233">敏感性</span><span class="sxs-lookup"><span data-stu-id="3508f-233">Sensitive</span></span>
    
- <span data-ttu-id="3508f-234">Private</span><span class="sxs-lookup"><span data-stu-id="3508f-234">Private</span></span>
    
- <span data-ttu-id="3508f-235">內部公用</span><span class="sxs-lookup"><span data-stu-id="3508f-235">Internal Public</span></span>
    
<span data-ttu-id="3508f-p126">這些標籤會對應到本文稍早的圖例與圖表中的建議網站。此解決方案建議您設定 DLP 原則，以協助避免標示為「敏感性」和「高度機密」的檔案外洩。</span><span class="sxs-lookup"><span data-stu-id="3508f-p126">These labels are mapped to the recommended sites in the illustrations and charts earlier in this article. This solution recommends configuring DLP policies to help prevent the leakage of files labeled as Sensitive and Highly Confidential.</span></span>
  
<span data-ttu-id="3508f-238">如需在此解決方案中設定保留標籤和 DLP 原則的步驟，請參閱[使用保留標籤與 DLP 來保護小組中的檔案](deploy-teams-retention-DLP.md)。</span><span class="sxs-lookup"><span data-stu-id="3508f-238">For the steps to configure retention labels and DLP policies in this solution, see [Protect SharePoint Online files with retention labels and DLP](deploy-teams-retention-DLP.md).</span></span>
  
## <a name="sensitivity-labels"></a><span data-ttu-id="3508f-239">敏感度標籤</span><span class="sxs-lookup"><span data-stu-id="3508f-239">Sensitivity labels</span></span> 

<span data-ttu-id="3508f-240">若您的安全性案例有需要，您可以使用敏感度標籤來套用可隨時追蹤檔案的保護。</span><span class="sxs-lookup"><span data-stu-id="3508f-240">If warranted for your security scenario, you can use sensitivity labels to apply protections that follow the files wherever they go.</span></span> <span data-ttu-id="3508f-241">Microsoft 365 合規性中心的敏感度標籤和 Azure 資訊保護標籤是相同的。</span><span class="sxs-lookup"><span data-stu-id="3508f-241">Sensitivity labels in the Microsoft 365 compliance center and Azure Information Protection labels are the same.</span></span> <span data-ttu-id="3508f-242">採用此解決方案時，建議您使用敏感度標籤或子標籤，來加密需要以最高安全性層級保護的檔案，和授與其權限。</span><span class="sxs-lookup"><span data-stu-id="3508f-242">For this solution, we recommend you use a scoped Azure Information Protection policy and a sub-label of the Highly Confidential label to encrypt and grant permissions to files that need to be protected with the highest level of security.</span></span> 

<span data-ttu-id="3508f-243">如需詳細資訊，請參閱[敏感度標籤概觀](../../compliance/sensitivity-labels.md)。</span><span class="sxs-lookup"><span data-stu-id="3508f-243">For more information, see [Overview of sensitivity labels](../../compliance/sensitivity-labels.md).</span></span>

<span data-ttu-id="3508f-244">如需在此解決方案中設定敏感度標籤的步驟，請參閱[使用靈敏度標籤保護小組中的檔案](deploy-teams-sensitivity-labels.md)。</span><span class="sxs-lookup"><span data-stu-id="3508f-244">For the steps to configure sensitivity labels in this solution, see [Protect files in teams with sensitivity labels](deploy-teams-sensitivity-labels.md).</span></span>
   
   
## <a name="see-also"></a><span data-ttu-id="3508f-245">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3508f-245">See also</span></span>
  
[<span data-ttu-id="3508f-246">雲端採用和混合式解決方案</span><span class="sxs-lookup"><span data-stu-id="3508f-246">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  