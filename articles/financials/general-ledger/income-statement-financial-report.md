---
title: Gelir tablosu mali raporu
description: "Bu makale varsayılan rapor için gelir tablolarını açıklar. Ayrıca, bu raporla ilişkili olan yapı taşlarını açıklar."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: f07aea0b87bc3e09982f9ba248d3c28540fd2dc5
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="income-statement-financial-report"></a>Gelir tablosu mali raporu

[!include[banner](../includes/banner.md)]


Bu makale varsayılan rapor için gelir tablolarını açıklar. Ayrıca, bu raporla ilişkili olan yapı taşlarını açıklar. 

<a name="default-income-statement-report"></a>Varsayılan gelir tablosu raporu
-------------------------------

| Varsayılan rapor             | Ne yapar                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Gelir Beyanı – Varsayılan | Geçerli dönem ve ayrıca yılbaşından bugüne kadar olan süre için organizasyonun karlılığını gösterir. |

## <a name="building-blocks"></a>Yapı taşları
Gelir tablosu mali raporu aşağıdaki yapı taşlarını kullanır.

| Varsayılan rapor             | Satır tanımı                     | Sütun tanımı          |
|----------------------------|------------------------------------|----------------------------|
| Gelir Tablosu - Varsayılan | Özet Gelir Tablosu - Varsayılan | Dönemsel ve YTD - Varsayılan |

### <a name="row-definition"></a>Satır tanımı

Satır tanımı, Özeti Gelir Tablosu – Varsayılan, klasik bir gelir tablosunun her bir kısmı için bir bölüm içerir. Ana Hesap Kategorisi boyutu bu satır tanımının oluşturulması için kullanılır. Bu nedenle, herhangi biri hiçbir değişiklik yapmasına gerek kalmadan rapor oluşturabilir.

### <a name="column-definition"></a>Sütun Tanımı

Sütun tanımları, farklı ayrıntı ve mali veri düzeyleri sunmak üzere farklı türlerde sütunlar içerir.

-   **Dönemsel ve YTD – Varsayılan sütun türleri:**
    -   **DESC** – Satır tanımının açıklaması
    -   **FD** – Mevcut dönem için mali veriler
    -   **FD** – Yılbaşından bugüne kadar olan süre için mali veriler

 

<a name="see-also"></a>Ayrıca bkz.
--------

[Mali raporlama](financial-reporting-getting-started.md)

[Mali raporları görüntüleme](view-financial-reports.md)

[Dynamics Mali Raporlama Blogu](http://blogs.msdn.com/b/dynamics_financial_reporting/)



