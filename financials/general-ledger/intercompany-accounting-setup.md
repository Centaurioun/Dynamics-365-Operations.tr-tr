---
title: "Şirketlerarası muhasebeyi ayarlama"
description: "Bu konu, defter tahsisatları ve mali günlükleri, örneğin günlük günlükler, satıcı faturası günlükleri ve ödeme günlükleri gibi şirketlerarası günlükleri kullanabilmeniz için şirketlerarası muhasebeyi ayarlamayı açıklar."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 506c7958a90bd5a891ea9859c679fcadb64a64d4
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="intercompany-accounting-setup"></a>Şirketlerarası muhasebeyi ayarlama

[!include[banner](../includes/banner.md)]


Bu konu, defter tahsisatları ve mali günlükleri, örneğin günlük günlükler, satıcı faturası günlükleri ve ödeme günlükleri gibi şirketlerarası günlükleri kullanabilmeniz için şirketlerarası muhasebeyi ayarlamayı açıklar.

Şirketler arası günlükler günlük günlükler, satıcı faturası günlükleri, genel muhasebe tahsisatları ve merkezi ödemeler vb. gibi çeşitli senaryolarda oluşturulabilir. Bu senaryoları etkinleştirmek için şirketler arası muhasebeyi kurmanız gerekir.

## <a name="define-main-accounts"></a>Ana hesapları tanımla
İlk olarak, Vade sonu ve Vade başlangıcı hesap girişleri için kullanılmak üzere şirketler arası ana hesaplar oluşturmanız gerekir. Şirketler arası muhasebe girişlerinin mutabakatını ve eliminasyonunu basitleştirmek amacıyla her bir şirket için özgün ana hesapların kullanılması iyi bir fikirdir. Şirketler arası tarafı tanımlamak üzere bir ticari ortak veya karşı boyut kullanıyorsanız bu boyutu şirketler arası muhasebede tanımlanan ana hesap üzerinde bir sabit boyut olarak tanımlayabilirsiniz. Ana hesapları ayarladığınızda, **Ana hesaplar** sayfasındaki **Ana hesap türü** alanını **Bilanço olarak** ayarlamanız gerekir.

## <a name="define-journal-names"></a>Varsayılan günlük tanımla
Ardından, bir günlük adı tanımlamalısınız. **Günlük adları** sayfası üzerindeki **Günlük türü** alanını **Günlük** olarak ayarlayın. Şirketler arası muhasebe için özel bir günlük adı kullanmak iyi bir fikirdir.

## <a name="define-intercompany-accounting-setup"></a>Şirketlerarası muhasebeyi kurulumunu tanımlama
**Şirketlerarası muhasebe** sayfası, birbiriyle işlemler gerçekleştirebilen tüzel varlık çiftleri oluşturmak için kullanılır. Şirketlerarası muhasebe kurulumu paylaşımlıdır, yani kurulum tüm tüzel varlıklar içerisinden görünür. Yeni bir tüzel varlık çifti oluştururken, hangi şirketin kaynak şirket, hangisinin ise hedef şirket olduğunun farkında olduğunuzdan emin olun. Şirketlerarası hareketler girerken, hareket, hangi tüzel varlığın hareketi başlattığını veya kaynağı olduğunu belirler. Örneğin, USMF (kaynak) ve USSI (hedef) için şirketlerarası muhasebe ayarlanır. Bir kullanıcı USSI içerisinde etkinse ve bir şirketlerarası hareketi USMF ile girerse, hareket şirketlerarası muhasebe yalnızca USMF'nin kaynak olarak tanımlandığı için hareket deftere aktarılmaz. Her iki şirketten biri hareketi başlatabiliyorsa, karşılıklı kurulum için ikinci bir varlık çifti oluşturmanız gerekir. 

Hem kaynak hem de hedef tüzel varlığı için **Borç hesabı (başlangıç)** ve **Borç hesabı (Bitiş)** seçin. Hangi **Günlük adı**'nın hareket hedef şirkette oluşturulduğunda kullanılacağını seçin. Kaynak şirketin günlüğü zaten bilinmektedir çünkü kullanıcı tarafından şirketlerarası hareketi oluştururken seçilmiştir. 

Son olarak, destekleyen tutarlar için hangi varlığın muhasebeyi alacağını seçin, örneğin nakit iskontosu veya merkezi ödemeler için gerçekleşmiş kazançlar/zararlar. 

Karşılıklı bir ilişki, **Şirketlerarası muhasebe** sayfasında, **Karşılıklı ilişki oluştur** düğmesine ilk tüzel kişilik oluşturulduktan sonra basılarak kolayca ayarlanabilir. Karşılıklı çift oluşturulduğunda, hedef şirketin bilgisi, kaynak şirkete ve tam tersi de diğerine kopyalanır. Hedef şirket için tanımlanan günlük kalacaktır. Çoğu kuruluş, günlük adlarında aynı adlandırma kuralını kullanır, böylece günlük adı aynıdır. Günlük adı farklıysa, günlüğün mevcut olmadığını ve başka bir günlüğün seçilebileceğini belirten bir uyarı, alanda gösterilir.



