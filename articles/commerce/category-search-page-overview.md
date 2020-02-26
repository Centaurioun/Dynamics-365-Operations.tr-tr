---
title: Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış
description: Bu konu, Dynamics 365 Commerce'te varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış sağlar.
author: v-chgri
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 17746d2923ab84311253c47647c0020807bdb75c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002508"
---
# <a name="overview-of-default-category-landing-page-and-search-results-page"></a>Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce e-Ticaret'te varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış sağlar.

## <a name="default-category-landing-page"></a>Varsyılan kategori açılış sayfası

Varsayılan kategori giriş sayfası, Web sitesi kullanıcılarının gezinti hiyerarşisinde bir kategori seçdiklerinde aldığı bir sayfa. Kategori sayfası gözatmanıza olanak tanır ve ayrıca kategorilere ayrılmış ürünleri sıralayabilir ve bunları iyileştirebilirsiniz.

![Varsyılan kategori açılış sayfası](./media/SimpleCategoryLandingDressCategory.png)

Sayfanın üst bölümünde, ticaret yöneticisinin kategorilere ayrılmış tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır. Konfigürasyon, kanal gezinme hiyerarşisinin konfigürasyonunun bir parçası olarak gerçekleştirilir. Sayfanın alt bölümünde, bir alışverişçinin ilgilenebileceği çeşitli konularda hızlı bağlantılar içeren bir altbilgi yer almaktadır.

Kategori için aşağıdaki bileşenler gereklidir:

- **Ürün yerleştirme döşemeleri**, ticaret yöneticisinin, gezinti hiyerarşisi konfigürasyonunun bir parçası olarak bir kategoride tanımladığı ürünleri gösterir.
- **İyileştiriciler ve seçim özeti**, sayıları sağlayan ve öğeleri iyileştirmek için kullanılabilecek filtrelerdir. Ticaret yöneticisi, kanal kategorileri ve ürün öznitelikleriyle ilgili meta verilerin konfigürasyonunun bir parçası olarak bunları yapılandırır.
- **Sıralama seçenekleri**, Web sitesi ziyaretçileri tarafından ürünleri sıralamak amacıyla kullanılır. Varsayılan olarak aşağıdaki sıralama seçenekleri kullanılabilir:

    - Fiyat: düşükten yükseğe
    - Fiyat: yüksekten düşüğe
    - Ürün adı - \[A-Z\]
    - Ürün adı - \[Z-A\]
    - Puanlar - düşükten yükseğe
    - Puanlar - yüksekten düşüğe

- **Sayfalandırma**, web sitesi ziyaretçileri, kategorilere ayrılmış bir ürün sonuçları sayfasından başka bir sayfaya gitmesini sağlar.
- **Toplam sayı**, bir kategoride tanımlanan toplam ürün sayısını sağlar.

## <a name="enrich-a-category-landing-page"></a>Kategori açılış sayfasını zenginleştirme

Kategori giriş sayfasının belirli bir kategori için daha özel bir deneyim olmasını istiyorsanız, o kategori için kategori giriş sayfasını "zenginleştirebilirsiniz". Örneğin, alışverişçinin dikkatini çekmek için pazarlama videosu ve bazı kategori öykülerinde bir hikaye ekleyebilirsiniz. Daha fazla bilgi için bkz. [Kategori giriş sayfasını zenginleştirme](enrich-category-page.md).

![Zenginleştirilmiş kategori açılış sayfası](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Otomatik önerme ve arama sonuçları sayfaları

Web sitesi kullanıcıları, gezinti hiyerarşisindeki bir kategoriye giderek veya arama alanına bir arama terimi girerek siteyi keşfeden bulabilir.

Kullanıcılar arama alanını yazma işlemi başladığında, arama terimlerini öneren derinlikli otomatik önerme işleviyle karşılaşır.

Aşağıda, gösterilebilecek öneri türleri yer verilmektedir:

- **Anahtar sözcükler**, kanala göre sıralanan tüm ürünlerin içinde öğe bulmak için kullanılır.
- **Ürünler**, ürün ayrıntıları sayfasına doğrudan bağlantılar sağlar.
- **Kapsamlı kategori arama önerileri**, çeşitli kategorileri listeler ve kullanıcıların anahtar sözcüğü belirli bir kategoride aramasını sağlar.

![Derinlikli otomatik önerme](./media/ImmersiveAutoSuggestUX.png)

Kullanıcılar anahtar sözcük veya kapsamlı kategori arama önerinden birini seçtiklerinde veya girdikleri arama terimi için hiçbir öneri olmadığında, bunlar arama sonuçları sayfasına yönlendirilir. Kullanıcılar daha sonra, istenen maddeyi bulmak için arama sonuçları listesine göz atabilir, sıralayabilir ve belirginleştirebilirsiniz.

![Arama giriş sayfası](./media/SearchLanding.png)

Arama sonuçları sayfası için aşağıdaki bileşenler gereklidir:

- **Ürün yerleştirme döşemeleri** kullanıcının araması için ürünleri gösterir. Varsayılan olarak, bu döşemeler kullanıcı aramasının bulut destekli arama puanı tarafından sıralanır.
- **İyileştiriciler ve seçim özeti**, sayıları sağlayan ve öğeleri iyileştirmek için kullanılabilecek filtrelerdir. Ticaret yöneticisi, kanal kategorileri ve ürün öznitelikleriyle ilgili meta verilerin konfigürasyonunun bir parçası olarak bunları yapılandırır.
- **Sıralama seçenekleri**, Web sitesi ziyaretçileri tarafından ürünleri sıralamak amacıyla kullanılır. Varsayılan olarak aşağıdaki sıralama seçenekleri kullanılabilir:

    - Fiyat: düşükten yükseğe
    - Fiyat: yüksekten düşüğe
    - Ürün adı - \[A-Z\]
    - Ürün adı - \[Z-A\]
    - Puanlar - düşükten yükseğe
    - Puanlar - yüksekten düşüğe
    - Varsayılan

- **Sayfalandırma**, web sitesi ziyaretçileri, kategorilere ayrılmış bir ürün sonuçları sayfasından başka bir sayfaya gitmesini sağlar.
- **Toplam sayı**, bir kategoride tanımlanan ve arama kriterlerine uyan toplam ürün sayısını sağlar.

## <a name="additional-resources"></a>Ek kaynaklar

[Giriş sayfasına genel bakış](quick-tour-home-page.md)

[Ürün ayrıntıları sayfalarına genel bakış](quick-tour-pdp.md)

[Sepet ve ödeme sayfalarına genel bakış](quick-tour-cart-checkout.md)

[Hesap yönetimi sayfalarına genel bakış](quick-tour-account-management.md)
