--- 
title: "Şirket içi stok transferi için bir transfer belgesi oluşturma"
description: "Bu yordam, bir şirket içinde malların taşınması için transfer belgeleri oluşturmayı gösterir."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0fe3d735d6309bf87047a27f9e68c579ca052012
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Şirket içi stok transferi için bir transfer belgesi oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

