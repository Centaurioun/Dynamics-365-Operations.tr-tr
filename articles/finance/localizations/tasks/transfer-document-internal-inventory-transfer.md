---
title: Şirket içi stok transferi için bir transfer belgesi oluşturma
description: Bu yordam, bir şirket içinde malların taşınması için transfer belgeleri oluşturmayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4da59781f3357a6713eebba03d87c5127b8cd3b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175070"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Şirket içi stok transferi için bir transfer belgesi oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir şirket içinde malların taşınması için transfer belgeleri oluşturmayı gösterir. Bu yordam yalnızca birincil adresi Litvanya'da bulunan tüzel kişilikler tarafından kullanılabilir. Bu yordam, birincil adresi Litvanya'da bulunan demo veri şirketi DEMF kullanılarak oluşturulmuştur. Bu yordamı tamamlayabilmeniz için "Şirket içinde malların taşınması için transfer belgelerini ayarlama" yordamını tamamlamanız gerekir. Bu yordam stok muhasebecileri için tasarlanmıştır. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="create-a-transfer-order"></a>Transfer emri oluşturma
1. Stok Yönetimi > Gelen siparişler > Transfer emri'ne gidin.
2. Yeni'ye tıklayın.
3. Kaynak ambar alanında bir değer girin veya bir değer seçin.
4. Hedef ambar alanında bir değer girin veya bir değer seçin.
5. Ekle öğesine tıklayın.
6. Listede, seçili satırı işaretleyin.
7. Madde numarası alanında bir değer girin veya seçin.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Transfer emri için taşıma ayrıntılarını girme
1. Kaydet'e tıklayın.
2. Eylem Bölmesinde, Sevk et'e tıklayın.
3. Taşıma Ayrıntıları'na tıklayın.
4. Taşıma ayrıntılarını yazdır alanında Evet'i seçin.
5. Malları veren alanına bir değer girin veya seçin.
6. Paket alanına bir değer yazın.
7. Yükün risk düzeyi alanına bir değer yazın.
8. Taşıyıcı alanına bir değer girin veya seçin.
9. Model alanına bir değer girin veya seçin.
10. Kayıt numarası alanına bir değer yazın.
11. Treyler kayıt numarası alanına bir değer girin.
12. Sürücü alanına bir değer girin veya seçin.
13. Sürücü adı alanına bir değer yazın.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Nakledilmemiş bir transfer emri için sevk irsaliyesini görüntüleme
1. Sevk irsaliyesi'ne tıklayın.
2. Tamam'a tıklayın.
3. Sayfayı kapatın.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Nakledilmiş transfer emri için sevk irsaliyesini görüntüleme
1. Eylem Bölmesi'nde, Transfer emri'ne tıklayın.
2. Eylem Bölmesinde, Sevk et'e tıklayın.
3. Sevk transfer emri'ne tıklayın.
4. Genel sekmesine tıklayın.
5. Güncelleştir alanında bir seçenek belirleyin.
6. Özet sekmesine tıklayın.
7. Sevk irsaliyesi alanına bir değer girin.
8. Tamam'a tıklayın.
9. Eylem Bölmesinde, Sevk et'e tıklayın.
10. Sevk irsaliyesi'ne tıklayın.
11. Tamam'a tıklayın.
