---
title: İleri tarih atılmış çekleri ayarlama
description: Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 035f6e3b0268f8ee4c9006ca5f0527133cf2771c
ms.sourcegitcommit: 69f8233e86b32347474a25d83b4ac5920f60407d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2019
ms.locfileid: "2538490"
---
# <a name="set-up-postdated-checks"></a>İleri tarih atılmış çekleri ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır. Ayrıca, verilen çekler, alınan çekler ve stopaj vergisi takas hesaplarını belirtebilirsiniz. Gelecekte ödeme yapmak veya almak için çıkartılan vadeli çekler. Çekin hesap defterlerinde, vade tarihinden önce yansıtılmasına gerek olup olmadığını belirtebilirsiniz.



Bu yordamın rolü Haznedar'dır. Bu yordam, USMF demo şirketini kullanır.


## <a name="set-up-postdated-checks"></a>İleri tarih atılmış çekleri ayarlama
1. Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.
2. Vadeli çekler sekmesini tıklatın.
3. Vadeli çekleri etkinleştirin onay kutusunu işaretleyin veya işareti kaldırın.
4. Vadeli çekler için defter girişlerini nakletme onay kutusunu temizleyin veya seçin.
5. Verilen çekler için takas hesabı alanında için istediğiniz değerleri belirtin.
6. Alınan çekler için takas hesabı alanında için istediğiniz değerleri belirtin.
7. Takas girişleri yevmiye defterine, bir değer yazın.
8. İleri tarih atılmış çekleri bu satıcı ödeme günlüğüne transfer et alanına bir değer yazın.
9. Stopaj vergisi takas hesabı alanına, istediğiniz değerleri belirleyin.
10. Kaydet'e tıklayın.
11. Sayfayı kapatın.
12. Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.
13. Yeni'ye tıklayın.
14. Ödeme yöntemi alanına bir değer girin.
15. Çek miktarının takas hesabına nakledildiğini belirtmek için vadeli hesap takas nakli seçeneğini işaretleyin.
16. Hesap türü alanında "Banka"yı seçin.
    * Ödeme yönteminin mahsup hesabı bir banka olacaktır.  
17. Ödeme hesabı alanında istediğiniz değerleri belirtin.
    * Fatura miktarının çekilmesi için kullanılacak banka hesabını seçin.  
18. Kaydet'i tıklatın.
19. Sayfayı kapatın.
