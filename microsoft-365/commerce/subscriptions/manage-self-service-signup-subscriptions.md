---
title: 管理自助註冊訂閱
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- commerce
- Adm_NonTOC
search.appverid:
- MET150
description: 瞭解如何管理組織的免費自助註冊訂閱。
ms.openlocfilehash: 056ae95f9f5067ea3fa86164b620c72c84e3aad4
ms.sourcegitcommit: e525bcf073a61e1350484719a0c3ceb6ff0d8db1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/06/2020
ms.locfileid: "43154127"
---
# <a name="manage-self-service-sign-up-subscriptions"></a><span data-ttu-id="a0cb2-103">管理自助註冊訂閱</span><span class="sxs-lookup"><span data-stu-id="a0cb2-103">Manage self-service sign-up subscriptions</span></span>

## <a name="what-are-self-service-sign-up-subscriptions"></a><span data-ttu-id="a0cb2-104">何謂自助註冊訂閱？</span><span class="sxs-lookup"><span data-stu-id="a0cb2-104">What are self-service sign-up subscriptions?</span></span>

<span data-ttu-id="a0cb2-105">您組織中的使用者可以註冊的免費自助註冊訂閱數目有限。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-105">There are a limited number of free self-service sign-up subscriptions that users in your organization can sign up for.</span></span> <span data-ttu-id="a0cb2-106">使用者只能為自己註冊和使用自助註冊訂閱服務。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-106">A user can only sign up for and use a self-service sign-up subscription for themselves.</span></span> <span data-ttu-id="a0cb2-107">這些訂閱會出現在 [**產品 & 服務**] 頁面上，標記為 [**可用**]，並顯示附注「這是您公司中使用者啟用的免費訂閱」。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-107">These subscriptions appear on the **Products & services** page, are marked as **Free**, and have a note that says, "This is a free subscription activated by users in your company."</span></span> <span data-ttu-id="a0cb2-108">您可以封鎖使用者的註冊，以及刪除使用者已註冊的免費訂閱，以管理自助註冊訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-108">You can manage self-service sign-up subscriptions by blocking users from signing up, and by deleting free subscriptions that users have signed up for.</span></span> <span data-ttu-id="a0cb2-109">如需自助註冊和可用訂閱的詳細資訊，請參閱[在您的組織中使用自助註冊](../../admin/misc/self-service-sign-up.md)。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-109">For more information about self-service sign up and the available subscriptions, see [Using self-service sign up in your organization](../../admin/misc/self-service-sign-up.md).</span></span>

## <a name="how-are-these-subscriptions-different-from-self-service-purchase-subscriptions"></a><span data-ttu-id="a0cb2-110">這些訂閱與自助購買訂閱有何不同？</span><span class="sxs-lookup"><span data-stu-id="a0cb2-110">How are these subscriptions different from self-service purchase subscriptions?</span></span>

<span data-ttu-id="a0cb2-111">自助註冊訂閱是免費的，可提供更大的產品清單，而非自助購買訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-111">Self-service sign-up subscriptions are free, and are available for a larger list of products than self-service purchase subscriptions.</span></span> <span data-ttu-id="a0cb2-112">當使用者註冊「自助購買」訂閱時，他們會負責支付服務。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-112">When a user signs up for a self-service purchase subscription, they are responsible for paying for it.</span></span> <span data-ttu-id="a0cb2-113">此外，自助購買訂閱只適用于電源平台產品（Power BI、Power Apps 及 Power 自動化）。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-113">Also, self-service purchase subscriptions are only available for Power Platform products (Power BI, Power Apps, and Power Automate).</span></span> <span data-ttu-id="a0cb2-114">如需詳細資訊，請參閱[自助購買常見問題](self-service-purchase-faq.md)。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-114">For more information, see [Self-service purchase FAQ](self-service-purchase-faq.md).</span></span>

## <a name="block-users-from-signing-up"></a><span data-ttu-id="a0cb2-115">封鎖使用者進行註冊</span><span class="sxs-lookup"><span data-stu-id="a0cb2-115">Block users from signing up</span></span>

<span data-ttu-id="a0cb2-116">您可以搭配**AllowAdHocSubscriptions**參數使用[**MsolCompanySettings 指令程式**](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0)，控制使用者是否可以註冊自助註冊訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-116">You use the [**Set-MsolCompanySettings**](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0) cmdlet with the **AllowAdHocSubscriptions** parameter to control whether users can sign up for self-service sign-up subscriptions.</span></span> <span data-ttu-id="a0cb2-117">如需詳細資訊，請參閱[如何控制自助設定？](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)</span><span class="sxs-lookup"><span data-stu-id="a0cb2-117">For more information, see [How do I control self-service settings?](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)</span></span>

## <a name="delete-a-self-service-sign-up-subscription"></a><span data-ttu-id="a0cb2-118">刪除自助註冊訂閱</span><span class="sxs-lookup"><span data-stu-id="a0cb2-118">Delete a self-service sign-up subscription</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0cb2-119">當您刪除自助註冊訂閱時，會封鎖所有使用者存取其資料和電子郵件，以及刪除所有的資料和電子郵件。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-119">When you delete a self-service sign-up subscription, you block all users from accessing their data and email and delete all data and email.</span></span>

1. <span data-ttu-id="a0cb2-120">在系統管理中心中，移至 [**帳單** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">產品 & 服務</a>] 頁面。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-120">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Products & services</a> page.</span></span>
2. <span data-ttu-id="a0cb2-121">尋找您要刪除的自助註冊訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-121">Find the self-service sign-up subscription that you want to delete.</span></span> <span data-ttu-id="a0cb2-122">在 [**設定 & 動作**] 區段中，選取 [**刪除訂閱**]。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-122">In the **Settings & Actions** section, select **Delete subscription**.</span></span>
3. <span data-ttu-id="a0cb2-123">在 [**刪除訂閱**] 窗格中，選取核取方塊，然後選取 [**刪除訂閱**]。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-123">In the **Delete subscription** pane, select the check box, then select **Delete subscription**.</span></span>

## <a name="i-have-a-self-service-sign-up-subscription-that-blocks-directory-deletion"></a><span data-ttu-id="a0cb2-124">我有封鎖目錄刪除的自助註冊訂閱</span><span class="sxs-lookup"><span data-stu-id="a0cb2-124">I have a self-service sign-up subscription that blocks directory deletion</span></span>

<span data-ttu-id="a0cb2-125">個別使用者可以註冊的自助註冊產品，也會建立來賓使用者，以便在 Azure AD 目錄中進行驗證。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-125">The self-service sign-up products that individual users can sign up for also create a guest user for authentication in your Azure AD directory.</span></span> <span data-ttu-id="a0cb2-126">為了避免資料遺失，這些自助產品會封鎖目錄刪除，直到完全從目錄中刪除。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-126">To avoid data loss, these self-service products block directory deletions until they're fully deleted from the directory.</span></span> <span data-ttu-id="a0cb2-127">它們只能由 Azure AD 系統管理員刪除。如需詳細資訊，請參閱[刪除 Azure Active directory 中的目錄](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto)。</span><span class="sxs-lookup"><span data-stu-id="a0cb2-127">They can be deleted only by the Azure AD admin. For more information, see [Delete a directory in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto).</span></span>