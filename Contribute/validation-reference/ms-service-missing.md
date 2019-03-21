---
title: ms-service-missing
description: Belgeler derleme sorunu ms-service-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987733"
---
# <a name="ms-service-missing"></a><span data-ttu-id="c6282-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="c6282-103">ms-service-missing</span></span>

<span data-ttu-id="c6282-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="c6282-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c6282-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="c6282-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="c6282-106">Bulut hizmetlerini belirtmek için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6282-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="c6282-107">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz, ancak `ms.subservice` belirtirseniz aynı zamanda `ms.service` belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6282-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="c6282-108">`ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c6282-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="c6282-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="c6282-109">Resolution</span></span>

<span data-ttu-id="c6282-110">Makaleniz için belirttiğiniz `ms.subservice` değerinin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c6282-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="c6282-111">Sonra `ms.subservice` için geçerli bir üst değer olan uygun `ms.service` değerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c6282-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="c6282-112">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="c6282-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
