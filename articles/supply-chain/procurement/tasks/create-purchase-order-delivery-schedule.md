--- 
title: "Teslimat planı olan satınalma siparişi oluşturma"
description: "Bu prosedür, satınalma siparişi için teslimat oluşturmayı göstermektedir."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 93bd832b4bbb91e6bd0288042098383eb5f4488d
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Teslimat planı olan satınalma siparişi oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, satınalma siparişi için teslimat oluşturmayı göstermektedir. Teslimat planı, bir siparişteki veya günlükteki miktarın birden fazla sevkiyatlar halinde teslim edilmesi istendiği zaman kullanılır. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Bu prosedür tipik olarak bir satın alma temsilcisi tarafından gerçekleştirilir.


## <a name="create-a-delivery-schedule"></a>Teslimat planı oluşturma
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanına, US-101 girin.
4. Tamam'a tıklayın.
5. Madde numarası alanına M0001 girin.
6. Miktar alanına 10 yazın.
7. Satınalma siparişi satırına tıklayın.
8. Teslimat planı öğesine tıklayın.
    * Teslimat planı sayfası, sipariş satırı toplam miktarının satıcıdan teslim edileceği sevkiyat sayısını belirtmenize olanak tanır.  
    * Varsayılan olarak, sistem orijinal satınalma satırının toplam miktarını ve diğer teslimat ayrıntılarını ilk teslimat planı satırına kopyalar. Bu örnekte iki sevkiyat planı oluşturacağız ve ikinci sevkiyatın tarihi, ilk sevkiyattan bir hafta sonra olacak.  
9. Miktar alanında miktarı 4 olarak değiştirin.
10. Yeni'ye tıklayın.
11. Miktar alanına, kalan miktar olarak 6 girin.
    * Teslimat tarihi alanında ilk teslimat satırındaki tarihten bir hafta sonraki tarihi seçin.  
    * Toplam ve Kalan alanlarına bakarak, teslimat planı satırlarına tahsis edilen toplam miktarı izleyebilirsiniz. Kalan miktar sıfır olduğunda, orijinal satırdan alınan tüm miktar plana tahsis edilmiştir.  
12. Gider dönüştürme bölümünü genişletin.
    * Burada seçenekler, teslimat planı satırları üzerinden masrafları nasıl dağıtmak istediğinizi kontrol etmenize olanak tanır. Brüt tutarları kopyala'yı seçerseniz her teslimat satırına orijinal sipariş satırındaki masraf tutarı kopyalanır. Teslimat satırlarına tahsis et seçeneği orijinal satırdaki masrafı her bir teslimat satırındaki miktara göre böler.  
13. Gider dönüştürme bölümünü daraltın.
14. Tamam'a tıklayın.
    * Teslimat planı siparişe artık uygulanmıştır.  
    * Ticari satırı olarak anılan orijinal sipariş satırı, birden fazla teslimatlı bir Siparişe dönüştürülmüştür. Farklı bir simgeyle işaretlenir ve teslimat satırları için başlık olarak işlev görür.  
15. İki teslimat satırının ilki olan ikinci sipariş satırını seçin.
    * Teslimat satırları olarak anılan iki yeni satır bir teslim planı oluşturur. Sipariş orijinal satıra göre değil, bu satırlara göre işlenir. Onaylar, ürün girişi günlükleri veya faturalar gibi belgeler yazdırılırken yalnızca teslimat satırları gösterilir.  

## <a name="change-the-delivery-schedule"></a>Teslimat planını değiştirin
    * Teslimat satırlarında miktarı değiştirebilirsiniz. Bunu yaparsanız, ticari satırı otomatik olarak güncelleştirilip, teslimat satırlarındaki toplam miktara çevrilir.  
1. İlk teslimat satırının miktar alanında miktarı 4'ten 5'e değiştirin.
2. İlk sipariş satırını (ticari satırı) seçin.
    * Ticari satırındaki miktar 11'e değiştirilmiştir.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Teslimat planlarını kullanarak ürün girişini işleyin
    * Satınalma siparişi ürün girişi işlenmeden önce onaylanmalıdır. Bu örnekte giriş doğrudan satınalma siparişi üzerinden kaydedilir. Mallar ambara ulaştığında da giriş kaydedilmiş olur.  
1. Eylem Bölmesinde, Satınalma öğesine tıklayın.
2. Onayla seçeneğine tıklayın.
3. Eylem Bölmesinde, Al öğesine tıklayın.
4. Ürün girişi seçeneğine tıklayın.
5. Ürün girişi alanına herhangi bir değer yazın.
    * Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.  
    * Miktar alanında, 'Sipariş edilen miktar'ı seçin. Bu seçenek, sipariş satırlarının birlikte oluşturulduğu miktar için girişin işleneceği anlamına gelir.  
    * Ürün girişi yazdır alanının Hayır olarak ayarlandığından emin olun. Bu örnekte, yazdırma gerekli değildir.  
6. Satırlar bölümünü genişletin.
    * Ürün girişinin orijinal sipariş satırı değil iki teslimat satırı için oluşturulduğuna dikkat edin. Giriş ambarda kaydedilmişse teslimat planı satırlarında da kaydedilmiş olur.  
7. Satırlar bölümünü daraltın.
8. Girişi nakletmek için Tamam'a tıklayın.

