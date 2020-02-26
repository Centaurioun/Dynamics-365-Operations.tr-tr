---
title: ER Lifecycle Services'tan bir yapılandırmayı içe aktarma
description: Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184842"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>ER Lifecycle Services'tan bir yapılandırmayı içe aktarma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir.

Bu örnekte Litware, Inc. örnek şirketi için bir istenilen ER yapılandırmasını seçecek ve bunu LCS'ye içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir. Bu adımları tamamlamak için, öncelikle "Bir ER yapılandırmasını Lifecycle Services'a içeri almak" yordamındaki adımları tamamlamanız gerekir. Bu adımları tamamlamak için LCS erişimi de gereklidir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Yapılandırmalar'a tıklayın.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Veri modeli yapılandırmasının paylaşılan bir sürümünü silin
1. Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.
    * Örnek veri modeli yapılandırmasının ilk sürümü oluşturuldu ve LCS'ye "ER yapılandırmasını Lifecycle Services'a karşıya yüklemek" yordamında yayımlandı. Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz. Bir örnek veri modeli yapılandırmasının bu modeli daha sonra LCS'den içe aktarılacaktır.  
2. Listede, istenen kaydı bulun ve seçin.
    * Bu yapılandırmanın 'Paylaşımlı' durumda olan sürümünü seçin. Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.  
3. Durumu değiştir öğesine tıklayın.
4. Devam ettirme'ye tıklatın.
    * Seçili sürümün durumunu, silinebilir duruma gelmesi için 'Paylaşılan'dan 'Devam ettirilmeyen' olarak değiştirin.  
5. Tamam'a tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
    * Bu yapılandırmanın 'Devam ettirilmeyen' durumda olan sürümünü seçin.  
7. Sil'i tıklatın.
8. Evet'i tıklatın.
    * Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin kullanılabilir olduğunu unutmayın.  
9. Sayfayı kapatın.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alın
1. Listede, seçili satırı işaretleyin.
    * 'Litware, Inc.' yapılandırma sağlayıcısı için havuzların listesini açın. yapılandırma sağlayıcısı.  
2. Depolar'a tıklayın.
3. Aç'a tıklayın.
    * LCS deposunu seçin ve açın.  
4. Listede, seçili satırı işaretleyin.
    * 'Örnek yapılandırma modeli'nin ilk sürümü sürümlerin listesinde seçin.  
5. İçe aktar'ı tıklatın.
6. Evet'i tıklatın.
    * Seçili sürümün LCS'den aktarıldığını onaylayın.  
    * Bilgi iletisinin (formun üstünde bulunan) seçili sürümün alma işleminin başarılı tamamlama onayladığını dikkate alın.  
7. Sayfayı kapatın.
8. Sayfayı kapatın.
9. Yapılandırmalar'a tıklayın.
10. Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.
11. Listede, istenen kaydı bulun ve seçin.
    * Bu yapılandırmanın 'Paylaşılan' durumda olan sürümünü seçin.  
    * Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.  
