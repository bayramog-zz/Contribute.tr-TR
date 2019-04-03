---
title: ms-prod-service-mismatch
description: Belgeler derleme sorunu ms-prod-service-mismatch için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636805"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Şirket içi ürünleri belirtmek için `ms.prod`, bulut hizmetleri için `ms.service` kullanın. `ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz. `ms.service` hakkında daha ayrıntılı bilgi belirtmek için `ms.subservice` belirtebilirsiniz. `ms.prod` seçeneğini `ms.subservice` veya `ms.service` seçeneğini `ms.technology` ile birlikte kullanamazsınız.

## <a name="resolution"></a>Çözüm

İlk olarak makaleniz için doğru üst özniteliği (`ms.prod` veya `ms.service`) seçtiğinizi doğrulayın. Ardından, geçerli bir eşleştirilmiş değeri olan uygun alt alanı ekleyin. Fazla alanları kaldırın.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
