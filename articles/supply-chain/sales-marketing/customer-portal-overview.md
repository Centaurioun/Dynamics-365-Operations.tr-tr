---
title: Dynamics 365 Supply Chain Management için Müşteri portalına genel bakış
description: Bu konu müşteri portalını tanıtır ve bunu kimin nasıl çalıştığını açıklar.
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 709ba18be9e2edd5d0a7f143aaed5ef94f365b91
ms.sourcegitcommit: 9a2e9f7dfec47c42178bb67a3e099e610515baf3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456938"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Dynamics 365 Supply Chain Management için Müşteri portalına genel bakış

## <a name="what-is-the-customer-portal"></a>Müşteri Portalı nedir?

Modern tedarik zinciri sistemleri tümleştirmeye dayanır. Bunlar ayrı bir siloda değil stok, müşteri talebi ve satış bölümlerinin entegre olmasını gerektirir. Müşteri Portalı, Microsoft Dynamics 365 Supply Chain Management'un Bu tümleştirmeyi geliştirmesine ve müşterilerinin bilgilendirilmesi konusunda daha etkili olmasını sağlayan kuruluşlara yardımcı olur.

Müşteri Portalı, şirketler satış siparişi işlemeyle ilişkili senaryolar için dışarıdan bakan işletmeler arası (B2B) bir Web sitesi oluşturmalarına olanak veren bir [Power Apps portal](https://docs.microsoft.com/powerapps/maker/portals/overview) şablonudur. Şablon, Harici kurumsal müşterilerin şirketin Dynamics 365 ortamından veri görüntülemesini ve oluşturmasını sağlamak için [çift-yazılır](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management ve Power Apps portalları kullanır.

Müşteri Portalı şablonu, Power Apps'in sunduğu tüm özelleştirme yeteneklerine sahiptir. Şablon, şirketin markasını temsil edecek şekilde değiştirilebilir, artırılmış işlevsellik ekleyebilir ve Kullanıcı deneyimini değiştirebilir. Kutunun dışında sunduğu şablonun tüm işlevleri istenildiği şekilde değiştirilebilir.

> [!IMPORTANT]
> Tek başına, şablonun tamamen işlevsel olması beklenmez. Yalnızca dışarıdan bakan bir Web sitesi oluşturmak isteyen müşteriler için Etkinleştirici görevi görür, böylece kuruluş müşterilerinin Supply Chain Management'nden veri ile dedebilmesini sağlar.

> [!NOTE]
> Müşteri Portalı belgeleri, bir Supply Chain Management yüklemesi için müşteri portalını kuran Yöneticiler, özelleştiriciler ve sistem tümleştiricilerine yönlendirilir. Supply Chain Management çalıştıran bir kuruluşun müşterileri olan kişileri açıklamak için _müşteri_ ve _Kullanıcı_ terimlerini kullanır ve son portalı kullanacak.

## <a name="video"></a>Görüntü

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

[Dynamics 365 Supply Chain Management'ta Müşteri portalı şablonuna genel bakış](https://youtu.be/nPrqoLuHfV8) videosu (yukarıda gösterilen), YouTube'daki [Finance and Operations çalma listesinde](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) yer almaktadır.

## <a name="who-should-use-it"></a>Kimler kullanacak?

Müşteri Portalı, Supply Chain Management çalıştıran ve şu özelliklere sahip şirketler için tasarlanmıştır:

- Sipariş işlem bilgilerini (sipariş durumu veya hesap bilgileri gibi) doğrudan Supply Chain Management sisteminden kurumsal müşterilerine ileten dışarıdan bakan bir Web sitesi oluşturmak ister.
- Dynamics AX 2012, Supply Chain Management'a ve daha önce [AX 2012 Müşteri Self Servis Portalı](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal)'na geçiş yaparken yapılır.

Aşağıdaki organizasyon tipleri Müşteri portalını gerçekleştirmek için uygun aday **değildir**:

- Kurumsal olmayan müşteriler için Web sitesi oluşturmak isteyen şirketler. Bu şirketler bir [Dynamics 365 Commerce e-ticaret Web sitesi](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site) oluşturmayı düşünmelidir.
- Benzer amaçlarla zaten varolan Power Apps Portal Web sitesini kullanan şirketler. Bu şirketler müşteri portalından hiçbir ek yarar almaz. Müşteri Portalı, iki yazma, Supply Chain Management ve Power Apps portallar arasında "noktaları bağlamak" isteyen müşteriler için kılavuz ve başlangıç noktası görevi gören bir şablon olarak teslim edilir. Bu amaca hizmet eden bir Web sitesini önceden ayarladıysanız, bu Web sitesini yeniden sağlamak için müşteri portalı şablonunu kullanmaktan çok daha fazla değer kazanmayabilir.

## <a name="how-does-it-work"></a>Nasıl çalışır?

Müşteri Portalı, Power Apps portal şablonu olarak sağlanır. Bunlar Power Apps portallarına ve çift yazmaya bağlıdır.

[Power Apps portallar](https://docs.microsoft.com/powerapps/maker/portals/overview), kullanıcıların, kuruluş dışından kişilerin oturum açmasını sağlayan dışarıdan bakan bir Web sitesi oluşturmalarına olanak tanıyan bir özelliktir. Portalları yapmak için bir kod oluşturma gerekmez. Müşteri Portalı, Microsoft tarafından kullanılabilen birçok [Dynamics 365 Portal şablonlarından](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) biridir.

[Çift yazım](https://docs.microsoft.com/powerapps/maker/portals/overview), Dynamics 365 ve Finance and Operations uygulamalardaki modele dayalı uygulamalar arasında yakın zamanda gerçek zamanlı etkileşim sağlayan bir altyapıdır. Çift-yazma, Finance and Operations uygulamalar ve Common Data Service arasında çift yönlü tümleştirme sağlar. Bu nedenle, uygulamalar arasında tümleşik bir kullanıcı deneyimi sağlar. Müşteri Portalı, Çift-yazılır olarak eşitlenen varlıklara bağlıdır. Supply Chain Management'tan alınan verilerin müşteri portalında yapılabilmesi için, ilgili tüm varlıklar için çift-yazım etkinleştirilmiş olmalıdır.

![Müşteri portalına bağımlılıklar](media/customer-portal-elements.png "Müşteri portalına bağımlılıklar")

Müşteri Portalı, Supply Chain Management yüklemesinden veri kullanan dışarıdan bakan bir Web sitesi oluşturmak amacıyla Power Apps portalları kullanmak isteyen kuruluşlar için bir başlangıç noktası görevi görür. Kuruluşların çift-yazılır, Supply Chain Management ve Power Apps portallara bağlanmasına yardımcı olur.