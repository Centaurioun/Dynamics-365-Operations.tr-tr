--- 
title: "Satış vergisi için genel muhasebe deftere nakil grupları ayarlama"
description: "Satış vergisi hesaplanır ve Genel muhasebe deftere nakil gruplarında belirtilen ana hesaplara nakledilir."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0682afed4664e1491ed46e4e40f467015701711
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Satış vergisi için genel muhasebe deftere nakil grupları ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Satış vergisi hesaplanır ve Genel muhasebe deftere nakil gruplarında belirtilen ana hesaplara nakledilir. Genel muhasebe deftere nakil grupları, her bir satış vergisi koduna eklenir. Her satış vergisi kodu için ayrı ayrı genel muhasebe deftere nakil grupları ayarlayabilir, bir genel muhasebe deftere nakil grubunu tüm satış vergisi kodları için kullanabilir veya satış vergisi kodlarına birden fazla genel muhasebe deftere nakil grubu atayabilirsiniz. Bu kayıtta DEMF demo şirketi kullanılmaktadır. 

1. Vergi > Kurulum > Satış vergisi > Genel muhasebe deftere nakil grupları'na gidin.
2. Yeni'ye tıklayın.
3. Genel muhasebe deftere nakil grubu alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Satış vergisi borcu alanında, vergi dairesine borç yazılacak giden satış vergileri için ana hesabı seçin.
    * Vergiye tabi mal ve hizmetler satıyorsanız, satış vergileri, vergi makamı adına tahsil edilir.  
6. Satış vergisi alacağı alanında, vergi dairesinden alınacak gelen vergiler için ana hesabı seçin.
    * Vergiye tabi mal ve hizmetler satın alıyorsanız, vergileri, vergi makamı adına satıcılar tahsil eder. Genel muhasebe parametreleri sayfasında Satış vergisi vergilendirme kurallarını uygula seçeneği belirtildiyse bu alan kullanılmaz. Bunun yerine, satıcılara ödenen satış vergileri, satın almada kullanılan hesaba borç kaydedilir.   
7. Kullanım vergisi gideri alanında, AB ters gider GST/HST'sinin bir parçası olarak satıcıların vergi dairesinden talep etmediği veya vergi dairesine bildirmediği, vergiden düşülebilir Kullanım vergileri için ana hesabı seçin.
    * Harekette kullanılan Satış vergisi grubunda Satış vergisi kodu için Kullanım vergisi seçeneğinin belirtilmesi gerekir.  Genel muhasebe parametreleri sayfasında Satış vergisi vergilendirme kurallarını uygula seçeneği belirtildiyse bu alan kullanılmaz.   
8. Kullanım vergisi borcu alanında, vergi dairelerine borç yazılacak giden Kullanım vergilerini nakletmek için ana hesabı seçin.
    * Kullanım vergisini nakletmek için, Satış vergisi grubunda Satış vergisi kodu için Kullanım vergisi seçeneğinin belirtilmesi gerekir. Genel muhasebe parametrelerinde Satış vergisi vergilendirme kurallarını uygula seçeneği belirtilirse, mahsubun hareket gider hesabına nakledilmesi gerekir.   
9. Kapatma hesabı alanında, Kullanım vergisi borcu ve Satış vergisi alacağı alanlarında belirtilen genel muhasebe hesaplarının net bakiyesinin nakledileceği ana hesabı seçin.
    * Satış vergisini kapat ve deftere naklet işi çalıştırılınca bakiye oluşturulur.  Kapatma döneminin Vergi dairesi bir satıcı hesabıyla ilişkilendirilmişse, bakiye, satıcı hesabına nakledilir.   
10. Satıcı nakit iskontosu alanında, bu Genel muhasebe deftere nakil grubuyla ilişkili Satış vergisi kodları için nakit iskontosunun nakledileceği ana hesabı seçin.
    * Bu, isteğe bağlıdır ve hiç hesap girilmezse, Nakit iskontosu kodlarındaki ana hesap kullanılır. Satış vergisi gruplarında Nakit iskontosundaki ters satış vergisi seçeneği kullanılıyorsa, Genel muhasebe deftere nakil grubu başına farklı hesaplar kullanırken yararlı olabilir.  
11. Müşteri dosyası iskontosu alanında, bu Genel muhasebe deftere nakil grubuyla ilişkili Satış vergisi kodları için nakit iskontosunun nakledileceği ana hesabı seçin.
    * Bu, isteğe bağlıdır ve hiç hesap girilmezse, Nakit iskontosu kodlarındaki ana hesap kullanılır. Satış vergisi gruplarında Nakit iskontosundaki ters satış vergisi seçeneği kullanılıyorsa, Genel muhasebe deftere nakil grubu başına farklı hesaplar kullanırken yararlı olabilir.  
12. Kaydet'e tıklayın.

