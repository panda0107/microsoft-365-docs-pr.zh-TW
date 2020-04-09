---
title: 設定個別使用者的密碼永不過期
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
- Adm_TOC
ms.custom:
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: f493e3af-e1d8-4668-9211-230c245a0466
description: 瞭解如何使用 Windows PowerShell 將部分個人的使用者密碼設為永不過期。
ms.openlocfilehash: 275fedf7bf4e52320b769689516ad39a31c63ea1
ms.sourcegitcommit: e695bcfc69203da5d3d96f3d6a891664a0e27ae2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2020
ms.locfileid: "43105732"
---
# <a name="set-an-individual-users-password-to-never-expire"></a><span data-ttu-id="fd8e6-103">設定個別使用者的密碼永不過期</span><span class="sxs-lookup"><span data-stu-id="fd8e6-103">Set an individual user's password to never expire</span></span>

## <a name="set-the-password-expiration-policy-for-your-organization"></a><span data-ttu-id="fd8e6-104">設定組織的密碼到期原則</span><span class="sxs-lookup"><span data-stu-id="fd8e6-104">Set the password expiration policy for your organization</span></span>

1. <span data-ttu-id="fd8e6-105">在系統管理中心中，移至 [**設定** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">安全性 & 隱私權</a>] 頁面。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-105">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Security & privacy</a> page.</span></span>
2. <span data-ttu-id="fd8e6-106">選取 [**密碼原則**] 旁邊的 [**編輯**]。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-106">Next to **Password policy** select **Edit**.</span></span> 
3. <span data-ttu-id="fd8e6-107">如果密碼設為永不過期，請將開關設定為 [**關閉**]。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-107">If passwords are set to never expire, set the toggle to **Off**.</span></span> <span data-ttu-id="fd8e6-108">您可以選擇指定密碼到期前的天數。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-108">You'll get the option to specify the number of days until passwords expire.</span></span>

## <a name="set-the-password-expiration-policy-for-individual-users"></a><span data-ttu-id="fd8e6-109">為個別使用者設定密碼到期原則</span><span class="sxs-lookup"><span data-stu-id="fd8e6-109">Set the password expiration policy for individual users</span></span>

<span data-ttu-id="fd8e6-110">Microsoft cloud service 的全域系統管理員可以使用 Microsoft Azure AD Module for Windows PowerShell，將密碼設為不會到期的特定使用者。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-110">A global admin for a Microsoft cloud service can use the Microsoft Azure AD Module for Windows PowerShell to set passwords not to expire for specific users.</span></span> <span data-ttu-id="fd8e6-111">您也可以使用 Windows PowerShell Cmdlet 來移除永不過期的設定，或查看哪些使用者密碼設定為永不過期。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-111">You can also use Windows PowerShell cmdlets to remove the never-expires configuration or to see which user passwords are set to never expire.</span></span>

<span data-ttu-id="fd8e6-112">本指南適用于其他提供者，例如 Intune 和 Office 365，也就是針對身分識別及目錄服務，也依賴 Azure AD。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-112">This guide applies to other providers, such as Intune and Office 365, which also rely on Azure AD for identity and directory services.</span></span> <span data-ttu-id="fd8e6-113">[密碼到期] 是原則中唯一可以變更的部分。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-113">Password expiration is the only part of the policy that can be changed.</span></span>

> [!NOTE]
> <span data-ttu-id="fd8e6-114">只有未透過目錄同步處理同步處理的使用者帳戶密碼才能設定為不會過期。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-114">Only passwords for user accounts that are not synchronized through directory synchronization can be configured to not expire.</span></span> <span data-ttu-id="fd8e6-115">如需目錄同步作業的詳細資訊，請參閱[CONNECT ad With AZURE AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect)。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-115">For more information about directory synchronization, see [Connect AD with Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect).</span></span>

### <a name="how-to-check-the-expiration-policy-for-a-password"></a><span data-ttu-id="fd8e6-116">如何檢查密碼的到期原則</span><span class="sxs-lookup"><span data-stu-id="fd8e6-116">How to check the expiration policy for a password</span></span>
<span data-ttu-id="fd8e6-117">執行下列其中一個命令：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-117">Run one of the following commands:</span></span>

- <span data-ttu-id="fd8e6-118">若要查看單一使用者的密碼是否設為永不過期，請使用 UPN （例如， *user@contoso.onmicrosoft.com*）或您要檢查之使用者的使用者識別碼，執行下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-118">To see if a single user's password is set to never expire, run the following cmdlet by using the UPN (for example, *user@contoso.onmicrosoft.com*) or the user ID of the user you want to check:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId <user id or UPN> | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```

    <span data-ttu-id="fd8e6-119">範例：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-119">Example:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId userUPN@contoso.com | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```  

- <span data-ttu-id="fd8e6-120">若要查看所有使用者的 [**密碼永不到期**] 設定，請執行下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-120">To see the **Password never expires** setting for all users, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
     }
    ```

- <span data-ttu-id="fd8e6-121">若要在目前使用者名稱為**ReportPasswordNeverExpires**的桌上型電腦上，取得所有具有 PasswordNeverExpires Html 的使用者報告</span><span class="sxs-lookup"><span data-stu-id="fd8e6-121">To get a report of all the users with PasswordNeverExpires in Html on the desktop of the current user with name  **ReportPasswordNeverExpires.html**</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    } | ConvertTo-Html | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.html
    ```  

