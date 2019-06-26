---
title: 保護您的系統管理員帳戶
ms.author: sirkkuw
author: sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-Campaigns
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
description: 瞭解如何設定和保護您的系統管理員帳戶。
ms.openlocfilehash: 857c24ac0ec134e119b3de083afe8dc3269bdbe2
ms.sourcegitcommit: c452413dff5d5388c9725f38871246237c313e65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/22/2019
ms.locfileid: "35183258"
---
# <a name="protect-your-administrator-accounts"></a><span data-ttu-id="04fdd-103">保護您的系統管理員帳戶</span><span class="sxs-lookup"><span data-stu-id="04fdd-103">Protect your administrator accounts</span></span>

<span data-ttu-id="04fdd-104">因為系統管理員帳戶具有較高的許可權, 所以對於駭客和網路罪犯來說, 它們是非常有價值的目標。</span><span class="sxs-lookup"><span data-stu-id="04fdd-104">Because the admin accounts come with elevated privileges, they are valuable targets for hackers and cyber criminals.</span></span> <span data-ttu-id="04fdd-105">本文說明：</span><span class="sxs-lookup"><span data-stu-id="04fdd-105">This article describes:</span></span>

- <span data-ttu-id="04fdd-106">如何為緊急情況設定額外的系統管理員帳戶。</span><span class="sxs-lookup"><span data-stu-id="04fdd-106">How to set up an additional administrator account for emergencies.</span></span>
- <span data-ttu-id="04fdd-107">如何保護這些帳戶。</span><span class="sxs-lookup"><span data-stu-id="04fdd-107">How to protect these accounts.</span></span>
 
<span data-ttu-id="04fdd-108">當您註冊 Microsoft 365 商務版並輸入您的資訊時, 您會自動成為全域系統管理員。全域管理員擁有使用者帳戶的最終控制權, 以及 Microsoft 系統管理中心的其他所有設定, 但有許多不同類型的系統管理員帳戶具有不同的存取程度。</span><span class="sxs-lookup"><span data-stu-id="04fdd-108">When you sign up for Microsoft 365 Business and enter your information, you automatically become the global admin. A global admin has the ultimate control of user accounts and all the other settings in the Microsoft admin center, but there are many different kinds of admin accounts with varying degrees of access.</span></span> <span data-ttu-id="04fdd-109">如需各種系統管理員角色之不同存取層級的詳細資訊, 請參閱[關於系統管理員角色](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)。</span><span class="sxs-lookup"><span data-stu-id="04fdd-109">See [about admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) for information about the different access levels for each kind of admin role.</span></span>


## <a name="create-additional-admin-accounts"></a><span data-ttu-id="04fdd-110">建立其他系統管理員帳戶</span><span class="sxs-lookup"><span data-stu-id="04fdd-110">Create additional admin accounts</span></span>

<span data-ttu-id="04fdd-111">僅使用系統管理帳戶進行管理。</span><span class="sxs-lookup"><span data-stu-id="04fdd-111">Use admin accounts only for administration.</span></span> <span data-ttu-id="04fdd-112">系統管理員應該要有個別的使用者帳戶, 以便定期使用 Office 應用程式, 並在必要時使用其系統管理帳戶來管理帳戶、裝置以及使用其他系統管理功能。</span><span class="sxs-lookup"><span data-stu-id="04fdd-112">Admins should have a separate user account for regular use of Office apps and only use their administrative account when necessary to manage accounts, devices and while working on other admin functions.</span></span>  <span data-ttu-id="04fdd-113">將 Microsoft 365 商務版授權從系統管理帳戶中移除是個好方法, 因此您不需要付費。</span><span class="sxs-lookup"><span data-stu-id="04fdd-113">It is also a good idea to remove the Microsoft 365 Business license from the admin accounts so you don't have to pay for them.</span></span>

<span data-ttu-id="04fdd-114">您至少要設定一個額外的全域系統管理員帳戶, 以授與其他受信任員工的系統管理員存取權。</span><span class="sxs-lookup"><span data-stu-id="04fdd-114">You'll want to set up at least one additional global admin account to give admin access to another trusted employee.</span></span> <span data-ttu-id="04fdd-115">您也可以為使用者管理建立不同的系統管理員帳戶 (這個角色稱為「**使用者管理管理員**」)。</span><span class="sxs-lookup"><span data-stu-id="04fdd-115">You can also create separate admin accounts for user management (this role is called **User management administrator**).</span></span> <span data-ttu-id="04fdd-116">如需詳細資訊, 請參閱[關於系統管理員角色](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)。</span><span class="sxs-lookup"><span data-stu-id="04fdd-116">See [about admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) for more information.</span></span>

