---
title: ms-prod-missing
description: Belgeler derleme sorunu ms-prod-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987710"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Şirket içi ürünler belirtmek için `ms.prod` kullanın. `ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz, ancak `ms.technology` belirtirseniz aynı zamanda `ms.prod` belirtmeniz gerekir. `ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır.

## <a name="resolution"></a>Çözüm

Makaleniz için belirttiğiniz `ms.technology` değerinin doğru olduğunu onaylayın. Sonra `ms.technology` için geçerli bir üst değer olan uygun `ms.prod` değerini ekleyin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