- <span data-ttu-id="fd8e6-122">若要在目前使用者名稱為**ReportPasswordNeverExpires**的電腦上使用 CSV 中的所有使用者報告，取得 PasswordNeverExpires</span><span class="sxs-lookup"><span data-stu-id="fd8e6-122">To get a report of all the users with PasswordNeverExpires in CSV on the desktop of the current user with name **ReportPasswordNeverExpires.csv**</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    } | ConvertTo-Csv -NoTypeInformation | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.csv
    ```

### <a name="set-a-password-to-expire"></a><span data-ttu-id="fd8e6-123">設定密碼為到期</span><span class="sxs-lookup"><span data-stu-id="fd8e6-123">Set a password to expire</span></span>

<span data-ttu-id="fd8e6-124">執行下列其中一個命令：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-124">Run one of the following commands:</span></span>

- <span data-ttu-id="fd8e6-125">若要設定一個使用者的密碼，使密碼到期，請使用 UPN 或使用者的使用者識別碼執行下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-125">To set the password of one user so that the password expires, run the following cmdlet by using the UPN or the user ID of the user:</span></span>

    ```powershell
    Set-AzureADUser -ObjectId <user ID> -PasswordPolicies None
    ```

- <span data-ttu-id="fd8e6-126">若要設定組織中所有使用者的密碼，使其到期，請使用下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-126">To set the passwords of all users in the organization so that they expire, use the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies None
    ```

### <a name="set-a-password-to-never-expire"></a><span data-ttu-id="fd8e6-127">將密碼設為永不過期</span><span class="sxs-lookup"><span data-stu-id="fd8e6-127">Set a password to never expire</span></span>

<span data-ttu-id="fd8e6-128">執行下列其中一個命令：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-128">Run one of the following commands:</span></span>

- <span data-ttu-id="fd8e6-129">若要將某個使用者的密碼設為永不過期，請使用 UPN 或使用者的使用者識別碼執行下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-129">To set the password of one user to never expire, run the following cmdlet by using the UPN or the user ID of the user:</span></span>

    ```powershell
    Set-AzureADUser -ObjectId <user ID> -PasswordPolicies DisablePasswordExpiration
    ```

- <span data-ttu-id="fd8e6-130">若要將組織中所有使用者的密碼設為永不過期，請執行下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fd8e6-130">To set the passwords of all the users in an organization to never expire, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies DisablePasswordExpiration
    ```

> [!WARNING]
> <span data-ttu-id="fd8e6-131">根據屬性設定`-PasswordPolicies DisablePasswordExpiration`為 [仍然存在的`pwdLastSet`密碼] 的密碼。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-131">Passwords set to `-PasswordPolicies DisablePasswordExpiration` still age based on the `pwdLastSet` attribute.</span></span> <span data-ttu-id="fd8e6-132">如果您將使用者密碼設為永不過期，而 90 + 天則為 [已移至]，密碼會到期。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-132">If you set the user passwords to never expire and then 90+ days go by, the passwords expire.</span></span> <span data-ttu-id="fd8e6-133">根據`pwdLastSet`屬性，如果您變更到期時間`-PasswordPolicies None`，則超過90天的所有密碼`pwdLastSet`都需要使用者在下次登入時變更。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-133">Based on the `pwdLastSet` attribute, if you change the expiration to `-PasswordPolicies None`, all passwords that have a `pwdLastSet` older than 90 days require the user to change them the next time they sign in.</span></span> <span data-ttu-id="fd8e6-134">這項變更可能會影響大量的使用者。</span><span class="sxs-lookup"><span data-stu-id="fd8e6-134">This change can affect a large number of users.</span></span>