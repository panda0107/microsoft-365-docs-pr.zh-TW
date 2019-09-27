---
title: Office 365 邮件加密 （OME） 版本比较
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: 有助于解释 Office 365 邮件加密版本之间的差异。
ms.openlocfilehash: b617d6a9f61ae8ec5a0133d405f89038bdab9fc4
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37077972"
---
# <a name="compare-versions-of-ome"></a><span data-ttu-id="67d78-103">比較 OME 版本</span><span class="sxs-lookup"><span data-stu-id="67d78-103">Compare versions of OME</span></span>

<span data-ttu-id="67d78-104">本文将旧版 Office 365 邮件加密 （OME） 与新的 OME 功能和 Office 365 高级邮件加密进行比较。</span><span class="sxs-lookup"><span data-stu-id="67d78-104">This article compares legacy Office 365 Message Encryption (OME) to the new OME capabilities and Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="67d78-105">新功能是 OME 和信息权限管理 （IRM） 的合并和较新版本。</span><span class="sxs-lookup"><span data-stu-id="67d78-105">The new capabilities are a merger and newer version of both OME and Information Rights Management (IRM).</span></span> <span data-ttu-id="67d78-106">还概述了部署到海合会高地的独特特点。</span><span class="sxs-lookup"><span data-stu-id="67d78-106">Unique characteristics of deploying into GCC High are also outlined.</span></span> <span data-ttu-id="67d78-107">两者可以共存于 Office 365 组织中。</span><span class="sxs-lookup"><span data-stu-id="67d78-107">The two can coexist in your Office 365 organization.</span></span> <span data-ttu-id="67d78-108">有关新功能如何工作的信息，请参阅 Office [365 邮件加密 （OME）。](ome.md)</span><span class="sxs-lookup"><span data-stu-id="67d78-108">For information on how the new capabilities work, see [Office 365 Message Encryption (OME)](ome.md).</span></span>

||
|:-----|
|<span data-ttu-id="67d78-109">本文是关于 Office 365 消息加密的较大系列文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="67d78-109">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="67d78-110">本文面向管理员和 ITPros。</span><span class="sxs-lookup"><span data-stu-id="67d78-110">This article is intended for administrators and ITPros.</span></span> <span data-ttu-id="67d78-111">如果您只想查找有关发送或接收加密邮件的信息，请参阅[Office 365 邮件加密 （OME）](ome.md)中的文章列表，并找到最适合您需求的文章。</span><span class="sxs-lookup"><span data-stu-id="67d78-111">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a><span data-ttu-id="67d78-112">特性和功能的并行比较</span><span class="sxs-lookup"><span data-stu-id="67d78-112">Side-by-side comparison of features and capabilities</span></span>

