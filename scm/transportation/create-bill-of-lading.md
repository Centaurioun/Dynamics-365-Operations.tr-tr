---
title: "Bir konşimento oluştur"
description: "Bu konu, ambar yönetimi işlemleri kullanırken bir konşimentonun nasıl oluşturulacağını açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f3010daa41f54cf026d46b1b7648a277651173da
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-bill-of-lading"></a>Bir konşimento oluştur

[!include[banner](../includes/banner.md)]


Bu konu, ambar yönetimi işlemleri kullanırken bir konşimentonun nasıl oluşturulacağını açıklar.  

Bir konşimento, maddeleri sevk eden şirket ve taşıyıcı arasındaki yasal bir belgedir. Belge sevk edilen maddelere eşlik eder ve öğeler varış noktasında teslim edildiğinde sevk irsaliyesi alış irsaliyesi olarak hizmet verir. Ambar yönetimi kullanıyorsanız, konşimento oluşturmanın iki yolu vardır:

  -   **Konşimento** sayfası kullanarak raporu el ile oluşturma.
  -   Raporu **Yük planlama workbench** üzerinden oluşturmak.

Konşimentoyu **Yük planlama workbench** üzerinden oluşturursanız, yük durumu **Sevk edilmiş.** olmalıdır. Yükte birden fazla sevkiyat varsa, her bir sevkiyat için bir konşimento oluşturulur. Bir konşimento oluşturulduktan sonra **Konşimento** sayfasında onun üzerinde değişiklik yapabilirsiniz.

## <a name="master-bill-of-lading"></a>Ana konşimento
Eğer yükte birden fazla sevkiyat varsa, bir ana konşimento oluşturabilirsiniz. Bu konşimento ile aynı biçime ve bilgilere sahiptir, ancak tüm sevkiyatların özetlenmiş bir içeriğini de içerir. Eğer **Bir yükte birden fazla sevkiyat olduğunda bir ana konşimento oluştur** seçeneği **Taşıma yönetim parametreleri** sayfasında **Evet** olarak ayarlanmışsa, bir konşimentoyu **Yük planlama workbench** üzerinden oluşturduğunuzda ve birden fazla sevkiyat bulunduğunda, otomatik olarak bir ana konşimento oluşturulacaktır. Ayrıca konşimento listelerini **İlgili bilgi** &gt; **Konşimento** üzerine tıklayarak da alabilirsiniz. Konşimentoları el ile oluşturuyorsanız, bir ana konşimentoyu **Konşimento** sayfası üzerinde oluşturabilirsiniz.



