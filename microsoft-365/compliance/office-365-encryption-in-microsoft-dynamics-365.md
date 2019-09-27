---
title: 微软动态 365 中的 Office 365 加密
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 摘要：了解微软动态365中的加密。
ms.openlocfilehash: 7c2a352dd712b0db9d2ad623745f854b863dd2e0
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37077859"
---
# <a name="office-365-encryption-in-microsoft-dynamics-365"></a><span data-ttu-id="eb4d7-103">微软动态 365 中的 Office 365 加密</span><span class="sxs-lookup"><span data-stu-id="eb4d7-103">Office 365 Encryption in Microsoft Dynamics 365</span></span>

<span data-ttu-id="eb4d7-104">Microsoft 使用加密技术在 Microsoft 数据库中静态时保护 Dynamics 365 中的客户数据，并在用户设备和数据中心之间传输。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-104">Microsoft uses encryption technology to protect customer data in Dynamics 365 while at rest in a Microsoft database and while it is in transit between user devices and our datacenters.</span></span> <span data-ttu-id="eb4d7-105">客户和 Microsoft 数据中心之间建立的连接经过加密，所有公共终结点都使用行业标准 TLS 进行保护。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-105">Connections established between customers and Microsoft datacenters are encrypted, and all public endpoints are secured using industry-standard TLS.</span></span> <span data-ttu-id="eb4d7-106">TLS 有效地建立了安全增强的浏览器到服务器连接，以帮助确保桌面和数据中心之间的数据机密性和完整性。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-106">TLS effectively establishes a security-enhanced browser-to-server connection to help ensure data confidentiality and integrity between desktops and datacenters.</span></span> <span data-ttu-id="eb4d7-107">激活数据加密后，无法将其关闭。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-107">After data encryption is activated, it cannot be turned off.</span></span> <span data-ttu-id="eb4d7-108">有关详细信息，请参阅[字段级数据加密](https://msdn.microsoft.com/en-us/library/dn481562.aspx)。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-108">For more information, see [Field-level data encryption](https://msdn.microsoft.com/en-us/library/dn481562.aspx).</span></span>

<span data-ttu-id="eb4d7-109">Dynamics 365 对一组包含敏感信息（如用户名和电子邮件密码）的默认实体属性使用标准的 Microsoft SQL Server 单元级加密。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-109">Dynamics 365 uses standard Microsoft SQL Server cell level encryption for a set of default entity attributes that contain sensitive information, such as user names and email passwords.</span></span> <span data-ttu-id="eb4d7-110">此功能可帮助组织满足与 FIPS 140-2 相关的合规性要求。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-110">This feature can help organizations meet the compliance requirements associated with FIPS 140-2.</span></span> <span data-ttu-id="eb4d7-111">字段级数据加密在利用[Microsoft Dynamics CRM 电子邮件路由器](https://technet.microsoft.com/en-us/library/hh699800.aspx)的方案中尤其重要，该路由器必须存储用户名和密码，才能在 Dynamics 365 实例和电子邮件服务之间实现集成。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-111">Field-level data encryption is especially important in scenarios that leverage the [Microsoft Dynamics CRM Email Router](https://technet.microsoft.com/en-us/library/hh699800.aspx), which must store user names and passwords to enable integration between a Dynamics 365 instance and an email service.</span></span> 

<span data-ttu-id="eb4d7-112">Dynamics 365 的所有实例都使用[Microsoft SQL Server 透明数据加密](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017)（TDE） 在写入磁盘（静态）时对数据执行实时加密。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-112">All instances of Dynamics 365 use [Microsoft SQL Server Transparent Data Encryption](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) (TDE) to perform real-time encryption of data when written to disk (at rest).</span></span> <span data-ttu-id="eb4d7-113">TDE 加密 SQL 服务器、Azure SQL 数据库和 Azure SQL 数据仓库数据文件。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-113">TDE encrypts SQL Server, Azure SQL Database, and Azure SQL Data Warehouse data files.</span></span> <span data-ttu-id="eb4d7-114">默认情况下，Microsoft 会存储和管理 Dynamics 365 实例的数据库加密密钥。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-114">By default, Microsoft stores and manages the database encryption keys for your instances of Dynamics 365.</span></span> <span data-ttu-id="eb4d7-115">（Dynamics 365 用于财务的密钥由 .NET 框架数据保护 API 生成。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-115">(The keys that are used by Dynamics 365 for Financials are generated by the .NET Framework Data Protection API.)</span></span> 

<span data-ttu-id="eb4d7-116">Dynamics 365 管理中心中的管理密钥功能使管理员能够自行管理与 Dynamics 365 实例关联的数据库加密密钥。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-116">The manage keys feature in the Dynamics 365 Administration Center gives administrators the ability to self-manage the database encryption keys that are associated with instances of Dynamics 365.</span></span> <span data-ttu-id="eb4d7-117">（自管数据库加密密钥仅在 Microsoft Dynamics 365 的 2017 年 1 月更新中可用，可能无法用于更高版本。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-117">(Self-managed database encryption keys are only available in the January 2017 update for Microsoft Dynamics 365 and may not be made available for later versions.</span></span> <span data-ttu-id="eb4d7-118">有关详细信息，请参阅管理[Dynamics 365（联机）实例的加密密钥。](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance)密钥管理功能同时支持 PFX 和 BYOK 加密密钥文件，例如存储在 HSM 中的文件。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-118">For more information, see [Manage the encryption keys for your Dynamics 365 (online) instance](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance).) The key management feature supports both PFX and BYOK encryption key files, such as those stored in an HSM.</span></span> <span data-ttu-id="eb4d7-119">（有关通过 Internet 生成和传输受 HSM 保护的密钥的详细信息，请参阅[如何为 Azure 密钥保管库生成和传输受 HSM 保护的密钥。](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)</span><span class="sxs-lookup"><span data-stu-id="eb4d7-119">(For more information about generating and transferring an HSM-protected key over the Internet, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys).)</span></span> 

<span data-ttu-id="eb4d7-120">要使用上载加密密钥选项，您需要公共加密密钥和私有加密密钥。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-120">To use the upload encryption key option, you need both the public and private encryption key.</span></span>

<span data-ttu-id="eb4d7-121">密钥管理功能通过使用 Azure 密钥保管库安全地存储加密密钥，从而从加密密钥管理中排除了复杂性。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-121">The key management feature takes the complexity out of encryption key management by using Azure Key Vault to securely store encryption keys.</span></span> <span data-ttu-id="eb4d7-122">Azure 密钥保管库有助于保护云应用程序和服务使用的加密密钥和机密。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-122">Azure Key Vault helps safeguard cryptographic keys and secrets used by cloud applications and services.</span></span> <span data-ttu-id="eb4d7-123">密钥管理功能不要求您具有 Azure 密钥保管库订阅，在大多数情况下，无需访问保管库中用于 Dynamics 365 的加密密钥。</span><span class="sxs-lookup"><span data-stu-id="eb4d7-123">The key management feature doesn't require that you have an Azure Key Vault subscription and for most situations there is no need to access encryption keys used for Dynamics 365 within the vault.</span></span>