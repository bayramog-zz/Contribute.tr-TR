---
title: ms-prod-missing
description: Belgeler derleme sorunu ms-prod-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713235"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="65590-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="65590-103">ms-prod-missing</span></span>

<span data-ttu-id="65590-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="65590-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="65590-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="65590-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="65590-106">Şirket içi ürünler belirtmek için `ms.prod` kullanın.</span><span class="sxs-lookup"><span data-stu-id="65590-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="65590-107">`ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz, ancak `ms.technology` belirtirseniz aynı zamanda `ms.prod` belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="65590-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="65590-108">`ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65590-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="65590-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="65590-109">Resolution</span></span>

<span data-ttu-id="65590-110">Makaleniz için belirttiğiniz `ms.technology` değerinin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="65590-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="65590-111">Sonra `ms.technology` için geçerli bir üst değer olan uygun `ms.prod` değerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="65590-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="65590-112">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/whitelists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="65590-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
