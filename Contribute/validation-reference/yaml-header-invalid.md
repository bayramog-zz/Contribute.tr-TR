---
title: yaml-header-invalid
description: Docs derleme sorunu yaml-header-invalid için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459039"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>Uyarı

`Invalid YAML header: Improper use of a colon in a metadata entry.`

Bu genellikle YAML üst bilgisindeki tırnak içine alınmamış meta veri değerinin iki nokta üst üste veya başka bir özel karakter içerdiği anlamına gelir. Ayrıca anahtar/değer çiftindeki iki nokta üst üste karakterinden önceki boşluğun eksik olduğu anlamına da gelebilir.

## <a name="resolution"></a>Çözüm

YAML üst bilginizi gözden geçirin. Aşağıdaki hataları arayın.

Tırnak içine alınmamış değerde iki nokta üst üste:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Şununla değiştirin:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

Anahtar/değer çiftinde iki nokta üst üste karakterinden sonra boşluk yok:

```yml
---
title:I omitted a space.
---
```

Şununla değiştirin:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