<span data-ttu-id="04fdd-117">若要建立其他系統管理員帳戶:</span><span class="sxs-lookup"><span data-stu-id="04fdd-117">To create additional admin accounts:</span></span>

 1. <span data-ttu-id="04fdd-118">移至系統<a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">管理中心</a>, 然後選擇左側導覽中的 [**使用者** \> ] [作用中**使用者**]。</span><span class="sxs-lookup"><span data-stu-id="04fdd-118">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span></span>

    ![選擇 [使用者], 然後在左側導覽中選擇 [作用中的使用者]](media/Activeusers.png)

2. <span data-ttu-id="04fdd-120">在 [作用中**使用者**] 頁面上, 選取頁面頂端的 [新增**使用者**], 然後在 [**新增使用者**] 面板上, 輸入名稱及其他資訊。</span><span class="sxs-lookup"><span data-stu-id="04fdd-120">On the **Active users** page select **Add a user** on the top of the page and on the **New user** panel,  enter the name and other information.</span></span>
3. <span data-ttu-id="04fdd-121">展開 [**角色**] 區段, 然後選擇 [**全域管理員**], 授與此使用者的全域系統管理員存取權。</span><span class="sxs-lookup"><span data-stu-id="04fdd-121">Expand the **Roles** section, and choose **Global administrator** to give this user global admin access.</span></span> <span data-ttu-id="04fdd-122">您也可以選擇 [**自訂系統管理員**], 然後選擇任何顯示的角色。</span><span class="sxs-lookup"><span data-stu-id="04fdd-122">You can also choose **Customized administrator** and choose any of the roles that are displayed.</span></span>

    <span data-ttu-id="04fdd-123">在 [替代電子郵件地址] 文字方塊中, 輸入備用電子郵件。</span><span class="sxs-lookup"><span data-stu-id="04fdd-123">Enter an alternate email in the Alternative email address text box.</span></span> <span data-ttu-id="04fdd-124">您可以使用此位址, 在您鎖定時, 復原您的密碼資訊。針對全域系統管理員, 帳單報表也會傳送至此位址。</span><span class="sxs-lookup"><span data-stu-id="04fdd-124">You can use this address to recover your password information if you get locked out. For global admins, a billing statement will also be sent to this address.</span></span>

    ![選擇系統管理員角色](media/adminroles.png)
    
4. <span data-ttu-id="04fdd-126">在 [**產品授權**] 區段中, 將 [ **Microsoft 365 商務**版] 的選取器移至 [**關閉**] \*\* **, 並將 [**建立不含產品授權的使用者\*\*]</span><span class="sxs-lookup"><span data-stu-id="04fdd-126">In the **Product licenses** section, move the selector for **Microsoft 365 Business** to **Off** and the **Create user without product license** to **On**.</span></span>

    ![選擇產品授權](media/productlicense.png)

## <a name="create-an-emergency-admin-account"></a><span data-ttu-id="04fdd-128">建立緊急系統管理員帳戶</span><span class="sxs-lookup"><span data-stu-id="04fdd-128">Create an emergency admin account</span></span>

<span data-ttu-id="04fdd-129">您也應該建立未使用多重要素驗證 (MFA) 進行設定的備份帳戶, 如此一來, 您就不會不慎鎖定自己, 例如, 如果您因遺失從驗證的第二個所用的電話而遺失您的電話。</span><span class="sxs-lookup"><span data-stu-id="04fdd-129">You should also create a backup account that isn't set up with multi-factor authentication (MFA) so you don't accidentally lock yourself out (for example if you lose your phone that you are using as a second from of verification).</span></span> <span data-ttu-id="04fdd-130">請確定此帳戶的密碼是片語或至少16個字元。</span><span class="sxs-lookup"><span data-stu-id="04fdd-130">Make sure the password for this account is a phrase or at least 16 characters long.</span></span> <span data-ttu-id="04fdd-131">這通常稱為「中斷玻璃帳戶」。</span><span class="sxs-lookup"><span data-stu-id="04fdd-131">This is often referred to as a "break-glass account."</span></span>

