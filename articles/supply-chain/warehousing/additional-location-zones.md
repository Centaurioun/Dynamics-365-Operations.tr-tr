---
title: Ek yerleşim bölgeleri
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'a eklenen yeni bölge bölgelerinin genel görünümünü sağlar .
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c0bed8c95760b3dee350048c5f824f974b784f26
ms.sourcegitcommit: 7b7cc93c0f78c6bfc7a3ea66a74a29ba0f218553
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/04/2020
ms.locfileid: "3658346"
---
# <a name="additional-location-zones"></a>Ek yerleşim bölgeleri

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'ta üç yeni bölge alanı vardır. Ambar yöneticileri bunları ek ambar kuruluşları veya mizanpajları tanımlamak için kullanabilirler. Yeni bölge alanları el ile veya **konum kurulum** Sihirbazı kullanılarak ayarlanabilir. Bunlar, konumlar tablosunu kullanan herhangi bir sorgu veya filtre uygulama içinde kullanılabilirler.

Bölge alanlarını kullanmak için ek bir kurulum gerekmez.

## <a name="turn-on-the-additional-location-zone-feature"></a>Ek konum dilimi özelliğini aç

*İlave konum bölgesi* özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ek konum bölgesi aç*

## <a name="use-location-zones"></a>Yerleşim bölgelerini kullan

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum kurulum sihirbazı**'na gidin.
2. Aşağıdaki değerleri ayarlayın:

    - **Ambar** alanında _62_'i seçin.
    - **Bölge kodu** alanında _ZEMİN_'i seçin.
    - **İlave Bölge 1** alanında _PICKZONE1_'i seçin.
    - **İlave Bölge 2** alanında _WEBSHOP1_'i seçin.
    - **Konum profil kimliği** alanında _ZEMİN_'i seçin.

3. **Zemin** satırını seçin.
4. **Gönderen numarası** alanına _1_ girin. **Kime numarası** alanına _3_ girin.
5. **Koridor** satırını seçin.
6. **Gönderen numarası** alanına _1_ girin. **Kime numarası** alanına _5_ girin.
7. **Oluştur**'u seçin.
8. Yeni konumların eklendiğini bildiren iletiler alırsınız. İletileri görüntülemek için **iletileri göster** düğmesini seçin.
9. **Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin. Yeni konumlar listede görünür ve tüm bölge alanları (yani, varolan bölge alanı ve yeni ek bölge alanları) kullanılabilir.