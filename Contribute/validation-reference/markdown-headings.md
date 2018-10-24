---
title: Markdown Başlıkları
description: Markdown başlıklarının gereksinimlerini açıklar.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084567"
---
# <a name="markdown-headings"></a><span data-ttu-id="59f79-103">Markdown başlıkları</span><span class="sxs-lookup"><span data-stu-id="59f79-103">Markdown headings</span></span>

<span data-ttu-id="59f79-104">Aşağıdaki doğrulama gereksinimleri, OPS Markdown dosyalarındaki başlıklar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="59f79-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="59f79-105">H1</span><span class="sxs-lookup"><span data-stu-id="59f79-105">H1</span></span>

<span data-ttu-id="59f79-106">`H1` bir Markdown dosyasındaki ilk başlığı gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f79-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="59f79-107">H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir.</span><span class="sxs-lookup"><span data-stu-id="59f79-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="59f79-108">H1, bir satıra tek bir çatal altı işareti (`#`), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="59f79-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="59f79-109">Örneğin bu makalenin H1 başlığı şöyledir:</span><span class="sxs-lookup"><span data-stu-id="59f79-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="59f79-110">H1 başlıkları için aşağıdaki kurallar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="59f79-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="59f79-111">Bir dosyada bir H1 bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f79-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="59f79-112">Yalnızca bir tane H1 bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="59f79-112">There can only be one H1.</span></span>
- <span data-ttu-id="59f79-113">H1'in içeriği olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f79-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="59f79-114">`#` ile H1 içeriği arasında bir boşluk olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f79-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="59f79-115">Boşluğu olmayan bir H1 yayımlanan bir sayfada bir başlık olarak ekrana çizilmez.</span><span class="sxs-lookup"><span data-stu-id="59f79-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="59f79-116">H1, dosyada YML meta veri başlığından sonraki ilk içerik olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f79-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="59f79-117">YML başlığı ile H1 arasına metin veya görüntü gibi hiçbir içerik konamaz.</span><span class="sxs-lookup"><span data-stu-id="59f79-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="59f79-118">İlk düzey başlıkların HTML öğesi olan `<h1>` kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f79-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="59f79-119">Markdown sözdizimini (`# `) kullanın.</span><span class="sxs-lookup"><span data-stu-id="59f79-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="59f79-120">H1 en çok 100 karakter uzunlukta olabilir.</span><span class="sxs-lookup"><span data-stu-id="59f79-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="59f79-121">Bu bir stil yönergesidir.</span><span class="sxs-lookup"><span data-stu-id="59f79-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="59f79-122">H2 - H6</span><span class="sxs-lookup"><span data-stu-id="59f79-122">H2 - H6</span></span>

<span data-ttu-id="59f79-123">H2 (`## `) ile H6 (`###### `) arasındaki başlıklar OPS'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="59f79-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="59f79-124">Başlık oluşturmak için HTML (`<h2>` - `<h6>`) değil Markdown başlıklarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="59f79-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
