---
title: ms-service-missing
description: Belgeler derleme sorunu ms-service-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713097"
---
# <a name="ms-service-missing"></a>ms-service-missing

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Bulut hizmetlerini belirtmek için `ms.service` kullanın. `ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz, ancak `ms.subservice` belirtirseniz aynı zamanda `ms.service` belirtmeniz gerekir. `ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır.

## <a name="resolution"></a>Çözüm

Makaleniz için belirttiğiniz `ms.subservice` değerinin doğru olduğunu onaylayın. Sonra `ms.subservice` için geçerli bir üst değer olan uygun `ms.service` değerini ekleyin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/whitelists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
