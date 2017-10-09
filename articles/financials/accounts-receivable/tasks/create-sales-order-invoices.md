--- 
title: "Satış siparişi faturaları oluşturma"
description: "Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 50c0ee41220461e282aace85f10a0e734a2ab688
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-order-invoices"></a>Satış siparişi faturaları oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır. Bu yordam, USMF demo şirketini kullanır.


## <a name="create-an-invoice-from-a-sales-order"></a>Satış siparişinden fatura oluşturma
1. Alacak hesapları > Siparişler > Sevk edilen ancak faturalanmayan satış siparişleri'ne gidin.
2. Listeden bir satış siparişi seçin. 
3. Eylem Bölmesinde, Fatura öğesine tıklayın.
4. Fatura'ya tıklayın.
    * Bu satış siparişiyle ilişkilendirilmiş birden fazla sevk irsaliyesi bulunmaktadır. Sevk irsaliyesi numarası yerine <multiple> sözcüğü görüntülenecektir.  
5. Parametreler bölümünü genişletin.
    * Faturanın deftere nakledilebilmesi için Nakil öğesinin Evet olarak ayarlanması gerekir. Deftere nakli devre dışı bırakıp yalnızca faturayı yazdırmayı da seçebilirsiniz. Ancak, fatura yerine bir proforma fatura hazırlayarak da aynı sonucu elde edebilirsiniz.  
    * Bu seçenek, toplu işler için kullanılır. Toplu iş çalıştırıldığında, sorgu çalıştırılır.    
6. Yazdırma alanında 'Sonra'yı seçin.
7. Fatura yazdır için Evet'i seçin.
    * Yazdırma yönetimi, faturanın birden çok kopyasını yazdırabilir ve aynı zamanda faturayı bir PDF dosyası olarak e-posta yoluyla gönderebilir.  
8. Giderleri yazdır alanında 'Özetle'yi seçin.
9. Kredi limitini denetle alanına 'Bakiye'yi seçin.
10. İptal'e tıklayın.

## <a name="combine-orders-into-a-single-invoice"></a>Siparişleri tek bir faturada birleştirme
1. Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.
2. Birden fazla açık faturası olan bir müşteri bulun.
3. Açık bir satış siparişi seçin.
4. Aynı müşteri için başka bir açık satış siparişi seçin.
5. Eylem Bölmesinde, Fatura öğesine tıklayın.
6. Fatura'ya tıklayın.
7. Parametreler bölümünü genişletin.
8. Miktar alanında, 'Tümü' öğesini seçin.
    * Genel bakış sekmesinde iki fatura bulunmaktadır. Şimdi bunları tek bir faturada birleştirin.  
9. Özet güncelleştirme kapsamı alanında 'Fatura'yı seçin.
10. Satış siparişlerini tek bir faturada birleştirmek için Düzenle'ye tıklayın.
    * İki satış siparişi artık tek bir fatura birleştirilmiştir.   
11. İptal'e tıklayın.
12. Evet'i tıklatın.

## <a name="post-invoices-in-a-batch"></a>Faturaları toplu işte deftere nakletme
1. Alacak hesapları > Faturalar > Toplu faturalama > Fatura'ya gidin.
2. Seç'e tıklayın.
3. Tamam'a tıklayın.
4. Toplu iş'e tıklayın.
5. Toplu işlem'i açmak için Evet'e tıklayın.
6. Yineleme'ye tıklayın.
7. Günler'i seçin
8. Tamam'a tıklayın.
9. Tamam'a tıklayın.
10. İptal'e tıklayın.
11. Evet'i tıklatın.

