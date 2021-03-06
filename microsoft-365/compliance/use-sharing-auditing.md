---
title: 稽核共用來找出與外部使用者共用的資源
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.collection: M365-security-compliance
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: '共享是共享点在线和一个业务一个驱动器的关键活动。 管理员现在可以在 Office 365 审核日志中使用共享审核来标识与组织外部用户共享的资源。 '
ms.openlocfilehash: 48fc1a67f501c807e76ba2333170df83a1248428
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078265"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>稽核共用來找出與外部使用者共用的資源

共享是 SharePoint 在线和 OneDrive 业务中的一项关键活动，在 Office 365 组织中广泛使用。 管理员可以在 Office 365 审核日志中使用共享审核来确定在其组织中如何使用共享。 
  
## <a name="the-sharepoint-sharing-schema"></a>共享点共享架构

共享事件（不包括与共享策略和共享链接相关的事件）以一种主要方式与文件和文件夹相关事件不同：一个用户正在执行对另一个用户有影响的操作。 例如，当资源用户 A 授予用户 B 对文件的访问权限时。 在此示例中，用户 A 是*代理用户，* 用户 B 是*目标用户。* 在 SharePoint 文件架构中，代理用户的操作仅影响文件本身。 当用户 A 打开文件时，"**文件访问"** 事件中所需的唯一信息是代理用户。 为了解决这种差异，有一个单独的架构，称为*SharePoint 共享架构，* 用于捕获有关共享事件的详细信息。 这可确保管理员能够了解共享资源的人员以及共享资源的用户。 
  
共享架构在审核记录中提供了与共享事件相关的两个附加字段： 
  
- **目标用户或组类型：** 标识目标用户或组是成员、来宾、SharePoint 组、安全组还是合作伙伴。

- **目标用户或组名称：** 存储与资源共享的资源的目标用户或组（上例中的用户 B）的 UPN 或名称。 

除了 Office 365 审核日志架构（如"用户、操作"和"日期"）中的其他属性外，这两个字段还可以讲述*有关哪些*用户与*谁*共享*哪些*资源以及*何时*共享资源的完整故事。 
  
