---
title: ms-date-too-late
description: Belgeler derleme sorunu ms-date-too-late için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713120"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="2ba2e-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="2ba2e-103">ms-date-too-late</span></span>

<span data-ttu-id="2ba2e-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="2ba2e-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="2ba2e-105">Uyarı</span><span class="sxs-lookup"><span data-stu-id="2ba2e-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="2ba2e-106">`ms.date` özniteliği "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ba2e-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="2ba2e-107">Bu yüzden gelecekteki bir tarih olamaz!</span><span class="sxs-lookup"><span data-stu-id="2ba2e-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="2ba2e-108">İçeriğin önemli bir olaya hazırlanırken kalite denetimi için kilitlenmesi gibi durumlarda serbest bırakma süresi için beş gün izin verilir.</span><span class="sxs-lookup"><span data-stu-id="2ba2e-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="2ba2e-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="2ba2e-109">Resolution</span></span>

<span data-ttu-id="2ba2e-110">Bugünden başlayarak AA/GG/YYYY biçiminde en fazla beş günlük `ms.date` belirtin.</span><span class="sxs-lookup"><span data-stu-id="2ba2e-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
