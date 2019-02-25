---
title: ms-date-too-late
description: Belgeler derleme sorunu ms-date-too-late için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431496"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="566c1-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="566c1-103">ms-date-too-late</span></span>

<span data-ttu-id="566c1-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="566c1-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="566c1-105">Uyarı</span><span class="sxs-lookup"><span data-stu-id="566c1-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="566c1-106">`ms.date` özniteliği "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="566c1-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="566c1-107">Bu yüzden gelecekteki bir tarih olamaz!</span><span class="sxs-lookup"><span data-stu-id="566c1-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="566c1-108">İçeriğin önemli bir olaya hazırlanırken kalite denetimi için kilitlenmesi gibi durumlarda serbest bırakma süresi için beş gün izin verilir.</span><span class="sxs-lookup"><span data-stu-id="566c1-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="566c1-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="566c1-109">Resolution</span></span>

<span data-ttu-id="566c1-110">Bugünden başlayarak AA/GG/YYYY biçiminde en fazla beş günlük `ms.date` belirtin:</span><span class="sxs-lookup"><span data-stu-id="566c1-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
