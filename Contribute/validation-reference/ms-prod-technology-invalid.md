---
title: ms-prod-and-technology-invalid
description: Belgeler derleme sorunu ms-prod-and-technology için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987595"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="df202-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="df202-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="df202-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="df202-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="df202-105">Uyarı</span><span class="sxs-lookup"><span data-stu-id="df202-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="df202-106">Şirket içi ürünler belirtmek için `ms.prod` kullanın.</span><span class="sxs-lookup"><span data-stu-id="df202-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="df202-107">`ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="df202-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="df202-108">`ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="df202-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="df202-109">`ms.prod` değeriniz geçersiz veya `ms.technology` değeriniz `ms.prod` ile geçerli bir çift değil.</span><span class="sxs-lookup"><span data-stu-id="df202-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="df202-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="df202-110">Resolution</span></span>

<span data-ttu-id="df202-111">Makaleniz için `ms.prod` değerinizin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="df202-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="df202-112">Sonra geçerli bir `ms.technology` değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="df202-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="df202-113">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="df202-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
