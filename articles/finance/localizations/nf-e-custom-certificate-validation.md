---
title: NF-e özel sertifika doğrulaması
description: Bu konu, NF-e özel sertifikasını etkinleştirme ve kullanma hakkında bilgi sağlar.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 3c88c4adafb78b807842b0b41c69b19cf2b7aa23
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973104"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e özel sertifika doğrulaması

[!include [banner](../includes/banner.md)]

NF-e özel sertifika doğrulama özelliğini etkinleştirdiğinizde, özel doğrulama Web hizmetleriyle bağlantı yapılmasına izin verir. Bu bağlantı, SEFAZ üzerinden NF-e aktarmak ve yetkilendirme almak için gereklidir.

Sertifika V5'deki **Sunucu kimlik doğrulama amacı** özelliği, Brezilya Kök Sertifika Yetkilisi tarafından verilir. Bu özellik varsayılan olarak kapalıdır ve el ile etkinleştirilmesi gerekir. Bazı durumlarda, otomatik sertifika güncelleştirme bu özelliği artık etkin olmayacak şekilde değiştirebilir. Bu durumda, TLS bağlantısı etkilenir ve artık güvenilir değildir. Minas Gerais (MG) ve Paraná (PR) eyaletlerinin üretim ortamlarında NF-e verme yeteneği de etkilenebilir.

Bu güncelleştirme, sertifika doğrulaması için alternatif bir çözüme olanak tanır, başka bir deyişle, güvenli bir iletişim kurma olanağı vardır.

