---
title: Varlıkları satınalma siparişlerine göre oluşturma
description: Bu konu, Varlık Yönetiminde bakım işleri için varlıklar oluşturmak üzere temel olarak kullanılabilecek bir varlık maddeleri listesini nasıl oluşturabileceğinizi açıklar.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 536795ac8ac164a6cc16e9ba22b0aa7bf30ddfd8
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783671"
---
# <a name="create-assets-based-on-purchase-orders"></a>Varlıkları satınalma siparişlerine göre oluşturma

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konu, Varlık Yönetiminde bakım işleri için varlıklar oluşturmak üzere temel olarak kullanılabilecek bir varlık maddeleri listesini nasıl oluşturabileceğinizi açıklar. Varlık maddelerine göre, bu maddelerde oluşturulan satınalma siparişi satırlarının listesini görüntüleyebilirsiniz. Bu işlevin amacı, Varlık Yönetiminde bir satınalma siparişini temel alarak kolayca bir varlık oluşturmaktır.

İlk olarak, **Varlık maddeleri**'ndeki bir satınalma siparişinden varlıklar oluşturmak için kullanılacak maddeler ayarlayın. Bir satınalma siparişi satırı oluşturduktan sonra, **Bekleyen varlıklar**'da varlıklar oluşturun. Varlığın satınalma siparişinin hangi aşamasında oluşturulması gerektiğine karar vermek mümkündür.


## <a name="select-asset-items"></a>Varlık maddelerini seçin

1. **Varlık yönetimi** > **Kurulum** > **Varlıklar** > **Maddeler**'e tıklayın.
2. Yeni bir varlık maddesi oluşturmak için **Yeni**'ye tıklayın.
3. **Madde numarası** alanında bir maddeyi seçin. Bu alandan çıktığınızda, madde adı otomatik olarak **Ürün adı** alanına eklenir.
4. **Genel** hızlı sekmesinde, madde için bir varlık türü seçin.
5. Madde için varlık üreticisi ve modeli seçin.
6. Maddeyi kaydedin.


## <a name="create-assets-from-pending-assets"></a>Bekleyen varlıklardan varlıklar oluşturma

1. **Varlık yönetimi** > **Genel** > **Varlıklar** > **Bekleyen Varlıklar**'a tıklayın.
2. **Varlık maddeleri**'nde seçilen maddelere göre satınalma siparişlerinin güncelleştirilmiş bir listesini görürsünüz.
3. Varlığın oluşturulması gereken yaşam döngüsü durumunu seçmek için satınalma siparişlerinin durumunu filtreleyebilirsiniz. Örneğin, yalnızca bir satınalma siparişinde bir ürün girişi deftere nakledildiğinde varlıklar oluşturmak isteyebilirsiniz.
4. Maddeyle ilgili ayrıntılı bilgileri görüntülemek için satınalma siparişi satırındaki **Referans numarası** bağlantısını seçin.
5. **Stok boyutları** hızlı sekmesinde hangi boyutların görüntüleneceğini düzenlemek istiyorsanız, **Boyutları Görüntüle** düğmesine tıklayın ve seçimlerinizi yapın.
6. Bir satınalma siparişi satırına dayalı bir varlık oluşturmak istiyorsanız, liste sayfasında bu satır için **İşaretle** sütunundaki onay kutusunu seçin ve **Varlıklar oluştur**'a tıklayın. Varlık kodunu size bildiren bir ileti görüntülenir.
7. **Tüm varlıklar** listesinde varlığı seçin ve varlığa daha fazla bilgi eklemek için **Düzenle** düğmesine tıklayın.
8. **Bekleyen varlıklar**'da, bir varlık oluşturmak istemediğiniz için bir satırı silmek istiyorsanız, ilgili satırın **İşaretle** sütunundaki onay kutusunu seçin ve **Bekleyen varlıkları at**'a tıklayın. Varlık kodunu size bildiren bir ileti görüntülenir. Satınalma siparişini veya satış siparişini silmezsiniz. Yalnızca **Varlık Yönetimi**'nde varlık oluşturabildiğiniz kaydı silersiniz.

>[!NOTE]
>Tüm ürün boyutları (boyut, renk, yapılandırma, vb.) otomatik olarak varlık özniteliklerine aktarılır. İzleme boyutları (seri numarası), varlık oluşturulduğunda doğrudan varlığa depolanır.


## <a name="find-pending-assets"></a>Bekleyen varlıkları bulma

Bekleyen varlıkları denetlemek için **Bekleyen varlık sayımı** çalıştırabilirsiniz. Örneğin, bu işlev bekleyen bir varlık, varlık olarak oluşturulmaya hazır olduğunda bir bildirim almak için kullanılabilir.

1. **Varlık yönetimi** > **Periyodik** > **Varlıklar** > **Bekleyen varlık sayısı**'na tıklayın.
2. İşi çalıştırmak için **Tamam**'a tıklayın ve **Bekleyen varlıklar**'daki listeyi güncelleştirin.
3. Bu işi, örneğin her gün bir toplu iş olarak çalışacak şekilde ayarlayabilirsiniz.

**Dikkat:** Bir satınalma siparişinde ilgili maddeyi temel alarak bir varlık oluşturduktan *sonra* veri dğiştirilirse, bu değişiklikler varlığa yansıtılmaz.