|                                   |<span data-ttu-id="67d78-113">旧功能</span><span class="sxs-lookup"><span data-stu-id="67d78-113">Old features</span></span>       |                   |<span data-ttu-id="67d78-114">新功能</span><span class="sxs-lookup"><span data-stu-id="67d78-114">New features</span></span>              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|<span data-ttu-id="67d78-115">**功能**</span><span class="sxs-lookup"><span data-stu-id="67d78-115">**Capability**</span></span>                     | <span data-ttu-id="67d78-116">**舊版 OME**</span><span class="sxs-lookup"><span data-stu-id="67d78-116">**Legacy OME**</span></span>    | <span data-ttu-id="67d78-117">**IRM**</span><span class="sxs-lookup"><span data-stu-id="67d78-117">**IRM**</span></span>           | <span data-ttu-id="67d78-118">**新的 OME 功能**</span><span class="sxs-lookup"><span data-stu-id="67d78-118">**New OME capabilities**</span></span> |
|<span data-ttu-id="67d78-119">*发送加密邮件*</span><span class="sxs-lookup"><span data-stu-id="67d78-119">*Sending an encrypted mail*</span></span>        |<span data-ttu-id="67d78-120">通过交换邮件流规则</span><span class="sxs-lookup"><span data-stu-id="67d78-120">Through Exchange mail flow rules</span></span>|<span data-ttu-id="67d78-121">最终用户从 Outlook 桌面或 Web 上的 Outlook 启动;或通过 Exchange 邮件流规则</span><span class="sxs-lookup"><span data-stu-id="67d78-121">End-user initiated from Outlook desktop or Outlook on the Web; or through Exchange mail flow rules</span></span>|<span data-ttu-id="67d78-122">最终用户从 Outlook 桌面、Mac Outlook 或 Web 上的 Outlook 启动;通过 Exchange 邮件流规则（也称为传输规则）和 Office 365 数据丢失防护 （DLP）</span><span class="sxs-lookup"><span data-stu-id="67d78-122">End-user initiated from Outlook desktop, Outlook for Mac, or Outlook on the Web; through Exchange mail flow rules (also known as transport rules) and Office 365 Data Loss Prevention (DLP)</span></span>|
|<span data-ttu-id="67d78-123">*权限管理模板*</span><span class="sxs-lookup"><span data-stu-id="67d78-123">*Rights management template*</span></span>       |   <span data-ttu-id="67d78-124">不適用</span><span class="sxs-lookup"><span data-stu-id="67d78-124">N/A</span></span>      |<span data-ttu-id="67d78-125">不转发选项和自定义模板</span><span class="sxs-lookup"><span data-stu-id="67d78-125">Do Not Forward option and custom templates</span></span>|<span data-ttu-id="67d78-126">不转发选项、仅加密选项和自定义模板</span><span class="sxs-lookup"><span data-stu-id="67d78-126">Do Not Forward option, Encrypt-Only option, and custom templates</span></span>|
|<span data-ttu-id="67d78-127">*收件者類型*</span><span class="sxs-lookup"><span data-stu-id="67d78-127">*Recipient type*</span></span>                   |<span data-ttu-id="67d78-128">内部和外部收件人</span><span class="sxs-lookup"><span data-stu-id="67d78-128">Internal and external recipients</span></span>|<span data-ttu-id="67d78-129">仅限内部收件人</span><span class="sxs-lookup"><span data-stu-id="67d78-129">Internal recipients only</span></span>         |<span data-ttu-id="67d78-130">内部和外部收件人</span><span class="sxs-lookup"><span data-stu-id="67d78-130">Internal and external recipients</span></span>|
|<span data-ttu-id="67d78-131">*内部收件人的经验*</span><span class="sxs-lookup"><span data-stu-id="67d78-131">*Experience for internal recipient*</span></span>|<span data-ttu-id="67d78-132">收件人收到 HTML 消息，他们在 Web 浏览器或移动应用中下载并打开该邮件</span><span class="sxs-lookup"><span data-stu-id="67d78-132">Recipients receive an HTML message, which they download and open in a web browser or mobile app</span></span>|<span data-ttu-id="67d78-133">Outlook 客户端中的本机内联体验</span><span class="sxs-lookup"><span data-stu-id="67d78-133">Native inline experience in Outlook clients</span></span>|<span data-ttu-id="67d78-134">使用 Outlook 客户端为同一组织中的收件人提供本机内联体验。</span><span class="sxs-lookup"><span data-stu-id="67d78-134">Native inline experience for recipients in the same organization using Outlook clients.</span></span>  <span data-ttu-id="67d78-135">收件人可以使用 Outlook 以外的客户端从 OME 门户读取邮件（无需下载或应用）。</span><span class="sxs-lookup"><span data-stu-id="67d78-135">Recipients can read message from OME portal using clients other than Outlook (no download or app required).</span></span>|
|<span data-ttu-id="67d78-136">*外部收件人的经验*</span><span class="sxs-lookup"><span data-stu-id="67d78-136">*Experience for external recipient*</span></span>|<span data-ttu-id="67d78-137">收件人收到 HTML 消息，他们在 Web 浏览器或移动应用中下载并打开该邮件</span><span class="sxs-lookup"><span data-stu-id="67d78-137">Recipients receive an HTML message, which they download and open in a web browser or mobile app</span></span>|<span data-ttu-id="67d78-138">不適用</span><span class="sxs-lookup"><span data-stu-id="67d78-138">N/A</span></span>|<span data-ttu-id="67d78-139">Office 365 收件人的本机内联体验。</span><span class="sxs-lookup"><span data-stu-id="67d78-139">Native inline experience for Office 365 recipients.</span></span> <span data-ttu-id="67d78-140">所有其他收件人都可以从 OME 门户阅读邮件（无需下载或应用）。</span><span class="sxs-lookup"><span data-stu-id="67d78-140">All other recipients can read message from OME portal (no download or app required).</span></span>|
|<span data-ttu-id="67d78-141">*附件权限*</span><span class="sxs-lookup"><span data-stu-id="67d78-141">*Attachment permissions*</span></span>           |<span data-ttu-id="67d78-142">对附件没有限制</span><span class="sxs-lookup"><span data-stu-id="67d78-142">No restrictions on attachments</span></span>|<span data-ttu-id="67d78-143">附件受到保护</span><span class="sxs-lookup"><span data-stu-id="67d78-143">Attachments are protected</span></span>|<span data-ttu-id="67d78-144">附件受"不转发"选项和自定义模板的保护。</span><span class="sxs-lookup"><span data-stu-id="67d78-144">Attachments are protected for the Do Not Forward option and custom templates.</span></span> <span data-ttu-id="67d78-145">管理员可以选择"仅加密"选项的附件是否受到保护。</span><span class="sxs-lookup"><span data-stu-id="67d78-145">Admins can choose whether attachments for the Encrypt-Only option are protected or not.</span></span>|
|<span data-ttu-id="67d78-146">*自带密钥 （BYOK） 支持*</span><span class="sxs-lookup"><span data-stu-id="67d78-146">*Bring your own key (BYOK) support*</span></span>|<span data-ttu-id="67d78-147">無</span><span class="sxs-lookup"><span data-stu-id="67d78-147">None</span></span>                |<span data-ttu-id="67d78-148">無</span><span class="sxs-lookup"><span data-stu-id="67d78-148">None</span></span>               |<span data-ttu-id="67d78-149">BYOK 支持</span><span class="sxs-lookup"><span data-stu-id="67d78-149">BYOK supported</span></span>          |
||

