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
# <a name="yaml-header-invalid"></a><span data-ttu-id="6ce7f-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="6ce7f-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="6ce7f-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="6ce7f-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="6ce7f-105">Bu genellikle YAML üst bilgisindeki tırnak içine alınmamış meta veri değerinin iki nokta üst üste veya başka bir özel karakter içerdiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6ce7f-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="6ce7f-106">Ayrıca anahtar/değer çiftindeki iki nokta üst üste karakterinden önceki boşluğun eksik olduğu anlamına da gelebilir.</span><span class="sxs-lookup"><span data-stu-id="6ce7f-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ce7f-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="6ce7f-107">Resolution</span></span>

<span data-ttu-id="6ce7f-108">YAML üst bilginizi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="6ce7f-108">Review your YAML header.</span></span> <span data-ttu-id="6ce7f-109">Aşağıdaki hataları arayın.</span><span class="sxs-lookup"><span data-stu-id="6ce7f-109">Look for the following mistakes.</span></span>

<span data-ttu-id="6ce7f-110">Tırnak içine alınmamış değerde iki nokta üst üste:</span><span class="sxs-lookup"><span data-stu-id="6ce7f-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="6ce7f-111">Şununla değiştirin:</span><span class="sxs-lookup"><span data-stu-id="6ce7f-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="6ce7f-112">Anahtar/değer çiftinde iki nokta üst üste karakterinden sonra boşluk yok:</span><span class="sxs-lookup"><span data-stu-id="6ce7f-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="6ce7f-113">Şununla değiştirin:</span><span class="sxs-lookup"><span data-stu-id="6ce7f-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
