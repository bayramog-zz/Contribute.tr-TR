---
title: ms-prod-service-mismatch
description: Belgeler derleme sorunu ms-prod-service-mismatch için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713189"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="61be9-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="61be9-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="61be9-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="61be9-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="61be9-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="61be9-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="61be9-106">Şirket içi ürünleri belirtmek için `ms.prod`, bulut hizmetleri için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="61be9-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="61be9-107">`ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61be9-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="61be9-108">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için `ms.subservice` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61be9-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="61be9-109">`ms.prod` seçeneğini `ms.subservice` veya `ms.service` seçeneğini `ms.technology` ile birlikte kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="61be9-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="61be9-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="61be9-110">Resolution</span></span>

<span data-ttu-id="61be9-111">İlk olarak makaleniz için doğru üst özniteliği (`ms.prod` veya `ms.service`) seçtiğinizi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="61be9-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="61be9-112">Ardından, geçerli bir eşleştirilmiş değeri olan uygun alt alanı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="61be9-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="61be9-113">Fazla alanları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="61be9-113">Remove any extra fields.</span></span>

<span data-ttu-id="61be9-114">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/whitelists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="61be9-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
