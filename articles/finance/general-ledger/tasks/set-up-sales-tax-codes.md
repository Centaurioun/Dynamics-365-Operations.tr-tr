---
title: Satış vergisi kodlarını ayarlama
description: Bu konuda, Dynamics 365 Finance'da satış vergisi kodlarının nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45a4a7a20b20961d707e43b35d61c10a08c74943
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185992"
---
# <a name="set-up-sales-tax-codes"></a>Satış vergisi kodlarını ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konuda, satış vergisi kodlarının nasıl ayarlanacağı açıklanmaktadır. Tüzel kişiliğin hesaplamak, tahsil etmek ve vergi dairelerine ödemekle yükümlü olduğu her dolaylı vergi ve harç için satış vergisi kodları oluşturulur.

Bu görevde USMF demo şirketi kullanılmaktadır.

1. **Gezinme bölmesi > Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kodları**'na gidin.
2. **Yeni**'yi seçin.
3. **Satış vergisi kodu** alanına bir değer girin.
4. **Ad** alanına bir değer yazın.
5. Bu satış vergisinin hangi vergi dairesine, hangi aralıklarda bildirilip ödenmesi gerektiğini belirtmek üzere açılır listeyi açarak bir **Kapatma dönemi** seçin.
6. Satış vergisinin genel muhasebeye nakledileceği ana hesapları belirtmek için bir **Genel muhasebe deftere nakil grubu** seçin.
7. **Hesaplama** hızlı sekmesini genişletin. Burada, satış vergisi tutarlarının nasıl hesaplanacağını denetleyen birden çok alan vardır. Bu alanları gerektiği gibi doldurun.  
8. Arabirimin üst kısmındaki **Eylem Bölmesinde**, **Satış vergisi kodunu** seçin.
9. **Değerler**'i seçin.
10. Bu vergi kodunun değerini **değer** sütununa girin.
    - **Hesaplama** hızlı sekmesindeki Kaynak alanında Birim başına tutar seçiliyse, değer, hareketteki miktarla çarpılarak satış vergisi tutarı hesaplanır.  Vergi kodu birim tabanlı bir vergi değilse, değer, satış vergisi tutarını hesaplamak için bu vergi kodunun Kaynağına uygulanan yüzdedir.     
11. **Kaydet**'i seçin.
12. Sayfayı kapatın.
13. **Kaydet**'i seçin.
