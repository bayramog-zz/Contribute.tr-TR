---
title: h1-empty
description: Belgeler derleme sorunu h1-empty için açıklama ve çözüm.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428168"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>Uyarı

`H1 is required. Add content to your top-level heading.`

H1 bir Markdown dosyasındaki ilk başlığı gösterir. H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir. H1, bir satıra tek bir çatal altı işareti (#), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur.

## <a name="resolution"></a>Çözüm

Bu sorunu düzeltmek için H1'inizde yalnızca çatal artı işareti değil içerik de bulunduğundan emin olun.

Kötü:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

İyi:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]