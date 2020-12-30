---
title: Planlama İyileştirmesi ile stok işaretleme
description: Bu konuda, Planlama İyileştirmesi'ni kullandığınızda, kesinleştirilmiş siparişlerde stok işaretleme için kullanılabilir seçenekler hakkında bilgi sağlanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99a52c03e519384955d68d7101a7b73b7e9a7af6
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672213"
---
# <a name="inventory-marking-with-planning-optimization"></a>Planlama İyileştirmesi ile stok işaretleme

[!include [banner](../../includes/banner.md)]

Bu konuda, Planlama İyileştirmesi'ni kullandığınızda, kesinleştirilmiş siparişlerde stok işaretleme için kullanılabilir seçenekler hakkında bilgi sağlanmaktadır.

*İşaretleme*, arz ve talebi bağlamak için kullanılır. Master planlamanın talebin nasıl olmasını beklediğini gösteren bir *ilişkilendirmeye* benzerdir. Planlama açısından temel fark işaretlemenin ilişkilendirmeden daha kalıcı olmasıdır.

İşaretleme özelliği, ilk giren ilk çıkar (FIFO) ve son giren ilk çıkar (LIFO) yaklaşımları için özel maliyetlendirme senaryolarını desteklemek üzere sunulmuştur. Ancak, artık bazı maliyetlendirme dışı senaryolar için de kullanılmaktadır. Arz ve talep arasında işaretleme isteğe bağlıdır ve neredeyse kalıcıdır. İşaretleme kullanıcı tarafından el ile kaldırılabileceği gibi, **İşaretlemeyi kaldır** seçeneğinin belirlendiği bir satış siparişi satırı açılımı çalıştırılarak da kaldırılır.

İlişkilendirme, talebi gerekli arzla bağlamak için kapsama sırasında master planlama tarafından kontrol edilir. İlişkilendirme, her planlama çalışmasının talebi kapsaması gereken arzı iyileştirmesi için güncelleştirilebilir. Master planlama, ilişkilendirme bilgilerini güncelleştirdiğinde, var olan tüm işaretler korunur.

İlişkilendirme; ilgili işaret, eldeki rezervasyonlar ve siparişe ait rezervasyonları dahil ederek aşağıdaki sırada başlar:

1. Talep ve arz arasında işaretleme
1. Eldeki rezervasyonlar
1. Siparişteki rezervasyonlar

Planlı bir siparişi kesinleştirirken, **Kesinleştirme** iletişim kutusu kesinleştirme sırasında oluşturulan siparişler için işaretleme seçeneklerini ayarlamak amacıyla kullanabileceğiniz bir **İşaretlemeyi güncelleştir** alanı sağlar. Aşağıdaki değerlerden birini seçin:

- **Hayır**: Stok işaretleme uygulanmaz.
- **Standart**: Stok işaretleme ilişkilendirmeye göre güncelleştirilir. Bir karşılama siparişi (arz) karşılığında bir gereksinim siparişi (talep) işaretlenir. Bazı miktarlar, karşılama siparişinde kalırsa işaretlenmez ve başvuru bilgileri boş bırakılır. Örneğin, 100 ea değerinde bir satış siparişi 150 ea değerinde bir satın alma siparişiyle ilişkilendirildirse, başvuru bilgileri yalnızca satış siparişine atanır.
- **Genişletilmiş**: Herhangi bir miktarın karşılama siparişinde kalıp kalmadığına bakılmaksızın, hem gereksinim siparişi (talep) hem karşılama siparişi (arz) işaretlenir. Örneğin, 100 ea değerinde bir satış siparişi 150 ea değerinde bir satın alma siparişiyle ilişkilendirildirse, başvuru bilgileri hem satış siparişine hem de satın alma siparişine atanır.