---
title: "Banka mutabakatı eşleştirme kuralları oluşturma"
description: "Bu makale, banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturmayı anlatır. Mutabakat eşleştirme kuralları, mutabakat süreci sırasında banka ekstresi satırlarını ve banka belge satırlarını filtrelemek için kullanılan bir ölçüt kümesidir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 60cd6a7f7b4d5c3acc68aa27c920f42f1d4b910e
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Banka mutabakatı eşleştirme kuralları oluşturma

[!include[banner](../includes/banner.md)]


Bu makale, banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturmayı anlatır. Mutabakat eşleştirme kuralları, mutabakat süreci sırasında banka ekstresi satırlarını ve banka belge satırlarını filtrelemek için kullanılan bir ölçüt kümesidir.

Banka mutabakatı sürecini kolaylaştırmak için banka mutabakatı eşleştirme kuralları ve mutabakat eşleştirme kural kümeleri oluşturabilirsiniz. Bir mutabakat eşleştirme kuralı, mutabakat süreci sırasında banka ekstresi satırlarını ve Microsoft Dynamics 365 for Finance and Operations, Enterprise edition banka hareket satırlarını filtrelemek için kullanılan bir ölçüt kümesidir. Mutabakat eşleştirme kurallarını ayarlamak için **Mutabakat eşleştirme kuralları** sayfasını kullanın. Birden fazla eşleştirme kuralı oluşturabilir ve ardından **Mutabakat eşleştirme kural kümeleri** sayfasında bir mutabakat eşleştirme kural kümesi oluşturabilirsiniz. 

> [!NOTE] 
> Banka mutabakatı eşleştirme kuralları, bir elektronik banka ekstresi için gelişmiş banka mutabakatı kullanarak mutabakat sağladığınızda kullanılır. 

**Mutabakat eşleştirme kuralları** sayfasında, eşleştirme kuralı çalıştırıldığında hangi eylemlerin ve seçimi ölçütlerinin kullanılacağını seçebilirsiniz. **Eylemler** alan grubunda, mutabakat işlemi sırasında eşleştirme kuralı çalıştırıldığı zaman gerçekleştirilecek eylemi seçin.  

> [!NOTE] 
> Belirttiğiniz seçenek görüntülenen alanları belirler.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eylem**                         |                                                                                                                                                                                                                                                                                                               | **Eylem seçildiğinde kullanılabilecek seçim ölçütleri**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Banka belgesiyle eşleştir**       | **Banka mutabakatı çalışma sayfası** sayfasından eşleştirme kuralı çalıştırıldığında banka belgelerinin ve banka ekstresi satırlarının nasıl eşleştirileceğini tanımlayan ölçütler oluşturun. Hareket satırları, Hızlı Sekmelerde ayarlanan ek ölçütlere göre seçilir.                                | **1. adım: Eşleştirme kuralını tanımlayın** – Finance and Operations banka hareketleriyle hangi banka ekstrelerinin eşleştirilmesi gerektiğini tanımlayan ölçütleri seçin. **2. Adım (isteğe bağlı): Eşleştirme kurallarının çalıştırılacağı ekstre satırlarını seçin:** Kuralların hangi ekstre satırında çalıştırılacağını belirlemek için bir filtre uygulayın.                                                                                                                                                                                                                                                                                                               |
| **Ters ekstre satırlarını temizle** | Eşleştirme kuralı çalıştırıldığında **Banka mutabakatı çalışma sayfası** sayfasından hangi ters ekstre satırlarının kaldırılacağını tanımlayan ölçütler oluşturun. Bu seçenek, bir banka hatasının, iki banka ekstresi satırının içe aktarılan banka ekstresinde listelenmesine neden olduğunda ve satırlar için mutlaka mutabakat sağlanması gerektiğinde kullanılır. | **1. adım**:**Ters ekstre satırlarını bulun**– Ters banka ekstresi satırlarını seçmek için seçim ölçütlerini ekleyin. Örneğin, yalnızca denetimleri seçmek için, Alan alanında **Banka hareket kodu** öğesini seçin, **İşleç** alanında artı işaretini (+) seçin ve Değer alanına **Denetimleri** girin. **2. Adım: Orijinal ekstre satırlarını bulun** – Banka belgesi satırlarını banka ekstresi satırlarıyla eşleştirmek için seçim ölçütleri ekleyebilirsiniz. **3. Adım: Finance and Operations banka hareketlerini bulun** – Finance and Operations banka hareketlerini banka ekstresi satırlarıyla eşleştirmek için seçim ölçütleri ekleyebilirsiniz. |
| **Yeni hareketleri işaretle**          | Eşleştirme kuralı çalıştırıldığında **Banka mutabakatı çalışma sayfası** sayfasında yeni hareketlerin nasıl işaretleneceğini tanımlayan ölçütler oluşturun.                                                                                                                                                                 | **1. adım: Ekstre satırlarını bulun**– **Banka mutabakatı çalışma sayfası** sayfasından hangi banka ekstresi satırlarının seçileceğini belirleyen seçim alanlarını ekleyin. **2. Adım: Finance and Operations'ı bulun – Banka belgeleri satırlarını aramak için seçim ölçütleri ekleyebilirsiniz. Hiçbir banka belgesi bulunursa, bir ekstre satırı yeni bir hareket olarak işaretlenecektir.                                                                                                                                                                                                                                             |

 






