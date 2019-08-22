---
title: Common Data Service'da kuruluş hiyerarşisi
description: Bu konu Finance and Operations ile Common Data Service arasında kuruluş verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789258"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Common Data Service'da kuruluş hiyerarşisi

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Microsoft Dynamics 365 for Finance and Operations finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar. İşletme mali öğeleri ve işlemleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.

Common Data Service'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur. Common Data Service tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Common Data Service'a eklenir.

## <a name="data-flow"></a>Veri akışı

Finance and Operations ve Common Data Service'dan olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir. Bu kuruluş hiyerarşisi Finance and Operations üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Common Data Service'da kullanıma sunulur. Aşağıdaki örnekte Common Data Service'ta Finance and Operations'tan Common Data Service'a tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir. 

![Mimari resmi](media/dual-write-data-flow.png)

## <a name="templates"></a>Şablonlar

Kuruluş hiyerarşisi varlık eşlemeleri, Finance and Operations'tan Common Data Service'a tek yönlü veri eşitleme için kullanılabilir.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Dahili Kuruluş Hiyerarşisi Amacı

Bu şablon, Finance and Operations'tan Dynamics 365 for Customer Engagement'a Kuruluş Hiyerarşisi Amacı varlığı için tek yönlü eşitleme sağlar.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Dahili Kuruluş Hiyerarşisi Türü

Bu şablon, Finance and Operations'tan Customer Engagement'a Kuruluş Hiyerarşisi Türü varlığı için tek yönlü eşitleme sağlar.

<!-- ![architecture image](media/dual-write-type.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AD | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Dahili Kuruluş Hiyerarşisi

Bu şablon, Finance and Operations'tan Customer Engagement'a Kuruluş Hiyerarşisi Yayımlanmış varlığı için tek yönlü eşitleme sağlar.

<!-- ![architecture image](media/dual-write-organization.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Dahili Kuruluş

Common Data Service'daki dahili kuruluş bilgileri iki Finance and Operations varlığından gelir: **Faaliyet birimi** ve **Tüzel kişilikler**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Faaliyet birimi

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
AD | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Tüzel kişilik

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
AD | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
yok | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Şirket

Finance and Operations ve Customer Engagement arasında tüzel kişi (şirket) bilgilerinin çift yönlü eşitlemesini sağlar.

<!-- ![architecture image](media/dual-write-company.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AD | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode