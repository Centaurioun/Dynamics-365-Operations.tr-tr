---
title: Field Service'taki iş emirlerini Finance and Operations'taki satış siparişleriyle eşitleme
description: Bu konu, Field Service'taki iş emirlerini Finance and Operations'daki satış siparişleriyle eşitlemek için kullanılan şablonları ve temel görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 49cb5942532e4feab64aa271ebfecf5cb60b1c61
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562730"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Field Service'taki iş emirlerini Finance and Operations'taki satış siparişleriyle eşitleme

[!include[banner](../includes/banner.md)]

Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service üzerinden Microsoft Dynamics 365 for Finance and Operations satış siparişine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/field-service-integration.png)](./media/field-service-integration.png)

Bu konu, Field Service'taki iş emirlerini Finance and Operations'daki satış siparişleriyle eşitlemek için kullanılan şablonları ve temel görevleri açıklar.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Aşağıdaki şablonlar, Field Service'taki iş emirlerini Finance and Operations'daki satış siparişleriyle eşitleme işi çalıştırmak için kullanılan şablonları ve temel görevleri açıklar.

### <a name="names-of-the-templates-in-data-integration"></a>Veri tümleştirmesindeki şablonların adları:

**İş emirlerini Satış siparişlerine (Field Service'tan Fin and Ops'a)** şablonu eşitlemeyi çalıştırmak için kullanılır.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Veri tümleştirme projesindeki görevlerin adları

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Aşağıdaki eşitleme görevleri, satış siparişi başlıkları ve satırlarının eşitlemesi gerçekleştirilmeden önce gereklidir.

- Field Service Ürünleri (Fin and Ops'tan Field Service'a)
- Hesaplar (Sales'ten Fin and Ops'a) - Doğrudan

## <a name="entity-set"></a>Varlık kümesi

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS satış siparişi başlıkları |
| msdyn_workorderservices | CDS satış siparişi satırları   |
| msdyn_workorderproducts | CDS satış siparişi satırları   |

## <a name="entity-flow"></a>Varlık akışı

İş emirleri Field Service'ta oluşturulur. İş emirleri yalnızca harici olarak tutulan ürünleri içerirse ve **İş emri durumu** **Açık-Zamanlanmamış** ve **Kapalı-İptal edildi** değerinden farklıysa, iş emirleri CDS Veri tümleştirme projesi aracılığıyla Finance and Operations'a eşitlenebilir. İş emirlerindeki güncelleştirmeler Finance and Operations'da satış siparişleri olarak eşitlenir. Bu güncelleştirmeler kaynak türü ve durum hakkındaki bilgileri içerir.

## <a name="estimated-versus-used"></a>Tahmini Kullanılan karşılaştırması

Field Service'ta, iş emirlerindeki ürünlerin ve hizmetlerin miktarlar ve tutarlar için hem **Tahmini** hem de **Kullanılan** değerleri bulunur. Bununla birlikte, Finance and Operations'da, satış siparişleri için **Tahmini** ve **Kullanılan** değerleri kavramı yoktur. Finance and Operations'da satış siparişindeki beklenen miktarı kullanan ürün tahsisatını desteklemek, ancak tüketilmesi ve faturalanması gereken kullanılan miktarı tutmak için iki görev kümesi iş emrinde ürünleri ve hizmetleri eşitler. Görev kümelerinden biri **Tahmini** değerleri için diğer görev kümesi **Kullanılan** değerleri içindir.

Bu davranış Finance and Operations'da tahmini değerlerin tahsisat veya rezervasyon için kullanıldığı senaryolar sağlar ve kullanılan değerler tüketim ve faturalama için kullanılır.

### <a name="estimated"></a>Tahmini

Ürün satırlarını eşitlemek için **Satır durumu** değeri **Tahmini**, **Tahsis edilen** seçeneği **Evet** ve **Sistem durumu** değeri **Kapalı - Deftere Nakledildi** olduğunda **Tahmini** değerler kullanılır.

