---
title: ms-service-missing
description: Belgeler derleme sorunu ms-service-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713097"
---
# <a name="ms-service-missing"></a><span data-ttu-id="156e0-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="156e0-103">ms-service-missing</span></span>

<span data-ttu-id="156e0-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="156e0-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="156e0-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="156e0-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="156e0-106">Bulut hizmetlerini belirtmek için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="156e0-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="156e0-107">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz, ancak `ms.subservice` belirtirseniz aynı zamanda `ms.service` belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="156e0-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="156e0-108">`ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="156e0-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="156e0-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="156e0-109">Resolution</span></span>

<span data-ttu-id="156e0-110">Makaleniz için belirttiğiniz `ms.subservice` değerinin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="156e0-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="156e0-111">Sonra `ms.subservice` için geçerli bir üst değer olan uygun `ms.service` değerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="156e0-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="156e0-112">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/whitelists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="156e0-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
