---
title: "Projeye kaynak oluşturma"
description: "Bu konu, projeye kaynak oluşturma hakkında bilgi sunar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5c00c63e3c55e818934c36b818c90025002092d4
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="project-resourcing"></a>Projeye kaynak oluşturma

[!include[banner](../includes/banner.md)]


Bu konu, projeye kaynak oluşturma hakkında bilgi sunar.

Proje yöneticileri ve kaynak yöneticilerinin proje planlama aşamasında karşılaştıkları zorluklardan biri, projede çalışacak doğru kaynağı belirlemek ve rezerve etmeleri gereken kaynak tahsisatıdır. Microsoft Dynamics 365 for Operations'da, projelere kaynak sağlama becerileri geçici kaynaklar olarak kullanılan ve belirli bir görev ya da görevin bir bölümü için rezerve edilebilen rolleri tanımlamanıza olanak tanır. Bu tür kaynak oluşturma, proje yöneticileri ve kaynak yöneticilerinin aşağıdaki görevleri yerine getirmesini sağlar:

-   Kaynakları eşleştirmeyi kolaylaştırmak için gerekli olan yetkinliklere sahip bir rol tanımlamak.
-   Rolleri, rezerve edilen kaynakarı temel alan ilk görev planlamasını belirlemek için kullanın.
-   Bir proje için atanan rolleri ve kaynakları temel alarak maliyetleri tahmin etmek ve başlangıç bütçesini belirlemek.
-   Her görev için gerekli olan kaynak rezervasyonları sayısını tahmin etmek için rolleri kullanın.
-   Tüm proje yaşam döngüsü için gereken kaynak sayısını tahmin etmek.
-   İlk kaynak atamalarını kullanarak iş kırılım yapısı (WBS) taslağı hazırlamak.

