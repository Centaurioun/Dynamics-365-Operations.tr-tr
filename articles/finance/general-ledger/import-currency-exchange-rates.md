---
title: Para birimi döviz kurlarını içe aktarma
description: Bu konu, döviz kuru sağlayıcıları tarafından yayımlanan yabancı döviz referans oranlarını içe aktarma gereksinimleri hakkında bilgi sağlar.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6684a1ef041d624d6bfe80337c4db0913f0ca066
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3013152"
---
# <a name="import-currency-exchange-rates"></a>Para birimi döviz kurlarını içe aktarma

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

Bir tüzel kişilik, yabancı para birimlerinde faturalar almışsa, yabancı para birimini yerel para birimine dönüştürmek gereklidir. Başka bir deyişle, farklı para birimlerinin döviz kurlarının güncel olması gereklidir. Bu konu, Avrupa Merkez Bankası ve Rusya Merkez Bankası gibi döviz kuru sağlayıcıları tarafından İnternet üzerinden yayınlanan önemli yabancı referans döviz kurlarını içe aktarmak için gerekli ayarlar ve işlemler hakkında genel bir bakış sağlar.

Aşağıdaki bölümler, yabancı döviz kurlarının içe aktarılmasında kullanılan bilgi akışının ayarlanması ve işlenmesini açıklar.

## <a name="configure-an-exchange-rate-provider"></a>Bir döviz kuru sağlayıcısı yapılandırma
Döviz kurlarını almadan önce, döviz kurlarını sunan sağlayıcılar tarafından gerek duyulan bilgileri ayarlamanız gerekir. **Döviz kuru sağlayıcılarını yapılandır** sayfasını kullanarak döviz kuru sağlayıcılarını seçin. Bazı döviz kuru sağlayıcıları Dynamics 365 Finance içerisindeki örnek veride bulunmaktadır. Aşağıdaki tabloda bu sayfadaki kontrollerle ilgili açıklamalar bulunur.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alan** | **Açıklama**                                                                                                                                                                                                             |
| **Ad**  | Döviz kuru sağlayıcının adı.                                                                                                                                                                                     |
| **Anahtar**   | Sağlayıcının istediği yapılandırma bilgilerinin her parçası için benzersiz kimlik. Her döviz kuru sağlayıcı ekleyişinizde bu bilgiler otomatik olarak eklenir. |
| **Value** | Her bir anahtar için bilgi. Her döviz kuru sağlayıcı ekleyişinizde bu bilgiler eklenir.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Para birimi döviz kurlarını içe aktarma
Döviz kurlarını, döviz kurları sağlayıcı kaynağından alabilirsiniz ve onları **Para birimi döviz kurları** sayfasında ekleyebilirsiniz. Döviz kurlarını içe aktarmak için **Para birimi döviz kurlarını alma** sayfasını kullanın. Aşağıdaki tablo, alma işlemini başarıyla tamamlamak için gerekli alanların açıklamalarını sağlar.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alan**                              | **Açıklama**                                                                                                                                                                                                                                                                                                                                                             |
| **Döviz kuru türü**                 | Bir döviz kuru tipi.                                                                                                                                                                                                                                                                                                                                                      |
| **Döviz kuru sağlayıcı**             | Bir döviz kuru sağlayıcısı.                                                                                                                                                                                                                                                                                                                                                  |
| **Şu tarihten itibaren içe aktar:**                       | Bu parametre, geçerli tarihten itibaren veya belirli bir tarih aralığı için almayı yönetir. Bir tarih aralığı kullanmak istiyorsanız, başlangıç ve bitiş tarihlerini seçin.                                                                                                                                                                                                                |
| **Gerekli para birimi çiftlerini oluştur**    | Bu onay kutusu, içe aktarılan para birimi çiftleri mevcut değilse, para birimi çiftlerinin otomatik olarak oluşturulmasını yönetir. Bu seçenek bazı sağlayıcılar için kullanılabilir olmayabilir.                                                                                                                                                                                               |
| **Mevcut döviz kurlarını geçersiz kıl**   | Bu onay kutusu, bir para birimi çifti için mevcut döviz kurunun güncelleştirilmesini yönetir, döviz kuru belirli bir tarih için halihazırda mevcutsa. Bu onay kutusunu seçmezseniz, belirli bir tarih için döviz kuru, başka bir döviz kuru halihazırda mevcutsa, içe aktarılmaz.                                                                                       |
| **Resmi tatilde içe aktarmayı önle** | Bu onay kutusu, resmi bir tatil olan bir tarih için döviz kurunu içe almayı yönetir. Örneğin, bu onay kutusunu seçerseniz ve Avrupa Merkez Bankası'nı döviz kur sağlayıcısı olarak kullanırsanız, sistem, geçerli tüzel kişilik ile ilgili bir resmi tatilde döviz kurunu güncelleştirmez. Bu seçenek bazı sağlayıcılar için kullanılabilir olmayabilir. |
| **Önceki günün kuru** | **Özellik yönetimi** sayfasında **geçerli veya önceki tarih özelliğinde ECB içe aktarmayı** etkinleştirirseniz bu onay kutusu kullanılabilir. Bu onay kutusu yalnızca *Avrupa Merkez Bankası* için kullanılabilir. Bir önceki çalışma gününde yaklaşık 16:00'da (CET) Avrupa Merkezi Bankası tarafından yayımlanan para birimi döviz kurunu içe aktarmak için bu onay kutusunu seçin. Varsayılan olarak bu onay kutusu seçilidir. Aynı çalışma gününde yayınlanmış para birimi döviz kurunu içe aktarmak için bu onay kutusunu temizleyin.  |