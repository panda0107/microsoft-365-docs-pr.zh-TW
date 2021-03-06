---
title: 高級 eDiscovery 中支援的檔案類型
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
description: Microsoft 365 Advanced eDiscovery 中支援的檔案類型清單。 這包括「高級 eDiscovery」中的 OCR 功能支援的影像檔案類型清單。
ms.openlocfilehash: 562b39664dd29ff3cf738e0d3ded7cc2f0cbb21c
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/13/2020
ms.locfileid: "42634631"
---
# <a name="supported-file-types-in-advanced-ediscovery"></a>高級 eDiscovery 中支援的檔案類型

「高級 eDiscovery」支援許多不同層級的檔案類型，如下表所述。 此清單尚未完成，我們會在繼續進行驗證測試時，新增檔案類型。 這些表格指出在原生檢視器中可查看檔案類型（和光學字元辨識或 OCR 文字提取），以及在高級 eDiscovery 的批註檢視器中支援的檔案類型。

## <a name="archive--container"></a>封存/容器

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 容器提取 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |
| application/x-7z-壓縮 | 是 | 是 | 是 | .7z |
| application/x-已壓縮的 rar | 是 | 是 | 是 | rar |
| application/x-tar | 是 | 是 | 是 | tar |
| application/zip | 是 | 是 | 是 | .zip |
||||||||

## <a name="audio--video"></a>Audio/Video

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/未用的 | 是 | 是 | 否 | 是 | 否 | f4v; m4a; m4v;... mp4v; mpeg;. mpeg4 |
| 音訊/mpeg | 是 | 是 | 否 | 是 | 否 | mpeg |
| 影片/3gpp | 是 | 是 | 否 | 是 | 否 | .3gp |
| 影片/3gpp2 | 是 | 是 | 否 | 是 | 否 | .3g2; .3gp2 |
| 影片/quicktime | 是 | 是 | 否 | 是 | 否 | 。 moov; mov; qt |
| 影片/x-m4v | 是 | 是 | 否 | 是 | 否 | .m4v |
||||||||

## <a name="database"></a>Database

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/x-msaccess | 是 | 是 | 是 | 否 | 否 | .mdb |
||||||||

## <a name="email"></a>電子郵件

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd.ms-excel。 ms-outlook | 是 | 是 | 是 | 是 | 是 | .msg |
| message//rfc822 | 是 | 是 | 是 | 是 | 是 | .eml |
| 文字/電子名片-連絡人 | 是 | 是 | 是 | 是 | 是 | .vcf |
||||||||

## <a name="email-container"></a>電子郵件容器

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 容器提取 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |
| application/mbox | 是 | 是 | 是 | .mbox |
| application/vnd.ms-excel。 ms-outlook-pst | 是 | 是 | 是 | .pst |
||||||||

## <a name="html"></a>HTML

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/xhtml + xml | 是 | 是 | 是 | 是 | 是 | 的 xhtml |
| application/xml | 是 | 是 | 是 | 是 | 是 | .xml |
| 文字/html | 是 | 是 | 是 | 是 | 是 | .htm; .html; shtml |
||||||||

## <a name="image"></a>影像

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | OCR 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| 影像/bmp | 是 | 是 | 是 | 是 | 是 | .bmp |
| 影像/emf | 是 | 是 | 是 | 是 | 是 | .emf |
| image/gif | 是 | 是 | 是 | 是 | 是 | .gif |
| 影像/jpeg | 是 | 是 | 是 | 是 | 是 | jpeg; .jpg |
| image/png | 是 | 是 | 是 | 是 | 是 | .png |
| 影像/svg + xml | 是 | 是 | 是 | 是 | 否 | 。 svg |
| 影像/tiff | 是 | 是 | 是 | 是 | 是 | .tif |
| image/vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | dwg; dxf |
| image/wmf | 是 | 是 | 是 | 是 | 是 | .wmf |
||||||||

## <a name="microsoft-excel"></a>Microsoft Excel

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd.ms-excel。 ms-excel | 是 | 是 | 是 | 是 | 是 | .dat; .xls |
| ms-excel 的 macroenabled （vnd.ms-excel） | 是 | 是 | 是 | 是 | 否 | 。 xlsb |
| ms-excel macroenabled （vnd.ms-excel） | 是 | 是 | 是 | 是 | 是 | 。 xlsm |
| ms-excel macroenabled （vnd.ms-excel） | 是 | 是 | 是 | 否 | 否 | 。 xltm |
| openxmlformats-officedocument 的 spreadsheetml （應用程式/vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | .xlsx |
| openxmlformats-officedocument spreadsheetml。 vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | 。 .xltx |
||||||||