还有另一个架构属性对共享故事很重要。 导出审核日志搜索结果时，导出的 CSV 文件中的**AuditData**列会存储有关共享事件的信息。 例如，当用户与另一个用户共享网站时，这是通过将目标用户添加到 SharePoint 组来实现的。 "**审核数据"** 列捕获此信息，为管理员提供上下文。 有关如何分析**AuditData**列中的信息的说明，请参阅[步骤 2。](#step-2-use-the-powerquery-editor-to-format-the-exported-audit-log)

## <a name="sharepoint-sharing-events"></a>共享点共享事件

共享由用户（*代理*用户）希望与其他用户（*目标*用户）共享资源时定义。 与与外部用户共享资源相关的审核记录（组织外部且在组织的 Azure 活动目录中没有来宾帐户的用户）由以下事件标识，这些事件记录在 Office 365 中审核日志：

- **共享邀请已创建：** 组织中的用户尝试与外部用户共享资源（可能是站点）。 这将导致向目标用户发送外部共享邀请。 此时不授予对资源的访问权限。

- **共享邀请接受：** 外部用户已接受代理用户发送的共享邀请，现在有权访问该资源。

- **匿名链接已创建：** 为资源创建匿名链接（也称为"任何人"链接）。 由于可以创建匿名链接，然后复制匿名链接，因此可以合理地假定具有匿名链接的任何文档都已与目标用户共享。

- **匿名链接已使用：** 顾名思义，当使用匿名链接访问资源时，将记录此事件。 

- **已创建安全链接：** 用户已创建"特定人员链接"，以便与特定人员共享资源。 此目标用户可能是组织外部的人员。 与资源共享的人员**在"添加到安全链接"** 事件的审核记录中标识。 这两个事件的时间戳几乎相同。

- **添加到安全链接：** 用户已添加到特定人员链接。 在此事件中**使用"目标用户或组名"** 字段来标识添加到相应特定人员链接的用户。 此目标用户可能是组织外部的人员。

## <a name="sharing-auditing-work-flow"></a>共享审核工作流
  
当用户（代理用户）希望与其他用户（目标用户）共享资源时，SharePoint（或企业 OneDrive）首先检查目标用户的电子邮件地址是否已与组织目录中的用户帐户关联。 如果目标用户位于目录中（并且具有相应的来宾用户帐户），则 SharePoint 执行以下操作：
  
-  通过将目标用户添加到相应的 SharePoint 组，立即分配目标用户访问资源的权限，并**记录"添加到组"** 事件。 
    
- 向目标用户的电子邮件地址发送共享通知。
    
- 记录**共享集**事件。 此事件在审核日志搜索工具的活动选取器**中的"共享**文件、文件夹或站点"下具有"共享文件、文件夹或站点"的友好名称。 请参阅[步骤 1](#step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file)中的屏幕截图。 
    
如果目标用户的用户帐户不在目录中，SharePoint 将执行以下操作： 
    
   - 根据资源的共享方式记录以下事件之一：
   
      - **匿名链接已创建**
   
      - **已创建安全链接**
   
      - **添加到安全链接** 

      - **共享邀请已创建**（仅当共享资源是站点时，才会记录此事件）
    
   - 当目标用户接受发送给他们的共享邀请时（通过单击邀请中的链接），SharePoint 会记录**共享邀请接受**事件，并分配目标用户访问资源的权限。 如果向目标用户发送匿名链接，则在目标用户使用该链接访问资源后，将记录**匿名链接事件。** 对于安全链接，当外部用户使用链接访问资源时，将记录**FileAccess 事件。**

还会记录有关目标用户的其他信息，例如邀请对象的用户的身份和接受邀请的用户的身份。 在某些情况下，这些用户（或电子邮件地址）可能不同。 

## <a name="how-to-identify-resources-shared-with-external-users"></a>如何识别与外部用户共享的资源

管理员的一个常见要求是创建与组织外部用户共享的所有资源的列表。 通过在 Office 365 中使用共享审核，管理员可以生成此列表。 方法如下。
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>步骤 1：搜索共享事件并将结果导出到 CSV 文件

第一步是搜索 Office 365 审核日志以查找共享事件。 有关搜索审核日志的详细信息（包括所需的权限），请参阅[在安全&合规性中心中搜索审核日志。](search-the-audit-log-in-security-and-compliance.md)
  
1. 移至 [https://protection.office.com](https://protection.office.com)。
    
2. 使用公司或學校帳戶登入 Office 365。
    
3. 在"安全&合规性中心"的左侧窗格中，**单击"搜索**  > **审核日志搜索"。**
    
    将显示**审核日志搜索**页。 
    
4. 在"**活动"** 下，**单击"共享"和"访问请求活动"** 以搜索与共享相关的事件。 
    
    ![在"活动"下，选择"共享和访问请求活动"](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  选择日期和时间范围以查找该时间段内发生的共享事件。 
    
6. **单击"搜索"** 以运行搜索。 
    
7. 当搜索完成运行并显示结果时，**单击"导出结果**\>**下载所有结果"。**
    
    选择导出选项后，窗口底部的一条消息将提示您打开或保存 CSV 文件。
    
8. **单击"另存**\>**为"，** 将 CSV 文件保存到本地计算机上的文件夹中。 

### <a name="step-2-use-the-powerquery-editor-to-format-the-exported-audit-log"></a>第 2 步：使用 PowerQuery 编辑器格式化导出的审核日志

下一步是使用 Excel 中的电源查询编辑器中的 JSON 转换功能将**AuditData**列中的每个属性（由多属性 JSON 对象组成）拆分为自己的列。 这允许您筛选列以查看与共享相关的记录

有关分步说明，请参阅"步骤 2：使用 Power 查询编辑器格式化导出的审核[日志"，请参阅导出、配置和查看审核日志记录。](export-view-audit-log-records.md#step-2-format-the-exported-audit-log-using-the-power-query-editor)

### <a name="step-3-filter-the-csv-file-for-resources-shared-with-external-users"></a>步骤 3：筛选 CSV 文件，以便与外部用户共享资源

下一步是筛选以前在[SharePoint 共享事件](#sharepoint-sharing-events)部分中描述的不同共享相关事件的 CSV。 或者，您可以**筛选"目标用户或组类型"** 列以显示此属性的值为**来宾**的所有记录。 

按照上一步中的说明使用 PowerQuery 编辑器准备 CSV 文件后，请执行以下操作：
    
1. 打开您在步骤 2 中创建的 Excel 文件。 

2. 在"**主页"** 选项卡上，**单击"排序&筛选器，** 然后单击"**筛选"。**
    
3. **在"操作"** 列的"**排序&筛选器"** 下拉列表中，清除所有选择，然后选择以下一个或多个与共享相关的事件，然后单击"**确定**"。
 
   - **共享邀请已创建**
   
   - **匿名链接已创建**
   
   - **已创建安全链接**
   
   - **添加到安全链接** 
    
    Excel 显示所选事件的行。
    
4. 转到**名为"目标用户或组类型"** 的列并选择它。 
    
5. 在"**排序&筛选器下**拉列表中，清除所有选择，然后**选择"目标用户或组类型：来宾"，** 然后单击"**确定"。**
    
    现在，Excel 显示用于共享事件的行和目标用户在组织之外的位置，因为外部用户由**值"目标用户"或"类型：来宾"** 标识。 
  
> [!TIP]
> 对于显示的审核**记录，"ObjectId"** 列标识与目标用户共享的资源;对于"目标 Id"列，将标识与目标用户共享的资源。例如`ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
