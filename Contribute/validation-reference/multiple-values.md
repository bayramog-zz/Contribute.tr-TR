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
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

Yalnızca bir değer içermesine izin verilen bir öznitelik için birden fazla değer belirttiniz.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Birden fazla değer içermesine izin verilmeyen özniteliklerin tek değerli (skaler) YML biçiminde belirtilmesi gerekir.

## <a name="resolution"></a>Çözüm

Tek değerli bir öznitelik için çok değerli bir dizi kullanıldığında (dizide birden çok değer veya tek bir değer olması fark etmeksizin) bu Öneriyi alırsınız.

YML, çok değerli öznitelikler için `ms.custom` gibi aşağıdaki dizi biçimlerini destekler:

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

Bu biçimler, `author` gibi tek değerli öznitelikler için geçerli değildir.

Birden fazla değer belirttiyseniz değerleri inceleyip doğru olanı belirleyin. Diğer değerleri kaldırın ve tek değeri, şu şekilde öznitelikle aynı satırda köşeli ayraç kullanmadan belirtin:

```yml
---
author: meganbradley
---
```

Tek değerli bir diziniz varsa bunu yukarıdaki skaler biçimle değiştirin.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
