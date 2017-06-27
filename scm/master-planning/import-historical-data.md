---
title: "Talep tahminleri için geçmiş verisini içe aktar"
description: "Doğru talep tahminleri elde etmek için madde veya madde tahsisat anahtarı başına tarihsel talep verisine ihtiyaç duyarsınız. Bu konu herhangi bir sistemden geçmiş verisini almak için veri varlıklarının nasıl kullanılacağını ve böylece daha uzun talep tahmin verisine nasıl sahip olacağınızı açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>Talep tahminleri için geçmiş verisini içe aktar

[!include[banner](../includes/banner.md)]

Talep tahminlerinin doğruluğunu garanti etmeye yardımcı olmak için, madde veya madde tahsisat anahtarı başına mümkün olduğunca fazla geçmiş talep verisine sahip olmalısınız. Geçmiş talep verisi halihazırda içe aktarılmamışsa, içe aktarmak için **Geçmiş harici talep** (ReqDemPlanHistoricalExternalDemandEntity) veri varlığını Microsoft Dynamics 365 for Operations içinde kullanın.

**Veri yönetimi** çalışma alanı içerisinde, varlık içerisindeki tüm alanların bir genel görünümünü görürsünüz.

1. **Veri yönetimi** çalışma alanını açın.
2. **Veri varlıkları** kutucuğuna tıklayın.
3. Varlık listesinde **Geçmiş harici talep** arayın.
4. **Hedef alanları** üzerine tıklayın. Aşağıdaki varlık alanları zorunludur: site (**DeliveringSiteId**), tarih (**DemandDate**), miktar (**DemandQuantity**), ve madde numarası (**ItemNumber**) veya madde tahsisat anahtarı (**ProductAllocationKeyId**).

Varlık verisini kullanmak için geçmiş talep verisini içeren Microsoft Excel dosyası veya virgülle ayrılmış değerler (CSV) dosyasına sahip olmalısınız. Aşağıdaki örnek, verinin bir CSV dosyasından nasıl alınacağını gösterir.

## <a name="example"></a>Örnek

Aşağıdaki dosyayı bir örnek olarak kullanabilirsiniz. [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) karşıdan yükleyin. Bu dosya, madde D0001 için geçmiş talep verisini içerir. Yalnızca aşağıdaki zorunlu alanları içerir: site, miktar ve talep tarihi.

1. Geçmiş talep verisinin aktarılacağı şirketi seçin.
2. **Veri yönetimi** çalışma alanını açın.
3. **İçe aktar** kutusunu tıklatın.
4. İçe aktarma projesi için bir ad seçin, örneğin **Madde D0001 için geçmiş talep verisi içe aktar**.
5. **Kaynak veri biçimi** alanında, içe aktardığınız dosyanın dosya formatını seçin. Bu örnek için HistoricalDemandData dosyasını içe aktarmak için, **CSV** seçeneğini işaretleyin.
6. **Varlık adı** alanında, **Geçmiş harici talep** seçeneğini işaretleyin.
7. Dosyayı bilgisayarınıza kaydedin ve sonra karşıya yükleyin.
8. **İçe aktar**'ı tıklatın.
9. **Yürütme özeti** sayfası otomatik olarak açılır. İçe aktarılan veriyi sayfada doğrulayın.

Geçmiş talep verisini içe aktardıktan sonra talep tahminleri oluşturabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

[İstatistiksel temel tahmin oluşturma](generate-statistical-baseline-forecast.md)
