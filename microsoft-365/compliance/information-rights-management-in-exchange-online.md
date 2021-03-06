---
title: 使用 AD RMS 的 Exchange Online 郵件加密
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/13/2017
audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2c956776-0016-4be6-b4cd-133a237f4a9e
description: 您可以設定 Exchange Online IRM 設定為使用內部部署 Active Directory 版權管理服務 (AD RMS)，如有需要以滿足您組織的需求。 這並不常見。 如果您沒有使用 AD RMS 的需求，請改為使用 Office 郵件加密。
ms.openlocfilehash: 24a86ad9b1a1f3bbd67e194143fa02cb4040a47e
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600650"
---
# <a name="exchange-online-mail-encryption-with-ad-rms"></a>使用 AD RMS 的 Exchange Online 郵件加密

為了防止資訊外洩，Exchange Online 包含資訊版權管理 (IRM) 功能，可針對電子郵件訊息和附件提供線上和離線保護。 您可以設定 Exchange Online IRM 設定為使用內部部署 Active Directory 版權管理服務 (AD RMS)，如有需要以滿足您組織的需求。 這並不常見。 如果您沒有使用 AD RMS 的需求，請改為使用[Office 365 郵件加密](ome.md)。 

可以由使用者在 Microsoft Outlook 或網頁型 Outlook 中套用 IRM 保護，它可以套用由系統管理員使用傳輸保護規則或 Outlook 保護規則。 IRM 可協助您和使用者控制能夠存取、轉寄、列印或複製電子郵件中之機密資料的人員。
  
## <a name="changes-to-how-irm-works-with-office-365-message-encryption-ome-and-azure-active-directory"></a>對 Office 365 郵件加密 (OME) 與 Azure Active Directory IRM 的運作方式

截至年 9 月 2017，當您設定新的 Office 365 郵件加密功能為您的組織，您也設定 IRM 與 Azure 版權管理 (Azure RMS) 搭配使用。 您無法再使用 Azure RMS 的 IRM 設定分別設定。 相反地，OME 和權限管理可以順暢地搭配使用。 如需有關的新功能的詳細資訊，請參閱[Office 365 郵件加密常見問題集](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e)。 如果您已準備好要開始使用您的組織內全新的 OME 功能，請參閱[設定以 Azure 資訊保護基礎所建置的全新 Office 365 郵件加密功能](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)。
  
## <a name="how-irm-works-with-exchange-online-and-active-directory-rights-management-services"></a>IRM 與 Exchange Online 和 Active Directory Rights Management Services 的運作方式

Exchange Online IRM 使用內部部署 Active Directory Rights Management Services (AD RMS)，在 Windows Server 2008 和更新版本的資訊保護技術。 系統會藉由將 AD RMS 權限原則範本套用至電子郵件，將 IRM 保護套用至電子郵件。 權限會附加到郵件本身，以便進行保護作業的線上及離線和內部和外部組織的防火牆。
  
使用者可以將範本套用至電子郵件來控制對郵件收件者擁有的權限。 透過將 AD RMS 權限原則套用至郵件，即可控制如轉寄、從郵件擷取資訊、儲存郵件或列印郵件等動作。
  
您可以設定 IRM 以使用 AD RMS 伺服器執行 Windows Server 2008 或更新版本。 您可以使用這個 AD RMS 伺服器來管理雲端架構組織的 AD RMS 權限原則範本。 Outlook 也會仰賴 AD RMS 伺服器，讓使用者將 IRM 保護套用至他們所傳送的郵件。 如需詳細資訊，請參閱[將 IRM 設定為使用內部部署 AD RMS 伺服器](configure-irm-to-use-an-on-premises-ad-rms-server.md)。 
  
啟用之後，您就可以依照下列方式，將 IRM 保護套用至郵件：
  
- **使用者可以手動套用的範本使用 Outlook 和 outlook 網頁版。** 使用者可以從 [**設定權限**] 清單中選取範本，以套用至電子郵件訊息 AD RMS 權限原則範本。 當使用者傳送受 IRM 保護的郵件時，使用受保護格式的任何附加檔案也會受到與郵件相同的 IRM 保護。 IRM 保護會套用至與 Word、Excel 和 PowerPoint 相關聯的檔案，以及 .xps 檔案和附加的電子郵件訊息。 
    
- **系統管理員可以使用傳輸保護規則，自動將 IRM 保護套用到 Outlook 和 outlook 網頁版。** 您可以建立傳輸保護規則，以 IRM 保護的郵件。 請設定傳輸保護規則動作，以便將 AD RMS 權限原則範本套用至符合規則條件的郵件。 啟用 IRM 之後，組織的 AD RMS 權限原則範本就可以搭配名為 **套用權限保護到具有下列條件的郵件**的傳輸保護規則動作使用。
    
- **管理員可以建立 Outlook 保護規則。** Outlook 保護規則會自動將 IRM 保護套用至郵件會根據條件包括寄件者的部門，使用者將郵件傳送到，在 Outlook 2010 (不在 web 上 Outlook) 中郵件和收件者位於內部或外部您組織。 如需詳細資訊，請參閱[Create an Outlook Protection Rule](https://technet.microsoft.com/library/da64750d-faaf-44de-ad8c-888eba7fbdbf.aspx)。
    

