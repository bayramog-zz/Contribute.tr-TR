---
title: ms-prod-or-service-missing
description: Belgeler derleme sorunu ms-prod-or-service-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8d8d01f95af74009cfa9cb1a57531663df4edf4d
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637380"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="c7484-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="c7484-103">ms-prod-or-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c7484-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="c7484-104">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="c7484-105">Çözüm</span><span class="sxs-lookup"><span data-stu-id="c7484-105">Resolution</span></span>

<span data-ttu-id="c7484-106">`ms.prod` veya `ms.service` gereklidir ve her ikisi de mevcut olamaz: `ms.prod` şirket içi ürünler için kullanılır, `ms.service` ise bulut hizmetleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7484-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="c7484-107">Makaleniz için hangisinin uygun olduğunu belirleyin, değerin doğru olduğunu onaylayın ve diğer alanı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="c7484-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="c7484-108">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="c7484-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]