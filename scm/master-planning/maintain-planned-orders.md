---
title: "Planlı siparişleri koru"
description: "Bu maddede planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 94f6f28ec4b255930f84a27eb5394503ff59e4c0
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="maintain-planned-orders"></a>Planlı siparişleri koru

[!include[banner](../includes/banner.md)]


Bu maddede planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.

Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz. İlerlemenizi takip etmeye yardımcı olan **Durum** alanını kullanabilirsiniz. Aşağıdaki değerler kullanılır:

-   Master planlama planlı siparişler ürettiğinde, planlı siparişler **İşlem görmedi** durumunda olur.
-   Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu **Tamamlandı** olarak ayarlayabilirsiniz.
-   Planlı bir siparişi kesinleştirmeye karar verdiğinizde, durumunu **Onaylandı** olarak ayarlayabilirsiniz. Bu durum, planlı siparişin kesinleştirilmesini onayladığınızı ama henüz kesinleştirmediğinizi gösterilir.

**Not:** Onaylanan bir planlı sipariş geçerli durumunda sonraki master planlama hesaplamasına transfer edilir. Planlı siparişleri **Kesinleştir** seçeneğine tıklayarak kesinleştirebilirsiniz. Aşağıdaki planlı siparişleri kesinleştirebilirsiniz:

-   Seçilen planlı sipariş.
-   Birden çok planlı sipariş.
-   **Açılım** sayfasından bir açılımla üretilen planlı siparişler. **Planlı siparişler** seçeneğine tıklayın, planlı siparişi seçin, sonra da **Kesinleştir** seçeneğine tıklayın.

Planlı bir sipariş kesinleştirildiğinde, ilgili modülün siparişler bölümüne taşınır. **Not:** Özel durumu olan planlı siparişi sağ tıklatıp, aynı durumda olan planlı siparişlere filtre uygulayabilirsiniz. Bu işlevsellik örneğin **Onaylandı** durumundaki tüm siparişleri filtrelemek istediğinizde kullanışlıdır, böylece bunları daha sonra kesinleştirebilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Master planlar](master-plans.md)



