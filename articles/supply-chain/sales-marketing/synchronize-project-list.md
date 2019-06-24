---
title: Finance and Operations'tan Field Service'a proje listelerini eşitleme
description: Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1525889"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Proje listesini Finance and Operations'dan Field Service'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve görevler, Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine projelerin eşitlenmesinde kullanılır.

**Veri Tümleştirmesindeki Şablon**
- Projeler (Fin and Ops'tan Field Service'a)

**Veri tümleştirme projesindeki görev**
- Projeler

Aşağıdaki eşitleme görevlerinin, proje listesinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:
- Hesaplar (Sales'ten Fin and Ops'a) 

## <a name="entity-set"></a>Varlık kümesi
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projeler                |

## <a name="entity-flow"></a>Varlık akışı
Finance and Operations'ta oluşturulan projeler. **Proje türü**, **Zaman ve malzeme**'ye ayarlanır ve **Proje aşaması**, **İşlevde olan** projelere ayarlanır, Field Service'ta **Harici Proje** varlığına eşitlenir, Proje numarası, Proje adı, Proje aşaması ve Müşteri hesap bilgisi de dahil. **Harici Proje** listesi, Field Service iş emirlerini, Finance and Operations projeleriyle eşleştirmekte kullanılır.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
**Harici Proje** varlığı, tüm projeleri Finance and Operations'tan alır. **Harici Proje** alanı, **İş Emri** varlığına eklenmiştir. Bu bir arama alanıdır, iş amirlerinizi bir proje ile etiketlediğinizde, satış siparişi Finance and Operations içindeki bir projeye bağlanacaktır. **Sistem Durumu**, **Açık – Sürmekte(690,970,000)** daha yüksek bir duruma değiştikten sonra, **Harici Proje** alanı kilitlenir ve değeri artık ekleyemez, kaldıramaz veya değiştiremezsiniz.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu
### <a name="finance-and-operations"></a>Finance and Operations
Veri varlığı projeleri için izlemeyi etkinleştir

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Projeler (Fin and Ops'tan Field Service'a): Projeler

[![Veri tümleştirmede şablon eşleme](./media/FSProject1.png)](./media/FSProject1.png)