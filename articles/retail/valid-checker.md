---
title: Perakende işlem tutarlılık denetleyicisi
description: Bu konuda Microsoft Dynamics 365 for Retail ürününde bulunan perakende işlem tutarlılık denetleyicisi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 05/30/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 1fc894206f9d90fce1e2eab292ac241e9d943e23
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617332"
---
# <a name="retail-transaction-consistency-checker"></a>Perakende işlem tutarlılık denetleyicisi


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Bu konuda Microsoft Dynamics 365 for Finance and Operations sürüm 8.1.3'te sunulan perakende işlem tutarlılık denetleyicisi açıklanmaktadır. Tutarlılık denetleyicisi, tutarsız hareketleri ekstre deftere nakil işlemi tarafından alınmadan önce tanımlayıp ayırır.

Bir ekstre Microsoft Dynamics 365 for Retail'de deftere nakledildiğinde deftere nakil işlemi, perakende hareket tablolarında tutarsız verilerin bulunması nedeniyle başarısız olabilir. Veri sorunu, satış noktası (POS) uygulamasında öngörülemeyen aksaklıklardan veya hareketlerin üçüncü taraf POS sistemleri tarafından yanlış aktarılmasından kaynaklanabilir. Bu tutarsızlıkların nasıl görünebileceğine ilişkin örnekler şunlardır: 

- Üstbilgi tablosundaki işlem toplamı, satırlardaki işlem toplamıyla eşleşmiyordur.
- Üstbilgi tablosundaki satır sayısı, işlem tablosundaki satır sayısıyla eşleşmiyordur.
- Üstbilgi tablosundaki vergiler, satırlardaki vergi tutarıyla eşleşmiyordur. 

Ekstre deftere nakil işlemi tarafından tutarsız işlemler seçildiğinde tutarsız satış faturaları ve ödeme günlükleri oluşturulur ve bunun sonucunda tüm ekstre deftere nakil işlemi başarısız olur. Ekstrelerin bu durumdan kurtarılması, birden fazla işlem tablosu arasında karmaşık veri düzeltmelerini içerir. Perakende işlem tutarlılık denetleyicisi, bu tür sorunları önler.

Aşağıdaki çizelgede işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi gösterilmektedir.

![Perakende işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi](./media/validchecker.png "Perakende işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi")

**Mağaza hareketlerini doğrula** toplu işlemi, aşağıdaki senaryolar için perakende hareket tablolarının tutarlılığını denetler.

- **Müşteri hesabı**: Perakende hareket tablolarındaki müşteri hesabının Genel Merkez müşteri yöneticisinde de bulunduğunu doğrular.
- **Satır sayısı**: Hareket başlığı tablosundan alındığı şekilde satır sayısının satış hareket tablolarındaki satır sayısıyla eşleştiğini doğrular.
- **Fiyata vergi dahil**: **Fiyata vergi dahil** parametresinin hareket satırları arasında tutarlı olduğunu doğrular.
- **Brüt tutar**: Başlıktaki brüt tutarın, satırlardaki net tutarlar ile vergi tutarının toplamı olduğunu doğrular.
- **Net tutar**: Başlıktaki net tutarın, satırlardaki net tutarların toplamı olduğunu doğrular.
- **Eksik/Fazla ödeme**: Başlıktaki brüt tutar ile ödeme tutarı arasındaki farkın maksimum eksik ödeme/fazla ödeme yapılandırmasını aşmadığını doğrular.
- **İskonto tutarı**: İskonto tablolarındaki iskonto tutarının ve perakende hareket satırı tablolarındaki iskonto tutarının tutarlı olduğunu ve başlıktaki iskonto tutarının satırlardaki iskonto tutarlarının toplamı olduğunu doğrular.
- **Satır iskontosu**: Hareket satırındaki satır iskontosunun, iskonto tablosunda hareket satırına karşılık gelen tüm satırların toplamı olduğunu doğrular.
- **Hediye kartı maddesi**: Retail hediye kartı maddelerinin iadesini desteklemez. Ancak, bir hediye kartının bakiyesi nakde çevrilebilir. Nakde çevirme satırı yerine iade satırı olarak işlenen bir hediye kartı maddesi için ekstre deftere nakil işlemi başarısız olur. Hediye kartı maddeleri için doğrulama işlemi, perakende hareket tablolarındaki yalnızca hediye kartı satır maddelerinin hediye kartı nakde çevirme satırları olmasını sağlamaya yardımcı olur.
- **Negatif fiyat**: Negatif fiyat hareketi satırı olmadığını doğrular.
- **Madde ve Ürün Çeşidi**: Hareket satırlarındaki maddelerin ve ürün çeşitlerinin madde ve ürün çeşidi ana dosyasında bulunduğunu doğrular.

## <a name="set-up-the-consistency-checker"></a>Tutarlılık denetleyicisini ayarlama

**Perakende \> Perakende BT \> POS deftere nakil** bölümünde "Mağaza hareketlerini doğrula" toplu işlemini düzenli aralıklar için yapılandırın. Toplu iş, "Ekstreyi toplu olarak hesaplama" ve "Ekstreyi toplu olarak deftere nakletme" işlemlerinin ayarlanmasına benzer şekilde, mağaza organizasyon hiyerarşisine göre zamanlanabilir. Bu toplu işlemi günde birden fazla kez yürütülecek şekilde yapılandırmanızı ve her P işi uygulamasının sonunda çalıştırılacak şekilde zamanlamanızı öneririz.

## <a name="results-of-validation-process"></a>Doğrulama işleminin sonuçları

Toplu işlem tarafından gerçekleştirilen doğrulama denetlemesinin sonuçları, uygun perakende işlemde işaretlenir. Perakende işlem kaydındaki **Doğrulama durumu** alanı, ya **Başarılı** ya da **Hata** olarak ayarlanır ve son doğrulama çalıştırma tarihi, **Son doğrulama saati** alanında görünür.

Doğrulama hatası ile ilgili daha fazla hata açıklaması görmek için ilgili perakende mağaza işlem kaydını seçip **Doğrulama hataları** düğmesine tıklayın.

Doğrulama denetlemesinden geçemeyen işlemler ve henüz doğrulanmamış olan işlemler ekstrelere eklenmez. "Ekstre hesaplama" işlemi sırasında ekstreye eklenebilecek, ancak eklenmemiş olan işlemlerin olması durumunda kullanıcılar bilgilendirilir.

Bir doğrulama hatası bulunursa hatayı düzeltmenin tek yolu, Microsoft Desteği ile iletişime geçmektir. Bir sonraki sürümde kullanıcıların kullanıcı arabiriminde başarısız olan kayıtları düzeltmelerine olanak tanıyan özellik eklenecektir. Değişiklik geçmişini takip etmek için günlüğe kaydetme ve denetleme özellikleri de kullanıma sunulacaktır.

> [!NOTE]
> Bir sonraki sürümde daha fazla senaryoyu desteklemek için ek doğrulama kuralları da eklenecektir.