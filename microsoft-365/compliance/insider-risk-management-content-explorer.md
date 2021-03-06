---
title: 測試人員風險管理內容總管
description: 了解 Microsoft 365 中的測試人員風險管理內容總管
keywords: Microsoft 365, 測試人員風險管理, 風險管理, 合規性
localization_priority: Normal
ms.prod: Microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: m365-security-compliance
ms.openlocfilehash: 68a472e4e6b7556fc1b738a49b3c82dcf4804842
ms.sourcegitcommit: 87cc278ea2ddcd536ecfaa3dfae9a5ddaa502cf9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2020
ms.locfileid: "42179074"
---
# <a name="insider-risk-management-content-explorer"></a>測試人員風險管理內容總管

風險分析師和現場，若要檢查的內容和擷取提醒中的通訊的詳細資訊，可讓測試人員風險管理內容的檔案總管。 所有警示，資料和郵件檔案的複本已封存為快照中的項目，同時維持原來的檔案及儲存來源中的郵件的時間。 資料和訊息複製為透明與警示相關聯的員工和內容的擁有者。 資料的存取權限與權限設定所複製的內容和訊息及風險分析師維護，而且現場需要這些權限和權限如果他們需要開啟並檢視的檔案。 每個檔案及郵件會自動指派管理用途測試人員風險管理案例中的唯一檔案識別碼。

## <a name="column-options"></a>資料行選項

若要讓風險分析師和現場檢閱所擷取的資料及訊息，以及檢閱的大小寫的內容更容易，數個篩選和排序工具隨附內容檔案總管中。 基本排序，[**日期**] 和 [**檔案類別**欄會支援排序使用佇列內容窗格中的資料行標題。 其他佇列欄是可供新增至檢視，以提供不同的樞紐分析表上的檔案和訊息。

若要新增或移除資料行標題的內容佇列，請使用**編輯欄位**控制項並從下列欄選項進行選取。 這些欄對應至常見，電子郵件，並屬性條件支援內容的檔案總管中，並列出在本主題稍後的文件。

| **資料行選項** | **描述** |
|:------------------|:----------------|
| **Author** | [作者] 欄位從 Office 文件，可保存如果複製文件。 例如，如果使用者建立文件和電子郵件至其他人然後將它上傳至 SharePoint 文件仍會保留原始作者。 |
| **Bcc** | 適用於電子郵件、 [密件副本郵件] 欄位中的使用者。 |
| **Cc** | 適用於電子郵件、 [副本] 的 [郵件] 欄位中的使用者。 |
| **複合路徑** | 描述項目的來源的人力可讀取路徑。 |
| **交談識別碼** | 從郵件的交談 Id。 |
| **交談的索引** | 從郵件的交談索引。 |
| **建立的時間** | 建立的檔案或電子郵件訊息的時間。 |
| **Date** | 電子郵件的日期已接收到收件者或寄件者所傳送。 對於文件，上次修改文件的日期。 |
| **主控項的佈景主題** | 主控項主題做為分析計算。 |
| **電子郵件設定識別碼** | 設定相同的電子郵件中的所有郵件的群組識別碼。 |
| **家庭識別碼** | 家庭識別碼分組的所有項目;電子郵件，這包括郵件，並將所有附件。對於文件，包括文件和任何內嵌的項目。 |
| **檔案類別** | 來自 SharePoint 和 OneDrive 的內容：**文件**;從 Exchange 內容: * * 電子郵件或**附件**。 |
| **檔案識別碼** | 文件內案例的唯一識別碼。 |
| **檔案類型的圖示** | 檔案; 的副檔名例如，docx、 一個、 pptx 或 xlsx。 這是做為 FileExtension 站台屬性相同的屬性。 |
| **識別碼** | 檔案的 GUID 識別碼。 |
| **固定 ID** | 為 Office 365 中儲存的固定識別碼。 |
| **內含類型** | 針對分析計算 （含） 的類型： **0** -不含;**1** -（含);**2** -內含減;**3** -（含） 的複本。 |
| **上次修改日期** | 上次變更文件的日期。 |
| **標示為代表性** | 從完全重複的每一組一份文件會標示為代表。 |
| **訊息類型** | 若要搜尋的電子郵件訊息的類型。 可能的值： 連絡人、 文件、 電子郵件、 外部資料、 傳真、 im、 日誌、 會議、 microsoft teams （傳回項目，從聊天、 會議及 Microsoft Teams 中的通話），備忘稿、 文章、 rssfeeds、 工作、 語音信箱 |
| **參與者** | 清單中的所有參與者的郵件。例如，寄件者、 To、 Cc [密件副本]。 |
| **樞紐分析表識別碼** | 樞紐分析表的識別碼。 |
| **收到日期** | 收件者收到電子郵件的日期。 這是做為接收電子郵件屬性相同的屬性。 |
| **收件者** | 電子郵件中的所有收件者欄位。 這些欄位是以 [副本] 及 [密件副本]。 |
| **具有代表性的識別碼** | 每一組完全重複的數值識別碼。 |
| **Sender** | 電子郵件的寄件者。 |
| **寄件者/作者** | 寄送郵件人員的電子郵件。 對於文件，在 Office 文件中的 [作者] 欄位中所引用的人員。 您可以輸入多個名稱，以逗號隔開。 OR 運算子會以邏輯方式連線兩個或多個值。 |
| **Sent** | 寄件者傳送電子郵件的日期。 這是做為已傳送電子郵件屬性相同的屬性。 |
| **大小** | 電子郵件與文件的大小 （以位元組為單位） 的項目。 |
| **Subject** | 電子郵件訊息的主旨行中的文字。 |
| **主旨/標題** | 電子郵件訊息的主旨行中的文字。 對於文件，文件的標題。 如先前所述，Title 屬性是 Microsoft Office 文件中指定的中繼資料。 您可以輸入多個主體/標題，以逗號隔開的名稱。 OR 運算子會以邏輯方式連線兩個或多個值。 |
| **佈景主題清單** | 計算中分析的佈景主題清單。 |
| **Title** | 文件的標題。 Title 屬性是在 Office 文件中指定的中繼資料。 它是不同於文件的檔案名稱。 |
| **To** | 電子郵件] 欄位中的收件者。 |

