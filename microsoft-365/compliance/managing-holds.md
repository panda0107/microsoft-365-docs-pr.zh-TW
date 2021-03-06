---
title: 管理高级电子数据展示中的保留
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1e457ffa05670e6a8b48692bbb382ebd8f2b404e
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2019
ms.locfileid: "37077173"
---
# <a name="manage-holds-in-advanced-ediscovery"></a>管理高级电子数据展示中的保留

您可以使用高级电子数据展示案例创建保留，以保留可能与您的案例相关的内容。 使用高级电子数据展示保留功能，您可以对保管人及其数据源进行保留。 此外，您还可以对邮箱和 OneDrive 进行非托管保留。 您还可以在 Office 365 组的组邮箱、SharePoint 站点和 OneDrive 业务站点上放置保留。 同样，您可以在与 Microsoft Teams 关联的邮箱和站点上放置保留。 将内容位置置于保留状态时，将保留内容，直到您释放保管人、删除特定数据位置或完全删除保留策略。

## <a name="manage-custodian-based-holds"></a>管理基于托管人的保留

在某些情况下，您可能具有一组已标识并选择保留的数据保管人。 在高级电子数据展示中，当这些保管人被置于保留状态时，用户及其所选数据源将自动添加到保管人保留策略中。 

要查看保管人持有策略：

1. 在**安全&合规中心**中，**单击"电子数据>高级电子数据展示"** 以显示组织中的案件列表。
   
2. **转到"保管人"** 选项卡，在案例中添加保管人。 要了解如何在高级电子数据展示案例中添加和将保管人置于保留状态，请参阅[将保管人添加到高级电子数据展示案例](add-custodians-to-case.md)。 如果您已添加保管人并将其置于保留状态，则转到步骤 3。
   
3. **转到"保留"** 选项卡并选择"保管政策"。
   
4. 在弹出窗口中，您可以看到策略的保留统计信息。 您还可以执行诸如将查询应用于基于保管人的保留等操作。 有关创建保留查询和使用条件的详细信息，请参阅[关键字查询和内容搜索的搜索条件。](keyword-queries-and-search-conditions.md)
 
## <a name="manage-non-custodial-holds"></a>管理非保管保留

创建保留时，您有以下选项来限定在指定内容位置中保留的内容的范围：

  - 创建无限保留，其中所有内容都置于保留状态。 或者，您可以创建基于查询的保留，其中仅将与搜索查询匹配的内容置于保留状态。
  - 您可以指定日期范围，以仅保存该日期范围内发送、接收或创建的内容。 或者，您可以保留所有内容，而不管内容是何时发送、接收或创建。

要为高级电子数据展示案例创建保留：

1. 在**安全&合规中心**中，**单击"电子数据>高级电子数据展示"** 以显示组织中的案件列表。
  
2. 单击要创建保留的案例**旁边的"打开"。**
  
3. 在案例的主页中，**单击"保留"** 选项卡。
  
4. 在"**保留"** 选项卡上，**单击"创建"。**
  
5. 在"**您的保留"** 页上，为保留提供名称。 保留的名称在您的组织中必须是唯一的。
 
6. （可选）在"**说明"** 框中，添加保留的说明。
  
7. 按 [下一步]****。
  
