---
title: 從 Google Postini、Barracuda Spam and Virus Firewall 或 Cisco IronPort 切換到 EOP
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 81b75194-3b04-48da-8b81-951afbabedde
description: 本主題的目的在於協助您了解從內部部署電子郵件檢疫裝置或雲端保護服務切換到 Exchange Online Protection (EOP) 的程序，然後提供給您開始使用的說明資源。
ms.openlocfilehash: c9d8bc73ee6226bececed7d8a4fc66b0eccfa6e1
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "39971391"
---
# <a name="switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco-ironport"></a><span data-ttu-id="b5ff7-103">從 Google Postini、Barracuda Spam and Virus Firewall 或 Cisco IronPort 切換到 EOP</span><span class="sxs-lookup"><span data-stu-id="b5ff7-103">Switch to EOP from Google Postini, the Barracuda Spam and Virus Firewall, or Cisco IronPort</span></span>

 <span data-ttu-id="b5ff7-p101">本主題的目的在於協助您了解從內部部署電子郵件檢疫裝置或雲端保護服務切換到 Exchange Online Protection (EOP) 的程序，然後提供給您開始使用的說明資源。有許多垃圾郵件篩選解決方案，但在大多數情況下，切換到 EOP 的程序類型很類似。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-p101">The purpose of this topic is to help you understand the process for switching to Exchange Online Protection (EOP) from an on-premises email hygiene appliance or cloud-based protection service, and then to provide you with help resources to get started. There are many spam-filtering solutions, but the process for switching to EOP is similar in most cases.</span></span>

<span data-ttu-id="b5ff7-106">如果您是初次使用 EOP 而且想要在決定切換前閱讀其功能概觀，請從[Exchange Online Protection 概觀](exchange-online-protection-overview.md)主題開始。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-106">If you are new to EOP and you want to read an overview of its features before you decide to switch, start with the [Exchange Online Protection overview](exchange-online-protection-overview.md) on TechNet.</span></span>

<span data-ttu-id="b5ff7-p102">在您切換到 EOP 之前，請思考要在雲端 (使用 Exchange Online)、內部部署或在混合案例中託管 EOP 保護的信箱 (「混合」的意思是，有些信箱裝載於內部部署，有些信箱裝載於 Exchange Online)。每個託管案例：雲端、內部部署和混合式部署都可行，但設定步驟有所不同。下列考量可協助您選擇適當的部署：</span><span class="sxs-lookup"><span data-stu-id="b5ff7-p102">Before you switch to EOP, it's important to think about whether you want to host your EOP-protected mailboxes in the cloud, with Exchange Online, on-premises, or in a hybrid scenario. (Hybrid means that you have some mailboxes hosted on-premises and another portion hosted with Exchange Online.) Each of these hosting scenarios: cloud, on-premises, and hybrid, is possible, but the setup steps can vary. Here are a few considerations to help you choose the appropriate deployment:</span></span>

