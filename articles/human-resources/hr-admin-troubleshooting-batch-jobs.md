---
title: Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme
description: Bu konu altında, saatler sonra uzun süre çalışan toplu işler planlayarak Microsoft Dynamics 365 Human Resources ile ilgili bazı performans sorunlarının nasıl çözüleceğini açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500517"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme

## <a name="issue"></a>Çıkış

Microsoft Dynamics 365 Human Resources, uzun süren toplu işler tipik iş saatlerinde çalışıyorsa, performans sorunlarıyla karşılaşabilir.

## <a name="resolution"></a>Çözünürlük

Aşağıdaki toplu işleri kapalı saatlerde zamanlar. Ayrıca, sık çalışan toplu işlerin sıklığını gözden geçirmeyi öneririz. Mümkünse, toplu işin tekrarlanma şeklini azaltın. Birçok durumda, varsayılan sıklık yeterlidir.

Aşağıdaki toplu işler gece veya saat tarihinden sonra çalışmalıdır. Bu yinelenen toplu işlerin saat dilimini kontrol edin. Bazı toplu işler Pasifik Standart Saati (PST) kullanabilir.

| Toplu iş | Varsayılan oluşum |
| --- | --- |
| Toplu iş geçmişi temizleme | Ayda 1 saat |
| Dışa aktarma hazırlığını temizleme | Günde 1 saat |
| Common Data Service tümleştirmesi, istek eşitlemesini atladı | Günde 1 saat |
| Saatler dışında düzenli olarak çalıştırılması gereken veritabanı sıkıştırma sistemi işi | Günde 1 saat |
| Saatler dışında düzenli olarak çalıştırılması gereken veritabanı dizin yeniden oluşturma sistem işi | Günde 1 saat |

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Arama** çubuğunda, yukarıdaki toplu işlerden birini arayın.

3. **Arka planda çalıştır**'ı ve sonra **Tekrar**ı seçin.

   ![Yinelemeyi ayarlayın](media/talent-batch-history-cleanup-recurrence.png)

4. **Yineleme tanımla** altında, **Başlangıç tarihi** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın. **Bitiş tarihi yok**'u seçin. 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın](media/talent-batch-history-cleanup-define-recurrence.png)

5. **Tamam**'ı seçin.

6. Gerekirse **Arka planda çalıştır** altındaki diğer parametreleri değiştirin ve **Tamam**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Otomatik temizleme görevleriyle performansı en iyi duruma getirme](hr-admin-troubleshooting-batch-history.md)