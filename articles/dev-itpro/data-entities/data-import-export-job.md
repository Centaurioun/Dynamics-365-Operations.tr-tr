---
title: "Veri içe ve dışa aktarma işleri"
description: "Veri yönetimi çalışma alanını veri içe aktarma ve dışa aktarma işlerini oluşturmak ve yönetmek için kullanın."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e79fcaa634c4b4eb601241d75da2f36f2455db4e
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="data-import-and-export-jobs"></a>Veri içe ve dışa aktarma işleri

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içinde içe ve dışa aktarma işlerini oluşturmak ve yönetmek için **Veri yönetimi** çalışma alanını kullanırsınız. Varsayılan olarak, veri içe ve dışa aktarma işlemi, hedef veritabanındaki her bir varlık için bir hazırlama tablosu oluşturur. Hazırlama tabloları, taşımadan önce verileri doğrulamanızı, temizlemenizi ve dönüştürmenizi sağlar.

## <a name="data-importexport-process"></a>Ver içe/dışa aktarma işlemi
Veri içe ve dışa aktarmak için adımlar buradadır.

1. Aşağıdaki görevleri tamamladığınız bir içe ve dışa aktarma işi oluşturun:

    - Proje kategorisini tanımlayın.
    - İçe veya dışa aktarılacak varlıkları belirleyin.
    - İş için veri biçimlerini ayarlayın.
    - Varlıkları sıralayın, böylece mantıksal gruplarda ve mantıklı bir sırada işlenebilirler.
    - Hazırlama tablolarının kullanılıp kullanılamayacağını belirleyin.

2. Kaynak veri ve hedef verinin doğru eşleştirildiğini doğrulayın.
3. İçe ve dışa aktarma işiniz için güvenliği doğrulayın.
4. İçe ve dışa aktarma işini çalıştırın.
5. İş geçmişini gözden geçirerek işin beklendiği gibi çalıştığını doğrulayın.
6. Hazırlama tablolarını temizleyin.

Bu konunun kalan bölümleri işlemin her bir adımı hakkında bilgi veri.

## <a name="create-an-import-or-export-job"></a>Bir içe ve dışa aktarma işi oluşturun
Bir veri içe ve dışa aktarma işi bir veya birden fazla defa çalıştırılabilir.

### <a name="define-the-project-category"></a>Proje kategorisini tanımlayın
İçe veya dışa aktarma işiniz için uygun proje kategorisi seçmek için vakit ayırmanızı öneririz. Proje kategorileri ilgili işleri yönetmenize yardımcı olur.

### <a name="identify-the-entities-to-import-or-export"></a>İçe veya dışa aktarılacak varlıkları belirleyin
Belirli varlıkları bir içe veya dışa aktarma işine ekleyin veya uygulanacak bir şablon seçin. Şablonlar, bir işi varlıkların listesi ile doldurur. **Şablonu Uygula** seçeneği, işe bir ad verdikten ve işi kaydettikten sonra kullanılabilir.

### <a name="set-the-data-format-for-the-job"></a>İş için veri biçimlerini ayarlayın
Bir varlık seçtiğinizde, içe veya dışa aktarılacak verinin biçimini seçmelisiniz. **Veri kaynakları kurulumu** kutucuğunu kullanarak biçimleri tanımlayabilirsiniz. Pek çok kuruluş, demo veri kümesinde varsayılan olarak bulunanlardan başlar. Bu biçimlerin bir listesi aşağıda verilmiştir:

- AX (Microsoft Dynamics 365 for Finance and Operations, Enterprise edition için kullanılanla aynı biçimde içe veya dışa aktarılması gereken veriler için)
- ColonSeparated
- CSV
- Excel
- Paket

### <a name="sequence-the-entities"></a>Varlıkları sıralayın
Varlıklar bir veri şablonunda veya içe veya dışa aktarma işlerinde sıralanabilir. Birden fazla veri varlığı içeren bir iş çalıştırdığınızda, veri varlıklarının doğru sıralandığından emin olmanız gerekir. Öncelikli olarka, varlıklar arasında işlevsel bağımlılıkları adreslendirebilmek için varlıkları sıralarsınız. Varlıklar işlevsel bağımlılıklara sahip değilse, paralel içe veya dışa aktarma için zamanlanabilirler.

#### <a name="execution-units-levels-and-sequences"></a>Yürütme birimleri, seviyeler ve sıralamalar
Yürütme birimi, yürütme birimi içindeki seviye ve bir varlığın sıralaması, verinin içe veya dışa aktarıldığı sırayı yönetmeye yardımcı olur.

- Farklı bir yürütme birimindeki varlıklar paralel şekilde işlenir.
- Her bir yürütme biriminde, aynı düzeye sahiplerse varlıklar paralel olarak işlenir.
- Her bir düzeyde, varlıklar, düzeydeki sıralama numaralarına göre işlenir.
- Bir düzey işlendikten sonra, bir sonraki düzey işlenir.

