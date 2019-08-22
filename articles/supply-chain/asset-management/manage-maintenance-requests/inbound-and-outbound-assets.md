---
title: Gelen ve giden varlıklar
description: Bu konuda Varlık Yönetimi'nde gelen ve giden varlıkları kaydetme açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847563"
---
# <a name="inbound-and-outbound-assets"></a>Gelen ve giden varlıklar

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Şirketiniz başka yerlerden veya müşterilerden alınan varlıklar üzerinde onarım işleri veya bakım işleri yapıyorsa, Varlık Yönetimi hem şirketinize giden gelen varlıkları hem de iade edilen varlıkları izleyebilir.

> [!NOTE]
> Gelen ve giden varlıkları yönetmek için gelen ve giden yaşam döngüsü durumlarını kullanmak istiyorsanız bu eylemleri desteklemek için bakım talebi yaşam döngüsü durumlarını ve yaşam döngüsü modellerini ayarlamanız gerekir. Daha fazla bilgi için bkz: [Bakım isteklerini kurma](../setup-for-maintenance-requests/requests.md).

Varlık Yönetimi kurulumu, gelen ve giden varlıklarla çalışabilir olup olmadığını belirler.

## <a name="register-assets-as-inbound"></a>Varlıkları gelen olarak kaydetme

1. **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.
2. Bakım talebini seçin.
3. **Bakım talebi durumunu güncelleştir**'i seçin.
4. **Gelen**'i (veya gelen varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.

![Şekil 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Gelen varlıkları alındı olarak kaydetme

1. **Varlık yönetimi** \> **Ortak** \> **Gelen/Giden** \> **Gelen varlıklar**'ı seçin.
2. Varlık veya bakım talebini seçin.
3. **Varlıkları al**'ı seçin.
4. **Alındı** alanında tarihi ve saati girin. Daha sonra **Tamam**'ı seçin. Kayıt, **Gelen varlıklar** listesi sayfasından kaldırılır.

![Şekil 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Varlıkları giden olarak kaydetme

Bakım veya onarım işini tamamladığınızda, varlığı iade edildiği gibi kaydedebilirsiniz.

1. **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.
2. Bakım talebini seçin.
3. **Bakım talebi durumunu güncelleştir**'i seçin.
4. **Giden**'i (veya giden varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.

## <a name="register-outbound-assets-as-delivered"></a>Giden varlıkları teslim edildi olarak kaydetme

1. **Varlık yönetimi** \> **Ortak** \> **Gelen/Giden** \> **Giden varlıklar**'ı seçin.
2. Varlık veya bakım talebini seçin.
3. Varlıkları **Teslim et**'i seçin.
4. **Teslim edildi** alanında tarihi ve saati girin. Daha sonra **Tamam**'ı seçin. Kayıt, **Giden varlıklar** listesi sayfasından kaldırılır.