8. 选择要置于保留状态的内容位置。 您可以将邮箱、站点和公用文件夹置于保留状态。

   a. **交换电子邮件**-**单击"选择用户、组或团队"，** 然后再次**单击"选择用户、组或团队"** 以指定要置于保留状态的邮箱。 使用搜索框查找用户邮箱和通讯组（对组成员的邮箱进行保留）以置于保留状态。 您还可以在 Office 365 组或 Microsoft 团队的关联邮箱上放置保留。 选择用户、组、团队复选框，**单击"选择"，** 然后单击"**完成"。**
 
    > [!NOTE]
    > 单击"**选择用户、组或团队**以指定要置于保留状态的邮箱"时，显示的邮箱选取器为空。 這項設計的目的是提升效能。 要将人员添加到此列表，在搜索框中键入名称（至少 3 个字符）。

    b. **SharePoint 网站**-**单击"选择网站"，** 然后再次**单击"选择网站"** 以指定"共享点"和"一个业务网站"以置于保留状态。 键入要保留的每个网站的 URL。 您还可以为 Office 365 组或 Microsoft 团队添加 SharePoint 网站的 URL。 **单击"选择"，** 然后单击"**完成"。**
    
     有关将 Office 365 组和 Microsoft 团队置于保留状态的提示，请参阅**常见问题解答**部分。

    > [!NOTE]
    > 在极少数情况下，某人的用户主体名称 （UPN） 已更改，其 OneDrive 帐户的 URL 也将更改以合并新的 UPN。 如果发生这种情况，您必须通过添加用户的新 OneDrive URL 并删除旧 URL 来修改保留。

     c. **交换公用文件夹**- 将切换开关移到"全部"位置，以将 Exchange Online 组织中的所有公用文件夹置于保留状态。 请注意，您无法选择要置于保留状态的特定公用文件夹。 如果不想对公用文件夹进行保留，请将切换开关**设置为"无"。**

9. 将内容位置添加到保留状态后，单击"**下一步"。**
  
10. 要创建具有条件的基于查询的保留，请完成以下操作。 否则，只需单击"**下一步"。**
    
    - **在"关键字"** 下的框中键入搜索查询，以便仅将满足搜索条件的内容置于保留状态。 您可以指定关键字、消息属性或文档属性（如文件名）。 您还可以使用使用布尔运算符的更复杂的查询，例如 AND、OR 或 NOT。 如果关键字框为空，则位于指定内容位置的所有内容都将置于保留状态。

    - **单击"添加**条件"以添加一个或多个条件以缩小保留的搜索查询范围。 每个条件都会向创建保留时创建和运行的 KQL 搜索查询添加一个子句。 例如，您可以指定日期范围，以便在日期范围内创建的电子邮件或网站文档置于保留状态。 條件會以 AND 運算子的邏輯方式連接至關鍵字查詢 (在關鍵字方塊中指定)。 这意味着项必须满足关键字查询和要置于保留的条件。

     有关创建搜索查询和使用条件的详细信息，请参阅[关键字查询和内容搜索的搜索条件。](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions)

12. 配置基于查询的保留后，**单击"下一步"。**
 
13. 查看您的设置，**然后单击"创建此保留"。**


## <a name="view-hold-statistics"></a>查看保留统计信息

一段时间后，有关新保留的信息将显示在所选保留**的"保留"** 选项卡上的详细信息窗格中。 此信息包括处于保留状态的邮箱和网站的数量以及有关置于保留中的内容的统计信息，例如置于保留状态的项目的总数和大小以及上次计算保留统计信息的时间。 这些保留统计信息可帮助您确定持有与电子数据展示案例相关的内容量。

请记住以下有关保留统计信息的事项：

- 保留的项目总数指示置于保留状态的所有内容源中的项数。 如果已创建基于查询的保留，则此统计信息将指示与查询匹配的项数。
  
- 保留的项目数还包括在内容位置中找到的未编制索引的项目。 请注意，如果创建基于查询的保留，则内容位置中的所有未编制索引的项目都将置于保留状态。 这包括不符合基于查询的保留的搜索条件的未编制索引项，以及可能超出日期范围条件的未编制索引项。 这与运行内容搜索时的情况不同，在内容搜索中，搜索结果中不包含与搜索查询不匹配或被日期范围条件排除的未编制索引的项目。 有关未编制索引的项目的详细信息，请参阅[Office 365 中内容搜索中部分索引的项目。](partially-indexed-items-in-content-search.md) 

- 您可以通过单击"更新统计信息"来重新运行计算当前保留项目数的搜索估计值，从而获取最新的保留统计信息。

- 如有必要，单击工具栏中的"刷新"以更新详细信息窗格中的保留统计信息。

- 保留项目的数量随时间而增加是正常的，因为邮箱或站点处于保留状态的用户通常会发送或接收新的电子邮件，并创建新的 SharePoint 和 OneDrive 业务文档。

