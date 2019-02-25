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
# <a name="multiple-values"></a>multiple-values

**Çok yakında!**

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