Hizmet satırlarını eşitlemek için **Satır durumu** değeri **Tahmini**, ve **Sistem durumu** değeri **Kapalı - Deftere Nakledildi** olduğunda **Tahmini** değerler kullanılır.

### <a name="used"></a>Kullanılan

**Kullanılan** değerler tüketim ve faturalama için kullanılır. Bu durumda, **Kullanılan** değerleri eşitlenir.

Aşağıdaki tabloda ürün satılarına ilişkin çeşitli birleşimlere genel bakış sağlanır.

| Sistem Durumu <br>(Field Service) | Satır Durumu <br>(Field Service) | Tahsis edilen <br>(Field Service) |Eşitlenen değer <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Açık - Planlandı   | Tahmini   | Evet       | Tahmini                       |
| Açık - Planlandı   | Tahmini   | Hayır        | Kullanılan                            |
| Açık - Planlandı   | Kullanılan        | Evet       | Kullanılan                            |
| Açık - Planlandı   | Kullanılan        | Hayır        | Kullanılan                            |
| Açık - Devam ediyor | Tahmini   | Evet       | Tahmini                       |
| Açık - Devam ediyor | Tahmini   | Hayır        | Kullanılan                            |
| Açık - Devam ediyor | Kullanılan        | Evet       | Kullanılan                            |
| Açık - Devam ediyor | Kullanılan        | Hayır        | Kullanılan                            |
| Açık - Tamamlandı   | Tahmini   | Evet       | Tahmini                       |
| Açık - Tamamlandı   | Tahmini   | Hayır        | Kullanılan                            |
| Açık - Tamamlandı   | Kullanılan        | Evet       | Kullanılan                            |
| Açık - Tamamlandı   | Kullanılan        | Hayır        | Kullanılan                            |
| Kapalı - Deftere nakledildi    | Tahmini   | Evet       | Kullanılan                            |
| Kapalı - Deftere nakledildi    | Tahmini   | Hayır        | Kullanılan                            |
| Kapalı - Deftere nakledildi    | Kullanılan        | Evet       | Kullanılan                            |
| Kapalı - Deftere nakledildi    | Kullanılan        | Hayır        | Kullanılan                            |

Aşağıdaki tabloda hizmet satılarına ilişkin çeşitli birleşimlere genel bakış sağlanır.

| Sistem Durumu <br>(Field Service) | Satır Durumu <br>(Field Service) | Eşitlenen değer <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Açık - Planlandı   | Tahmini   | Tahmini |
| Açık - Planlandı   | Kullanılan        | Kullanılan      |
| Açık - Devam ediyor | Tahmini   | Tahmini |
| Açık - Devam ediyor | Kullanılan        | Kullanılan      |
| Açık - Tamamlandı   | Tahmini   | Tahmini |
| Açık - Tamamlandı   | Kullanılan        | Kullanılan      |
| Kapalı - Deftere nakledildi    | Tahmini   | Kullanılan      |
| Kapalı - Deftere nakledildi    | Kullanılan        | Kullanılan      |

**Tahmini** değerlerin **Kullanılan** değerlere karşı eşitlenmesi ürün satırları ve hizmet satırları için iki görev kümesiyle yönetilir. Önceden tanımlanmış filtreler doğru görevi tetikler ve temel eşleme **Beklenen** değerlerin **Kullanılan** değerlere karşı doğru değerlerle eşitlenmesini sağlamaya yardımcı olur.

### <a name="example"></a>Örnek

1. Field Service'ta bir iş emri oluşturulur ve planlanır.

    **Sistem Durumu** değeri **Açık – Planlandı**'dır.

    - **Ürün satırı:** Tahmini miktar = 5ea, Kullanılan miktar = 0ea, Satır durumu = Tahmini, Tahsis edilen = Hayır
    - **Hizmet satırı:** Tahmini miktar= 2 s, Kullanılan miktar = 0 h, Satır durumu = Tahmini

    Bu örnekte, ürünün **0** (sıfır) olan **kullanılan miktar** değeri ve hizmetin **2s** olan **Tahmini Miktar** değeri Finance and Operations ile eşitlenir.

