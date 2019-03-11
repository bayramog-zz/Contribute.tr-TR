---
title: h1-missing
description: Docs derleme sorunu h1-missing için açıklama ve çözüm.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459131"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>Uyarı

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 bir Markdown dosyasındaki ilk başlığı gösterir. H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir. H1, bir satıra tek bir çatal altı işareti (#), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur.

## <a name="resolution"></a>Çözüm

Bu sorunu düzeltmek için dosyanıza YML meta veri bloğundan sonra ilk içerik olarak bir H1 ekleyin:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Bu kural ekli dosyalara uygulanmaz. Ekli dosyalarda H1 uyarıları alırsanız, büyük olasılıkla ekli dosyalarınızı bir `includes` klasörüne taşımanız gerekir. `includes` klasörü dosya yolunda herhangi bir düzeyde olabilir. Yola bağlı olarak, Docs derlemesi dosyayı ekli dosya olarak tanır ve H1 doğrulamaları çalıştırılmaz.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]