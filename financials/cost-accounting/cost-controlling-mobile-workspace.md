---
title: "Mobil çalışma alanının maliyet denetimi"
description: "Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Maliyet denetimi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, maliyet merkezi yöneticilerinin maliyet merkezi performansı hakkındaki bilgileri her zaman ve her yerde görebilmelerini sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 09383c24b0dd2ad61a836f6c8dc97f4389915772
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Mobil çalışma alanının maliyet denetimi

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Maliyet denetimi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, maliyet merkezi yöneticilerinin maliyet merkezi performansı hakkındaki bilgileri her zaman ve her yerde görebilmelerini sağlar. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Maliyet denetimi mobil çalışma alanına genel bakış
-------------------------------------------------

**Maliyet denetleme** mobil çalışma alanı, maliyet merkezlerinin mevcut performansı hakkında anında bilgiyi, ffili maliyetleri, bütçelendirilmiş maliyete kıyaslayarak sağlar. Tekil maliyet öğelerinin durumlarının detayına inebilirsiniz. 

Örneğin, bir personel uluslararası bir konferansa davetiye almıştır ancak kuruluşun tüm seyahat masraflarını üstlenmesi gerekir. Personel, yöneticisi kendi konferansa katılıp katılamayacağını sorar. Yönetici, personelin konferansa katılması için bütçeye sahip olup olmadığını görmek için mobil cihazında **Maliyet denetimi** mobil çalışma alanını açar.

### <a name="data-security"></a>Veri güvenliği

**Maliyet denetimi** mobil çalışma alanındaki veriler, kullanıcı kimlik bilgileriyle güvenlik altına alınır. Maliyet merkezi yöneticilerinin yalnızca kendi maliyet merkezleri için verileri görmelerine izin verilir. Erişim düzeyi güvenliği **Maliyet muhasebesi** modülünde yönetilir. 

Maliyet muhasebecileri, **Maliyet muhasebesi** modülünde **Maliyet denetimi** mobil çalışma alanının yapılandırmasını tanımlar. Çalışma alanı Microsoft Dynamics 365 for Operations mobil uygulamasında yayımlandıktan sonra, uygulamada kullanılabilir. Bu sayede, kuruluşunuzdaki tüm maliyet merkezi yöneticilerinin aynı biçimdeki veriyi görüntüleyebilirler.

### <a name="actions-views-and-links"></a>Eylemler, görünümler ve bağlantılar

Dynamics 365 for Operations uygulaması için **Maliyet denetleme** mobil çalışma alanı, aşağıdaki eylem, görünüm ve bağlantıları sağlar:

-   **Eylemler:**
    -   Düzeni seçmek için **Yapılandırmayı seç**'i kullanın.
    -   **Maliyet nesnesini seç**'i, verinin filtreleneceği maliyet merkezini seçmek için kullanın. **Not:** Listede görünen maliyet merkezleri, **Maliyet muhasebesi** modülünde verilmiş olan erişime bağlıdır.
-   **Görünümler:** **Maliyet muhasebesi** modülünün yapılandırmasında seçilen eylemlere dayanarak, kartlarda aşağıdaki bilgileri görüntüleyebilirsiniz:
    -   Fiili - bütçe (geçerli dönem) karşılaştırması
    -   Fiili - revize edilmiş bütçe (geçerli dönem) karşılaştırması
    -   Fiili - bütçe (önceki dönem) karşılaştırması
    -   Fiili - revize edilmiş bütçe (önceki dönem) karşılaştırması
    -   Fiili - bütçe (günümüze kadar yıl) karşılaştırması
    -   Fiili - revize edilmiş bütçe (günümüze kadar yıl) karşılaştırması

    Aşağıda tutarlar tüm kartlar üzerinde gösterilir: Fiili, Bütçe, Fark ve Fark %'si.