2. Ürünler Field Service'ta tahsis edilir.

    **Sistem Durumu** değeri **Açık – Planlandı**'dır.

    - **Ürün satırı:** Tahmini miktar = 5ea, Kullanılan miktar = 0ea, Satır durumu = Tahmini, Tahsis edilen = Evet
    - **Hizmet satırı:** Tahmini miktar= 2 s, Kullanılan miktar = 0 h, Satır durumu = Tahmini

    Bu örnekte, ürünün **5ea** olan **Tahmini miktar** değeri ve hizmetin **2s** olan **Tahmini Miktar** değeri Finance and Operations ile eşitlenir.

3. Servis teknisyeni iş emrinde çalışmaya başlar ve 6 malzeme kullanımını kaydeder.

    **Sistem Durumu** değeri **Açık – Devam Ediyor**'dur.

    - **Ürün satırı:** Tahmini miktar = 5ea, Kullanılan miktar = 6ea, Satır durumu = Kullanıldı, Tahsis edilen = Evet
    - **Hizmet satırı:** Tahmini miktar= 2 s, Kullanılan miktar = 0 h, Satır durumu = Tahmini

    Bu örnekte, ürünün **6** olan **kullanılan miktar** değeri ve hizmetin **2s** olan **Tahmini Miktar** değeri Finance and Operations ile eşitlenir.

4. Servis teknisyeni iş emrini tamamlar ve 1,5 saat kullanılan zaman kaydeder.

    **Sistem Durumu** değeri **Açık – Tamamlandı**'dır.

    - **Ürün satırı:** Tahmini miktar = 5ea, Kullanılan miktar = 6ea, Satır durumu = Kullanıldı, Tahsis edilen = Evet
    - **Hizmet satırı:** Tahmini miktar= 2 s, Kullanılan miktar = 1,5 s, Satır durumu = Kullanıldı

    Bu örnekte, ürünün **6** olan **kullanılan miktar** değeri ve hizmetin **1,5s** olan **Kullanılan Miktar** değeri Finance and Operations ile eşitlenir.

## <a name="sales-order-origin-and-status"></a>Satış siparişi kaynağı ve durumu

### <a name="sales-origin"></a>Satış menşei

Finance and Operations'ta kaynağı iş emirleri olan satış siparişlerini takip etmek için **Kaynak türü ataması** seçeneğinin **Evet** ve **Satış kaynağı türü** alanının **İş emri tümleştirmesi** olarak ayarlandığı bir satış kaynağı oluşturabilirsiniz.

Varsayılan olarak, eşleme iş emirlerinden oluşturulan tüm satış siparişleri için **İş emri tümleştirmesi** satış kaynağı türü için satış kaynağını seçer. Bu davranış Finance and Operations'da satış siparişiyle çalışırken yararlı olabilir. Kaynağı iş emirleri olan satış siparişlerinin Field Service'a yeniden iş emirleri olarak eşitlenmemesini sağlamanız gerekir.

Finance and Operations'da doğru satış kaynağı kurulumunu oluşturma ayrıntıları için bu konunun "Önkoşullar ve eşleme kurulumu" bölümüne bakın.

### <a name="status"></a>Durum

Satış siparişinin kaynağı bir iş emri olduğunda, **Harici iş emri durumu**alanı satış siparişi başlığının **Kurulum** sekmesinde görüntülenir. Bu alan Field Service'daki iş emrinden gelen sistem durumunu göstererek Finance and Operations'daki satış siparişlerinin eşitlenen iş emri durumunun izlenmesine yardımcı olur. Bu alan Finance and Operations kullanıcısının satış siparişinin ne zaman sevk edilmesi veya faturalanması gerektiğini belirlemesine yardımcı olur.

**Harici iş emri durumu** alanı aşağıdaki değerleri içerebilir:

- Açık - Planlandı
- Açık - Devam ediyor
- Açık - Tamamlandı
- Kapalı - Deftere nakledildi

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü

Field Service ile Finance and Operations arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir. Çözüm aşağıdaki değişiklikleri içerir.