## <a name="microsoft-onenote"></a>Microsoft OneNote

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/onenote | 是 | 是 | 是 | 是 | 否 | 。 one |
||||||||

## <a name="microsoft-powerpoint"></a>Microsoft PowerPoint

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd.ms-excel。 ms-powerpoint | 是 | 是 | 是 | 是 | 是 | .pot; .pps; .ppt |
| openxmlformats-officedocument presentationml。簡報中的 vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | .pptx |
| openxmlformats-officedocument 的 presentationml。投影片放映 vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | 。 ppsx |
| openxmlformats-officedocument presentationml。 vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | 。 potx |
||||||||

## <a name="microsoft-project"></a>Microsoft Project

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd.ms-excel。 ms-project | 是 | 是 | 是 | 否 | 是 | mpp |
||||||||

## <a name="microsoft-publisher"></a>Microsoft Publisher

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/x-mspublisher | 是 | 是 | 是 | 是 | 是 | pub |
||||||||

## <a name="microsoft-visio"></a>Microsoft Visio

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| ms-visio 的應用程式/vnd.ms-excel | 是 | 是 | 是 | 是 | 否 |  |
| application/vnd.ms-excel。 visio | 是 | 是 | 是 | 是 | 是 | .vsd |
||||||||

## <a name="microsoft-word"></a>Microsoft Word

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/msword | 是 | 是 | 是 | 是 | 是 | .dat; .doc |
| application/rtf | 是 | 是 | 是 | 是 | 是 | .doc; .rtf |
| ms-word macroenabled （vnd.ms-excel） | 是 | 是 | 是 | 是 | 是 | .docm |
| ms-word macroenabled （vnd.ms-excel） | 是 | 是 | 是 | 是 | 是 | normal.dotm |
| openxmlformats-officedocument 的 wordprocessingml。檔 vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | .docx |
| openxmlformats-officedocument wordprocessingml。 vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | 。 dotx |
||||||||

## <a name="microsoft-works"></a>Microsoft Works

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| ms-works-ss （應用程式/vnd.ms-excel） | 是 | 是 | 否 | 否 | 否 | wps |
| application/vnd.ms-excel。 ms-works-wp | 是 | 是 | 否 | 否 | 否 | wps |
||||||||

## <a name="open-document-format"></a>開放式檔案格式

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| oasis。 text vnd.ms-excel | 是 | 是 | 是 | 是 | 是 | odt |
||||||||

## <a name="other"></a>其他

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/json | 是 | 是 | 是 | 是 | 是 | n/a |
| application/vnd.ms-excel。 ms-graph | 是 | 是 | 否 | 否 | 否 |  |
| application/winhlp | 是 | 是 | 否 | 否 | 否 | .hlp |
| application/x-tnef | 是 | 是 | 否 | 否 | 否 |  |
||||||||

## <a name="plain-text"></a>純文字

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| 文字/csv | 是 | 是 | 是 | 是 | 是 | .csv |
| 文字/無格式 | 是 | 是 | 是 | 是 | 是 | con; .css; .csv; .dat;. pl; .txt |
||||||||

## <a name="portable-document-format"></a>可移植檔案格式

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/pdf | 是 | 是 | 是 | 是 | 是 | .pdf |
||||||||

## <a name="word-perfect"></a>Word 完美

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd.ms-excel-wordperfect;版本 = 5。0 | 是 | 是 | 是 | 否 | 否 | .wpd |
| application/vnd.ms-excel-wordperfect;版本 = 5。1 | 是 | 是 | 是 | 否 | 否 | .wpd |
| application/vnd.ms-excel-wordperfect;版本 = 6。 x | 是 | 是 | 是 | 否 | 否 | .wpd |
||||||||

## <a name="word-pro"></a>Word Pro

| Mime 類型 | 檔識別 | 中繼資料解壓縮 | 文字提取 | 原生檢視器 | 批註檢視器 | 可能的分機 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd.ms-excel。 lotus-wordpro | 是 | 是 | 否 | 否 | 否 | lwp |
||||||||
