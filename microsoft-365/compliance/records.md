---
title: 記錄概觀
ms.author: laurawi
author: laurawi
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: 若要在您的 Office 365 或 Microsoft 組織中執行記錄管理策略，請使用保留標籤將內容宣告為記錄。 然後發佈或自動套用保留記錄標籤。
ms.openlocfilehash: 37f23dcd9c2b94edce99fa55977cb26e1faa4d8e
ms.sourcegitcommit: 9a420b16aaa401a822ccfd9b133977ad8bd1024b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "39637822"
---
# <a name="overview-of-records"></a><span data-ttu-id="86902-104">記錄概觀</span><span class="sxs-lookup"><span data-stu-id="86902-104">Overview of records management planning</span></span>

<span data-ttu-id="86902-105">在 Microsoft 365 中記錄管理可協助組織遵守公司政策、法律和法規義務，同時降低風險和法律責任。</span><span class="sxs-lookup"><span data-stu-id="86902-105">Managing records in Microsoft 365 helps an organization comply with their corporate policies, legal and regulatory obligations while reducing risk and legal liability.</span></span>

<span data-ttu-id="86902-106">將內容宣告為記錄的更深一層意義為：</span><span class="sxs-lookup"><span data-stu-id="86902-106">At a high level, declaring content as a record means that:</span></span>