### <a name="work-order-entity"></a>İş Emri varlığı

**İş Emri** varlığına **Yalnızca Harici Olarak Tutulan Ürünleri Var** alanı eklenir ve sayfada görüntülenir. Bu, bir iş emrinin tamamen harici olarak tutulan ürünlerden oluşup oluşmadığını sürekli olarak izlemek için kullanılır. Tüm ilgili ürünler Finance and Operations'ta korunduğunda iş emri tamamen harici olarak tutulan ürünlerden oluşur. Bu alan, kullanıcıların Finance and Operations tarafından bilenmeyen ürünlere sahip iş emirlerini eşitlememesini garanti etmeye yardımcı olur.

### <a name="work-order-product-entity"></a>İş Emri Ürün varlığı

- **İş Emri Ürünü** varlığına **Siparişte Yalnızca Harici Olarak Tutulan Ürünler Var** alanı eklenir ve sayfada görüntülenir. İş emri ürününün Finance and Operations'ta tutulup tutulmadığını sürekli olarak izlemek üzere kullanılır. Bu alan, kullanıcıların Finance and Operations tarafından bilenmeyen iş emri ürünlerini eşitlememesini garanti etmeye yardımcı olur.
- **İş Emri Ürünü** varlığına **Başlık Sistem Durumu** alanı eklenir ve sayfada görüntülenir. İş emrinin sistem durumunu sürekli olarak izlemek için kullanılır ve iş emri ürünleri Finance and Operations'a eşitlenirken doğru filtreleme yapılmasını sağlamaya yardımcı olur. Filtreleri tümleştirme görevlerinde ayarlandığında, **Başlık Sistem Durumu** bilgileri tahmini veya kullanılan değerlerin eşitlenip eşitlenmeyeceğini belirlemek için de kullanılır.
- **Faturalanan Birim Tutarı** alanı kullanılan geçerli birim başına faturalanan tutarı gösterir. Değer **Toplam tutar** değeri olarak hesaplanır ve **Fiili Miktar** değere bölünür. Alan, kullanılan miktar ve faturalanan miktar için farklı değerler desteklemeyen sistemlerin tümleştirilmesi için kullanılır. Bu alan kullanıcı arabiriminde (UI) görünmez. 
- **Faturalanan İskonto Tutarı** alanı **İskonto Tutarı** değeri artı **Faturalanan Birim Tutarı** değeri hesaplamasının yuvarlaması olarak hesaplanır. Bu alan, tümleştirme için kullanılır ve kullanıcı arabiriminde görüntülenmez.
- **Ondalık Miktarı** alanı **Miktar** alanındaki değeri ondalık sayı olarak depolar. Bu alan, tümleştirme için kullanılır ve kullanıcı arabiriminde görüntülenmez. 
- İş emri ürününün **Satır durumu** değeri **Kullanılan** yerine **Tahmini** olarak değiştirilirse **Kullanılan** alanlarındaki değer **0** (sıfır) olarak sıfırlanır. Bu değişiklik, yanlışlıkla girilen bir kullanılan miktarın **Satır durumu** değeri **Tahmini** ve **Tahsis edilen** seçeneği **Hayır** olarak ayarlandığında eşitleme için kullanılmasını engellemeye yardımcı olur.

### <a name="work-order-service-entity"></a>İş Emri Hizmet varlığı

