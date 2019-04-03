---
title: ms-prod-service-mismatch
description: Belgeler derleme sorunu ms-prod-service-mismatch için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636805"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="b611e-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="b611e-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b611e-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="b611e-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="b611e-105">Şirket içi ürünleri belirtmek için `ms.prod`, bulut hizmetleri için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="b611e-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="b611e-106">`ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b611e-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="b611e-107">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için `ms.subservice` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b611e-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="b611e-108">`ms.prod` seçeneğini `ms.subservice` veya `ms.service` seçeneğini `ms.technology` ile birlikte kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b611e-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="b611e-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="b611e-109">Resolution</span></span>

<span data-ttu-id="b611e-110">İlk olarak makaleniz için doğru üst özniteliği (`ms.prod` veya `ms.service`) seçtiğinizi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b611e-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="b611e-111">Ardından, geçerli bir eşleştirilmiş değeri olan uygun alt alanı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b611e-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="b611e-112">Fazla alanları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b611e-112">Remove any extra fields.</span></span>

<span data-ttu-id="b611e-113">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="b611e-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
