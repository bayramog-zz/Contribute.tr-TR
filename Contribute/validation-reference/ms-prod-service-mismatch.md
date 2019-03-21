---
title: ms-prod-service-mismatch
description: Belgeler derleme sorunu ms-prod-service-mismatch için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987627"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**Çok yakında!**

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
