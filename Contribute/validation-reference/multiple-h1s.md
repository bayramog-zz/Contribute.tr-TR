---
title: multiple-h1
description: Docs derleme sorunu multiple-h1 için açıklama ve çözme.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428211"
---
# <a name="multiple-h1"></a>multiple-h1

## <a name="warning"></a>Uyarı

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 bir Markdown dosyasındaki ilk başlığı gösterir. H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir. H1, bir satıra tek bir çatal altı işareti (#), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur. Her dosyada tek bir H1 kullanabilirsiniz.

## <a name="resolution"></a>Çözüm

Bu sorunu çözmek için, izleyen H1'lerin başlık düzeyini H2 (`##`) olarak değiştirin veya dosyayı başka bir şekilde yeniden düzenleyin. Başlık düzeylerini atlamaya, örneğin H1'den sonra H3 kullanmaya izin verilmediğini unutmayın.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]