#### <a name="resequencing"></a>Yeniden sıralama
Varlıklarınızı aşağıdaki durumlarda yeniden sıralamak isteyebilirsiniz:

- Yalnızca bir veri işi tüm varlıklarınız için kullanılacaksa, yeniden sıralama seçeneklerini, tam işin yürütme süresini optimize etmek için kullanabilirsiniz. Bu gibi durumlarda, modül, modül ve dizinin varlığı temsil etmek için özellik alanını temsil eden düzeyi temsil etmek için yürütme birimi kullanabilirsiniz. Bu yöntemi kullanarak, paralel modülleri arasında çalışır, ancak modül içindeki sıra yine de çalışabilir. Paralel işlemlerin başarılı olmasına yardımcı olmak için tüm bağımlılıkları dikkate almanız gerekir.
- Birden fazla veri işi kullanılıyorsa (örneğin, her bir modül için bir iş), düzeyi ve varlıkların sırasını en iyi yürütme için sıralamayı kullanabilirsiniz.
- Hiç bağımlılık yoksa, farklı yürütme birimlerinde maksimum optimizasyon için tüm varlıkları sıralayabilirsiniz.

**Yeniden sıralama**, birden fazla varlık seçildiğinde menü kullanılabilir. Yürütme birimi, düzeyi veya sıralama seçeneklerine dayanarak yeniden sıralayabilirsiniz. Seçilen varlıkları yeniden sıralamak için bir artış ayarlayabilirsiniz. Her bir varlık için seçilen birim, düzey ve/veya sıralama numarası, belirtilen artışla güncelleştirilir.

#### <a name="sorting"></a>Sıralama
**Şuna göre sırala** seçeneğini, varlık listesini sıralama sırasında görüntülemek için kullanabilirsiniz.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Kaynak veri ve hedef verinin doğru eşleştirildiğini doğrulayın
Eşleşme, hem içe hem dışa aktarma işlerine uygulanan bir fonksiyondur.

- Bir içe aktarma işinin bağlamında, eşleşme kaynak dosyada hangi sütunların hazırlama tablosunda sütunlar haline geleceğini belirtir. Bu nedenle, sistem hazırlama tablosunun hangi sütuna veri kaynak dosyasındaki sütun kopyalayacağını belirtebilir.
- Bir dışa aktarma işinin bağlamında, eşleşme hazırlama tablosunda (kaynakta) hangi sütunların hedef dosyasında sütunlar haline geleceğini belirtir.

Sütun adları hazırlama tablosunda ve dosyada sütun adları eşleşiyorsa, adlara dayalı olarak sistem otomatik olarak eşleşmeyi başlatır. Ancak, adları farklıysa, sütunları otomatik olarak eşleştirilmez. Bazı durumlarda, veri işindeki **Eşleşmeyi görüntüle** seçeneğini seçerek eşleşmeyi tamamlamanız gerekir.

İki eşleşme görünümü vardır: varsayılan görünüm olan **Eşleşme görselleştirmeleri** ve **Eşleştirme ayrıntıları**. Kırmızı bir yıldız (\*), varlıktaki gerekli alanları belirtir. Varlıkla çalışmadan önce bu alanların eşleşmesi gerekir. Diğer alanlar, varlık ile çalışmanız gerektiğinde eşleşmeyi iptal edebilirsiniz. Bir eşleşmeyi kaldırmak için **Varlık** sütunu veya **Kaynak** sütununda alanları seçin ve **Varlık seçimini** işaretleyin. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin ve sonra projeye dönmek için sayfayı kapatın. İçe aktardıktan sonra kaynaktan hazırlamaya alan eşleştirmeyi düzenlemek için aynı işlemi kullanabilirsiniz.

**Kaynak eşleştirme oluştur**'u seçerek sayfada bir eşleştirme oluşturabilirsiniz. Oluşturulan bir eşleme bir otomatik eşleme gibi davranır. Bu nedenle, eşlenmemiş tüm alanlar el ile eşleşmelidir.

