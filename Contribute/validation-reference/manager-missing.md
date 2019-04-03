---
title: manager-missing
description: Belgeler derleme sorunu manager-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637265"
---
# <a name="manager-missing"></a><span data-ttu-id="ca508-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="ca508-103">manager-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ca508-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="ca508-104">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="ca508-105">Bazı içerik grupları `manager` özniteliğinde yazarın yöneticisinin tanımlanmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="ca508-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="ca508-106">Çözüm</span><span class="sxs-lookup"><span data-stu-id="ca508-106">Resolution</span></span>

<span data-ttu-id="ca508-107">`manager` için geçerli bir Microsoft diğer adı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="ca508-107">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
