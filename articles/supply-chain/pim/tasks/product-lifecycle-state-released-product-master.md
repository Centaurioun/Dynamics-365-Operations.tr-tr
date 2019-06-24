---
title: Ürün yaşam döngüsü durumunu serbest bırakılan bir ana ürüne atama
description: Bu yordam, serbest bırakılan bir ana ürüne ve onun ürün çeşitlerine nasıl ürün yaşam döngüsü durumu atanacağını açıklar.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555920"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Ürün yaşam döngüsü durumunu serbest bırakılan bir ana ürüne atama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, serbest bırakılan bir ana ürüne ve onun ürün çeşitlerine nasıl ürün yaşam döngüsü durumu atanacağını açıklar. Önkoşul: Bu görev kılavuzunu oynatabilmek için önce "Yeni ürün yaşam döngüsü durumu oluşturma" görev kılavuzunu oynatarak en az bir ürün yaşam döngüsü durumu oluşturmuş olduğunuzdan emin olmanız gerekir.


## <a name="find-a-released-product-master"></a>Serbest bırakılan bir ana ürünü bulma
1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. Listede, istenen kaydı bulun ve seçin.

> [!NOTE]
> Bir ana üründe Ürün alt türü Ana ürün bulunuyor.  

## <a name="update-the-lifecycle-state"></a>Yaşam döngüsü durumunu güncelleştirme
1. Düzenle öğesine tıklayın.
2. Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.
3. Kaydet'e tıklayın.
4. Evet'i tıklatın.

> [!NOTE]
> Evet seçilirse, serbest bırakılan ana ürünle aynı orijinal duruma sahip serbest bırakılmış tüm ilgili ürün çeşitleri de yeni ürün yaşam döngüsü durumuna güncelleştirilir. Hayır seçilirse tüm ürün çeşitlerinin geçerli durumları korunur. Serbest bırakılan ana üründen farklı ürün yaşam döngüsü durumuna sahip ürün çeşitleri güncelleştirilmez.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Ürün çeşitlerinin yaşam döngüsü durumunu doğrulama
1. Serbest bırakılan ürün çeşitleri'ne tıklayın

> [!NOTE]
> Tüm ürün çeşitlerinin seçilen yaşam döngüsü durumunu serbest bırakılan ana üründen devraldığını unutmayın.  

2. Listede, seçili satırı işaretleyin.
3. Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.