## <a name="advantages-of-the-new-ome-capabilities-over-legacy-ome"></a><span data-ttu-id="67d78-150">与传统的 OME 产品具有新的 OME 功能的优势</span><span class="sxs-lookup"><span data-stu-id="67d78-150">Advantages of the new OME capabilities over legacy OME</span></span>

<span data-ttu-id="67d78-151">新功能具有以下优点：</span><span class="sxs-lookup"><span data-stu-id="67d78-151">The new capabilities provide the following advantages:</span></span>

- <span data-ttu-id="67d78-152">能够使用"仅加密"（支持安全协作）、不转发和自定义限制。</span><span class="sxs-lookup"><span data-stu-id="67d78-152">Ability to use Encrypt-Only (which enables secure collaboration), Do Not Forward, and custom restrictions.</span></span>
- <span data-ttu-id="67d78-153">发件人可以从 Outlook 桌面、Mac Outlook 和 Web 客户端上的 Outlook 发送使用新功能手动加密的邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-153">Senders can send mail encrypted with the new capabilities manually from Outlook Desktop, Outlook for Mac and Outlook on the web clients.</span></span>
- <span data-ttu-id="67d78-154">Office 365 收件人在支持的 Outlook 客户端中使用内联体验。</span><span class="sxs-lookup"><span data-stu-id="67d78-154">Office 365 recipients get to use an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="67d78-155">或者，管理员可以选择向 Office 365 收件人显示品牌体验。</span><span class="sxs-lookup"><span data-stu-id="67d78-155">Alternatively, admins can choose to show Office 365 recipients a branded experience.</span></span>
- <span data-ttu-id="67d78-156">Office 365 以外的帐户（如 Gmail、雅虎和 Microsoft 帐户）与 OME 门户联合使用，该门户为这些收件人提供更好的用户体验。</span><span class="sxs-lookup"><span data-stu-id="67d78-156">Accounts outside of Office 365, such as Gmail, Yahoo, and Microsoft accounts, are federated with the OME portal, which provides a better user experience for these recipients.</span></span> <span data-ttu-id="67d78-157">所有其他标识使用一次性密码访问加密邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-157">All other identities use a one-time pass code to access encrypted messages.</span></span>
- <span data-ttu-id="67d78-158">管理员可以自定义品牌，并创建多个品牌模板。</span><span class="sxs-lookup"><span data-stu-id="67d78-158">Admins can customize branding, and create multiple branding templates.</span></span>
- <span data-ttu-id="67d78-159">管理员可以撤消使用新功能加密的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-159">Admins can revoke emails encrypted with the new capabilities.</span></span>
- <span data-ttu-id="67d78-160">新功能通过安全&amp;合规性中心提供详细的使用情况报告。</span><span class="sxs-lookup"><span data-stu-id="67d78-160">The new capabilities provide detailed usage reports through the Security &amp; Compliance Center.</span></span>

