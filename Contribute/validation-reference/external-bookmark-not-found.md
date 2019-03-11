---
title: external-bookmark-not-found
description: Docs derleme sorunu external-bookmark-not-found için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428187"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="c8638-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="c8638-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="c8638-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="c8638-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="c8638-105">Başka bir dosyada varolmayan bir başlığa bağlanmaya çalışıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="c8638-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="c8638-106">Çözüm</span><span class="sxs-lookup"><span data-stu-id="c8638-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="c8638-107">Bağlandığınız dosyayı gözden geçirin ve yer işareti bağlantınızı dosyanın geçerli bölümüne işaret edecek şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c8638-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="c8638-108">Başka bir makalenin bölüm başlığına bağlanmak için, göreli dosya veya göreli site bağlantısını, yanında çatal artı işareti sembolünü ve ardından da başlığın sözcüklerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8638-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="c8638-109">Başlıktan noktalama işaretlerini kaldırın ve boşlukları çizgilerle değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c8638-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c8638-110">Aşağıda bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c8638-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
