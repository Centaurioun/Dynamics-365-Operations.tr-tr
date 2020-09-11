---
title: Çift yazma için para birimi veri türü geçişi
description: Bu konu, çift yazmanın para birimi için desteklediği ondalık basamak sayısının nasıl değiştirileceğini açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456826"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Çift yazma için para birimi veri türü geçişi

[!include [banner](../../includes/banner.md)]

Para birimi değerleri için desteklenen ondalık basamak sayısını en fazla 10'a artırabilirsiniz. Varsayılan sınır dört ondalık haneye sahiptir. Ondalık basamakların sayısını artırarak, verileri eşitlemek için çift yazma kullandığınızda veri kaybını engelleyebilirsiniz. Ondalık basamak sayısında artış kabul edilerek yapılan bir değişikliktir. Bunu uygulamak için, Microsoft'tan yardım istemeniz gerekir.

Ondalık basamak sayısının değiştirilmesi işleminde iki adım vardır:

1. Microsoft'tan geçiş talep edin.
2. Common Data Service'ta ondalık basamak sayısını değiştirin.

Finance and Operations uygulaması ve Common Data Service'ın para birimi değerlerinde aynı sayıda ondalık basamak desteklemesi gerekir. Aksi takdirde, bu bilgiler uygulamalar arasında eşitlendiğinde veri kaybı ortaya çıkabilir. Geçiş işlemi para birimi ve döviz kuru değerlerinin depolanma biçimini yeniden yapılandırır, ancak hiçbir veriyi değiştirmez. Geçiş tamamlandıktan sonra, para birimi kodları ve fiyatlandırma için ondalık basamak sayısı artırılabilir ve kullanıcıların girdiği ve görüntülediği verilerde daha fazla ondalık duyarlığı olabilir.

Geçiş isteğe bağlıdır. Daha fazla ondalık basamak desteğinden avantaj sağlayabilecekseniz, geçiş yapmayı düşünmeniz önerilir. Dörtten fazla ondalık basamak içeren değerlerin gerekli olmadığı kuruluşların geçiş yapması gerekmez.

## <a name="requesting-migration-from-microsoft"></a>Microsoft'tan geçiş talep etme

Common Data Service'teki mevcut para birimi alanları için depolama, dörtten fazla ondalık basamak destekleyemez. Bu nedenle, geçiş işlemi sırasında, para birimi değerleri veritabanındaki yeni iç alanlara kopyalanır. Bu işlem, tüm veriler geçirilene kadar sürekli olarak gerçekleşir. Dahili olarak, geçişin sonunda yeni depolama türleri eski depolama türlerinin yerini alır, ancak veri değerleri değiştirilmez. Böylece para birimi alanları en fazla 10 ondalık basamağı destekleyebilir. Geçiş işlemi sırasında Common Data Service kesinti olmadan kullanılabilir.

Aynı zamanda, döviz kurları, geçerli 10 limiti yerine 12'ye kadar ondalık basamağı destekleyecek şekilde değiştirilir. Bu değişiklik, ondalık basamak sayısının hem Finance and Operations hem de Common Data Service'te aynı olmasını sağlamak için gereklidir.

Geçiş hiçbir veriyi değiştirmez. Para birimi ve döviz kuru alanları dönüştürüldükten sonra, yöneticiler hem hareket para birimi hem de fiyatlandırma için ondalık basamak sayısını belirterek sistemi, para birimi alanları için en çok 10 ondalık basamak kullanacak şekilde yapılandırabilir.

### <a name="request-a-migration"></a>Geçiş talep etme

Bu özelliği kullanılabilir hale getirmek için, **CDSExpandDecimal@microsoft.com** adresine aşağıdaki bilgileri ekleyerek e-posta gönderin:

+ **Konu:** \<organizationID\> için genişletilmiş ondalık desteği etkinleştirme isteği
+ **Gövde:** \<organizationID\> kuruluşum için genişletilmiş ondalık desteğini etkinleştirmek istiyorum.

