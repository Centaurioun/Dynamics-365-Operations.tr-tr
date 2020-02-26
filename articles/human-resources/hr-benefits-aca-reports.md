---
title: Ekonomik Bakım Yasası (ACA) raporları oluşturma
description: Ekonomik Bakım Yasası'nın İşveren Yönergesi bölümündeki Formlar 1095-B ve 1095-C'den raporlanan bilgileri izlemesi gereken işverenlere destek olmak için işlev mevcuttur. Bu işlevin yalnızca Amerika Birleşik Devletleri'ndeki tüzel varlıklar için etkin olduğunu unutmayın.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 47532861203fedbffc49aa92d25fc99de9d25376
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010881"
---
# <a name="generate-affordable-care-act-aca-reports"></a>Ekonomik Bakım Yasası (ACA) raporları oluşturma

Ekonomik Bakım Yasası'nın **İşveren Yönergesi** bölümündeki Formlar 1095-B ve 1095-C'den raporlanan bilgileri izlemesi gereken işverenlere destek olmak için işlev mevcuttur. Bu işlevin yalnızca Amerika Birleşik Devletleri'ndeki tüzel varlıklar için etkin olduğunu unutmayın.

## <a name="getting-started"></a>Başlarken
Formlar 1095-B ve 1095-C üzerindeki bilgiler izlemeye başlandığında, ilk önce bir veya birden fazla Ekonomik Bakım kapsama grubu oluşturmalısınız. Bu Ekonomik Bakım kapsama grupları, bir personele sağlanan kapsamanın teklifini belirtmek, personelin en düşük maliyet aylık primi (maliyet federal yoksulluk sınırının üzerindeyse) payı ve mevcutsa, işveren tarafından kullanılan Güvenilen Liman. Ekonomik Bakım Yasası gruplarını kullanmak, tüm koşulların aynı olduğu tüm personel kayıtlarına dokunmak zorunda kalınmadan bu alanlardaki bilgiyi yönetmenize olanak sağlar. Ek olarak, Ekonomik Bakım kapsama grupları, bir veya birden fazla personele, sayfa üzerindeki Toplu atama işlevi kullanarak kolaylıkla atanabilir.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Bir kapsama grubunun birden fazla sürümünü tutmak
Herhangi bir kapsama grubunun birden fazla sürümünü tutabilirsiniz, bu da kuruluşunuzda veya sunulan kazançlarda bir değişiklik olduğunda, yeni bir grup oluşturmak ve personeli atamak zorunda olmadan, bu da grubun bilgisini güncel tutacak değişiklikler yapmanıza izin verir. 

İhtiyaç duyduğunuz Ekonomik Bakım kapsama gruplarını oluşturduktan sonra, sayfa üzerinde **Toplu atama** işlevini kullanarak grupları personele atamayı seçebilir veya her bir personeli seçip, bu personel için ACA bilgisinin izlenmesinin gerekip gerekmediği belirtebilir ve personeli bir Ekonomik Bakım kapsama grubuna atayabilirsiniz.

Ekonomik bakım kapsamı bilgisinin bir personel için izlenmesi veya raporlanması gerekmiyorsa, örneğin bir yarı zamanlı personel ise, **Rapor kapsamı** alanı Hayır olarak ayarlanabilir. Her ne kadar ACA bilgisinin izlenmesi gereken her bir personelin bir Ekonomik Bakım kapsama grubuna atanması gerekse de, Ekonomik Bakım kapsama grubuna girilen değerlerden farklı olması gereken herhangi bir ay veya aylar için **Kapsamın teklifi**, **Personelin maliyet payı** ve **Güvenli Liman** seçeneklerini yine de değiştirebilirsiniz.

Herhangi bir Ekonomik Bakım kapsama grubu değerine istisnalar eklemek için, Çalışma sekmesinin Ek bilgi altında bulunan Çalışan ayrıntı sayfasındaki Ekonomik Bakım Kapsama bağlantısına tıklayın.

## <a name="reporting-health-care-coverage"></a>Sağlık bakımı kapsamasını raporlama
Bir tam zamanlı personele sunulan herhangi bir sağlık sigortası kapsamını izlemeye ek olarak, işveren personelin kayıtlı olduğu işveren tarafından sponsorlu kendinden sağlık sigortası kapsaması veriyorsa (çalışma durumlarının tam zamanlı mı yarı zamanlı mı olduğundan bağımsız olarak), ek bilgilerin 1095-C üzerinde raporlanması gerekir. İşveren tarafından desteklenen kazanç planları tarafından kapsanan her personelin (bakmakla yükümlü olduğu kişi dahil), kapsanmış oldukları aylar için rapora dahil edilmeleri gerekir. 

