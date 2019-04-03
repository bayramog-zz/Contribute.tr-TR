---
title: multiple-values
description: Docs derleme sorunu multiple-values için açıklama ve çözme
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: f8c2825801392e8ff1114e6abd08518a59ee8087
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637343"
---
# <a name="multiple-values"></a><span data-ttu-id="e2742-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="e2742-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e2742-104">Öneri</span><span class="sxs-lookup"><span data-stu-id="e2742-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="e2742-105">Yalnızca bir değer içermesine izin verilen bir öznitelik için birden fazla değer belirttiniz.</span><span class="sxs-lookup"><span data-stu-id="e2742-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="e2742-106">Birden fazla değer içermesine izin verilmeyen özniteliklerin tek değerli (skaler) YML biçiminde belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2742-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="e2742-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="e2742-107">Resolution</span></span>

<span data-ttu-id="e2742-108">Tek değerli bir öznitelik için çok değerli bir dizi kullanıldığında (dizide birden çok değer veya tek bir değer olması fark etmeksizin) bu Öneriyi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="e2742-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="e2742-109">YML, çok değerli öznitelikler için `ms.custom` gibi aşağıdaki dizi biçimlerini destekler:</span><span class="sxs-lookup"><span data-stu-id="e2742-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="e2742-110">Bu biçimler, `author` gibi tek değerli öznitelikler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="e2742-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="e2742-111">Birden fazla değer belirttiyseniz değerleri inceleyip doğru olanı belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e2742-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="e2742-112">Diğer değerleri kaldırın ve tek değeri, şu şekilde öznitelikle aynı satırda köşeli ayraç kullanmadan belirtin:</span><span class="sxs-lookup"><span data-stu-id="e2742-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="e2742-113">Tek değerli bir diziniz varsa bunu yukarıdaki skaler biçimle değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e2742-113">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
