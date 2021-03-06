---
title: 在 Microsoft 威脅防護中處理假像的誤報或漏報
description: 在 Microsoft 威脅防護中，AIR 是否已錯過或錯誤地偵測到什麼？ 瞭解如何將誤報或錯誤否定提交給 Microsoft 進行分析。
keywords: 自動化，調查，警示，觸發器，動作，修正，誤報，誤報，false 負數
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.date: 01/29/2020
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: 90651aa258adb9f7fe46f99bcadf1d4d552a5b76
ms.sourcegitcommit: 58c1b4208a5e231463091573e40696d08fc39b8e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/25/2020
ms.locfileid: "42955658"
---
# <a name="handle-false-positivesnegatives-in-automated-investigation-and-response-capabilities"></a>在自動化調查和回應功能中處理誤報/負片

適用於：****
- Microsoft 威脅防護

Microsoft 威脅防護中的[自動化調查和回應功能](mtp-autoir.md)是否遺漏或錯誤地偵測到某項內容？ 您可以採取一些步驟加以修正。 您可以：

- [向 Microsoft 報告誤報/負數](#report-a-false-positivenegative-to-microsoft-for-analysis)

- [調整提醒](#adjust-an-alert-to-prevent-false-positives-from-recurring)（如有需要）;和 

- [復原對裝置採取的修正動作](#undo-a-remediation-action-that-was-taken-on-a-device)。 

使用本文做為指南。 

## <a name="report-a-false-positivenegative-to-microsoft-for-analysis"></a>將誤報報告給 Microsoft 進行分析

|偵測到未接或誤接專案 |服務  |處理方式  |
|---------|---------|---------|
|-電子郵件 <br/>-電子郵件附件 <br/>-電子郵件訊息中的 URL<br/>-Office 檔案中的 URL      |[Office 365 進階威脅防護](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)        |[將可疑的垃圾郵件、網路釣魚、URLs 和檔案提交至 Microsoft for Office 365 掃描](https://docs.microsoft.com/microsoft-365/security/office-365-security/admin-submission)         |
|裝置上的檔或應用程式    |[Windows Defender 進階威脅防護](https://docs.microsoft.com/windows/security/threat-protection)         |[將檔案提交給 Microsoft 以進行惡意程式碼分析](https://www.microsoft.com/wdsi/filesubmission)         |

## <a name="adjust-an-alert-to-prevent-false-positives-from-recurring"></a>調整提醒以避免定期誤報

|案例 |服務 |處理方式 |
|--------|--------|--------|
|-由合法使用所觸發的警示 <br/>-警示不准確    |[Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)<br/> 或 <br/>[Azure 高級威脅偵測](https://docs.microsoft.com/azure/security/fundamentals/threat-detection)         |[在雲端應用程式安全性入口網站中管理提醒](https://docs.microsoft.com/cloud-app-security/managing-alerts)         |
|檔案、IP 位址、URL 或網域在裝置上視為惡意程式碼，即使它是安全的|[Windows Defender 進階威脅防護](https://docs.microsoft.com/windows/security/threat-protection) |[使用 "Allow" 動作建立自訂指示器](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators) |


## <a name="undo-a-remediation-action-that-was-taken-on-a-device"></a>復原裝置上所執行的修復動作

如果在裝置（例如 Windows 10 裝置）上採取修正動作，且該專案實際上不是威脅，您的安全性作業小組可以復原[動作中心](mtp-action-center.md)的修復動作。

> [!IMPORTANT]
> 在嘗試執行下列工作之前，請先確定您具備[必要的許可權](mtp-action-center.md#required-permissions-for-action-center-tasks)。

1. 移至 [https://security.microsoft.com](https://security.microsoft.com) 並登入。 

2. 在功能窗格中，選擇 [控制中心]****。 

3. 在 [**記錄**] 索引標籤上，選取您要復原的動作。 這會開啟快顯視窗。<br/>
    > [!TIP]
    > 使用篩選器縮小結果清單。 

4. 在選取專案的浮出控制項中，選取 [**開啟調查] 頁面**。

5. 在 [調查詳細資料] 視圖中，選取 [**動作**] 索引標籤。

6. 選取狀態為 [**已完成**] 的專案，然後在 [**決策**] 欄中尋找連結（如「**已核准**」）。 這會開啟快顯視窗，包含動作的詳細資料。

7. 若要復原動作，請選取 [**刪除修正**]。

## <a name="related-articles"></a>相關文章

- [與自動化調查及回應相關的核准或拒絕動作](mtp-autoir-actions.md)

- [深入了解重要訊息中心](mtp-action-center.md)

- [使用 Microsoft 威脅防護中的進階搜捕功能主動尋找威脅](advanced-hunting-overview.md)
