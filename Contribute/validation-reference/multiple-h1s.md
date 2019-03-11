---
title: multiple-h1
description: Docs derleme sorunu multiple-h1 için açıklama ve çözme.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428211"
---
# <a name="multiple-h1"></a><span data-ttu-id="71a86-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="71a86-103">multiple-h1</span></span>

## <a name="warning"></a><span data-ttu-id="71a86-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="71a86-104">Warning</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="71a86-105">H1 bir Markdown dosyasındaki ilk başlığı gösterir.</span><span class="sxs-lookup"><span data-stu-id="71a86-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="71a86-106">H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir.</span><span class="sxs-lookup"><span data-stu-id="71a86-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="71a86-107">H1, bir satıra tek bir çatal altı işareti (#), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="71a86-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="71a86-108">Her dosyada tek bir H1 kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="71a86-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="71a86-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="71a86-109">Resolution</span></span>

<span data-ttu-id="71a86-110">Bu sorunu çözmek için, izleyen H1'lerin başlık düzeyini H2 (`##`) olarak değiştirin veya dosyayı başka bir şekilde yeniden düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="71a86-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="71a86-111">Başlık düzeylerini atlamaya, örneğin H1'den sonra H3 kullanmaya izin verilmediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="71a86-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]