---
title: "Tahsisatları işleme"
description: "Bu makalede tahsisatlar, Microsoft Dynamics 365 for Operations&quot;da tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgiler verilmektedir. Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gider ve gelirlerin muhasebede doğru nesneye yazılmasının garanti altına alınmasına yardımcı olurlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1cfaeab1562716aa4c91806b228f17625e25dfff
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="process-allocations"></a>Tahsisatları işleme

[!include[banner](../includes/banner.md)]


Bu makalede tahsisatlar, Microsoft Dynamics 365 for Operations'da tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgiler verilmektedir. Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gider ve gelirlerin muhasebede doğru nesneye yazılmasının garanti altına alınmasına yardımcı olurlar.

Microsoft Dynamics 365 for Operations bu süreci desteklemek için şu özellikleri sağlar:

-   Muhasebe dağılımlarında Böl eylemini kullanarak veya bir belgeye mali boyut varsayılan şablonları uygulayarak hareket tutarlarını el ile atayabilirsiniz. Daha fazla bilgi için bkz.  [Hesap dağıtımları.](../accounts-payable/accounting-distributions.md)
-   Her bir ana hesapta tanımlanan atama şartlarına dayalı olarak hareket tutarlarını otomatik olarak atayın. Tahsisat hesabı girişleri, bir muhasebe girişinin kaynak defter hesabı olarak tanımlanan kriterleri karşılaması durumunda her bir günlük için yüzdeye ve hedef defter hesabına dayalı olarak üretilecektir.
-   Defter bakiyelerini veya sabit tutarları defter tahsisat kurallarına dayalı olarak otomatik olarak atayın. Defter tahsisat kuralları, atama günlükleri kullanılarak düzenli olarak işlenir. 

###  <a name="allocations-in-budget-planning"></a>Bütçe planlamasında tahsisatlar

Defter tahsisat kuralları, bütçe planları için kullanılabilir. Defter tahsisat kurallarını bütçe planlamada kullanıyorsanız, tahsisat kuralları, defterdekiyle aynı şekilde çalışacaktır, ancak kaynak verileri ve hedef verileri bütçe planından gelir. Bütçe planları için kullanılacak genel muhasebe tahsisat kurallarını el ile seçebilirsiniz. Alternatif olarak, bir iş akışı işleminin bir parçası olarak çalışan bir tahsisat zamanlaması kullanabilirsiniz.

> [!NOTE]
> Bütçe planlama için şirketler arası defter tahsisat kurallarını kullanamazsınız.