## <a name="office-365-advanced-message-encryption-capabilities"></a><span data-ttu-id="67d78-161">Office 365 高级邮件加密功能</span><span class="sxs-lookup"><span data-stu-id="67d78-161">Office 365 Advanced Message Encryption capabilities</span></span>

<span data-ttu-id="67d78-162">Office 365 高级邮件加密在新的 OME 功能之上提供了其他功能。</span><span class="sxs-lookup"><span data-stu-id="67d78-162">Office 365 Advanced Message Encryption offers additional capabilities on top of the new OME capabilities.</span></span> <span data-ttu-id="67d78-163">您必须在组织中设置新的 Office 365 邮件加密功能，才能使用高级邮件加密功能。</span><span class="sxs-lookup"><span data-stu-id="67d78-163">You must have the new Office 365 Message Encryption capabilities set up in your organization in order to use the Advanced Message Encryption capabilities.</span></span> <span data-ttu-id="67d78-164">此外，为了使用这些功能，收件人必须通过 OME 门户查看和回复安全邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-164">Also, in order to use these capabilities, recipients must view and reply to secure mail through the OME Portal.</span></span> <span data-ttu-id="67d78-165">高级功能包括：</span><span class="sxs-lookup"><span data-stu-id="67d78-165">The advanced capabilities  include:</span></span>

- <span data-ttu-id="67d78-166">消息吊销</span><span class="sxs-lookup"><span data-stu-id="67d78-166">Message revocation</span></span>

- <span data-ttu-id="67d78-167">消息过期</span><span class="sxs-lookup"><span data-stu-id="67d78-167">Message expiration</span></span>

- <span data-ttu-id="67d78-168">多个品牌模板</span><span class="sxs-lookup"><span data-stu-id="67d78-168">Multiple branding templates</span></span>

<span data-ttu-id="67d78-169">GCC 高不支持 Office 365 高级邮件加密。</span><span class="sxs-lookup"><span data-stu-id="67d78-169">Office 365 Advanced Message Encryption is not supported in GCC High.</span></span>

<span data-ttu-id="67d78-170">有关使用高级邮件加密的信息，请参阅[Office 365 高级邮件加密](ome-advanced-message-encryption.md)。</span><span class="sxs-lookup"><span data-stu-id="67d78-170">For information on using Advanced Message Encryption, see [Office 365 Advanced Message Encryption](ome-advanced-message-encryption.md).</span></span>

## <a name="unique-characteristics-of-office-365-message-encryption-in-a-gcc-high-deployment"></a><span data-ttu-id="67d78-171">GCC 高部署中 Office 365 消息加密的独特特性</span><span class="sxs-lookup"><span data-stu-id="67d78-171">Unique characteristics of Office 365 Message Encryption in a GCC High deployment</span></span>

<span data-ttu-id="67d78-172">Office 365 高级邮件加密在 GCC 高环境中不可用。</span><span class="sxs-lookup"><span data-stu-id="67d78-172">Office 365 Advanced Message Encryption is not available in a GCC High environment.</span></span> <span data-ttu-id="67d78-173">您仍然可以在 GCC 高环境中使用单个品牌模板。</span><span class="sxs-lookup"><span data-stu-id="67d78-173">You can still use a single brand template in a GCC High environment.</span></span>