-   **Bağlantılar:**
    -   Geçerli dönem için ayrıntılar
    -   Önceki dönem için ayrıntılar
    -   Yıl başından bu güne için ayrıntılar

    Bir bağlantıyı seçtiğinizde, her bir maliyet öğesi için bir kart gösterilir. Her kart için aşağıdaki tutarlar gösterilir: Fiili, Bütçe, Bütçe farkı, Bütçe farkı %'si, Revize edilmiş bütçe, Revize edilmiş farkı ve Revize edilmiş farkı %'si. 
    
    [![Bir maliyet öğesi için kart ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Ön koşullar
**Maliyet denetimi** mobil çalışma alanını kullanmadan önce, sistem yöneticinizin aşağıdaki önkoşulları yerine getirdiğinden emin olun.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Rol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dynamics 365 for Operations sürüm 1611 platform güncelleştirmesi 3 veya daha sonraki sürümünün uygulanmış olması gerekir.</td>
<td>Sistem yöneticisi</td>
<td>Dynamics 365 for Operations'u kuruluşunuz için halihazırda dağıtılmadıysa, sistem yöneticisi <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Bir Microsoft Dynamics 365 for Operations demo ortamı dağıt</a>'ı görmelidir.</td>
</tr>
<tr class="even">
<td>KB 4013633 uygulanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td>KB 4013633 (bir X++ güncelleştirmesi veya meta veri düzeltmesi), tedarik zinciri yönetimi için dört mobil çalışma alanı içerir. KB 4013633 uygulamak için sistem yöneticiniz bu adımları atması gerekir:
<ol>
<li>KB 4013633'yi, Microsoft Lifecycle Services (LCS) üzerinden karşıdan yükleyin.</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi</a>, Dynamics 365 for Operations sisteminize uygulayın.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Maliyet denetimi</strong> mobil çalışma alanı, Dynamics 365 for Operations mobil uygulaması için yayınlanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td><ol>
<li>Dynamics 365 for Operations'ı tarayıcınızda başlatın.</li>
<li><strong>Sistem parametreleri</strong> sayfasında, <strong>Mobil çalışma alanlarını yönet</strong>'i seçin.</li>
<li><strong>Maliyet nesnesi genel bakış</strong> çalışma alanını seçin.</li>
<li><strong>Mobil çalışma alanını yayınla</strong> üzerine tıklayın.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobil uygulamasını yükleyin ve kurun
Dynamics 365 for Operations mobil uygulamasını mobil uygulama mağazanızdan yükleyin ve kurun.

-   Android için: [Google Play Store'da Dynamics 365 for Operations](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone için: [iTunes apps mağazsında Dynamics 365 for Operations](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobil uygulamasına oturum açın
1.  Mobil cihazınızda uygulamayı başlatın.
2.  Dynamics 365 for Operations URL'nizi girin.
3.  Oturum açılacak şirketi girin. Örneğin **USMF** yazın.
4.  İlk defa oturum açtığınızda, Dynamics 365 for Operations hesabınızın kullanıcı adı ve parolasını girmeniz için uyarılırsınız. Kimlik bilgilerinizi girin.
5.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz. Sistem yöneticiniz daha sonra yeni bir çalışma alanı yayınlarsa, mobil çalışma alanlarının listesini yenilemek için çekebileceğinizi unutmayın. 

    [![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Maliyet merkezinizin performansını Maliyet denetimi mobil çalışma alanını kullanarak görüntüleyin
1.  Mobil cihazınızda **Maliyet denetleme** çalışma alanını seçin.
2.  **Maliyet nesnesi denetleme** seçeneğini işaretleyin.
3.  **Eylemler**'i seçin.
4.  **Yapılandırma seç**'i seçerek bir maliyet denetleme biçimi seçin.
5.  **Tamam**'ı seçin.
6.  **Eylemler**'i seçin.
7.  **Maliyet nesnesi seç**'i seçerek erişiminizin sağlandığı maliyet merkezlerini seçin.
8.  **Tamam**'ı seçin.
9.  Maliyet merkezinizin toplam performansını görün.
10. **Geçerli dönem için ayrıntılar** bağlantısını seçin.
11. Bireysel maliyet öğelerinin performansını görün.
12. Belirli maliyet öğeleri için de arama yapabilirsiniz.




