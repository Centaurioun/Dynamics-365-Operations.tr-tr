---
title: Sabit kıymet alım deftere nakil hesapları
description: Bu makalede, genel muhasebe deftere nakil hesaplarının, kıymet alımları için nasıl ayarlanacağı açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fea6b1cd79b5536341a7cb50e5592ea38a7392d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187257"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a>Sabit kıymet alım deftere nakil hesapları

[!include [banner](../includes/banner.md)]

Bu makalede, genel muhasebe deftere nakil hesaplarının, kıymet alımları için nasıl ayarlanacağı açıklanmaktadır.

Sabit kıymet alımlarını deftere nakletmek için kullanılan hesaplar kıymeti almak için kullanılan yönteme bağlı olarak değişebilir. Sabit kıymet nakil profilleri sayfasında, genel muhasebe hesapları sekmesinde, genel muhasebeye nakletmek için sabit kıymet hesaplarını ayarlamak için Alım ve Alım ayarlamayı seçin. 

Günlüklerde ve satınalma siparişlerinde, Genel muhasebe hesabı genellikle yeni bir sabit kıymetin alım değerinin borç kaydedildiği bilanço hesabıdır. Bu hesap günlüklerde görüntülenmez ve hareketlerde değiştirilemez. 

Mahsup hesap ayrıca bir bilanço hesabıdır. Genel günlükte ve sabit kıymetler günlüğünde, bu hesap genellikle kıymetin alımı için ödeme yapmak üzere kullanılan banka hesabı olacaktır. Mahsup hesabı, günlüklerde tavsiye edilen bir varsayılan hesaptır. Sabit kıymet bir satıcından satınalınmışsa, günlükte hesap planından bir diğer hesaba veya bir satıcı hesabına değiştirilebilir. 

Borç hesaplarındaki fatura günlüğü veya Satınalma siparişleri sabit kıymet alımları için kullanılıyorsa, sabit kıymet hareketi için mahsup hesabı hareket için seçilen satıcı hesabı ile değiştirilir.

Genel muhasebedeki Stoktan sabit kıymetlere günlüğünü kullanarak nakledilmiş alımlar için, sabit kıymet harici kaynaklardan alınmaz ve şirketin kendi stokundan transfer edilir. Bu yüzden Stok yönetimindeki mahsup hesap, Stok yönetimindeki stok maddesi için bir stok çıkış hesabıdır.

Daha fazla bilgi için bkz: [Satınalma aracılığıyla kıymet alma](acquire-assets-procurement.md).


