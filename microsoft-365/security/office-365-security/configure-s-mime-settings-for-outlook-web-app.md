---
title: 在 Exchange Online 中設定 Outlook 網頁版的 S/MIME 設定
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: 簡要描述 Exchange Online 系統管理員需要執行哪些動作才能在 Exchange Online 的 Outlook 網頁版中查看和設定 S/MIME 設定。
ms.openlocfilehash: 354b247c2b0e0e610e6cb0626f4a404b582db717
ms.sourcegitcommit: c2a36b16e354e20db5fd6275175ca856eae55bfc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2020
ms.locfileid: "41960319"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a>在 Exchange Online 中設定 Outlook 網頁版的 S/MIME 設定

如果您是 Exchange Online 的系統管理員，您可以設定 Outlook 網頁版（先前稱為 Outlook Web App），允許傳送和接收 S/MIME 保護的郵件。 在 Exchange Online PowerShell 中使用 **SmimeConfig** 和 **SmimeConfig** Cmdlet 來查看及管理這個功能。 若要連線至 Exchange Online PowerShell，請參閱[連線至 Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)。

如需詳細的語法及參數資訊，請參閱 [Get-SmimeConfig](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/get-smimeconfig) 和 [Set-SmimeConfig](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/set-smimeconfig)。

## <a name="considerations-for-new-microsoft-edge-chromium-based"></a>新的 Microsoft Edge （Chromium 型） 的考量

若要在新的[Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge) web 瀏覽器中網頁型 Outlook 中使用 S/MIME，您 （或另一個系統管理員） 必須設定，然後設定名為**ExtensionInstallForcelist**在新的 Microsoft Edge 中安裝 Microsoft S/MIME 分機的 Microsoft Edge 瀏覽器原則。 原則值為 `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`。 並請注意，將套用此原則需要加入網域的電腦，因此有效率地在新的 Microsoft Edge 瀏覽器中使用 S/MIME 需要加入網域的電腦。

如需詳細的 **ExtensionInstallForcelist** 原則的資訊，請參閱 [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)。

此步驟是使用新的 Microsoft Edge 中; 的先決條件它不會取代由使用者安裝 S/MIME 控制項。 在初次使用 S/MIME 時，系統會提示使用者下載並安裝 Outlook 網頁版中的 S/MIME 控制。 或者，使用者可以主動移至 Outlook 網頁版設定中的 **S/MIME**，取得控制的下載連結。

## <a name="considerations-for-chrome"></a>Chrome 使用者的考量

若要在 Google Chrome 網頁瀏覽器的 Outlook 網頁版中使用 S/MIME，您（或另一個系統管理員）必須設定名為 **ExtensionInstallForcelist** 的 Chromium 原則，以在 Chrome 中安裝 Microsoft S/MIME 擴充功能。 原則值為 `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`。 請注意，若要套用此原則，必須有加入網域的電腦，因此，要有效地在 Chrome 使用 S/MIME 必須有加入網域的電腦。

如需詳細的 **ExtensionInstallForcelist** 原則的資訊，請參閱 [ExtensionInstallForcelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallForcelist)。

此步驟是使用 Chrome 的先決條件；它不會取代由使用者安裝的 S/MIME 控制。 在初次使用 S/MIME 時，系統會提示使用者下載並安裝 Outlook 網頁版中的 S/MIME 控制。 或者，使用者可以主動移至 Outlook 網頁版設定中的 **S/MIME**，取得控制的下載連結。

## <a name="for-more-information"></a>如需詳細資訊

[可用於訊息簽署和加密的 S/MIME](s-mime-for-message-signing-and-encryption.md)
