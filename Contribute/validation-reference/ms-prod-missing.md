---
title: ms-prod-missing
description: Belgeler derleme sorunu ms-prod-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636782"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Şirket içi ürünler belirtmek için `ms.prod` kullanın. `ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz, ancak `ms.technology` belirtirseniz aynı zamanda `ms.prod` belirtmeniz gerekir. `ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır.

## <a name="resolution"></a>Çözüm

Makaleniz için belirttiğiniz `ms.technology` değerinin doğru olduğunu onaylayın. Sonra `ms.technology` için geçerli bir üst değer olan uygun `ms.prod` değerini ekleyin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
