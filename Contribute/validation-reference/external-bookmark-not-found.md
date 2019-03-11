---
title: external-bookmark-not-found
description: Docs derleme sorunu external-bookmark-not-found için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428187"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>Uyarı

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

Başka bir dosyada varolmayan bir başlığa bağlanmaya çalışıyorsunuz.

## <a name="resolution"></a>Çözüm

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Bağlandığınız dosyayı gözden geçirin ve yer işareti bağlantınızı dosyanın geçerli bölümüne işaret edecek şekilde güncelleştirin.

Başka bir makalenin bölüm başlığına bağlanmak için, göreli dosya veya göreli site bağlantısını, yanında çatal artı işareti sembolünü ve ardından da başlığın sözcüklerini kullanın. Başlıktan noktalama işaretlerini kaldırın ve boşlukları çizgilerle değiştirin. Aşağıda bir örnek verilmiştir:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
