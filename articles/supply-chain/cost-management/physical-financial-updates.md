---
title: "Fiziksel ve mali güncellemeler"
description: "Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a0eeb5a57f9b82150150752c64e89c2c91856889
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="physical-and-financial-updates"></a>Fiziksel ve mali güncellemeler

[!include[banner](../includes/banner.md)]


Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar. 

Stok hareketleri, Microsoft Dynamics 365 for Finance and Operations'da fiziksel olarak ve mali olarak güncelleştirilebilir. Bazı fiziksel ve mali hareket türleri stok miktarlarını artırırken, bazıları bu miktarlar azaltır.

## <a name="physical-increases"></a>Fiziksel artışlar
Bir fiziksel hareket nakledildiğinde, hareket kaydının durumu **Alındı** olur. Aşağıdaki hareketler fiziksel artış olarak kabul edilir:

-   Satınalma siparişi girişi
-   Satış siparişinin sevk irsaliyesi iadesi
-   Bir üretim emrinin tamamlandı olarak rapor edilmesi
-   Üretim emri malzeme çekme listesinde ürüne göre

## <a name="financial-increases"></a>Mali artışlar
Bir mali giriş hareketi nakledildiğinde, miktarı artıran hareket kaydının durumu **Satın alındı** olur. Aşağıdaki hareketler mali artış olarak kabul edilir:

-   Satıcı faturası
-   İade için satınalma siparişi faturası
-   Üretim emri maliyeti
-   Hareket, kar ve zarar, sayım, malzeme listesi ve transfer vb. gibi pozitif miktar stok günlükleri

## <a name="transactions-that-increase-quantity"></a>Miktarı artıran hareketler
Miktarı artıran hareketler çalışan ortalama maliyet fiyatı üzerinden nakledilir. Finance and Operations, mali olarak takip edilen her bir stok boyutu için bu hareketlerin her birinin maliyetine dayalı olarak bir çalışan ortalama maliyeti fiyatı hesaplar. Çalışan ortalama maliyet fiyatları hakkında daha fazla bilgi için [Çalışan ortalama maliyet fiyatı](running-average-cost-price.md) bölümüne bakın.

## <a name="transactions-that-decrease-quantity"></a>Miktarı azaltan hareketler
Finance and Operations, miktarı azaltan bir hareket nakledildiğinde bu stokla bağlantılı stok modelinden bağımsız olarak, hesaplanan ortalama maliyet fiyatını kullanır. Miktarı azaltan hareket kesinlikle nakledilmeden önce başka bir harekete işaretlenmemiş olmalıdır. Fiziksel eldeki stokun negatif olması durumunda Finance and Operations, madde için **Madde** sayfasında tanımlanan stok maliyetini kullanır. **Not:** Birden fazla saha içeren bir işlev etkinleştirilirse maliyet yerine bir saha için **Varsayılan sipariş ayarları** sayfasında tanımlanan envanter maliyeti kullanılacaktır.

## <a name="physical-issues-vs-financial-issues"></a>Fiziksel çıkışlar ile mali çıkışlar karşılaştırması
Bir fiziksel çıkış hareketi nakledildiğinde, hareket kaydının durumu **Kesinti yapıldı** olur. Aşağıdaki hareketler fiziksel çıkışlar olarak kabul edilir:

-   Üretim emri malzeme çekme listesi günlüğü
-   Satış siparişinin sevk irsaliyesi
-   Satınalma siparişinin sevk irsaliyesi iadesi

Bir finansal hareket nakledildiğinde, hareket kaydının durumu **Satılan** olur. Aşağıdaki hareketler mali çıkışlar olarak kabul edilir:

-   Bir üretim emrinin sonlandırılması
-   Satış siparişi faturası
-   Satıcı fatura iadesi
-   Hareket, kar ve zarar, sayım, malzeme listesi ve transfer vb. gibi negatif miktar stok günlükleri

Miktarı azaltan hareketler çalışan ortalama maliyet fiyatı üzerinden nakledilir. Bu nedenle, her bir maddeye atanan stok modeline dayalı olarak, çıkış hareketlerinin giriş hareketlerine kapatılması için stok kapanışı prosedürü uygulanmalıdır.