- 如果将 SharePoint 站点或 OneDrive 帐户移动到多地理位置环境中的不同区域，则该站点的统计信息将不会包含在保留统计信息中。 但是，网站中的内容仍将处于保留状态。 此外，如果将网站移动到其他区域，则保留中显示的 URL 将不会更新。 您必须编辑保留并更新 URL。

## <a name="frequently-asked-questions"></a>常見問題集

- **如何将其他 Office 365 组或 Microsoft 团队网站映射到保管人？那么，在 Office 365 组和 Microsoft 团队上放置非托管保留怎么样？** 微软团队基于 Office 365 组构建。 因此，在电子数据展示案例中将其置于保留状态是非常类似的。 将 Office 365 组和 Microsoft 团队置于保留状态时，请记住以下事项。
  - 要将位于 Office 365 组和 Microsoft Teams 中的内容置于保留状态，必须指定与组或团队关联的邮箱和 SharePoint 网站。
  
  - 在联机交换中运行**Get-Unified 组**cmdlet 以查看 Office 365 组或 Microsoft 团队的属性。 这是获取与 Office 365 组或 Microsoft 团队关联的网站的 URL 的好方法。 例如，以下命令显示名为高级领导团队的 Office 365 组选定的属性：


    ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
    DisplayName            : Senior Leadership Team
    Alias                  : seniorleadershipteam
    PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
    SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > 要运行 Get-UnifiedGroup cmdlet，您必须在 Exchange 联机中分配仅查看收件人角色，或者成为分配了"仅查看收件人"角色的角色组的成员。

 - 搜索用户的邮箱时，不会搜索用户是其成员的任何 Office 365 组或 Microsoft Team。 同样，当您放置 Office 365 组或 Microsoft Team 保留时，只有组邮箱和组站点处于保留状态;否则，将保留组邮箱和组网站。除非明确将它们添加为保管人或将其数据源保留，否则组成员的业务网站的邮箱和 OneDrive 不会置于保留状态。 因此，如果您需要将 Office 365 组或 Microsoft Team 置于特定保管人的位置，请考虑将组站点和组邮箱映射到保管人（请参阅高级电子数据展示中的管理保管人）。 如果 Office 365 组或 Microsoft 团队不能归于单个保管人，请考虑将源添加到非托管保留中。 
 
 - 要获取 Office 365 组或 Microsoft 团队成员的列表，可以在 Microsoft 365 管理中心的"主页>组"页上查看属性。 或者，您可以在 Exchange 在线电源外壳中运行以下命令：

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > 要运行**Get-UnifiedGroupLinks** cmdlet，您必须在 Exchange 联机中分配仅查看收件人角色，或者成为分配了"仅查看收件人"角色的角色组的成员。

- 属于 Microsoft Teams 频道的渠道对话存储在与团队关联的邮箱中。 同样，团队成员在通道中共享的文件存储在团队的 SharePoint 网站上。 因此，您必须将 Microsoft Team 邮箱和 SharePoint 网站置于保留状态，才能在通道中保留对话和文件。
  
- 或者，作为 Microsoft Teams 中聊天列表一部分的对话存储在参与聊天的用户的邮箱中。  用户在聊天对话中共享的文件存储在共享该文件的用户的 OneDrive 业务网站中。 因此，您必须将单个用户邮箱和一个业务网站的 OneDrive 置于保留状态，才能在"聊天"列表中保留对话和文件。 
  
- 每个 Microsoft 团队或团队渠道都包含一个用于记笔记和协作的 Wiki。 Wiki 内容会自动保存到具有 .mht 格式的文件。 此文件存储在团队 SharePoint 网站上的团队 Wiki 数据文档库中。 通过将团队的 SharePoint 网站置于保留状态，可以将 Wiki 中的内容置于保留状态。

  > [!NOTE]
  > 2017 年 6 月 22 日发布了为 Microsoft 团队或团队渠道保留 Wiki 内容的功能（当您将团队的 SharePoint 网站置于保留状态时）。 如果团队网站处于保留状态，则从该日期开始将保留 Wiki 内容。 但是，如果团队网站处于保留状态，并且 Wiki 内容在 2017 年 6 月 22 日之前被删除，则 Wiki 内容不会保留。
