--- 
title: "Müşteri ödeme yöntemi oluşturma"
description: "Müşteri ödemeleri için bir ödeme yöntemi oluşturun."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bfafcccb12112ca7cceefb65be3f942bfc307751
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-method-of-payment"></a>Müşteri ödeme yöntemi oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Müşteri ödemeleri için bir ödeme yöntemi oluşturun. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi'ne gidin.
2. Yeni'ye tıklayın.
3. Ödeme yöntemi alanına, ödeme yöntemi için bir kod girin.
    * Ödeme yöntemi kodu faturalarda ve ödemelerde gösterilir ve bu sayede, kaydedilmekte olan ödemenin türü ve ödeme yapılacak banka hesabının yeterince anlaşılması sağlanır.  
4. Açıklama alanına bir açıklama girin.
5. Ödemelerin nakledilmesi için gereken ödeme durumunu seçin.
    * Bir müşteri ödemesi oluşturulurken, yalnızca, ödeme durumu burada tanımladığınız ödeme durumuyla eşleştiği zaman nakledilebilir.  
6. Faturalar için müşteri ödemelerinin nasıl oluşturulacağını seçin.
    * Bu seçenek, yalnızca bir ödeme teklifi çalıştırılırken kullanılır. Doğrudan ödemeler yapılırken ve müşterilerin banka hesaplarından fonlar çekilirken müşteri ödemeleri için bir ödeme teklifi kullanılabilir.  
7. Ödeme türünü seçin.
    * Ödeme türü, ödemede bazı doğrulamalar yapılıp yapılmayacağını belirlemeye yardımcı olur.  
8. Ödemelerin nakledileceği hesap türünü seçin.
    * Genellikle bu seçenek için Banka seçili olacaktır.  
9. Bu ödemenin kaydedileceği banka hesabını seçin.
10. Bankanızın kullandığı ödeme türünü tanımak için Banka hareketi türünü girin.
    * Banka hareket türü, banka mutabakat işlemi sırasında kullanılır ve mutabakatı kolaylaştırabilir.  
11. Bu ödemenin geçici olarak bir bağlantılı hesaba nakledilip nakledilmeyeceğini belirtin.
    * Ödemenin bankadan çekilmesinde kasa devri zamanını denemek istiyorsanız Bağlantı işlevini kullanın. Ödeme bankadan çekilene kadar (ödemenin burada tanımladığınız banka hesabına geçtiği zamana kadar) geçici olarak bir Genel muhasebe hesabına nakledilir.  
12. Bağlantılı nakil için kullanılacak ana hesabı girin.
    * Bu, bağlantı kullanıldığı zaman ödemenin geçici olarak nakledileceği ana hesaptır.  
13. Elektronik ödemelere ilişkin ayarı tanımlamak için Dosya biçimi sekmesini kullanın.
14. Zorunlu alanlar tanımlamak için Ödeme kontrolü sekmesini kullanın.
    * Örneğin, bu ödeme yöntemiyle yapılan tüm ödemelerin yatırılmasını zorunlu kılıyorsanız, o seçeneği bu sekmede seçebilirsiniz.  
15. Bu ödeme yönteminde kullanmak istediğiniz ödeme özniteliklerini tanımlamak için Ödeme öznitelikleri sekmesini kullanın.
16. Kaydet'e tıklayın.