<span data-ttu-id="67d78-174">此外，如果您计划在 GCC 高环境中使用 Office 365 邮件加密，则收件人体验有一些独特的特征。</span><span class="sxs-lookup"><span data-stu-id="67d78-174">In addition, if you plan to use Office 365 Message Encryption in a GCC High environment, there are some unique characteristics about the recipient experience.</span></span>

<span data-ttu-id="67d78-175">GCC 高不支持 Office 365 高级邮件加密。</span><span class="sxs-lookup"><span data-stu-id="67d78-175">Office 365 Advanced Message Encryption is not supported in GCC High.</span></span>

### <a name="encrypted-email-from-gcc-high-to-gcc-high-recipients"></a><span data-ttu-id="67d78-176">从 GCC 高到 GCC 高收件人的加密电子邮件</span><span class="sxs-lookup"><span data-stu-id="67d78-176">Encrypted email from GCC High to GCC High recipients</span></span>

<span data-ttu-id="67d78-177">发件人可以在 Outlook 中手动加密 Web 上的 PC 和 Mac 和 Outlook 中的电子邮件，或者组织可以使用 Exchange 邮件流规则设置策略来加密电子邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-177">Senders can manually encrypt emails in Outlook for PC and Mac and Outlook on the web, or organizations can set up a policy to encrypt emails using Exchange mail flow rules.</span></span>

<span data-ttu-id="67d78-178">GCC High 中的收件人在 Web 上的 PC 和 Mac Outlook 和 Outlook 中接收与所有其他 Office 365 用户相同的内联阅读体验。</span><span class="sxs-lookup"><span data-stu-id="67d78-178">Recipients inside GCC High receive the same inline reading experience in Outlook for PC and Mac and Outlook on the web as all other Office 365 users.</span></span>

### <a name="encrypted-email-from-gcc-high-to-non-gcc-high-recipients"></a><span data-ttu-id="67d78-179">从 GCC 高到非 GCC 高收件人的加密电子邮件</span><span class="sxs-lookup"><span data-stu-id="67d78-179">Encrypted email from GCC High to Non-GCC High recipients</span></span>

<span data-ttu-id="67d78-180">GCC 高内部的发件人可以在 GCC 高边界之外发送加密电子邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-180">Senders inside GCC High can send encrypted email outside of the GCC High boundary.</span></span>

<span data-ttu-id="67d78-181">GCC High 以外的所有收件人（包括商业 Office 365 用户、Outlook.com用户和其他电子邮件提供商（如 Gmail 和 Yahoo）的用户都会收到一封包装邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-181">All recipients outside GCC High, including commercial Office 365 users, Outlook.com users, and other users of other email providers such as Gmail and Yahoo, receive a wrapper mail.</span></span> <span data-ttu-id="67d78-182">此包装邮件将收件人重定向到 OME 门户，收件人可以在其中读取和回复邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-182">This wrapper mail redirects the recipient to the OME Portal where the recipient can read and reply to message.</span></span>

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a><span data-ttu-id="67d78-183">在同一租户中共存旧 OME 和新功能</span><span class="sxs-lookup"><span data-stu-id="67d78-183">Coexistence of legacy OME and the new capabilities in the same tenant</span></span>

<span data-ttu-id="67d78-184">您可以在同一租户中同时使用旧版 OME 和新功能。</span><span class="sxs-lookup"><span data-stu-id="67d78-184">You can use both legacy OME and the new capabilities in the same tenant.</span></span> <span data-ttu-id="67d78-185">作为管理员，您可以通过选择要在创建邮件流规则时使用的 OME 版本来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="67d78-185">As an administrator, you do this by choosing which version of OME you want to use when you create your mail flow rules.</span></span>

- <span data-ttu-id="67d78-186">要指定 OME 的旧版本，请使用 Exchange 邮件流规则操作**应用 OME 的早期版本。**</span><span class="sxs-lookup"><span data-stu-id="67d78-186">To specify the legacy version of OME, use the Exchange mail flow rule action **Apply the previous version of OME**.</span></span>

