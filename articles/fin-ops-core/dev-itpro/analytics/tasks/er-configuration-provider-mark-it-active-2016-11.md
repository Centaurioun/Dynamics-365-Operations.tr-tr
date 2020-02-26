---
title: Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme
description: Bu konu Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2c092414f058a27cde963b1e8befd41ab3d1e3c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249216"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konu Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar. Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır. Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.

## <a name="create-a-provider"></a>Sağlayıcı oluşturun
1. Sol üst köşedeki **gezinti bölmesi**'ne gidin ve **Kuruluş yönetimi**'ni seçin.
2. Sırasıyla **Çalışma alanları > Elektronik raporlama**'ya gidin.
3. **İlgili bağlantılar > Yapılandırma sağlayıcılar**'a gidin.
4. **Yeni**'yi seçin.
    - Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir. Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (https://www.litware.com) için bir kayıt zaten varsa bu yordamı atlayın.  
5. İsim alanına `Litware, Inc.`. yazın.
6. İnternet adresi alanına "`https://www.litware.com`" yazın.
7. **Kaydet**'i seçin.
8. Sayfayı kapatın.

## <a name="select-as-an-active-provider"></a>Etkin bir sağlayıcı olarak seçin
1. Litware, Inc. sağlayıcısını seçin.
2. **Etkin olarak ayarla**'ya tıklayın.

![Elektronik raporlama çalışma alanı sayfası](../media/GER-Task-ActiveProvider-1.png)