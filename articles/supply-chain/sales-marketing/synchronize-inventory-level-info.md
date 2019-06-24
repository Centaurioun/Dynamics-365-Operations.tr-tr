---
title: Stok düzeyi bilgisini Finance and Operations'tan Field Service'a eşitlemek
description: Bu konu stok düzey bilgisini Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535710"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Stok düzeyi bilgilerini Field Service'dan Finance and Operations'a eşitleme 

[!include[banner](../includes/banner.md)]

Bu konu stok düzey bilgisini Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve altındaki görevler, eldeki stok düzeylerini Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılır.

**Veri Tümleştirmesindeki Şablon**
- Ürün envanteri (Fin and Ops'tan Field Service'a)
  
**Veri tümleştirme projesindeki görev**
- Ürün stoku

Aşağıdaki eşitleme görevlerinin, stok düzeylerinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:
- Ambarlar (Fin and Ops'tan Field Service'a) 
- Stok birimli Field Service ürünleri (Fin and Ops'tan Sales'a) 

## <a name="entity-set"></a>Varlık kümesi

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS ambara göre eldeki stok     |

## <a name="entity-flow"></a>Varlık akışı
Finance and Operations'tan stok seviyesi bilgisi Field Service'a seçilen ürünler için gönderildi. Düzey Stok bilgileri şunları içerir: 
- Eldeki miktarı (geçerli kayıtlı fiziksel olarak ambarda miktar)
- Sipariş miktarı (toplam kaydedilen siparişindeki miktar - satış siparişleri gibi)
- Sipariş edilen toplam miktar (toplam kaydedilen sipariş tutarı - satınalma siparişleri gibi)

Bu bilgiler her ambar için serbest bırakılan ürün başına yakalanan ve stok düzeyini değiştiğinde, değişiklik izlemeyi dayalı eşitlenmiş.

Field Service servis düzeyleri ve Finance and Operations işlemleri eşleştirmek için düzeyin almak için delta Stok günlüklerini tümleştirme çözümü oluşturur.

Finance and Operations, stok düzeyleri için üst görevi görür. Bu nedenle Field Service'tan Finance and Operations'a iş emirleri, aktarmalar ve ayarlamalar için kurulum tümleştirmesi, bu özellik Field Service'ta Finance and Operations'tan stok düzeyleri eşitlemesi ile kullanılıyorsa, önemlidir.

Stok düzeylerinin Finance and Operations'tan üstlenildiği ürünler ve ambarlar, Gelişmiş Sorgu ve Filtreleme (Power Query) ile kontrol edilebilir.

> [!NOTE]
> Field Services'ta birden fazla ambar (**Harici Korunan = Hayır**) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür. Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri yalnızca Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır. Bu durumda, Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır. Daha fazla bilgi için bkz. [Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
**Harici ürün stoku** varlığı yalnızca arka uç tümleştirmesinde kullanılır. Finance and Operations ve stok düzeyi değerlerinin birleştirilmesinde alır ve daha sonra bu ambarı stok ürünler sonra değişen Manuel Stok günlüklerini değerlere dönüştürür.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="data-integration"></a>Veri tümleştirmesi
Projenin çalışması için, Tümleştirme anahtarının msdynce_externalproductinventories için güncelleştirilmiş olduğundan emin olmanız gerekir.
1.  **Veri tümleştirmesi > Bağlantı kümeleri**'ne gidin.
2.  Kullanılan Bağlantı kümesini seçin.
3.  **Tümleştirme anahtarı** sekmesinde, aşağıdaki anahtarların msdynce_externalproductinventories öğesine eklendiğinden emin olun:
      - msdynce_productnumber (Ürün Numarası)
      - msdynce_warehouseid (Ambar Kodu)
      
### <a name="data-integration-project"></a>Veri tümleştirme projesi
Gelişmiş Sorgu ve Filtreleme ile filtreler uygulayabilirsiniz, böylece yalnızca istenilen ürünler ve ambarlar stok düzeyi bilgisine Finance and Operations'tan Field Service'a gönderilir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>Ürün stoku (Fin and Ops'tan Field Service'a): Ürün stoku

[![Veri tümleştirmede şablon eşleme](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)