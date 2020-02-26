---
title: Müşteriye serbest metin faturası şablonu atama
description: Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c64a00a839522ea14fc5fcdaca08ab17748f894
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000036"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Müşteriye serbest metin faturası şablonu atama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir. USMF demo şirketinin kullanıldığı bu görev, alacak hesapları faturalarının yönetiminden ve işlenmesinden sorumlu kullanıcılara yöneliktir.

1. **Gezinti bölmesinde** **Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. **Eylem Bölmesinde** **Fatura** öğesine tıklayın.
4. **Yinelenen faturalar**'a tıklayın. Müşterilere serbest metin faturası şablonları atamak ve faturaların müşterilere ne sıklıkta gönderileceğini belirlemek için bu sayfayı kullanın.  
5. Müşteriye yeni şablon atamak için **Yeni**'ye tıklayın.
6. **Şablon** alanında müşteriye atamak istediğiniz serbest metin faturası şablonunu seçin.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Faturalama başlangıç tarihi** alanına, ilk faturanın oluşturulacağı tarihi girin.
10. **Yinelenme sonu** bölümüne, yinelenen bir bitiş tarihi girin.  
    * Şunlardan birini seçin: Bitiş tarihi yok – Faturalar sonsuz olarak oluşturulur ve şablon müşteri hesabından kaldırılana kadar geçerli kalır.
    * Faturalama bitiş tarihi – Bu seçeneği belirtin ve faturanın oluşturulabileceği son tarihi girin.  
11. **Maksimum toplam tutar** alanına, fatura oluşturma işleminin durdurulacağı maksimum toplam tutarı girin. Seçili şablon kullanarak erişilebilen maksimum toplam tutarı girin. Örneğin 1000,00 girer ve her biri 100,00 tutarında aylık faturalar oluşturursanız, onuncu fatura oluşturulduktan sonra fatura oluşturma süreci sona erer.  
12. **Alınan varsayılan değerleri kullanarak yinelenen faturalar oluştur** bölümünde serbest metin faturası şablonunu veya müşteri hesabını seçin. Faturaları oluştururken dil, deftere nakil profili, satış vergisi grubu, madde satış vergisi grubu, liste kodu, teslimat ülkesi/bölgesi, ödeme koşulları, para birimi, ödeme koşulları, ödeme yöntemi, ödeme belirtimi, ödeme planı, nakit iskontosu, mali boyutlar ve havale makbuzu için varsayılan değerleri belirlemek üzere serbest metin faturası şablonunu veya müşteri hesabını kullanın.  
13. **Yineleme modeli** alanında yinelenme modelini seçin.
    + Günlük – Bu seçeneği belirtin ve Dönem alanına gün sayısını girin. Örneğin 15 girerseniz, bu müşteri için 15 günde bir fatura oluşturulur.
    + Haftalık – Bu seçeneği belirtin Dönem alanına hafta sayısını girin. Örneğin 2 girerseniz, bu müşteri için 2 haftada bir fatura oluşturulur.
    + Aylık – Bu seçeneği belirtin ve Dönem alanına ay sayısını girin. Örneğin 6 girerseniz, bu müşteri için her altı ayda bir fatura oluşturulur.
    + Yıllık – Bu seçeneği belirtin ve Dönem alanına yıl sayısını girin. Örneğin 2 girerseniz, bu müşteri için her iki yılda bir fatura oluşturulur.  
14. **Dönem** alanına bir sayı girin.
