---
title: deprecated-attribute
description: Docs derleme sorunu deprecated-attribute için açıklama ve çözünürlük
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987802"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="b8caf-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="b8caf-103">deprecated-attribute</span></span>

<span data-ttu-id="b8caf-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="b8caf-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b8caf-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="b8caf-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="b8caf-106">Bulut hizmetlerini belirtmek için `ms.service` kullanın.</span><span class="sxs-lookup"><span data-stu-id="b8caf-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="b8caf-107">`ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8caf-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="b8caf-108">`ms.component` kullanmayın; bu içerik için kullanım dışıdır.</span><span class="sxs-lookup"><span data-stu-id="b8caf-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="b8caf-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="b8caf-109">Resolution</span></span>

<span data-ttu-id="b8caf-110">Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="b8caf-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="b8caf-111">Sonra geçerli bir `ms.subservice` değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="b8caf-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="b8caf-112">Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="b8caf-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