- <span data-ttu-id="b5ff7-110">**內部部署信箱的 EOP 保護**：如果有想要使用的現有郵件託管基礎結構，或有將信箱保留在內部部署的業務需求，而且想要使用 EOP 做為您雲端電子郵件的保護，則適合使用此案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-110">**EOP protection with on-premises mailboxes** This scenario is appropriate if you have existing mail-hosting infrastructure you want to use, or you have business requirements to keep mailboxes on-premises, and you want EOP's cloud-based email protection.</span></span> <span data-ttu-id="b5ff7-111">[切換至 Exchange Online](#switch-to-eop-standalone) 詳細說明此案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-111">[Switch to EOP standalone](#switch-to-eop-standalone) describes this scenario in more detail.</span></span>

- <span data-ttu-id="b5ff7-112">**Exchange Online 信箱的 EOP 保護**：如果您想要 EOP 保護而所有信箱都裝載在雲端，則適合使用此案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-112">**EOP protection with Exchange Online mailboxes** This scenario is appropriate if you want EOP protection and all of your mailboxes hosted in the cloud.</span></span> <span data-ttu-id="b5ff7-113">這可協助您降低複雜度，因為您不需維護內部部署的郵件伺服器。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-113">It can help you reduce complexity, because you don't have to maintain on-premises messaging servers.</span></span> <span data-ttu-id="b5ff7-114">[切換至 Exchange Online](#switch-to-exchange-online) 說明此案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-114">[Switch to Exchange Online](#switch-to-exchange-online) describes this scenario.</span></span>

- <span data-ttu-id="b5ff7-115">**混合信箱的 EOP 保護**：也許您想要雲端信箱，但您必須將某些使用者的信箱保留在內部部署。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-115">**EOP protection with hybrid mailboxes** Perhaps you want cloud mailboxes, but you need to keep mailboxes for some users on-premises.</span></span> <span data-ttu-id="b5ff7-116">如果您希望有些信箱裝載於內部部署，而有些信箱裝載於 Exchange Online，則選擇此案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-116">Choose this scenario if you want some mailboxes hosted on-premises and another portion hosted with Exchange Online.</span></span> <span data-ttu-id="b5ff7-117">[切換至混合解決方案](#switch-to-a-hybrid-solution)說明此案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-117">[Switch to a hybrid solution](#switch-to-a-hybrid-solution) describes this scenario.</span></span>

## <a name="switch-to-eop-standalone"></a><span data-ttu-id="b5ff7-118">切換至獨立式 EOP</span><span class="sxs-lookup"><span data-stu-id="b5ff7-118">Switch to EOP standalone</span></span>

<span data-ttu-id="b5ff7-p106">如果您目前將信箱託管於內部部署，而且使用內部部署保護裝置或雲端郵件保護服務，即可切換至 EOP，充分利用其保護功能和可用性。若要在獨立環境中設定 EOP (這表示您將信箱託管於內部部署並使用 EOP 提供郵件保護)，可以遵循[設定 EOP 服務](set-up-your-eop-service.md)中簡述的步驟。本主題檢視設定 EOP 保護的步驟，包含註冊、新增網域以及設定郵件流程與連接器。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-p106">If you currently host your mailboxes on premises and use an on-premises protection appliance or a cloud messaging-protection service, you can switch to EOP to take advantage of its protection features and availability. To set up EOP in a standalone scenario, which means you host your mailboxes on premises and use EOP to provide email protection, you can follow the steps outlined in [Set up your EOP service](set-up-your-eop-service.md). The topic outlines the steps for setting up EOP protection, which include sign up, adding your domain, and setting up mail flow with connectors.</span></span>

## <a name="switch-to-exchange-online"></a><span data-ttu-id="b5ff7-122">切換至 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b5ff7-122">Switch to Exchange Online</span></span>

<span data-ttu-id="b5ff7-123">或許您有以內部部署裝置保護的內部部署信箱，而想要換成 Exchange Online 雲端託管信箱與 EOP 保護，以享有 Office365 雲端郵件和保護功能。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-123">Perhaps you have on-premises mailboxes protected by an on-premises appliance, and you want to jump to Exchange Online cloud-hosted mailboxes and EOP protection to take advantage of Office 365 cloud messaging and protection features.</span></span> <span data-ttu-id="b5ff7-124">若要開始進行，您可以註冊 Office365 並新增網域。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-124">To get started, you can sign up for Office 365 and add your domain.</span></span> <span data-ttu-id="b5ff7-125">此案例不需要設定連接器，因為沒有任何資料路由傳送至內部部署信箱。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-125">This scenario doesn't require you to setup connectors, because there isn't any routing to on-premises mailboxes.</span></span> <span data-ttu-id="b5ff7-126">從[使用 Office 365 獲取最新的進階功能](https://www.microsoft.com/microsoft-365/business/compare-more-office-365-for-business-plans)開始，註冊並熟悉其功能。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-126">Begin at [Get the latest advanced features with Office 365](https://www.microsoft.com/microsoft-365/business/compare-more-office-365-for-business-plans) to sign-up and get familiar with its features.</span></span>

<span data-ttu-id="b5ff7-127">在 Office 365 設定過程中，您將建立雲端信箱使用者。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-127">During the Office 365 setup process, you will create your cloud-based mailbox users.</span></span>

## <a name="switch-to-a-hybrid-solution"></a><span data-ttu-id="b5ff7-128">切換至混合解決方案</span><span class="sxs-lookup"><span data-stu-id="b5ff7-128">Switch to a hybrid solution</span></span>

<span data-ttu-id="b5ff7-p108">您可能因為業務需求或法規考量，只想要將部分信箱移至雲端。當您部署混合案例時，可根據業務需求將信箱移至雲端。遷移至具有 EOP 保護的混合案例，比移至全雲端案例更加複雜，但 Microsoft 提供了完整的混合支援和豐富的資源，讓您能更加輕鬆地移至混合案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-p108">You may want to move only a portion of your mailboxes to the cloud because of business requirements or regulatory considerations. When you deploy a hybrid scenario, you can move mailboxes to the cloud as your business requirements dictate. Migrating to a hybrid scenario with EOP protection is more complicated than moving to an all-cloud scenario, but Microsoft provides full hybrid support and ample resources to make the move to hybrid easier.</span></span>

<span data-ttu-id="b5ff7-132">如果考慮採用混合式部署，[Exchange Server 混合式部署](https://docs.microsoft.com/exchange/exchange-hybrid)是最佳起點。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-132">The best place to start, if you are considering a hybrid deployment, is [Exchange Server 2013 Hybrid Deployments](https://docs.microsoft.com/exchange/exchange-hybrid).</span></span> <span data-ttu-id="b5ff7-133">此外，還有幾個不同且重要的方式，可讓您在混合案例中路由郵件。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-133">Additionally, there are a few different ways you can route mail in a hybrid scenario that are important to understand.</span></span> <span data-ttu-id="b5ff7-134">[在 Exchange 混合式部署傳輸路由](https://docs.microsoft.com/exchange/transport-routing)說明每種類型，以便您根據業務需求來選擇最佳路由案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-134">[Transport Routing in Exchange 2013 Hybrid Deployments](https://docs.microsoft.com/exchange/transport-routing) explains each type, so you can choose the best routing scenario, based on your business requirements.</span></span>

## <a name="migration-planning"></a><span data-ttu-id="b5ff7-135">移轉規劃</span><span class="sxs-lookup"><span data-stu-id="b5ff7-135">Migration planning</span></span>

<span data-ttu-id="b5ff7-136">當您決定切換至 EOP 時，請務必提供下列方面的特殊考量：</span><span class="sxs-lookup"><span data-stu-id="b5ff7-136">When you decide to switch to EOP, make sure you give special consideration to the following areas:</span></span>

- <span data-ttu-id="b5ff7-137">**自訂篩選規則**：如果您有自訂篩選規則或企業政策規則可捕捉特定垃圾郵件，建議您先以預設設定試用 EOP 一段時間，然後才遷移規則。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-137">**Custom Filtering Rules** If you have custom filtering or business-policy rules to catch specific spam, we recommend that you try EOP with the default settings for a period, before you migrate your rules.</span></span> <span data-ttu-id="b5ff7-138">EOP 提供具有預設設定的企業級垃圾郵件保護，結果可能是您不需要將部分規則遷移至 EOP。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-138">EOP offers enterprise-level spam protection with the default settings, it may turn out that you don't need to migrate some of your rules to EOP.</span></span> <span data-ttu-id="b5ff7-139">當然，如果現有的規則會強制執行特定自訂業務原則，即可建立這些原則。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-139">Of course, if you have rules in place that enforce specific custom business policies, you can create those.</span></span> <span data-ttu-id="b5ff7-140">[Exchange Online Protection 中的郵件流程規則（傳輸規則）](mail-flow-rules-transport-rules-0.md)提供在 EOP 建立郵件流程規則的詳細指示。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-140">[Mail flow rules (transport rules) in Exchange Online Protection](mail-flow-rules-transport-rules-0.md) provides detailed instructions for creating mail flow rules in EOP.</span></span>

- <span data-ttu-id="b5ff7-141">**IP 允許清單和 IP 封鎖清單**：如果您有每一使用者的允許清單和封鎖清單，請在設定過程中留出一些時間將這些清單複製到 EOP。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-141">**IP allow lists and IP block lists** If you have per-user allow lists and block lists, allow some time to copy the lists to EOP as part of your setup process.</span></span> <span data-ttu-id="b5ff7-142">如需 IP 允許清單和 IP 封鎖清單的相關資訊，請參閱[設定連線篩選原則](configure-the-connection-filter-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-142">For more information about IP allow lists and IP block lists, see [Configure the Connection Filter Policy](configure-the-connection-filter-policy.md).</span></span>

- <span data-ttu-id="b5ff7-143">**安全通訊**：如果合作夥伴要求郵件必須加密，建議您在 Exchange 系統管理中心設定此案例。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-143">**Secure Communication** If you have a partner that requires encrypted messaging, we recommend that you set this up in the Exchange admin center.</span></span> <span data-ttu-id="b5ff7-144">如要設定此案例，請查閱[設定連接器以保護與合作夥伴間的郵件流程安全](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-for-secure-mail-flow-with-a-partner)。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-144">For details, see [Set up connectors for secure mail flow with a partner organization](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-for-secure-mail-flow-with-a-partner).</span></span>

> [!TIP]
> <span data-ttu-id="b5ff7-145">當您從內部部署裝置切換至 EOP 時，有可能將裝置或伺服器保留在原地，以執行業務規則檢查。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-145">When you switch from an on-premises appliance to EOP, it is possible to leave your appliance or a server in place that performs business rule checks.</span></span> <span data-ttu-id="b5ff7-146">例如，若裝置對輸出郵件執行自訂篩選，而且希望繼續這麼做，您可以設定 EOP，在郵件路由傳送至網際網路之前，直接傳送至此裝置進行額外篩選。</span><span class="sxs-lookup"><span data-stu-id="b5ff7-146">For instance, if your appliance performs custom filtering on outbound mail, and you want it to continue doing so, you can configure EOP to send mail directly to the appliance for additional filtering, before it is routed to the Internet.</span></span>