---
title: internal-bookmark-not-found
description: Docs derleme sorunu internal-bookmark-not-found için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428199"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="c40c8-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="c40c8-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="c40c8-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="c40c8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c40c8-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="c40c8-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="c40c8-106">Geçerli dosyada varolmayan bir başlığa bağlanmaya çalışıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="c40c8-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="c40c8-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="c40c8-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="c40c8-108">Bağlanmak istediğiniz başlığı doğrulayın ve bağlantıyı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c40c8-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="c40c8-109">Geçerli makalenin bir bölümüne bağlanmak için, çatal artı işareti sembolünü ve ardından başlığın sözcüklerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c40c8-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="c40c8-110">Başlıktan noktalama işaretlerini kaldırın ve boşlukları çizgilerle değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c40c8-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c40c8-111">Aşağıda bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c40c8-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
