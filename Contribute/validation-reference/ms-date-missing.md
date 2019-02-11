---
title: ms-date-missing
description: Belgeler derleme sorunu ms-date-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713258"
---
# <a name="ms-date-missing"></a><span data-ttu-id="ea17b-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="ea17b-103">ms-date-missing</span></span>

<span data-ttu-id="ea17b-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="ea17b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ea17b-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="ea17b-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="ea17b-106">Bu tarih "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ea17b-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="ea17b-107">Bu tarih makalenin *yayımlandığı* son tarih ile aynı değildir. Son yayımlama tarihi `ms.date` açıkça belirtilmezse sayfada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ea17b-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="ea17b-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="ea17b-108">Resolution</span></span>

<span data-ttu-id="ea17b-109">Makalenin bozuk bir içerik olmaksızın güncel olduğunu onaylayın, ardından AA/GG/YYYY biçiminde geçerli bir tarih ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ea17b-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
