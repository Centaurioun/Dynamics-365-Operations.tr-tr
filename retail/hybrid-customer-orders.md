---
title: "Karma müşteri siparişleri"
description: "Bir karma müşteri siparişi, hem müşteri tarafından mağazadan alınabilecek ürünler içeren hem de daha sonra çekilecek veya sevk edilecek tek bir sipariştir."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: eb6ba7cfdf098671192d4d6e73119f96b287c437
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="hybrid-customer-orders"></a>Karma müşteri siparişleri

[!include[banner](includes/banner.md)]


Bir karma müşteri siparişi, hem müşteri tarafından mağazadan alınabilecek ürünler içeren hem de daha sonra çekilecek veya sevk edilecek tek bir sipariştir.

Microsoft Dynamics 365 for Operations - Perakende içerisinde, bir müşteri siparişi için tüm ürünleri yerine getirmeyi veya yalnızca seçilen ürünleri yerine getirmeyi seçebilirsiniz. Yerine getirilmek üzere işaretlenmiş ürün satırları, sipariş oluşturulduktan sonra otomatik olarak faturalanır, sipariş oluşturulduktan sonra çekilecek bir sipariş için de aynı şey geçerlidir. Karma siparişlerde kalan tutar, ürün çekme ve sevk satırlarındaki depozito yüzdesini, yürütülecek satırların toplam tutarına eklenerek belirlenir. Sistem, karma siparişler için müşteri sipariş modur ve nakit ve taşı modları arasında şöyle geçiş yapar:

-   Sepetteki tüm ürünler **Teslim alınan taşıma** olarak ayarlanmışsa, sipariş Öde ve Al hareketi olarak ele alınır.
-   Sepetteki tüm veya bazı satırlar **Çekme** veya **sevk nakliyesi** olarak ayarlanmışsa, sipariş Müşteri sipariş hareketi olarak ele alınır.

Bir sepet satırı seçildiyse ve **Seçileni çek**, **Seçileni sevk et** veya **Seçileni al git** seçiliyse, sadece belirli sepet satırları bu teslim yöntemiyle ayarlanır. Bu durumda, işlem akışı her zaman olduğu gibi devam eder. Ancak, **Seçileni çek**, **Seçileni sevk et** veya **Seçileni al git**, sepet satırı seçmeden seçildiyse, tüm sepet satırlarını listeleyen yeni bir sayfa açılır. Bu ekranda, bir teslim yöntemi ayarlamak için birden fazla satırı aynı anda seçebilirsiniz. Satırları seçmek için bu yöntemi kullandığınızda, satıra daha önce atanan tüm teslim yöntemleri geçersiz kılınır.

<a name="see-also"></a>Ayrıca bkz.
--------

[Müşteri siparişlerine genel bakış](customer-orders-overview.md)



