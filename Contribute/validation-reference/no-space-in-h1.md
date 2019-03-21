---
title: no-space-in-h1
description: Belgeler derleme sorunu no-space-in-h1 için açıklama ve çözüm.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428200"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="5fc54-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="5fc54-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="5fc54-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="5fc54-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="5fc54-105">H1 bir Markdown dosyasındaki ilk başlığı gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fc54-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="5fc54-106">H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5fc54-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="5fc54-107">H1, bir satıra tek bir çatal altı işareti (#), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5fc54-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="5fc54-108">Çatal artı işaretinden sonra boşluk olmazsa, Docs H1'i tanımaz.</span><span class="sxs-lookup"><span data-stu-id="5fc54-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="5fc54-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="5fc54-109">Resolution</span></span>

<span data-ttu-id="5fc54-110">Bu hatayı düzeltmek için H1'inizde çatal artı işaretinden sonra bir boşluk ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5fc54-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]