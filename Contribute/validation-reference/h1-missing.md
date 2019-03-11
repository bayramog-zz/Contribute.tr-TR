---
title: h1-missing
description: Docs derleme sorunu h1-missing için açıklama ve çözüm.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459131"
---
# <a name="h1-missing"></a><span data-ttu-id="6f182-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="6f182-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="6f182-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="6f182-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="6f182-105">H1 bir Markdown dosyasındaki ilk başlığı gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f182-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="6f182-106">H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir.</span><span class="sxs-lookup"><span data-stu-id="6f182-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="6f182-107">H1, bir satıra tek bir çatal altı işareti (#), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6f182-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="6f182-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="6f182-108">Resolution</span></span>

<span data-ttu-id="6f182-109">Bu sorunu düzeltmek için dosyanıza YML meta veri bloğundan sonra ilk içerik olarak bir H1 ekleyin:</span><span class="sxs-lookup"><span data-stu-id="6f182-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="6f182-110">Bu kural ekli dosyalara uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="6f182-110">This rule does not apply to included files.</span></span> <span data-ttu-id="6f182-111">Ekli dosyalarda H1 uyarıları alırsanız, büyük olasılıkla ekli dosyalarınızı bir `includes` klasörüne taşımanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f182-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="6f182-112">`includes` klasörü dosya yolunda herhangi bir düzeyde olabilir.</span><span class="sxs-lookup"><span data-stu-id="6f182-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="6f182-113">Yola bağlı olarak, Docs derlemesi dosyayı ekli dosya olarak tanır ve H1 doğrulamaları çalıştırılmaz.</span><span class="sxs-lookup"><span data-stu-id="6f182-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]