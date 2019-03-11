---
title: manager-missing
description: Belgeler derleme sorunu manager-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428196"
---
# <a name="manager-missing"></a><span data-ttu-id="4d4de-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="4d4de-103">manager-missing</span></span>

<span data-ttu-id="4d4de-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="4d4de-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4d4de-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="4d4de-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="4d4de-106">Bazı içerik grupları `manager` özniteliğinde yazarın yöneticisinin tanımlanmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4d4de-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="4d4de-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="4d4de-107">Resolution</span></span>

<span data-ttu-id="4d4de-108">`manager` için geçerli bir Microsoft diğer adı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="4d4de-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