Her bir Kazanç planını raporlanması gerekip gerekmediğini, **ACA raporlanabilir** onay kutusunu seçerek belirtebilirsiniz.

Ek olarak, personeller, bakmakla yükümlü oldukları kişilerden herhangi birinin bir kazanç altında kapsanmasını seçmişlerse, bakılmakla yükümlü olan kişinin, her bir personel için kapsandığı tarihleri Kazançları yönet sayfası üzerinde belirtebilirsiniz. Bakılmakla yükümlü kişinin kazanç tarafından kapsandığını belirtmek amacıyla, Bakılmakla yükümlüler hızlı sekmesinin eylem panosunda Düzenle düğmesini seçin.

**Bakılmakla yükümlü kapsama veri yöneticisi** sayfası üzerinde, bakılmakla yükümlü kişinin kazanç tarafından kapsandığı tarihi belirtebilirsiniz. Bu sayfaya tarihler girmek, **Kazançları koru** sayfası üzerindeki **Kapsanan** onay kutusunu otomatik seçer.

## <a name="generate-1095b-and-1095c-forms"></a>1095B ve 1095C formlarını oluştur
109-B ve 1095-C formlarını bir ürünün içinden oluşturabilir ve personellerinizin her birine dağıtabilirsiniz. IRS'ye gönderilmek için kullanılabilecek 1095-C'yi ve karşılık gelen 1094-C gönderme dosyalarını elektronik olarak oluşturmak, ayrıca sistem tarafından da oluşturulabilir.  

1095-C formunu oluştururken, ilgili vergi yılını girin ve sosyal güvenlik numaralarının maskelenmiş olması gerekip gerekmediğini belirtin. 1095-C formlarını 500'den fazla personel için yazdırıyorsanız, birden fazla PDF dosyası alacaksınız. **Belge yönetimi parametreleri** penceresindeki **Maksimum dosya boyutu**'nu 150 MB'a artırmanız önerilir.

## <a name="viewing-information"></a>Görüntüleme bilgisi
**Çalışan Ekonomik Bakım kapsamı** sayfasını, hangi personellerin her bir kapsama grubuna atandığını, hangi personellerin bir rapora dahil edilmesi gerekmediğini ve hangi personellerin atanmamış olduğunu görmek için kullanabilirsiniz.

Ekonomik Bakım kapsama grubundaki varsayılan değerlerden herhangi bir geçersiz kılınmışsa, değiştirilmiş olan değerin yanında bir yıldız işareti görüntülenir. 12 ayın tamamı için değerler aynı ise ve geçersiz kılınmamışsa, değer **Tüm 12 ay** sütununda yazdırılır.

Hangi personellerin ACA raporlanabilir olarak işaretlenmediğini anlamak için sorgulama penceresini de kullanabilirsiniz, yani, onlara kapsamanın teklif edilip edilmediğini izlemeniz gerekmediği ve onlara yıl sonunda 1095-C formu çıkartmak zorunda olmadığınız anlamına gelir. **Filtrele** alanında **ACA raporlanabilir değil** seçerek, 1095-C almamak üzere işaretlemiş tüm personellerin bir listesini oluşturabilirsiniz.

ACA raporlanabilir olmayan personellerin bir listesini görüntülemeye ek olarak, atanmamı ş(**ACA Rapor kapsama** alanı boş) olan herhangi bir personeli görüntüleyebilir veya **Yıl** alanında seçilmiş yıl için süresi dolmuş Ekonomik Bakım kapsama grubuna atanmış personeli görüntüleyebilirsiniz.

Filtreleme seçeneklerinden herhangi birini kullanarak oluşturulan personel listelerini Excel'e aktarabilirsiniz.

Bir işveren olarak kendinden sigortalı kapsama sağladığınız için kapsanan bireyleri raporlamanız gerekiyorsa, kazanç planları altında **ACA raporlanabilir** olarak işaretlenmiş bakıma ihtiyaç duyulanları, eylem bölmesi şeridindeki Bakıma ihtiyaç duyulanlar kapsama eylemini seçerek görüntüleyebilirsiniz.

**Not:** Yalnızca planı **ACA raporlanabilir** olarak işaretlenmiş olan kazançlar sorgulama penceresinde görüntülenir.