---
title: ms-service-and-subservice-invalid
description: Belgeler derleme sorunu ms-service-and-subservice-invalid için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637311"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="735f6-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="735f6-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="735f6-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="735f6-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="735f6-105">Bulut hizmetlerini belirtmek için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="735f6-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="735f6-106">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="735f6-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="735f6-107">`ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="735f6-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="735f6-108">`ms.service` değeriniz geçersiz veya `ms.subservice` değeriniz `ms.service` ile geçerli bir çift değil.</span><span class="sxs-lookup"><span data-stu-id="735f6-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="735f6-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="735f6-109">Resolution</span></span>

<span data-ttu-id="735f6-110">Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="735f6-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="735f6-111">Sonra geçerli bir `ms.subservice` değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="735f6-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="735f6-112">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="735f6-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
