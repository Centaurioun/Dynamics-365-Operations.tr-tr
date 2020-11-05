---
title: Otomatik satıcı faturalama işlemlerine genel bakış
description: Bu konu, otomatik bir işlem kullanmanın yararlarını ve satıcı fatura işlemeyi otomatikleştirme yeteneğini açıklamaktadır.
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 187b3c4f1a8b2c9ec6df95c19b261756ec4562dc
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3905039"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Otomatik satıcı faturalama işlemlerine genel bakış

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konu, otomatik bir işlem kullanmanın yararlarını ve satıcı fatura işlemeyi otomatikleştirme yeteneğini açıklamaktadır. Bu yetenek, Özellik yönetiminde etkinleştirilmiş olan özelliklerden oluşur. Bu özellikler, **Fatura günlüğü** veya **Fatura kayıt günlüğü** sayfası aracılığıyla işlenen faturalara değil, yalnızca satıcı faturalarına uygulanır.

Çoğu durumda, kuruluşlar kağıt faturaların optik karakter tanıma (OCR) servis sağlayıcısı kullanılarak işlenmesi için üçüncü taraflarla birlikte çalışırlar. Servis sağlayıcı makine tarafından okunabilen fatura meta verilerini döndürür. Otomasyona yardımcı olmak amacıyla Borç hesapları otomasyon özellikleri, bu yapıları Borç hesaplarından kullanmanıza olanak tanır.

Bazı Borç hesapları satıcı faturalama işlemlerini otomatikleştirebilirsiniz. Bu işlemler içe aktarılan satıcı faturalarını iş akışı sistemine göndermeyi ve deftere nakledilen ürün giriş satırlarını bekleyen satıcı fatura satırlarına eşleştirmeyi içerir. Otomatik işlem, bir satıcı faturasının ilerlemesi hakkında bilgileri fatura her bir işlemde hareket ederken gösterir. Bu yetenek, Borç hesapları görevlileri ve yöneticilerinin satıcı faturalarını daha etkili şekilde işlemesine yardımcı olabilir. Ayrıca, bilginin el ile girildiği ve işlendiği durumlarda oluşabilecek hataları ve verimsizliği azaltmaya da yardımcı olur.

Otomasyon süreçleri, bu görevleri gerçekleştirmek için kullanılabilir:

- İçe aktarılan faturaları otomatik olarak iş akışı sistemine gönderme.
- Ürün girişlerini bekleyen satıcı faturası satırlarıyla eşleştirme.
- Satıcı faturası deftere nakledilmeden önce deftere nakil benzetimi yapma.
- İş akışı geçmişini hızlı ve etkili şekilde görüntüleme.
- Satıcı faturası işlemeyi otomatikleştirme sonuçlarını görüntüleme ve inceleme.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Satıcı faturası otomasyonu – İçe aktarılan satıcı faturalarını iş akışı sistemine gönderme

Temassız Borç hesapları faturalama işleminin bir parçası olarak, sistemin içe aktarılan bir faturayı iş akışı sistemine otomatik olarak göndermesini sağlayabilirsiniz. Bu işlem arka planda, belirttiğiniz bir sıklıkta (saatlik veya günlük) çalışacaktır. İçe aktarılan faturaları otomatik olarak iş akışı sistemine gönderme yeteneği, işleminizin içe aktarılan bir faturayla başlamasını gerektirir. Faturanın el ile müdahale olmadan başlangıçtan bitişe kadar işlendiğinden emin olmak için, iş akışı yapılandırmasına otomatik deftere nakil görevinin dahil edilmesi gerekir.

Satınalma siparişleri (PO'lar) ile ilgili faturalar ve PO dışı tedarik kategorisi ve stoklanmayan satırlar içeren faturalar, otomatik olarak iş akışı sistemine gönderilebilir. El ile girilen faturalar ve **Satıcı işbirliği faturalama** çalışma alanı aracılığıyla oluşturulan faturalar iş akışı sistemine el ile gönderilmelidir.

Otomasyon özelliği, içe aktarılan satıcı faturalarını iş akışı sistemine göndermek için şirkete özgü kurallar tanımlamanıza ve deftere nakledilen ürün giriş satırlarını bekleyen satıcı fatura satırlarına eşleştirmenize olanak sağlayan esnek bir çerçeve sağlar.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Satıcı faturası otomasyonu – Ürün girişlerini üç yönlü eşleştirme ilkesine sahip fatura satırlarıyla eşleştirme

Sistem, deftere nakledilen ürün girişlerini, üç yönlü eşleştirme ilkesi için tanımlanmış olan fatura satırlarına otomatik olarak eşleştirebilir. İşlem, eşlenen ürün giriş miktarı fatura miktarına eşit oluncaya kadar çalışacaktır. Bu işlemin bir parçası olarak, işlemin başarısız olması sonucuna varmadan önce, sistemin ürün girişlerini bir fatura satırıyla eşleştirmek için kaç kez deneme yapması gerektiğini belirtebilirsiniz. İşlem, saatlik ya da günlük olarak arka planda çalışacaktır. Otomatik eşleştirme sürecini, faturaları iş akışı sistemine gönderme sürecinin bir parçası olarak çalıştırabilirsiniz. Alternatif olarak, bunu bağımsız bir işlem olarak da çalıştırabilirsiniz.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Satıcı faturası otomasyonu – Satıcı faturası deftere naklini önceden doğrula

Deftere nakil benzetimi, satıcı faturalarının deftere nakil işlemi sırasında yapılan doğrulama adımlarını tamamlar, ancak hiçbir hesap güncelleştirilmez. Bu işlemi çalıştırmak için, **Bekleyen satıcı faturaları** sayfasında tek bir fatura veya birden fazla fatura seçebilirsiniz.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Satıcı faturası otomasyonu – Satıcı faturaları için iş akışı geçmiş bilgilerini görüntüleme için geliştirilmiş deneyim

Satıcı faturası iş akışı geçmişiyle ilgili kolay okunabilir bir görünüm sağlanmıştır. Satıcı faturası iş akışı geçmişine doğrudan satıcı faturasından erişilebilir. Bu nedenle, bu bilgileri bulmak için daha az tıklama gerekir.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Satıcı faturası otomasyonu – Analizler ve ölçümler

**Satıcı fatura girişi** çalışma alanı, otomatik işlem aracılığıyla bunu yapmamış olan satıcı faturalarına odaklanmanızı sağlar. Çalışma alanı üzerindeki kutucuklar iş akışı sistemine başarıyla gönderilmemiş, içe aktarılan veya ürün girişleriyle eşleştirilemeyen satıcı faturaları hakkındaki bilgileri listeler. Microsoft Power BI ölçümleri ayrıca, satıcı fatura otomasyonunun verimlilkleri için Borç hesapları yöneticilerine içgörü sunmak amacıyla da sağlanır.