---
title: Video oynatıcı modülü
description: Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025698"
---
# <a name="video-player-module"></a>Video oynatıcı modülü


[!include [banner](includes/banner.md)]

Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Video oynatımını desteklemek için video oynatma modülü kullanılır. Video içeriğinin içerik yönetim sistemi ne (CMS) yüklenmesi ve kullanılabilir olması koşuluyla, herhangi bir sayfaya eklenebilir. Video oynatıcı modülü .mp4 ortam türünü destekler.

## <a name="video-player-module"></a>Video oynatıcı modülü

Video oynatıcı modülü bir e-ticaret sitesinde videoları sergileyebilecek şekilde kullanılabilir. Yürüt, Duraklat, tam boyut modu, ses açıklamaları ve kapalı açıklamalı alt yazılar gibi tüm kayıttan yürütme yeteneklerini destekler. Video oynatıcı modülü, Microsoft erişilebilirlik standartlarını karşılamak için kapalı açıklamalı alt yazıların özelleştirmesini de destekler. Örneğin, yazı tipi boyutunu ve arka plan rengini özelleştirebilirsiniz.

Video oynatıcı modülü ikincil ses parçalarını da destekler. Bir video CMS'ye karşıya yüklendiğinde, ikincil bir ses parçası da karşıya yüklenebilir. Böylece, bir kullanıcı seçerse, video oynatıcı modülü ikincil ses kanalını yürütebilir.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>E-ticaret'da video oynatıcı modülleri örnekleri

- Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki yönerge videoları
- Tüm pazarlama sayfaları üzerindeki ilkelerle ilgili videolar veya promosyon videoları
- Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki ürün özelliklerini vurgulayan pazarlama videoları

### <a name="video-player-module-properties"></a>Video oynatıcı modülü özellikleri

| Özellik adı         | Değer                               | Tanım |
|-----------------------|-------------------------------------|-------------|
| Otomatik Yürütme             | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video otomatik olarak yürütülür. |
| Sesi Kapat                  | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, ses kapatılır. Bu oynatıcı için varsayılan değer **yanlış**'tır. Chrome tarayıcıda, Otomatik yürütme videoları varsayılan olarak kapalı ve ses ancak videoyu el ile oynadığında yürütülür. |
| Döngü                  | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video döngü olarak tekrarlanır. |
| Ortam                 | Video dosya yolu ve adı. | Video oynatıcı tarafından oynanan video dosyası. |
| Tam ekran oynat       | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video tam ekran modunda yürütülür. |
| Oynat/duraklat tetikleyicisi    | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, videoda bir Oynat/Duraklat düğmesi görüntülenir. |
| Video oynatıcı denetimleri | **Doğru** veya **yanlış**               | Değer **Doğru** olarak ayarlandığında, tüm video oynatıcı denetimler gösterilir. Bu denetimler, oynat ve Duraklat düğmelerini, ilerleme göstergesini ve açıklamalı alt yazıları seçeneklerini içerir. |
| Poster görüntüsünü gizle     | **Doğru** veya **yanlış**               | Videoda poster karesi olabilir. Bu özelliğin değeri **doğru** olarak ayarlandığında, poster çerçevesi gizlenir. |
| Maske düzeyi            | **0** ile **100** arasında bir sayı | Stil oluşturma için videoya uygulanan maske. |

## <a name="add-a-video-player-module-to-a-page"></a>Sayfaya video oynatıcı modülü ekleme

> [!NOTE] 
> Video oynatıcı modülü oluşturmadan önce, ortam kitaplığı 'na bir video yüklemeniz gerekir.

Bir yeni sayfaya video oynatma modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Video oynatıcı şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir konteyner modülü ekleyin.
1. Konteyner modülünde, video oynatıcı ve ortam video oynatıcı modülleri ekleyin.
1. Şablon düzenlemeyi tamamlayın ve sonra yayımlayın.
1. **Video oynatıcı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz video oynatıcı şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir video oynatıcı modülü ekleyin.
1. Video oynatıcı modülüyle ilgili Özellik bölmesinde **video Ekle**'yi seçin.
1. **Ortam Seçicisi** iletişim kutusunda bir video seçin ve sonra **yeni ortam öğesiniyükle**'yi seçin.
1. Sayfayı kaydet ve önizleyin. Sayfada video modülünü görmelisiniz. Modülün davranışını özelleştirmek için ek ayarları değiştirebilirsiniz.
1. Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Promosyon başlık modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[Metin bloku modülü](add-content-rich-block.md)

[İçerik blok modülü](add-hero-module.md)