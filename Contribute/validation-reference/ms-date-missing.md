---
title: ms-date-missing
description: Belgeler derleme sorunu ms-date-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637288"
---
# <a name="ms-date-missing"></a><span data-ttu-id="c567e-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="c567e-103">ms-date-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c567e-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="c567e-104">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="c567e-105">Bazı içerik grupları "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için `ms.date` gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c567e-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="c567e-106">Bu tarih makalenin *yayımlandığı* son tarih ile aynı değildir. Son yayımlama tarihi `ms.date` açıkça belirtilmezse sayfada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c567e-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="c567e-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="c567e-107">Resolution</span></span>

<span data-ttu-id="c567e-108">Makalenin bozuk bir içerik olmaksızın güncel olduğunu onaylayın, ardından AA/GG/YYYY biçiminde geçerli bir tarih ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c567e-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
