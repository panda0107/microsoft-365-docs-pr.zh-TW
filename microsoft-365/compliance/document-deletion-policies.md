---
title: 文件刪除原則概觀
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: 基於規範、法律或其他商業需求，您的組織可能需要將文件保留一段時間。 但如果您的組織保留文件的時間過久，則會產生不必要的法律風險。 使用文件刪除原則，您可以在一段特定時間後，透過刪除網站上的文件以積極降低風險 - 例如，您可以在文件建立五年之後，在使用者的商務用 OneDrive 網站上刪除文件。
ms.openlocfilehash: 60bf7808daad3eaead99ef64ea24be0bcfd9be0e
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2020
ms.locfileid: "42075195"
---
# <a name="overview-of-document-deletion-policies"></a>文件刪除原則概觀

> [!IMPORTANT]
> 我們建議您使用在 Microsoft 365 合規性中心、Microsoft 365 安全性中心或 Office 365 安全性與合規性中心中建立的保留原則或標籤，而不是使用文件刪除原則。 文件刪除原則會繼續與保留原則並行，但是如果您需要保留或刪除 Office 365 中任何地方的內容，我們建議您使用保留原則。 如需詳細資訊，請參閱[使用保留原則，而不是這些功能](retention-policies.md#use-a-retention-policy-instead-of-these-features)。
  
基於規範、法律或其他商業需求，您的組織可能需要將文件保留一段時間。 但如果您的組織保留文件的時間過久，則會產生不必要的法律風險。 使用文件刪除原則，您可以在一段特定時間後，透過刪除網站上的文件以積極降低風險 - 例如，您可以在文件建立五年之後，在使用者的商務用 OneDrive 網站上刪除文件。
  
文件刪除原則兼具功能性和彈性 - 例如，您可以：
  
- 讓站台擁有者選擇您集中建立和管理的原則。您也可讓站台擁有者在認為原則不適用於其內容時，選擇完全不採用。
    
- 對站台集合中的所有站台 (例如所有 OneDrive for Business 站台) 施行單一強制原則，甚或對建立自特定站台集合範本 (例如「小組站台」範本) 的所有站台集合施行原則。
    
- 提供具有預設規則、無須站台擁有者執行任何動作即會自動套用的預設原則。
    
- 建立有數個刪除規則可供站台擁有者選擇的原則。
    
您可以使用「文件刪除原則中心」建立和管理文件刪除原則。 或者，您可以[建立網站集合](https://go.microsoft.com/fwlink/p/?LinkID=404342)，並在 [企業]**** 索引標籤上選擇 [合規性原則中心]****，以手動方式建立原則中心。每個租用戶只能有一個「文件刪除原則中心」。 
  
![文件刪除原則中心的首頁](../media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a>文件刪除原則的使用時機

除了文件刪除原則以外，Office 365 還為站台內容提供下列保留原則：
  
- [記錄管理](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [內容類型、清單和文件庫的資訊管理原則](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [網站原則](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
每個類型的站台或資料都有其最適用的原則類型。舉例來說，您的組織可能會有使用內容類型的高度結構化站台，例如用於合約的財務站台，或文章的知識庫等。在此情況下，您即可使用內容類型原則。或者，您的組織可能需要保留法律文件，在此情況下，您可以使用內容類型和記錄中心來實作檔案規劃。
  
文件刪除原則不應取代記錄管理或資訊管理原則，因為這些都是最適用於結構化資料和內容類型的功能。 正確來說，您應在需要概括管理非結構化資料 (例如 OneDrive for Business 站台和小組站台) 的自動刪除時，使用文件刪除原則。
  
![顯示網站內容保留選項的圖表](../media/IP-Retention-policies-for-site-content.png)
  
如果您將文件刪除原則套用至已對清單或文件庫使用內容類型原則或資訊管理原則的站台，這些原則將會被忽略，而文件刪除原則會有效用。 這表示，您在規劃站台時應僅使用適用於結構化或非結構化內容的原則，而非同時使用兩種原則。 如需有關文件刪除原則會如何覆寫其他原則的詳細資訊，請參閱[套用或移除網站的文件刪除原則](apply-or-remove-a-document-deletion-policy-for-a-site.md)。
  
不同於其他原則，文件刪除原則只對文件庫有效用，對清單則否。
  
## <a name="deletion-policies-and-rules"></a>刪除原則和規則

文件刪除原則包含一或多個刪除規則，分別指定：
  
- 刪除之前的期間。
    
- 是否要從文件的建立時間或前次修改時間計算刪除日期。
    
- 要永久刪除文件，還是放置到資源回收筒。
    
如果原則包含多個規則，站台擁有者可以從中選取最適用於其內容的規則。
  
![新增刪除規則頁面](../media/IP-New-deletion-rule.png)
  
## <a name="policies-and-assignments"></a>原則和指派

建立文件刪除原則後，您可以將其指派至網站集合範本；例如，您可以將原則指派至商務用 OneDrive 範本，使其包含每個使用者的 OneDrive 網站。 當您將原則指派至站台集合範本時，該範本不僅會套用至往後任何從該範本建立的站台集合，也會套用至已從該範本建立的所有站台集合。
  
![選擇範本頁面，顯示 OneDrive 選項](../media/IP-Choose-a-template.png)
  
您也可以將原則指派至特定站台集合 — 這會覆寫任何已指派至該站台集合範本的原則。例如，您可以將原則指派至「小組站台」範本，但接著將不同的原則集套用至建立自該範本的特定站台集合，而覆寫該原則。
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a>選擇一個強制原則或數個原則

在指派原則時，您可以選擇將其設為強制原則，而使其成為唯一可供指派的原則，且將會套用至站台集合中的所有站台。站台擁有者無法選擇不採用強制原則，也就是說，站台中的文件無論如何都會受到刪除原則的管理。
  
除了設定單一強制原則以外，您也可以將數個原則指派至站台集合，這樣可讓每個站台擁有者能夠選擇要對其站台套用的原則，甚或選擇完全不採用。例如，您可以為一般商業文件建立一個原則，並且為具有不同保留排程的財務文件建立另一個原則。站台擁有者通常最清楚其站台包含哪些內容，因此也最了解應套用哪個文件刪除原則。每個站台只能套用一個原則。
  
### <a name="one-rule-or-several-rules-to-choose-from"></a>選擇一個規則或數個規則

一個原則可包含許多規則，例如，一般商業文件的刪除原則可能會有兩個規則：
  
- 根據法律義務或現行商業需求而不需要保留的文件，自建立後不應保留一年以上。
    
- 現行商業用途所需、且需使用一年以上的文件，自建立後不應保留三年以上。
    
站台擁有者可自行判定其站台包含一般商業文件，而選取此刪除原則，然後由此原則中選取適當的規則。 您只能從目前套用至站台的原則中選取規則 (而無法從任何原則中選取)，此規則將會套用至站台中的所有文件庫。
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a>站台集合、原則和規則的關係

基本關係如下：
  
對一個站台集合或站台集合範本可以指派一或多個原則，且其中每個原則都可以有一或多個規則。 但是，每個網站只能有一個作用中的原則，而對於網站中的文件庫，則只能有一個刪除原則可以隨時發生作用。
  
![顯示原則間關係的圖表](../media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a>繼承文件刪除原則

如同權限、瀏覽和許多其他站台功能，文件刪除原則是可繼承的。站台擁有者可為其站台選取文件刪除原則，並且讓子站台繼承父項的原則。子站台的擁有者可選取不同的原則和規則組合以解除繼承，而該原則將會套用至所有子站台，直到繼承再次解除為止。
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a>第一次指派文件刪除原則

請務必了解，文件刪除原則所指定的期限並不是從套用原則的日期算起，而是從建立文件或文件最後一次更新的時間算起。 例如，假設您建立了會在文件建立的兩年後永久加以刪除的文件刪除原則，然後將該原則指派給在四或五年前有數個站台集合從中建立的站台集合範本。 在此情況下，現有的網站集合中很可能包含許多存留期已超過兩年 (刪除原則所指定) 的文件，這表示，有許多內容在文件刪除原則第一次指派後不久即會被刪除。
  
如果您是初次指派原則，網站上所有文件皆會列入評估，符合標準的文件就會遭到刪除。此原則適用於所有現有文件，而不是只適用於指派原則後才建立的新文件。同時請切記，原則的期間是以各文件的存留期為準，而不是第一次指派原則的時間。
  
因此，在第一次指派站台的原則之前，您應先考量現有內容的存留期，以及原則對這些內容可能造成的影響。您也可以在指派新原則前先與站台擁有者溝通，讓他們有足夠的時間可評估可能的影響。
  
## <a name="time-lag-for-propagating-policies"></a>傳播原則的時間延遲

在您將原則指派至站台集合後，站台擁有者可以使用 **[站台設定]** 頁面上的 **[文件刪除原則]** 連結，來檢視及套用適用於站台的原則。 
  
只有在原則指派至網站集合後，才會出現 **[文件刪除原則]** 連結。 此外，此連結並不會在原則指派至站台後隨即出現 - 指派原則後至最可能要 24 小時，**[文件刪除原則]** 連結才會出現。 
  
## <a name="permissions"></a>權限

您的法規小組成員若要使用文件刪除原則中心，將必須同時取得原則中心和將要套用原則之站台集合的權限。我們建議您：
  
1. 建立包含所有文件刪除原則中心使用者的安全性群組 - 很可能是您的法規原則管理小組。 請參閱[管理啟用郵件功能的安全性群組](https://go.microsoft.com/fwlink/p/?LinkID=404345)。 
    
2. 在「文件刪除原則中心」中，將網站集合擁有者權限指派給安全性群組。 如需詳細資訊，請參閱[網站集合系統管理員的權限](https://go.microsoft.com/fwlink/p/?LinkID=404346)。 
    
3. 在每個需要指派文件刪除原則的站台集合中，將站台集合擁有者權限指派給安全性群組。
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a>文件刪除原則與保留原則的搭配運作方式

保留原則可確保所有內容皆能在特定的一段時間內保存，而文件刪除原則則可確保所有內容會在特定的一段時間後刪除。
  
如果您需要在固定的一段時間內保有文件，您可以將保留原則與刪除原則搭配使用。例如，您可以在文件修改後將其保留三年，然後設定會在文件前次修改的三年之後加以刪除的刪除原則。
  
請注意，刪除原則不可覆寫保留原則。如果站台處於保留狀態，而文件刪除原則刪除了某文件，該文件將會保存在文件保留庫中，如同文件是以手動方式刪除一般。
  
## <a name="see-also"></a>另請參閱

[套用或移除網站的文件刪除原則](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[建立文件刪除原則](create-a-document-deletion-policy.md)