- **İş Emri Hizmet** varlığına **Siparişte Yalnızca Harici Olarak Tutulan Ürünler Var** alanı eklenir ve sayfada görüntülenir. İş emri hizmetinin Finance and Operations'ta tutulup tutulmadığını sürekli olarak izlemek üzere kullanılır. Bu alan, kullanıcıların Finance and Operations tarafından bilenmeyen iş emri hizmetlerini eşitlememesini garanti etmeye yardımcı olur.
- **İş Emri Hizmeti** varlığına **Başlık Sistem Durumu** alanı eklenir ve sayfada görüntülenir. İş emrinin sistem durumunu sürekli olarak izlemek için kullanılır ve iş emri hizmetleri Finance and Operations'a eşitlenirken doğru filtreleme yapılmasını sağlamaya yardımcı olur. Filtreleri tümleştirme görevlerinde ayarlandığında, **Başlık Sistem Durumu** bilgileri tahmini veya kullanılan değerlerin eşitlenip eşitlenmeyeceğini belirlemek için de kullanılır.
- **Saat cinsinden süre** alanı değeri dakikadan saate dönüştürdükten sonra **Süre** alanındaki değeri depolar. Bu alan, tümleştirme için kullanılır ve kullanıcı arabiriminde görüntülenmez.
- **Saat cinsinden tahmini süre** alanı değeri dakikadan saate dönüştürdükten sonra **Tahmini Süre** alanındaki değeri depolar. Bu alan, tümleştirme için kullanılır ve kullanıcı arabiriminde görüntülenmez.
- **Faturalanan Birim Tutarı** alanı kullanılan geçerli birim başına faturalanan tutarı depolar. Değer **Toplam tutar** değeri olarak hesaplanır ve **Fiili Miktar** değere bölünür. Bu alan, kullanılan miktar ve faturalanan miktar için farklı değerler desteklemeyen sistemlerin tümleştirilmesi için kullanılır. Alan kullanıcı arabiriminde (UI) görünmez.
- **Faturalanan İskonto Tutarı** alanı **İskonto Tutarı** değeri artı **Faturalanan Birim Tutarı** değeri hesaplamasının yuvarlaması olarak hesaplanır. Bu alan, tümleştirme için kullanılır ve kullanıcı arabiriminde görüntülenmez.
- **Harici Satır Siparişi** alanı, iş emri ürün ve hizmet satırlarının birleştirildiği harici sistemlerde kullanılabilen hesaplanmış negatif satış siparişi numarasıdır. Bu alan, pozitif satır sayıları olacak şekilde eklenen iş emri ürünlerine ve iş emri hizmetlerinin negatif satır sayıları olmasını sağlar. Bu alanın değeri -1 ile çarpılan **Satır Siparişi** değeri olarak hesaplanır. Bu alan kullanıcı arabiriminde (UI) görünmez.
- İş emri hizmetinin **Satır durumu** değeri bir nedenle **Kullanılan** yerine **Tahmini** olarak değiştirilirse **Kullanılan** alanlarındaki değer **0** (sıfır) olarak sıfırlanır. Bu değişiklik, yanlışlıkla girilen bir kullanılan miktarın **Satır durumu** değeri **Tahmini** ve **Başlık Sistem Durumu** seçeneği **Kapalı - Deftere Nakledildi** olarak ayarlandığında eşitleme için kullanılmasını engellemeye yardımcı olur.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

İş emirlerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:

### <a name="setup-in-field-service"></a>Field Service'ta kurulum

- Field Service'taki iş emirleri için kullanılan numara serilerinin Finance and Operations'taki satış siparişleri için kullanılan numara serisiyle çakışmadığından emin olun. Aksi durumda, mevcut satış siparişleri Field Service veya Finance and Operations'ta hatalı şekilde güncelleştirilebilir.
- **İş Emri Fatura Oluşturma** alan **Hiçbir zaman** olarak ayarlanmalıdır, bunun nedeni faturalamanın Finance and Operations'dan yapılacak olmasıdır. **Field Service** \> **Ayarlar** \> **Yönetim** \> **Field Service Ayarları**'na gidin ve **İş Emri Fatura Oluşturma** alanının **Hiçbir Zaman** olarak ayarlandığından emin olun.

### <a name="setup-in-finance-and-operations"></a>Finance and Operations'ta kurulum

İş emri tümleştirmesi satış kaynağı ayarlamanızı gerektirir. Satış kaynağı Finance and Operations'ta Field Service'taki iş emirlerinden oluşturulmuş olan satış siparişlerinin ayrılması için kullanılır. Satış siparişinin **İş emri tümleştirmesi** türünde bir satış kaynağı olduğunda **Harici iş emri durumu** alanı satış siparişi başlığında görüntülenir. Ayrıca, satış kaynağı Field Service'taki iş emirlerinden oluşturulmuş olan satış siparişlerinin Finance and Operations'tan Field Service'a satış siparişi eşitlemesi sırasında filtrelenmesini sağlamaya yardımcı olur.

