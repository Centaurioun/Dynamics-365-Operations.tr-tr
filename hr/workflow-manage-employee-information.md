---
title: "Personel bilgilerini yönetmek için iş akışlarını kullanma"
description: "Bu konu, personel bilgisini yönetmek için İnsan kaynakları için iş akışı yeteneğini nasıl kullanabileceğinizi açıklar. Örneğin, bir iş akışını bir pozisyonla ilişkilendirebilir ve çalışanların kendi kayıtlarını değiştirdiklerinde başlatılan bir onay iş akışı yapılandırabilirsiniz."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 806860e5df9252c074e04e9e1670f4215fd94ca2
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Personel bilgilerini yönetmek için iş akışlarını kullanma

[!include[banner](includes/banner.md)]


Bu konu, personel bilgisini yönetmek için İnsan kaynakları için iş akışı yeteneğini nasıl kullanabileceğinizi açıklar. Örneğin, bir iş akışını bir pozisyonla ilişkilendirebilir ve çalışanların kendi kayıtlarını değiştirdiklerinde başlatılan bir onay iş akışı yapılandırabilirsiniz.

İnsan kaynakları için iş akışı kabiliyeti, insan kaynakları faaliyetlerini yönetmek için çok sayıda iş akışı sağlar. Ek olarak, belirli iş akışlarını değiştirebilmeniz ve onları bir raporlama hiyerarşisiyle ilişkilendirebilmeniz için çok sayıda seçenek kullanabilmektedir. İş akışları, yöneticilerin personel bilgilerinin çeşitli standart türlerinde değişik yapmalarını kolaylaştırmak için mevcuttur. İş akışını bir pozisyon ile ilişkilendirebilirsiniz. Daha sonra, personeller kendi personel kayıtlarını değiştirirlerse, yeni bilgiler kaydedilemeden önce onay gerektiren bir iş akışı başlatılır. İş akışları, değişiklikleri daha etkin şekilde yönetebilmeniz ve personel bilgilerinizi daha doğru tutabilmeniz için aşağıdaki türde bilgiler için önceden tanımlıdır:

-   Kimlik numaraları
-   Kurslar
-   Eğitim
-   Resim
-   Ödünç verilen maddeler
-   Mesleki deneyim
-   Proje deneyimi
-   Yetenekler
-   Güven gerektiren pozisyonlar
-   İnsan kaynakları eylemleri
-   Kurs kaydı

Personeller işe alındıklarını, transfer edildiklerinde veya işten çıkarıldıklarında, iş akışı bir gözden geçirme işlemi içerebilir. Bu şekilde, bir belge gözden geçirilebilir veya bir eylemin koşulları, iş akışının bir parçası tanımlanabilir. Gözden geçirme işlemi tamamlandığında, belge veya eylem tamamlanır ve iş akışını son onayı adımına taşınır.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>İş akışını bir pozisyon hiyerarşisiyle ilişkilendirin.
Bir iş akışını, yapılandırdığınız herhangi bir hiyerarşiyle ilişkilendirebilirsiniz. Örneğin, bir pozisyon, bir matris raporlama hiyerarşisi ile ilişkili ise, bir iş akışının belirli bir proje için giderleri, bu pozisyonla ilişkili bir personelin yöneticisi yerine proje liderine yönlendirmesini sağlayacak üzere yapılandırabilirsiniz. Yeni bir iş akışı oluşturun veya varolan bir iş akışını değiştirmek için **İnsan Kaynakları iş akışı** sayfasında **Yeni** üzerine tıklayın. İş akışı tasarımcısını başlatmak için listeden bir iş akışını seçin. Yeni bir iş akışı oluşturmak için tasarımcıyı kullanabilir veya mevcut bir iş akışındaki adımları değiştirebilirsiniz. Mevcut bir iş akışını değiştirdiğinizde, değişiklikleriniz yeni bir sürüm olarak kaydedilir. Gerekirse bu nedenle, her zaman önceki sürüme geri dönebilirsiniz.

## <a name="configure-a-human-resources-workflow"></a>İnsan kaynakları iş akışı yapılandırma
Çalışanlar kişisel kimlik saptamalarında değişiklik talep ettiklerinde başlatılacak basit bir iş akışı yapılandırmak için şu adımları izleyin.

1.  **İnsan Kaynakları iş akışları** sayfasında **Yeni**'yi tıklatın.
2.  Kullanılabilir iş akışları listesinden **Kimlik saptama numaraları**'nı seçin.
3.  İş akışı tasarımcısını başlatmak için **Çalıştır**'ı tıklatın ve istenildiğinde kullanıcı adınızı ve parolanızı girin.
4.  İş akışı öğeleri listesinden **Kimlik saptama numarasını** öğesini, tasarımcı tuvaline sürükleyin.
5.  Onay öğesini **Başlat** ve **Bitir** ile bağlayın.
6.  **Öğeyi onayla** üzerine çift tıklatın ve sonra sağ tıklayıp **Özellikler**'i seçin.
7.  İş öğesi yönergeleri eklemek için şu adımları izleyin:
    1.  **Atama**'yı seçin ve sonra atama türü altında **Hiyerarşi**'yi seçin.
    2.  **Hiyerarşi** seçimi altında **Yapılandırılabilir hiyerarşi**'yi seçin.
    3.  Bir durdurma koşulu ekleyin ve sayfayı kapatın.

8.  Tüm ek yönergeleri tamamlayın (ek uyarılar mevcut olmamalıdır).
9.  **Kaydet ve kapat**'ı tıklatın. Yeni iş akışını etkinleştirip iletişim kutusu açılınca **Etkinleştir**'i seçin.
10. **İnsan Kaynakları** &gt; **Pozisyonlar** &gt; **Pozisyon hiyerarşi türleri**'ne gidin.
11. **Matris**'i seçin.
12. **Çalışan kimlik saptama numarası**'nı iş akışı listesine ekleyin.




