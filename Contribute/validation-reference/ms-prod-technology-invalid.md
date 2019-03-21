---
title: ms-prod-and-technology-invalid
description: Belgeler derleme sorunu ms-prod-and-technology için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987595"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**Çok yakında!**

## <a name="warning"></a>Uyarı

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Şirket içi ürünler belirtmek için `ms.prod` kullanın. `ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz. `ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır. `ms.prod` değeriniz geçersiz veya `ms.technology` değeriniz `ms.prod` ile geçerli bir çift değil.

## <a name="resolution"></a>Çözüm

Makaleniz için `ms.prod` değerinizin doğru olduğunu onaylayın. Sonra geçerli bir `ms.technology` değeri seçin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
