--- 
title: "Yalın planlama gruplarını tanımlama"
description: "Yalın planlama grupları, ürünleri kanban planlamada gruplamak ve ayırt etmek için tanımlanır."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 75d8b6614fd3b36d87bcb95b0b753b611a101f62
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="define-lean-schedule-groups"></a>Yalın planlama gruplarını tanımlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Yalın planlama grupları, ürünleri kanban planlamada gruplamak ve ayırt etmek için tanımlanır. Gruplandırma, şirket başına genel bir ilişkilendirmeyle veya belirli bir iş hücresine özgü olarak yapılabilir. Kanban planlama liste sayfasında görsel bir gösterge olması amacıyla her grup için atanmış bir renk kodu vardır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="define-lean-scheduling-group"></a>Yalın planlama grubunu tanımlama
1. Ürün bilgileri yönetimi > Yalın imalat > Kanban planlama kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Zamanlama grubu alanında bir değer girin.
    * Zamanlama grubu, genel grup olarak veya belirli bir iş hücresine özgü şekilde tanımlanabilir. Bu basit örnekte, genel bir grup tanımlanmıştır ve iş hücresi boş tutulur. Bu grubun ayarları, belirli zamanlama grupları olmayan tüm iş hücreleri için geçerlidir.  
4. Renk seçiminden bir renk seçin.
    * Renkler, kanban zamanlama listesi sayfasındaki veya kanban işlem panosundaki işleri vurgulamak için kullanılır.  
5. Listede, seçili satırı işaretleyin.
6. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="associate-product"></a>Ürün ilişkilendirme
1. Belirli bir ürünle ilişkilendirme yapma
    * Yalın planlama gruplarıyla, belirli bir ürün (Ürün ilişkisi türü = Ürün) ya da bir ürün tahsisat anahtarının parçası olarak (Ürün ilişkisi türü = grup) ürün ilişkilendirmek için iki yol vardır.    
2. İlişki türü alanında Ürün öğesini seçin.
3. Madde numarası alanına bir değer girin.
4. İş çıkarma yeteneği oranı alanında bir sayı girin.
    * Varsayılan İş çıkarma yeteneği oranı 1'dir ve bunun anlamı ilgili ürünlerin üretim akışlarının işlem faaliyetlerinde belirtilen tam kapasiteyi tüketeceğidir. İş çıkarma yeteneği oranı > 1, daha yüksek kaynak tüketimi, İş çıkarma yeteneği oranı > 1 ise daha düşük bir kaynak tüketimi ifade edilir. Oran, maliyet hesaplamasında ve kanban işi tüketiminin hesaplanmasında kullanılır.  

## <a name="associate-item-allocation-key"></a>Ürün tahsisat anahtarını ilişkilendirme
1. Ürün tahsisat anahtarını ilişkilendirme
    * Ürün ilişki türü Grubu kullanarak bir ürün tahsisat anahtarına bir ilişki ekleyin.   Bu işlem için verilerinizde tanımlanan bir tahmini ürün tahsisatı anahtarı gerektiğini unutmayın.  
2. İlişki türü alanında Grup öğesini seçin.
3. Ürün tahsisat anahtarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.
4. Listede, seçili satırdaki bağlantıya tıklayın.

