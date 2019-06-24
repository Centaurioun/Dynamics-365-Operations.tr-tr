---
title: Project Service Automation
description: Bu konu, Project Service Automation'dan Finance and Operations'a tümleştirme çözümü hakkında bilgiler sağlar. Bu tümleştirme çözümü Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation arasında veri eşitleme için Veri tümleştirme özelliğini Common Data Service aracılığıyla kullanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557318"
---
# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

Project Service Automation'tan Finance and Operations çözümüne tümleştirme, Veri tümleştirme özelliğini Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation arasında eşitlemek için Common Data Service aracılığıyla kullanmaktadır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, projeler, proje sözleşmeleri, proje sözleşme satırları, proje sözleşme satırı kilometre taşları, proje görevleri, gider hareketi kategorileri, saat tahminleri ve gider tahminlerinin Project Service Automation'dan Finance and Operations'a akışına olanak tanır.

> [!NOTE]
> - Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.
> - Finance and Operations 7.3.0 kullanıyorsanız KB 4074835'i yüklemeniz gerekir. Yüklemeden sonra sabit fiyatlı projeleri tümleştirebilirsiniz.
> - Finance and Operations 7.3.0 kullanıyorsanız ve Project Service Automation'dan masraf hareketlerini görüntülüyorsanız bu masrafları proje faturasına dahil etmek için KB 4345320'yi yüklemeniz gerekir.
> - Microsoft Dynamics 365 for Finance and Operations sürüm 8.0 kullanıyorsanız, proje görevleri tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlev kilitlemeyi kullanabilirsiniz.
> - Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.1 kullanıyorsanız, fiili değerleri eşitleyebileceksiniz.

Project Service Automation'ı Finance and Operations'la tümleştirebilmeniz için Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir. Daha fazla bilgi için bkz. [Project Service Automation tümleştirme parametreleri](PSA-parameters.md).

Bu tümleştirme çözümü aşağıdaki senaryolarda doğrudan eşitlemeyi etkinleştirir:

- Proje sözleşmelerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Project Service Automation'da projeler oluşturma ve bu projeleri Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Proje sözleşme satırlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Proje sözleşme satırı kilometre taşlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Proje görevlerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Gider hareketi kategorilerini Finance and Operations'ta yönetme ve Finance and Operations'tan Project Service Automation'a doğrudan eşitleme.
- Project Service Automation'da proje saat tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Project Service Automation'da proje gider tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Finance and Operations'a nakledilebilmeleri için Project Service Automation'da proje süresi, gider ve ücret gerçek değerleri ile Project Service Automation tümleştirme günlüğünde proje hareketleri oluşturun.

## <a name="data-synchronization"></a>Veri eşitleme

Aşağıdaki şekilde, Project Service Automation ile Finance and Operations arasında verilerin tümleştirmenin bir parçası olarak nasıl eşitlendiği gösterilmektedir.

> [!NOTE]
> Şu anda tüm şablonlar kullanımda değil. Şablonlar tamamlandıkça yayınlanacaktır.

[![Finance and Operations ile Project Service Automation tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations için sistem gereksinimleri

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3'ü platform güncelleştirmesi 12 veya daha ileri bir platform güncelleştirmesiyle birlikte yüklemeniz gerekir.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation için sistem gereksinimleri

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

- Microsoft Dynamics 365 for Project Service Automation sürüm 9.0.0.0 veya üstü
- Microsoft Dynamics 365 for Sales, sürüm 1.14.0.0 (v14) veya sonraki sürüm için Aday'dan nakite çözüm.
- Project Service Automation'tan Finance and Operations'a çözümü, Microsoft Dynamics 365 for Project Service Automation sürüm 1.0.0.0 veya sonrası için

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü Project Service Automation örneğinize yükleme

[Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016)'dan Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü indirin ve çözümün içinde verilen yönergeleri izleyin.