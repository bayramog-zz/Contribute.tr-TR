---
title: ms-service-and-subservice-invalid
description: Belgeler derleme sorunu ms-service-and-subservice-invalid için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987655"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

**Çok yakında!**

## <a name="warning"></a>Uyarı

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Bulut hizmetlerini belirtmek için `ms.service` kullanın. `ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz. `ms.service` ve `ms.subservice` değerleri geçerli bir çift olmalıdır. `ms.service` değeriniz geçersiz veya `ms.subservice` değeriniz `ms.service` ile geçerli bir çift değil.

## <a name="resolution"></a>Çözüm

Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın. Sonra geçerli bir `ms.subservice` değeri seçin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
