---
title: ms-prod-and-service
description: Belgeler derleme sorunu ms-prod-and-service için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 77c0dd71cf526ee837799bcd01e21290ce7d6058
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636759"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="5e849-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="5e849-103">ms-prod-and-service</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5e849-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="5e849-104">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="5e849-105">Çözüm</span><span class="sxs-lookup"><span data-stu-id="5e849-105">Resolution</span></span>

<span data-ttu-id="5e849-106">`ms.prod` veya `ms.service` gereklidir ve her ikisi de mevcut olamaz: `ms.prod` şirket içi ürünler için kullanılır, `ms.service` ise bulut hizmetleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e849-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="5e849-107">Makaleniz için hangisinin uygun olduğunu belirleyin, değerin doğru olduğunu onaylayın ve diğer alanı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5e849-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="5e849-108">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="5e849-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
