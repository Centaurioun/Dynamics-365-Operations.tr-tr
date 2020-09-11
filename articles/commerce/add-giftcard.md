---
title: Hediye kartı modülü
description: Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661254"
---
# <a name="gift-card-module"></a>Hediye kartı modülü

[!include [banner](includes/banner.md)]

Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Özet

Hediye kartları, genel bir ödeme biçimidir ve hediye kartı kabul etmek üzere ödeme modülünde bir hediye kartı modülü kullanılabilir. Hediye kartı modülü Dynamics 365, SVS ve Givex hediye kartlarını destekler. SVS ve Givex hediye kartları, Adyen ödeme sağlayıcısı aracılığıyla kullanılır.

SVS ve Givex gibi harici hediye kartları desteği hakkında daha fazla bilgi için bkz. [Harici hediye kartları için destek](./dev-itpro/gift-card.md)

Aşağıdaki resimde ödeme sayfasında kullanılan bir hediye kartı modülü örneği gösterilmektedir.

![Hediye kartı modülü örneği](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modül özellikleri

- **Ek alanları göster** - Bu özellik, her zaman varsayılan olarak görüntülenen hediye kartı numarasına ek olarak, hediye kartları için hangi alanların görüntüleneceğini tanımlar. Örneğin, bazı hediye kartları bir kişisel kimlik numarası (PIN) görüntülemeyi ve başka hediye kartları PIN ve son kullanma tarihini görüntülemeyi destekler. Alternatif olarak, bu özellik yalnızca hediye kartı numarasını görüntüleyebilen ve ek alanlar içermeyen "Hiçbiri" seçeneğine ayarlanabilir.

Desteklenen değerler:
-   PIN
-   Son kullanma tarihi
-   PIN ve son kullanma tarihi 
-   Hiçbiri

## <a name="site-settings-for-gift-card-modules"></a>Hediye kartı modülleri için site ayarları

Commerce site oluşturucuda **Site Ayarları \> Uzantılar**altında, **Desteklenen hediye kartı türü** adında bir hediye kartı modülü ayarı vardır. Bu ayar üç değeri destekler:
- **Dynamics 365 hediye kartı** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Dynamics 365 hediye kartlarının kullanılmasına izin verir. Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.
- **SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Givex ve SVS hediye kartlarının kullanılmasına izin verir. Bu ayar e-Ticaret sitesindeki oturum açmış ve anonim kullanıcılar için desteklenir.
- **Dynamics 365, SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü Dynamics 365, Givex ve SVS hediye kartlarının kullanılmasına izin verir. Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.

## <a name="add-a-gift-card-module-to-a-page"></a>Sayfaya hediye kartı modülü ekleme

Bir ödeme sayfasına hediye kartı modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Harici hediye kartları için destek](./dev-itpro/gift-card.md)