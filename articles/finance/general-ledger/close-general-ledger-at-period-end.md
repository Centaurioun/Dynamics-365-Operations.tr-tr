---
title: Genel muhasebeyi dönemi sonunda kapatma
description: Bu konu, genellikle bir dönem kapanışı için genel muhasebe gerçekleştirirken tamamlanmış görevleri açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cabdce5e23704fbf12e631a138235174ebc5772
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770793"
---
# <a name="close-the-general-ledger-at-period-end"></a>Genel muhasebeyi dönemi sonunda kapatma

[!include [banner](../includes/banner.md)]

Bu konu, genellikle bir dönem kapanışı için genel muhasebe gerçekleştirirken tamamlanmış görevleri açıklar. 

Genel muhasebede bir dönem veya bir yıl için kapatma prosedürlerini tamamlayabilirsiniz. Kapanış işlemleri, sistemi yeni bir dönem için hazırlar. Sistemi yeni yıl için hazırlamak için mutlaka yıl sonu kapanış işlemini yürütmeniz gerekir. Her kuruluşun farklı işlemleri ve bir dönemin sonu için gerçekleştirdiği adımları vardır. Dönem sonu için bazı isteğe bağlı adımlar şunlardır:

-   Borç hesapları, Alacak hesapları ve Stok gibi tüm diğer modüler için tüm görevleri tamamlayın.
-   Tüm günlüklerin nakledildiğini doğrulayın.
-   Gerçekleşmemiş kazanç veya kayıp tutarları üretmek için yabancı para biriminde yeniden değerleme çalıştırın.
-   Her bir genel muhasebe hesabı için hareketleri kapatın.
-   Gerekli tahsisatları işleyin.
-   Dönem sonu ayarlamaları el ile nakledin.
-   Hareketleri günlüğe aktarın ve **Genel muhasebe günlüğü** raporunu gözden geçirin.
-   Bir konsolidasyon şirketini veya Mali raporlamayı kullanarak bir konsolidasyon gerçekleştirin.
-   Mali raporlamayı kullanarak dönem sonu mali beyanları oluşturun.
-   Genel muhasebe dönemlerini **Beklemede** konumuna ayarlayın, böylece daha fazla nakil oluşmaz. Ayrıca, daha iyi bir kontrol için, dönem sonu faaliyetleri gerçekleşirken bir dönemi bir özel kullanıcı grubuyla sınırlayabilirsiniz. Kapatılmış bir dönemi yeniden açamayacağınızdan dönemleri **Kalıcı olarak kapalı** olarak ayarlamak iyi bir fikirdir.

Mali dönem kapanış çalışma alanı, gerekli çeşitli dönem sonu işlemlerini organize etmek ve izlemek için kullanabilir. 


Daha fazla bilgi için aşağıdaki konulara bakın:
- [Mali dönem kapatma çalışma alanı](financial-period-close-workspace.md) 
- [Yıl sonu kapanışı](Year-end-close.md)  
- [Toplu mali dönem kapatma](tasks/mass-financial-period-close.md)