- <span data-ttu-id="67d78-187">要指定新功能，请使用 Exchange 邮件流规则操作**应用 Office 365 邮件加密和权限保护**。</span><span class="sxs-lookup"><span data-stu-id="67d78-187">To specify the new capabilities, use the Exchange mail flow rule action **Apply Office 365 Message Encryption and rights protection**.</span></span>

<span data-ttu-id="67d78-188">用户可以手动发送使用 Outlook 桌面、Outlook Mac 和 Web 上的 Outlook 中的新功能加密的邮件。</span><span class="sxs-lookup"><span data-stu-id="67d78-188">Users can manually send mail that is encrypted with the new capabilities from Outlook Desktop, Outlook for Mac, and Outlook on the web.</span></span>

## <a name="migrate-from-legacy-ome-to-the-new-capabilities"></a><span data-ttu-id="67d78-189">从旧版 OME 迁移到新功能</span><span class="sxs-lookup"><span data-stu-id="67d78-189">Migrate from legacy OME to the new capabilities</span></span>

<span data-ttu-id="67d78-190">即使两个版本的 OME 可以共存，我们强烈建议您编辑使用规则操作的旧邮件流规则**应用 OME 的早期版本**以使用新功能。</span><span class="sxs-lookup"><span data-stu-id="67d78-190">Even though both versions of OME can coexist, we highly recommend that you edit your old mail flow rules that use the rule action **Apply the previous version of OME** to use the new capabilities.</span></span> <span data-ttu-id="67d78-191">更新这些规则以使用邮件流规则操作应用**Office 365 邮件加密和权限保护**。</span><span class="sxs-lookup"><span data-stu-id="67d78-191">Update these rules to use the mail flow rule action **Apply Office 365 Message Encryption and rights protection**.</span></span> <span data-ttu-id="67d78-192">有关说明，请参阅[定义邮件流规则以加密 Office 365 中的电子邮件。](define-mail-flow-rules-to-encrypt-email.md)</span><span class="sxs-lookup"><span data-stu-id="67d78-192">For instructions, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>

## <a name="get-started-with-ome"></a><span data-ttu-id="67d78-193">开始使用 OME</span><span class="sxs-lookup"><span data-stu-id="67d78-193">Get started with OME</span></span>

<span data-ttu-id="67d78-194">通常，新的 OME 功能会自动为 Office 365 组织启用。</span><span class="sxs-lookup"><span data-stu-id="67d78-194">Typically, the new OME capabilities are automatically enabled for your Office 365 organization.</span></span> <span data-ttu-id="67d78-195">有关组织中新的 OME 功能的详细信息，请参阅[设置新的 Office 365 邮件加密功能](set-up-new-message-encryption-capabilities.md)。</span><span class="sxs-lookup"><span data-stu-id="67d78-195">For more information about the new OME capabilities within your organization, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md).</span></span>

<span data-ttu-id="67d78-196">如果启用了 Azure 信息保护，则 Office 365 组织将自动启用旧版 OME。</span><span class="sxs-lookup"><span data-stu-id="67d78-196">The legacy version of OME is automatically enabled for your Office 365 organization if you have enabled Azure Information Protection.</span></span> <span data-ttu-id="67d78-197">过去，即使未启用 Azure 信息保护，旧版 OME 也有效。</span><span class="sxs-lookup"><span data-stu-id="67d78-197">In the past, legacy OME worked even if Azure Information Protection wasn’t enabled.</span></span> <span data-ttu-id="67d78-198">情况已经不同了。</span><span class="sxs-lookup"><span data-stu-id="67d78-198">This is no longer the case.</span></span>

<span data-ttu-id="67d78-199">要开始使用旧版 OME，如果已启用 Azure 信息保护，请配置使用规则操作的邮件流规则**应用 OME 的早期版本。**</span><span class="sxs-lookup"><span data-stu-id="67d78-199">To start using legacy OME, if you have enabled Azure Information Protection, configure mail flow rules that use the rule action **Apply the previous version of OME**.</span></span> <span data-ttu-id="67d78-200">有关说明，请参阅[定义邮件流规则以加密 Office 365 中的电子邮件。](define-mail-flow-rules-to-encrypt-email.md)</span><span class="sxs-lookup"><span data-stu-id="67d78-200">For instructions, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>