![Veri eşleme](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>İçe ve dışa aktarma işiniz için güvenliği doğrulayın
**Veri yönetimi** çalışma alanına erişim kısıtlanmış olabilir, bu yüzden yönetici olmayan kullanıcılar yalnızca belirli veri işlerine erişebilir. Bir veri işine erişim, söz konusu işin yürütme geçmişine ve hazırlama tablolarına tam erişim anlamına gelir. Bu nedenle, bir veri işi oluşturduğunuzda, uygun erişim denetimlerinin mevcut olduğundan emin olun.

### <a name="secure-a-job-by-roles-and-users"></a>Bir işi roller ve kullanıcılarla güvenli hale getirin
**Uygulanabilir roller** menüsünü, işi birden fazla güvenlik rolüne kısıtlama için kullanın. Yalnızca bu rollerdeki kullanıcıların işe erişimi olacaktır.

Bir işi belirli kullanıcılara da kısıtlayabilirsiniz. Bir işi roller yerine kullanıcılarla güvenli hale getirirseniz, birden fazla kullanıcı bir role atanmışsa daha fazla kontrol olur.

### <a name="secure-a-job-by-legal-entity"></a>Tüzel kişiliğe göre bir işi güvenli hale getirin
Veri işleri doğaları gereği geneldir. Bu nedenle, bir veri işi oluşturulursa ve bir tüzel varlıkta kullanılırsa, iş sistemdeki diğer yasal varlıklarda görünür olur. Bu varsayılan davranış, bazı uygulama senaryolarında tercih edilebilir. Örneğin, veri varlıklarını kullanarak faturaları içe aktaran bir kuruluş, kuruluş içindeki tüm departmanlar için fatura hatalarını yönetmekten sorumlu merkezi bir fatura işleme ekibi oluşturabilir. Bu senaryoda, merkezi fatura işleme ekibinin tüm tüzel varlıklardaki tüm fatura içe aktarma işlerine erişiminin olması faydalıdır. Bu nedenle, varsayılan davranış açısından bir tüzel kişilik gereksinimini karşılar.

Ancak, bir kuruluş tüzel varlık başına fatura işleme ekiplerine sahip olmak isteyebilir. Bu durumda, bir tüzel kişilikteki bir ekip, yalnızca kendi tüzel varlığındaki fatura içe aktarma işine erişime sahip olmalıdır. Bu gereksinimi karşılamak için veri işleri üzerindeki tüzel varlığa dayalı erişim denetimini, veri işi içindeki **Uygulanabilir tüzel varlıklar** menüsünü kullanarak yapılandırabilirsiniz. Yapılandırma sona erdikten sonra, kullanıcılar yalnızca mevcut olarak oturum açılmış oldukları tüzel varlıktaki işleri görebilirler. Diğer tüzel varlıklardaki işleri görmek için kullanıcıların söz konusu tüzel varlığa geçmeleri gerekir.

Bir iş aynı anda roller, kullanıcılar ve tüzel varlıklarla güvenlik altına alınabilir.

## <a name="run-the-import-or-export-job"></a>İçe ve dışa aktarma işini çalıştırın
Bir işi tanımladıktan sonra **İçe aktar** veya **Dışa aktar** seçerek bir defa çalıştırabilirsiniz. Yinelenen bir iş ayarlamak için **Yinelenen veri işi oluştur** seçebilirsiniz.

## <a name="validate-that-the-job-ran-as-expected"></a>İşin beklendiği çalıştığını doğrulayın.
İş geçmişi hem içe hem de dışa aktarma işlerinde sorun giderme ve sorgulama için kullanılabilir. Tarihi iş yürütmeleri zaman aralıkları ile düzenlenir.

![İş geçmişi aralıkları](./media/dixf-job-history.md.png)

Çalıştırılan her iş aşağıdaki ayrıntıları sağlar:

- Yürütme ayrıntıları
- Yürütme günlüğü

Yürütme ayrıntıları, işin işlediği her bir veri varlığın durumunu gösterir. Bu nedenle, aşağıdaki bilgileri hızlı bir şekilde bulabilirsiniz:

- Hangi varlıkları işlendi
- Bir varlık için, kaç kaydın başarıyla işlendiği ve kaçının başarısız olduğu
- Her bir varlık için hazırlama kayıtları

Dışa aktarma işleri için hazırlama verisini bir dosya içinde indirebilir veya içe ve dışa aktarma işleri için bir paket olarak indirebilirsiniz.

Yürütme ayrıntılarından yürütme kaydını da açabilirsiniz.

## <a name="clean-up-the-staging-tables"></a>Hazırlama tablolarını temizleyin
Hazırlama tablolarını **Veri yönetimi** çalışma alanındaki **Hazırlama temizleme** özelliğini kullanarak temizleyebilirsiniz. Aşağıdaki seçenekleri, hangi kayıtların hangi hazırlama tablosundan silineceğini seçmek için kullanabilirsiniz:

- **Varlık** – Yalnızca bir varlık sağlandıysa, o varlığın hazırlama tablosundaki tüm kayıtlar silinir. Varlık için tüm veri projeleri ve tüm işler için tüm veriyi silmek için bu seçeneği işaretleyin.
- **İş Kodu** – Yalnızca bir iş kodu sağlandıysa, seçilen işteki tüm varlıklar için tüm kayıtlar uygun hazırlama tablolarından silinir.
- **Veri projeleri** – Yalnızca bir veri projesi seçiliyse, seçilen veri projesi için tüm işler arasındaki tüm varlıklar için tüm kayıtlar silinir.

Silinen kayıt kümesini daha da kısıtlamak için seçenekleri birleştirebilirsiniz.
