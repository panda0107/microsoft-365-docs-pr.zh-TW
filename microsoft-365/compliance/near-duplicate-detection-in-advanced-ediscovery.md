---
title: 近似重複項偵測
f1.keywords:
- NOCSH
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
ms.openlocfilehash: e1a9ffe264925911f475732ffd98a43fa533e458
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2020
ms.locfileid: "42071310"
---
# <a name="near-duplicate-detection"></a>近似重複項偵測

請考慮一組文件檢閱子集根據相同範本和具有大部分相同重複使用的語言，具有以下，有一些差異。 如果檢閱者無法識別此子集、 徹底，檢閱其中並檢閱其餘的差異，他們會不有未接唯一的任何資訊時採取的時間分數，可能需要花它們讀取封面至封面的所有文件。 接近重複資料偵測群組在一起，以協助您進行檢閱程序更有效率加 1 類似的文件。

## <a name="how-does-it-work"></a>它的運作方式為何？

執行接近重複資料偵測時，系統會剖析文字的所有文件。 然後，它會比較根據彼此判斷其相似性是否大於設定的臨界值的每個文件。 如果是的話，則文件，將群組在一起。 一旦所有文件有相較，且分組，每個群組的文件會標示為 「 中樞 」;檢閱您的文件，您可以先檢閱樞紐分析表，並檢閱在接近重複組相同的其他文件將重點放在樞紐分析表和檢閱中之文件之間的差異。