Bir Microsoft temsilcisi, sonraki adımlar için iki ile üç iş günü içinde sizinle iletişim kuracaktır.

Bir geçiş istediğinizde, aşağıdaki ayrıntılara sahip olmanız ve bunları uygun şekilde planlamanız gerekir:

+ Verileri geçirmek için gereken süre sistemdeki veri miktarına bağlıdır. Büyük veritabanlarının geçiş işlemi birkaç gün sürebilir.
+ Veritabanı boyutu, geçiş işlemi çalışırken geçici olarak artar, çünkü dizinler için ek alan gereklidir. Geçiş tamamlandığında, ek alanın büyük bir çoğunluğu serbest kalır.
+ Geçiş işlemi sırasında, geçişin tamamlanmasını engelleyen hatalar oluşursa, sistem Microsoft Desteği'ne uyarıları gönderir ve Destek personeli müdahale edebilir. Ancak, geçiş sırasında hatalar oluşsa bile, Common Data Service olağan kullanım için tamamen kullanılabilir durumda kalır.
+ Geçiş işlemi geri alınamaz.

## <a name="changing-the-number-of-decimal-places"></a>Ondalık basamak sayısının değiştirilmesi

Geçiş tamamlandıktan sonra, Common Data Service daha fazla ondalık basamak içeren sayıları depolayabilir. Yöneticiler, belirli para birimi kodları ve fiyatlandırma için kaç ondalık basamak kullanılacağını seçebilirler. Microsoft Power Apps, Power BI, ve Power Automate kullanıcıları daha sonra daha fazla ondalık basamak içeren sayıları görüntüleyebilir ve kullanabilir.

Bu değişikliği yapmak için Power Apps'te aşağıdaki ayarları güncelleştirmeniz gerekir:

+ **Sistem Ayarları: Fiyatlandırma için para birimi duyarlığı** – **Sistem genelinde fiyatlandırma için kullanılan para birimi duyarlığını ayarla** alanı **Fiyatlandırma Duyarlığı**  seçildiğinde, para biriminin kuruluş için nasıl davranacağını tanımlar.
+ **İş Yönetimi: Para birimleri** – **Para Birimi Duyarlığı** alanı, belirli bir para birimi için özel bir ondalık basamak sayısı belirlemenizi sağlar. Kuruluş genelinde ayara geri dönüş vardır.

Bazı kısıtlamalar bulunur:

+ Bir varlık üzerinde para birimi alanını yapılandıramazsınız.
+ Yalnızca **Fiyatlandırma** ve **Hareket Para Birimi** düzeylerinde dörtten fazla ondalık basamak belirtebilirsiniz.

### <a name="system-settings-currency-precision-for-pricing"></a>Sistem Ayarları: Fiyatlandırma için para birimi duyarlığı

Geçiş tamamlandıktan sonra, yöneticiler para birimi duyarlığını ayarlayabilir. **Ayarlar \> Yönetim**'e gidin ve **Sistem Ayarları**'nı seçin. Daha sonra, **Genel** sekmesinde, **Sistem genelinde fiyatlandırma için kullanılan para birimi duyarlığını ayarla** alanındaki değeri aşağıda gösterildiği şekilde değiştirin.

![Para birimi sistem ayarları](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>İş Yönetimi: Para Birimleri

Belirli bir para birimi için para birimi duyarlığının fiyatlandırma için kullanılan para birimi duyarlığından farklı olmasını istiyorsanız, bunu değiştirebilirsiniz. **Ayarlar \> İş Yönetimi**'ne gidin **Para birimleri**'ni ve ardından değiştirilecek para birimini seçin. Sonra, aşağıdaki çizimde gösterildiği gibi, **Para Birimi Duyarlığı** alanını istediğiniz ondalık basamak sayısına ayarlayın.

![Belirli bir yerel ayarın para birimi ayarları](media/specific-currency.png)

### <a name="entities-currency-field"></a>Varlıklar: Para birimi alanı

Belirli para birimi alanları için yapılandırılabilecek ondalık basamak sayısı dört ile sınırlıdır.