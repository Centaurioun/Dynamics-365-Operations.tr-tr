---
title: Alacak hesapları ile alacak ve tahsilatları yapılandırma
description: Faturaları ve müşterilerden gelen ödemeleri izlemek için Alacak hesaplarını ve Alacak ve Tahsilatları yapılandırın.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc, CollectionLetterCourse, CreditCardProcessors, CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsAgent, CustCollectionsPool, CustGroup, CustParameters, CustPaymMode, CustPosting, CustVendReportInterval, Interest, PaymTerm, Reasons
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24631
ms.assetid: 8c1fc7c5-b461-41ed-b102-2648cc58eb0b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6a64aeb9a98eae7b54de5870118d6c49e5370cc
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000291"
---
# <a name="configure-accounts-receivables-and-credit-and-collections"></a>Alacak hesapları ile alacak ve tahsilatları yapılandırma

[!include [banner](../includes/banner.md)]

Faturaları ve müşterilerden gelen ödemeleri izlemek için Alacak hesaplarını ve Alacak ve Tahsilatları yapılandırın.

Müşteri grupları, müşteriler, nakil profilleri, çeşitli ödeme seçenekleri, faiz notları, tahsilat mektupları, komisyon ücretleri, müşterilerle ilgili parametreler, giderler, teslimatlar ve teslimat yerleri ve diğer Alacak hesapları ve Alacaklar ile Tahsilatların bilgilerini oluşturabilirsiniz.
Aşağıdaki tablo, Alacak hesapları ve kredi ve tahsilatların yapılandırma ve bakımını destekleyen sayfaları listeler. Tablo girişleri önce göreve göre, ardından sayfa adına göre alfabetik olarak sıralanmıştır.

> [!NOTE]
> Veri veya parametre ayarları diğer sayfalara girilmemişse aşağıdaki tabloda bazı sayfalara gidemezsiniz.