- <span data-ttu-id="86902-107">項目會變成不可改變的 (無法修改或刪除記錄)</span><span class="sxs-lookup"><span data-stu-id="86902-107">The item becomes immutable (a record can't be modified or deleted)</span></span>

- <span data-ttu-id="86902-108">關於項目的其他活動會予以記錄</span><span class="sxs-lookup"><span data-stu-id="86902-108">Additional activities about the item are logged</span></span>

- <span data-ttu-id="86902-109">在記錄規定的保留期限結束後，會將記錄丟棄。</span><span class="sxs-lookup"><span data-stu-id="86902-109">Records are finally disposed of after their stated lifetime is past.</span></span>

<span data-ttu-id="86902-110">您可以使用[保留標籤](labels.md)將內容分類為記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-110">You can use retention labels to declare content as a record.</span></span> <span data-ttu-id="86902-111">建立保留標籤來宣告記錄後，您可以[發佈](labels.md#how-retention-labels-work-with-retention-label-policies)這些標籤 (讓使用者使用這些標籤將內容分類為記錄)，或[自動套用這些標籤](labels.md#applying-a-retention-label-automatically-based-on-conditions)將您想要的內容分類為記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-111">After you create retention labels that declare records, you can either [publish](labels.md#how-retention-labels-work-with-retention-label-policies) those labels (so that users can use them to classify content as records) or [auto-apply those labels](labels.md#applying-a-retention-label-automatically-based-on-conditions) to content that you want to classify as a record.</span></span> <span data-ttu-id="86902-112">透握使用保留標籤來宣告記錄，您就可以在 Office 365 中實作單一且一致的記錄管理策略，而其他記錄管理功能 (例如 [記錄中心]) 只能套用至 SharePoint 內容。</span><span class="sxs-lookup"><span data-stu-id="86902-112">By using retention labels to declare records, you can implement a single, consistent records-management strategy across all of Office 365, whereas other records-management features such as the Record Center apply only to content in SharePoint Online.</span></span>

<span data-ttu-id="86902-113">請記住以下關於記錄的事實：</span><span class="sxs-lookup"><span data-stu-id="86902-113">Keep the following things in mind about records:</span></span>

  - <span data-ttu-id="86902-114">**記錄是不可改變的。**</span><span class="sxs-lookup"><span data-stu-id="86902-114">**Records are immutable.**</span></span> <span data-ttu-id="86902-115">除了 SharePoint 和商務用 OneDrive，也可以將內容宣告為記錄的保留標籤套用到 Exchange 中的內容。</span><span class="sxs-lookup"><span data-stu-id="86902-115">A retention label that declares content as a record can be applied to content in Exchange, in addition to SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="86902-116">不過，[記錄版本設定](#record-versioning)僅適用於 SharePoint 和 OneDrive，而不適用於 Exchange。</span><span class="sxs-lookup"><span data-stu-id="86902-116">However, [record versioning](#record-versioning) is available only in SharePoint and OneDrive, and not for Exchange.</span></span>

    <span data-ttu-id="86902-117">在 Exchange 中，標示為記錄的內容在最後刪除之前是不可改變的。</span><span class="sxs-lookup"><span data-stu-id="86902-117">In Exchange, content labeled as a record is immutable until its final deletion.</span></span> <span data-ttu-id="86902-118">如果將 Exchange 項目標示為記錄，會發生四件事：</span><span class="sxs-lookup"><span data-stu-id="86902-118">When an item is labeled as a record, four things happen:</span></span>

    - <span data-ttu-id="86902-119">無法永久刪除此項目。</span><span class="sxs-lookup"><span data-stu-id="86902-119">The item can't be permanently deleted.</span></span>

    - <span data-ttu-id="86902-120">無法編輯此項目。</span><span class="sxs-lookup"><span data-stu-id="86902-120">The item can't be edited.</span></span>

    - <span data-ttu-id="86902-121">無法變更此標籤。</span><span class="sxs-lookup"><span data-stu-id="86902-121">The label can't be changed.</span></span>

    - <span data-ttu-id="86902-122">無法移除此標籤。</span><span class="sxs-lookup"><span data-stu-id="86902-122">The label can't be removed.</span></span>

  - <span data-ttu-id="86902-123">**記錄和資料夾。**</span><span class="sxs-lookup"><span data-stu-id="86902-123">**Records and folders**</span></span> <span data-ttu-id="86902-124">您可以將保留標籤套用至 Exchange、SharePoint 或 OneDrive 中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="86902-124">You can apply a retention label to a folder in Exchange, SharePoint, and OneDrive.</span></span> <span data-ttu-id="86902-125">如果資料夾已被標示為記錄，當您將項目移至該資料夾時，該項目也會被標示為記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-125">If a folder is labeled as a record, and you move an item into the folder, the item is labeled as a record.</span></span> <span data-ttu-id="86902-126">即使您將項目移出資料夾，該項目仍會繼續標示為記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-126">When you move the item out of the folder, the item remains labeled as a record.</span></span>

    <span data-ttu-id="86902-127">此外，如果您將套用到資料夾的記錄標籤 (在 SharePoint 和 OneDrive 中) 變更為未將內容宣告為記錄的保留標籤，則該資料夾中的項目會保留其現有的記錄標籤。</span><span class="sxs-lookup"><span data-stu-id="86902-127">Also, if you change the record label that's applied to a folder (in SharePoint and OneDrive) to a retention label that does not declare content as a record, then items in the folder keep their existing  record label.</span></span>

    <span data-ttu-id="86902-128">如需將保留標籤套用至 SharePoint 和 OneDrive 資料夾的詳細資訊，請參閱[將預設的保留標籤套用至 SharePoint 文件庫、資料夾或文件組的所有內容](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set)。</span><span class="sxs-lookup"><span data-stu-id="86902-128">For more information about applying retention labels to SharePoint and OneDrive folders, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>

  - <span data-ttu-id="86902-129">**無法刪除記錄**。</span><span class="sxs-lookup"><span data-stu-id="86902-129">Records can't be deleted</span></span> <span data-ttu-id="86902-130">如果使用者嘗試刪除 Exchange 中的記錄，該項目會移到 [可復原的項目] 資料夾中，如[保留原則如何就地使用內容](retention-policies.md#content-in-mailboxes-and-public-folders)中所述。</span><span class="sxs-lookup"><span data-stu-id="86902-130">If you attempt to delete a record in Exchange, the item is moved to the Recoverable Items folder as described in [How a retention policy works with content in place](retention-policies.md#content-in-mailboxes-and-public-folders).</span></span>

    <span data-ttu-id="86902-131">如果使用者嘗試刪除 SharePoint 中的記錄，您會看到無法刪除該項目的錯誤，且該項目仍會保留在文件庫中。</span><span class="sxs-lookup"><span data-stu-id="86902-131">If you attempt to delete a record in a SharePoint, you see an error that the item wasn't deleted, and the item remains in the library.</span></span>

    ![無法從 SharePoint 中刪除項目的訊息](media/d0020726-1593-4a96-b07c-89b275e75c49.png)

    <span data-ttu-id="86902-133">如果使用者嘗試刪除 OneDrive 中的記錄，該項目會移到 [文件保留庫] 中，如 [保留原則如何就地使用內容](retention-policies.md#content-in-onedrive-accounts-and-sharepoint-sites)中所述。</span><span class="sxs-lookup"><span data-stu-id="86902-133">If you attempt to delete a record in OneDrive, the item is moved to the Preservation Hold library as described in  [How a retention policy works with content in place](retention-policies.md#content-in-onedrive-accounts-and-sharepoint-sites).</span></span>

  - <span data-ttu-id="86902-134">**無法移除記錄標籤。**</span><span class="sxs-lookup"><span data-stu-id="86902-134">**Records labels can't be removed.**</span></span> <span data-ttu-id="86902-135">將記錄標籤套用到某個項目後，只有該位置的系統管理員 (例如 SharePoint 網站的網站集合系統管理員) 可以移除該記錄標籤。</span><span class="sxs-lookup"><span data-stu-id="86902-135">Once a record label has been applied to an item, only the admin of that location (for example, a site collection admin of a SharePoint site) can remove that record label.</span></span>

## <a name="using-retention-labels-to-declare-records"></a><span data-ttu-id="86902-136">使用 [保留標籤] 宣告記錄</span><span class="sxs-lookup"><span data-stu-id="86902-136">Using retention labels to declare records</span></span>

<span data-ttu-id="86902-137">當您建立保留標籤時，可以選擇使用保留標籤將內容分類為記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-137">When you create a retention label, you have the option to use the retention label to classify the content as a record.</span></span> <span data-ttu-id="86902-138">若要將內容宣告為記錄，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="86902-138">To declare content as a record, you need to do the following:</span></span>

1. <span data-ttu-id="86902-139">建立保留標籤。</span><span class="sxs-lookup"><span data-stu-id="86902-139">Create a retention label and DLP policy.</span></span> <span data-ttu-id="86902-140">在 Microsoft 365 合規性中心中，移至 [記錄管理]\*\*\*\* \> [檔案計畫]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="86902-140">In the Microsoft 365 compliance center, go to **Records Management** \> **File Plan**.</span></span> <span data-ttu-id="86902-141">在 [檔案計畫]\*\*\*\* 頁面上，按一下 [建立標籤]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="86902-141">On the **File plan** page, click  **Create a label**.</span></span>

2. <span data-ttu-id="86902-142">在精靈的 [標籤設定]\*\*\*\* 頁面上，選擇設定保留標籤的選項，將內容宣告為記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-142">On the **Label settings** page in the wizard, choose the option to set the retention label to declare content as a record.</span></span><br/>

   ![按一下 [使用標籤以將內容分類為「記錄」] 核取方塊](media/recordversioning6.png)

3. <span data-ttu-id="86902-144">[發佈](labels.md#how-retention-labels-work-with-retention-label-policies)或[自動套用](labels.md#applying-a-retention-label-automatically-based-on-conditions)保留標籤到 SharePoint 網站和/或 OneDrive 帳戶。</span><span class="sxs-lookup"><span data-stu-id="86902-144">[Publish](labels.md#how-retention-labels-work-with-retention-label-policies) or [auto-apply](labels.md#applying-a-retention-label-automatically-based-on-conditions) the retention label to SharePoint sites and/or OneDrive accounts.</span></span> 

### <a name="applying-a-retention-label-to-content"></a><span data-ttu-id="86902-145">將保留標籤套用至內容</span><span class="sxs-lookup"><span data-stu-id="86902-145">Applying a retention label to email by using rules</span></span>

<span data-ttu-id="86902-146">針對 Exchange，任何有信箱寫入存取權的使用者都可以將記錄標籤套用至電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="86902-146">For Exchange, any user with write-access to the mailbox can apply a record label to an email message.</span></span> <span data-ttu-id="86902-147">對於 SharePoint 和 OneDrive 中的內容，預設 [成員] 群組 ([參與] 權限等級) 中的任何使用者都能將記錄標籤套用到內容。</span><span class="sxs-lookup"><span data-stu-id="86902-147">For content in SharePoint and OneDrive, any user in the default Members group (the Contribute permission level) can apply a record label to content.</span></span> <span data-ttu-id="86902-148">套用標籤後，只有網站集合系統管理員可以移除或變更該記錄標籤。</span><span class="sxs-lookup"><span data-stu-id="86902-148">Only a site collection admin can remove or change that record label after it's been applied.</span></span> <span data-ttu-id="86902-149">如先前所述，將內容分類成記錄的保留標籤可自動套用至內容。</span><span class="sxs-lookup"><span data-stu-id="86902-149">As previously explained, a retention label that classifies content as a record can be auto-applied to content.</span></span>

<span data-ttu-id="86902-150">當您將記錄標籤套用至 SharePoint 網站或 OneDrive 帳戶上的文件後，就會顯示以下內容。</span><span class="sxs-lookup"><span data-stu-id="86902-150">Here's what this looks like when a record label is applied to a document on a SharePoint site or OneDrive account.</span></span>
<br/><br/>

<span data-ttu-id="86902-151">:::image type="content" source="media/recordversioning7.png" alt-text="標記為記錄的文件的詳細資料窗格":::</span><span class="sxs-lookup"><span data-stu-id="86902-151">:::image type="content" source="media/recordversioning7.png" alt-text="Details pane for document tagged as a record":::</span></span>

## <a name="record-versioning"></a><span data-ttu-id="86902-152">記錄版本設定</span><span class="sxs-lookup"><span data-stu-id="86902-152">Record versioning</span></span>

<span data-ttu-id="86902-153">記錄管理的重要部分是可將文件宣告為記錄，且該記錄是不可改變的。</span><span class="sxs-lookup"><span data-stu-id="86902-153">An essential part of records management is the ability to declare a document as a record and have that record be immutable.</span></span> <span data-ttu-id="86902-154">同時，如果人們需要建立後續版本，則記錄的不變性可防止在文件上進行共同作業。</span><span class="sxs-lookup"><span data-stu-id="86902-154">At the same time, record immutability prevents collaboration on the document if people need to create subsequent versions.</span></span> <span data-ttu-id="86902-155">例如，您將銷售合約宣告為記錄，但是之後需要使用新的條款來更新合約，並將最新的版本宣告為新記錄，同時保留前一份記錄版本。</span><span class="sxs-lookup"><span data-stu-id="86902-155">For example, you might declare a sales contract as a record, but then need to update the contract with new terms and declare the latest version as a new record while still retaining the previous record version.</span></span> <span data-ttu-id="86902-156">針對這些類型的案例，SharePoint Online 和商務用 OneDrive 現在支援*記錄版本設定*。</span><span class="sxs-lookup"><span data-stu-id="86902-156">For these types of scenarios, SharePoint Online and OneDrive for Business now support *record versioning*.</span></span> <span data-ttu-id="86902-157">不支援 OneNote 筆記本資料夾。</span><span class="sxs-lookup"><span data-stu-id="86902-157">OneNote notebook folders are not supported.</span></span>

<span data-ttu-id="86902-158">若要使用記錄版本設定，第一個步驟是使用 Microsoft 365 合規性中心來建立和發佈保留標籤，以將記錄向所有 SharePoint 網站和/或 OneDrive 帳戶宣告，或將記錄發佈至特定 SharePoint 網站和/或 OneDrive 帳戶。</span><span class="sxs-lookup"><span data-stu-id="86902-158">To use record versioning, the first step is to use the Microsoft 365 compliance center to create and publish retention labels that declare records to all SharePoint sites and/or OneDrive accounts, or publish them to specific SharePoint sites and/or OneDrive accounts.</span></span> <span data-ttu-id="86902-159">下一個步驟是將已發佈的保留記錄標籤套用至文件。</span><span class="sxs-lookup"><span data-stu-id="86902-159">The next step is to apply a published retention record label to a document.</span></span> <span data-ttu-id="86902-160">完成此動作之後，保留標籤旁會顯示名為 [記錄狀態]\*\* 的文件內容，而初始記錄狀態會是 [鎖定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="86902-160">When this is done, a document property, called *Record status* is displayed next to the retention label, and the initial record status will be **Locked**.</span></span> <span data-ttu-id="86902-161">這個時候可以執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="86902-161">At this point, you can do the following things:</span></span>

  - <span data-ttu-id="86902-162">**解鎖並鎖定 [記錄狀態] 內容，持續編輯並將文件的個別版本宣告為記錄。**</span><span class="sxs-lookup"><span data-stu-id="86902-162">**Continually edit and declare individual versions of the document as records, by unlocking and locking the Record status property.**</span></span> <span data-ttu-id="86902-163">當 [記錄狀態]\*\*\*\* 內容設定為 [鎖定]\*\*\*\* 時，只會保留宣告為記錄的版本。</span><span class="sxs-lookup"><span data-stu-id="86902-163">Only the versions declared as records are retained when the **Record status** property is set to **Locked**.</span></span> <span data-ttu-id="86902-164">這可降低保留不必要文件版本和複本的風險。</span><span class="sxs-lookup"><span data-stu-id="86902-164">This reduces the risk of retaining unnecessary versions and copies of the document.</span></span>

  - <span data-ttu-id="86902-165">**將記錄自動儲存在位於網站集合內的就地記錄儲存庫中。**</span><span class="sxs-lookup"><span data-stu-id="86902-165">**Have the records automatically stored in an in-place records repository located within the site collection.**</span></span> <span data-ttu-id="86902-166">SharePoint 和 OneDrive 中的每個網站集合會在其 [文件保留庫] 中保留內容。</span><span class="sxs-lookup"><span data-stu-id="86902-166">Each site collection in SharePoint and OneDrive preserves content in its Preservation Hold library.</span></span> <span data-ttu-id="86902-167">記錄版本會儲存在此文件庫的 [記錄] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="86902-167">Record versions are stored in the Records folder in this library.</span></span>

  - <span data-ttu-id="86902-168">**維護包含所有版本的長青文件。**</span><span class="sxs-lookup"><span data-stu-id="86902-168">**Maintain an evergreen document that contains all versions.**</span></span> <span data-ttu-id="86902-169">根據預設，每個 SharePoint 和 OneDrive 文件在項目功能表上都會有版本歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-169">By default, each SharePoint and OneDrive document has a version history available on the item menu.</span></span> <span data-ttu-id="86902-170">在這個版本歷程記錄中，您可以輕鬆查看記錄的版本，並檢視這些文件。</span><span class="sxs-lookup"><span data-stu-id="86902-170">In this version history, you can easily see which versions are records and view those documents.</span></span>

<span data-ttu-id="86902-171">如果任何文件的保留標籤會將項目宣告為記錄，則會自動提供記錄版本設定。</span><span class="sxs-lookup"><span data-stu-id="86902-171">Record versioning is automatically available for any document that has a retention label that declares the item as a record.</span></span> <span data-ttu-id="86902-172">當使用者透過 [詳細資料] 窗格查看文件內容時，系統會將 [記錄狀態]\*\*\*\* 從 [鎖定]\*\*\*\* 切換為 [解除鎖定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="86902-172">When a user views the document properties through the details pane, they toggle the **Record status** from **Locked** to **Unlocked**.</span></span> <span data-ttu-id="86902-173">只要按一下就能在 [文件保留庫] 的 [記錄] 資料夾中建立記錄，該記錄將在保留期的剩餘時間內保留在其中。</span><span class="sxs-lookup"><span data-stu-id="86902-173">This single click creates a record in the Records folder in the Preservation Hold library, where it resides for the remainder of its retention period.</span></span> <span data-ttu-id="86902-174">文件解除鎖定後，任何擁有權限的使用者都可以編輯該檔案。</span><span class="sxs-lookup"><span data-stu-id="86902-174">While the document is unlocked, any user with permissions can edit the file.</span></span> <span data-ttu-id="86902-175">不過，使用者無法刪除檔案，因為這是已宣告的記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-175">However, users can't delete the file, because it's considered a declared record.</span></span> <span data-ttu-id="86902-176">完成必要的變更之後，使用者就可以將 [記錄狀態]\*\*\*\* 從 [已解鎖]\*\*\*\* 切換為 [鎖定]\*\*\*\*，這樣文件就會再次宣告為記錄，且無法編輯。</span><span class="sxs-lookup"><span data-stu-id="86902-176">After the necessary changes are made, the user can then toggle the **Record status** from **Unlocked** to **Locked**, so that the document is again declared a record and can't be edited.</span></span>
<br/><br/>

<span data-ttu-id="86902-177">:::image type="content" source="media/recordversioning8.png" alt-text="標記為記錄的文件的 [記錄狀態] 內容":::</span><span class="sxs-lookup"><span data-stu-id="86902-177">:::image type="content" source="media/recordversioning8.png" alt-text="Record status property on document tagged as a record":::</span></span>

> [!NOTE]
> <span data-ttu-id="86902-178">記錄版本設定要求每位有權編輯在 SharePoint 網站或 OneDrive 帳戶中被宣告為記錄的內容的使用者，都必須獲得 Office 365 Enterprise E5 授權。</span><span class="sxs-lookup"><span data-stu-id="86902-178">Record versioning requires an Office 365 Enterprise E5 license for each user who has permissions to edit content that's been declared a record in a SharePoint site or OneDrive account.</span></span> <span data-ttu-id="86902-179">具有唯讀存取權的使用者不需要授權。</span><span class="sxs-lookup"><span data-stu-id="86902-179">Users who have read-only access don't require a license.</span></span>

### <a name="locking-and-unlocking-a-record"></a><span data-ttu-id="86902-180">鎖定和解除鎖定記錄</span><span class="sxs-lookup"><span data-stu-id="86902-180">Locking and unlocking a record</span></span>

<span data-ttu-id="86902-181">當您將記錄標籤指派給文件之後，預設 [成員] 群組 ([參與] 權限等級) 中的任何使用者都可以解除鎖定記錄或鎖定已解鎖的記錄。</span><span class="sxs-lookup"><span data-stu-id="86902-181">After a record label is assigned to a document, any user in the default Members group (the Contribute permission level) can unlock a record or lock an unlocked record.</span></span>
<br/><br/>

<span data-ttu-id="86902-182">:::image type="content" source="media/recordversioning9.png" alt-text="記錄狀態顯示記錄文件已解鎖":::</span><span class="sxs-lookup"><span data-stu-id="86902-182">:::image type="content" source="media/recordversioning9.png" alt-text="Record status shows record document is unlocked":::</span></span>

<span data-ttu-id="86902-183">當使用者解鎖記錄後，會發生下列動作：</span><span class="sxs-lookup"><span data-stu-id="86902-183">When a user unlocks a record, the following actions occur:</span></span>

1. <span data-ttu-id="86902-184">如果目前的網站集合沒有文件保留庫，則會建立一個。</span><span class="sxs-lookup"><span data-stu-id="86902-184">If the current site collection doesn't have a Preservation Hold library, one is created.</span></span>

2. <span data-ttu-id="86902-185">如果 [文件保留庫] 沒有 [記錄] 資料夾，則會建立一個。</span><span class="sxs-lookup"><span data-stu-id="86902-185">If the Preservation Hold library doesn't have a Records folder, one is created.</span></span>

3. <span data-ttu-id="86902-186">[複製到]\*\*\*\* 動作會將最新版本的文件複製到 [記錄] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="86902-186">A **Copy to** action copies the latest version of the document to the Records folder.</span></span> <span data-ttu-id="86902-187">[複製到]\*\*\*\* 動作只會包含最新版本，而不包含先前的版本。</span><span class="sxs-lookup"><span data-stu-id="86902-187">The **Copy to** action includes only the latest version and no prior versions.</span></span> <span data-ttu-id="86902-188">複製的文件現在被視為文件的記錄版本，其檔案名稱的格式為：\[標題 GUID 版本\#\]</span><span class="sxs-lookup"><span data-stu-id="86902-188">This copied document is now considered a record version of the document, and its file name has the format: \[Title GUID Version\#\]</span></span>

4. <span data-ttu-id="86902-189">在 [記錄] 資料夾中建立的複本會新增到原始文件的版本歷程記錄中，而這個版本則會在 [註解] 欄位中顯示 [記錄]\*\*\*\* 這兩個字。</span><span class="sxs-lookup"><span data-stu-id="86902-189">The copy created in the Records folder added to the version history of the original document, and this version shows the word **Record** in the comments field.</span></span>

5. <span data-ttu-id="86902-190">原始文件是可以編輯 (但無法刪除) 的新版本。</span><span class="sxs-lookup"><span data-stu-id="86902-190">The original document is a new version that can be edited (but not deleted).</span></span> <span data-ttu-id="86902-191">[文件庫] 欄位 [項目是一筆記錄]\*\*\*\* 仍然會顯示 [是]\*\*\*\* 值，因為文件仍被視為記錄，即使現在可以編輯。</span><span class="sxs-lookup"><span data-stu-id="86902-191">The document library column **Item is a Record** still shows the **Yes** value because the document is still considered a record, even if it can now be edited.</span></span>

<span data-ttu-id="86902-192">當使用者鎖定記錄後，就不能再次編輯原始檔案。</span><span class="sxs-lookup"><span data-stu-id="86902-192">When a user locks a record, the original document again can't be edited.</span></span> <span data-ttu-id="86902-193">但是，解鎖記錄的動作會將版本複製到 [文件保留庫] 中的 [記錄] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="86902-193">But it is the action of unlocking a record that copies a version to the Records folder in the Preservation Hold library.</span></span>

### <a name="record-versions"></a><span data-ttu-id="86902-194">記錄版本</span><span class="sxs-lookup"><span data-stu-id="86902-194">Record versions</span></span>

<span data-ttu-id="86902-195">每次使用者解鎖記錄時，系統會將最新版本複製到 [文件保留庫] 的 [記錄] 資料夾中，而該版本則會在版本歷程記錄的 [註解]\*\*\*\* 欄位中包含 [記錄]\*\*\*\* 的值。</span><span class="sxs-lookup"><span data-stu-id="86902-195">Each time a user unlocks a record, the latest version is copied to the Records folder in the Preservation Hold library, and that version contains the value of **Record** in the **Comments** field of the version history.</span></span>
<br/><br/>

<span data-ttu-id="86902-196">:::image type="content" source="media/recordversioning10.png" alt-text="在文件保留庫中顯示的記錄":::</span><span class="sxs-lookup"><span data-stu-id="86902-196">:::image type="content" source="media/recordversioning10.png" alt-text="Record shown in the Preservation Hold library":::</span></span>

<span data-ttu-id="86902-197">若要查看版本歷程記錄，請選取文件庫中的文件，然後按一下項目功能表中的 [版本歷程記錄]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="86902-197">To view the version history, select a document in the document library and then click **Version history** in the item menu.</span></span>

### <a name="where-records-are-stored"></a><span data-ttu-id="86902-198">記錄的儲存位置</span><span class="sxs-lookup"><span data-stu-id="86902-198">Where records are stored</span></span>

<span data-ttu-id="86902-199">記錄會儲存在網站集合中，頂層網站中 [文件保留庫] 的 [記錄] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="86902-199">Records are stored in the Records folder in the Preservation Hold library in the top-level site in the site collection.</span></span> <span data-ttu-id="86902-200">在頂層網站的左側瀏覽中，選擇 [網站內容]\*\*\*\* \> [文件保留庫]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="86902-200">In the left nav on the top-level site, choose **Site contents** \> **Preservation Hold Library**.</span></span>
<br/><br/>

<span data-ttu-id="86902-201">:::image type="content" source="media/recordversioning11.png" alt-text="文件保留庫":::</span><span class="sxs-lookup"><span data-stu-id="86902-201">:::image type="content" source="media/recordversioning11.png" alt-text="Preservation hold library":::</span></span>

<br/><br/>

<span data-ttu-id="86902-202">:::image type="content" source="media/recordversioning12.png" alt-text="文件保留庫中的記錄資料夾":::</span><span class="sxs-lookup"><span data-stu-id="86902-202">:::image type="content" source="media/recordversioning12.png" alt-text="The Records folder in the Preservation Hold library":::</span></span>

<span data-ttu-id="86902-203">只有網站集合系統管理員才能看到 [文件保留庫]。</span><span class="sxs-lookup"><span data-stu-id="86902-203">The Preservation Hold library is visible only to site collection admins.</span></span> <span data-ttu-id="86902-204">此外，預設不存在 [文件保留庫]。</span><span class="sxs-lookup"><span data-stu-id="86902-204">Also, the Preservation Hold library doesn't exist by default.</span></span> <span data-ttu-id="86902-205">只有在網站集中第一次刪除具有保留標籤或保留原則的內容時，才會建立。</span><span class="sxs-lookup"><span data-stu-id="86902-205">It's created only when content subject to a retention label or retention policy is deleted for the first time in the site collection.</span></span>

### <a name="searching-the-audit-log-for-record-versioning-events"></a><span data-ttu-id="86902-206">搜尋記錄版本設定事件的稽核記錄</span><span class="sxs-lookup"><span data-stu-id="86902-206">Searching the audit log for record versioning events</span></span>

<span data-ttu-id="86902-207">鎖定和解鎖記錄的動作會記錄在 Office 365 稽核記錄中。</span><span class="sxs-lookup"><span data-stu-id="86902-207">The actions of locking and unlocking records are logged in the Office 365 audit log.</span></span> <span data-ttu-id="86902-208">您可以搜尋 [已將記錄狀態變更為「鎖定」]\*\*\*\* 和 [已將記錄狀態變更為「未鎖定」]\*\*\*\* 的特定活動，其位於 [安全性與合規性中心]\*\*\*\* 的 [稽核記錄搜尋]\*\*\*\* 頁面上，[檔案與頁面活動] 區段的 [活動]\*\*\*\* 下拉式清單中。</span><span class="sxs-lookup"><span data-stu-id="86902-208">You can search for the specific activities **Changed record status to locked** and **Changed record status to unlocked**, which are located in the **File and page activities** section in the **Activities** dropdown list on the **Audit log search** page in the security and compliance center.</span></span>
<br/><br/>

<span data-ttu-id="86902-209">:::image type="content" source="media/recordversioning13.png" alt-text="搜尋記錄版本設定事件的稽核記錄":::</span><span class="sxs-lookup"><span data-stu-id="86902-209">:::image type="content" source="media/recordversioning13.png" alt-text="Search the audit log for record versioning events":::</span></span>

<span data-ttu-id="86902-210">如需搜尋這些活動的詳細資訊，請參閱[在安全性與合規性中心搜尋稽核記錄](search-the-audit-log-in-security-and-compliance.md#file-and-page-activities)中的「檔案和頁面活動」一節。</span><span class="sxs-lookup"><span data-stu-id="86902-210">For more information about searching for these events, see the "File and page activities" section in [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md#file-and-page-activities).</span></span>