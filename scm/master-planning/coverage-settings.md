---
title: "Kapsam ayarları"
description: "Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b42f0515823bd42ec260aa1d175855a923162b62
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="coverage-settings"></a>Kapsam ayarları

[!include[banner](../includes/banner.md)]


Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır. 

Karşılama ayarlarını birkaç şekilde belirtebilirsiniz:

-   Bir kapsam grubuna yönelik kapsam ayarlarını belirtin. Kapsam grubuyla bağlantılı tüm ürünlere yönelik ayarları içeren bir kapsam grubu oluşturabilirsiniz. **Master planlama &gt; Kurulum &gt; Kapsam &gt; Kapsam grupları'na** tıklayarak karşılama grubu oluşturun. Ürüne bir kapsam grubu bağlayabilirsiniz. Bağlantı belirli bir siteye, ambara veya ürün boyutuna ise, **Madde kapsamı** sayfasındaki **Kapsam grubu** alanını kullanın. Bağlantı genel ise, ürün boyutlarından bağımsız olarak **Ürün ayrıntıları** sayfasındaki **Plan** FastTab'inde yer alan **Kapsam grubu**'un kullanın. Bir kapsam grubunu bir ürüne bağlamazsanız, master planlama **Master planlama parametreleri** sayfasında varsayılan olarak belirtilen **Genel kapsam grubu**'nu kullanır.

-   Bir ürün için kapsam ayarları belirtin. Özel bir ürün için kapsam ayarları oluşturabilirsiniz. **Ürün bilgileri yönetimi &gt; Ürünler &gt; Serbest bırakılan ürünler** seçeneğine tıklayın. Ürünü seçin, **Eylem Bölmesi**'nde, **Plan** sekmesinde, **Kapsam grubu**'nda **Madde kapsamı**'na tıklayarak **Madde kapsamı** sayfasını açın. Ürün bir kapsam grubuna zaten bağlanmışsa, **Üstüne yazdır** alanını kullanarak kapsam grubu ayarlarının üstüne yazdırabilirsiniz. **Madde kapsamı** sayfasındaki kapsam ayarları, **Kapsam grubu** sayfasındaki ayarlardan önceliklidir.

<!-- -->

-   Sihirbaz kullanarak bir ürüne yönelik kapsam ayarlarını belirleyin. Sihirbaz, birincil madde karşılama parametrelerini ayarlamaya yönelik bir adım adım kılavuzdur. **Madde kapsamı** sayfasında **Sihirbaz**'a tıklayarak **Madde Kapsamı Sihirbazı**'nı açın.

<!-- -->

-   Boyut grubu için kapsam ayarları belirtin. **Ürün bilgileri yönetimi &gt; Ortak &gt; Serbest bırakılan ürünler**'e tıklayın. **Serbest bırakılan ürün ayrıntısı **sayfasında, **Genel** sekmesinde, **Yönetim** grubunda, **Depolama boyut grubu** bağlantısına tıklayın. **Depolama boyut grubu** sayfasında **Boyuta göre kapsam planı** alanını seçerek depolama boyut grubundaki bir boyut için kapsam ayarları oluşturabilirsiniz. Yapılandırma, renk, boyut, stil gibi tüm ürün boyutlarının **Boyuta göre kapsam planı** alanı seçilmiş olmalıdır.



<a name="see-also"></a>Ayrıca bkz.
--------

[Master planlar](master-plans.md)



