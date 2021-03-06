---
title: 第1 階段：網路基礎結構的允出準則
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/23/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: 請確定您的設定符合 Microsoft 365 企業版的網路基礎結構的準則。
ms.openlocfilehash: 1ace68fd19c62e4dc389604c1b0c02ddc18b52dc
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/13/2020
ms.locfileid: "42633201"
---
# <a name="phase-1-networking-infrastructure-exit-criteria"></a>第1 階段：網路基礎結構的允出準則

![階段 1 - 網路](../media/deploy-foundation-infrastructure/networking_icon-small.png)

請確定您的網路基礎結構符合下列必要準則，而且您已將這些視為選擇性準則。

<a name="crit-networking-step1"></a>
## <a name="required-your-network-is-ready-for-microsoft-365-enterprise"></a>必要：Microsoft 365 企業版可以使用您的網路

- 您的辦公室有足夠的網際網路頻寬，可容納 Microsoft 365 流量，包括 Office 365、Microsoft Intune 以及 Windows 10 企業版安裝和更新。
- 您的整體網路對應至 [Office 365 參考架構](https://docs.microsoft.com/office365/enterprise/office-365-network-connectivity-principles#BKMK_P2)。
- 您的網路變更已經過試驗和測試，並符合您的流量延遲需求。

如有需要，[步驟 1](networking-provide-bandwidth-cloud-services.md) 可協助您符合這項要求。

<a name="crit-networking-step2"></a>
## <a name="required-your-local-offices-have-local-internet-connections-and-name-resolution"></a>必要：您的當地辦公室具備當地網際網路連線和名稱解析

您已設定每個當地辦公室可透過當地 ISP 存取網際網路，而 ISP 的 DNS 伺服器會使用當地公用 IP 位址來識別它們在網際網路上的位置。這可確保存取 Microsoft 365 雲端服務的使用者獲得最佳效能。

如果您的分公司不是使用當地 ISP，效能可能會變差，因為網路流量必須通過組織的骨幹，或是資料要求會交由遠處的前端伺服器處理。

### <a name="how-to-test"></a>如何測試
在辦公室內的裝置上使用工具或網站來判斷 Proxy 伺服器所使用的公用 IP 位址。例如，使用 [What Is My IP Address](https://www.whatismypublicip.com/) (我的 IP 位址是什麼) 網頁。此公用 IP 位址由 ISP 指派，應該是地理區域性的。不應該來自總公司公用 IP 位址範圍或雲端型網路安全性廠商。

如有需要，[步驟 2](networking-dns-resolution-same-location.md) 可協助您符合這項要求。

<a name="crit-networking-step3"></a>
## <a name="optional-unnecessary-network-hairpins-are-removed"></a>選用：已移除不需要的網路 Hairpin

您已檢查網路 Hairpin，並判斷出其對您的所有辦公室之效能的影響。您已移除可能的網路 Hairpin，或與協力廠商網路或安全性提供者合作，為其網路實作最佳化的 Microsoft 365 對等。

如有需要，[步驟 3](networking-avoid-network-hairpins.md) 可協助您使用此選項。


<a name="crit-networking-step4"></a>
## <a name="optional-you-have-configured-traffic-bypass-on-your-internet-browsers-and-edge-devices"></a>選用：已在您的網際網路瀏覽器和邊緣裝置上設定流量旁路

已將最新的 PAC 檔案部署至內部部署網際網路瀏覽器，以便送至 Microsoft 365 DNS 網域名稱的流量可以略過 Proxy 伺服器。

已設定您的網路周邊裝置 (例如防火牆、SSL 中斷和檢查，以及封包檢查裝置) 來使用流量旁路，或最低限度地處理送至 Microsoft 365 端點之最佳化和允許類別的流量。


### <a name="how-to-test"></a>如何測試

在網路周邊裝置上使用記錄工具，以確保送至 Microsoft 365 的流量沒有經過檢查、解密或其他形式妨礙。

如有需要，[步驟 4](networking-configure-proxies-firewalls.md) 可協助您使用此選項。


<a name="crit-networking-step5"></a>
## <a name="optional-your-clients-and-office-365-applications-are-configured-for-optimal-performance"></a>選用：設定用戶端和 Office 365 應用程式達到最佳效能

您已在用戶端裝置上針對 Exchange Online、商務用 Skype Online、SharePoint Online 和 Project Online 服務最佳化傳輸控制通訊協定 (TCP) 設定。

如有需要，[步驟 5](networking-optimize-tcp-performance.md) 可協助您使用此選項。

## <a name="results-and-next-steps"></a>結果和後續步驟

您的內部網路使用者現在可以透過有效的網路路徑及透過網際網路取用 Microsoft 365 雲端服務。

|||
|:-------|:-----|
|![階段 2 - 身分識別](../media/deploy-foundation-infrastructure/identity_icon-small.png)| 如果您會遵循 Microsoft 365 企業版的端對端部署階段，則下一個階段是[身分識別](identity-infrastructure.md)。 |