[![Proje yaşam döngüsü](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Proje planlama aşaması ilerledikçe, planlanan kaynaklar personelli kaynaklarla değiştirilebilir. Proje yöneticisi, geriye dönerek herhangi bir proje aşamasında kaynak rezervasyonlarını güncelleştirebilir.

## <a name="set-up-project-resources"></a>Proje kaynaklarını ayarlama
Bir takvim ayarlamanız ve bunu bir personel veya çalışanla ilişkilendirmeniz gerekir. Takvim, projeyi ve projeye rezerve edilen kaynakların çalışma zamanını planlamak için kullanılır. Takvim ayarlama işlemi sırasında, proje yöneticileri kaynak eşitlemeyi kaynak optimizasyonunun bir parçası olarak gerçekleştirebilirler. Takvim planına bağlı olarak, kaynaklara kısıtlamalar getirilebilir. **Takvimler** sayfasından bir takvim ayarlayabilirsiniz. 

Bir çalışanı proje kaynağı olarak ayarlarken, kaynakları ayarladığınız şirkette çalışan çalışanlar arasından seçim yapabilir veya kuruluşunuzdaki diğer şirketlerden çalışanlar seçebilirsiniz. Bunlar şirketlerarası kaynaklardır. Aşağıdaki yordamlar bir çalışanı şirketinizdeki bir proje kaynağı olarak nasıl ayarlayacağınızı ve nasıl bir şirketlerarası proje kaynağı ayarlayabileceğinizi açıklamaktadır.

### <a name="set-up-a-worker-as-a-project-resource"></a>Bir çalışanı proje kaynağı olarak ayarlama

1.  **Çalışanlar** sayfasındaki **Çalışanlar** listesinde proje kaynağı olarak eklediğiniz çalışanı seçin ve çalışan kaydını açın.
2.  Eylem Bölmesinde **Proje** &gt; **Ayar** &gt; **Proje ayarı**'na tıklayın.
3.  Bir takvim seçin ve sayfayı kapatın.

Bir kaynak için ön atama türü olarak varsayılan projeleri de belirtebilirsiniz. Ön atamalar, kaynak yöneticisi veya proje yöneticisi, kaynağın hangi projede çalışacağını önceden bildiğinde kullanılır. Ön atamalar için bir proje sponsoru veya müşterinin talebi de temel alınabilir. Bir projeyi önceden atamak için **Projeleri ata** sayfasındaki **Projeler** sekmesinde bulunan **Kalan projeler** listesinden ilgili projeyi seçin.

### <a name="set-up-an-intercompany-resource"></a>Şirketlerarası bir kaynak ayarlama

Bir çalışanı şirketlerarası kaynak olarak ayarladığınızda, ayarı ödünç veren ve ödünç alan şirkette tamamlamanız gerekir. 

**Ödünç veren şirkette:**

1.  Dynamics 365 for Operations'da, ödünç veren şirketin seçildiğini doğrulayın ve ardından yukarıdaki "Bir çalışanı proje kaynağı olarak ayarlama" yordamını tamamlayın.
2.  **Genel muhasebe **&gt; **Deftere nakil kurulumu **&gt;**Şirketlerarası muhasebe**'ye gidin. **Yeni**'ye tıklayın.
3.  **Tüzel kişilik kimliği **alanında, ödünç veren şirketi seçin. Kalan alanları uygun şekilde doldurun ve **Kaydet**'e tıklayın.
4.  **Proje yönetimi ve muhasebe**&gt; **Ayar **&gt; **Fiyatlar ** &gt; **Transfer fiyatı**** ** öğesine gidin.
5.  **Transfer fiyatı **formunda, **Yeni**'ye tıklayın ve **Ödünç alan tüzel kişilik **alanında, ilgili şirketi seçin.
6.  Ödünç alan şirkete yalnızca bölümün başında oluşturulan kaynağı ödünç vermek istiyorsanız, **Kaynak** alanında, oluşturduğunuz kaynak adını seçin. Şirketteki tüm kaynakları ödünç alan şirketin kullanımına sunmak istiyorsanız, **Kaynak ** alanını boş bırakın.
7.  **Proje yönetimi ve muhasebe **&gt; **Kurulum **&gt; **Proje yönetimi ve muhasebe parametreleri**'ne gidin ve **Şirketlerarası **sekmesinde, **Şirketlerarası kaynak planlamayı ve zaman çizelgelerini etkinleştir **alanını **Evet** olarak ayarlayın.

**Ödünç alan şirkette:**

1.  **Proje yönetimi ve muhasebe** &gt; **Proje kaynakları** &gt; **Kaynaklar listesi**'ne gidin.
2.  Arama filtresi alanına, ödünç alan şirketin kaynak listesine adın eklendiğini doğrulamak için önceki yordamda ödünç veren şirket için oluşturduğunuz kaynağın adını girin.

## <a name="manage-resource-competencies"></a>Kaynak yetkinliklerini yönetme
Kaynak uzmanlıkları, kaynak yönetiminin önemli bir parçasıdır. Yetkinlikler, doğru yetenek, sertifika ve proje deneyimi açısından uygun dengeye sahip kaynakların belirlenmesinde temel olarak kullanılabilir. Bu bilgiyi her kaynak için ayarlamanız ve düzenli olarak güncellemeniz gerekir. Bu şekilde, proje kaynak ataması sırasında belirli kaynak yetkinlikleri eşleştiğinde becerileri en üst seviyeye çıkarabilirsiniz. [![Beceri, sertifika, eğitim ve proje deneyimi örnekleri](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Aşağıdaki yordamlar bir kaynak için bazı yetkinliklerin nasıl ayarlanacağını açıklar. 

Bir çalışan için yetkinlikleri ayarlamak üzere, İnsan kaynaklarındaki **Çalışanlar** liste sayfasını veya Proje yönetimi ve muhasebedeki **Kaynaklar** listesi sayfasını kullanabilirsiniz. Aşağıdaki yordamlar için İnsan kaynaklarındaki **Çalışanlar** listesi sayfasını kullanılır.

### <a name="set-up-competencies-certificates"></a>Yetkinlikleri ayarlama: Sertifikalar

1.  **Çalışanlar** listesi sayfasında, sertifika bilgisi ekleyeceğiniz çalışanın satırını seçin.
2.  Eylem Bölmesinde, **Çalışanlar** sekmesindeki **Yetkinlikler** gurubunda **Sertifikalar**'a tıklayın.
3.  **Yeni**'ye tıklayın.
4.  **Sertifika türü** alanında **PMP**'yi seçin.
5.  **Başlangıç tarihi** alanında, **1/10/2015** tarihini seçin.
6.  **Kaydet**'e tıklayıp sayfayı kapatın.

### <a name="set-up-competencies-skills"></a>Yetenekleri ayarlama: Beceriler

1.  **Çalışanlar** listesi sayfasında, önceki yordamda kullanmış olduğunuz çalışanın hala seçili olduğundan emin olun. Ardından Eylem Bölmesinde, **Çalışanlar** sekmesindeki **Yetkinlikler** gurubunda **Beceriler**'e tıklayın.
2.  **Yeni**'ye tıklayın.
3.  **Beceri** alanında **Proje yönetimi**'ni seçin.
4.  **Düzey** alanında **5 Uzman**'ı seçin.
5.  **Düzey tarihi** alanında **14/1/2014** tarihini seçin.
6.  **Deneyim yıl sayısı** alanına **10** girin.
7.  **Kaydet**'e tıklayıp sayfayı kapatın.

## <a name="create-a-new-project"></a>Yeni proje oluştur
1.  **Proje yönetimi ve muhasebe** &gt; **Çalışma alanları** &gt; **Proje yönetimi**'ne tıklayın.
2.  **Yeni proje**'ye tıklayın ve şu değerleri girin:
    -   **Proje türü** - Zaman ve malzeme
    -   **Proje adı:** - XYZ Yükseltme Aşaması 2
    -   **Project grubu:** TM\_WIP
    -   **Proje sözleşme kodu:** - 00000002
3.  **Proje oluştur**'a tıklayın.

### <a name="assign-a-resource-to-a-project"></a>Projeye kaynak atama

1.  **İnsan kaynakları** &gt; **Çalışanlar** &gt; **Çalışanlar**'a tıklayın.
2.  **Çalışanlar** listesinde, daha önce yetkinlikleri ayarladığınız çalışanın kaydını seçin ve çalışan kaydını açın.
3.  Eylem Bölmesinde, **Proje** sekmesindeki **Ayar** gurubunda **Projeleri ata**'ya tıklayın.
4.  **Kaynak doğrulama proje atamaları** sayfasında, **Projeler** sekmesine tıklayın.
5.  **Projeyi seçilen projelere ekle**'de,  XYZ Yükseltme Aşaması 2 projesini filtreleyin.
6.  **Kalan projeler** bölmesinde, bir proje seçin ve ardından **Seçilen projeler** bölmesine eklemek için oka tıklayın.
7.  Sayfayı kapatın.

Gerekirse, kaynak için kategoriler de atayabilirsiniz. Kategori türü Maliyet veya Gelir'dir. Bu kuruluş tarafından belirlenir. Kaynak için atanan kategori yoksa, Dynamics 365 for Operations maliyet ve gelir için saat fiyatlarında varsayılan kategoriyi arayacaktır.

### <a name="set-up-project-resource-and-role-characteristics"></a>Proje kaynağını ve rol özelliklerini ayarlama

Proje yöneticisi, bir proje için gerekli olan rolleri oluşturmak için proje kaynak oluşturma işlevini kullanabilir. Roller, teyit edilen kaynaklar kaynaklar rezerve edilirken hala bilinmediğinde kullanılabilir. Roller geçici olarak planlanan kaynak olarak kullanılabilir; bu durumda proje planlama aşamalarına devam edebilirsiniz. 

[![Rol örneği](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Senaryo:** Contoso, onaylanmış bir proje tüzüğü olan bir Zaman ve malzeme projesini tamamlamak üzere işe alınmıştır. Yardımcı proje müdürü, projenin amacını doldurmaya devam etmektedir. Kaynak yöneticisi, yeni projede çalışmak üzere rezerve edilecek belirli kaynakları belirlemektedir. Proje sponsorunun istediği rollerden biri, projenin kritik yapısı nedeniyle, Kıdemli proje yöneticisi konumudur. Kaynak yöneticisinin yeni bir kaynak alması ve yardımcı proje yöneticisi için proje planlama sırasında kaynak bilgisi gerekli olduğundan, rolü sistemde tanımlamalıdır. 

Aşağıdaki adımlarda, kaynak yöneticisinin Kıdemli proje yöneticisi rolünü nasıl ayarlayabileceği ve kaynak özelliklerini bununla nasıl ilişkilendirebileceği gösterilmektedir. Daha sonra, rol istenen kaynak yetkinlikleriyle eşleşen kullanılabilir kaynakları aramak için kullanılabilir.

1.  **Proje yönetimi ve muhasebe** &gt; **Ayar** &gt; **Kaynaklar** &gt; **Rolleri ayarla**'ya tıklayın.
2.  **Yeni**'ye tıklayın ve şu değerleri girin:
    -   **Rol Kimliği:** - Kıdemli Proje Yöneticisi
    -   **Açıklama:** - Kıdemli Proje Yöneticisi
3.  **Oluştur**'a tıklayın.
4.  **Kıdemli Proje Yöneticisi** rolünü seçip **Özellikleri yapılandır**'a tıklayın.
5.  **Özelliklerin türü** alanında, **Beceri**'yi seçin.
6.  **Kullanılabilir özellikler** alanına, aradığınız beceriyi girin.
7.  **Özellik türü** alanında **Sertifika**'yı seçin.
8.  **Kullanılabilir özellikler** alanına, aradığınız sertifika türünü girin.
9.  **Tamam**'a tıklayıp sayfayı kapatın.

### <a name="assign-a-project-resource-to-a-project"></a>Projeye proje kaynağı atama

1.  **Proje yönetimi ve muhasebe** &gt; **Ortak** &gt; **Projeler** &gt; **Tüm projeler**'i seçin ve **XYZ Yükseltme Aşaması 2** projesini açın.
2.  **Proje ekibi ve planlama** sekmesinde **Ekle**'ye tıklayın.
3.  **Rol** alanında **Ekip üyesi**'ni seçin.
4.  **Takvimden rezerve et**'e tıklayın.
5.  **Kaynak kullanılabilirliği** sayfasında, **Görünüm ayarları**'na tıklayın.
6.  **Görünüm ayarlarını ayarla** sayfasına şu değerleri girin:
    -   **Tarih aralığı görünüm biçimi:** - Gün
    -   **Uygunluk açıklamalarını görüntüle:** - Evet
    -   **Kalan kapasiteyi görüntüle:** - Evet
7.  Kaynak listesinde, bir kaynak seçin.
8.  **Kesin rezervasyon** &gt; **Tam kapasite**'ye tıklayın.
9.  Sayfayı kapatın.

### <a name="assign-a-resource-to-a-default-role"></a>Varsayılan bir role kaynak atama

Proje veya kaynak yöneticilerine yardımcı olmak için, bir proje için rezerve edilebilecek kaynaklarla ilgili daha ayrıntılı inceleme yapabilirsiniz. Varsayılan bir rolü mevcut bir kaynakla veya yeni edinilen bir kaynakla ilişkilendirebilirsiniz. örneğin, Daniel işe alındığında, İş analisti rolünü yerine getirmek için beceri ve deneyimi vardı. Kaynak yöneticisi, bu rolü Daniel'ın varsayılan rolü olarak atadı. Bu nedenle, kaynak yöneticisi Daniel'ı projelerde çalışmak üzere kullanılabilir olan iş analistleri havuzuna eklendi. 

Kaynak rezervasyonu sırasında, proje yöneticileri projede çalışabilecek rol kaynaklarını filtreleyebilir. Bu bilgiyi, kaynak karşılama sırasında çok ölçütlü karar analizi gerçekleştirirken bir ölçüt olarak kullanabilirler. Ayrıca, söz konusu proje için belirli becerileri, eğitimi ve deneyimi olan kaynakları aramak için filtre uygulamak amacıyla diğer kaynak özelliklerini ekleyebilirler. 

**Senaryo:** Onaylanmış bir proje başlamıştır ve Kıdemli proje yöneticisi rolü proje planlama aşamasında planlanan kaynak olarak rezerve edilmiştir. Kaynak yöneticisi, Kıdemli proje yöneticisi rolünü yerine getirecek bir kaynak edinmiştir.

1.  **Proje yönetimi ve muhasebe** &gt; **Proje kaynakları** &gt; **Kaynaklar listesi**'ne tıklayın.
2.  **Kaynak** listesinden, **Daniel Goldschmidt**'i seçin.
3.  **Proje kaynağı** &gt; **Koru** &gt; **Kaynak rolü**'ne tıklayın.
4.  **Yeni**'ye tıklayın ve şu değerleri girin:
    -   **Yürürlüğe giriş:** - (Güncel tarih)
    -   **Süre sonu:** - Hiçbir zaman
    -   **Rol:** - Kıdemli Proje Yöneticisi
5.  **Kaydet**'e tıklayıp sayfayı kapatın.
6.  **Yetkinlikler** sekmesinde, **ProjectMgmt** becerisini ve **PMP** sertifikasını ekleyin.

## <a name="set-up-role-based-pricing"></a>Rol tabanlı fiyatlandırmayı ayarlama
Tüm satış, maliyet ve transfer fiyatları roller için ayarlanabilir.

1.  **Proje yönetimi ve muhasebe** &gt; **Ayar** &gt; **Fiyatlar** &gt; **Satış fiyatı (saat)**'na tıklayın.
2.  **Yeni**'ye tıklayın.
3.  Bir yürürlük tarihi girin.
4.  **Rol** sütunundan bir rol seçin.
5.  **Fiyatlandırma** sütununa, seçilen kaynak rolü için bir fiyat girin.

## <a name="form-a-project-team"></a>Proje ekibi oluşturma
Bir projedeki önceden ayarlanmış olan rolleri kullanmak için bir proje yöneticisinin rolleri projeyle ilişkilendirmesi gerekir. Bir proje için birden çok rol atanabilir ve Dynamics 365 for Operations, karışıklığı önlemek için rezervasyon sırasında bu rolleri otomatik olarak etiketler. Örneğin, proje yöneticisi üç yazılım mühendisi istiyorsa, yazılım mühendisi 1, yazılım mühendisi 2 ve yazılım mühendisi 3 etiketlerine sahip üç Yazılım mühendisi rolü otomatik olarak oluşturulur. Rol için rol özellikleri önceden ayarlanmışsa, kaynak arama sırasında filtre olarak uygulanır. Aramayı daha detaylı hale getirmek için ek özellikler eklenebilir. 

Kaynak kullanılabilirliğinin daha iyi görüntülenebilmesi için görüntüleme ayarları özelleştirilebilir. Saatlik, günlük, haftalık, aylık, üç aylık ve yıllık kullanılabilirliği gösterme seçenekleri vardır. Ayrıca, kullanılabilir ve kalan kaynak kapasitesini görüntüleme seçeneği de bulunur. Bu seçenek, faaliyetler veya kaynak kullanılabilirliği için kullanılabilir zamanı tahmin etmeniz gerektiğinde yararlıdır. 

Proje yöneticisi sayfadan bir rol seçebilir ve gereksinimi karşılayan kullanılabilir bir kaynak varsa, rolü doldurmak için bir kaynak rezerve etmeyi seçebilir. Kaynakların, planlama aşamasının bu noktasında rezerve edilmemesi gerektiğini unutmayın. Bir WBS oluşturduğunuzda, rolleri projedeki personelli kaynaklarla değiştirebilirsiniz. Roller, WBS'deki personelli kaynaklarla değiştirilirse, kaynak ayarı proje ekibi listesini ve planlamasını otomatik olarak güncelleştirir. 

[![Hem rolleri hem de gerçek kaynakları içeren proje ekibi listesi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Proje yöneticisinin bir proje için bir kaynağı rezerve etmek için kullanabileceği **Kalan kapasite**, **Tam kapasite**, **Kapasite yüzdesi** ve **Saatleri belirtme** gibi çeşitli seçenekleri vardır. Kaynak atamalarını değiştirirseniz, bu rezerve etme seçenekleri herhangi bir zamanda iptal edilebilir. İki tür rezervasyon desteklenir:

-   **Kesin Rezervasyon** – Kaynak rezervasyonu onaylanmış ve belirtilen süre için görevde çalışmak üzere doğrulanmıştır.
-   **Geçici Rezervasyon** – Kaynak rezervasyonları geçici olarak belirtilen süre için görevde çalışmak üzere ayarlanmıştır.

Aşağıdaki yordamda bir proje ekibinin nasıl oluşturulacağı açıklanmaktadır.

### <a name="create-a-project-team"></a>Proje ekibi oluşturma

1.  **Tüm projeler** liste sayfasında bir proje seçin ve ardından **Düzenle**'ye tıklayın.
2.  **Proje ekibi ve planlama** sekmesindeki **Bitiş tarihini planla** alanına, planlanan başlama tarihi artı bir ay girin. Örneğin, planlama başlangıç tarihi 24 Haziran 2017 ise (24/06/2017), **24/07/2017** girin.
3.  **Ekle**'ye tıklayın.
4.  **Projeye roller ekle** bölmesindeki **Rol**alanında **Kıdemli Proje Yöneticisi**'ni seçin.
5.  **Gerekli yetkinlikler**'e tıklayın.
6.  **Özelliklerini seçin** sayfasında, Kıdemli proje yöneticisi rolü için önceden ayarlamış olduğunuz özellikler varsayılan olarak seçilir. **Tamam** düğmesine tıklayın.
7.  **Projeye roller ekle** sayfasındaki **Kaynak sayısı** alanına **1** girin.
8.  **Kaynak** alanında, arama gerekli yetkinliklere sahip tüm kaynakları gösterir. **Daniel Goldschmidt**'i seçin ve **Oluştur**'a tıklayın.
9.  **Proje** sayfasında **Ekle**'ye tıklayın.
10. **Projeye roller ekle** bölmesindeki **Rol**alanında **Ekip üyesi**'ni seçin. **Kaynak sayısı** alanına **5** girin.
11. **Oluştur**'a tıklayın.
12. **Projeler** sayfasında **Kaynağı karşıla**'ya tıklayın.

## <a name="resource-capacity-synchronization"></a>Kaynak kapasitesi eşitleme
Kaynak eşitleme işlemleri, takvim ve temel takvim bilgilerini, proje kaynak planlamasına doğru çekilmesinin sağlanmasına yardımcı olur. Takvim değiştirilse, işlemler proje kaynak planlama için gerekli güncelleştirmeleri yapar. İşlemler, takvim kaynak bilgileri önceden eşitlendiği için performansın artmasına da yardımcı olur. Bu durumda, kaynak planlama bilgilerindeki güncelleştirmeler daha hızlı gerçekleşir. İşlemleri tek tek planlamak yerine toplu iş olarak planlamanızı öneririz. Aksi halde, birisinin bilgiler son eşitlendiğinde dahil edilen tarihleri unutma riski vardır. Dahil olan tarihler kullanılmazsa, tarih eşitleme sırasında boşluklar oluşabilir.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Takvim eşitleme](./media/projectresourcing04-1024x471.jpg)

**Kaynak kapasite toplamlarını eşitle**

Eşitleme işlemi, tüm kaynak takvim bilgilerini eşitlemek üzere tasarlanmıştır. Bu bilgiler, projenin Kaynak takvimi kapasite tablosundaki değişikliklerle ilgili temel takvim bilgilerini içerir. Projeye yeni kaynaklar eklenirse, eşitleme güncellenen takvim bilgilerinin kullanılmasının sağlanmasına yardımcı olur. Eşitleme herhangi bir zamanda yapılabilir. 

Toplu iş kullanmanızı öneririz. Eşitleme kapasite rezervasyonunda seçenekler bulunmaktadır.

-   **Proje yönetimi ve muhasebe** &gt; **Periyodik** &gt; **Kapasite eşitleme** &gt; **Kaynakların kapasite toplamlarını eşitle**'ye tıklayın.

| Seçenek | Açıklama                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evet    | Tüm kaynak verilerini takvimle ve temel takvim bilgileriyle eşitleyin ve proje kaynak kapasitesi takvimindeki tüm bilgileri değiştirin.                                                  |
| Hayır     | Tarih aralığı kodu ve belirtilen başlangıç ve bitiş tarihlerini temel alarak kaynak verilerini eşitleyin. Bu seçenek, mevcut verileri kaldırmaz ve yalnızca yeni eklenen kaynaklarla ilgili bilgileri güncelleştirir. |

[![Eşitleme işlemi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>WBS şablonlarında rolleri ayarlama
Proje yöneticileri, yeni projeler için WBS oluştururken uygulayabilecekleri WBS şablonlarını ayarlayabilirler. Proje yöneticileri bir şablon oluştururken roller ekleyebilirler. WBS şablonuna rol atamak için aşağıdaki yordamı kullanın.** **

1.  **Proje yönetimi ve muhasebe** &gt; **Ayar** &gt; **Projeler** &gt; **İş kırılım yapısı şablonları**'na tıklayın.
2.  Seçilen İKY şablonu için **Ayrıntıları** tıklayın.
3.  Listeden bir görev seçin ve **Rol** alanında, göreve atamak için bir rol seçin.

### <a name="work-with-a-wbs"></a>İKY ile çalışma

Yeni bir İKY oluşturabilir veya mevcut bir İKY şablonundan İKY kopyalayabilirsiniz. Proje Yöneticisi, İKY'deki yeni görevlere roller atayarak kaynakları kolayca yönetebilir. Roller, bir kaynak edinildikten veya görevde çalışmak üzere onaylı bir kaynak tanımlandıktan sonra değiştirilebilir. Bu esneklik, proje yöneticilerinin aşağıdaki görevleri gerçekleştirmesine olanak sağlar:

-   İKY iş paketleri için gereken kaynak sayısını belirlemek.
-   Proje maliyetlerini tahmin etmek.
-   Ön bütçe belirlemek.
-   Roller ve kaynakları temel alarak faaliyet süresini tahmin etmek.
-   Kullanılabilir proje bilgilerine dayanarak bazı proje yönetim planları geliştirmek.

Kaynak oluşturma işlevinin daha etkin kullanılması için İKY'ye ek seçenekler eklenmiştir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaynak atamaları</td>
<td>İKY'deki görevler için atanan kaynakları, tarihleri, saat sayısını ve rezervasyon türünü görüntüleyin.</td>
</tr>
<tr class="even">
<td>Takımı otomatik olarak oluştur</td>
<td>Görevle ilişkili rolleri kullanarak planlanmış kaynakları otomatik olarak ekleyin. Dynamics 365 for Operations, rollere göre çok ölçütlü karar analizini kullanarak planlanmış kaynakları otomatik olarak önerir. İKY'deki görevler için roller ve çalışma (saat) ayarlandıktan ve yapı serbest bırakıldıktan sonra, <strong>Ekibi otomatik oluştur</strong>'a tıklayın. Gereken sayıda planlanmış kaynak İKY'ye ve <strong>Proje ve ekip planlama</strong> sekmesine eklenir.</td>
</tr>
<tr class="odd">
<td>Kaynak (açılan liste)</td>
<td><strong>Kaynak atamayı başlat </strong>sayfasında, belirtilen süreye göre kesin rezervasyon veya geçici rezervasyon yapmak için kaynakları seçebilirsiniz. Kaynak faaliyetlerini görmek ve süresini ayarlamak için görüntüleme ayarlarını düzenleyebilirsiniz. Aşağıdaki seçenekleri kullanarak, kaynakları seçebilir ve iş paketi düzeyinde atayabilirsiniz:
<ul>
<li><strong>Kabul et</strong> – Bir göreve atanan kaynakla ilgili değişiklikleri onaylar.</li>
<li><strong>İptal et</strong> – Bir göreve atanan kaynakla ilgili değişiklikleri iptal eder.</li>
<li><strong>Otomatik olarak ata</strong> – Bu seçenek, seçili görevle eşleşen bir role sahip kullanılabilir personelli bir kaynak seçer.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  **Proje yönetimi ve muhasebe** &gt; **Projeler** &gt; **Tüm projeler**'e tıklayın.
2.  Listeden **XYZ Yükseltme Aşaması 2** projesini seçin.
3.  **Plan** &gt; **Faaliyetler** &gt; **İş kırılım yapısı**'na tıklayın.
4.  İKY'ye aşağıdaki düzey bir faaliyetlerini eklemek için **Yeni**'ye tıklayın:
    -   Başlatma
    -   Planlama
    -   Yürütme
    -   İzleme ve Denetim
    -   Kapalı

5.  Tarihleri ve çalışmayı (saat) aşağıdaki ekran görüntüsünde gösterildiği şekilde ayarlayın. [![Tarihleri ve çalışmayı ayarlama](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  **Başlatma** görev satırını seçin, ardından **Rol** alanında **Kıdemli Proje Yöneticisi**'ni seçin.
7.  **Yayımla**'ya tıklayın.
8.  Aynı satırda, **Kaynak** alanında **Daniel Goldschmidt**'i seçin.
9.  **Kabul et**'e tıklayın
10. **Planlama** görev satırını seçin ve ardından **Rol** alanında **İş analisti**'ni seçin.
11. **Yayımla**'ya ve ardından **Ekibi otomatik oluştur**'a tıklayın.
12. Görüntülenen iletişim kutusunda **Evet**'e tıklayın.
13. **Kaynak** alanında, değerin **İş analisti 1** olduğunu doğrulayın.
14. **İş analisti 1** kaynağı için aramayı açın ve **Kaynak atama formunu aç**'a tıklayın.
15. Görev için bir çalışan seçin.
16. **Geçici atama** &gt; **Tam kapasite**'ye tıklayın.
17. **Kaydet**'e tıklayıp sayfayı kapatın. 

> [!NOTE] 
> Kaynakların sayısı 1'de kaldığı için belirtilen kaynağın artık 2 olduğunu belirten bir uyarı almazsınız.
18. **İş kırılım yapısı**sayfasında, İKY'deki kaynak atamasını doğrulayın ve **Kaydet**'e tıklayın.

## <a name="resource-fulfillment-for-planned-resources"></a>Planlanmış kaynaklar için kaynak karşılama
Proje yöneticisi, bir proje için gerekli kaynak rollerini planlayabilir. Kaynak yöneticisi **Kaynak karşılama** sayfasında planlanan bu kaynakları istek olarak görür ve gerçek kaynakları atayabilir.

1.  **Proje yönetimi ve muhasebe** &gt; **Projeler** &gt; **Tüm projeler**'e tıklayın.
2.  Listeden **XYZ Yükseltme Aşaması 2** projesini seçin.
3.  **Proje**'ye tıklayın.
4.  **Düzenle**'yi tıklatın.
5.  **Proje ekibi ve planlama** sekmesinde ** ** **Ekle**'ye tıklayın.
6.  **Rolleri ekle** iletişim kutusunda **Yazılım geliştiricisi** rolünü seçin.
7.  **Oluştur**'a tıklayın.
8.  Proje sayfasını kapatın.
9.  **Proje yönetimi ve muhasebe** &gt; **Proje kaynakları** &gt; **Kaynak karşılama**'ya tıklayın.
10. **XYZ Yükseltme projesi Aşama 2** projesi için **Yazılım geliştirici 1**'i seçin.
11. Bir çalışan seçip **Ata** öğesine tıklayın.
12. **XYZ Yükseltme projesi Aşama 2** projesi için **Yazılım geliştirici 1** satırının kaldırıldığından emin olun.
13. **Proje ekibi ve planlama** sekmesinde, **XYZ Yükseltme Aşama2** projesi için, adım 11'de seçtiniz çalışanın **Yazılım geliştiricisi** olarak eklendiğini kontrol edin.

## <a name="requests-for-project-resources"></a>Proje kaynakları talepleri
Proje kaynak planlama işlevselliği yalnızca kaynak yöneticilerinin personellei kaynakları görevlere veya projelere dağıtmasını destekler. Bu işlevi etkinleştirmek için aşağıdaki görevleri tamamlayın veya bu görevlerin tamamlandığını doğrulayın.

-   Numara serileri ayarlayın.
-   Proje yönetimi ve muhasebe iş akışları ayarlayın.
-   Kaynak isteği iş akışını etkinleştirin.

Yukarıdaki görevleri tamamladıktan veya doğruladıktan sonra gerektiğinde aşağıdaki görevleri tamamlayabilirsiniz.

-   Geçici rezervasyon personelli kaynağından bir kaynak isteği oluşturun.
-   Kaynak isteklerini izleyin.
-   Kaynak isteklerini karşılayın.
-   WBS'den personelli bir kaynak isteyin.
-   Personelli kaynak isteği olmayan bir projeye kaynaklar rezerve edin.

## <a name="monitor-project-teams"></a>Proje ekiplerini izleme
1.  **Proje yönetimi ve muhasebe** &gt; **Projeler** &gt; **Tüm projeler**'e tıklayın.
2.  Projeler listesinde **XYZ Yükseltme Aşama 2** projesi için **Proje kimliği** bağlantısına tıklayın.
3.  **Proje ekibi ve planlama** hızlı sekmesinde, listelenen proje kaynaklarının doğru olduğunu kontrol edin.




