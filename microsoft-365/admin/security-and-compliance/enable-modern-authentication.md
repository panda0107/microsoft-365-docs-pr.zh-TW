---
title: 為 Windows 裝置上的 Office 2013 啟用新式驗證
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 7dc1c01a-090f-4971-9677-f1b192d6c910
description: 了解如何設定登錄機碼，以啟用新式驗證已安裝的 Microsoft Office 2013 的裝置。
ms.openlocfilehash: f1264affa5be93b19e564a0edea00bfb78f452f1
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/24/2020
ms.locfileid: "42240311"
---
# <a name="enable-modern-authentication-for-office-2013-on-windows-devices"></a>為 Windows 裝置上的 Office 2013 啟用新式驗證

若要為已安裝 Office 2013 的任何 Windows 裝置啟用新式驗證，您必須先設定專用登錄機碼。
  
## <a name="enable-modern-authentication-for-office-2013-clients"></a>為 Office 2013 用戶端啟用新式驗證

> [!NOTE]
> Office 2016 用戶端已啟用新式驗證，您無需為 Office 2016 設定登錄機碼。 
  
若要針對已安裝 Microsoft Office 2013、且執行 Windows 的任何裝置啟用新式驗證 (比如膝上型電腦和平板電腦)，您必須先設定下列登錄機碼。您必須在每部要啟用新式驗證的裝置上設定機碼：
  
|**登錄機碼**|**類型**|**Value** |
|:-------|:------:|--------:|
|HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL  |REG_DWORD  |1  |
|HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\Version |REG_DWORD |1 |
   
登錄機碼設定完成後，您即可設定 Office 2013 裝置 App 為 Office 365 搭配使用[多重要素驗證 (MFA)](set-up-multi-factor-authentication.md)。 
  
如果您目前使用任何用戶端 App 登入，您就必須在登出後再次登入，變更才會生效。否則，在 ADAL 識別建立之前，您將無法使用 MRU 和漫遊設定。
  
## <a name="disable-modern-authentication-on-devices"></a>停用裝置上的新式驗證

若要停用裝置上的新式驗證，請在裝置上設定下列登錄機碼：
  
|**登錄機碼**|**類型**|**Value**|
|:-------|:------:|--------:|
|HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL |REG_DWORD|0|
   
## <a name="related-articles"></a>相關文章
[使用第二種驗證方式登入 Office 2013](https://support.office.com/article/2b856342-170a-438e-9a4f-3c092394d3cb.aspx)

  