| Görev                                                 | Sayfa adı                            | Kullanım                                                                                                                                                                                                                                                                             |
|------------------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gerekli Alacak hesapları bilgilerini konfigüre etme | Alacak hesapları parametreleri       | Alacak hesapları modülü için parametreler ayarlayın.                                                                                                                                                                                                                             |
|                                                      | Alacak hesapları iş akışları         | Bir iş akışı oluşturun veya varolan bir iş akışında değişiklik yapın.                                                                                                                                                                                                                                      |
|                                                      | Müşteri grupları                      | Anahtar parametreleri paylaşan alıcıları oluşturun ve sürdürün. Bunlar, ödeme koşulları, kapatma dönemleri, stok deftere nakil genel muhasebe hesapları, vergi grubu ve varsayılan hesap ayarını içerir.                                                                                  |
|                                                      | Müşteri nakil profili             | Müşteri hareketlerinin genel muhasebeye naklini kontrol eden nakil profillerini ayarlayın.                                                                                                                                                                              |
|                                                      | Form kurulumu                           | Satış siparişleri, malzeme çekme listeleri, sevk irsaliyeleri ve faturalar gibi müşterilerle ilgili çeşitli belgelerdeki bilgilerin biçimini tanımlayın.                                                                                                                            |
|                                                      | Ödeme yöntemleri - müşteri        | Müşterilere yönelik ödeme yöntemleri hakkındaki bilgileri oluşturun ve güncelleştirin.                                                                                                                                                                                                           |
|                                                      | Ödeme koşulları                     | Alacak hesapları veya Borç hesaplarındaki satış siparişlerine, satınalma siparişlerine, müşterilere ve satıcılara atamak istediğiniz ödeme koşullarını tanımlayın.                                                                                                                           |
|                                                      |                                      |                                                                                                                                                                                                                                                                                   |
| Alacak hesapları günlüklerini konfigüre etme             | Günlük adları                        | Günlük şablonlarını oluşturun ve yönetin. Seçili kullanıcılar veya kullanıcı gruplarıyla ilgili deftere nakil sınırlamalarının yönetimi de buna dahildir.                                                                                                                                                 |
|                                                      |                                      |                                                                                                                                                                                                                                                                                   |
| Müşteri faturalarını konfigüre etme                        | Faturalama kodları                        | Dekont/Serbest metin faturası satırlarında kullanmak üzere ödeme masrafları için isteğe bağlı kodları ayarlayın.                                                                                                                                                                                                      |
|                                                      | Masraf kodu                         | Satış siparişleri ve satınalma siparişlerinde kullanılmak üzere fatura masrafları, navlun ve sigorta gibi giderler için kodlar ayarlayın.                                                                                                                                                            |
|                                                      | Altbilgi metni                          | Yazdırma yönetim kaydı için birden çok dilde alt bilgi metni belirtmek. Belge yazdırıldığında, belgenin dili alt bilgi metninin dilini belirler.                                                                                                   |
|                                                      | Form notları                           | Faturalar, satış siparişleri ve vade farkı dekontları gibi organizasyonunuzun kullandığı çeşitli sayfaların üzerinde görünen standart metni düzenleyin.                                                                                                                                         |
|                                                      | Form kurulumu                           | Teklifler, teyitler, malzeme çekme listeleri, sevk irsaliyeleri, müşteri faturalar, serbest metin faturaları ve vade farkı dekontları için sayfa not parametreleri tanımlayın.                                                                                                                               |
|                                                      | Form sıralama parametreleri              | Birden fazla faturayı yazdırırken bir sıralama düzeni kurun; örneğin fatura tutarı ve satış siparişi numarasına göre.                                                                                                                                                                          |
|                                                      | Yazdırma yönetimi kurulumu               | Yazdırma yönetimi orijinal veya kopya kayıtları ile koşullu ayarları oluşturmak. Bu bilgiler satış siparişleri ve satınalma siparişleri gibi belgelerin onaylanma sırasında yazdırılma şeklini kontrol eder.                                                               |
|                                                      |                                      |                                                                                                                                                                                                                                                                                   |
| Müşteri ödemelerini konfigüre etme                        | Nakit iskontoları                       | Müşteri ve satıcı hesabıyla ilişkili olan ve satış siparişleri ile satınalma siparişlerine uygulanabilecek nakit iskontosu kodlarını ayarlayın ve yönetin.                                                                                                                                      |
|                                                      | Kredi kartı işlem merkezleri               | Satış siparişlerinin ödemesi için verilmiş olan kredi kartlarına onay veren kredi kartı işlem merkezlerine ait bilgileri ayarlayın.                                                                                                                                                     |
|                                                      | Para birimleri                           | Kuruluşunuzun kullandığı para birimlerini görüntüleyin ve oluşturun.                                                                                                                                                                                                                       |
|                                                      | Döviz kurları              | Muhasebe para birimi ve diğer para birimleri arasında uygun döviz kurlarını yönetin ve sürdürün.                                                                                                                                                                              |
|                                                      | Şirketlerarası muhasebe              | Geçerli tüzel kişiliğin deftere nakil yapabileceği bir hesaplar listesi oluşturun. Borç ve alacak hesaplarını ve aynı zamanda diğer tüzel kişilikteki hareketleri alan günlüğü ayarlamanız gerekir.                                                                             |
|                                                      | Ödeme yöntemleri - müşteri        | Müşterilere yönelik ödeme yöntemleri hakkındaki bilgileri oluşturun ve güncelleştirin. Daha fazla bilgi için bkz. [Müşteri ödeme yöntemi geliştir](tasks/establish-customer-method-payment.md).                                                                                             |
|                                                      | Kuruluş hiyerarşileri             | Merkezi ödemeler için bir kuruluş hiyerarşisi ayarlayın.                                                                                                                                                                                                                        |
|                                                      | Kuruluş hiyerarşisi amaçları      | Merkezi ödemeler için bir amaç belirtin.                                                                                                                                                                                                                                       |
|                                                      | Ödeme günleri                         | Müşterilerden alacağınız ödemelere veya satıcılara yapacağınız ödemelere ait vade tarihlerini hesaplamak için kullanılan ödeme günlerini tanımlayın.                                                                                                                                                |
|                                                      | Ödeme masrafı                          | Kambiyo senetlerinin masrafları gibi müşterilerle ilgili ödeme masraflarını oluşturun ve saklayın.                                                                                                                                                                         |
|                                                      | Ödeme masrafı kurulumu                    | Banka, ödeme yöntemi, havale tipleri, ödeme şekilleri, para birimleri ve tarih aralıklarının çeşitli birleşimleri için ödeme masraflarını ayarlayın.  Daha fazla bilgi için bkz. [Müşteri ödeme ücretleri geliştir](tasks/establish-customer-payment-fees.md).                                                                                   |
|                                                      | Ödeme planları                    | Müşterilerden alacağınız ve satıcılara yapacağınız taksit ödemelerini planlamak için kullanabileceğiniz ödeme planları oluşturun.                                                                                                                                                                       |
|                                                      | Ödeme şekli                | Ödeme yöntemleri sayfasında seçtiğiniz ödeme yöntemiyle ilgili ödeme şekli kodları oluşturun ve görüntüleyin. Ödeme şekli kodlarını, bankayla yapmış olduğunuz ve seçili ödeme yöntemi için belirtilmiş sözleşmeye göre tanımlarsınız.                    |
|                                                      | Hareket metni                     | Genel muhasebeye otomatik nakiller için hareket metinleri oluşturun. Çeşitli dillerde hareket metinleri ayarlayabilirsiniz.                                                                                                                                                           |
|                                                      | Çeviriler                         | Başka bir dilde metin oluşturun. Harici kullanım için (ödeme koşulları, teslim koşulları ve teslimat modları gibi) tüm metinleri bir veya daha fazla dile çevirebilirsiniz.                                                                                                    |
|                                                      |                                      |                                                                                                                                                                                                                                                                                   |
| Müşteri ödeme biçimlerini konfigüre etme                 | Kambiyo senedi düzeni              | Banka hesapları sayfasında seçtiğiniz banka hesabı için kambiyo senetlerinin düzenini ayarlayın.                                                                                                                                                                          |
|                                                      | Çek düzeni                         | Banka hesapları sayfasında seçtiğiniz banka hesabı için çeklerin düzenini ayarlayın.                                                                                                                                                                                     |
|                                                      | Ödeme yöntemlerine ait dosya biçimleri  | Müşteri ödemelerinde kullanmak için içe aktarma, dışa aktarma, iade ve havale dosya biçimleri seçin.                                                                                                                                                                                          |
|                                                      | Ödeme yöntemleri - müşteri        | Müşterilere yönelik ödeme yöntemleri hakkındaki bilgileri oluşturun ve güncelleştirin.                                                                                                                                                                                                           |
|                                                      | İmza                            | .bmp, .jpg veya .gif dosyaları gibi imza resmi dosyalarını ekleyin, değiştirin veya kaldırın. İmza resim dosyaları resmi tüzel kişilik imzaları olarak çeklere yazdırılır.                                                                                                             |
|                                                      |                                      |                                                                                                                                                                                                                                                                                   |
| Alacak hesapları istatistiklerini konfigüre etme           | Yaşlandırma dönem tanımları             | Müşteri hesaplarının ve satıcı hesaplarının vadesini girdiğiniz bir tarihe göre analiz etmek için kullanılan kullanıcı tarafından tanımlanmış yaşlandırma dönem tanımlarını ayarlayın ve yönetin. Daha fazla bilgi için bkz. [Alacak hesapları yaşlandırma bilgisi ayarla ve oluştur](tasks/set-up-accounts-receivable-aging-information.md).                                                           |
|                                                      | İşletme istatistikleri                  | Organizasyonunuzun performansını analiz etmenize yardımcı olacak ticari istatistik sorgulamaları ayarlayın.                                                                                                                                                                              |
|                                                      | Ticari istatistik verileri             | Bir seçili ticari istatistik için verileri kılavuz biçiminde görüntüleyin.                                                                                                                                                                                                                     |
|                                                      |                                      |                                                                                                                                                                                                                                                                                   |
| Müşteri bilgilerini sürdürme                     | Adres defteri                         | Olasılıklar, müşteri adayları, iş fırsatları, müşteriler, ilgili kişiler, rakipler ve çalışanlarla ilgili bilgileri girin veya görüntüleyin.                                                                                                                                                          |
|                                                      | Müşteri banka hesapları               | Müşteri banka hesapları oluşturun ve yönetin.                                                                                                                                                                                                                                         |
|                                                      | Müşteri grupları                      | Anahtar parametreleri paylaşan alıcıları oluşturun ve sürdürün. Bunlar, ödeme koşulları, kapatma dönemleri, stok deftere nakil genel muhasebe hesapları, vergi grubu ve varsayılan hesap ayarını içerir.                                                                                  |
|                                                      | Müşteriler                            | Şirketin iş yaptığı müşteriler için olan müşteri hesaplarını oluşturun ve yönetin.                                                                                                                                                                                    |
|                                                      | Yazdırma yönetimi kurulumu               | Yazdırma yönetimi orijinal veya kopya kayıtları ile koşullu ayarları oluşturmak. Bu bilgiler satış siparişleri ve satınalma siparişleri gibi belgelerin deftere nakil işlemi sırasında yazdırılma şeklini kontrol eder.                                                                    |
|                                                      |                                      |                                                                                                                                                                                                                                                                                   |
| Alacak ve tahsilatları yapılandırma                   | Alacak hesapları parametreleri       | Alacak ve Tahsilat modülü için parametreleri ayarla.                                                                                                                                                                                                                          |
|                                                      | Vaka kategorileri                      | Tahsilatlar vakaları için kullanılacak bir vaka kategorisi oluşturun.                                                                                                                                                                                                                   |
|                                                      | Tahsilat mektubu                    | Tahsilat mektubu sıralarını oluşturun ve tahsilat mektubu satırlarıyla aralarında bağlantı kurun.                                                                                                                                                                                      |
|                                                      | Tahsilat temsilcisi                    | Tahsilatlar sayfasında kullanılmak üzere tahsilat temsilcileri ayarlayın.                                                                                                                                                                                                                        |
|                                                      | Tahsilatlar ekibi                     | Aracılar olarak kullanılabilir çalışanları temsil eden bir tahsilat ekibi ayarlayın. Eğer takım mevcut değilse, Alacak hesapları parametrelerinde Tahsilat isimli bir takım otomatik olarak ayarlanır.                                                                                 |
|                                                      | Müşteri yaşlandırma anlık görüntüsü              | Müşteriler için yaşlandırma anlıö görüntüleri oluşturun Bir yaşlandırma anlık görüntüsü, bir grup müşterinin belirli bir zamandaki hesaplanan yaşlandırılmış bakiyesini içerir. Bu adım, bir yaşlandırma dönemi tanımının ayarlanmış olmasını gerektirir.                                                                           |
|                                                      | Müşteri kişileri ve e-posta ayarları | Müşteriler için kişileri, e-posta adresleriyle ayarlayın. Bu adresler Tahsilatlar sayfasında görünür ve müşterilere giden e-postaları oluşturmak için kullanılır. Ayrıca her bir müşteri için, Tahsilatlar sayfasında ilk sırada görüntülenecek varsayılan Tahsilat kişisini oluşturun. |
|                                                      | Müşteri havuzları                       | Tahsilatlar veya yaşlandırma işlemleri için görüntülenebilen veya yönetilebilen müşteri hesaplarının bir grubunu tanımlayan müşteri havuzları ayarlayın.                                                                                                                           |
|                                                      | Müşteri nakil profili             | Müşteri hareketlerinin genel muhasebeye naklini kontrol eden profilleri ayarlayın.                                                                                                                                                                                      |
|                                                      | Müşteri neden kodları                | Müşteri neden kodlarını ayarlayın.                                                                                                                                                                                                                                                    |
|                                                      | Müşteri silme neden kodları      | Silme hareketleri için kullanılacak müşteri sebep kodları ayarlayın.                                                                                                                                                                                             |
|                                                      | Form kurulumu                           | Teklifler, teyitler, malzeme çekme listeleri, sevk irsaliyeleri, müşteri faturaları, serbest metin faturaları ve vade farkı dekontları için form not parametreleri tanımlayın.                                                                                                                               |
|                                                      | İlgi Alanı                             | Faiz kodlarını ayarlayın ve yönetin.                                                                                                                                                                                                                                                 |
|                                                      | NSF bilgisi                     | Banka hesabındaki bir ödemenin Tahsilatlar sayfasında bir NSF hareketi olarak işaretlendiğinde, kullanılacak NSF bilgilerini ayarlayın.                                                                                                                                              |
|                                                      | Satış temsilcisi bilgileri              | Satış temsilcileri için e-posta adresi ayarlayın. Bu adresler Tahsilatlar sayfasında görünür ve bu sayfadan bir satış temsilcisine e-posta göndermek için kullanabilirsiniz.                                                                                                                |


Daha fazla bilgi için bkz. [Alacak hesaplarındaki borç ve alacaklar](collections-credit-accounts-receivable.md).