## <a name="advanced-search-conditions"></a>進階的搜尋條件

您可以新增搜尋條件縮小搜尋範圍，並傳回更精細的結果集。 每個條件會將一個子句新增至在啟動搜尋時便會建立並執行的搜尋查詢中。 條件是以邏輯方式連線到 （在 [關鍵字] 方塊中指定） 的關鍵字查詢邏輯運算子 （這當成 c:c） 都與 AND 運算子相似的功能。 這表示項目必須符合的關鍵字查詢和搜尋結果中包含的一或多個條件。 這是條件協助縮小搜尋結果的方式。

進階的篩選及搜尋工具，依序展開 [內容佇列左側的 [**篩選**] 窗格。 選取 [**新增條件**] 按鈕，開啟 [條件] 清單中：

### <a name="operators-used-with-conditions"></a>與條件搭配使用的運算子

|**Operator**|**查詢對等用法**|**描述**|
|:-----------|:-------------------|:--------------|
| **After** |`property>date`| 日期條件搭配使用。 傳回已傳送、 接收或修改所指定日期之後的項目。|
| **Before** |`property<date`| 日期條件搭配使用。 傳回已傳送、 接收或所指定日期之前修改的項目。|
| **之間** |`date..date`| 使用日期與大小條件。 日期條件搭配使用時，傳回的項目那里已傳送、 接收或修改指定的日期範圍內。 大小條件搭配使用時，傳回其大小是在指定範圍內的項目。|
| **包含所有的** |`(property:value) OR (property:value)`| 與指定的字串值的屬性的條件搭配使用。 會傳回包含所有的一或多個指定的字串值的項目。 |
| **包含任何** |`(property:value) OR (property:value)`| 與指定的字串值的屬性的條件搭配使用。 會傳回包含一或多個指定的字串任何的值部分的項目。|
| **不包含** |`-property:value`  <br/> `NOT property:value`| 與指定的字串值的屬性的條件搭配使用。 會傳回不含任何部分指定的字串值的項目。|
| **不等於任何** |`-property=value`  <br/> `NOT property=value`| 與指定的字串值的屬性的條件搭配使用。 會傳回不含特定字串的項目。|
| **等於** |`size=value`| 會傳回與指定大小相等的項目。<sup>1</sup>|
| **等於任何** |`(property=value) OR (property=value)`| 與指定的字串值的屬性的條件搭配使用。 會傳回一或多個指定的字串值完全相符的項目。|
| **等於任何** |`(property=value) OR (property=value)`| 與指定的字串值的屬性的條件搭配使用。 會傳回與一或多個指定的字串值不相符的項目。 |
| **大於** |`size>value`| 傳回指定的屬性大於指定值的項目。<sup>1</sup>|
| **大於或等於** |`size>=value`| 傳回的項目指定的屬性大於或等於指定值。<sup>1</sup>|
| **小於** |`size<value`| 會傳回大於或等於特定值的項目。<sup>1</sup>|
| **小於或等於** |`size<=value`| 會傳回大於或等於特定值的項目。<sup>1</sup>|
| **不等於** |`size<>value`| 會傳回不等於指定的大小的項目。<sup>1</sup>|

> [!NOTE]
> <sup>1</sup>此運算子是僅適用於使用 Size 屬性的條件。

### <a name="common-property-conditions"></a>常見屬性條件

| **條件選項** | **描述** |
|:---------------------|:----------------|
| **Date** | 電子郵件的日期已接收到收件者或寄件者所傳送。 對於文件，上次修改文件的日期。 |
| **寄件者/作者** | 寄送郵件人員的電子郵件。 對於文件，在 Office 文件中的 [作者] 欄位中所引用的人員。 您可以輸入多個名稱，以逗號隔開。 **OR**運算子會以邏輯方式連線兩個或多個值。 |
| **大小** | 電子郵件與文件的大小 （以位元組為單位） 的項目。 |
| **主旨/標題** | 電子郵件訊息的主旨行中的文字。 對於文件，文件的標題。 在文件中的 [標題] 屬性是 Microsoft Office 文件中指定的中繼資料。 您可以輸入多個主體/標題，以逗號隔開的名稱。 OR 運算子會以邏輯方式連線兩個或多個值。 |

### <a name="email-property-conditions"></a>電子郵件屬性的條件

下表列出的電子郵件訊息屬性條件提供內容的檔案總管]。

