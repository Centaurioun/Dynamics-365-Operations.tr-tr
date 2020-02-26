---
title: POS cihazlarında hareket ekranına öneriler denetimi ekleme
description: Bu konu, öneri denetiminin bir satış noktası (POS) cihazına, Microsoft Dynamics 365 Commerce'de ekran düzeni tasarımcısını kullanarak nasıl ekleneceğini açıklar.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d6f48197a36f633e3cd63cbad4518f53946fc7f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024280"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>POS cihazlarında hareket ekranına öneriler denetimi ekleme

[!include [banner](includes/banner.md)]


Bu konu, öneri denetiminin bir satış noktası (POS) cihazına, Microsoft Dynamics 365 Commerce'de ekran düzeni tasarımcısını kullanarak nasıl ekleneceğini açıklar. Ürün önerileri hakkında daha fazla bilgi için [POS belgelerindeki ürün önerilerini okuyun](product.md).


Commerce kullanırken ürün önerilerini POS cihazınızda görüntüleyebilirsiniz. Ürün önerilerini görüntülemek için, ekran düzeni tasarımcısını kullanarak bir denetimi hareket ekranına eklemeniz gerekir. 

## <a name="open-layout-designer"></a>Açık Düzen tasarımcısı

1. **Retail ve Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri** öğelerini seçin.
2. Denetimi eklemek istediğiniz ekranı bulmak için Hızlı Filtre'yi kullanın. **Örneğin Ekran düzeni kimliği** üzerinde, **F2CP16:9M** kullanarak filtrele.
3. Listede, istenen kaydı bulun ve seçin. Örneğin, **Ad: F2CP16:9M Ekran Düzeni Kimliği: F2CP16:9M** seçin.
4. **Düzen tasarımcısı**'na tıklayın.
5. Düzeni tasarımcısını başlatmak için istemleri izleyin. Kimlik bilgileri istendiğinde, Düzen tasarımcısı **Ekran düzenleri** sayfasından başlatıldığında girilenle aynı kimlik bilgilerini girin.
6. Oturum açtığınızda, aşağıdakine benzer bir sayfa görüntülenir. Düzen, mağazanız için yapılan özelleştirmelere bağlı olarak farklı olacaktır.


    [![Düzen tasarımcısı](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Bir görüntüleme seçeneği seçin

İki yapılandırma seçeneği mevcuttur. Mağazanız için en iyi çalışan seçeneği seçin ve denetimin kurulumunu tamamlamak için kalan yönergeleri izleyin. İki seçenek şunlardır:

- Önerileri her zaman görünür durumdadır.
- Bir **Öneriler** sekmesi, ekranın sağ tarafındaki kılavuzda görüntülenir.

### <a name="make-recommendations-always-visible"></a>Önerileri her zaman görünür yapmak


1. Hareket satırı ayrıntıları alanının yüksekliğini, solundaki müşteri paneliyle aynı boyda olacak şekilde azaltın.


    [![Hareket satırı ayrıntıları alanının yüksekliği azaltıldı](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Soldaki menüden, öneriler denetimini hareket satırı ayrıntıları alanı ve hareket erkanının alt ortasındaki düğme kılavuzu arasında sürükleyip bırakın. Bu alana sığacak şekilde yeniden boyutlandırın.

    [![Öneriler denetimi düzene eklendi](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.
4. Commerce içinde, **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım tabloları**'na gidin.
5. Listede **1090 Kayıtları**'nı seçin.
6. **Şimdi çalıştır** üzerine tıklayın.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Ekranın sağ tarafındaki düğme kılavuzuna bir Öneriler sekmesi eklemek

1. Sayfanın sağ tarafında bulunan düğme kılavuzundaki son sekmenin altındaki boş alana sağ tıklayın.

2. **Özelleştir**'e tıklayın.

    [![Özelleştirme - Sekme denetimi iletişim kutusu](./media/pic-5.png)](./media/pic-5.png)

3. **Yeni sekme** üzerine tıklayın.
4. Şimdi eklemiş olduğunuz yeni sekmeyi bulun. Aşağı doğru gitmeniz gerekebilir.
5. **İçerikler** açılır listesinde, **Önerilen ürünler**'i seçin.

    [![Önerilen ürünleri İçerik alanında seçmek](./media/pic-6.png)](./media/pic-6.png)

6. **Etiket** alanı içinde, öneriler sekmesi için bir ad girin. Örneğin, 'Önerilen ürünler' yazın.
7. **Resim** alanında, sekme üzerinde görünecek resmi seçin.
8. **Tamam**'a tıklayın. Yeni sekme düğme kılavuzunda görüntülenir.
9. Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.
10. Commerce içinde, **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım tabloları**'na gidin.
11. Listede **1090 Kayıtları**'nı seçin.
12. **Şimdi çalıştır** üzerine tıklayın.

## <a name="additional-resources"></a>Ek kaynaklar

[POS'ta ürün önerileri](product.md)

[Ürün önerilerine genel bakış](../commerce/product-recommendations.md)