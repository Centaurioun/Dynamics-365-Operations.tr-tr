---
title: "Karma plaka alımı"
description: "Bu konu, bir mobil cihaz ile çoklu öğe için iş oluşturma ve kaydetme amacıyla karma plaka alma kullanmayı açıklar."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0e785d71e7ae3c5f60d36d8b190001b5e356c626
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="mixed-license-plate-receiving"></a>Karma plaka alımı

[!include[banner](../includes/banner.md)]

Karma plaka almak, yerine koyma işlemi oluşturmadan önce çoklu öğelerden oluşan bir plaka oluşturmanıza izin verir. 

Birden fazla öğeden oluşan bir plakanın, sizin her bir öğeyi kaydetmeniz için teslim alma noktasında bölünmesi gerekmez. 

Belge satırlarının kaynağını belirlemek için maddeye bağlı akış kullanırken, madde denetimi üzerindeki barkodları taratabilirsiniz. Barkodun üzerinde miktar ve bir ölçüm birimi (UOM) yapılandırılmışsa, madde ve miktar otomatik olarak karma plaka eklenir ve başka bir madde taramak için ekrana döndürülürsünüz. Bu da tüm maddeleri, her adımda bir onay vermek zorunda kalmadan hızlıca taramanıza olanak sağlar. 

Karma plaka alma akışı içerisinde, plakaya taranmış olan maddelerin listesini görüntüleyebilir ve buradan bir maddeyi değiştirebilir veya miktarını düzeltebilirsiniz.

## <a name="where-it-applies"></a>Uygulandığı yerler

Karma plaka alma, çoklu satır/madde için aynı anda kayıt ve iş oluşturma sağlayan bir mobil cihaz alma akışıdır. Bu, birden çok öğe içeren gelen plakalar alıyorsanız yararlıdır. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>Karma plaka almanın ayarlanması
Karma plaka alma, bir mobil cihaz menü öğesi olarak ayarlanır.

Mevcut işi kullanmayan ve aşağıdaki yöntemlerden birini kullanan, iş moduna sahip yeni bir menü öğesi oluşturmanız gerekir:

- Karma plaka alımı
- Karma plaka alımı ve yerine koyma işlemi

Kaynak belge satırlarını belirlemek için seçenekler şunlardır: satınalma siparişi maddesi, satınalma siparişi satırı, iade siparişi, transfer sipariş maddesi ve transfer emri satırı. Bu seçenekler, tek bir plaka üzerindeki alma sırasını değiştirebilir. Son seçenek yük maddesine göredir. Birden fazla maddeyi bir plakaya ekleyebilirsiniz ancak çoklu yükler arasında geçiş yapamazsınız.
