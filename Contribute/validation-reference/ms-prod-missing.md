---
title: ms-prod-missing
description: Belgeler derleme sorunu ms-prod-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636782"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="e2334-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="e2334-103">ms-prod-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e2334-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="e2334-104">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="e2334-105">Şirket içi ürünler belirtmek için `ms.prod` kullanın.</span><span class="sxs-lookup"><span data-stu-id="e2334-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="e2334-106">`ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz, ancak `ms.technology` belirtirseniz aynı zamanda `ms.prod` belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2334-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="e2334-107">`ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e2334-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="e2334-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="e2334-108">Resolution</span></span>

<span data-ttu-id="e2334-109">Makaleniz için belirttiğiniz `ms.technology` değerinin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e2334-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="e2334-110">Sonra `ms.technology` için geçerli bir üst değer olan uygun `ms.prod` değerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e2334-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="e2334-111">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="e2334-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
