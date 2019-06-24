---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (28 Mayız 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8b401717e598b8a37dc773cbe7ce1f15fa2f60e5
ms.sourcegitcommit: 291d90a857dd1be4ad58dc10d57415d6bddb09c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2019
ms.locfileid: "1616488"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-28-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (28 Mayız 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler
Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içerir.

## <a name="coming-soon-in-attract"></a>Yakın zamanda Attract'e geliyor

### <a name="job-approvals-on-home-page"></a>Giriş sayfasındaki iş onayları

Onaylar, panonun bir **Onaylar** bölümünde görüntülenir. Onaylayanlar, iş kodunu, başlığı, diğer onaylayanları ve atanan tarihi görüntüleyen, **size atanan** altında onayları gözden geçirebilir. Bir işi onaya gönderen kullanıcılar **Sizin tarafından talep edilen** işi onaylaması gereken onaylayanları görüntüleyen, size ait işleri gözden geçirebilir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler
Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler
Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2319 için geçerlidir.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Özel alanlar için Common Data Service varlığı desteği

Bu sürümde şu Common Data Service varlıkları artık özel alanları destekliyor: Kazanç hesaplama oranı ayrıntısı, İş takvimi tatili satırı ve İşe alma.

### <a name="copy-position-now-includes-payroll-details"></a>Konumu kopyala şimdi bordro ayrıntılarını içerir
**Konumu Kopyala**'yı kullandığınızda ve seçeneklerin tümünü seçtiğinizde, bordro ayrıntıları bilgileri şimdi kopyalama bilgilerine dahil edilir. 

## <a name="in-preview-in-core-hr"></a>Core HR'da önizlemede

### <a name="restrict-the-leave-types-in-time-off-requests"></a>İzin taleplerindeki izin türlerini kısıtlama

Kuruluşlar, çalışanlara birçok farklı türde izin sunabilir. Bu izin türlerinden bazıları, çalışanların izin göndermelerine uygun olmayabilir ve bunun yerine İnsan Kaynakları (İK) tarafından yönetilir. Bu sürümle, çalışanların serbest bırakma taleplerini hangi izin türlerine gönderebilecekleri ile ilgili olarak ayarlayabilirsiniz. 

### <a name="new-page-to-validate-position-hierarchy-data"></a>Konum hiyerarşisi verilerini doğrulamak için yeni sayfa

İK ve yöneticiler yanlışlıkla içe aktarılmış olabilecek herhangi bir döngüsel referans için yönetim hiyerarşisini doğrulayabilir. Bu yeni sayfaya **Kuruluş yönetimi > Bağlantılar > Pozisyonlar > Pozisyon hiyerarşisi doğrulaması** üzerinden erişebilirsiniz.

### <a name="specify-reason-codes-on-leave-types"></a>İzin türlerinde neden kodları belirtme

Kuruluşlar izin istekleri hakkında ek bilgiler gerektirebilir. Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>İzin talepleri üzerindeki belirli izin türleri için sebep kodları gerektir

Kuruluşlar, bir çalışan izin talepleri gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Şirket ilkesi veya mevzuat gereksinimleri nedeniyle bu gereksinim bulunabilir. Hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>İK için izin ve devamsızlık hareket listesi sağlama

Çalışan iznini takip etme ve iznin nasıl hesaplandığını anlama özelliği, yalnızca İK'nın çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda çalışanlar için doğru izin ödülleri verilmesini sağlar. İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece İK personeli, izin bakiyeleri arkasındaki nedenleri görebilir.