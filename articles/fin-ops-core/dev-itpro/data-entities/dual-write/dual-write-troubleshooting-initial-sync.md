---
title: Başlangıç eşitlemesi sırasında sorunları giderme
description: Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: e4ee3bf07a1df445875197f38f655464cc9b44d3
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443861"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Başlangıç eşitlemesi sırasında sorunları giderme

[!include [banner](../../includes/banner.md)]

Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finance and Operations uygulamadaki ilk eşitleme hatalarını denetle

Eşleme şablonları etkinleştirildikten sonra, haritaların durumu **çalışıyor** olmalıdır. Durum **çalışmıyorsa**, ilk eşitleme sırasında hata meydana geldi. Hataları görüntülemek için **çift-yazma** sayfasında **ilk eşitleme ayrıntıları** sekmesini seçin.

![İlk eşitleme ayrıntıları sekmesinde hata](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>İlk eşitlemeyi tamamlayamıyoruz: 400 Hatalı Istek

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Eşlemeyi ve ilk senkronizasyonu çalıştırmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*(\[Hatalı İstek\], Uzak sunucu hata verdi: (400) Hatalı İstek.), AX dışarı aktarma işlemi bir hatayla karşılaştı*

Burada tam hata mesajı tablosu için bir örnek verilmiştir.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Bu hata sürekli olarak oluşuyorsa ve ilk eşitlemeyi tamamlayamıyorsa, sorunu düzeltmek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.
2. Microsoft Yönetim Konsolu 'Nu açın.
3. **Hizmetler** bölmesinde, Microsoft Dynamics 365 veri alma verme çerçevesi hizmetinin çalışmakta olduğundan emin olun. Durdurulmuşsa, ilk eşitleme gerektirdiğinden yeniden Başlat.

## <a name="initial-synchronization-error-403-forbidden"></a>İlk eşitleme hatası: 403 Yasak

İlk eşitlemede aşağıdaki hata iletisini alabilirsiniz:

*(\[Yasak\], Uzak sunucu hata verdi: (403) Yasak), AX dışarı aktarma bir hatayla karşılaştı*

Sorunu düzeltmek için şu adımları izleyin.

1. Finance and Operations Uygulamaya oturum açın.
2. **Azure Active Directory uygulamalar** sayfasında **DtAppID** istemcisini silin ve sonra yeniden ekleyin.

![Azure AD uygulamaları listesinde DtAppID istemcisi](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>İlk eşitleme sırasında kendi kendine referans veya döngüsel referans hataları

Eşlemelerinizin kendi kendine veya çevresel referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz: Hatalar aşağıdaki kategorilere ayrılır:

- [Satıcılar V2–to–msdyn_vendors varlık eşlemesinde hatalar](#error-vendor-map)
- [Müşteriler V3–to–Accounts varlık eşlemesinde hatalar](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Satıcılar V2–to–msdyn_vendors varlık eşlemesinde hataları çözümleme

Varlıkların, **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarında değerleri bulunan mevcut kayıtları varsa **Satıcılar V2** ile **msdyn\_vendors** eşlemesinde ilk eşitleme hatalarıyla karşılaşabilirsiniz. Bu hatalar **InvoiceVendorAccountNumber** kendi kendine başvuran bir alan olduğundan ve **PrimaryContactPersonId** satıcı eşlemede döngüsel bir başvuru olduğundan gerçekleşir.

Aldığınız hata iletileri aşağıdaki şekilde olacaktır.

*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Burada bazı örnekler verilmiştir:

- *Alan için GUID çözümlenemedi: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Alan için GUID çözümlenemedi: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Arama bulunamadı: V24-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Satıcı varlığında **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanında değerleri bulunan kayıtlarınız varsa, ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin.

1. Finance and Operations uygulamada, eşlemeden önce **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarını silin ve ardından eşlemeyi kaydedin.

    1. **Satıcılar v2 (msdyn\_vendors)** için ikili yazma eşleme sayfasında, **Varlık eşlemeleri** sekmesinde, sol filtrede **Finance and Operations apps.Vendors V2**'yi seçin. Sağ filtrede, **Sales.Vendor**'u seçin.
    2. **primarycontactperson**'ı arayıp **PrimaryContactPersonId** kaynak alanını bulur .
    3. **Eylemler**'i ve sonra **Sil**'i seçin.

        ![PrimaryContactPersonId alanını silme](media/vend_selfref3.png)

    4. **InvoiceVendorAccountNumber** alanını silmek için bu adımları tekrarlayın.

        ![InvoiceVendorAccountNumber alanını silme](media/vend-selfref4.png)

    5. Değişikliklerinizi eşlemeye kaydedin.

2. **Satıcılar V2** varlığı için değişiklik izlemeyi kapatın.

    1. **Veri yönetimi** çalışma alanında **Veri varlıkları** kutucuğunu seçin.
    2. **Satıcılar V2** tüzel kişiliğini seçin.
    3. Eylem Bölmesinde, **Seçenekler**'i ve sonra **Değişiklik izleme**'yi seçin.

        ![Değişiklik izleme seçeneğini belirleme](media/selfref_options.png)

    4. **Değişiklik izlemeyi devre dışı bırak**'ı seçin.

        ![Değişiklik İzlemeyi Devre Dışı Bırak'ı seçme](media/selfref_tracking.png)

3. **Satıcı v2 (msdyn\_vendors)** eşlemesinin ilk eşitlemesini çalıştırın. İlk eşitleme hatasız olarak çalışmalıdır.
4. **CDS İlgili Kişileri V2 (ilgili kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın. İlk eşitlemenin ilgili kişi kayıtları için de yapılması gerektiğinden, satıcı varlığındaki birincil ilgili kişi alanını eşitlemek istiyorsanız bu eşlemeyi eşitlemeniz gerekir.
5. **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarını **Satıcılar v2 (msdyn\_vendors)** eşlemesine geri ekleyin ve eşlemeyi kaydedin.
6. **Satıcı v2 (msdyn\_vendors)** eşlemesinin ilk eşitlemesini yeniden çalıştırın. Değişiklik izleme devre dışı bırakıldığından tüm kayıtlar eşitlenecek.
7. **Satıcılar V2** varlığı için değişiklik izlemeyi yeniden açın.

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a>Müşteriler V3 ile Hesaplar varlık eşlemesinde hataları giderme

Varlıkların, **ContactPersonID** ve **InvoiceAccount** alanlarında değerleri bulunan mevcut kayıtları varsa **Müşteriler V3** ile **Hesaplar** eşlemesinde ilk eşitleme hatalarıyla karşılaşabilirsiniz. Bu hataların oluşma nedeni, **InvoiceAccount** alanının kendine başvuruda bulunan bir alan olması ve **ContactPersonID**'nin satıcı eşlemesindeki döngüsel bir başvuru olmasıdır.

Aldığınız hata iletileri aşağıdaki şekilde olacaktır.

*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Burada bazı örnekler verilmiştir:

- *Alan için GUID çözümlenemedi: primarycontactid.msdyn\_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Alan için GUID çözümlenemedi: msdyn\_billingaccount.accountnumber. Arama bulunamadı: 1206-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Müşteri varlığında **ContactPersonID** ve **InvoiceAccount** alanında değerleri bulunan kayıtlarınız varsa, ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin. Bu yaklaşımı, **Hesaplar** ve **İlgili kişiler** gibi, kutudan çıkan herhangi bir varlık için kullanabilirsiniz.

1. Finance and Operations uygulamada, **Müşteriler V3 (firmalar)** eşlemesinden önce **ContactPersonID** ve **InvoiceAccount** alanlarını silin ve değişiklikleri kaydedin.

    1. **Müşteriler V3 (firmalar)** için ikili yazma eşleme sayfasında, **Varlık eşlemeleri** sekmesinde, sol filtrede, **Finance and Operations app.Customers V3** öğesini seçin. Sağ filtrede, **Common Data Service.Firma**'yı seçin.
    2. **contactperson**'ı arayıp **ContactPersonID** kaynak alanını bulur .
    3. **Eylemler**'i ve sonra **Sil**'i seçin.

        ![ContactPersonID alanını silme](media/cust_selfref3.png)

    4. **InvoiceAccount** alanını silmek için bu adımları tekrarlayın.

        ![InvoiceAccount alanını silme](media/cust_selfref4.png)

    5. Değişikliklerinizi eşlemeye kaydedin.

2. **Müşteriler V3** varlığı için değişiklik izlemeyi kapatın.

    1. **Veri yönetimi** çalışma alanında **Veri varlıkları** kutucuğunu seçin.
    2. **Müşteriler V3** tüzel kişiliğini seçin.
    3. Eylem Bölmesinde, **Seçenekler**'i ve sonra **Değişiklik izleme**'yi seçin.

        ![Değişiklik izleme seçeneğini belirleme](media/selfref_options.png)

    4. **Değişiklik izlemeyi devre dışı bırak**'ı seçin.

        ![Değişiklik İzlemeyi Devre Dışı Bırak'ı seçme](media/selfref_tracking.png)

3. **Müşteriler V3 (Hesaplar)** eşlemesi için başlangıç eşitlemesini çalıştırın. İlk eşitleme hatasız olarak çalışmalıdır.
4. **CDS İlgili Kişileri V2 (ilgili kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın.

    > [!NOTE]
    > Aynı ada sahip iki eşleme var. **Ayrıntılar** sekmesinde şu açıklama bulunan eşlemeyi seçtiğinizden emin olun: **FO.CDS Satıcı İlgili Kişileri V2 ile CDS.İlgili Kişileri arasında eşitleme için çift yazma şablonu. \[Dynamics365SupplyChainExtended\] yeni paketini gerektirir.**

5. **Müşteriler V3 (Hesaplar)** eşlemesinden önce **ContactPersonId** ve **InvoiceAccount** alanlarını silin ve değişiklikleri kaydedin. Şimdi, hem **InvoiceAccount** alanı hem de **ContactPersonId** alanı yeniden canlı eşitleme modunun parçası olarak kullanılır. Sonraki adımda, bu alanlar için başlangıç eşitlemesini tamamlayacaksınız.
6. **Müşteriler V3 (Hesaplar)** eşlemesi için başlangıç eşitlemesini yeniden çalıştırın. Değişiklik izleme devre dışı bırakıldığından, **InvoiceAccount** ve **ContactPersonId** için veriler Finance and Operations uygulamasından Common Data Service'e eşitlenecektir.
7. **InvoiceAccount** ve **ContactPersonId** için verileri Common Data Service'dan Finance and Operations uygulamasına eşitlemek için bir veri tümleştirme projesi kullanmanız gerekir.

    1. Power Apps içinde , **Satış. firma** ve **Finance and Operations apps.Customers V3** varlıkları arasında veri entegrasyonu projesi oluşturunuygulamalar arasında bir veri tümleştirme projesi oluşturun. Veri yönü, Common Data Service'ten Finance and Operations uygulamasına olmalıdır. **InvoiceAccount** çift yazmada yeni bir öznitelik olduğundan, bunun için ilk eşitlemeyi atlamak isteyebilirsiniz. Daha fazla bilgi için bkz. [Common Data Service'e veri entegre edin](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Aşağıdaki resimde **CustomerAccount** ve **ContactPersonId**'yi güncelleştiren bir proje gösterilmektedir .

        ![CustomerAccount ve ContactPersonId alanını güncelleştirmek için veri tümleştirme projesi](media/cust_selfref6.png)

    2. Finance and Operations uygulamasında, filtre ölçütleriyle eşleşen kayıtlar güncelleştirilecek şekilde şirket ölçütlerini Common Data Service  tarafına ekleyin. Filtre eklemek için filtre düğmesini seçin. Ardından, **Sorguyu düzenle** iletişim kutusunda **\_msdyn\_company\_value eq '\<guid\>'** gibi bir filtre sorgusu ekleyebilirsiniz. 

        > [NOT] Filtre düğmesi yoksa, veri tümleştirme ekibinin kiracınızda filtre yeteneğini etkinleştirmesini istemek için bir destek bileti oluşturun.

        **\_msdyn\_company\_value** için bir filtre sorgusu girmezseniz , tüm kayıtlar eşitlenir.

        ![Filtre sorgusu ekleme](media/cust_selfref7.png)

    Kayıtların ilk eşitlenme işlemi şimdi tamamlandı.

8. Finance and Operations uygulamasında, **Müşteriler V3** varlığı için değişiklik izlemeyi yeniden açın.