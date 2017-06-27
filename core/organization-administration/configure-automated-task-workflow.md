---
title: "Bir görev akışında otomatikleştirilmiş görev yapılandır"
description: "Bu konu, otomatik bir görevin özelliklerini yapılandırmayı açıklar."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 358065dd127703191ba441d0603307a3b7e5df60
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="configure-an-automated-task-in-a-workflow"></a>Bir görev akışında otomatikleştirilmiş görev yapılandır

[!include[banner](../includes/banner.md)]


Bu konu, otomatik bir görevin özelliklerini yapılandırmayı açıklar.

Otomatik bir görevi iş akışı düzenleyicisinde yapılandırmak için göreve sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın. Ardından otomatik görevin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-task"></a>Görevi adlandırma
Otomatik göreve bir ad vermek için aşağıdaki adımları takip edin.

1.  Sol bölmede **Temel Ayarlar**'ı tıklatın.
2.  **Ad** alanına görev için benzersiz bir ad girin.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme
Otomatik bir görev çalıştırıldığında veya iptal edildiğinde insanlara bildirimler gönderebilirsiniz. Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.

1.  Sol bölmede **Bildirimler**'i tıklatın.
2.  Bildirim gönderilecek etkinliklerin yanındaki onay kutusunu seçin:
    -   **Yürütme** – Görev çalıştırıldığında bildirim gönderilir.
    -   **İptal Edildi** – Görev iptal edildiğinde bildirim gönderilir.

3.  2. adımda seçtiğiniz bir olay için bir satır seçin.
4.  **Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.
5.  Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz. Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:
    1.  Metin kutusunda, yer tutucunun görüneceği yere tıklayın.
    2.  **Yer tutucu ekle**'yi tıklatın.
    3.  Beliren listede, eklenecek yer tutucuyu seçin.
    4.  **Ekle**'yi tıklatın.

6.  Bildirimin çevirilerini eklemek için şu adımları izleyin:
    1.  **Çeviriler**'e tıklayın.
    2.  Beliren sayfada **Ekle**'yi tıklatın.
    3.  Beliren listede, metni girdiğiniz dili seçin.
    4.  **Çevrilen metin** alanında, metni girin.
    5.  Metni kişiselleştirmek için, 5. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.
    6.  **Kapat** düğmesini tıklayın.

7.  **Alıcı** sekmesinde, bildirimlerin kime gönderildiğini belirtin. Aşağıdaki tablodaki seçeneklerden birini seçin ve 8. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Seçenek</th>
    <th>Bildirim alıcıları</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td><ol>
    <li><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, bildirimlerin gönderileceği grup ya da rolün türünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>İş akışı kullanıcısı</td>
    <td>Mevcut iş akışına katılım gösteren kullanıcılar</td>
    <td><ul>
    <li><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Kullanıcı</td>
    <td>Belirli Microsoft Dynamics 365 for Operations kullanıcıları</td>
    <td><ol>
    <li><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</li>
    <li><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Dynamics 365 for Operations kullanıcılarını içerir. Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.