| **條件選項** | **描述** |
|:---------------------|:----------------|
| **Bcc** | 電子郵件的密件副本] 欄位。 |
| **Cc** | 電子郵件 [副本] 欄位。 |
| **電子郵件安全性** | 郵件的安全性設定。 |
| **電子郵件的敏感度** | 郵件的 [敏感度] 設定值。 |
| **電子郵件設定識別碼** | 設定相同的電子郵件中的所有郵件的群組識別碼。 |
| **寄件者** | 電子郵件的寄件者。 |
| **具有附件** | 會指出郵件是否具有附件。 使用值 **，則為 true**或**false**。 |
| **Importance** | 電子郵件，這會傳送郵件時，可以指定寄件者的重要性。 根據預設，郵件會傳送與普通重要性，除非寄件者設定為**高重要性**或**低**重要性。 |
| **會議結束日期** | 會議的會議結束日期。 |
| **會議開始日期** | 會議的會議開始日期。 |
| **訊息類型** | 若要搜尋的電子郵件訊息的類型。 可能的值： 連絡人、 文件、 電子郵件、 外部資料、 傳真、 im、 日誌、 會議、 microsoft teams （傳回項目，從聊天、 會議及 Microsoft Teams 中的通話），備忘稿、 文章、 rssfeeds、 工作、 語音信箱 |
| **參與者的網域** | 清單中的所有網域的郵件的參與者。 |
| **參與者** | 所有的人員欄位中的電子郵件訊息。 這些欄位為、 To、 [副本] 及 [密件副本]。 |
| **收到日期** | 收件者收到電子郵件的日期。 |
| **收件者網域** | 所有網域的郵件收件者的清單。 |
| **Sender** | 寄件者的郵件類型的欄位 （中）。  格式為**DisplayName \<SmtpAddress>**。 |
| **寄件者網域** | 寄件者的網域。 |
| **Subject** | 電子郵件訊息的主旨行中的文字。  <br/> **附註：** 當您在查詢中使用 Subject 屬性時，搜尋會傳回所有郵件的主旨行中包含您要搜尋的文字。 換句話說，查詢不會傳回已完全符合這些郵件。 例如，如果您搜尋`subject:"Quarterly Financials"`，您的結果會包含郵件主旨為 「 Quarterly Financials 2018 」。 |
| **To** | 電子郵件訊息的 [到] 欄位。 |
| **唯一的電子郵件設定** | 如果沒有重複的電子郵件並將其設定中的附件，則為 false。 |

