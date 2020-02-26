---
title: Proje faturaları için ödeme makbuzu biçimini ayarlama
description: İşletmeler fatura nakli ve ödemeleri için ödeme başvurusu sağlamak ve müşterilere yardımcı olmak amacıyla genellikle ödeme makbuzlarını yazılı şekilde faturaya iliştirirler.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4671e1df3bc86361736b5882d67e6b160b4c5644
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175073"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Proje faturaları için ödeme makbuzu biçimini ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

İşletmeler fatura nakli ve ödemeleri için ödeme başvurusu sağlamak ve müşterilere yardımcı olmak amacıyla genellikle ödeme makbuzlarını yazılı şekilde faturaya iliştirirler. Ödeme makbuzu proje veya servis faturaları, tahsilat mektupları, vade farkı dekontları, hesap özetleri, satış faturaları ve serbest metin faturalarının yanı sıra hesap ekstreleri için kullanılabilir. Ödeme makbuzlarınızı işlemek için ilk önce alacaklı kimlik numaranızı ve ödeme makbuzunu iliştirme biçimlerini ayarlayın.

Bu yordam, DEMF demo şirketini kullanır. 

Bu işlevsellik, birincil adresi Danimarka içinde olan tüzel kişilikler için kullanılabilir.


## <a name="set-up-a-creditor-id-number"></a>Bir Alacaklı kimliği numarası ayarlayın
1. Organizasyon yönetimi > Kuruluşlar > Tüzel kişilikler'e gidin.
2. Banka hesabı bilgileri bölümünü genişletin veya daraltın.
3. Düzenle öğesine tıklayın.
4. FI-Creditor Kimlik alanına bir değer yazın.
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Faturalar, notlar, mektuplar ve hesap özetleri bir ödeme makbuzu biçimi ayarlayın
1. Alacak hesapları > Kurulum > Formlar > Form kurulumu seçeneğine gidin.
2. Fatura sekmesine tıklayın.
3. Müşteri fatura alanındaki ilişkili ödeme ekine ait bir seçenek belirleyin.
    * Hiçbiri – Bir ödeme makbuzu yazdırmayın. Ödeme tutarı Danimarka Kronu'ndan (DKK) farklı bir para biriminde ise, bu seçeneği işaretleyin.   FIK 751 – Ödeme tutarını ve son ödeme tarihini ödeme makbuzu üzerine el ile yazmak isterseniz bir FIK 751 ödeme makbuzu yazdırın.   FIK 752 - Önceden basılmış ödeme tutarı ile bilgisayar tarafından oluşturulmuş bir ödeme makbuzu kullanmak istiyorsanız bir FIK 752 ödeme makbuzu yazdırın.  
4. Kaydet'e tıklayın.
5. Serbest metin faturası sekmesine tıklayın.
6. Serbest metin faturası alanındaki ilişkili ödeme ekine ait bir seçenek belirleyin.
    * Hiçbiri – Bir ödeme makbuzu yazdırmayın. Ödeme tutarı Danimarka Kronu'ndan (DKK) farklı bir para biriminde ise, bu seçeneği işaretleyin.   FIK 751 – Son ödeme tarihi ve ödeme tutarını ödeme makbuzu üzerine el ile yazmak istiyorsanız, bir FIK 751 ödeme makbuzu yazdırın.   FIK 752 - Önceden basılmış ödeme tutarı ile bilgisayar tarafından oluşturulmuş bir ödeme makbuzu kullanmak istiyorsanız bir FIK 752 ödeme makbuzu yazdırın.  
7. Kaydet'e tıklayın.
8. Vade farkı dekontu sekmesine tıklayın.
9. Vade farkı dekontu alanındaki ilişkili ödeme ekine ait bir seçenek belirleyin.
    * Hiçbiri – Bir ödeme makbuzu yazdırmayın. Ödeme tutarı Danimarka Kronu'ndan (DKK) farklı bir para biriminde ise, bu seçeneği işaretleyin.   FIK 751 – Son ödeme tarihi ve ödeme tutarını ödeme makbuzu üzerine el ile yazmak istiyorsanız, bir FIK 751 ödeme makbuzu yazdırın.   FIK 752 - Önceden basılmış ödeme tutarı ile bilgisayar tarafından oluşturulmuş bir ödeme makbuzu kullanmak istiyorsanız bir FIK 752 ödeme makbuzu yazdırın.  
10. Kaydet'e tıklayın.
11. Tahsilat mektubu sekmesini tıklatın.
12. Tahsilat mektubu alanındaki ilişkili ödeme ekine ait bir seçenek belirleyin.
    * Hiçbiri – Bir ödeme makbuzu yazdırmayın. Ödeme tutarı Danimarka Kronu'ndan (DKK) farklı bir para biriminde ise, bu seçeneği işaretleyin.   FIK 751 – Son ödeme tarihi ve ödeme tutarını ödeme makbuzu üzerine el ile yazmak istiyorsanız, bir FIK 751 ödeme makbuzu yazdırın.   FIK 752 - Önceden basılmış ödeme tutarı ile bilgisayar tarafından oluşturulmuş bir ödeme makbuzu kullanmak istiyorsanız bir FIK 752 ödeme makbuzu yazdırın.  
13. Kaydet'e tıklayın.
14. Hesap özeti sekmesini tıklatın.
15. Hesap özeti alanındaki ilişkili ödeme ekine ait bir seçenek belirleyin.
    * Hiçbiri – Bir ödeme makbuzu yazdırmayın. Ödeme tutarı Danimarka Kronu'ndan (DKK) farklı bir para biriminde ise, bu seçeneği işaretleyin.   FIK 751 – Son ödeme tarihi ve ödeme tutarını ödeme makbuzu üzerine el ile yazmak istiyorsanız, bir FIK 751 ödeme makbuzu yazdırın.   FIK 752 - Önceden basılmış ödeme tutarı ile bilgisayar tarafından oluşturulmuş bir ödeme makbuzu kullanmak istiyorsanız bir FIK 752 ödeme makbuzu yazdırın.  
16. Kaydet'e tıklayın.
17. Sayfayı kapatın.
