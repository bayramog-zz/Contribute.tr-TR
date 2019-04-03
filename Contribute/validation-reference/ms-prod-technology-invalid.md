---
title: ms-prod-and-technology-invalid
description: Belgeler derleme sorunu ms-prod-and-technology için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8c6f12629cf4b8cf7fd2471ef4d1287562435696
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636851"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="0741e-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="0741e-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="0741e-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="0741e-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="0741e-105">Şirket içi ürünler belirtmek için `ms.prod` kullanın.</span><span class="sxs-lookup"><span data-stu-id="0741e-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="0741e-106">`ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0741e-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="0741e-107">`ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0741e-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="0741e-108">`ms.prod` değeriniz geçersiz veya `ms.technology` değeriniz `ms.prod` ile geçerli bir çift değil.</span><span class="sxs-lookup"><span data-stu-id="0741e-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="0741e-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="0741e-109">Resolution</span></span>

<span data-ttu-id="0741e-110">Makaleniz için `ms.prod` değerinizin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="0741e-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="0741e-111">Sonra geçerli bir `ms.technology` değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="0741e-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="0741e-112">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="0741e-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
