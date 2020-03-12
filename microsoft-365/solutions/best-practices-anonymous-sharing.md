---
title: 未驗證共用的最佳做法
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: sharepoint-online
ms.collection: SPO_Content
localization_priority: Priority
f1.keywords: NOCSH
description: 了解與未驗證使用者共用檔案和資料夾的最佳做法。
ms.openlocfilehash: bf6472c21f97ed9c278a4cf8ba5fbf2803579d53
ms.sourcegitcommit: 21338a9287017a66298e0ff557e80051946ebf13
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/11/2020
ms.locfileid: "42604550"
---
# <a name="best-practices-for-sharing-files-and-folders-with-unauthenticated-users"></a><span data-ttu-id="c41aa-103">與未驗證使用者共用檔案和資料夾的最佳做法</span><span class="sxs-lookup"><span data-stu-id="c41aa-103">Best practices for sharing files and folders with unauthenticated users</span></span>

<span data-ttu-id="c41aa-104">未驗證共用 (*任何人*連結) 在許多案例下都相當方便。</span><span class="sxs-lookup"><span data-stu-id="c41aa-104">Unauthenticated sharing (*Anyone* links) can be convenient and is useful in various scenarios.</span></span> <span data-ttu-id="c41aa-105">*任何人*連結為共用最簡單的方式：人員可以不經驗證就開啟連結，且可隨意將它傳送給其他人。</span><span class="sxs-lookup"><span data-stu-id="c41aa-105">*Anyone* links are the easiest way to share: people can open the link without authentication and are free to pass it on to others.</span></span>

<span data-ttu-id="c41aa-106">一般來說，並非組織中的所有內容都適合進行未驗證共用。</span><span class="sxs-lookup"><span data-stu-id="c41aa-106">Usually, not all content in an organization is appropriate for unauthenticated sharing.</span></span> <span data-ttu-id="c41aa-107">本文涵蓋可協助您建立一個環境的選項，您的使用者能夠在該環境中未驗證共用檔案和資料夾，但在其中有一些既有措施可協助保護組織內容的安全。</span><span class="sxs-lookup"><span data-stu-id="c41aa-107">This article covers the options available to help you create an environment where your users can use unauthenticated sharing of files and folders, but where there are safeguards in place to help protect your organization's content.</span></span>

> [!NOTE]
> <span data-ttu-id="c41aa-108">若要讓未驗證共用運作，您必須為組織以及您將使用的個別網站或小組啟用該功能。</span><span class="sxs-lookup"><span data-stu-id="c41aa-108">For unauthenticated sharing to work, you must enable it for your organization and for the individual site or team that you'll be using.</span></span> <span data-ttu-id="c41aa-109">如需您要啟用的案例，請參閱[與組織外部人員共同作業](collaborate-with-people-outside-your-organization.md)。</span><span class="sxs-lookup"><span data-stu-id="c41aa-109">See [Collaborating with people outside your organization](collaborate-with-people-outside-your-organization.md) for the scenario that you want to enable.</span></span>

## <a name="set-an-expiration-date-for-anyone-links"></a><span data-ttu-id="c41aa-110">設定任何人連結的到期日</span><span class="sxs-lookup"><span data-stu-id="c41aa-110">Set an expiration date for Anyone links</span></span>

<span data-ttu-id="c41aa-111">檔案通常會長時間儲存在網站、群組和小組。</span><span class="sxs-lookup"><span data-stu-id="c41aa-111">Files are often stored in sites, groups, and teams for long periods of time.</span></span> <span data-ttu-id="c41aa-112">有時候，有一些資料保留原則會要求將檔案保留數年。</span><span class="sxs-lookup"><span data-stu-id="c41aa-112">Occasionally there are data retention policies that require files to be retained for years.</span></span> <span data-ttu-id="c41aa-113">如果將這類檔案與未驗證的人員共用，可能導致未來非預期地存取和變更這些檔案。</span><span class="sxs-lookup"><span data-stu-id="c41aa-113">If such files are shared with unauthenticated people, this could lead to unexpected access and changes to files in the future.</span></span> <span data-ttu-id="c41aa-114">若要降低此可能性，您可以為*任何人*連結設定到期時間。</span><span class="sxs-lookup"><span data-stu-id="c41aa-114">To mitigate this possibility, you can configure an expiration time for *Anyone* links.</span></span>