## <a name="create-a-user-account-for-yourself"></a><span data-ttu-id="04fdd-132">為自己建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="04fdd-132">Create a user account for yourself</span></span>

<span data-ttu-id="04fdd-133">使用您的使用者帳戶參與與您的組織的共同作業, 包括檢查郵件。</span><span class="sxs-lookup"><span data-stu-id="04fdd-133">Use your user account to participate in collaboration with your organization, including checking mail.</span></span> <span data-ttu-id="04fdd-134">這表示您的系統管理員認證可能類似于*小紅 Chavez<span></span>@Contoso。 org*和您的一般使用者帳戶可能與*alice<span></span>@Contoso*相同。</span><span class="sxs-lookup"><span data-stu-id="04fdd-134">This means your admin credentials might be similar to  *Alice.Chavez<span></span>@Contoso.org* and your regular user account might be similar to *Alice<span></span>@Contoso.com*.</span></span>

<span data-ttu-id="04fdd-135">若要建立新的使用者帳戶:</span><span class="sxs-lookup"><span data-stu-id="04fdd-135">To create a new user account:</span></span>
1. <span data-ttu-id="04fdd-136">移至系統<a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">管理中心</a>, 然後選擇左側導覽中的 [**使用者** \> ] [作用中**使用者**]。</span><span class="sxs-lookup"><span data-stu-id="04fdd-136">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span></span>
2. <span data-ttu-id="04fdd-137">在 [作用中**使用者**] 頁面上, 選取頁面頂端的 [新增**使用者**], 然後在 [**新增使用者**] 面板上, 輸入名稱及其他資訊。</span><span class="sxs-lookup"><span data-stu-id="04fdd-137">On the **Active users** page select **Add a user** on the top of the page and on the **New user** panel,  enter the name and other information.</span></span>
3. <span data-ttu-id="04fdd-138">展開 [**角色**] 區段, 然後選擇 [**使用者] (無系統管理存取)**。</span><span class="sxs-lookup"><span data-stu-id="04fdd-138">Expand the **Roles** section, and choose **User (no administrative access)**.</span></span>
1. <span data-ttu-id="04fdd-139">在 [**產品授權**] 區段中, 將**Microsoft 365 商務**版的選擇器移至 [**開啟**]。</span><span class="sxs-lookup"><span data-stu-id="04fdd-139">In the **Product licenses** section, move the selector for **Microsoft 365 Business** to **On**.</span></span> 

## <a name="register-each-of-these-accounts-for-multi-factor-authentication"></a><span data-ttu-id="04fdd-140">針對多重要素驗證註冊這些帳戶</span><span class="sxs-lookup"><span data-stu-id="04fdd-140">Register each of these accounts for multi-factor authentication</span></span>


## <a name="additional-recommendations"></a><span data-ttu-id="04fdd-141">其他建議</span><span class="sxs-lookup"><span data-stu-id="04fdd-141">Additional recommendations</span></span>

- <span data-ttu-id="04fdd-142">請確定系統管理員帳戶也設定為多重要素驗證。</span><span class="sxs-lookup"><span data-stu-id="04fdd-142">Be sure admin accounts are also set up for multi-factor authentication.</span></span> <span data-ttu-id="04fdd-143">我們將在[設定條件式存取原則](m365-campaigns-conditional-access.md)中示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="04fdd-143">We'll show you how to do this in [Configure conditional access policies](m365-campaigns-conditional-access.md).</span></span>
- <span data-ttu-id="04fdd-144">使用系統管理帳戶之前, 請關閉所有不相關的瀏覽器會話和應用程式, 包括個人電子郵件帳戶。</span><span class="sxs-lookup"><span data-stu-id="04fdd-144">Before using admin accounts, close out all unrelated browser sessions and apps, including personal email accounts.</span></span> <span data-ttu-id="04fdd-145">您也可以在私人或 incognito 瀏覽器視窗中使用。</span><span class="sxs-lookup"><span data-stu-id="04fdd-145">You can also use in private, or incognito browser windows.</span></span>
- <span data-ttu-id="04fdd-146">完成系統管理工作之後, 請務必登出瀏覽器會話。</span><span class="sxs-lookup"><span data-stu-id="04fdd-146">After completing admin tasks, be sure to sign out of the browser session.</span></span>