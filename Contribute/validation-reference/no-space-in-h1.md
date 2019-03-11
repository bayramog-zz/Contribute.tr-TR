---
title: no-space-in-h1
description: Belgeler derleme sorunu no-space-in-h1 için açıklama ve çözüm.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428200"
---
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>Uyarı

`A space is required after the hash (#) in H1.`

H1 bir Markdown dosyasındaki ilk başlığı gösterir. H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir. H1, bir satıra tek bir çatal altı işareti (#), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur. Çatal artı işaretinden sonra boşluk olmazsa, Docs H1'i tanımaz.

## <a name="resolution"></a>Çözüm

Bu hatayı düzeltmek için H1'inizde çatal artı işaretinden sonra bir boşluk ekleyin.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]