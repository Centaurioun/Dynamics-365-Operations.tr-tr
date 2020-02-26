---
title: Power Apps Yönetim merkezinde ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft Power Apps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010830"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps Yönetim merkezinde ortam oluşturulamıyor

**Çıkış**

- Kiracı/ortam yöneticisi, Microsoft Power Apps Yönetici merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
- Kullanıcılara ortam oluşturma adımını gerçekleştirme hakkı tanıyan bir ortam, bu adımı gerçekleştirmekte olan kullanıcıya doğrudan atanmamıştır.

**Çözüm**

Kiracı yöneticisinin, geçerli bir Power Apps P2 lisansını doğrudan ortam oluşturma adımını gerçekleştirecek kullanıcıya atamış olduğundan emin olun. Bu hakkı tanıyan Microsoft Dynamics servis planları buradadır.

| Tüm ürün stok tutma birimi (SKU)       | Power Apps P2 servis planı  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Çeşitli Microsoft Office SKU'larının da bu hakkı, tek başına Power Apps Plan 2 SKU'larıyla birlikte tanıdığına dikkat edin. Buradaki önemli nokta bu SKU'lardan birinin mevcut olması zorunluluğudur.

1. [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) gidin.
2. [İnsan Kaynakları sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) içindeki talimatları izleyerek ortamlar oluşturun.