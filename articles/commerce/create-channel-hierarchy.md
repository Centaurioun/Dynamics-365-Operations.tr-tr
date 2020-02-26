---
title: Kanal gezinme hiyerarşisi oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002048"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Kanal gezinme hiyerarşisi oluşturma


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Kanal gezinme hiyerarşisi, ürünleri gruplandırıp kategoriler halinde düzenleyerek ürünlere çevrimiçi veya satış noktasında (POS) göz atılabilmesi için kullanılır.

## <a name="create-a-channel-navigation-hierarchy"></a>Kanal gezinme hiyerarşisi oluşturma

Kanal gezinti hiyerarşisi oluşturmak için aşağıdaki adımları izleyin.

1. Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Kanal gezinme kategorileri**'ne gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ad** kutusuna bir ad girin.
1. **Açıklama** kutusuna bir açıklama girin.
1. **Oluştur**'u seçin.
1. Eylem bölmesinde, kök düğüm oluşturmak için **Yeni kategori düğümü**'nü seçin.
1. **Ad** kutusuna bir ad girin.
1. **Açıklama** kutusuna bir açıklama girin.
1. **Kolay ad** kutusuna bir kolay ad girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde örnek bir kök düğüm gösteriliyor.

![Örnek kök düğüm](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Gezinme kategorisi düğümleri oluşturma

Kanaldaki ürün kategorilerini temsil edecek ek gezinme kategorisi düğümleri oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde, kategori eklenecek ana düğümü seçin.
1. Eylem bölmesinde **Yeni kategori düğümü**'nü seçin.
1. **Ad** kutusuna bir ad girin.
1. **Açıklama** kutusuna bir açıklama girin.
1. **Kolay ad** kutusuna bir kolay ad girin.
1. **Görüntüleme sırası** kutusuna bir görüntüleme sırası girin (isteğe bağlı).
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde, tamamlanmış kanal gezinme hiyerarşisinin bir örneği gösteriliyor.

![Örnek kanal hiyerarşisi](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Kategori düğümlerine ürünler ekleme

Kategori düğümlerine ürünler eklemek için bu adımları izleyin.

1. Bir kategori düğümü seçin.
1. **Ürünler** altında, **Ekle**'yi seçin.
1. Ürün numarası veya ürün adı kullanarak eklemek istediğiniz yeni ürünü veya ürünleri bulun ve **Tamam**'ı seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

> [!NOTE]
> Kanal gezinme hiyerarşisi içinde bir düğüme ürünlerin eklenmesi, ürünlerin seçili bir kanalda görünmesi için yeterli değildir; ürünlerin bir ürünle ilişkili olması da gereklidir.

Aşağıdaki resimde, ürünler eklenmiş bir düğüm örneği gösteriliyor.

![Kategori düğümüne ürünler ekleme](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Kategori düğümlerine ürün öznitelik grupları ekleme

> [!NOTE]
> Öznitelik gruplarını kanal gezinme hiyerarşisinin içindeki bir düğüme ekleyebilmeniz için önce bu grupların oluşturulması gerekir.

Kategori düğümüne ürün öznitelik grubu eklemek için bu adımları izleyin.

1. Bir kategori düğümü seçin.
1. **Ürün öznitelik grubu** altında, **Ekle**'yi seçin.
1. Eklemek istediğiniz öznitelik grubunu veya gruplarını bulun ve **Tamam**'ı seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde, ürün öznitelik grupları eklenmiş bir düğüm örneği gösteriliyor.

![Düğümdeki ürün öznitelik grupları](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün çeşitlerini ayarlama](set-up-assortments.md)

[Öznitelikleri ve öznitelik gruplarını yönetme](attribute-attributegroups-lifecycle.md)