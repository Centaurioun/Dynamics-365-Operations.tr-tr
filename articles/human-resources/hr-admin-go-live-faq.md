---
title: Servise almayla ilgili SSS
description: Bu konu, bir Dynamics 365 Human Resources uygulama projesiyle uygulamaya geçme ile ilgili sık sorulan soruları listeler.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a85840be328702a06779390fe383fd1896fd04
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011444"
---
# <a name="go-live-faq"></a>Servise almayla ilgili SSS 

Bu konu, bir Dynamics 365 Human Resources uygulama projesiyle uygulamaya geçme ile ilgili sık sorulan soruları listeler. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Üretim ortamımı ne zaman konfigüre edebilir ve isteyebilirim? 

Tipik olarak, üretim ortamı aşağıdaki ölçütler karşılandıktan sonra dağıtılır:

- Tüm özelleştirmelerin kodları tamamlanmıştır.
- Kullanıcı kabul sınamaları (UAT) tamamlanmıştır.
- Müşteri, çözümü onaylamıştır.
- Uygulamaya geçmeyi engelleyici bir sorun yoktur. 

Uygun müşteriler bu aşamada olduğunda, Microsoft FastTrack ekibi, proje ekibiyle birlikte bir uygulamaya geçme değerlendirmesi yapacaktır. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Üretim ortamını dağıtma önkoşulları nelerdir? 

Önkoşulların listesi için, bkz  [Uygulamaya geçmeye hazırlık](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Uygulamaya geçme değerlendirmesi nedir?  

Uygulamaya geçme değerlendirmesi,  [Microsoft FastTrack programının](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview) bir parçasıdır. Bu İnceleme sırasında, bir çözüm mimarı uygulama projesinin başarılı bir kesin bitiş ve uygulamaya geçme için hazır olup olmadığını değerlendirir. Üretim ortamında uygulamaya geçmeyi isteyebilmeniz için, bu inceleme her uygulama projesi için zorunludur. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Korumalı alan ortamlarımız Orta ABD veri merkezinde dağıtılır. Üretim ortamlarımızın Batı ABD veri merkezi'nde dağıtılmasını istiyoruz. Üretim konfigürasyonumda veri merkezi olarak Batı ABD'yi seçebilir miyim? 

LCS, İnsan Kaynakları ortamı dağıttığınızda farklı bir veri merkezi seçmenizi engellemez, ancak farklı bir veri merkezini seçmemenizi önemle öneririz.  

Üretim ortamınızın Batı ABD veri merkezinde olmasını istiyorsanız, önce korumalı alan ortamlarınızı Batı ABD veri merkezine yeniden dağıtmanız, test etmeniz ve onaylamanız gerekir. 

Doğru veri merkezini seçme hakkında bilgi için bkz. [ağ gereksinimleri](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>İnsan Kaynakları ortamlarım için Azure kaynaklarına hangi düzeyde erişime sahibim?  

İnsan Kaynakları ortamlara erişim sınırlıdır. Sanal makineye (VM) veya Microsoft Internet Information Services'a (IIS) erişemezsiniz. Ayrıca, veritabanına Microsoft SQL Server Management Studio üzerinden erişemezsiniz. 

Azure kaynaklarınıza veya Dynamics 365 Human Resources ortamınıza doğrudan erişemeseniz de verilerinize erişmek için kullanabileceğiniz ek özellikler vardır:

- Azure SQL veritabanını kendi Azure kiracınıza dağıtabilir ve verileri eşitlemek için kendi veritabanınızı getirin (BYOD) özelliğini kullanabilirsiniz. Daha fazla bilgi için bkz. [Kendi veritabanınızı getirme (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Belirli varlıkları Common Data Service veritabanıyla senkronize etmek için Common Data Service tümleştirmesini kullanabilirsiniz. Daha fazla bilgi için bkz. [Common Data Service varlıkları](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Üretim veritabanı ne sıklıkta yedeklenir? 

Veritabanları otomatik yedeklemeler tarafından aşağıdaki sıklıklarda korunur:

| Yedekleme türü | Sıklık |
| --- | --- |
| Tam veritabanı yedekleme | Weekly |
| Farklı veritabanı yedekleme | Her 12-24 saatte bir |
| İşlem günlüğü yedeklemesi | Her 5-10 dakikada bir |

Microsoft, son yedi gün içinde belirli bir noktaya geri yüklemeye (PITR) izin vermek için yeterli yedeği saklar. 

Daha fazla bilgi için bkz.  [Otomatik SQL Veritabanı yedeklemeleri hakkında daha fazla bilgi alın](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Üretim veritabanımın yedeğinin bir kopyasını isteyebilir miyim? 

Hayır. Ancak üretim ortamınızı korumalı alan ortamınıza kopyalamak için veritabanı yenileme hizmeti isteği gönderebilirsiniz. Azure SQL veritabanını kendi Azure kiracınıza dağıtabilir ve üretim ortamınızdan verileri eşitlemek için BYOD özelliğini kullanabilirsiniz. Daha fazla bilgi için bkz. [Kendi veritabanınızı getirme (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Korumalı alan ortamımı uygulamaya geçirmek üzere üretime nasıl taşıyabilirim? 

Ortamınızı bir korumalı alan ortamından üretim ortamına taşımak için kullanılabilecek bir kopya özelliği olmadığından, verileri üretim ortamınıza taşımak için veri paketlerini kullanmanız gerekir.  

Proje boyunca korumalı alanda yapılandırılmış varlıkların açık bir listesini tutmanızı öneririz. Daha sonra, uygulamaya geçirme işleminiz için gereken tüm veri paketlerinin kesin bitiş ve geçiş işlemlerini sınayın. Uygulamaya geçmeye hazır olduğunuzda, tüm veri paketlerini üretim ortamına el ile taşımanız gerekir. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Üretim ortamım arızalıyla ne yapmam gerekir? 

Üretim kesintisi bildirmek için,  [üretim kesintisi bildir](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) bölümünde açıklanan süreci izleyin. 

 ## <a name="see-also"></a>Ayrıca bkz.

 [Servise almak için hazırlama](hr-admin-go-live-prepare.md)