---
title: 建立並使用範本來新增使用者
f1.keywords:
- NOCSH
ms.author: v-sharos
author: shars
manager: scotv
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
- MET150
- MOE150
description: 您可以建立及使用範本來節省時間和標準化的設定，當您新增多位使用者。
ms.openlocfilehash: 340d0ae3329b441c2b9773ba06e4f9e69be88526
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/02/2020
ms.locfileid: "42353244"
---
# <a name="create-and-use-a-template-to-add-users"></a>建立並使用範本來新增使用者

您可以建立及使用範本來節省時間和標準化的設定，當您要新增多個使用者。 範本會特別有用，如果您有共用許多常見屬性，如使用者有相同的角色，且在相同的位置和那些人員需要相同的軟體工作的使用者。 例如，您可能必須支援工程師合作相同的 office 中的小組。  

## <a name="create-a-template"></a>建立範本

範本很容易建立&mdash;您可以選取**使用者** > **作用中使用者** > **使用者範本**，然後選取 [**新增範本**，從下拉式清單] 清單中，或您可以新增新的使用者，當您完成時，您必須將項目儲存為範本的選項。

當您建立的範本新增使用者之後時，您選擇下列設定值會儲存在範本中：

- 網域名稱
- 密碼設定選擇： 您可以選擇建立密碼或已將其自動產生
- 單次密碼選擇： 您可以要求使用者在第一個登入之後建立新的密碼
- 授權位置
- 授權選項
- 應用程式選項
- 角色
- 大部分設定檔資訊，例如**工作的設定檔**、**部門**、 **Office**、**辦公室電話**，以及 **-路/街地址** 

下列資訊是特定使用者，並不會儲存在範本中：

- 名字和姓氏
- 辨別名稱 (DN)
- 使用者名稱
- 選擇要將密碼傳送電子郵件及由誰在密碼電子郵件傳送至
- 行動電話號碼

如果您選擇不要輸入資訊] 區段中的設定，這個值會是空白，該設定將不會顯示在範本中。 例如，如果空白**職稱**，檢閱您的範本時，並使用您的範本時，**工作標題**不會出現所有。 如果所有的**設定檔**] 區段中設定保留空白，[**設定檔**] 區段中會顯示**無提供**在最後一個範本中。

當您選取 [**新增範本**] 選項來建立範本時，您可以選擇要完成之值。 任何空白的項目會顯示為**沒有提供**範本中。

## <a name="use-a-template-to-add-a-user"></a>使用範本來新增使用者

若要使用現有的範本，將使用者新增：

1. 在系統管理中心中，選取 [**使用者** > **作用中的使用者**。

2. 選取 [**使用者範本**，然後從下拉式清單中選取範本。 （清單會包含只有範本所建立，不那些其他系統管理員所建立）。

 > [!NOTE]
 > 您也可以使用範本來新增使用者藉由選取**使用者範本** > **管理範本**] 下，選取範本，然後選取 [**使用範本**。

3. 請依照下列步驟來建立使用者從您所選的範本。

> [!NOTE]
> 如果您有不足，無法供您新增使用者的授權，而您的付款資訊，我們會嘗試購買其他授權，使用您現有的付款資訊。 如果您的付款資訊無法使用，使用者會被建立為未授權的使用者。

## <a name="manage-templates"></a>管理範本

您可以輕鬆地刪除您不再需要並加入新的範本。 若要刪除範本：

1. 在系統管理中心中，選取 [**使用者** > **作用中的使用者**。

2. 選取**範本**]，然後從下拉式清單中選取 [**管理範本**。

3. 會顯示範本的清單。 您可以刪除範本執行下列其中一項動作：
    - 選取一或多個範本，然後選取 [**刪除**。 
    - 選取三個點右邊的範本名稱，然後再選取 [**刪除**。
    - 選取 [範本名稱。 當畫面的右側顯示範本的詳細資訊時，請選取 [**刪除範本**]。

## <a name="related-articles"></a>相關文章

[個別或大量新增使用者至 Office 365](add-users.md)

[從 Office 365 中移除前任員工](remove-former-employee.md)
  
