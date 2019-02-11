---
title: ms-prod-and-technology-invalid
description: Belgeler derleme sorunu ms-prod-and-technology için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713281"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**Çok yakında!**

## <a name="warning"></a>Uyarı

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Şirket içi ürünler belirtmek için `ms.prod` kullanın. `ms.prod` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.technology` belirtebilirsiniz. `ms.prod` ve `ms.technology` değerleri geçerli bir çift olmalıdır. `ms.prod` değeriniz geçersiz veya `ms.technology` değeriniz `ms.prod` ile geçerli bir çift değil.

## <a name="resolution"></a>Çözüm

Makaleniz için `ms.prod` değerinizin doğru olduğunu onaylayın. Sonra geçerli bir `ms.technology` değeri seçin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/whitelists) bulunabilir.

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
