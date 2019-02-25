---
title: multiple-values
description: Docs derleme sorunu multiple-values için açıklama ve çözme
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8cee25b07e5bd1e019f8d270888eff73292d8e7c
ms.sourcegitcommit: ae71ca811c143deb6214147c7eea8704444a6093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56465128"
---
# <a name="multiple-values"></a><span data-ttu-id="0b108-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="0b108-103">multiple-values</span></span>

<span data-ttu-id="0b108-104">**Çok yakında!**</span><span class="sxs-lookup"><span data-stu-id="0b108-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0b108-105">Öneri</span><span class="sxs-lookup"><span data-stu-id="0b108-105">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="0b108-106">Yalnızca bir değer içermesine izin verilen bir öznitelik için birden fazla değer belirttiniz.</span><span class="sxs-lookup"><span data-stu-id="0b108-106">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="0b108-107">Birden fazla değer içermesine izin verilmeyen özniteliklerin tek değerli (skaler) YML biçiminde belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b108-107">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="0b108-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="0b108-108">Resolution</span></span>

<span data-ttu-id="0b108-109">Tek değerli bir öznitelik için çok değerli bir dizi kullanıldığında (dizide birden çok değer veya tek bir değer olması fark etmeksizin) bu Öneriyi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="0b108-109">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="0b108-110">YML, çok değerli öznitelikler için `ms.custom` gibi aşağıdaki dizi biçimlerini destekler:</span><span class="sxs-lookup"><span data-stu-id="0b108-110">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

<span data-ttu-id="0b108-111">Bu biçimler, `author` gibi tek değerli öznitelikler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="0b108-111">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="0b108-112">Birden fazla değer belirttiyseniz değerleri inceleyip doğru olanı belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0b108-112">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="0b108-113">Diğer değerleri kaldırın ve tek değeri, şu şekilde öznitelikle aynı satırda köşeli ayraç kullanmadan belirtin:</span><span class="sxs-lookup"><span data-stu-id="0b108-113">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="0b108-114">Tek değerli bir diziniz varsa bunu yukarıdaki skaler biçimle değiştirin.</span><span class="sxs-lookup"><span data-stu-id="0b108-114">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
