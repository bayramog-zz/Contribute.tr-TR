---
title: deprecated-attribute
description: Docs derleme sorunu deprecated-attribute için açıklama ve çözünürlük
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636897"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="d51b4-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="d51b4-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d51b4-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="d51b4-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="d51b4-105">Bulut hizmetlerini belirtmek için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="d51b4-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="d51b4-106">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51b4-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="d51b4-107">`ms.component` kullanmayın; bu içerik için kullanım dışıdır.</span><span class="sxs-lookup"><span data-stu-id="d51b4-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="d51b4-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="d51b4-108">Resolution</span></span>

<span data-ttu-id="d51b4-109">Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="d51b4-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="d51b4-110">Sonra geçerli bir `ms.subservice` değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="d51b4-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="d51b4-111">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="d51b4-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