<span data-ttu-id="c41aa-115">*任何人*連結到期後，就無法再用來存取內容。</span><span class="sxs-lookup"><span data-stu-id="c41aa-115">Once an *Anyone* link expires, it can no longer be used to access content.</span></span>

<span data-ttu-id="c41aa-116">設定任何人連結的到期日</span><span class="sxs-lookup"><span data-stu-id="c41aa-116">To set an expiration date for Anyone links</span></span>
1. <span data-ttu-id="c41aa-117">開啟 SharePoint Online 系統管理中心。</span><span class="sxs-lookup"><span data-stu-id="c41aa-117">Open the SharePoint Online admin center.</span></span>
2. <span data-ttu-id="c41aa-118">在左側導覽窗格中，按一下 [共用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-118">In the left navigation, click **Sharing**.</span></span>
3. <span data-ttu-id="c41aa-119">在 [「任何人」連結的進階設定]\*\*\*\* 底下，選取 [這些連結必須在此天數內過期]\*\*\*\* 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="c41aa-119">Under **Advanced settings for "Anyone" links**, select the **These links must expire within this many days** check box.</span></span></br>
   <span data-ttu-id="c41aa-120">![SharePoint 組織層級任何人連結到期設定的螢幕擷取畫面](../media/sharepoint-organization-anyone-link-expiration.png)</span><span class="sxs-lookup"><span data-stu-id="c41aa-120">![Screenshot of SharePoint organization-level Anyone link expiration settings](../media/sharepoint-organization-anyone-link-expiration.png)</span></span>
4. <span data-ttu-id="c41aa-121">在方塊中輸入天數，然後按一下 [儲存]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-121">Type a number of days in the box, and then click **Save**.</span></span>

<span data-ttu-id="c41aa-122">請注意，*任何人*連結到期之後，就可以使用新的*任何人*連結重新共用檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="c41aa-122">Note that once an *Anyone* link expires, the file or folder can be re-shared with a new *Anyone* link.</span></span>

## <a name="set-link-permissions"></a><span data-ttu-id="c41aa-123">設定連結權限</span><span class="sxs-lookup"><span data-stu-id="c41aa-123">Set link permissions</span></span>

<span data-ttu-id="c41aa-124">根據預設，檔案的*任何人*連結會允許人員編輯檔案，而資料夾的*任何人*連結則會允許人員編輯和檢視檔案，以及上傳新檔案到資料夾。</span><span class="sxs-lookup"><span data-stu-id="c41aa-124">By default, *Anyone* links for a file allow people to edit the file, and *Anyone* links for a folder allow people to edit and view files, and upload new files to the folder.</span></span> <span data-ttu-id="c41aa-125">您可以獨立將檔案和資料夾的這些權限變更為僅供檢視。</span><span class="sxs-lookup"><span data-stu-id="c41aa-125">You can change these permissions for files and for folders independently to view-only.</span></span>

<span data-ttu-id="c41aa-126">如果您想要允許未驗證共用，但擔心未驗證的人員修改組織的內容，請考慮將檔案和資料夾權限設定為 [檢視]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-126">If you want to allow unauthenticated sharing, but are concerned about unauthenticated people modifying your organization's content, consider setting the file and folder permissions to **View**.</span></span>

<span data-ttu-id="c41aa-127">設定任何人連結的權限</span><span class="sxs-lookup"><span data-stu-id="c41aa-127">To set permissions for Anyone links</span></span>
1. <span data-ttu-id="c41aa-128">開啟 SharePoint Online 系統管理中心。</span><span class="sxs-lookup"><span data-stu-id="c41aa-128">Open the SharePoint Online admin center.</span></span>
2. <span data-ttu-id="c41aa-129">在左側導覽窗格中，按一下 [共用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-129">In the left navigation, click **Sharing**.</span></span>
3. <span data-ttu-id="c41aa-130">在 [「任何人」連結的進階設定]\*\*\*\* 底下，選取您要使用的檔案和資料夾權限。</span><span class="sxs-lookup"><span data-stu-id="c41aa-130">Under **Advanced settings for "Anyone" links**, select the file and folder permissions that you want to use.</span></span></br>
   <span data-ttu-id="c41aa-131">![SharePoint 組織層級任何人連結權限設定的螢幕擷取畫面](../media/sharepoint-organization-anyone-link-permissions.png)</span><span class="sxs-lookup"><span data-stu-id="c41aa-131">![Screenshot of SharePoint organization-level Anyone link permissions settings](../media/sharepoint-organization-anyone-link-permissions.png)</span></span>

<span data-ttu-id="c41aa-132">將*任何人*連結設為 [檢視]\*\*\*\* 時，使用者仍然可以與來賓共用檔案和資料夾，並使用*特定人員*連結提供編輯權限。</span><span class="sxs-lookup"><span data-stu-id="c41aa-132">With *Anyone* links set to **View**, users can still share files and folders with guests and give them edit permissions by using *Specific people* links.</span></span> <span data-ttu-id="c41aa-133">這些連結要求組織外的人員驗證為來賓身分，而您可以追蹤和稽核使用這些連結共用的檔案和資料夾上的來賓活動。</span><span class="sxs-lookup"><span data-stu-id="c41aa-133">These links require people outside your organization to authenticate as guests, and you can track and audit guest activity on files and folders shared with these links.</span></span>

## <a name="set-default-link-type-to-only-work-for-people-in-your-organization"></a><span data-ttu-id="c41aa-134">將預設連結類型設定為僅適用組織中的人員</span><span class="sxs-lookup"><span data-stu-id="c41aa-134">Set default link type to only work for people in your organization</span></span>

<span data-ttu-id="c41aa-135">為組織啟用*任何人*共用時，預設的共用連結一般會設定為**任何人**。</span><span class="sxs-lookup"><span data-stu-id="c41aa-135">When *Anyone* sharing is enabled for your organization, the default sharing link is normally set to **Anyone**.</span></span> <span data-ttu-id="c41aa-136">雖然這對使用者而言很方便，但可能會增加無意間未驗證共用的風險。</span><span class="sxs-lookup"><span data-stu-id="c41aa-136">While this can be convenient for users, it can increase the risk of unintentional unauthenticated sharing.</span></span> <span data-ttu-id="c41aa-137">如果使用者在共用機密文件時忘記變更連結類型，他們可能會意外建立不需要驗證的共用連結。</span><span class="sxs-lookup"><span data-stu-id="c41aa-137">If a user forgets to change the link type while sharing a sensitive document, they might accidentally create a sharing link that doesn't require authentication.</span></span>

<span data-ttu-id="c41aa-138">您可以透過將預設連結設定變更為僅適用組織內部人員的連結，來降低此風險。</span><span class="sxs-lookup"><span data-stu-id="c41aa-138">You can mitigate this risk by changing the default link setting to a link that only works for people inside your organization.</span></span> <span data-ttu-id="c41aa-139">這麼一來，想要進行未驗證共用的使用者，必須特別選取該選項。</span><span class="sxs-lookup"><span data-stu-id="c41aa-139">Users who want to share with unauthenticated people would then have to specifically select that option.</span></span>

<span data-ttu-id="c41aa-140">設定預設的檔案和資料夾共用連結</span><span class="sxs-lookup"><span data-stu-id="c41aa-140">To set the default file and folder sharing link</span></span>
1. <span data-ttu-id="c41aa-141">在 SharePoint 管理中心中，按一下左側導覽窗格中的 [共用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-141">In the SharePoint admin center, in the left navigation, click **Sharing**.</span></span>
2. <span data-ttu-id="c41aa-142">在 [檔案與資料夾連結]\*\*\*\* 下，選取 [只有貴組織中的人員]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-142">Under **File and folder links**, select **Only people in your organization**.</span></span></br>
   <span data-ttu-id="c41aa-143">![SharePoint 預設連結類型設定的螢幕擷取畫面](../media/sharepoint-default-sharing-link-company-link.png)</span><span class="sxs-lookup"><span data-stu-id="c41aa-143">![Screenshot of SharePoint default link type setting](../media/sharepoint-default-sharing-link-company-link.png)</span></span>
3. <span data-ttu-id="c41aa-144">按一下 [儲存]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c41aa-144">Click **Save**</span></span>

## <a name="protect-against-malicious-files"></a><span data-ttu-id="c41aa-145">防範惡意檔案</span><span class="sxs-lookup"><span data-stu-id="c41aa-145">Protect against malicious files</span></span>

<span data-ttu-id="c41aa-146">允許匿名使用者上傳檔案時，可能會增加某人上傳惡意檔案的風險。</span><span class="sxs-lookup"><span data-stu-id="c41aa-146">When you allow anonymous users to upload files, you're at an increased risk of someone uploading a malicious file.</span></span> <span data-ttu-id="c41aa-147">在 Microsoft 365 中，您可以使用進階威脅防護中的*安全附件*功能，自動掃描發現不安全的已上傳檔案和隔離檔案。</span><span class="sxs-lookup"><span data-stu-id="c41aa-147">In Microsoft 365, you can use the *safe attachments* feature in Advanced Threat Protection to automatically scan uploaded files and quarantine files that are found to be unsafe.</span></span>

<span data-ttu-id="c41aa-148">開啟安全附件</span><span class="sxs-lookup"><span data-stu-id="c41aa-148">To turn on safe attachments</span></span>
1. <span data-ttu-id="c41aa-149">開啟 [Microsoft 365 安全性](https://security.microsoft.com)系統管理中心。</span><span class="sxs-lookup"><span data-stu-id="c41aa-149">Open the [Microsoft 365 security](https://security.microsoft.com) admin center.</span></span>
2. <span data-ttu-id="c41aa-150">在左側導覽窗格中，按一下 [原則]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-150">In the left navigation, click **Policies**.</span></span>
3. <span data-ttu-id="c41aa-151">在 [威脅防護]\*\*\*\* 底下，按一下 [ATP 安全附件 (Office 365)]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-151">Under **Threat protection**, click **ATP safe attachments (Office 365)**.</span></span>
4. <span data-ttu-id="c41aa-152">選取 [為 SharePoint、OneDrive 與 Microsoft Teams 開啟 ATP]\*\*\*\* 核取方塊，然後按一下 [儲存]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-152">Select the **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams** check box, and then click **Save**.</span></span></br>
   <span data-ttu-id="c41aa-153">![安全性與合規性中心安全附件設定的螢幕擷取畫面](../media/safe-attachments-setting.png)</span><span class="sxs-lookup"><span data-stu-id="c41aa-153">![Screenshot of the safe attachments setting in the Security and Compliance center](../media/safe-attachments-setting.png)</span></span>

## <a name="add-copyright-information-to-your-files"></a><span data-ttu-id="c41aa-154">新增著作權資訊至您的檔案</span><span class="sxs-lookup"><span data-stu-id="c41aa-154">Add copyright information to your files</span></span>

<span data-ttu-id="c41aa-155">如果您在 Microsoft 365 合規性系統管理中心使用敏感度標籤，即可以設定您的標籤，以自動新增浮水印或頁首或頁尾至組織的 Office 文件中。</span><span class="sxs-lookup"><span data-stu-id="c41aa-155">If you use sensitivity labels in the Microsoft 365 Compliance admin center, you can configure your labels to add a watermark or a header or footer automatically to your organization's Office documents.</span></span> <span data-ttu-id="c41aa-156">這麼一來，您就可以確定共用的檔案包含著作權或其他擁有權資訊。</span><span class="sxs-lookup"><span data-stu-id="c41aa-156">In this way, you can make sure that shared files contain copyright or other ownership information.</span></span>

<span data-ttu-id="c41aa-157">新增頁尾至標籤的檔案</span><span class="sxs-lookup"><span data-stu-id="c41aa-157">To add a footer to a labeled file</span></span>
1. <span data-ttu-id="c41aa-158">開啟 [Microsoft 365 合規性系統管理中心](https://compliance.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="c41aa-158">Open the [Microsoft 365 compliance admin center](https://compliance.microsoft.com).</span></span>
2. <span data-ttu-id="c41aa-159">在左側導覽窗格中，於 [分類]\*\*\*\* 底下，按一下 [敏感度標籤]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-159">In the left navigation, under **Classification**, click **Sensitivity labels**.</span></span>
3. <span data-ttu-id="c41aa-160">按一下您要新增頁尾的標籤，然後按一下 [編輯標籤]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-160">Click the label that you want to have add a footer, and then click **Edit label**.</span></span>
4. <span data-ttu-id="c41aa-161">按一下 [內容標示]\*\*\*\* 索引標籤，然後 [開啟]\*\*\*\* 內容標示。</span><span class="sxs-lookup"><span data-stu-id="c41aa-161">Click the **Content marking** tab, and then turn **On** content marking.</span></span>
5. <span data-ttu-id="c41aa-162">選取要新增的文字類型的核取方塊，然後按一下 [自訂文字]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-162">Select the check box for the type of text you want to add, and then click **Customize text**.</span></span>
6. <span data-ttu-id="c41aa-163">輸入要新增至文件的文字，選取需要的文字選項，然後按一下 [儲存]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-163">Type the text that you want added to your documents, select the text options that you want, and then click **Save**.</span></span></br>
   <span data-ttu-id="c41aa-164">![敏感度標籤內容標示設定的螢幕擷取畫面](../media/content-marking-for-anonymous-sharing.png)</span><span class="sxs-lookup"><span data-stu-id="c41aa-164">![Screenshot of the content marking settings for a sensitivity label](../media/content-marking-for-anonymous-sharing.png)</span></span>
7. <span data-ttu-id="c41aa-165">按一下 [儲存]\*\*\*\*，然後按一下 [關閉]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c41aa-165">Click **Save**, and then click **Close**.</span></span>

<span data-ttu-id="c41aa-166">為標籤啟用內容標示後，當使用者套用該標籤，您指定的文字就會新增至 Office 文件中。</span><span class="sxs-lookup"><span data-stu-id="c41aa-166">With content marking enabled for the label, the text you specified will be added to Office documents when a user applies that label.</span></span>

## <a name="see-also"></a><span data-ttu-id="c41aa-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c41aa-167">See Also</span></span>


[<span data-ttu-id="c41aa-168">敏感度標籤概觀</span><span class="sxs-lookup"><span data-stu-id="c41aa-168">Overview of sensitivity labels</span></span>](https://docs.microsoft.com/Office365/SecurityCompliance/sensitivity-labels)

[<span data-ttu-id="c41aa-169">與來賓共用時限制意外暴露檔案</span><span class="sxs-lookup"><span data-stu-id="c41aa-169">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="c41aa-170">建立安全的來賓共用環境</span><span class="sxs-lookup"><span data-stu-id="c41aa-170">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)