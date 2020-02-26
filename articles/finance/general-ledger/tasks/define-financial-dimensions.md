---
title: Mali boyutları tanımlama
description: Bu görev kılavuzu, varlığa dayalı bir mali boyutun ve özel bir mali boyutun nasıl ekleneceğini gösterir.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb2dc5df96198f3c9f68fcac70b2e5dcbe8c8832
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175675"
---
# <a name="define-financial-dimensions"></a>Mali boyutları tanımlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu, varlığa dayalı bir mali boyutun ve özel bir mali boyutun nasıl ekleneceğini gösterir.  Kılavuz, USMF demo şirketini kullanır.


## <a name="create-an-entity-backed-financial-dimension"></a>Bir varlığa dayalı mali boyut oluştur
1. **Gezinti bölmesi > Modüller > Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar**'a gidin.
2. **Yeni**'ye tıklayın.
3. **Kullanıcı değerleri formu** alanında, mali boyuta temel oluşturacak sistem tanımlı bir varlık seçin. 
4. **Boyut adı** alanında, mali boyutu tanımlamak için bir değer girin. Ad, sistem tanımlı varlıktan farklı olabilir ancak boşluk veya özel karakterler içeremez.
5. **Etkinleştir**'e tıklayın. Mali boyut etkinleştirmesi tabloyu mali boyut adıyla güncelleştirir ve silinen boyutları kaldırır. Mali boyutu etkinleştirmeden önce boyut değerleri girebilirsiniz ancak mali boyut etkinleştirilene kadar kullanılamaz.  
6. Etkinleştirme iletisinde **Kapat** düğmesine tıklayın.
7. **Etkinleştir**'e tıklayın. Boyut etkinleştirmesi, toplu iş tarafından belirli bir tarih ve saatte çalışacak şekilde zamanlanabilir.  
8. **Eylem bölmesinde** **Boyut değerleri** öğesine tıklayın. Bazı boyut değerleri şirkete özgüdür. Şirket adı boyut değerleri listesinde gösteriliyorsa, şirkete özgü olup olmadığını doğrulayabilirsiniz.  

## <a name="create-a-custom-financial-dimension"></a>Bir özel mali boyut oluştur
1. Sayfayı kapatın.
2. **Yeni**'ye tıklayın.
3. **Şuradan alınan değerleri kullan** alanında, **Özel boyut** öğesini seçin.
4. **Boyut adı** alanında, mali boyutu tanımlamak için bir değer girin.
    - Ad, boşluk veya özel karakter içeremez.  
    - Boyut değerleri için girebileceğiniz bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz.   
    - Harf veya tire gibi her boyut değeri için aynı kalan karakterler girebilirsiniz. Her boyut değeri oluşturulduğunda değişen harfler ve sayılar için yer tutucu olarak sayı işaretleri (#) ve 've' işareti (&) de girebilirsiniz. Bir sayının yer tutucusu olarak sayı işareti (#) ve bir harfin yer tutucusu olarak "ve" işareti (&) kullanın.  Örnek: Boyutu CC harfleri ve üç sayıyla sınırlamak için CC-### biçim maskesini girin.  
5. **Etkinleştir**'e tıklayın. Mali boyut etkinleştirmesi tabloyu mali boyut adıyla güncelleştirir ve silinen boyutları kaldırır. Mali boyutu etkinleştirmeden önce boyut değerleri girebilirsiniz ancak mali boyut etkinleştirilene kadar kullanılamaz.     
6. **Etkinleştir**'e tıklayın. Boyut etkinleştirmesi, toplu iş tarafından belirli bir tarih ve saatte çalışacak şekilde zamanlanabilir.      
7. **Eylem bölmesinde** **Boyut değerleri** öğesine tıklayın.
8. **Yeni**'ye tıklayın.
9. **Boyut değeri** alanında, mali boyut değerinizi tanımlamak için bir ad girin.
10. **Açıklama** alanına, mali boyut değerinizi tanımlayan bir açıklama yazın.
