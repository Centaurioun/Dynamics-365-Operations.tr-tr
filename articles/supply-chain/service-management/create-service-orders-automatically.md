---
title: Servis siparişlerini otomatik olarak oluşturma
description: Bir servis sözleşmesi veya birden fazla servis sözleşmesi için servis siparişleri oluşturabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee68190b117b974ff4131f5d2237d138cac1fda3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552288"
---
# <a name="create-service-orders-automatically"></a>Servis siparişlerini otomatik olarak oluşturma    

[!include [banner](../includes/banner.md)]


Bir servis sözleşmesi veya birden fazla servis sözleşmesi için servis siparişleri oluşturabilirsiniz. Oluşturulduklarında, servis siparişlerinizi **Servis siparişleri** formunda görüntüleyebilirsiniz.

Servis siparişleri servis anlaşmasının geçerli periyodu için oluşturulur. **Servis siparişleri oluştur** formunda belirttiğiniz aralık servis sözleşmesinin başlangıç tarihinden önce veya bitiş tarihinden sonraysa, servis siparişleri yalnızca aralığın servis sözleşmesinin süresi içinde yer alan parçası için oluşturulur.

Servis siparişlerini el ile veya servis sözleşmesi satırından otomatik olarak oluşturduğunuzda, satırda bir bitiş tarihi belirlemediyseniz, servis siparişi satırın başlangıç ve bitiş tarihleri tarafından tanımlanan zaman aralığı içinde olmalıdır.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Servis anlaşması için otomatik olarak servis siparişleri oluşturma

1.  **Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.

2.  Bir servis anlaşması seçin.

3.  **Teslim et** sekmesine ve ardından **Planlanan servis siparişleri**'ne tıklayın.

4.  Servis dönemini tanımlamak için tarihleri **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında belirtin.

5.  Oluşturulan servis siparişleri listesini göstermek için **Bilgi Günlüğünü Göster** onay kutusunu işaretleyin.

6.  **Hareket türlerini dahil et** alan grubunda hareket türlerini seçin. Hareket türleri, servis anlaşmasında oluşturulan satırları temsil eder ve seçtiğiniz her hareket türü, servis anlaşması satırında belirttiğiniz servis aralığına bağlı olarak çeşitli servis siparişleri oluşturur.

7.  Sürekli bir servis siparişleri serisinde eksik olan servis siparişlerini oluşturmak için **Sürekli** onay kutusunu işaretleyin.

8.  **Tamam** seçeneğini tıklatın.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Servis anlaşması için otomatik olarak çeşitli servis siparişleri oluşturma

1.  **Servis yönetimi** \> **Periyodik** \> **Servis siparişleri** \> **Servis siparişleri oluştur**'a tıklayın.

2.  Servis siparişleri oluştururken kullanmak amacıyla ölçüt eklemek veya kaldırmak üzere seçim yapmak **Seç**'e tıklayın.

3.  **Tamam** seçeneğini tıklatın.

## <a name="see-also"></a>Ayrıca bkz.

[Servis emirleri](service-orders.md)

[Servis siparişlerini otomatik oluşturma](auto-create-service-orders.md)

  

