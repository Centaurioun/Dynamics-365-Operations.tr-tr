---
title: İade edilen maddelerin kısmi teslimatlarını alma
description: Kısmi teslimatlar sipariş iadesi sevkiyatlarına göre değil, sipariş iadesi satırlarına göre tanımlanır.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570331"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>İade edilen maddelerin kısmi teslimatlarını alma    

[!include [banner](../includes/banner.md)]


Kısmi teslimatlar sipariş iadesi sevkiyatlarına göre değil, sipariş iadesi satırlarına göre tanımlanır.

Diğer bir deyişle, bir sipariş iadesi satırındaki tam miktarı alır ancak sipariş iadesindeki diğer satırlardan hiçbir şey almazsanız, teslimat kısmi bir teslimat olmaz. Ancak, bir sipariş iadesi satırında belirli bir maddenin 10 biriminin iade edilmesi isteniyorsa, ancak siz yalnızca dördünü alırsanız, bu kısmi bir teslimattır.

Bir iade sevkiyatı bir sipariş iadesi satırının tam miktarından daha azını içeriyorsa, sevkiyatı bir kenara bırakıp iade edilen miktarın geri kalanının gelmesini bekleyebilirsiniz veya kısmi miktarı kaydedip deftere nakledebilirsiniz.

## <a name="register-and-post-a-partial-quantity"></a>Kısmi miktarı kaydetme ve deftere nakletme

1.  **Varışa genel bakış - Ambar: %1, Nokta: %2, Günlük adı: %3** formunda varış için bir iade siparişi seçtikten sonra, varış günlüğünü oluşturmak için **Varışı başlat**'a tıklayın ve ardından **Günlükler** \> **Girişlerden varışları göster**'e tıklayarak **Yerleşim günlüğü** formunu açın.

2.  Çalışmak istediğiniz günlük satırını seçin ve **Satırlar**'ı tıklayarak **Günlük satırları, yerleşimler** formunu açın.

3.  Yalnızca kısmi miktarın geldiği madde numarasının satırını seçin ve **Böl** formunu açmak için sırasıyla **İşlevler** \> **Böl**'e tıklayın.

4.  **Miktarı böl** alanında alınan toplam madde sayısı için miktarı girin ve **Tamam**'a tıklayın.

5.  **Günlük satırları, yerleşimler** formunda gelen madde miktarı için satırı seçin ve **Deftere naklet**'e tıklayın. Maddeler geldikten sonra ek miktar için satırı deftere nakledebilirsiniz.



