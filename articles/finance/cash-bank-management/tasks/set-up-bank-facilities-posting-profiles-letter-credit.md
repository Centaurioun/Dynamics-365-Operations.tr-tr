---
title: Kredi mektubu için banka hizmetlerini ve banka deftere nakil profillerini ayarlama
description: Bu yordam, akreditif mektubunu işlemek için gerekli olan banka tesisi ve nakletme profilini oluşturmayı gösterir.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3d35bd265ad31da083d2437fae886569766085
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188085"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Kredi mektubu için banka hizmetlerini ve banka deftere nakil profillerini ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, akreditif mektubunu işlemek için gerekli olan banka tesisi ve nakletme profilini oluşturmayı gösterir. 

Bu görevler, USMF demo şirketini kullanır.






## <a name="general-ledger-parameter"></a>Genel muhasebe defteri parametresi
1. Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.
2. Banka belgesi bölümünü genişletin.
3. Akreditif mektubunu içeri alma seçeneğini etkinleştir'i seçin.
4. Akreditif mektubunu dışarıya verme seçeneğini etkinleştir'i seçin.
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.

## <a name="create-bank-facility"></a>Banka hizmeti yarat
1. Nakit ve Banka yönetimi > Kurulum > Banka tesisleri seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Tesis grubu alanında, banka tesisi grup adını girin.
4. Tanım alanında, banka tesisi grup tanımını girin.
5. Kaydet'e tıklayın.
6. Tesis türleri sekmesini tıklatın.
7. Yeni'ye tıklayın.
8. Tesis türü alanına benzersiz bir kod yazın.
9. Açıklama alanına bir değer girin.
10. Tesis grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
11. Listede, istenen kaydı bulun ve seçin.
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. Tesis niteliği alanında banka tesisinin niteliğini seçin.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.

## <a name="bank-posting-profile"></a>Banka nakil profili
1. Nakit ve Banka yönetimi > Kurulum > Banka belgesi nakletme profili seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Hesap/Grup numarası alanında, aramayı açmak için açılır menü düğmesini tıklatın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Hesap kesme için ana hesabı seçin.
    * Nakit akışı tahminini hesaplarken bu hesap kullanılır.  
7. Gider hesabı alanında masraf hareketleri hesabını seçin.
8. Marj hesabı alanında marj hareketleri hesabını seçin.
    * Bu hesaba açılış marjı nakledilirken alacak, ödeme nakledilirken ise borç kaydedilir.  
9. Kaydet'e tıklayın.
