---
title: ms-service-and-subservice-invalid
description: Belgeler derleme sorunu ms-service-and-subservice-invalid için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637311"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Bulut hizmetlerini belirtmek için `ms.service` kullanın. `ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz. `ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır. `ms.service` değeriniz geçersiz veya `ms.subservice` değeriniz `ms.service` ile geçerli bir çift değil.

## <a name="resolution"></a>Çözüm

Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın. Sonra geçerli bir `ms.subservice` değeri seçin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