## <a name="document-property-conditions"></a>文件屬性的條件

下表列出可用的文件屬性條件內容的檔案總管]。 許多條件會與共用這些屬性的檢閱[進階電子文件探索案例](document-metadata-fields-in-Advanced-eDiscovery.md)中包含的集合。

| **條件選項** | **描述** |
|:---------------------|:----------------|
| **設定律師-委託人權限分數** | 設定律師-委託人權限模型內容分數。 |
| **Author** | [作者] 欄位從 Office 文件，可保存如果複製文件。 例如，如果使用者建立文件和電子郵件至其他人然後將它上傳至 SharePoint 文件仍會保留原始作者。 |
| **合規性標籤** | 套用 Office 365 中的合規性標籤。 |
| **複合路徑** | 描述項目的來源的人力可讀取路徑。 |
| **交談識別碼** | 從郵件的交談 Id。 |
| **建立的時間** | 建立的檔案或電子郵件訊息的時間。 |
| **監管人** | Custodian 項目名稱已與相關聯。 |
| **主控項的佈景主題** | 主控項主題做為分析計算。 |
| **家庭識別碼** | 家庭識別碼分組的所有項目;電子郵件，這包括郵件，並將所有附件。對於文件，包括文件和任何內嵌的項目。 |
| **檔案類別** | 來自 SharePoint 和 OneDrive 的內容：**文件**;從 Exchange 內容: * * 電子郵件或**附件**。 |
| **檔案類型** | 檔案; 的副檔名例如，docx、 一個、 pptx 或 xlsx。 |
| **Attorney-client 位參與者** | 至少要有一個參與者在律師] 清單中，找到時，則為 true。否則，則值為 False。 |
| **固定 ID** | 為 Office 365 中儲存的固定識別碼。 |
| **內含類型** | 針對分析計算 （含） 的類型： **0** -不含;**1** -（含);**2** -內含減;**3** -（含） 的複本。 |
| **項目類別** | 由 exchange 伺服器; 所提供的項目類別例如， **IPM。附註** |
| **上次修改日期** | 上次變更文件的日期。 |
| **負載識別碼** | 載入的識別碼，此項目已載入檢閱設定。 |
| **位置名稱** | 識別項目的來源的字串。  對於 exchange，這是信箱的 SMTP 地址。 SharePoint 和 OneDrive 網站集合的 URL。 |
| **標示為代表性** | 從完全重複的每一組一份文件會標示為代表。 |
| **原生副檔名** | 項目的的原生擴充。 |
| **原生檔案名稱** | 原生檔案名稱的項目。 |
| **NdEtSortExclAttach** | 電子郵件設定和 ND 有效率排序在檢閱階段; 設定串連而成D 新增為前置詞 ND 設定和 E 新增至電子郵件設定。 |
| **樞紐分析表識別碼** | 樞紐分析表的識別碼。 |
| **可能特殊權限** | 設定律師-委託人權限偵測模型考量可能特殊權限的文件，其值為 true。 |
| **處理狀態** | 處理狀態之後的項目已新增至檢閱設定。 |
| **讀取百分位數** | 閱讀相關性為基礎的文件的百分位數。 |
| **相關性分數** | 相關性為基礎的文件的相關性分數。 |
| **相關性標記** | 相關性為基礎的文件的相關性分數。 |
| **具有代表性的識別碼** | 每一組完全重複的數值識別碼。 |
| **標記** | 在檢閱套用標記設定。 |
| **佈景主題清單** | 計算中分析的佈景主題清單。 |
| **Title** | 文件的標題。 Title 屬性是在 Office 文件中指定的中繼資料。 它是不同於文件的檔案名稱。 |
| **已修復** | 如果項目已修復，否則為 False，則為 true。 |
| **字數統計** | 在檔案中的字詞數目。 |
