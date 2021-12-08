---
title: IoT Hub mesajları için şema biçimleri
description: Bu konu, IoT'de kullanabileceğiniz bir ileti şemasını nasıl tasarlayabileceğinizi açıklamaktadır.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b24a6e14182baa91299abad0da2987b2dca92601
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781624"
---
# <a name="schema-formats-for-iot-hub-messages"></a>IoT Hub mesajları için şema biçimleri

[!include [banner](../../includes/banner.md)]

Bu konu, IoT'de kullanabileceğiniz bir ileti şemasını nasıl tasarlayabileceğinizi açıklamaktadır.

## <a name="message-requirements"></a>İleti gereksinimleri

Aşağıdaki kurallar, IoT zekası içindeki iletilerin izlenmesi için geçerlidir:

+ İleti şemaları, JavaScript Nesne Gösterimi (JSON) biçiminde olmalıdır.
+ Değerin milisaniye (MS) olarak ifade edildiği bir UNIX **zaman damgası** özelliği, Microsoft Azure IoT Hub iletisinde bulunmalıdır.
+ Bir ileti yalnızca senaryo kurulumunda tanımlanan tüm özellikleri içeriyorsa izlenir. Örneğin, **kimlik**, **zaman damgası** ve **değer** özelliklerini tanımlarsanız, aşağıdaki ileti izlenir.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    **Değer** özelliği eksik olduğundan bu ileti izlenmez.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT Zekası, senaryo yapılandırmasında tanımlanmayan iletideki özellikleri yok sayar. Örneğin, **kimlik**, **zaman damgası** ve **değer** özelliklerini tanımlarsanız, IoT Zekası aşağıdaki tüm iletileri izler.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT Zekası, senaryo konfigürasyonu ölçütleriyle eşleşmeyen iletileri sessizce yok sayar.
+ Birden çok türde ileti şeması tanımlayabilir ve kullanabilirsiniz.
+ Her ileti şeması türünün tanımlanması gerekmez. Yalnızca IoT Zeka senaryoları için kullanılacak şemalar tanımlanmalıdır.

## <a name="id-value-pair-schema"></a>Kod değer çifti şeması

Bir kimlik değer çifti, IoT Zekası ileti şemaları için ortak bir desendir. Bir kimlik değer çifti kullanarak, ileti şemanızı tüm senaryolarda aynı olmasını güvence altına alırsınız. Örneğin, **Donatım kapalı kalma süresi** veya **Üretim gecikmeleri** senaryosu için bir ileti aşağıdadır.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Aşağıda, **Ürün kalitesi** senaryosu için bir ileti verilmiştir.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Yukarıdaki iletiler **kimlik** ve **değer** özelliklerini içerir. Senaryo kurulumu sırasında, **kimlik** değerleri **Sinyal Veri Değerleri** tablosunda eşlenebilir. **Donatım kapalı kalma** senaryosunda, **IoTInt.Machine1225.PartOut** değerini eşlersiniz. **Ürün kalitesi** senaryosunda, **IoTInt.Machine1225.Temperature** değerini eşlersiniz.

Daha fazla bilgi için bkz. [Azure IoT Hub Belgeleri](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]