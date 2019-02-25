---
title: ms-date-missing
description: Belgeler derleme sorunu ms-date-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431473"
---
# <a name="ms-date-missing"></a><span data-ttu-id="795ff-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="795ff-103">ms-date-missing</span></span>

<span data-ttu-id="795ff-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="795ff-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="795ff-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="795ff-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="795ff-106">Bu tarih "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="795ff-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="795ff-107">Bu tarih makalenin *yayımlandığı* son tarih ile aynı değildir. Son yayımlama tarihi `ms.date` açıkça belirtilmezse sayfada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="795ff-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="795ff-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="795ff-108">Resolution</span></span>

<span data-ttu-id="795ff-109">Makalenin bozuk bir içerik olmaksızın güncel olduğunu onaylayın, ardından AA/GG/YYYY biçiminde geçerli bir tarih ekleyin:</span><span class="sxs-lookup"><span data-stu-id="795ff-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
