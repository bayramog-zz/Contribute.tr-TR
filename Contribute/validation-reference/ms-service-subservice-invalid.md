---
title: ms-service-and-subservice-invalid
description: Belgeler derleme sorunu ms-service-and-subservice-invalid için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713143"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="5b2d9-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="5b2d9-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="5b2d9-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="5b2d9-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="5b2d9-105">Uyarı</span><span class="sxs-lookup"><span data-stu-id="5b2d9-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="5b2d9-106">Bulut hizmetlerini belirtmek için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="5b2d9-107">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="5b2d9-108">`ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="5b2d9-109">`ms.service` değeriniz geçersiz veya `ms.subservice` değeriniz `ms.service` ile geçerli bir çift değil.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="5b2d9-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="5b2d9-110">Resolution</span></span>

<span data-ttu-id="5b2d9-111">Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="5b2d9-112">Sonra geçerli bir `ms.subservice` değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="5b2d9-113">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/whitelists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
