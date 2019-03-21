---
title: ms-service-and-subservice-invalid
description: Belgeler derleme sorunu ms-service-and-subservice-invalid için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987655"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="2a189-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="2a189-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="2a189-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="2a189-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="2a189-105">Uyarı</span><span class="sxs-lookup"><span data-stu-id="2a189-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="2a189-106">Bulut hizmetlerini belirtmek için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a189-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="2a189-107">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a189-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="2a189-108">`ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a189-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="2a189-109">`ms.service` değeriniz geçersiz veya `ms.subservice` değeriniz `ms.service` ile geçerli bir çift değil.</span><span class="sxs-lookup"><span data-stu-id="2a189-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="2a189-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="2a189-110">Resolution</span></span>

<span data-ttu-id="2a189-111">Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2a189-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="2a189-112">Sonra geçerli bir `ms.subservice` değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="2a189-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="2a189-113">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="2a189-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
