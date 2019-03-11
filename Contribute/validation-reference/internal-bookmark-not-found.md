---
title: internal-bookmark-not-found
description: Docs derleme sorunu internal-bookmark-not-found için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428199"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Current file doesn't contain a bookmark named '{bookmark}'.`

Geçerli dosyada varolmayan bir başlığa bağlanmaya çalışıyorsunuz.

## <a name="resolution"></a>Çözüm

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Bağlanmak istediğiniz başlığı doğrulayın ve bağlantıyı güncelleştirin.

Geçerli makalenin bir bölümüne bağlanmak için, çatal artı işareti sembolünü ve ardından başlığın sözcüklerini kullanın. Başlıktan noktalama işaretlerini kaldırın ve boşlukları çizgilerle değiştirin. Aşağıda bir örnek verilmiştir:

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
