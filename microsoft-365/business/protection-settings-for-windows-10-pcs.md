---
title: 設定適用於 Windows 10 電腦的裝置保護設定
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
ms.assetid: bd66c26c-73a4-45a8-8642-3ea4ee7cd89d
description: 了解預設和其他 Microsoft 365 商務版來保護 Windows 10 裝置中可用的設定。
ms.openlocfilehash: 5d4bce02df1276dc9b284c7b0709c7dc26b0dbce
ms.sourcegitcommit: 8ca97fa879ae4ea44468be629d6c32b429efeeec
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/16/2019
ms.locfileid: "38676041"
---
# <a name="set-device-protection-settings-for-windows-10-pcs"></a>設定適用於 Windows 10 電腦的裝置保護設定

## <a name="secure-windows-10-devices"></a>保護 Windows 10 裝置

觀看如何使用 Microsoft 365 商務版 來保護 Windows 10 裝置的影片：
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/a5734146-620a-4cec-8618-536b3ca37972?autoplay=false]
  
1. 移至位於 <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> 的系統管理中心。 
    
2. 在左側導覽中，選擇 [**裝置** \> **原則** \> **新增**。
  
3. 在 [**新增原則**] 窗格中，輸入此原則的唯一名稱。 
    
4. [**原則類型**] 下選擇 [ **Windows 10 裝置設定**]。
    
5. 依序展開 [**保護 Windows 10 裝置**\>設定您想要的設定。 See [Available settings](#available-settings) for more information. 
    
    您隨時可以使用 [**重設預設設定**] 連結回復到預設設定。 
    
    ![Add policy pane with Windows 10 Device configuration selected](media/fa9e2dc2-7eae-4c96-af34-765a1f641ecf.png)
  
6. 下一步] 決定**人員會收到這些設定？** 如果您不想要使用預設**的所有使用者**安全性群組，選擇**變更**] 中，搜尋人員會收到這些設定的 [安全性] 群組\>**選取**。
    
7. 最後，選擇 [**完成**] 以儲存原則，並將它指派到裝置。 
    
## <a name="available-settings"></a>可用的設定

預設所有設定都是**上**。 下列為可用的設定。
  
如需詳細資訊，請參閱 [Microsoft 365 商務版中的保護功能如何對應 Intune 設定](map-protection-features-to-intune-settings.md)。 
  
|||
|:-----|:-----|
|設定  <br/> |描述  <br/> |
|使用 Windows Defender 防毒軟體來協助保護電腦免於遭受病毒與其他威脅的侵害  <br/> |需要開啟 Windows Defender 防毒軟體，以保護電腦免於遭受連接至網際網路時的安全威脅。  <br/> |
|協助保護電腦免於遭受 Microsoft Edge 中的網路安全威脅  <br/> |開啟 Microsoft Edge 中的設定，以協助保護使用者免受惡意網站與下載檔案的威脅。  <br/> |
|使用能減少裝置受攻擊面的規則  <br/> |設定為 [開啟] 時，受攻擊面縮減能協助系統封鎖惡意程式碼通常會用來感染裝置的動作和 App。只有在 Windows Defender 防毒軟體設為 [開啟] 時，這項設定才能夠使用。請參閱[縮減受攻擊面](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/exploit-protection)以深入了解。  <br/> |
|保護資料夾來抵擋勒索軟體等威脅  <br/> |這項設定使用受控資料夾存取權來保護公司資料，不讓可疑或惡意的 App 修改。 系統會封鎖這類型的 App，不讓它們變更受保護資料夾中的資料。 只有在 Windows Defender 防毒軟體設為 [開啟] 時，這項設定才能夠使用。 請參閱[使用受控資料夾存取權來保護資料夾](https://docs.microsoft.com/configmgr/protect/deploy-use/create-deploy-exploit-guard-policy#bkmk_CFA)來了解更多。  <br/> |
|避免連線到網際網路上可能有惡意之內容的網路存取行為  <br/> |請使用這項設定來封鎖前往聲譽不佳之網際網路位置 (可能裝載了網路釣魚詐騙郵件、惡意探索或其他惡意內容) 的連外使用者連線。只有在 Windows Defender 防毒軟體設為 [開啟] 時，這項設定才能夠使用。請參閱[保護您的網路](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-real-time-protection-windows-defender-antivirus)以深入了解。  <br/> |
|利用 BitLocker 來協助您保護電腦上的檔案和資料夾，抵擋未經授權的存取行為  <br/> |Bitlocker 能為電腦硬碟加密來保護資料，以及在電腦遺失或遭竊時保護資料來避免資料外洩。如需詳細資訊，請參閱 [Bitlocker 常見問題集](https://go.microsoft.com/fwlink/?linkid=871000)。  <br/> |
|允許使用者從 Microsoft Store 下載 App  <br/> |讓使用者從 Microsoft Store 下載並安裝 App。 應用程式包括所有項目從遊戲生產力工具]，讓我們保留**上**，此設定，但您可以將它關閉額外的安全性。  <br/> |
|允許使用者存取 Cortana  <br/> |Cortana 非常實用！ 她可以開啟設定或關閉您，提供指示，並請確定您已在約會現場，因此我們將此**上**預設。  <br/> |
|允許使用者接收來自 Microsoft 的 Windows 祕訣和廣告  <br/> |Windows 祕訣相當實用，並且能在新功能推出時引導使用者。  <br/> |
|自動讓 Windows 10 裝置保持在最新狀態  <br/> |確保 Windows 10 裝置能自動收到最新的更新。  <br/> |
|閒置這段時間之後關閉裝置螢幕  <br/> |確保使用者閒置時，公司資料已受到保護。使用者可能會在咖啡館等公共場所工作，當使用者暫時離開或是分心時，他們的裝置就容易受到他人任意窺伺。此設定能讓您控制螢幕將於使用者閒置多久之後關閉。  <br/> |
   
  

