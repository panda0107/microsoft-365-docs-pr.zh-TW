---
title: 在 Office 365 中创建和管理非活动邮箱
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: 您可以通过将保留或 Office 365 保留策略应用于邮箱，然后删除相应的 Office 365 用户帐户，在 Office 365 中创建非活动邮箱。 非活动邮箱中的项目在非活动之前应用于它的保留或保留策略的持续时间内保留。 要永久删除非活动邮箱，只需删除保留或保留策略。
ms.openlocfilehash: ca6fc5b579b6974ce89db14d318a6dc5a50f3f5c
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37076493"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a><span data-ttu-id="28aa9-105">在 Office 365 中创建和管理非活动邮箱</span><span class="sxs-lookup"><span data-stu-id="28aa9-105">Create and manage inactive mailboxes in Office 365</span></span>

<span data-ttu-id="28aa9-106">Office 365 使您能够保留已删除邮箱的内容。</span><span class="sxs-lookup"><span data-stu-id="28aa9-106">Office 365 makes it possible for you to retain the contents of deleted mailboxes.</span></span> <span data-ttu-id="28aa9-107">此功能称为[非活动邮箱。](inactive-mailboxes-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="28aa9-107">This feature is called [inactive mailboxes](inactive-mailboxes-in-office-365.md).</span></span> <span data-ttu-id="28aa9-108">非活动邮箱允许您在员工离开组织后保留他们的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="28aa9-108">Inactive mailboxes allow you to retain former employees' email after they leave your organization.</span></span> <span data-ttu-id="28aa9-109">在删除相应的 Office 365 用户帐户之前，当诉讼保留或 Office 365 保留策略（在 Office 365 或 Microsoft 365 中的安全和合规性中心创建）应用于邮箱时，邮箱将变为非活动状态。</span><span class="sxs-lookup"><span data-stu-id="28aa9-109">A mailbox becomes inactive when a Litigation Hold or an Office 365 retention policy (created in the security and compliance center in Office 365 or Microsoft 365) is applied to the mailbox before the corresponding Office 365 user account is deleted.</span></span> <span data-ttu-id="28aa9-110">非活动邮箱的内容在邮箱处于非活动状态之前放在邮箱上的保留期间保留。</span><span class="sxs-lookup"><span data-stu-id="28aa9-110">The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive.</span></span> <span data-ttu-id="28aa9-111">这允许管理员、合规性官和记录管理员使用内容搜索来搜索和导出非活动邮箱的内容。</span><span class="sxs-lookup"><span data-stu-id="28aa9-111">This allows administrators, compliance officers, and records managers to use Content Search to search and export the contents of an inactive mailbox.</span></span> <span data-ttu-id="28aa9-112">非作用中的信箱無法接收電子郵件，也不會顯示於貴組織的共用通訊錄或其他清單中。</span><span class="sxs-lookup"><span data-stu-id="28aa9-112">Inactive mailboxes can't receive email and aren't displayed in your organization's shared address book or other lists.</span></span>
  
> [!NOTE]
> <span data-ttu-id="28aa9-p103">我們已將 2017 年 7 月 1 日的期限延後，以建立新的「就地保留」來建立非使用中的信箱。但到今年年底或明年年初，您將無法在 Exchange Online 中建立新的「就地保留」。到時，只有「訴訟資料暫留」和 Office 365 保留原則可以用來建立非使用中的信箱。不過，仍會支援「就地保留」上現有的非使用中信箱，並且您可以繼續管理非使用信箱上的「就地保留」。這包括變更「就地保留」期間，以及透過移除「就地保留」永久刪除非使用中的信箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="28aa9-118">開始之前</span><span class="sxs-lookup"><span data-stu-id="28aa9-118">Before you begin</span></span>

- <span data-ttu-id="28aa9-119">要使邮箱处于非活动状态，必须为其分配 Exchange 联机计划 2 许可证，以便在删除邮箱之前将诉讼保留或 Office 365 保留策略应用于该邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-119">To make a mailbox inactive, it must be assigned an Exchange Online Plan 2 license so that a Litigation Hold or an Office 365 retention policy can be applied to the mailbox before it's deleted.</span></span> <span data-ttu-id="28aa9-120">Exchange 在线计划 2 许可证是 Office 365 企业版 E3 和 E5 订阅的一部分。</span><span class="sxs-lookup"><span data-stu-id="28aa9-120">Exchange Online Plan 2 licenses are part of an Office 365 Enterprise E3 and E5 subscription.</span></span> <span data-ttu-id="28aa9-121">如果邮箱被分配了 Exchange 在线计划 1 或 Exchange 在线 Kiosk 许可证（分别属于 Office 365 E1 和 F1 订阅），则您必须为其分配单独的 Exchange 联机存档许可证，以便保留可以应用于邮箱 b因此，它被删除。</span><span class="sxs-lookup"><span data-stu-id="28aa9-121">If a mailbox is assigned an Exchange Online Plan 1 or Exchange Online Kiosk license (which are part of an Office 365 E1 and F1 subscription respectively), you would have to assign it a separate Exchange Online Archiving license so that a hold can be applied to the mailbox before it's deleted.</span></span> <span data-ttu-id="28aa9-122">有关详细信息，请参阅[交换联机存档](https://go.microsoft.com/fwlink/p/?LinkId=286153)。</span><span class="sxs-lookup"><span data-stu-id="28aa9-122">For more information, see [Exchange Online Archiving](https://go.microsoft.com/fwlink/p/?LinkId=286153).</span></span>
    
- <span data-ttu-id="28aa9-123">删除相应的 Office 365 用户帐户后，与已删除的 Exchange Online 邮箱关联的许可证将可用。</span><span class="sxs-lookup"><span data-stu-id="28aa9-123">The licenses associated with the deleted Exchange Online mailbox will be available after you delete the corresponding Office 365 user account.</span></span> <span data-ttu-id="28aa9-124">然后，您可以将[这些许可证分配给其他用户。](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc)</span><span class="sxs-lookup"><span data-stu-id="28aa9-124">You can then [assign those licenses to another user](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).</span></span> 
    
- <span data-ttu-id="28aa9-125">如果诉讼保留或 Office 365 保留策略（配置为保留或保留然后删除内容）在删除之前未应用于邮箱，则邮箱的内容将不会保留或可发现。</span><span class="sxs-lookup"><span data-stu-id="28aa9-125">If a Litigation Hold or an Office 365 retention policy (that's configured to retain or retain and then delete content) isn't applied to a mailbox before it's deleted, the contents of the mailbox won't be retained or discoverable.</span></span> <span data-ttu-id="28aa9-126">但是，删除的邮箱可以在删除后的 30 天内恢复，但如果邮箱及其内容未恢复，则该邮箱及其内容将在 30 天后永久删除。</span><span class="sxs-lookup"><span data-stu-id="28aa9-126">However, the deleted mailbox can be recovered within 30 days of deletion, but the mailbox and its contents will be permanently deleted after 30 days if it isn't recovered.</span></span>
    
- <span data-ttu-id="28aa9-127">有关诉讼保留的详细信息，请参阅[就地保留和诉讼保留](https://go.microsoft.com/fwlink/p/?LinkId=846124)。</span><span class="sxs-lookup"><span data-stu-id="28aa9-127">For more information about Litigation Hold, see [In-Place Hold and Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=846124).</span></span> <span data-ttu-id="28aa9-128">有关 Office 365 保留策略的详细信息，请参阅[Office 365 中的保留策略概述。](retention-policies.md)</span><span class="sxs-lookup"><span data-stu-id="28aa9-128">For more information about Office 365 retention policies, see [Overview of retention policies in Office 365](retention-policies.md).</span></span>
  
## <a name="create-an-inactive-mailbox"></a><span data-ttu-id="28aa9-129">创建非活动邮箱</span><span class="sxs-lookup"><span data-stu-id="28aa9-129">Create an inactive mailbox</span></span>

<span data-ttu-id="28aa9-130">使邮箱处于非活动状态需要两个步骤：1） 将邮箱置于诉讼保留状态或对邮箱 365 保留策略应用，2） 删除邮箱或相应的 Office 365 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="28aa9-130">Making a mailbox inactive involves two steps: 1) placing the mailbox on Litigation Hold or applying an Office 365 retention policy to it, and 2) deleting the mailbox or corresponding Office 365 user account.</span></span> <span data-ttu-id="28aa9-131">邮箱处于非活动状态后，其内容将保留，直到删除保留或保留策略。</span><span class="sxs-lookup"><span data-stu-id="28aa9-131">After the mailbox is inactive, its contents are retained until the hold or retention policy is removed.</span></span>
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a><span data-ttu-id="28aa9-132">第 1 步：将邮箱置于诉讼保留或应用 Office 365 保留策略</span><span class="sxs-lookup"><span data-stu-id="28aa9-132">Step 1: Place a mailbox on Litigation Hold or apply an Office 365 retention policy</span></span>

<span data-ttu-id="28aa9-133">将邮箱置于诉讼保留或应用 Office 365 保留策略（配置为保留或保留然后删除内容）在删除之前保留邮箱中的内容。</span><span class="sxs-lookup"><span data-stu-id="28aa9-133">Placing a mailbox on Litigation Hold or applying an Office 365 retention policy (that's configured to retain or retain and then delete content) retains the contents in the mailbox before it's deleted.</span></span> <span data-ttu-id="28aa9-134">这两种类型的保留将保留所有邮箱内容，包括已删除的项目和已修改项目的原始版本。</span><span class="sxs-lookup"><span data-stu-id="28aa9-134">Both types of holds will retain all mailbox content, including deleted items and original versions of modified items.</span></span> <span data-ttu-id="28aa9-135">已删除和修改的项目将保留在非活动邮箱中指定一段时间，或者直到您通过删除应用于非活动邮箱的保留或保留策略永久删除非活动邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-135">Deleted and modified items are retained in the inactive mailbox for a specified period, or until you permanently delete the inactive mailbox by removing the hold or retention policy that's applied to the inactive mailbox.</span></span>
  
<span data-ttu-id="28aa9-136">如果邮箱上已放置保留，或者 Office 365 保留策略已应用于邮箱，则所有操作就是删除步骤 2 中所述的相应的 Office 365 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="28aa9-136">If a hold is already placed on a mailbox, or if an Office 365 retention policy is already applied to a mailbox, then all you have to do is delete the corresponding Office 365 user account as explained in Step 2.</span></span>
  
<span data-ttu-id="28aa9-137">有关将邮箱置于诉讼保留或应用 Office 365 保留策略的分步过程，请参阅：</span><span class="sxs-lookup"><span data-stu-id="28aa9-137">For step-by-step procedures for placing a mailbox on Litigation Hold or applying an Office 365 retention policy, see:</span></span>
  
- [<span data-ttu-id="28aa9-138">將信箱設定為訴訟資料暫留狀態</span><span class="sxs-lookup"><span data-stu-id="28aa9-138">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [<span data-ttu-id="28aa9-139">Office 365 中的保留策略概述</span><span class="sxs-lookup"><span data-stu-id="28aa9-139">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
> [!NOTE]
> <span data-ttu-id="28aa9-140">对于诉讼保留和 Office 365 保留策略，您可以创建无限期保留或基于时间的保留。</span><span class="sxs-lookup"><span data-stu-id="28aa9-140">For Litigation Holds and Office 365 retention policies, you can create an indefinite hold or on a time-based hold.</span></span> <span data-ttu-id="28aa9-141">在无限期保留中，非活动邮箱的内容将永久保留，或直到删除保留或更改保留持续时间。</span><span class="sxs-lookup"><span data-stu-id="28aa9-141">In an indefinite hold, the contents of the inactive mailbox will be retained forever, or until the hold is removed or until the hold duration is changed.</span></span> <span data-ttu-id="28aa9-142">删除保留或保留策略后（假设邮箱在 30 天前已删除），将非活动邮箱标记为永久删除，并且将不再保留或发现邮箱的内容。</span><span class="sxs-lookup"><span data-stu-id="28aa9-142">After the hold or retention policy is removed (assuming that the mailbox was deleted more than 30 days ago), the inactive mailbox will be marked for permanent deletion and the contents of the mailbox will no longer be retained or discoverable.</span></span> <span data-ttu-id="28aa9-143">在基于时间的保留或 Office 365 保留策略中，指定保留的持续时间。</span><span class="sxs-lookup"><span data-stu-id="28aa9-143">In a time-based hold or Office 365 retention policy, you specify the duration of the hold.</span></span> <span data-ttu-id="28aa9-144">此持續時間視個別項目而定，會從接收或建立信箱項目的日期開始計算。</span><span class="sxs-lookup"><span data-stu-id="28aa9-144">This duration is on a per-item basis and is calculated from the date a mailbox item was received or created.</span></span> <span data-ttu-id="28aa9-145">邮箱项目的保留过期，并且该项目移动到或位于非活动邮箱中的"可恢复项目"文件夹中后，在已删除的项目保留期到期后，该项目将从非活动邮箱中永久删除（清除）。</span><span class="sxs-lookup"><span data-stu-id="28aa9-145">After the hold expires for a mailbox item, and that item moved to or is located in the Recoverable Items folder in the inactive mailbox, the item is permanently deleted (purged) from the inactive mailbox after the deleted item retention period expires.</span></span> 
  
### <a name="step-2-delete-the-mailbox"></a><span data-ttu-id="28aa9-146">步驟 2：刪除信箱</span><span class="sxs-lookup"><span data-stu-id="28aa9-146">Step 2: Delete the mailbox</span></span>

<span data-ttu-id="28aa9-147">将邮箱置于保留状态或向其应用 Office 365 保留策略后，下一步是删除邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-147">After the mailbox is placed on hold or an Office 365 retention policy is applied to it, the next step is to delete the mailbox.</span></span> <span data-ttu-id="28aa9-148">删除邮箱的最佳方法是删除 Microsoft 365 管理中心中的相应 Office 365 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="28aa9-148">The best way to delete a mailbox is to delete the corresponding Office 365 user account in the Microsoft 365 admin center.</span></span> <span data-ttu-id="28aa9-149">有关删除 Office 365 用户帐户的信息，请参阅[从组织中删除用户。](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e)</span><span class="sxs-lookup"><span data-stu-id="28aa9-149">For information about deleting Office 365 user accounts, see [Delete a user from your organization](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).</span></span>
  
> [!NOTE]
> <span data-ttu-id="28aa9-150">您还可以使用 Exchange 在线电源外壳**中的"删除邮箱"** 删除邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-150">You can also delete the mailbox by using the **Remove-Mailbox** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="28aa9-151">有关详细信息，请参阅[联机交换中删除或还原用户邮箱。](https://go.microsoft.com/fwlink/?linkid=856287)</span><span class="sxs-lookup"><span data-stu-id="28aa9-151">For more information, see [Delete or restore user mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856287).</span></span> 
  

## <a name="view-a-list-of-inactive-mailboxes"></a><span data-ttu-id="28aa9-152">查看非活动邮箱的列表</span><span class="sxs-lookup"><span data-stu-id="28aa9-152">View a list of inactive mailboxes</span></span>

<span data-ttu-id="28aa9-153">要查看组织中非活动邮箱的列表，请以下操作：</span><span class="sxs-lookup"><span data-stu-id="28aa9-153">To view a list of the inactive mailboxes in your organization:</span></span>
  
1. <span data-ttu-id="28aa9-154">转到[https://protection.office.com](https://protection.office.com)并使用 Office 365 组织中管理员帐户的凭据登录。</span><span class="sxs-lookup"><span data-stu-id="28aa9-154">Go to [https://protection.office.com](https://protection.office.com) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="28aa9-155">**单击"数据治理** > **保留"。**</span><span class="sxs-lookup"><span data-stu-id="28aa9-155">Click **Data governance** > **Retention**.</span></span>
    
3. <span data-ttu-id="28aa9-156">在"**保留"** 页上，**单击"更多**![导航栏"](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif)椭圆，**然后单击"非活动邮箱"。**</span><span class="sxs-lookup"><span data-stu-id="28aa9-156">On the **Retention** page, click **More**![Navigation Bar ellipses](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif), and then click **Inactive mailboxes**.</span></span>
    
    ![在"保留"页上，单击"更多"，然后单击"非活动邮箱"以显示非活动邮箱列表](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    <span data-ttu-id="28aa9-158">将显示"**非活动邮箱"** 页。</span><span class="sxs-lookup"><span data-stu-id="28aa9-158">The **Inactive mailboxes** page is displayed.</span></span> <span data-ttu-id="28aa9-159">请注意，将显示组织中非活动邮箱的总数。</span><span class="sxs-lookup"><span data-stu-id="28aa9-159">Note the total number of inactive mailboxes in your organization is displayed.</span></span> 
    
    ![将显示组织中所有非活动邮箱的列表](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
<span data-ttu-id="28aa9-161">或者，您可以在 Exchange 联机 PowerShell 中运行以下命令以显示非活动邮箱列表。</span><span class="sxs-lookup"><span data-stu-id="28aa9-161">Alternatively, you can run the following command in Exchange Online PowerShell to display the list of inactive mailboxes.</span></span>

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

<span data-ttu-id="28aa9-162">您可以单击"![导出搜索结果"](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)**图标"导出"** 以查看或下载包含组织中非活动邮箱的其他信息的 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="28aa9-162">You can click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Export** to view or download a CSV file that contains additional information about the inactive mailboxes in your organization.</span></span> 
  
<span data-ttu-id="28aa9-163">还可以运行以下命令，将非活动邮箱列表和其他信息导出到 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="28aa9-163">You can also run the following command to export the list of inactive mailboxes and other information to a CSV file.</span></span> <span data-ttu-id="28aa9-164">在此示例中，CSV 文件在当前目录中创建。</span><span class="sxs-lookup"><span data-stu-id="28aa9-164">In this example, the CSV file is created in the current directory.</span></span>

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> <span data-ttu-id="28aa9-165">非活动邮箱可能具有与活动用户邮箱相同的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="28aa9-165">It's possible that an inactive mailbox may have the same SMTP address as an active user mailbox.</span></span> <span data-ttu-id="28aa9-166">在这种情况下，可用于唯一标识非活动邮箱**的"可分辨名称"\*\*\*\*或"ExchangeGuid"** 属性的值。</span><span class="sxs-lookup"><span data-stu-id="28aa9-166">In this case, the value of the **DistinguishedName** or **ExchangeGuid** property can be used to uniquely identify an inactive mailbox.</span></span> 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a><span data-ttu-id="28aa9-167">搜索并导出非活动邮箱的内容</span><span class="sxs-lookup"><span data-stu-id="28aa9-167">Search and export the contents of an inactive mailbox</span></span>

<span data-ttu-id="28aa9-168">您可以使用安全&合规性中心中的内容搜索工具访问非活动邮箱的内容。</span><span class="sxs-lookup"><span data-stu-id="28aa9-168">You can access the contents of the inactive mailbox by using the Content Search tool in the Security & Compliance Center.</span></span> <span data-ttu-id="28aa9-169">在搜尋非使用中的信箱時，您可以建立關鍵字搜尋查詢以搜尋特定項目，也可以傳回非使用中信箱的完整內容。</span><span class="sxs-lookup"><span data-stu-id="28aa9-169">When you search an inactive mailbox, you can create a keyword search query to search for specific items or you can return the entire contents of the inactive mailbox.</span></span> <span data-ttu-id="28aa9-170">您可以预览搜索结果或将搜索结果导出到 Outlook 数据 （PST） 文件或作为单个电子邮件。</span><span class="sxs-lookup"><span data-stu-id="28aa9-170">You can preview the search results or export the search results to an Outlook Data (PST) file or as individual email messages.</span></span> <span data-ttu-id="28aa9-171">有关搜索邮箱和导出搜索结果的分步过程，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="28aa9-171">For step-by-step procedures for searching mailboxes and exporting search results, see the following topics:</span></span>
  
- [<span data-ttu-id="28aa9-172">Office 365 中的内容搜索</span><span class="sxs-lookup"><span data-stu-id="28aa9-172">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="28aa9-173">匯出內容搜尋結果</span><span class="sxs-lookup"><span data-stu-id="28aa9-173">Export Content Search results</span></span>](export-search-results.md)
    
<span data-ttu-id="28aa9-174">在搜索非活动邮箱时，需要记住一些事项。</span><span class="sxs-lookup"><span data-stu-id="28aa9-174">Here are a few things to keep in mind when searching inactive mailboxes.</span></span>
  
- <span data-ttu-id="28aa9-175">如果内容搜索包含用户邮箱，然后该邮箱处于非活动状态，则当您在非活动后重新运行搜索时，内容搜索将继续搜索该非活动邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-175">If a content search includes a user mailbox and that mailbox is then made inactive, the content search will continue to search the inactive mailbox when you re-run the search after it becomes inactive.</span></span>
    
- <span data-ttu-id="28aa9-176">在某些情况下，用户可能具有活动邮箱和非活动邮箱具有相同的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="28aa9-176">In some cases, a user may have an active mailbox and an inactive mailbox that have the same SMTP address.</span></span> <span data-ttu-id="28aa9-177">在这种情况下，将仅搜索您选择作为内容搜索位置的特定邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-177">In this case, only the specific mailbox that you select as a location for a content search will be searched.</span></span> <span data-ttu-id="28aa9-178">换句话说，如果将用户的邮箱添加到搜索中，则不能假定将搜索其活动邮箱和非活动邮箱;如果将用户的邮箱添加到搜索中，则不能假定用户邮箱的邮箱和非活动邮箱都将被搜索。只会搜索您显式添加到搜索中的邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-178">In other words, if you add a user's mailbox to a search, you can't assume that both their active and inactive mailboxes will be searched; only the mailbox that you explicitly add to the search will be searched.</span></span>
    
- <span data-ttu-id="28aa9-179">我们强烈建议您避免使用具有相同 SMTP 地址的活动邮箱和非活动邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-179">We strongly recommend that you avoid having an active mailbox and inactive mailbox with the same SMTP address.</span></span> <span data-ttu-id="28aa9-180">如果需要重用当前分配给非活动邮箱的 SMTP 地址，我们建议您恢复非活动邮箱或将非活动邮箱的内容还原到活动邮箱（或活动邮箱的存档），然后删除非活动邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-180">If you need to reuse the SMTP address that is currently assigned to an inactive mailbox, we recommend that you recover the inactive mailbox or restore the contents of an inactive mailbox to an active mailbox (or the archive of an active mailbox), and then delete the inactive mailbox.</span></span>
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="28aa9-181">變更非作用中信箱的保留持續時間</span><span class="sxs-lookup"><span data-stu-id="28aa9-181">Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="28aa9-182">使邮箱处于非活动状态后，可以更改应用于非活动邮箱的保留期或 Office 365 保留策略的持续时间。</span><span class="sxs-lookup"><span data-stu-id="28aa9-182">After a mailbox is made inactive, you can change the duration of the hold or the Office 365 retention policy applied to the inactive mailbox.</span></span> <span data-ttu-id="28aa9-183">有关分步过程，请参阅[更改 Office 365 中非活动邮箱的保留持续时间。](change-the-hold-duration-for-an-inactive-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="28aa9-183">For step-by-step procedures, see [Change the hold duration for an inactive mailbox in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).</span></span>
  
## <a name="recover-an-inactive-mailbox"></a><span data-ttu-id="28aa9-184">復原非作用中的信箱</span><span class="sxs-lookup"><span data-stu-id="28aa9-184">Recover an inactive mailbox</span></span>

<span data-ttu-id="28aa9-185">如果前员工返回您的组织，或者如果雇用新员工来承担离职员工的工作职责，则可以恢复非活动邮箱的内容。</span><span class="sxs-lookup"><span data-stu-id="28aa9-185">If a former employee returns to your organization, or if a new employee is hired to take on the job responsibilities of the departed employee, you can recover the contents of the inactive mailbox.</span></span> <span data-ttu-id="28aa9-186">當您復原不在作用中的信箱時，信箱轉換成新的信箱、 保留的內容和非使用中的信箱資料夾結構，及信箱連結至新的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="28aa9-186">When you recover an inactive mailbox, the mailbox is converted to a new mailbox, the contents and folder structure of the inactive mailbox are retained, and the mailbox is linked to a new user account.</span></span> <span data-ttu-id="28aa9-187">它會復原之後，非使用中的信箱不存在。</span><span class="sxs-lookup"><span data-stu-id="28aa9-187">After it's recovered, the inactive mailbox no longer exists.</span></span> <span data-ttu-id="28aa9-188">有关恢复非活动邮箱时的分步过程和详细信息，请参阅[在 Office 365 中恢复非活动邮箱。](recover-an-inactive-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="28aa9-188">For step-by-step procedures and more information about happens when you recover an inactive mailbox, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a><span data-ttu-id="28aa9-189">将非活动邮箱的内容还原到另一个邮箱</span><span class="sxs-lookup"><span data-stu-id="28aa9-189">Restore the contents of an inactive mailbox to another mailbox</span></span>

<span data-ttu-id="28aa9-190">如果其他员工承担前员工的工作职责，或者如果其他人需要访问非活动邮箱的内容，则可以将非活动邮箱的内容还原（或合并）到现有邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-190">If another employee takes on the job responsibilities of a former employee, or if another person needs access to the contents of the inactive mailbox, you can restore (or merge) the contents of the inactive mailbox to an existing mailbox.</span></span> <span data-ttu-id="28aa9-191">當您還原非使用中信箱內容複製到另一個信箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-191">When you restore an inactive mailbox, the contents are copied to another mailbox.</span></span> <span data-ttu-id="28aa9-192">非使用中的信箱，則會保留與會維持不在作用中的信箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-192">The inactive mailbox is retained and remains an inactive mailbox.</span></span> <span data-ttu-id="28aa9-193">仍可以使用电子数据展示搜索非活动邮箱，其内容可以还原到另一个邮箱，也可以在以后恢复或删除。</span><span class="sxs-lookup"><span data-stu-id="28aa9-193">The inactive mailbox can still be searched using eDiscovery, its contents can be restored to another mailbox, or it can be recovered or deleted at a later date.</span></span> <span data-ttu-id="28aa9-194">有关分步过程，请参阅[在 Office 365 中还原非活动邮箱。](restore-an-inactive-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="28aa9-194">For step-by-step procedures, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>
  
## <a name="delete-an-inactive-mailbox"></a><span data-ttu-id="28aa9-195">刪除非作用中的信箱</span><span class="sxs-lookup"><span data-stu-id="28aa9-195">Delete an inactive mailbox</span></span>

<span data-ttu-id="28aa9-196">如果不再需要保留非活动邮箱的内容，则可以通过删除保留或删除应用于非活动邮箱的 Office 365 保留策略来永久删除非活动邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-196">If you no longer need to retain the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold or removing the Office 365 retention policy applied to the inactive mailbox.</span></span> <span data-ttu-id="28aa9-197">如果邮箱在 30 天前被删除，则在删除保留后，该邮箱将被标记为永久删除，并且邮箱将变得不可恢复。</span><span class="sxs-lookup"><span data-stu-id="28aa9-197">If the mailbox was deleted more than 30 days ago, the mailbox will be marked for permanent deletion after you remove the hold, and the mailbox will become non-recoverable.</span></span> <span data-ttu-id="28aa9-198">如果邮箱在过去 30 天内被删除，您仍然可以在删除保留或保留策略后恢复邮箱。</span><span class="sxs-lookup"><span data-stu-id="28aa9-198">If the mailbox was deleted within the last 30 days, you can still recover the mailbox after removing the hold or retention policy.</span></span> <span data-ttu-id="28aa9-199">有关删除保留或 Office 365 保留策略以永久删除非活动邮箱的分步过程，请参阅删除 Office [365 中的非活动邮箱。](delete-an-inactive-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="28aa9-199">For step-by-step procedures for removing a hold or a Office 365 retention policy to permanently delete an inactive mailbox, see [Delete an inactive mailbox in Office 365](delete-an-inactive-mailbox.md).</span></span>