1. **Satış ve pazarlama** \> **Kurulum** \> **Satış siparişleri** \> **Satış kaynağı** seçeneğine gidin.
2. **Yeni**'yi seçerek yeni bir satış kaynağı oluşturun.
3. **Satış kaynağı** alanına, satış kaynağı için **WorkOrder** gibi bir ad girin.
4. **Açıklama** alanında, **Field Service İş Emri** gibi bir açıklama girin.
5. **Kaynak türü ataması** onay kutusunu seçin.
6. **Satış kaynağı türü** alanını **İş emri tümleştirmesi** olarak ayarlayın.
7. **Kaydet**'i seçin.


### <a name="setup-in-data-integration"></a>Veri tümleştirmesinde kurulum

**msdyn_workorders** için **Tümleştirme anahtarı** bulunduğundan emin olun. 
1. Veri Tümleştirme'ye gidin
2. **Bağlantı Kümesi** sekmesini seçin
3. İş emri eşitlemede kullanılacak Bağlantı kümesini seçin
4. **Tümleştirme anahtarı** sekmesini seçin
5. msdyn_workorders öğesini bulun ve **msdyn_name (Work Order Number)** anahtarının eklendiğini kontrol edin. Görünmüyorsa, **Anahtar ekle**'ye tıklayarak ekleyin sayfanın üst kısmındaki **Kaydet**'e tıklayın

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderheader"></a>İş emirlerinden Satış siparişlerine (Field Service'tan Fin and Ops'a): WorkOrderHeader

Filtre: (msdyn_systemstatus ne 690970005) ve (msdyn_systemstatus ne 690970000) ve (msdynce_hasexternallymaintainedproductsonly eq true)

[![Veri tümleştirmede şablon eşleme](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineestimate"></a>İş emirlerinden Satış siparişlerine (Field Service'tan Fin and Ops'a): WorkOrderServiceLineEstimate

Filtre: (msdynce_headersystemstatus ne 690970005) ve (msdynce_headersystemstatus ne 690970000) ve (msdynce_orderhasexternalmaintainedproductsonly eq true) ve (msdyn_linestatus eq 690970000) ve (msdynce_headersystemstatus ne 690970004)

[![Veri tümleştirmede şablon eşleme](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineused"></a>İş emirlerinden Satış siparişlerine (Field Service'tan Fin and Ops'a): WorkOrderServiceLineUsed

Filtre: (msdynce_headersystemstatus ne 690970005) ve (msdynce_headersystemstatus ne 690970000) ve (msdynce_orderhasexternalmaintainedproductsonly eq true) ve ((msdyn_linestatus eq 690970001) veya (msdynce_headersystemstatus eq 690970004))

[![Veri tümleştirmede şablon eşleme](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineestimate"></a>İş emirlerinden Satış siparişlerine (Field Service'tan Fin and Ops'a): WorkOrderProductLineEstimate

Filtre: (msdynce_headersystemstatus ne 690970005) ve (msdynce_headersystemstatus ne 690970000) ve (msdynce_orderhasexternalmaintainedproductsonly eq true) ve (msdyn_linestatus eq 690970000) ve (msdynce_headersystemstatus ne 690970004) ve (msdyn_allocated eq true)

[![Veri tümleştirmede şablon eşleme](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineused"></a>İş emirlerinden Satış siparişlerine (Field Service'tan Fin and Ops'a): WorkOrderProductLineUsed

Filtre: (msdynce_headersystemstatus ne 690970005) ve (msdynce_headersystemstatus ne 690970000) ve (msdynce_orderhasexternalmaintainedproductsonly eq true) ve ((msdyn_linestatus eq 690970001) veya (msdynce_headersystemstatus eq 690970004) veya (msdyn_allocated ne true))

[![Veri tümleştirmede şablon eşleme](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)